# 🚨 Warden

### An introduction to Warden <a href="#an-introduction-to-warden" id="an-introduction-to-warden"></a>

Warden is the most versatile module that you can find in Defender.\
It allows you to define custom rules by combining a rich set of events, conditions and actions.\
Need to filter messages only in certain channels? Or maybe rename people meeting very specific requirements? Warden got you covered!

#### Rule format: a basic example <a href="#rule-format-a-basic-example" id="rule-format-a-basic-example"></a>

Rules can be written in the YAML language and must be structured in a very specific way to be deemed a valid rule.\
Let's start with a basic scenario: you have an innate fear of spiders and you wish to delete any message that mentions them.\
So, without further ado, you add this rule through `[p]defender warden add`

```
name: spiders-are-spookyrank: 1event: on-messageif:  - message-matches-any: ["*spider*"]do:  - delete-user-message:
```

And now let's break this down.

* `name` is the name of this rule. Every rule that you add will have an unique name to tell them apart. If you try to add a rule with a name that is already registered a confirmation will be asked before proceeding with overwrite.
* `rank` is the highest rank that this rule will target. As explained in `[p]defender status`, Rank 1 is the highest rank there is. This means that every message that is sent will be targeted, even staff's.
* `event` is _when_ this rule will enter into effect. You can find the complete event list below. A rule can also be defined with multiple events by using a list, example: `[on-message, on-message-edit]`
* `if` is the section where the conditions are defined. It supports both basic condition and special condition blocks (we'll get to that later). Every condition (and condition block) must resolve to `true` for the rule's action to be executed.
* `do` is the section where the actions are defined. Actions are ordered and will be executed in the order you have defined them. If one of them errors out for whatever reason, the action's execution will stop. You can monitor errors in `[p]defender monitor`.

The condition `message-matches-any` takes the message in the _context_ and analyzes its content. Here we have put the word spider surrounded by the wildcard `*`: this means that the word spider simply being present in a message is enough for this condition to pass.

As you may have noticed the action `delete-user-message` doesn't need any parameter: it simply deletes the message in the context.

#### Context <a href="#context" id="context"></a>

Events have a context. `on-message` for example, will have `message` and `user` (the message author's) available, so any condition and action that is bound to analyze or take action on a message will be allowed to be used in that rule.\
A rule with the condition `message-matches-any` combined with the event `on-user-join` will be rejected: Warden doesn't have a message to analyze in this event, therefore the rule will be simply deemed invalid.\
Depending on the context you will have certain context variables available: there are some special actions that accept these variables in their parameters.\
Example:\


```
send-mod-log: "No particular reason: I just really dislike $user."
```

If the user in context is called HairySpider#9999 Warden will post a mod-log entry as\


```
No particular reason: I just really dislike HairySpider#9999.
```

#### Defining a more complex rule <a href="#defining-a-more-complex-rule" id="defining-a-more-complex-rule"></a>

This first rule was very basic. What if, instead, we wanted to outright **ban** any user that mentions spiders _OR_ has the word spider in their username/nickname, like our friend HairySpider#9999?\
But, since we are also hindered by a conscience, we want to give new users time to read the #rules channel, so we'll make sure to only punish infidels who are knowingly breaking the rules.\
Finally, the ruling class, staff members, must be free to discuss the enemy of the state without ever getting banned themselves.\
Wow, this got complicated fast huh? Luckily this is where _condition blocks_ come to our aid.

At the time of writing there are three condition blocks:

* `if-any`
* `if-all`
* `if-not`

When a rule is processed, conditions blocks are individually resolved to **true** or **false**.\
For `if-all` to pass, every condition that it contains must be **true**.\
Every condition contained in `if-not` must resolve to **false**.\
And as you can probably guess by now, a single **true** condition inside `if-any` is enough for it to pass.

```
name: spiders-are-spookyrank: 1event: on-messageif:  - if-any:     - username-matches-any: ["*spider*"]     - message-matches-any: ["*spider*"]     - nickname-matches-any: ["*spider*"]  - if-not:     - user-joined-less-than: 2 hours     - is-staff: truedo:  - ban-user-and-delete: 1  - send-mod-log: "Usage of the S word is not welcome in this community. Begone, $user."
```

This is how a condition block is structured: it contains basic conditions.\
In our case here _if_ the author's of a message has the word spider in their username/nickname _OR_ their message contains the word spider _AND_ at the same time hasn't joined less than **2** hours ago and is also not a staff member _then_ they will be banned and all the messages sent by them in the last day will be deleted.\
Additionally, a mod-log entry for this last ban will be posted, condemning the author of this unspeakable crime for everyone to see.\
Our Orwellian quest of never ever allowing the S word to be used in our community again is now completed.

As you can see condition blocks are a nice to have when you need a slightly more complex logic but remember that they're not mandatory, you can choose to use them only when you truly need to.

#### A quick recap <a href="#a-quick-recap" id="a-quick-recap"></a>

Rules are triggered when the specified event takes place.\
The user's rank (if applicable, not every event has a user context) will be matched against the one defined in the rule.\
After that, the conditions will be evaluated and finally, if the conditions have passed, Warden will start processing the actions one by one.\
If any of the actions fail execution will stop and the error will be reported in `[p]defender monitor`.\
Rules can have an order of execution. See advanced features for more informations.

#### Final notes <a href="#final-notes" id="final-notes"></a>

Rules give you complete freedom by design.\
In that last example even _trusted roles_ and _helper roles_ aren't protected: if they pass the conditions they will be targeted by the actions.\
Be careful when you design the logic of a rule with drastic actions such as bans. The parameter **rank** is there to help you protect categories of users: trusted users, helper users and staff will always be immune if you set the rank to at least level 2.

### Advanced features <a href="#advanced-features" id="advanced-features"></a>

#### Execution order <a href="#execution-order" id="execution-order"></a>

The rules that you add do not have any guaranteed order of execution. You can change this, however, for example to make sure that a particular rule is always executed first (or after all your other ordered rules): this is done with the optional `priority` parameter.\
Priority can be a number between 1 and 999. When something happens, Defender gathers all the rules that you have added for that particular event and reorders them based on the priority parameter. Rules that lack a priority parameter will always be executed last, in an unordered manner.\
Defender will not stop you from defining multiple rules with the same priority: this is fine for rules that are for different events as they won't "conflict" with each other, however be mindful of that when you set up prioritized rules for a single event.\
This is how you define a rule with priority:

```
name: always-firstrank: 1priority: 1event: on-messageif:  - message-matches-any: ["*"]do:  - send-to-monitor: "I'm 1st!"
```

#### Heat level <a href="#heat-level" id="heat-level"></a>

Conditions give you a way to have your rules only execute under very specific conditions. However, what if, for example, we want our rule to execute after an user triggered some other rule a defined amount of times? That's where the heat level system comes in handy.\
Imagine that each user has an invisible bar, just like an health bar in videogames, where their heat level is being tracked:

`[____________________]`

This bar can contain a maximum of 100 heat points. Normally it is empty. Through rule actions you can assign points to this bar. Each point has a definite lifetime and you decide how much that is:

`add-user-heatpoint: 10s` (also accepts minutes and hours. Up to 24 hours)\
`[X___________________]`

After 10 seconds have elapsed, the bar will go back to being empty. You can also assign multiple heatpoints at once with the same lifetime:

`add-user-heatpoints: [5, 10m]`\
`[XXXXX_______________]`

And in case you want to empty the bar:\
`empty-user-heat:`

But how do you check for heat points in rules? With conditions:\
`user-heat-is: 5` or\
`user-heat-more-than: 2`

You may want to first assign heatpoints and _then_, in a separate rule, check the heat level. Since rules are normally executed in an unordered manner, remember to use the priority parameter to make sure that your heat-assigning rules are executed first.\
Channels also have heat levels and they work the same way as users'. You can find all the related conditions and actions in the sections below plus some handy examples in their dedicated page.

#### Custom heat level <a href="#custom-heat-level" id="custom-heat-level"></a>

Assuming you've read the previous section before this (please do so!), you may be wondering if you're limited to only two heat levels, per-channel and per-user. What if you want separate heat levels for each different rule, for example?\
This is where _custom_ heat levels can help. They work exactly like channel and user heat levels, except for the fact that you can assign to them the name you want. A few context variables (specifically the IDs and rule name) are also available for extra flexibility.\
Custom heat levels are extremely versatile. To demonstrate the variety of use cases they can used for we'll build a rule specific cooldown using them.

```
rank: 2name: trigger-with-cooldownevent: on-messageif:  - message-matches-any: ["hello"]  - custom-heat-is: ["$rule_name", 0]do:  - add-custom-heatpoint: ["$rule_name", 5 minutes]  - send-message: [$channel_id, "hello $user_mention"]
```

This rule can only be triggered every 5 minutes: as you can see in the actions a single custom heatpoint gets added, making the custom heat level "one" for five minutes. This will make the condition `custom-heat-is` "zero" false, not allowing the rule to be run until the heatpoint expires.

#### Periodic rules <a href="#periodic-rules" id="periodic-rules"></a>

Periodic rules are rules that can be set to run automatically every once in a while. Just like manual rules, they run against the entire server userbase: every user that satisfies its conditions will be affected by it. They can be particularly useful for certain needs, such as enforcing name conventions.\
A simple example:

```
rank: 2name: dehoist-taskevent: [periodic]run-every: 15 minutesif:  - username-matches-any: ["!*"]  - if-not:      - nickname-matches-any: ["*"]do:  - set-user-nickname: "no hoisting"
```

This rule will run every 15 minutes (as defined by the mandatory `run-every` parameter) and will rename every user that has a name starting with an exclamation mark.\
Keep in mind that a bot restart will reset the timer: the rule above, for example, will only run 15 minutes after the bot first starts.

#### Conditional actions <a href="#conditional-actions" id="conditional-actions"></a>

Sometimes you may want to carry on different actions according to certain conditions: this is doable by using conditions (or condition blocks) inside the `do` block. Each condition, or condition block, will equal to `true` or `false` and you can control the flow of the rule with `if-true` and `if-false`.

```
# Replies with pong when the user says ping, and viceversarank: 1name: ping-pongevent: [on-message]if:  - message-matches-any: ["ping", "pong"]do:  - compare: ["$message", "contains-pattern", "ping"]  - if-true:      - send-message: [$channel_id, "pong"]  - if-false:     - send-message: [$channel_id, "ping"]
```

```
rank: 3name: filterevent: on-messageif:  - message-matches-any: ["*bad*", "*words*"]do:  - add-custom-heatpoint: ["filter-$user_id", 5 minutes]  - custom-heat-more-than: ["filter-$user_id", 4] # check if the user triggered this rule 5 or more times  - if-true: # if they did, ban them      - ban-user-and-delete: 0  - delete-user-message: # and proceed to delete the message in any case, ban or not
```

#### Nesting <a href="#nesting" id="nesting"></a>

Starting from Defender v1.12 you can make rules with nested condition blocks. This allows to define conditions with much greater complexity.\
An example:

```
rank: 1name: dehoisterevent: [periodic, on-user-join]run-every: 5 minutesif:  - is-staff: false # Ignore staff members  - if-any: # Check if the user has either...     - nickname-matches-any: ["!*"] # (A) a hoisting nickname     - if-all:        - username-matches-any: ["!*"] # (B1) or a hoisting username ...        - if-not:            - nickname-matches-any: ["*"] # ... (B2) with no nickname already set  - if-not: # They also need NOT to be...     - user-has-any-role-in: ["Patron"] # (1) ... a Patron member     - nickname-matches-any: ["dehoisted"] # (2) ... and not already dehoisteddo:  - set-user-nickname: "dehoisted"
```

### Events <a href="#events" id="events"></a>

| Event                | When                                                                                                                                                                                        | Context       |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| `on-message`         | A new message is sent                                                                                                                                                                       | message, user |
| `on-message-edit`    | A message is edited                                                                                                                                                                         | message, user |
| `on-message-delete`  | A message is deleted                                                                                                                                                                        | message, user |
| `on-user-join`       | A new user joins the server                                                                                                                                                                 | user          |
| `on-user-leave`      | A user leaves the server                                                                                                                                                                    | user          |
| `on-role-add`        | A role is assigned to a user                                                                                                                                                                | user          |
| `on-role-remove`     | A role is removed from a user                                                                                                                                                               | user          |
| `on-reaction-add`    | A user added a reaction                                                                                                                                                                     | message, user |
| `on-reaction-remove` | A reaction is removed from a message. 'User' will always be the messages' original author.                                                                                                  | message, user |
| `on-emergency`       | The server enters a state of emergency, either automatic or manual                                                                                                                          | none          |
| `manual`             | The rule is manually run by an admin with `[p]defender warden run`                                                                                                                          | user          |
| `periodic`           | <p>The rule runs periodically, as defined by its own <code>run-every</code> parameter.<br>The interval can be set between 5 minutes and 24 hours.<br>See more info about periodic rules</p> | user          |

Important

The reaction events only work for cached messages. This means that messages that are too old or predate your bot's last boot will not trigger these events. Events that work for non cached messages may be added in a future update.

### Deprecated syntax <a href="#deprecated-syntax" id="deprecated-syntax"></a>

The following syntax is deprecated: while there are currently no plans to remove old Warden syntax it is recommended that you switch to the recommended alternatives as soon as possible. It is not possible to create new rules with deprecated syntax.

* `send-dm`, `dm-user`, `send-to-channel`, `send-in-channel` replaced by `send-message`
* `notify-staff-and-ping`, `notify-staff-with-embed` replaced by `notify-staff`

### Context variables <a href="#context-variables" id="context-variables"></a>

| Context variable           | Description                                                                    |
| -------------------------- | ------------------------------------------------------------------------------ |
| `$rule_name`               | The rule's name                                                                |
| `$notification_channel_id` | The notification channel ID for the server                                     |
| `$guild`                   | The guild's name                                                               |
| `$guild_id`                | The guild's ID                                                                 |
| `$guild_icon_url`          | The guild's icon url                                                           |
| `$guild_banner_url`        | The guild's banner url                                                         |
| `$user`                    | The user's name + the discriminator                                            |
| `$user_name`               | The user's name                                                                |
| `$user_display`            | The user's name or nickname, if one is set                                     |
| `$user_id`                 | The user's ID                                                                  |
| `$user_mention`            | The user's mention                                                             |
| `$user_avatar_url`         | The user avatar's url                                                          |
| `$user_nickname`           | The user's nickname. "None" if not set                                         |
| `$user_created_at`         | The date and time in which the user created the account                        |
| `$user_joined_at`          | The date and time in which the user joined the server                          |
| `$user_heat`               | The user's heat level                                                          |
| `$message`                 | The raw message content. Mentions are automatically escaped                    |
| `$message_clean`           | The message content. Mentions are transformed into the way the client shows it |
| `$message_id`              | The message's ID                                                               |
| `$message_created_at`      | The date and time in which the message was created                             |
| `$message_link`            | The URL pointing to the message                                                |
| `$message_reaction`        | In a `on-reaction-*` event this contains the reaction that triggered it        |
| `$attachment_filename`     | The message attachment's filename, if any                                      |
| `$attachment_url`          | The message attachment's url, if any                                           |
| `$channel`                 | The channel's name in the form of #channel\_name                               |
| `$channel_name`            | The channel's name                                                             |
| `$channel_id`              | The channel's ID                                                               |
| `$channel_mention`         | The channel's mention                                                          |
| `$channel_category`        | The channel category's name, if any                                            |
| `$channel_category_id`     | The channel category's id, if any                                              |
| `$channel_heat`            | The channel's heat level                                                       |
| `$role_id`                 | The role's id in a `on-role-*` event                                           |
| `$role_name`               | The role's name in a `on-role-*` event                                         |
| `$role_mention`            | The role's mention in a `on-role-*` event                                      |
| `$role_added`              | Equals to 'true' in `on-role-add`, 'false' in `on-role-remove`                 |

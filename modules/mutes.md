# 🔇 Mutes

### Usage[¶](broken-reference)

Mute users temporarily or indefinitely.

### Commands[¶](broken-reference)

#### activemutes[¶](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

**Description**

Displays active mutes on this server.

#### mute[¶](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

```
[p]mute <users...> [time_and_reason]
```

**Description**

Mute users.

Examples:

* `[p]mute @member1 @member2 spam 5 hours`
* `[p]mute @member1 3 days`

**Arguments**

* `<users...>`: A space separated list of usernames, ID’s, or mentions.
* `[time_and_reason]`: The time and reason. If no time is provided, the mute will use the default set time or indefinite if this hasn’t been configured.

#### mutechannel[¶](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

```
[p]mutechannel <users...> [time_and_reason]
```

**Description**

Mute a user in the current text channel.

Examples:

* `[p]mutechannel @member1 @member2 spam 5 hours`
* `[p]mutechannel @member1 3 days`

**Arguments**

* `<users...>`: A space separated list of usernames, ID’s, or mentions.
* `[time_and_reason]`: The time and reason. If no time is provided, the mute will use the default set time or indefinite if this hasn’t been configured.

#### muteset[¶](broken-reference)

**Syntax**

**Description**

Mute settings.

**muteset defaulttime**[**¶**](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

```
[p]muteset defaulttime [time]
```

**Description**

Set the default mute time for the mute command.

If no time interval is provided this will be cleared.

**Arguments**

* `[time]`: The length of time for a default mute.

**muteset forcerole**[**¶**](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

```
[p]muteset forcerole <true_or_false>
```

**Description**

Whether or not to force role only mutes on the bot.

**Arguments**

* `<true_or_false>`: Whether to enable or disable this setting, must provide `true` or `false`.

**muteset makerole**[**¶**](broken-reference)

**Syntax**

```
[p]muteset makerole <name>
```

**Description**

Create a Muted role.

This will create a role and apply overwrites to all available channels to more easily setup muting a user.

If you already have a muted role created on the server use `[p]muteset role ROLE_NAME_HERE`

**Arguments**

* `<name>`: The name of the muted role to create.

**muteset notification**[**¶**](broken-reference)

**Syntax**

```
[p]muteset notification [channel]
```

**Description**

Set the notification channel for automatic unmute issues.

If no channel is provided this will be cleared and notifications about issues when unmuting users will not be sent anywhere.

**Arguments**

* `[channel]`: The channel to receive unmute issue updates. You can either mention the channel, provide its exact name or its ID.

**muteset role**[**¶**](broken-reference)

**Syntax**

**Description**

Sets the role to be applied when muting a user.

If no role is setup the bot will attempt to mute a user by setting channel overwrites in all channels to prevent the user from sending messages.

Note

If no role is setup a user may be able to leave the server and rejoin no longer being muted.

**Arguments**

* `[role]`: The role for muted users to receive. Please give **the exact role name or ID**, or it won’t be detected.

**muteset senddm**[**¶**](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

```
[p]muteset senddm <true_or_false>
```

**Description**

Set whether mute notifications should be sent to users in DMs.

**Arguments**

* `<true_or_false>`: Whether to enable or disable this setting, must provide `true` or `false`.

**muteset settings**[**¶**](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

Tip

Alias: `muteset showsettings`

**Description**

Shows the current mute settings for this guild.

**muteset showmoderator**[**¶**](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

```
[p]muteset showmoderator <true_or_false>
```

**Description**

Decide whether the name of the moderator muting a user should be included in the DM to that user.

**Arguments**

* `<true_or_false>`: Whether to enable or disable this setting, must provide `true` or `false`.

#### unmute[¶](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

```
[p]unmute <users...> [reason]
```

**Description**

Unmute users.

**Arguments**

* `<users...>`: A space separated list of usernames, ID’s, or mentions.
* `[reason]`: The reason for the unmute.

#### unmutechannel[¶](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

```
[p]unmutechannel <users...> [reason]
```

**Description**

Unmute a user in this channel.

**Arguments**

* `<users...>`: A space separated list of usernames, ID’s, or mentions.
* `[reason]`: The reason for the unmute.

#### voicemute[¶](broken-reference)

**Syntax**

```
[p]voicemute <users...> [reason]
```

**Description**

Mute a user in their current voice channel.

Examples:

* `[p]voicemute @member1 @member2 spam 5 hours`
* `[p]voicemute @member1 3 days`

**Arguments**

* `<users...>`: A space separated list of usernames, ID’s, or mentions.
* `[time_and_reason]`: The time and reason. If no time is provided, the mute will use the default set time or indefinite if this hasn’t been configured.

#### voiceunmute[¶](broken-reference)

**Syntax**

```
[p]voiceunmute <users...> [reason]
```

**Description**

Unmute a user in their current voice channel.

**Arguments**

* `<users...>`: A space separated list of usernames, ID’s, or mentions.
* `[reason]`: The reason for the unmute

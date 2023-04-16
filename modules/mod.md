# ⚒ Mod

### Usage[¶](broken-reference)

A range of highly customizable moderation tools used to protect your guild from users who cannot follow the rules.

### Commands[¶](broken-reference)

#### ban[¶](broken-reference)

**Syntax**

```
[p]ban <user> [days] [reason]
```

**Description**

Ban a user from this server and optionally delete days of messages.

`days` is the amount of days of messages to cleanup on ban.

**Arguments**

* `<user>`: The user to ban. You can either provide the member’s ID or their exact name with the tag or not.
* `[days]`: The amount of days of messages to cleanup on ban. This parameter defaults to the defaultdays setting, or no days if this has not yet been configured.
* `[reason]`: The reason why the user was banned (optional).

**Example Usage**

*   `[p]ban 428675506947227648 7 Continued to spam after told to stop.`

    This will ban the user with ID 428675506947227648 and it will delete 7 days worth of messages.
*   `[p]ban @Twentysix 7 Continued to spam after told to stop.`

    This will ban Twentysix and it will delete 7 days worth of messages.

A user ID should be provided if the user is not a member of this server. If days is not a number, it’s treated as the first word of the reason. Minimum 0 days, maximum 7. If not specified, the defaultdays setting will be used instead.

#### kick[¶](broken-reference)

**Syntax**

```
[p]kick <member> [reason]
```

**Description**

Kick a user.

**Arguments**

* `<member>`: The member to kick. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname.
* `[reason]`: The reason why the user was kicked (optional).

**Example Usage**

*   `[p]kick 428675506947227648 wanted to be kicked.`

    This will kick the user with ID 428675506947227648 from the server.
*   `[p]kick @Twentysix wanted to be kicked.`

    This will kick Twentysix from the server.

If a reason is specified, it will be the reason that shows up in the audit log.

#### massban[¶](broken-reference)

**Syntax**

```
[p]massban <user_ids...> [days] [reason]
```

**Description**

Mass bans user(s) from the server.

**Arguments**

* `<user_ids...>`: The users to ban. This must be a list of user IDs separated by spaces.
* `[days]`: The amount of days of messages to cleanup on massban.
* `[reason]`: The reason why these users were banned.

**Example Usage**

*   `[p]massban 345628097929936898 57287406247743488 7 they broke all rules.`

    This will ban all the added userids and delete 7 days worth of their messages.

#### modset[¶](broken-reference)

**Syntax**

**Description**

Manage server administration settings.

**modset defaultdays**[**¶**](broken-reference)

**Syntax**

```
[p]modset defaultdays [days=0]
```

**Description**

Set the default number of days worth of messages to be deleted when a user is banned.

The number of days must be between 0 and 7.

**Arguments**

* `[days=0]`: The default number of days of messages to be deleted when a user is banned.

Note

This value must be between 0 and 7.

**modset defaultduration**[**¶**](broken-reference)

**Syntax**

```
[p]modset defaultduration <duration>
```

**Description**

Set the default time to be used when a user is tempbanned.

Accepts: seconds, minutes, hours, days, weeks

**Arguments**

* `<duration>`: The default duration for when a user is temporarily banned. Accepts seconds, minutes, hours, days or weeks.

**Example Usage**

* `[p]modset defaultduration 7d12h10m`
* `[p]modset defaultduration 7 days 12 hours 10 minutes`

**modset deletenames**[**¶**](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

```
[p]modset deletenames [confirmation=False]
```

**Description**

Delete all stored usernames and nicknames.

**Arguments**

* `<confirmation>`: Whether to delete all stored usernames and nicknames. You should provide either ‘true’ or ‘false’.

**modset deleterepeats**[**¶**](broken-reference)

**Syntax**

```
[p]modset deleterepeats [repeats]
```

**Description**

Enable auto-deletion of repeated messages.

**Arguments**

* `[repeats]`: The number of repeated messages needed before further messages are deleted.

Note

Must be between 2 and 20. Set to -1 to disable this feature.

**modset dm**[**¶**](broken-reference)

**Syntax**

**Description**

Toggle whether a message should be sent to a user when they are kicked/banned.

If this option is enabled, the bot will attempt to DM the user with the guild name and reason as to why they were kicked/banned.

**Arguments**

* `[enabled]`: Whether a message should be sent to a user when they are kicked/banned. You should provide either ‘true’ or ‘false’.

**modset hierarchy**[**¶**](broken-reference)

**Syntax**

**Description**

Toggle role hierarchy check for mods and admins.

Warning

Disabling this setting will allow mods to take actions on users above them in the role hierarchy!

This is enabled by default.

**modset mentionspam**[**¶**](broken-reference)

**Syntax**

**Description**

Manage the automoderation settings for mentionspam.

**modset mentionspam ban**[**¶**](broken-reference)

**Syntax**

```
[p]modset mentionspam ban <max_mentions>
```

**Description**

Set the autoban conditions for mention spam.

Users will be banned if they send any message which contains more than `<max_mentions>` mentions.

**Arguments**

* `<max_mentions>`: Must be 0 or greater. Set to 0 to disable this feature.

**modset mentionspam kick**[**¶**](broken-reference)

**Syntax**

```
[p]modset mentionspam kick <max_mentions>
```

**Description**

Set the autokick conditions for mention spam.

Users will be kicked if they send any message which contains more than `<max_mentions>` mentions.

**Arguments**

* `<max_mentions>`: Must be 0 or greater. Set to 0 to disable this feature.

**modset mentionspam strict**[**¶**](broken-reference)

**Syntax**

```
[p]modset mentionspam strict [enabled]
```

**Description**

Setting to account for duplicate mentions.

If enabled all mentions will count including duplicated mentions. If disabled only unique mentions will count.

Use this command without any parameter to see the current setting.

**Arguments**

* `[enabled]`: Whether all mentions will count, including duplicated mentions. You should provide either ‘true’ or ‘false’.

**modset mentionspam warn**[**¶**](broken-reference)

**Syntax**

```
[p]modset mentionspam warn <max_mentions>
```

**Description**

Sets the autowarn conditions for mention spam.

Users will be warned if they send any messages which contain more than `<max_mentions>` mentions.

**Arguments**

* `<max_mentions>`: Must be 0 or greater. Set to 0 to disable this feature.

**modset reinvite**[**¶**](broken-reference)

**Syntax**

**Description**

Toggle whether an invite will be sent to a user when unbanned.

If this is True, the bot will attempt to create and send a single-use invite to the newly-unbanned user.

**modset showsettings**[**¶**](broken-reference)

**Syntax**

**Description**

Show the current server administration settings.

**modset trackallnames**[**¶**](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

```
[p]modset trackallnames [enabled]
```

**Description**

Toggle whether all name changes should be tracked.

Toggling this off also overrides the tracknicknames setting.

**Arguments**

* `[enabled]`: Whether all name changes should be tracked. You should provide either ‘true’ or ‘false’.

**modset tracknicknames**[**¶**](broken-reference)

**Syntax**

```
[p]modset tracknicknames [enabled]
```

**Description**

Toggle whether nickname changes should be tracked.

This setting will be overridden if trackallnames is disabled.

**Arguments**

* `[enabled]`: Whether all nickname changes should be tracked. You should provide either ‘true’ or ‘false’.

#### movedeletedelay[¶](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

**Description**

Move deletedelay settings to core

#### moveignoredchannels[¶](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

**Description**

Move ignored channels and servers to core

#### names[¶](broken-reference)

**Syntax**

**Description**

Show previous names and nicknames of a member.

**Arguments**

* `<member>`: You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname.

#### rename[¶](broken-reference)

**Syntax**

```
[p]rename <member> [nickname]
```

**Description**

Change a member’s nickname.

Leaving the nickname empty will remove it.

**Arguments**

* `<member>`: You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname.
* `[nickname]`: The new nickname for the member.

#### slowmode[¶](broken-reference)

**Syntax**

```
[p]slowmode [interval=0:00:00]
```

**Description**

Changes channel’s slowmode setting.

Interval can be anything from 0 seconds to 6 hours. Use without parameters to disable.

**Arguments**

* `[interval=0:00:00]`: The time for the channel’s slowmode settings.

Note

Interval can be anything from 0 seconds to 6 hours. Use without parameters to disable.

#### softban[¶](broken-reference)

**Syntax**

```
[p]softban <member> [reason]
```

**Description**

Kick a member and delete 1 day’s worth of their messages.

**Arguments**

* `<member>`: The member to softban. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname enclosed in quotes if there are spaces.
* `[reason]`: Reason for the kick (optional).

#### tempban[¶](broken-reference)

**Syntax**

```
[p]tempban <member> [duration] [days] [reason]
```

**Description**

Temporarily ban a user from this server.

**Arguments**

* `<member>`: The member to temporarily ban. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname enclosed in quotes if there are spaces.
* `[duration]`: The amount of time the user should be banned for.
* `[days]`: The amount of days of messages to cleanup on tempban.
* `[reason]`: The reason for the tempban (optional).

**Example Usage**

*   `[p]tempban @Twentysix Because I say so`

    This will ban Twentysix for the default amount of time set by an administrator.
*   `[p]tempban @Twentysix 15m You need a timeout`

    This will ban Twentysix for 15 minutes.
*   `[p]tempban 428675506947227648 1d2h15m 5 Evil person`

    This will ban the user with ID 428675506947227648 for 1 day 2 hours 15 minutes and will delete the last 5 days of their messages.

#### unban[¶](broken-reference)

**Syntax**

```
[p]unban <user_id> [reason]
```

**Description**

Unban a user from this server.

**Arguments**

* `<user_id>`: You can either provide the member’s ID or their exact name with the tag or not.
* `[reason]`: The reason for the unban (optional).

#### userinfo[¶](broken-reference)

**Syntax**

**Description**

Show information about a user.

This includes fields for status, discord join date, server join date, voice state and previous names/nicknames.

If the user has no roles, previous names or previous nicknames, these fields will be omitted.

**Arguments**

* `[member]`: You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname.

#### voiceban[¶](broken-reference)

**Syntax**

```
[p]voiceban <member> [reason]
```

**Description**

Ban a user from speaking and listening in the server’s voice channels.

**Arguments**

* `<member>`: The member to ban from voice. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname.
* `[reason]`: The reason for the voiceban (optional).

#### voicekick[¶](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

```
[p]voicekick <member> [reason]
```

**Description**

Kick a member from a voice channel.

**Arguments**

* `<member>`: You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname.
* `[reason]`: The reason for the voicekick (optional).

#### voiceunban[¶](broken-reference)

**Syntax**

```
[p]voiceunban <member> [reason]
```

**Description**

Unban a user from speaking and listening in the server’s voice channels.

**Arguments**

* `<member>`: The member to unban from voice. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname enclosed in quotes if there are spaces.
* `[reason]`: The reason for the voiceunban (optional).

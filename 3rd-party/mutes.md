---
description: Temporarily or permanently remove a user's text or voice ability.
---

# Mutes

## voicemute

* Usage: `!voicemute <users> [time_and_reason]`
* Checks: `server_only`

Mute a user in their current voice channel.\
\
\<users...> is a space separated list of usernames, ID's, or mentions.\
\[time\_and\_reason] is the time to mute for and reason. Time is\
any valid time length such as 30 minutes or 2 days. If nothing\
is provided the mute will use the set default time or indefinite if not set.\
\
Examples:\
!voicemute @member1 @member2 spam 5 hours\
!voicemute @member1 3 days

## voiceunmute

* Usage: `!voiceunmute <users> [reason]`
* Checks: `server_only`

Unmute a user in their current voice channel.\
\
\<users...> is a space separated list of usernames, ID's, or mentions.\
\[reason] is the reason for the unmute.

## muteset

* Usage: `!muteset`
* Checks: `server_only`

Mute settings.

### muteset role

* Usage: `!muteset role [role]`
* Restricted to: `ADMIN`
* Checks: `bot_has_server_permissions`

Sets the role to be applied when muting a user.\
\
If no role is setup the bot will attempt to mute a user by setting\
channel overwrites in all channels to prevent the user from sending messages.\
\
Note: If no role is setup a user may be able to leave the server\
and rejoin no longer being muted.

### muteset settings

* Usage: `!muteset settings`
* Restricted to: `MOD`
* Aliases: `showsettings`

Shows the current mute settings for this server.

### muteset makerole

* Usage: `!muteset makerole <name>`
* Restricted to: `ADMIN`
* Checks: `bot_has_server_permissions`

Create a Muted role.\
\
This will create a role and apply overwrites to all available channels\
to more easily setup muting a user.\
\
If you already have a muted role created on the server use\
!muteset role ROLE\_NAME\_HERE

### muteset defaulttime

* Usage: `!muteset defaulttime [time]`
* Restricted to: `MOD`
* Aliases: `time`

Set the default mute time for the mute command.\
\
If no time interval is provided this will be cleared.

### muteset senddm

* Usage: `!muteset senddm <true_or_false>`
* Restricted to: `MOD`
* Checks: `server_only`

Set whether mute notifications should be sent to users in DMs.

### muteset showmoderator

* Usage: `!muteset showmoderator <true_or_false>`
* Restricted to: `MOD`
* Checks: `server_only`

Decide whether the name of the moderator muting a user should be included in the DM to that user.

### muteset notification

* Usage: `!muteset notification [channel=None]`
* Restricted to: `ADMIN`

Set the notification channel for automatic unmute issues.\
\
If no channel is provided this will be cleared and notifications\
about issues when unmuting users will not be sent anywhere.

## activemutes

* Usage: `!activemutes`
* Restricted to: `MOD`
* Checks: `server_only`

Displays active mutes on this server.

## mute

* Usage: `!mute <users> [time_and_reason]`
* Restricted to: `MOD`
* Checks: `server_only`

Mute users.\
\
\<users...> is a space separated list of usernames, ID's, or mentions.\
\[time\_and\_reason] is the time to mute for and reason. Time is\
any valid time length such as 30 minutes or 2 days. If nothing\
is provided the mute will use the set default time or indefinite if not set.\
\
Examples:\
!mute @member1 @member2 spam 5 hours\
!mute @member1 3 days

## mutechannel

* Usage: `!mutechannel <users> [time_and_reason]`
* Restricted to: `MOD`
* Aliases: `channelmute`
* Checks: `bot_has_server_permissions`

Mute a user in the current text channel (or in the parent of the current thread).\
\
\<users...> is a space separated list of usernames, ID's, or mentions.\
\[time\_and\_reason] is the time to mute for and reason. Time is\
any valid time length such as 30 minutes or 2 days. If nothing\
is provided the mute will use the set default time or indefinite if not set.\
\
Examples:\
!mutechannel @member1 @member2 spam 5 hours\
!mutechannel @member1 3 days

## unmute

* Usage: `!unmute <users> [reason]`
* Restricted to: `MOD`
* Checks: `server_only`

Unmute users.\
\
\<users...> is a space separated list of usernames, ID's, or mentions.\
\[reason] is the reason for the unmute.

## unmutechannel

* Usage: `!unmutechannel <users> [reason]`
* Restricted to: `MOD`
* Aliases: `channelunmute`
* Checks: `bot_has_server_permissions`

Unmute a user in this channel (or in the parent of this thread).\
\
\<users...> is a space separated list of usernames, ID's, or mentions.\
\[reason] is the reason for the unmute.

---
description: Learn how to take moderative action using Sentri
---

# Moderating

## timeout

* Usage: `!timeout <member_or_role> [time=None] [reason]`
* Restricted to: `MOD`
* Aliases: `tt`
* Cooldown: `1 per 1.0 second`
* Checks: `server_only`

Timeout users.\
\
\<member\_or\_role> is the username/rolename, ID or mention. If provided a role,\
everyone with that role will be timedout.\
\[time] is the time to mute for. Time is any valid time length such as 45 minutes\
or 3 days. If nothing is provided the timeout will be 60 seconds default.\
\[reason] is the reason for the timeout. Defaults to None if nothing is provided.\
\
Examples:\
!timeout @member 5m talks too much\
!timeout @member 10m

## untimeout

* Usage: `!untimeout <member_or_role> [reason]`
* Restricted to: `MOD`
* Aliases: `utt`
* Cooldown: `1 per 1.0 second`
* Checks: `server_only`

Untimeout users.\
\
\<member\_or\_role> is the username/rolename, ID or mention. If\
provided a role, everyone with that role will be untimed.\
\[reason] is the reason for the untimeout. Defaults to None\
if nothing is provided.



## slowmode

* Usage: `!slowmode [interval]`
* Checks: `bot_can_manage_channel and server_only`

Changes thread's or text channel's slowmode setting.\
\
Interval can be anything from 0 seconds to 6 hours.\
Use without parameters to disable.

## rename

* Usage: `!rename <member> [nickname]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Change a member's server nickname.\
\
Leaving the nickname argument empty will remove it.

## userinfo

* Usage: `!userinfo [member]`
* Checks: `server_only`

Show information about a member.\
\
This includes fields for status, discord join date, server\
join date, voice state and previous usernames/global display names/nicknames.\
\
If the member has no roles, previous usernames, global display names, or server nicknames,\
these fields will be omitted.

## names

* Usage: `!names <member>`

Show previous usernames, global display names, and server nicknames of a member.

## kick

* Usage: `!kick <member> [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Kick a user.\
\
Examples:\
\- !kick 428675506947227648 wanted to be kicked.\
This will kick the user with ID 428675506947227648 from the server.\
\- !kick @Twentysix wanted to be kicked.\
This will kick Twentysix from the server.\
\
If a reason is specified, it will be the reason that shows up\
in the audit log.

## ban

* Usage: `!ban <user> [days=None] [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Ban a user from this server and optionally delete days of messages.\
\
days is the amount of days of messages to cleanup on ban.\
\
Examples:\
\- !ban 428675506947227648 7 Continued to spam after told to stop.\
This will ban the user with ID 428675506947227648 and it will delete 7 days worth of messages.\
\- !ban @Twentysix 7 Continued to spam after told to stop.\
This will ban Twentysix and it will delete 7 days worth of messages.\
\
A user ID should be provided if the user is not a member of this server.\
If days is not a number, it's treated as the first word of the reason.\
Minimum 0 days, maximum 7. If not specified, the defaultdays setting will be used instead.

## massban

* Usage: `!massban <user_ids> [days=None] [reason]`
* Restricted to: `ADMIN`
* Aliases: `hackban`
* Checks: `server_only`

Mass bans user(s) from the server.\
\
days is the amount of days of messages to cleanup on massban.\
\
Example:\
\- !massban 345628097929936898 57287406247743488 7 they broke all rules.\
This will ban all the added userids and delete 7 days worth of their messages.\
\
User IDs need to be provided in order to ban\
using this command.

## tempban

* Usage: `!tempban <member> [duration=None] [days=None] [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Temporarily ban a user from this server.\
\
duration is the amount of time the user should be banned for.\
days is the amount of days of messages to cleanup on tempban.\
\
Examples:\
\- !tempban @Twentysix Because I say so\
This will ban Twentysix for the default amount of time set by an administrator.\
\- !tempban @Twentysix 15m You need a timeout\
This will ban Twentysix for 15 minutes.\
\- !tempban 428675506947227648 1d2h15m 5 Evil person\
This will ban the user with ID 428675506947227648 for 1 day 2 hours 15 minutes and will delete the last 5 days of their messages.

## softban

* Usage: `!softban <member> [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Kick a user and delete 1 day's worth of their messages.

## voicekick

* Usage: `!voicekick <member> [reason]`
* Restricted to: `MOD`
* Checks: `server_only`

Kick a member from a voice channel.

## voiceunban

* Usage: `!voiceunban <member> [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Unban a user from speaking and listening in the server's voice channels.

## voiceban

* Usage: `!voiceban <member> [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Ban a user from speaking and listening in the server's voice channels.

## unban

* Usage: `!unban <user_id> [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Unban a user from this server.\
\
Requires specifying the target user's ID. To find this, you may either:\
1\. Copy it from the mod log case (if one was created), or\
2\. Enable Developer Mode, go to Bans in this server's settings, right-click the user and select 'Copy ID'.

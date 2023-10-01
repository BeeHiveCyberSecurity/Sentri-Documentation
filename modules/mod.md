---
description: >-
  A range of highly customizable moderation tools used to protect your guild
  from users who cannot follow the rules.
---

# ⚒ Mod

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

Change a member's nickname.\
\
Leaving the nickname empty will remove it.

## userinfo

* Usage: `!userinfo [member]`
* Checks: `server_only`

Show information about a member.\
\
This includes fields for status, discord join date, server\
join date, voice state and previous names/nicknames.\
\
If the member has no roles, previous names or previous nicknames,\
these fields will be omitted.

## names

* Usage: `!names <member>`

Show previous names and nicknames of a member.

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

## modset

* Usage: `!modset`
* Restricted to: `GUILD_OWNER`

Manage server administration settings.

### modset banmessage

* Usage: `!modset banmessage <message>`
* Checks: `server_only`

Set the message sent when a user is banned.\
\
Available placeholders:\
{user} - member that was banned.\
{moderator} - moderator that banned the member.\
{reason} - reason for the ban.\
{server} - server name.\
{days} - number of days of messages deleted.

### modset dm

* Usage: `!modset dm [enabled=None]`
* Checks: `server_only`

Toggle whether a message should be sent to a user when they are kicked/banned.\
\
If this option is enabled, the bot will attempt to DM the user with the server name\
and reason as to why they were kicked/banned.

### modset showmessages

* Usage: `!modset showmessages`

Show the current messages for moderation commands.

### modset mentionspam

* Usage: `!modset mentionspam`
* Checks: `server_only`

Manage the automoderation settings for mentionspam.

#### modset mentionspam kick

* Usage: `!modset mentionspam kick <max_mentions>`
* Checks: `server_only`

Sets the autokick conditions for mention spam.\
\
Users will be kicked if they send any messages which contain more than\
\<max\_mentions> mentions.\
\
\<max\_mentions> Must be 0 or greater. Set to 0 to disable this feature.

#### modset mentionspam warn

* Usage: `!modset mentionspam warn <max_mentions>`
* Checks: `server_only`

Sets the autowarn conditions for mention spam.\
\
Users will be warned if they send any messages which contain more than\
\<max\_mentions> mentions.\
\
\<max\_mentions> Must be 0 or greater. Set to 0 to disable this feature.

#### modset mentionspam strict

* Usage: `!modset mentionspam strict [enabled=None]`
* Checks: `server_only`

Setting to account for duplicate mentions.\
\
If enabled all mentions will count including duplicated mentions.\
If disabled only unique mentions will count.\
\
Use this command without any parameter to see current setting.

#### modset mentionspam ban

* Usage: `!modset mentionspam ban <max_mentions>`
* Checks: `server_only`

Set the autoban conditions for mention spam.\
\
Users will be banned if they send any message which contains more than\
\<max\_mentions> mentions.\
\
\<max\_mentions> Must be 0 or greater. Set to 0 to disable this feature.

### modset kickmessage

* Usage: `!modset kickmessage <message>`
* Checks: `server_only`

Set the message sent when a user is kicked.\
\
Available placeholders:\
{user} - member that was kicked.\
{moderator} - moderator that kicked the member.\
{reason} - reason for the kick.\
{server} - server name.

### modset defaultdays

* Usage: `!modset defaultdays [days=0]`
* Checks: `server_only`

Set the default number of days worth of messages to be deleted when a user is banned.\
\
The number of days must be between 0 and 7.

### modset reinvite

* Usage: `!modset reinvite`
* Checks: `server_only`

Toggle whether an invite will be sent to a user when unbanned.\
\
If this is True, the bot will attempt to create and send a single-use invite\
to the newly-unbanned user.

### modset hierarchy

* Usage: `!modset hierarchy`
* Checks: `server_only`

Toggle role hierarchy check for mods and admins.\
\
**WARNING**: Disabling this setting will allow mods to take\
actions on users above them in the role hierarchy!\
\
This is enabled by default.

### modset tempbanmessage

* Usage: `!modset tempbanmessage <message>`
* Checks: `server_only`

Set the message sent when a user is tempbanned.\
\
Available placeholders:\
{user} - member that was tempbanned.\
{moderator} - moderator that tempbanned the member.\
{reason} - reason for the tempban.\
{server} - server name.\
{days} - number of days of messages deleted.\
{duration} - duration timedelta of the tempban.

### modset defaultduration

* Usage: `!modset defaultduration <duration>`
* Checks: `server_only`

Set the default time to be used when a user is tempbanned.\
\
Accepts: seconds, minutes, hours, days, weeks\
duration must be greater than zero.\
\
Examples:\
!modset defaultduration 7d12h10m\
!modset defaultduration 7 days 12 hours 10 minutes

### modset tracknicknames

* Usage: `!modset tracknicknames [enabled=None]`
* Checks: `server_only`

Toggle whether nickname changes should be tracked.\
\
This setting will be overridden if trackallnames is disabled.

### modset unbanmessage

* Usage: `!modset unbanmessage <message>`
* Checks: `server_only`

Set the message sent when a user is unbanned.\
\
Available placeholders:\
{user} - member that was unbanned.\
{moderator} - moderator that unbanned the member.\
{reason} - reason for the unban.\
{server} - server name.

### modset deleterepeats

* Usage: `!modset deleterepeats [repeats=None]`
* Checks: `server_only`

Enable auto-deletion of repeated messages.\
\
Must be between 2 and 20.\
\
Set to -1 to disable this feature.

### modset showsettings

* Usage: `!modset showsettings`

Show the current server administration settings.

## kick (Hybrid Command)

* Usage: `!kick <member> [reason]`
* Slash Usage: `/kick <member> [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Kick a user.\
Examples:\
\- !kick 428675506947227648 wanted to be kicked.\
This will kick the user with ID 428675506947227648 from the server.\
\- !kick @Twentysix wanted to be kicked.\
This will kick Twentysix from the server.\
If a reason is specified, it will be the reason that shows up\
in the audit log.

## tempban (Hybrid Command)

* Usage: `!tempban <member> [duration=None] [days=None] [reason]`
* Slash Usage: `/tempban <member> [duration=None] [days=None] [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Temporarily ban a user from this server.\
duration is the amount of time the user should be banned for.\
days is the amount of days of messages to cleanup on tempban.\
Examples:\
\- !tempban @Twentysix Because I say so\
This will ban Twentysix for the default amount of time set by an administrator.\
\- !tempban @Twentysix 15m You need a timeout\
This will ban Twentysix for 15 minutes.\
\- !tempban 428675506947227648 1d2h15m 5 Evil person\
This will ban the user with ID 428675506947227648 for 1 day 2 hours 15 minutes and will delete the last 5 days of their messages.

## softban (Hybrid Command)

* Usage: `!softban <member> [reason]`
* Slash Usage: `/softban <member> [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Kick a user and delete 1 day's worth of their messages.

## ban (Hybrid Command)

* Usage: `!ban <user> [days=None] [reason]`
* Slash Usage: `/ban <user> [days=None] [reason]`
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

## unban (Hybrid Command)

* Usage: `!unban <user_id> [reason]`
* Slash Usage: `/unban <user_id> [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Unban a user from this server.\
Requires specifying the target user's ID. To find this, you may either:\
1\. Copy it from the mod log case (if one was created), or\
2\. enable developer mode, go to Bans in this server's settings, right-\
click the user and select 'Copy ID'.\
\
A mod note cog for moderators to add notes to users

## modnoteset

* Usage: `!modnoteset`
* Restricted to: `ADMIN`

Setup modnotes

### modnoteset usemodlog

* Usage: `!modnoteset usemodlog <toggle>`

Toggle whether to use the modlog or not.\
\
If toggled, whenever a note is created on a user it will create a case in the modlog.\
\
**Arguments**\
\- toggle Whether to enable or disable the modlog logging.

### modnoteset nonauthoredits

* Usage: `!modnoteset nonauthoredits <toggle>`
* Aliases: `nae`

Allow any moderator to edit notes, regardless of who authored it\
\
**Arguments**\
\- toggle Whether moderators other than the author can edit notes.

## modnote

* Usage: `!modnote <user> <note>`
* Restricted to: `MOD`
* Aliases: `mnote`
* Checks: `server_only`

Create a note for a user. This user cannot be a bot.\
\
If enabled this will also log to the modlog.\
\
**Arguments**\
\- user A non-bot user to log for.\
\- note The note to add to them.

### modnote remove

* Usage: `!modnote remove <user> <index>`

Remove a note from a user. This user cannot be a bot.\
\
**Arguments**\
\- user The user to remove a note from.\
\- index The index of the note to remove.

### modnote edit

* Usage: `!modnote edit <user> <index> <note>`

Edit a note on a user. This user cannot be a bot.\
\
**Arguments**\
\- user The user to edit a note on. This user cannot be a bot.\
\- index The index of the reason to edit.\
\- note The new note.

### modnote list

* Usage: `!modnote list <user>`

List the notes on a certain user.\
\
This user cannot be a bot.\
\
**Arguments**\
\- user The user to view notes of.

### modnote listall

* Usage: `!modnote listall`

List all the members with notes in this server

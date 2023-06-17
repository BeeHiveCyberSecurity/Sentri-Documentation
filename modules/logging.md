---
description: Keep track of all the happenings inside your server!
---

# 📜 Logging

## modlog

* Usage: `!modlog`
* Restricted to: `ADMIN`
* Aliases: `modlogtoggle and modlogs`
* Checks: `server_only`

Toggle various extended modlog notifications\
\
Requires the channel to be setup with !modlogset modlog #channel\
Or can be sent to separate channels with !modlog channel #channel event\_name

### modlog resetchannel

*   Usage: `!modlog resetchannel <events>`

    Reset the modlog event to the default modlog channel.\
    \
    \- \[events...] must be any of the following options (more than one event can be provided at once):\
    \- channel\_change - Updates to channel name, etc.\
    \- channel\_create\
    \- channel\_delete\
    \- commands\_used - Bot command usage\
    \- emoji\_change - Emojis added or deleted\
    \- server\_change - Server settings changed\
    \- message\_edit\
    \- message\_delete\
    \- member\_change - Member changes like roles added/removed, nicknames, etc.\
    \- role\_change - Role updates permissions, name, etc.\
    \- role\_create\
    \- role\_delete\
    \- voice\_change - Voice channel join/leave\
    \- member\_join\
    \- member\_left\
    \- invite\_created\
    \- invite\_deleted\
    \- thread\_create\
    \- thread\_delete\
    \- thread\_change\
    \- stickers\_change

### modlog member

* Usage: `!modlog member`
* Aliases: `members and memberchanges`

Toggle individual member update settings.

#### modlog member avatar

* Usage: `!modlog member avatar`

Toggle avatar updates for member changes.

#### modlog member timeout

* Usage: `!modlog member timeout`

Toggle timeout updates for members.\
\
Note: Due to a discord limitation this will not update when a members\
timeout has expired and may display a before timeout in the past.

#### modlog member pending

* Usage: `!modlog member pending`

Toggle pending updates for members.

#### modlog member settings

* Usage: `!modlog member settings`

Show the current settings on member updates.

#### modlog member roles

* Usage: `!modlog member roles`
* Aliases: `role`

Toggle role updates for members.

#### modlog member nickname

* Usage: `!modlog member nickname`
* Aliases: `nicknames`

Toggle nickname updates for member changes.

#### modlog member flags

* Usage: `!modlog member flags`

Toggle flags updates for members.\
\
This includes things like:\
\- did\_rejoin\
\- completed\_onboarding\
\- bypasses\_verification\
\- started\_onboarding

### modlog unignore

* Usage: `!modlog unignore <channel>`

Unignore a channel from message delete/edit events and bot commands.\
\
\- the channel to unignore message delete/edit events.

### modlog delete

* Usage: `!modlog delete`

Delete logging settings.

#### modlog delete bulkdelete

* Usage: `!modlog delete bulkdelete`

Toggle bulk message delete notifications.

#### modlog delete ignorecommands

* Usage: `!modlog delete ignorecommands`

Toggle message delete notifications for valid bot command messages.

#### modlog delete cachedonly

* Usage: `!modlog delete cachedonly`

Toggle message delete notifications for non-cached messages.\
\
Delete notifications for non-cached messages\
will only show channel info without content of deleted message or its author.

#### modlog delete individual

* Usage: `!modlog delete individual`

Toggle individual message delete notifications for bulk message delete.

### modlog emojiset

*   Usage: `!modlog emojiset <emoji> <events>`

    Set the emoji used in text modlogs.\
    \
    \- \<new\_emoji> can be any discord emoji or unicode emoji the bot has access to use.\
    \
    \- \[events...] must be any of the following options (more than one event can be provided at once):\
    \- channel\_change - Updates to channel name, etc.\
    \- channel\_create\
    \- channel\_delete\
    \- commands\_used - Bot command usage\
    \- emoji\_change - Emojis added or deleted\
    \- server\_change - Server settings changed\
    \- message\_edit\
    \- message\_delete\
    \- member\_change - Member changes like roles added/removed, nicknames, etc.\
    \- role\_change - Role updates permissions, name, etc.\
    \- role\_create\
    \- role\_delete\
    \- voice\_change - Voice channel join/leave\
    \- member\_join\
    \- member\_left\
    \- invite\_created\
    \- invite\_deleted\
    \- thread\_create\
    \- thread\_delete\
    \- thread\_change\
    \- stickers\_change

### modlog bot

* Usage: `!modlog bot`
* Aliases: `bots`

Bot filter settings.

#### modlog bot change

* Usage: `!modlog bot change`

Toggle bots from being logged in user updates.\
\
This includes roles and nickname.

#### modlog bot deletes

* Usage: `!modlog bot deletes`
* Aliases: `delete`

Toggle message delete notifications for bot users.\
\
This will not affect delete notifications for messages that aren't in bot's cache.

#### modlog bot edits

* Usage: `!modlog bot edits`
* Aliases: `edit`

Toggle message edit notifications for bot users.

#### modlog bot voice

* Usage: `!modlog bot voice`

Toggle bots from being logged in voice state updates.

### modlog channel

*   Usage: `!modlog channel <channel> <events>`

    Set the channel for modlogs.\
    \
    \- The text channel to send the events to.\
    \
    \- \[events...] must be any of the following options (more than one event can be provided at once):\
    \- channel\_change - Updates to channel name, etc.\
    \- channel\_create\
    \- channel\_delete\
    \- commands\_used - Bot command usage\
    \- emoji\_change - Emojis added or deleted\
    \- server\_change - Server settings changed\
    \- message\_edit\
    \- message\_delete\
    \- member\_change - Member changes like roles added/removed, nicknames, etc.\
    \- role\_change - Role updates permissions, name, etc.\
    \- role\_create\
    \- role\_delete\
    \- voice\_change - Voice channel join/leave\
    \- member\_join\
    \- member\_left\
    \- invite\_created\
    \- invite\_deleted\
    \- thread\_create\
    \- thread\_delete\
    \- thread\_change\
    \- stickers\_change

### modlog ignore

* Usage: `!modlog ignore <channel>`

Ignore a channel from message delete/edit events and bot commands.\
\
\- the channel or category to ignore events in

### modlog all

* Usage: `!modlog all <true_or_false>`

Turn all logging options on or off.\
\
\- \<true\_or\_false> True of False, what to set all loggable settings to.

### modlog embeds

* Usage: `!modlog embeds <true_or_false> <events>`
*   Aliases: `embed`

    Set modlog events to use embeds or text\
    \
    \- \<true\_or\_false> The desired embed setting either on or off.\
    \
    \- \[events...] must be any of the following options (more than one event can be provided at once):\
    \- channel\_change - Updates to channel name, etc.\
    \- channel\_create\
    \- channel\_delete\
    \- commands\_used - Bot command usage\
    \- emoji\_change - Emojis added or deleted\
    \- server\_change - Server settings changed\
    \- message\_edit\
    \- message\_delete\
    \- member\_change - Member changes like roles added/removed, nicknames, etc.\
    \- role\_change - Role updates permissions, name, etc.\
    \- role\_create\
    \- role\_delete\
    \- voice\_change - Voice channel join/leave\
    \- member\_join\
    \- member\_left\
    \- invite\_created\
    \- invite\_deleted\
    \- thread\_create\
    \- thread\_delete\
    \- thread\_change\
    \- stickers\_change

### modlog commandlevel

* Usage: `!modlog commandlevel <level>`
* Aliases: `commandslevel`

Set the level of commands to be logged.\
\
\- \[level...] must include all levels you want from:\
\- NONE\
\- MOD\
\- ADMIN\
\- GUILD\_OWNER\
\- BOT\_OWNER\
\
These are the basic levels commands check for in permissions.\
NONE is a command anyone has permission to use, where as MOD\
can be mod or permissions

### modlog toggle

*   Usage: `!modlog toggle <true_or_false> <events>`

    Turn on and off specific modlog actions\
    \
    \- \<true\_or\_false> Either on or off.\
    \
    \- \[events...] must be any of the following options (more than one event can be provided at once):\
    \- channel\_change - Updates to channel name, etc.\
    \- channel\_create\
    \- channel\_delete\
    \- commands\_used - Bot command usage\
    \- emoji\_change - Emojis added or deleted\
    \- server\_change - Server settings changed\
    \- message\_edit\
    \- message\_delete\
    \- member\_change - Member changes like roles added/removed, nicknames, etc.\
    \- role\_change - Role updates permissions, name, etc.\
    \- role\_create\
    \- role\_delete\
    \- voice\_change - Voice channel join/leave\
    \- member\_join\
    \- member\_left\
    \- invite\_created\
    \- invite\_deleted\
    \- thread\_create\
    \- thread\_delete\
    \- thread\_change\
    \- stickers\_change

### modlog settings

* Usage: `!modlog settings`

Show the servers current ExtendedModlog settings

### modlog colour

* Usage: `!modlog colour <colour> <events>`
*   Aliases: `color`

    Set custom colours for modlog events\
    \
    \- must be a hex code or a [built colour.](https://discordpy.readthedocs.io/en/latest/api.html#colour)\
    \
    \- \[events...] must be any of the following options (more than one event can be provided at once):\
    \- channel\_change - Updates to channel name, etc.\
    \- channel\_create\
    \- channel\_delete\
    \- commands\_used - Bot command usage\
    \- emoji\_change - Emojis added or deleted\
    \- server\_change - Server settings changed\
    \- message\_edit\
    \- message\_delete\
    \- member\_change - Member changes like roles added/removed, nicknames, etc.\
    \- role\_change - Role updates permissions, name, etc.\
    \- role\_create\
    \- role\_delete\
    \- voice\_change - Voice channel join/leave\
    \- member\_join\
    \- member\_left\
    \- invite\_created\
    \- invite\_deleted\
    \- thread\_create\
    \- thread\_delete\
    \- thread\_change\
    \- stickers\_change

---
description: >-
  Punish users that only join your server for goods/giveaways and then leave
  right after a certain point.
---

# 🤮 Freeloader Mode

## freeloader

* Usage: `!freeloader`
* Restricted to: `ADMIN`
* Aliases: `fm and freeloadermode`
* Checks: `server_only`

Configuration options for freeloader mode.

### freeloader on

* Usage: `!freeloader on [time=None]`
* Aliases: `start`

Toggle freeloader mode with an optional time to untoggle.\
\
To use this command properly please make sure you have set the action and time length.

### freeloader settings

* Usage: `!freeloader settings`
* Aliases: `showsettings and show`

Show the current settings for freeloader mode.

### freeloader off

* Usage: `!freeloader off`
* Aliases: `end`

Toggle freeloader mode off.

### freeloader whitelist

* Usage: `!freeloader whitelist <add_or_remove> <users>`

Adds or removes managers for your server.\
\
\<add\_or\_remove> should be either add to add users or remove to remove users.

### freeloader time

* Usage: `!freeloader time <time>`
* Aliases: `length`

Sets the time length of the tempban.\
\
\- The length of the ban. Must be entered as a valid integer and must be better 1 and 7 days.

### freeloader action

* Usage: `!freeloader action <action>`

Set the action to take upon freeloaders that leave the server.\
\
Actions can be one of:\
\- Ban\
\- Tempban

### freeloader log

* Usage: `!freeloader log [channel=None]`
* Aliases: `logchannel`

Set the channel where freeloader stats are logged in.

### freeloader message

* Usage: `!freeloader message [message]`

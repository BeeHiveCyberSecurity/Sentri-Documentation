---
description: Check new users with AltDentifier API
---

# 👮 AltDentification

### altcheck

* Usage: `!altcheck [member]`
* Restricted to: `MOD`
* Checks: `server_only`

Check a user on AltDentifier.

## altset

* Usage: `!altset`
* Restricted to: `ADMIN`
* Checks: `server_only`

Manage AltDentifier Settings.

### altset unwhitelist

* Usage: `!altset unwhitelist <user_id>`
* Aliases: `unwl`

Remove a user from the AltDentifier whitelist.

### altset channel

* Usage: `!altset channel [channel=None]`

Set the channel to send AltDentifier join checks to.\
\
This also works as a toggle, so if no channel is provided, it will disable join checks for this server.

### altset settings

* Usage: `!altset settings`

View AltDentifier Settings.

### altset whitelist

* Usage: `!altset whitelist <user_id>`
* Aliases: `wl`

Whitelist a user from AltDentifier actions.

### altset action

* Usage: `!altset action <level> [action=None]`

Specify what actions to take when a member joins and has a certain Trust Level.\
\
Leave this empty to remove actions for the Level.\
The available actions are:\
kick\
ban\
role (don't say 'role' for this, pass an actual role)

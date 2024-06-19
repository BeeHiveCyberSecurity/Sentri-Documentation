---
description: Hulk-smash links out of existence in your server.
---

# AntiLink

## antilinks

* Usage: `!antilinks`
* Restricted to: `MOD`
* Aliases: `nolinks, nolink, antilink, and alset`
* Checks: `server_only`

Configuration options.

### antilinks channel

* Usage: `!antilinks channel [channel=None]`
* Aliases: `chan`

Set the message transfer channel.\
\
Leave the channel blank to turn it off.

### antilinks whitelist

* Usage: `!antilinks whitelist`

Whitelist options.

#### antilinks whitelist user

* Usage: `!antilinks whitelist user <add_or_remove> [members=None]`

Add or remove users from the whitelist.

**antilinks whitelist user list**

* Usage: `!antilinks whitelist user list`

List whitelisted users.

#### antilinks whitelist role

* Usage: `!antilinks whitelist role <add_or_remove> [roles=None]`

Add or remove roles from the whitelist.

**antilinks whitelist role list**

* Usage: `!antilinks whitelist role list`
* Aliases: `view`

List whitelisted roles.

### antilinks watch

* Usage: `!antilinks watch <add_or_remove> [channels=None]`

Add/remove/list channels to watch.\
\
\- If added, links will be removed in these channels.

#### antilinks watch list

* Usage: `!antilinks watch list`

List the channels being watched.

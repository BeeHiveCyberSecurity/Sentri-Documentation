---
description: >-
  Empower a multi-lingual community with on-demand and reaction-based machine
  learning translation!
---

# 🛄 Translate

## translate (Hybrid Command)

* Usage: `!translate <to_language> <text>`
* Slash Usage: `/translate <to_language> <text>`

Translate messages \
\
\<to\_language> is the language you would like to translate\
is the text you want to translate.

### translate stats (Hybrid Command)

* Usage: `!translate stats <server_id>`
* Slash Usage: `/translate stats <server_id>`

Shows translation usage

### translate allowlist (Hybrid Command)

* Usage: `!translate allowlist`
* Slash Usage: `/translate allowlist`
* Restricted to: `MOD`
* Aliases: `whitelist`
* Checks: `server_only`

Set whitelist options for translations\
\
whitelisting supports channels, users, or roles

#### translate allowlist remove (Hybrid Command)

* Usage: `!translate allowlist remove <channel_user_role>`
* Slash Usage: `/translate allowlist remove <channel_user_role>`
* Restricted to: `MOD`
* Aliases: `rem and del`
* Checks: `server_only`

Remove a channel, user, or role from translation whitelist

#### translate allowlist list (Hybrid Command)

* Usage: `!translate allowlist list`
* Slash Usage: `/translate allowlist list`
* Restricted to: `MOD`
* Checks: `server_only`

List Channels, Users, and Roles in the servers translation whitelist.

#### translate allowlist add (Hybrid Command)

* Usage: `!translate allowlist add <channel_user_role>`
* Slash Usage: `/translate allowlist add <channel_user_role>`
* Restricted to: `MOD`
* Checks: `server_only`

Add a channel, user, or role to translation whitelist

### translate blocklist (Hybrid Command)

* Usage: `!translate blocklist`
* Slash Usage: `/translate blocklist`
* Restricted to: `MOD`
* Aliases: `blacklist`
* Checks: `server_only`

Set blacklist options for translations\
\
blacklisting supports channels, users, or roles

#### translate blocklist remove (Hybrid Command)

* Usage: `!translate blocklist remove <channel_user_role>`
* Slash Usage: `/translate blocklist remove <channel_user_role>`
* Restricted to: `MOD`
* Aliases: `rem and del`
* Checks: `server_only`

Remove a channel, user, or role from translation blacklist

#### translate blocklist add (Hybrid Command)

* Usage: `!translate blocklist add <channel_user_role>`
* Slash Usage: `/translate blocklist add <channel_user_role>`
* Restricted to: `MOD`
* Checks: `server_only`

Add a channel, user, or role to translation blacklist

#### translate blocklist list (Hybrid Command)

* Usage: `!translate blocklist list`
* Slash Usage: `/translate blocklist list`
* Restricted to: `MOD`
* Checks: `server_only`

List Channels, Users, and Roles in the servers translation blacklist.

### translate set (Hybrid Command)

* Usage: `!translate set`
* Slash Usage: `/translate set`

Toggle the bot auto translating

#### translate set flag (Hybrid Command)

* Usage: `!translate set flag`
* Slash Usage: `/translate set flag`
* Restricted to: `MOD`
* Aliases: `flags`
* Checks: `server_only`

Toggle translations with flag emojis in text

#### translate set react (Hybrid Command)

* Usage: `!translate set react`
* Slash Usage: `/translate set react`
* Restricted to: `MOD`
* Aliases: `reaction and reactions`
* Checks: `server_only`

Toggle translations to flag emoji reactions

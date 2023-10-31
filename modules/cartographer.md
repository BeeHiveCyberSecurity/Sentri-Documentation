---
description: Backup & Restore tools for Discord servers.
---

# 🎒 Cartographer

This feature can backup & restore the following:\
\- Categories (permissions/order)\
\- Text channels (permissions/order)\
\- Voice channels (permissions/order)\
\- Forum channels (permissions/order)\[Not forum posts]\
\- Roles (permissions and what members they're assigned to)\
\
**Caveats**\
Note the following\
\- If there are multiple roles, channels, categories, or forums with the same name, only 1 of each will be restored.\
\- This is because object IDs cannot be restored so the bot relies on the name of the object.\
\- When restoring, some roles may not be fully restored (such as order) if they were higher than the bot's role.

## cartographer

* Usage: `!cartographer`
* Checks: `server_only`

Open the Backup/Restore menu

## cartographerset

* Usage: `!cartographerset`
* Checks: `server_only`

Backup & Restore Tools

### cartographerset backup

* Usage: `!cartographerset backup`

Create a backup of this server

### cartographerset restorelatest

* Usage: `!cartographerset restorelatest [delete_existing=False]`

Restore the latest backup for this server\
\
**Arguments**\
\- delete\_existing: if True, deletes existing channels/roles that aren't part of the backup.

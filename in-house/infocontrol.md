---
description: >-
  Prevent certain types of information from being shared in your chats to impede
  efforts at DOXing and other types of harassment
icon: binary-circle-check
---

# InfoControl

## infocontrol

* Usage: `!infocontrol`
* Checks: `server_only`

Manage info enforcement settings.

### infocontrol enable

* Usage: `!infocontrol enable`
* Restricted to: `ADMIN`

Enable info enforcement

### infocontrol alerts

* Usage: `!infocontrol alerts <channel>`
* Restricted to: `ADMIN`

Set the log channel for info control deletions.

### infocontrol toggle

* Usage: `!infocontrol toggle <data_type>`
* Restricted to: `ADMIN`

Toggle blocking of a specific data type.

### infocontrol disable

* Usage: `!infocontrol disable`
* Restricted to: `ADMIN`

Disable info enforcement

### infocontrol settings

* Usage: `!infocontrol settings`

List current settings for blocking data types.

### infocontrol removemodrole

* Usage: `!infocontrol removemodrole <role>`
* Restricted to: `ADMIN`

Remove a role from the list of roles to mention in alerts.

### infocontrol addmodrole

* Usage: `!infocontrol addmodrole <role>`
* Restricted to: `ADMIN`

Add a role to the list of roles to mention in alerts.

### infocontrol reset

* Usage: `!infocontrol reset`
* Restricted to: `ADMIN`

Reset the info control settings to default for this server.

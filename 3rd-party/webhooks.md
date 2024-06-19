---
description: Utility commands for webhooks per-server
---

# Webhooks

## webhook

* Usage: `!webhook`
* Checks: `server_only`

Webhook related commands.

### webhook create

* Usage: `!webhook create [channel=None] [webhook_name]`
* Restricted to: `ADMIN`

Creates a webhook in the channel specified with the name specified.\
\
If no channel is specified then it will default to the current channel.

### webhook permissions

* Usage: `!webhook permissions`
* Restricted to: `MOD`
* Aliases: `perms`

Show all members in the server that have Manage Webhook permissions.

### webhook session

* Usage: `!webhook session <webhook_link>`
* Restricted to: `ADMIN`

Initiate a session within this channel sending messages to a specified webhook link.

#### webhook session close

* Usage: `!webhook session close [channel=None]`

Close an ongoing webhook session in a channel.

### webhook send

* Usage: `!webhook send <webhook_link> <message>`
* Restricted to: `ADMIN`

Sends a message to the specified webhook using your avatar and display name.

### webhook say

* Usage: `!webhook say <message>`

Sends a message to the channel as a webhook with your avatar and display name.

### webhook clear

* Usage: `!webhook clear`

Delete all webhooks in this server.

### webhook sudo

* Usage: `!webhook sudo <member> <message>`
* Restricted to: `ADMIN`

Sends a message to the channel as a webhook with the specified member's avatar and display name.

### webhook edit

* Usage: `!webhook edit <message> <content>`
* Restricted to: `ADMIN`
* Cooldown: `5 per 10.0 seconds`

Edit a message sent by a webhook.

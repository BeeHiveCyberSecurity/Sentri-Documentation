---
description: Create clickable buttons attached to messages
---

# 🔘 URL Buttons

## urlbuttons (Hybrid Command)

* Usage: `!urlbuttons`
* Slash Usage: `/urlbuttons`
* Restricted to: `ADMIN`
* Checks: `server_only`

Group of commands to use UrlButtons.

### urlbuttons add (Hybrid Command)

* Usage: `!urlbuttons add <message> <url> <emoji> [text_button]`
* Slash Usage: `/urlbuttons add <message> <url> <emoji> [text_button]`
* Aliases: `+`
* Checks: `server_only`

Add a url-button for a message.

### urlbuttons clear (Hybrid Command)

* Usage: `!urlbuttons clear <message>`
* Slash Usage: `/urlbuttons clear <message>`
* Checks: `server_only`

Clear all url-buttons for a message.

### urlbuttons bulk (Hybrid Command)

* Usage: `!urlbuttons bulk <message> <url_buttons>`
* Slash Usage: `/urlbuttons bulk <message> <url_buttons>`
* Checks: `server_only`

Add a url-button for a message.

### urlbuttons remove (Hybrid Command)

* Usage: `!urlbuttons remove <message> <config_identifier>`
* Slash Usage: `/urlbuttons remove <message> <config_identifier>`
* Aliases: `-`
* Checks: `server_only`

Remove a url-button for a message.\
\
Use !urlbuttons list to find the config identifier.

### urlbuttons list (Hybrid Command)

* Usage: `!urlbuttons list [message=None]`
* Slash Usage: `/urlbuttons list [message=None]`
* Checks: `server_only`

List all url-buttons of this server or display the settings for a specific one.

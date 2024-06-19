---
description: Create customizable forms and more using Discord interactions
---

# 🔳 Modals

## discordmodals (Hybrid Command)

* Usage: `!discordmodals`
* Slash Usage: `/discordmodals`
* Restricted to: `ADMIN`
* Checks: `server_only`

Group of commands to use DiscordModals.

### discordmodals add (Hybrid Command)

* Usage: `!discordmodals add <message> <argument>`
* Slash Usage: `/discordmodals add <message> <argument>`
* Aliases: `+`
* Checks: `server_only`

Add a Modal for a message.\
\
Use YAML syntax to set up everything.\
\
**Example:**\
\
!discordmodals add\
title: Report a bug\
button:\
label: Report\
emoji: ⚠️\
style: 4 # blurple = 1, grey = 2, green = 3, red = 4\
modal:\
\- label: What is the problem?\
style: 2 # short = 1, paragraph = 2\
required: True\
default: None\
placeholder: None\
min\_length: None\
max\_length: None\
channel: general # id, mention, name\
anonymous: False\
messages:\
error: Error!\
submit: Form submitted.\
pings: user1, user2, role1, role2\
whitelist\_roles: role1, role2\
blacklist\_roles: role3, role4\
\
The emoji, style, required, default, placeholder, min\_length, max\_length, channel, anonymous, messages, pings, whitelist\_roles and blacklist\_roles are not required.

### discordmodals remove (Hybrid Command)

* Usage: `!discordmodals remove <message>`
* Slash Usage: `/discordmodals remove <message>`
* Aliases: `-`
* Checks: `server_only`

Remove a Modal for a message.

### discordmodals list (Hybrid Command)

* Usage: `!discordmodals list [message=None]`
* Slash Usage: `/discordmodals list [message=None]`
* Checks: `server_only`

List all Modals of this server or display the settings for a specific one.

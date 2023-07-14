---
description: Utilize OpenAI to react to messages in the computer-determined "perfect" way.
---

# 🍋 Emoji AI

## aiemote

* Usage: `!aiemote`
* Restricted to: `ADMIN`

Totally not glorified sentiment analysis™\
\
Picks a reaction for a message using ChatGPT\
\
To get started, please add a channel to the whitelist with:\
!aiemote allow <#channel>

### aiemote whitelist

* Usage: `!aiemote whitelist`
* Restricted to: `ADMIN`

List all channels in the whitelist

### aiemote remove

* Usage: `!aiemote remove <channel>`
* Restricted to: `ADMIN`
* Aliases: `rm`

Remove a channel from the whitelist\
\
_Arguments_\
\- The mention of channel

### aiemote optin

* Usage: `!aiemote optin`

Opt in of sending your message to OpenAI (bot-wide)\
\
This will allow the bot to react to your messages

### aiemote allow

* Usage: `!aiemote allow <channel>`
* Restricted to: `ADMIN`
* Aliases: `add`

Add a channel to the whitelist\
\
_Arguments_\
\- The mention of channel

### aiemote optout

* Usage: `!aiemote optout`

Opt out of sending your message to OpenAI (bot-wide)\
\
The bot will no longer react to your messages

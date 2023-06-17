---
description: Utilize OpenAI to reply to messages and images in approved channels.
---

# 🧠 Language AI

Utilize OpenAI to reply to messages and images in approved channels.

## chat (Slash Command)

* Usage: `/chat <text>`
* `text:` (Required) The prompt you want to send to the AI.
* Checks: \`

Talk directly to this bot's AI. Ask it anything you want!

## ai\_user

* Usage: `!ai_user`
* Checks: `server_only`

Utilize OpenAI to reply to messages and images in approved channels

### ai\_user config

* Usage: `!ai_user config`
* Aliases: `settings and showsettings`

Returns current config\
\
(Current config per server)

### ai\_user trigger

* Usage: `!ai_user trigger`

Configure trigger settings for the bot to respond to

#### ai\_user trigger public\_forget

* Usage: `!ai_user trigger public_forget`
* Restricted to: `ADMIN`

Toggles whether anyone can use the forget command, or only moderators

#### ai\_user trigger ignore

* Usage: `!ai_user trigger ignore <regex_pattern>`
* Restricted to: `ADMIN`
* Aliases: `ignoreregex`

Messages matching this regex won't be replied to or seen, by the bot

### ai\_user remove

* Usage: `!ai_user remove <channel>`
* Restricted to: `ADMIN`

Remove a channel from the whitelist\
\
**Arguments**\
\- channel A mention of the channel

### ai\_user add

* Usage: `!ai_user add <channel>`
* Restricted to: `ADMIN`

Adds a channel to the whitelist\
\
**Arguments**\
\- channel A mention of the channel

### ai\_user prompt

* Usage: `!ai_user prompt`
* Restricted to: `ADMIN`

Change the prompt settings for the current server\
\
(All subcommands are per server)

#### ai\_user prompt show

* Usage: `!ai_user prompt show`

Show the prompt for the current context. Subcommands: server, members, channels

**ai\_user prompt show server**

* Usage: `!ai_user prompt show server`
* Aliases: `server`

Show the current server prompt

**ai\_user prompt show members**

* Usage: `!ai_user prompt show members`
* Aliases: `users`

Show users with custom prompts

**ai\_user prompt show channels**

* Usage: `!ai_user prompt show channels`

Show all channels with custom prompts

#### ai\_user prompt preset

* Usage: `!ai_user prompt preset <preset>`
* Restricted to: `ADMIN`

List presets using 'list', or set a preset

### ai\_user forget

* Usage: `!ai_user forget`
* Aliases: `lobotomize`

Forces the bot to forget the current conversation up to this point\
\
This is useful if the LLM is stuck doing unwanted behaviour or giving undesirable results.\
See !ai\_user triggers public\_forget to allow non-admins to use this command.

### ai\_user response

* Usage: `!ai_user response`
* Restricted to: `ADMIN`

Change bot response settings\
\
(All subcommands are per server)

#### ai\_user response blocklist

* Usage: `!ai_user response blocklist`
* Restricted to: `ADMIN`

Any generated responses matching these regex patterns will not sent

**ai\_user response blocklist reset**

* Usage: `!ai_user response blocklist reset`
* Restricted to: `ADMIN`

Reset the blocklist to default

**ai\_user response blocklist add**

* Usage: `!ai_user response blocklist add <regex_pattern>`
* Restricted to: `ADMIN`

Add a regex pattern to the blocklist

**ai\_user response blocklist remove**

* Usage: `!ai_user response blocklist remove <regex_pattern>`
* Restricted to: `ADMIN`

Remove a regex pattern from the blacklist

**ai\_user response blocklist show**

* Usage: `!ai_user response blocklist show`
* Restricted to: `ADMIN`

Show the current regex patterns in the blocklist

#### ai\_user response removelist

* Usage: `!ai_user response removelist`
* Restricted to: `ADMIN`

Any string in a generated response matching these regex patterns will be removed

**ai\_user response removelist show**

* Usage: `!ai_user response removelist show`
* Restricted to: `ADMIN`

Show the current regex patterns in the removelist

**ai\_user response removelist reset**

* Usage: `!ai_user response removelist reset`
* Restricted to: `ADMIN`

Reset the removelist to default

**ai\_user response removelist add**

* Usage: `!ai_user response removelist add <regex_pattern>`
* Restricted to: `ADMIN`

Add a regex pattern to the removelist

**ai\_user response removelist remove**

* Usage: `!ai_user response removelist remove <regex_pattern>`
* Restricted to: `ADMIN`

Remove a regex pattern from the removelist

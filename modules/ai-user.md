---
description: Utilize OpenAI to reply to messages and images in approved channels.
---

# 🧠 AI User

## chat (Slash Command)

* Usage: `/chat <text>`
* `text:` (Required) The prompt you want to send to the AI.
* Checks: \`

Talk directly to this bot's AI. Ask it anything you want!

## aiuser

* Usage: `!aiuser`
* Aliases: `ai_user`
* Checks: `server_only`

Utilize OpenAI to reply to messages and images in approved channels and by opt-in users

### aiuser forget

* Usage: `!aiuser forget`
* Aliases: `lobotomize`

Forces the bot to forget the current conversation up to this point\
\
This is useful if the LLM is stuck doing unwanted behaviour or giving undesirable results.\
See !aiuser triggers public\_forget to allow non-admins to use this command.

### aiuser config

* Usage: `!aiuser config`
* Aliases: `settings and showsettings`

Returns current config\
\
(Current config per server)

### aiuser remove

* Usage: `!aiuser remove <channel>`
* Restricted to: `ADMIN`

Remove a channel from the whitelist\
\
**Arguments**\
\- channel A mention of the channel

### aiuser response

* Usage: `!aiuser response`
* Restricted to: `ADMIN`

Change bot response settings\
\
(All subcommands are per server)

#### aiuser response weights

* Usage: `!aiuser response weights`
* Aliases: `logit_bias and bias`

Bias the LLM for/against certain words (tokens)\
\
See [here](https://help.openai.com/en/articles/5247780-using-logit-bias-to-define-token-probability) for additional info.\
\
(All subcommands are per server)

**aiuser response weights list**

* Usage: `!aiuser response weights list`
* Restricted to: `ADMIN`
* Aliases: `show`

Show weights

**aiuser response weights add**

* Usage: `!aiuser response weights add <word> <weight>`
* Restricted to: `ADMIN`

Sets weight for a specific word\
\
Will also use all possible tokens for a word when setting weight\
See [https://platform.openai.com/tokenizer](https://platform.openai.com/tokenizer) for detailed text to token conversion.\
\
_Arguments_\
\- word The word to set weight for\
\- weight The weight to set (-100 to 100)

**aiuser response weights remove**

* Usage: `!aiuser response weights remove <word>`
* Restricted to: `ADMIN`
* Aliases: `delete`

Removes weight for a specific word\
\
_Arguments_\
\- word The word to remove

#### aiuser response removelist

* Usage: `!aiuser response removelist`
* Restricted to: `ADMIN`

Any string in a generated response matching these regex patterns will be removed

**aiuser response removelist reset**

* Usage: `!aiuser response removelist reset`
* Restricted to: `ADMIN`

Reset the removelist to default

**aiuser response removelist show**

* Usage: `!aiuser response removelist show`
* Restricted to: `ADMIN`

Show the current regex patterns in the removelist

**aiuser response removelist remove**

* Usage: `!aiuser response removelist remove <regex_pattern>`
* Restricted to: `ADMIN`

Remove a regex pattern from the removelist

**aiuser response removelist add**

* Usage: `!aiuser response removelist add <regex_pattern>`
* Restricted to: `ADMIN`

Add a regex pattern to the removelist

### aiuser optinbydefault

* Usage: `!aiuser optinbydefault`
* Restricted to: `ADMIN`

Toggles whether users are opted in by default in this server\
\
This command is disabled for servers with more than 150 members.

### aiuser trigger

* Usage: `!aiuser trigger`

Configure trigger settings for the bot to respond to\
\
(All subcommands per server)

#### aiuser trigger public\_forget

* Usage: `!aiuser trigger public_forget`
* Restricted to: `ADMIN`

Toggles whether anyone can use the forget command, or only moderators

#### aiuser trigger random

* Usage: `!aiuser trigger random`
* Restricted to: `ADMIN`

Configure the random trigger\
\
Every 33 minutes, a RNG roll will determine if a random message will be sent using a list of topics as a prompt.\
\
(All subcommands per server)

**aiuser trigger random topics**

* Usage: `!aiuser trigger random topics`
* Restricted to: `ADMIN`

Manage topics to be used in random messages for current server

**aiuser trigger random topics add**

* Usage: `!aiuser trigger random topics add <topic>`
* Restricted to: `ADMIN`
* Aliases: `a`

Add a new topic

**aiuser trigger random topics remove**

* Usage: `!aiuser trigger random topics remove <number>`
* Restricted to: `ADMIN`
* Aliases: `rm and delete`

Removes a topic (by number) from the list

**aiuser trigger random topics show**

* Usage: `!aiuser trigger random topics show`
* Restricted to: `ADMIN`
* Aliases: `list`

Lists topics to used in random messages

#### aiuser trigger ignore

* Usage: `!aiuser trigger ignore <regex_pattern>`
* Restricted to: `ADMIN`
* Aliases: `ignoreregex`

Messages matching this regex won't be replied to or seen, by the bot

### aiuser optout

* Usage: `!aiuser optout`

Opt out of sending your messages / images to OpenAI or another endpoint (bot-wide)\
\
This will prevent the bot from replying to your messages or using your messages.

### aiuser optin

* Usage: `!aiuser optin`

Opt in of sending your messages / images to OpenAI or another endpoint (bot-wide)\
\
This will allow the bot to reply to your messages or using your messages.

### aiuser prompt

* Usage: `!aiuser prompt`
* Restricted to: `ADMIN`

Change the prompt settings for the current server\
\
(All subcommands are per server)

#### aiuser prompt show

* Usage: `!aiuser prompt show <mention>`

Show the prompt for the server (or provided mention)\
**Arguments**\
\- mention _(Optional)_ Mention of user or channel

**aiuser prompt show server**

* Usage: `!aiuser prompt show server`
* Aliases: `server`

Show the current server prompt

**aiuser prompt show channels**

* Usage: `!aiuser prompt show channels`

Show all channels with custom prompts

**aiuser prompt show members**

* Usage: `!aiuser prompt show members`
* Aliases: `users`

Show all users with custom prompts

#### aiuser prompt preset

* Usage: `!aiuser prompt preset <preset>`
* Restricted to: `ADMIN`

Set/list preset prompts\
\
Use !aiuser prompt preset list to see available presets.\
\
**Arguments**\
\- preset The preset to use

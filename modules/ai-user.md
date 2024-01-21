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

**aiuser prompt show members**

* Usage: `!aiuser prompt show members`
* Aliases: `users`

Show all users with custom prompts

**aiuser prompt show channels**

* Usage: `!aiuser prompt show channels`

Show all channels with custom prompts

**aiuser prompt show server**

* Usage: `!aiuser prompt show server`
* Aliases: `server`

Show the current server prompt

#### aiuser prompt preset

* Usage: `!aiuser prompt preset`

Manage presets for the current server\


**aiuser prompt preset add**

* Usage: `!aiuser prompt preset add <prompt>`
* Aliases: `a`

Add a new preset to the presets list\
\
**Arguments**\
\- prompt The prompt to set. Use | to separate the preset name from the prompt at the start. eg. preset\_name|prompt\_text

**aiuser prompt preset remove**

* Usage: `!aiuser prompt preset remove <preset>`
* Aliases: `rm and delete`

Remove a preset by its name from the presets list\
\
**Arguments**\
\- preset The name of the preset to remove

**aiuser prompt preset show**

* Usage: `!aiuser prompt preset show`
* Aliases: `list`

Show all presets for the current server

#### aiuser prompt reset

* Usage: `!aiuser prompt reset`

Reset ALL prompts in this server to default (inc. channels and members)

#### aiuser prompt topics

* Usage: `!aiuser prompt topics`

Manage topics to be used in random messages for current server (if enabled for server by bot owner)

**aiuser prompt topics show**

* Usage: `!aiuser prompt topics show`
* Aliases: `list`

Lists topics to used in random messages

**aiuser prompt topics add**

* Usage: `!aiuser prompt topics add <topic>`
* Aliases: `a`

Add a new topic

**aiuser prompt topics remove**

* Usage: `!aiuser prompt topics remove <number>`
* Aliases: `rm and delete`

Removes a topic (by number) from the list

#### aiuser prompt set

* Usage: `!aiuser prompt set <mention> <prompt>`
* Aliases: `custom and customize`

Set a custom prompt or preset for the server (or provided mention)\
\
**Arguments**\
\- mention _(Optional)_ Mention of a specific user or channel\
\- prompt _(Optional)_ The prompt (or name of a preset) to set. If blank, will remove current prompt.

### aiuser trigger

* Usage: `!aiuser trigger`
* Restricted to: `ADMIN`

Configure trigger settings for the bot to respond to\
\
(All subcommands per server)

#### aiuser trigger ignore

* Usage: `!aiuser trigger ignore <regex_pattern>`
* Aliases: `ignoreregex`

Messages matching this regex won't be replied to or seen, by the bot

#### aiuser trigger public\_forget

* Usage: `!aiuser trigger public_forget`

Toggles whether anyone can use the forget command, or only moderators

### aiuser optin

* Usage: `!aiuser optin`

Opt in of sending your messages / images to OpenAI or another endpoint (bot-wide)\
\
This will allow the bot to reply to your messages or using your messages.

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

### aiuser optout

* Usage: `!aiuser optout`

Opt out of sending your messages / images to OpenAI or another endpoint (bot-wide)\
\
This will prevent the bot from replying to your messages or using your messages.

### aiuser optinbydefault

* Usage: `!aiuser optinbydefault`
* Restricted to: `ADMIN`

Toggles whether users are opted in by default in this server\
\
This command is disabled for servers with more than 150 members.

### aiuser response

* Usage: `!aiuser response`
* Restricted to: `ADMIN`

Change settings used for generated responses\
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

**aiuser response weights remove**

* Usage: `!aiuser response weights remove <word>`
* Restricted to: `ADMIN`
* Aliases: `delete`

Removes weight for a specific word\
\
_Arguments_\
\- word The word to remove

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

#### aiuser response removelist

* Usage: `!aiuser response removelist`
* Restricted to: `ADMIN`

Any string in a generated response matching these regex patterns will be removed

**aiuser response removelist add**

* Usage: `!aiuser response removelist add <regex_pattern>`
* Restricted to: `ADMIN`

Add a regex pattern to the removelist

**aiuser response removelist reset**

* Usage: `!aiuser response removelist reset`
* Restricted to: `ADMIN`

Reset the removelist to default

**aiuser response removelist remove**

* Usage: `!aiuser response removelist remove <regex_pattern>`
* Restricted to: `ADMIN`

Remove a regex pattern from the removelist

**aiuser response removelist show**

* Usage: `!aiuser response removelist show`
* Restricted to: `ADMIN`

Show the current regex patterns in the removelist

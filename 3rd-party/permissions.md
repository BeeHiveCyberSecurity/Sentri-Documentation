---
description: >-
  Configure Sentri's default permissions to customize them for your server's
  needs and usage
---

# 🔓 Permissions

### Usage[¶](broken-reference)

Customise permissions for commands and modules

This module extends the default permission model of the bot. By default, many commands are restricted based on what the command can do. This module allows you to refine some of those restrictions. You can allow wider or narrower access to most commands using it. You cannot, however, change the restrictions on owner-only commands.

When additional rules are set using this module, those rules will be checked prior to checking for the default restrictions of the command. Global rules (set by us) are checked first, then rules set for servers. If multiple global or server rules apply to the case, the order they are checked in is:

1. Rules about a user.
2. Rules about the voice channel a user is in.
3. Rules about the text channel a command was issued in.
4. Rules about a role the user has (The highest role they have with a rule will be used).
5. Rules about the server a user is in (Global rules only).

### Commands[¶](broken-reference)

## permissions

* Usage: `!permissions`

Command permission management tools.

### permissions canrun

* Usage: `!permissions canrun <user> <command>`

Check if a user can run a command.\
\
This will take the current context into account, such as the\
server and text channel.

### permissions setdefaultserverrule

* Usage: `!permissions setdefaultserverrule <allow_or_deny> <cog_or_command>`
* Restricted to: `GUILD_OWNER`
* Aliases: `setdefaultserverrule`
* Checks: `server_only`

Set the default rule for a command in this server.\
\
This is the rule a command will default to when no other rule\
is found.\
\
\<allow\_or\_deny> should be one of "allow", "deny" or "clear".\
"clear" will reset the default rule.\
\
\<cog\_or\_command> is the cog or command to set the default\
rule for. This is case sensitive.

### permissions clearserverrules

* Usage: `!permissions clearserverrules`
* Restricted to: `GUILD_OWNER`
* Aliases: `clearserverrules`
* Checks: `server_only`

Reset all rules in this server.

### permissions removeserverrule

* Usage: `!permissions removeserverrule <cog_or_command> <who_or_what>`
* Restricted to: `GUILD_OWNER`
* Aliases: `removeserverrule`
* Checks: `server_only`

Remove a server rule from a command.\
\
\<cog\_or\_command> is the cog or command to remove the rule\
from. This is case sensitive.\
\
\<who\_or\_what...> is one or more users, channels or roles the rule is for.

### permissions acl

* Usage: `!permissions acl`
* Restricted to: `GUILD_OWNER`
* Aliases: `yaml`

Manage permissions with YAML files.

#### permissions acl yamlexample

* Usage: `!permissions acl yamlexample`

Sends an example of the yaml layout for permissions

#### permissions acl updateserver

* Usage: `!permissions acl updateserver`
* Restricted to: `GUILD_OWNER`
* Aliases: `updateserver`
* Checks: `server_only`

Update rules for this server with a YAML file.\
\
This won't touch any rules not specified in the YAML\
file.

#### permissions acl setserver

* Usage: `!permissions acl setserver`
* Restricted to: `GUILD_OWNER`
* Aliases: `setserver`
* Checks: `server_only`

Set rules for this server with a YAML file.\
\
**WARNING**: This will override reset _all_ rules in this\
server to the rules specified in the uploaded file.

#### permissions acl getserver

* Usage: `!permissions acl getserver`
* Restricted to: `GUILD_OWNER`
* Aliases: `getserver`
* Checks: `server_only`

Get a YAML file detailing all rules in this server.

### permissions explain

* Usage: `!permissions explain`

Explain how permissions works.

### permissions addserverrule

* Usage: `!permissions addserverrule <allow_or_deny> <cog_or_command> <who_or_what>`
* Restricted to: `GUILD_OWNER`
* Aliases: `addserverrule`
* Checks: `server_only`

Add a rule to a command in this server.\
\
\<allow\_or\_deny> should be one of "allow" or "deny".\
\
\<cog\_or\_command> is the cog or command to add the rule to.\
This is case sensitive.\
\
\<who\_or\_what...> is one or more users, channels or roles the rule is for.

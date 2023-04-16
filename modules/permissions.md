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

#### permissions[¶](broken-reference)

**Syntax**

**Description**

Command permission management tools.

**permissions acl**[**¶**](broken-reference)

**Syntax**

**Description**

Manage permissions with YAML files.

Tip

See here for more information with configuring these yaml files.

**permissions acl getglobal**[**¶**](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

```
[p]permissions acl getglobal
```

**Description**

Get a YAML file detailing all global rules.

**permissions acl getserver**[**¶**](broken-reference)

**Syntax**

```
[p]permissions acl getserver
```

**Description**

Get a YAML file detailing all rules in this server.

**permissions acl setglobal**[**¶**](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

```
[p]permissions acl setglobal
```

**Description**

Set global rules with a YAML file.

Warning

This will override reset _all_ global rules to the rules specified in the uploaded file.

This does not validate the names of commands and cogs before setting the new rules.

**permissions acl setserver**[**¶**](broken-reference)

**Syntax**

```
[p]permissions acl setserver
```

**Description**

Set rules for this server with a YAML file.

Warning

This will override reset _all_ rules in this server to the rules specified in the uploaded file.

**permissions acl updateglobal**[**¶**](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

```
[p]permissions acl updateglobal
```

**Description**

Update global rules with a YAML file.

This won’t touch any rules not specified in the YAML file.

**permissions acl updateserver**[**¶**](broken-reference)

**Syntax**

```
[p]permissions acl updateserver
```

**Description**

Update rules for this server with a YAML file.

This won’t touch any rules not specified in the YAML file.

**permissions acl yamlexample**[**¶**](broken-reference)

**Syntax**

```
[p]permissions acl yamlexample
```

**Description**

Sends an example of the yaml layout for permissions

**permissions addglobalrule**[**¶**](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

```
[p]permissions addglobalrule <allow_or_deny> <cog_or_command> <who_or_what...>
```

**Description**

Add a global rule to a cog or command.

**Arguments**

* `<allow_or_deny>`: This should be one of “allow” or “deny”.
* `<cog_or_command>`: The cog or command to add the rule to. This is case sensitive.
* `<who_or_what...>`: One or more users, channels or roles the rule is for.

**permissions addserverrule**[**¶**](broken-reference)

**Syntax**

```
[p]permissions addserverrule <allow_or_deny> <cog_or_command> <who_or_what...>
```

**Description**

Add a rule to a cog or command in this server.

**Arguments**

* `<allow_or_deny>`: This should be one of “allow” or “deny”.
* `<cog_or_command>`: The cog or command to add the rule to. This is case sensitive.
* `<who_or_what...>`: One or more users, channels or roles the rule is for.

**permissions canrun**[**¶**](broken-reference)

**Syntax**

```
[p]permissions canrun <user> <command>
```

**Description**

Check if a user can run a command.

This will take the current context into account, such as the server and text channel.

**Arguments**

* `<user>`: The user to check permissions for.
* `<command>`: The command to check whether the user can run it or not.

**permissions clearglobalrules**[**¶**](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

```
[p]permissions clearglobalrules
```

**Description**

Reset all global rules.

**permissions clearserverrules**[**¶**](broken-reference)

**Syntax**

```
[p]permissions clearserverrules
```

**Description**

Reset all rules in this server.

**permissions explain**[**¶**](broken-reference)

**Syntax**

**Description**

Explain how permissions works.

**permissions removeglobalrule**[**¶**](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

```
[p]permissions removeglobalrule <cog_or_command> <who_or_what...>
```

**Description**

Remove a global rule from a command.

**Arguments**

* `<cog_or_command>`: The cog or command to remove the rule from. This is case sensitive.
* `<who_or_what...>`: One or more users, channels or roles the rule is for.

**permissions removeserverrule**[**¶**](broken-reference)

**Syntax**

```
[p]permissions removeserverrule <cog_or_command> <who_or_what...>
```

**Description**

Remove a server rule from a command.

**Arguments**

* `<cog_or_command>`: The cog or command to remove the rule from. This is case sensitive.
* `<who_or_what...>`: One or more users, channels or roles the rule is for.

**permissions setdefaultglobalrule**[**¶**](broken-reference)

Note

This command is locked to the bot owner.

**Syntax**

```
[p]permissions setdefaultglobalrule <allow_or_deny> <cog_or_command>
```

**Description**

Set the default global rule for a command or a cog.

This is the rule a command will default to when no other rule is found.

**Arguments**

* `<cog_or_command>`: The cog or command to add the rule to. This is case sensitive.
* `<who_or_what...>`: One or more users, channels or roles the rule is for.

**permissions setdefaultserverrule**[**¶**](broken-reference)

**Syntax**

```
[p]permissions setdefaultserverrule <allow_or_deny> <cog_or_command>
```

**Description**

Set the default rule for a command or a cog in this server.

This is the rule a command will default to when no other rule is found.

**Arguments**

* `<cog_or_command>`: The cog or command to add the rule to. This is case sensitive.
* `<who_or_what...>`: One or more users, channels or roles the rule is for.

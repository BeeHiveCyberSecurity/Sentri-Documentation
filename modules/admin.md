# 🎟 Admin

### Usage[¶](broken-reference)

This cog will provide tools for server admins and bot owners.

It can add or remove a role to a member, edit one or make some available for members so they can self-assign them as they wish.

It also provides tools for the bot owner such as server locking (once enabled, the bot will instantly leave new servers it joins) and announcements, which can send something in all the servers of the bot.

### Commands[¶](broken-reference)

Here’s a list of all commands available for this cog.

#### selfrole[¶](broken-reference)

**Syntax**

**Description**

Add or remove a role from yourself. It must have been configured as user settable by admins using the selfroleset command.

**Arguments**

* `<selfrole>`: The role you want to attribute or remove from yourself. Please give **the exact role name or ID**, or it won’t be detected.

**selfrole add**[**¶**](broken-reference)

**Syntax**

```
[p]selfrole add <selfrole>
```

**Description**

Add a role to yourself. It must have been configured as user settable by admins using the selfroleset command.

**Arguments**

* `<selfrole>`: The role you want to attribute to yourself. Please give **the exact role name or ID**, or it won’t be detected.

**selfrole remove**[**¶**](broken-reference)

**Syntax**

```
[p]selfrole remove <selfrole>
```

**Description**

Remove a role from yourself. It must have been configured as user settable by admins using the selfroleset command.

**Arguments**

* `<selfrole>`: The role you want to remove from yourself. Please give **the exact role name or ID**, or it won’t be detected.

**selfrole list**[**¶**](broken-reference)

**Syntax**

**Description**

List all of the available roles you can assign to yourself.

#### selfroleset[¶](broken-reference)

Note

This command is locked to the admin role. This is also usable by the members with the `Manage roles` permission.

**Syntax**

**Description**

Define the list of user settable roles. Those roles will be available to any member using the selfrole command.

**selfroleset add**[**¶**](broken-reference)

**Syntax**

```
[p]selfroleset add <role>
```

**Description**

Add a role, or a selection of roles, to the list of available selfroles.

Warning

Members will be able to assign themselves the role. Make sure it doesn’t give extra perms or anything that can break your server’s security.

**Arguments**

* `<role>`: The role to add to the list. Please give **the exact role name or ID**, or it won’t be detected.

**selfroleset clear**[**¶**](broken-reference)

**Syntax**

**Description**

Clear the list of available selfroles for this server.

**selfroleset remove**[**¶**](broken-reference)

**Syntax**

```
[p]selfroleset remove <role>
```

**Description**

Remove a role, or a selection of roles, from the list of available selfroles.

**Arguments**

* `<role>`: The role to remove from the list. Please give **the exact role name or ID**, or it won’t be detected.

#### addrole[¶](broken-reference)

Note

This command is locked to the admin role. This is also usable by the members with the `Manage roles` permission.

**Syntax**

```
[p]addrole <rolename> [user]
```

**Description**

Adds a role to a member. If `user` is not given, it will be considered as yourself, the command author.

**Arguments**

* `<role>`: The role to add to the member. Please give **the exact role name or ID**, or it won’t be detected. If the role name has spaces, provide it enclosed in quotes like this: `"my role with spaces"`
* `[user]`: The member you want to add the role to. Defaults to the command author. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname.

#### removerole[¶](broken-reference)

Note

This command is locked to the admin role. This is also usable by the members with the `Manage roles` permission.

**Syntax**

```
[p]removerole <rolename> [user]
```

**Description**

Removes a role from a member. If `user` is not given, it will be considered as yourself, the command author.

**Arguments**

* `<role>`: The role to remove. Please give **the exact role name or ID**, or it won’t be detected. If the role name has spaces, provide it enclosed in quotes like this: `"my role with spaces"`
* `[user]`: The member to remove the role from. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname. Defaults to the command author.

#### editrole[¶](broken-reference)

**Syntax**

**Description**

Edits the settings of a role.

**editrole name**[**¶**](broken-reference)

**Syntax**

```
[p]editrole name <role> <name>
```

**Description**

Edits the name of a role.

**Arguments**

* `<role>`: The role name to edit. Please give **the exact role name or ID**, or it won’t be detected. If the role name has spaces, provide it enclosed in quotes like this: `"my role with spaces"`
* `<name>`: The new role name. If it has spaces, you must use quotes.

**editrole color**[**¶**](broken-reference)

**Syntax**

```
[p]editrole color <role> <color>
```

**Description**

Edits the color of a role.

**Arguments**

* `<role>`: The role name to edit. Please give **the exact role name or ID**, or it won’t be detected. If the role name has spaces, provide it enclosed in quotes like this: `"my role with spaces"`
* `<color>`: The new color to assign. You can either provide the hexadecimal code of the color, or one of the colors listed here: `discord.Color`.

**Examples**

* `[p]editrole color "My role" #ff0000`
* `[p]editrole color "My role" dark_blue`

#### announceset[¶](broken-reference)

**Syntax**

**Description**

Change how announcements are received in this guild.

**announceset channel**[**¶**](broken-reference)

**Syntax**

```
[p]announceset channel [channel]
```

**Description**

Sets the channel where the bot owner announcements will be sent.

**Arguments**

* `[channel]`: The channel that will be used for bot announcements. You can either mention the channel, provide its exact name or its ID. Defaults to where you typed the command.

**announceset clearchannel**[**¶**](broken-reference)

**Syntax**

```
[p]announceset clearchannel
```

**Description**

Disables announcements on your server. To enable them again, you will have to re-enter your announcements channel with the announceset channel command.



Tip

Another way to prevent your bot from being invited on more servers is making it private directly from the developer portal.

Once a bot is private, it can only be invited by its owner (or team owners). Other users will get an error on Discord’s webpage explaining that the bot is private.

To do this, go to the [Discord developer portal](https://discord.com/developers), select your application, click “Bot” in the sidebar, then untick “Public bot”

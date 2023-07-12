---
description: Get started configuring Sentri to serve your staff and userbase!
---

# 😨 Setting Up

#### Inviting Sentri

First, you'll need to invite Sentri. That's easy enough, just click [here!](https://discord.com/oauth2/authorize?client\_id=1095981492884209804\&scope=bot\&permissions=8)

{% hint style="warning" %}
While Sentri doesn't **require** `Administrator`, it's a security bot - it asks for it and more than likely will need it at some point in time. You are welcome to select your own permissions that you feel comfortable with, but, you may then introduce complexities with your own roles system. Customize Sentri's permissions at your own risk.
{% endhint %}

{% hint style="info" %}
After invite, you'll need to adjust Sentri's role position for the sake of Discord moderative hierarchy.

`MOVE THE SENTRI INTEGRATION ROLE JUST ABOVE THE HIGHEST ROLE THAT YOU WOULD LIKE SENTRI TO MODERATE`
{% endhint %}

#### The commands

The command you’re going to use the most is **help**. This command will show you **all of the available commands** of the bot with a small description.

```
[p]help
```

{% hint style="info" %}
The help message is generated dynamically and users will only see the commands they can use. If users roles change, they'll see additional commands unlock - equally, removing permissions may remove their ability to use particular commands inside your server. You can change what commands users can use with the permissions module, command is `!permissions`.
{% endhint %}



You can also pick a command to get its detailed description and the parameters.

```
[p]help command
```

{% hint style="info" %}
Arguments enclosed in `< >` are **required** for the command to work.

Arguments enclosed in `[ ]` are **optional** for the command; you can decide whether to use them or not.

If your argument includes spaces like `Hello world!`, most of the time you will need to place it in double quotes like this: `"Hello world!"`. Sometimes (especially for the last argument) these double quotes are not required.

Arguments followed by an ellipsis `...` means that you may provide multiple arguments for the command.

Arguments followed by `=value` means that, if not specified, the argument will be equal to `value`.
{% endhint %}

For example, the command `[p]cleanup messages` in the cleanup cog has the syntax `cleanup messages <number> [delete_pinned=False]`, which means `delete_pinned` default will be false, unless you specify it as true.

You can use help to show the **categories** too, generally called cogs or modules, by doing the following (notice the capitalization):

```
[p]help YourCategory
```

Help also shows **command groups**. They are group of commands. To get the description of a subcommand, type this:

```
[p]help commandgroup subcommand
```

When using subcommands, you also need to specify the command group. As an example, `cleanup` has 6 subcommands. If you want to use one of them, do: `[p]cleanup messages 10`

### Permissions

Sentri works with different levels of permissions. Every module defines the level of permission needed for a command.

{% hint style="danger" %}
Permissions configuration is **REQUIRED** for Sentri to function properly. Sentri will **NOT** assume any permissions you've previously given a user are intended. A server owner **MUST** specify a Moderator-level and Administrator-level role for proper function and usage.
{% endhint %}

#### Server owner

The server owner can access all commands on his guild, except the global ones or those that can interact with system files (available for the bot owner).

#### Administrator

The administrator is defined by its roles. You can set multiple admin roles with the `[p]set roles` commands.

For example, in the mod cog, an admin can use the `[p]modset` command which defines the cog settings.

#### Moderator

A moderator is a step above the average users. You can set multiple moderator roles with the `[p]set roles addmodrole` and `[p]set roles removemodrole` commands.

For example, in the filter cog, a mod will be able to use the various commands under `[p]filter` (such as adding and removing filtered words), but they will not be able to modify the cog settings with the `[p]filterset` command.


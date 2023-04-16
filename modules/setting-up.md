# 😨 Setting Up

#### The commands

The command you’re going to use the most is **help**. This command will show you **all of the available commands** of the bot with a small description.

```
[p]help
```

Tip

The message is generated dynamically and users will only see the commands they can use. You can change what commands users can use with the permissions module.

You can also pick a command to get its detailed description and the parameters.

```
[p]help command
```

Note

Arguments enclosed in `< >` are **required** for the command to work.

Arguments enclosed in `[ ]` are **optional** for the command; you can decide whether to use them or not.

If your argument includes spaces like `Hello world!`, most of the time you will need to place it in double quotes like this: `"Hello world!"`. Sometimes (especially for the last argument) these double quotes are not required.

Arguments followed by an ellipsis `...` means that you may provide multiple arguments for the command.

For example, the command `[p]cog install` in the downloader cog has the syntax `cog install <repo> <cogs...>`, meaning that you can provide 1 or more `cogs` to install from the `repo`.

Arguments followed by `=value` means that, if not specified, the argument will be equal to `value`.

For example, the command `[p]cleanup messages` in the cleanup cog has the syntax `cleanup messages <number> [delete_pinned=False]`, which means `delete_pinned` default will be false, unless you specify it as true.

You can use help to show the **categories** too, generally called cogs, by doing the following (notice the capitalization):

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

#### Server owner

The server owner can access all commands on his guild, except the global ones or those that can interact with system files (available for the bot owner).

#### Administrator

The administrator is defined by its roles. You can set multiple admin roles with the `[p]set addadminrole` and `[p]set removeadminrole` commands.

For example, in the mod cog, an admin can use the `[p]modset` command which defines the cog settings.

#### Moderator

A moderator is a step above the average users. You can set multiple moderator roles with the `[p]set addmodrole` and `[p]set removemodrole` commands.

For example, in the filter cog, a mod will be able to use the various commands under `[p]filter` (such as adding and removing filtered words), but they will not be able to modify the cog settings with the `[p]filterset` command.


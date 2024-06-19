---
description: The tag related commands.
---

# ⚡ Tags

## tag

* Usage: `!tag <name>`
* Checks: `server_only`

Allows you to tag text for later retrieval.\
If a subcommand is not called, then this will search the tag database\
for the tag requested.

### tag stats

* Usage: `!tag stats`

Gives stats about the tag database.

### tag list

* Usage: `!tag list [member]`

Lists all the tags that belong to you or someone else.\
\
Parameters\
\----------\
member: discord.Member (optional)\
Another server member that you wish to look up tags for.

### tag transfer

* Usage: `!tag transfer <tag_name> <user>`
* Checks: `server_only and roles_or_mod_or_permissions`

Transfer your tag to another user.\
\
This can be done by the creator of the tag. Cannot transfer\
if the user being transfered to is over the tag limit.\
\
Parameters:\
\-----------\
tag\_name: str\
The tag name.\
user: discord.Member\
The server member you wish to transfer this tag to.

### tag info

* Usage: `!tag info <name>`
* Aliases: `owner`

Retrieves info about a tag.\
The info includes things like the owner and how many times it was used.

### tag generic

* Usage: `!tag generic <name> <content>`
* Restricted to: `MOD`

Creates a new generic tag owned by you.\
Unlike the create tag subcommand, this will always attempt to create\
a generic tag and not a server-specific one.

### tag add

* Usage: `!tag add <name> <content>`
* Aliases: `create`
* Checks: `server_only and roles_or_mod_or_permissions`

Creates a new tag owned by you.\
If you create a tag via private message then the tag is a generic\
tag that can be accessed in all servers. Otherwise the tag you\
create can only be accessed in the server that it was created in.

### tag edit

* Usage: `!tag edit <name> <content>`
* Checks: `roles_or_mod_or_permissions`

Modifies an existing tag that you own.\
This command completely replaces the original text. If you edit\
a tag via private message then the tag is looked up in the generic\
tag database. Otherwise it looks at the server-specific database.

### tag rename

* Usage: `!tag rename <oldName> <newName>`

Renames a tag.\
\
This is useful to help preserve tag statistics.\
\
Parameters\
\----------\
oldName: str\
The old tag name.\
newName: str\
The new tag name.

### tag delete

* Usage: `!tag delete <name>`
* Aliases: `del, remove, and rm`
* Checks: `roles_or_mod_or_permissions`

Removes a tag that you own.\
The tag owner can always delete their own tags. If someone requests\
deletion and has Manage Messages permissions or a Bot Mod role then\
they can also remove tags from the server-specific database. Generic\
tags can only be deleted by the bot owner or the tag owner.\
Deleting a tag will delete all of its aliases as well.

### tag raw

* Usage: `!tag raw <name>`

Gets the raw content of the tag.\
This is with markdown escaped. Useful for editing.

### tag all

* Usage: `!tag all`
* Checks: `server_only`

Lists all server-specific tags for this server.

### tag search

* Usage: `!tag search <query>`

Searches for a tag.\
This searches both the generic and server-specific database. If it's\
a private message, then only generic tags are searched.\
The query must be at least 2 characters.

### tag make

* Usage: `!tag make`
* Checks: `server_only and roles_or_mod_or_permissions`

Interactive makes a tag for you.\
This walks you through the process of creating a tag with\
its name and its content. This works similar to the tag\
create command.

### tag settings

* Usage: `!tag settings`
* Restricted to: `MOD`
* Checks: `server_only`

Tag settings.

#### tag settings max

* Usage: `!tag settings max <role> <num_tags>`

Set the max number of tags per member per role.\
\
For each member of the specified role, each member will have a maximum\
number of tags they can create. If the member is part of more than one\
role, then they will take the MAXIMUM number from the roles that they\
have.\
\
This limit does not apply to admins or mods.\
\
Parameters:\
\-----------\
role: discord.Role\
The role to set a maximum for.\
num\_tags: int\
The maximum number of tags per member for that role.\
If 0, then the tier is removed.

#### tag settings togglealias

* Usage: `!tag settings togglealias`

Toggle creating aliases for tags.

#### tag settings dump

* Usage: `!tag settings dump`

Dumps server-specific tags to a CSV file, sorted by number of uses.

#### tag settings tiers

* Usage: `!tag settings tiers`

Show the tiers and their respective max tags.

### tag alias

* Usage: `!tag alias <new_name> <old_name>`
* Restricted to: `MOD`
* Checks: `server_only`

Creates an alias for a pre-existing tag.\
You own the tag alias. However, when the original\
tag is deleted the alias is deleted as well.\
Tag aliases cannot be edited. You must delete\
the alias and remake it to point it to another\
location.\
You cannot have generic aliases.

### tag purge

* Usage: `!tag purge <member>`
* Restricted to: `MOD`
* Checks: `server_only`

Removes all server-specific tags by a user.\
You must have Manage Messages permissions to use this.

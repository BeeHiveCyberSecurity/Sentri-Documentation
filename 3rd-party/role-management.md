---
description: Manage your server's roles, reaction roles, and more!
---

# Role Management

## roletools

* Usage: `!roletools`
* Checks: `server_only`

Commands for creating custom role settings

### roletools selfrem

* Usage: `!roletools selfrem [true_or_false=None] <role>`
* Restricted to: `ADMIN`

Set whether or not a user can remove the role from themselves.\
\
\[true\_or\_false] optional boolean of what to set the setting to.\
If not provided the current setting will be shown instead.\
The role you want to set.

### roletools autorole

* Usage: `!roletools autorole [true_or_false=None] <role>`
* Restricted to: `ADMIN`
* Aliases: `auto`

Set a role to be automatically applied when a user joins the server.\
\
\[true\_or\_false] optional boolean of what to set the setting to.\
If not provided the current setting will be shown instead.\
The role you want to set.

### roletools atomic

* Usage: `!roletools atomic [true_or_false=None]`
* Restricted to: `ADMIN`

Set the atomicity of role assignment.\
What this means is that when this is True roles will be\
applied inidvidually and not cause any errors. When this\
is set to False roles will be grouped together into one call.\
\
This can cause race conditions if you have other methods of applying\
roles setup when set to False.\
\
\[true\_or\_false] optional boolean of what to set the setting to.\
To reset back to the default global rules use clear.\
If not provided the current setting will be shown instead.

### roletools sticky

* Usage: `!roletools sticky [true_or_false=None] <role>`
* Restricted to: `ADMIN`

Set whether or not a role will be re-applied when a user leaves and rejoins the server.\
\
\[true\_or\_false] optional boolean of what to set the setting to.\
If not provided the current setting will be shown instead.\
The role you want to set.

### roletools cost

* Usage: `!roletools cost [cost=None] <role>`
* Restricted to: `ADMIN`

Set the cost to acquire a role.\
\
\[cost] The price you want to set the role at in bot credits.\
Setting this to 0 or lower will remove the cost.\
If not provided the current setting will be shown instead.\
The role you want to set.

### roletools exclude

* Usage: `!roletools exclude`
* Aliases: `exclusive`

Set role exclusions

#### roletools exclude remove

* Usage: `!roletools exclude remove <role> <exclude>`
* Restricted to: `ADMIN`

Remove role exclusion\
\
This is the role a user may acquire you want to set exclusions for.\
The role(s) currently excluded you no longer wish to have excluded

#### roletools exclude mutual

* Usage: `!roletools exclude mutual <roles>`
* Restricted to: `ADMIN`

Allow setting roles mutually exclusive to eachother\
\
This is equivalent to individually setting each roles exclusive roles to another\
set of roles.\
\
\[role...] The roles you want to set as mutually exclusive.

#### roletools exclude add

* Usage: `!roletools exclude add <role> <exclude>`
* Restricted to: `ADMIN`

Add role exclusion (This will remove if the designated role is acquired\
if the included roles are not selfremovable they will not be removed\
and the designated role will not be given)\
\
This is the role a user may acquire you want to set exclusions for.\
The role(s) you wish to have removed when a user gains the\
\
Note: This will only work for roles assigned by this cog.

### roletools removerole

* Usage: `!roletools removerole <role> <who>`
* Restricted to: `ADMIN`
* Cooldown: `1 per 10.0 seconds`

Removes a role from the designated members.\
\
The role you want to give.\
\[who...] Who you want to give the role to. This can include any of the following:diff\
\+ Member\
A specified member of the server.\
\+ Role\
People who already have a specified role.\
\+ TextChannel\
People who have access to see the channel provided.\
Or one of the following:\
\+ everyone - everyone in the server.\
\+ here - everyone who appears online in the server.\
\+ bots - all the bots in the server.\
\+ humans - all the humans in the server.\
\
**Note:** This runs through exclusive and inclusive role checks\
which may cause unintended roles to be removed/applied.\
\
**This command is on a cooldown of 10 seconds per member who receives**\
**a role up to a maximum of 1 hour.**

### roletools required

* Usage: `!roletools required`
* Aliases: `requires, require, and req`

Set role requirements

#### roletools required any

* Usage: `!roletools required any <role> <require_any>`
* Restricted to: `ADMIN`

Set the required roles to require any of the roles instead of all of them\
\
This is the role a user may acquire you want to set requirements for.\
\<require\_any> Either True or False. If True any of the required roles will allow\
the user to acquire the .\
\
Note: This will only work for roles assigned by this cog.

#### roletools required add

* Usage: `!roletools required add <role> <required>`
* Restricted to: `ADMIN`

Add role requirements\
\
This is the role a user may acquire you want to set requirements for.\
The role(s) the user requires before being allowed to gain this role.\
\
Note: This will only work for roles assigned by this cog.

#### roletools required remove

* Usage: `!roletools required remove <role> <required>`
* Restricted to: `ADMIN`

Remove role requirements\
\
This is the role a user may acquire you want to set requirements for.\
The role(s) you wish to have added when a user gains the\
\
Note: This will only work for roles assigned by this cog.

### roletools selfrole

* Usage: `!roletools selfrole`

Add or remove a defined selfrole

#### roletools selfrole add

* Usage: `!roletools selfrole add <role>`

Give yourself a role\
\
The role you want to give yourself

#### roletools selfrole remove

* Usage: `!roletools selfrole remove <role>`

Remove a role from yourself\
\
The role you want to remove.

### roletools viewroles

* Usage: `!roletools viewroles [role]`
* Aliases: `viewrole`

View current roletools setup for each role in the server\
\
\[role] The role you want to see settings for.

### roletools giverole

* Usage: `!roletools giverole <role> <who>`
* Restricted to: `ADMIN`
* Cooldown: `1 per 10.0 seconds`

Gives a role to designated members.\
\
The role you want to give.\
\[who...] Who you want to give the role to. This can include any of the following:diff\
\+ Member\
A specified member of the server.\
\+ Role\
People who already have a specified role.\
\+ TextChannel\
People who have access to see the channel provided.\
Or one of the following:\
\+ everyone - everyone in the server.\
\+ here - everyone who appears online in the server.\
\+ bots - all the bots in the server.\
\+ humans - all the humans in the server.\
\
**Note:** This runs through exclusive and inclusive role checks\
which may cause unintended roles to be removed/applied.\
\
**This command is on a cooldown of 10 seconds per member who receives**\
**a role up to a maximum of 1 hour.**

### roletools buttons

* Usage: `!roletools buttons`
* Restricted to: `ADMIN`
* Aliases: `button`

Setup role buttons

#### roletools buttons create

* Usage: `!roletools buttons create <name> <role> [label=None] [emoji=None] [style=ButtonStyle.primary]`

Create a role button\
\
\- The name of the button for use later in setup.\
\- The role this button will assign or remove.\
\[label] - The optional label for the button.\
\[emoji] - The optional emoji used in the button.\
\[style] - The background button style. Must be one of the following:\
\- primary\
\- secondary\
\- success\
\- danger\
\- blurple\
\- grey\
\- green\
\- red\
\
Note: If no label and no emoji are provided the roles name will be used instead.\
This name will not update if the role name is changed.

#### roletools buttons view

* Usage: `!roletools buttons view`
* Restricted to: `ADMIN`

View current buttons setup for role assign in this server.

#### roletools buttons delete

* Usage: `!roletools buttons delete <name>`
* Aliases: `del and remove`

Delete a saved button.\
\
\- the name of the button you want to delete.

### roletools forcerole

* Usage: `!roletools forcerole <users> <role>`
* Restricted to: `ADMIN`

Force a sticky role on one or more users.\
\
The users you want to have a forced stickyrole applied to.\
The role you want to set.\
\
Note: The only way to remove this would be to manually remove the role from\
the user.

### roletools select

* Usage: `!roletools select`
* Restricted to: `ADMIN`
* Aliases: `selects`

Setup role select menus

#### roletools select deleteoption

* Usage: `!roletools select deleteoption <name>`
* Aliases: `deloption, removeoption, and remoption`

Delete a saved option.\
\
\- the name of the select option you want to delete.

#### roletools select viewoptions

* Usage: `!roletools select viewoptions`
* Restricted to: `ADMIN`
* Aliases: `listoptions, viewoption, and listoption`

View current select menus setup for role assign in this server.

#### roletools select create

* Usage: `!roletools select create <name> <options> [min_values=None] [max_values=None] [placeholder]`

Create a select menu\
\
\- The name for you to use when you send a message with this menu.\
\[options]... - The select menu options you designated previously.\
\[min\_values] - The minimum number of items from this menu to be selected.\
\[max\_values] - The maximum number of items from this menu that can be selected.\
(If not provided this will default to the number of options provided.)\
\[placeholder] - This is the default text on the menu when no option has been\
chosen yet.

#### roletools select delete

* Usage: `!roletools select delete <name>`
* Aliases: `del and remove`

Delete a saved select menu.\
\
\- the name of the select menu you want to delete.

#### roletools select createoption

* Usage: `!roletools select createoption <name> <role> [label=None] [description=None] [emoji=None]`
* Aliases: `addoption`

Create a select menu option\
\
\- The name of the select option for use later in setup.\
\- The role this select option will assign or remove.\
\[label] - The optional label for the option, max of 25 characters.\
\[description] - The description for the option, max of 50 characters.\
\[emoji] - The optional emoji used in the select option.\
\
Note: If no label and no emoji are provided the roles name will be used instead.\
This name will not update if the role name is changed.

#### roletools select view

* Usage: `!roletools select view`
* Restricted to: `ADMIN`
* Aliases: `list`

View current select menus setup for role assign in this server.

### roletools include

* Usage: `!roletools include`
* Aliases: `inclusive`

Set role inclusion

#### roletools include remove

* Usage: `!roletools include remove <role> <include>`
* Restricted to: `ADMIN`

Remove role inclusion\
\
This is the role a user may acquire you want to set exclusions for.\
The role(s) currently inclusive you no longer wish to have included

#### roletools include add

* Usage: `!roletools include add <role> <include>`
* Restricted to: `ADMIN`

Add role inclusion (This will add roles if the designated role is acquired\
if the designated role is removed the included roles will also be removed\
if the included roles are set to selfremovable)\
\
This is the role a user may acquire you want to set exclusions for.\
The role(s) you wish to have added when a user gains the\
\
Note: This will only work for roles assigned by this cog.

#### roletools include mutual

* Usage: `!roletools include mutual <roles>`
* Restricted to: `ADMIN`

Allow setting roles mutually inclusive to eachother\
\
This is equivalent to individually setting each roles inclusive roles to another\
set of roles.\
\
\[role...] The roles you want to set as mutually inclusive.

### roletools forceroleremove

* Usage: `!roletools forceroleremove <users> <role>`
* Restricted to: `ADMIN`

Force remove sticky role on one or more users.\
\
The users you want to have a forced stickyrole applied to.\
The role you want to set.\
\
Note: This is generally only useful for users who have left the server.

### roletools message

* Usage: `!roletools message`

Commands for sending/editing messages for roletools

#### roletools message editbutton

* Usage: `!roletools message editbutton <message> <buttons>`

Edit a bots message to include Role Buttons\
\
\- The existing message to add role buttons to. Must be a bots message.\
\[buttons]... - The names of the buttons you want to include up to a maximum of 25.

#### roletools message sendselect

* Usage: `!roletools message sendselect <channel> <menus> <message>`

Send a select menu to a specified channel for role assignment\
\
\- the channel to send the button role buttons to.\
\[menus]... - The names of the select menus you want included in the\
message up to a maximum of 5.\
\- The message to be included with the select menu.

#### roletools message send

* Usage: `!roletools message send <channel> <buttons> <menus> <message>`

Send a select menu to a specified channel for role assignment\
\
\- the channel to send the button role buttons to.\
\[buttons]... - The names of the buttons you want included in the\
\[menus]... - The names of the select menus you want included in the\
message up to a maximum of 5.\
\- The message to be included with the select menu.\
\
Note: There is a maximum of 25 slots available on one message. Each menu\
uses up 5 slots while each button uses up 1 slot.

#### roletools message editselect

* Usage: `!roletools message editselect <message> <menus>`

Edit a bots message to include Role Buttons\
\
\- The existing message to add role buttons to. Must be a bots message.\
\[menus]... - The names of the select menus you want to include up to a maximum of 5.

#### roletools message edit

* Usage: `!roletools message edit <message> <buttons> <menus>`

Edit a bots message to include Role Buttons\
\
\- The existing message to add role buttons to. Must be a bots message.\
\[buttons]... - The names of the buttons you want to include up to a maximum of 25.\
\[menus]... - The names of the select menus you want to include up to a maximum of 5.\
\
Note: There is a maximum of 25 slots available on one message. Each menu\
uses up 5 slots while each button uses up 1 slot.

#### roletools message sendbutton

* Usage: `!roletools message sendbutton <channel> <buttons> <message>`

Send buttons to a specified channel with optional message.\
\
\- the channel to send the button role buttons to.\
\[buttons]... - The names of the buttons you want included in the\
message up to a maximum of 25.\
\- The message to be included with the buttons.

### roletools reaction

* Usage: `!roletools reaction`
* Aliases: `react and reactions`

Reaction role settings

#### roletools reaction reactroles

* Usage: `!roletools reaction reactroles`
* Restricted to: `ADMIN`
* Aliases: `reactionroles and reactrole`

View current bound roles in the server

#### roletools reaction remove

* Usage: `!roletools reaction remove <message> <role_or_emoji>`
* Restricted to: `ADMIN`
* Aliases: `rem`

Remove a reaction role\
\
can be the channel\_id-message\_id pair\
from copying message ID while holding SHIFT or a message link\
The emoji you want people to react with to get the role.\
The role you want people to receive for reacting.\
\
Note: This will not remove the emoji reactions on the message.

#### roletools reaction cleanup

* Usage: `!roletools reaction cleanup`
* Restricted to: `ADMIN`

Cleanup old/missing reaction roles and settings.\
\
Note: This will also clear out reaction roles if the bot is just\
missing permissions to see the reactions.

#### roletools reaction clearreact

* Usage: `!roletools reaction clearreact <message> <emojis>`
* Restricted to: `ADMIN`
* Aliases: `clearreacts`

Clear the reactions for reaction roles. This will remove\
all reactions and then re-apply the bots reaction for you.\
\
The message you want to clear reactions on.\
\[emojis...] Optional emojis you want to specifically remove.\
If no emojis are provided this will clear all the reaction role\
emojis the bot has for the message provided.\
\
Note: This will only clear reactions which have a corresponding\
reaction role on it.

#### roletools reaction bulk

* Usage: `!roletools reaction bulk <message> <role_emoji>`
* Restricted to: `ADMIN`
* Aliases: `bulkcreate and bulkmake`

Create multiple roles reactions for a single message\
\
can be the channel\_id-message\_id pair\
from copying message ID while holding SHIFT or a message link\
\[role\_emoji...] Must be a role-emoji pair separated by either ;, ,, |, or -.\
\
Note: Any spaces will be considered a new set of role-emoji pairs, if you\
want to specify a role with a space in it without pinging it enclose\
the full role-emoji pair in quotes.\
\
e.g. !roletools bulkreact 461417772115558410-821105109097644052 @member-:smile:\
!roletools bulkreact 461417772115558410-821105109097644052 "Super Member-:frown:"

#### roletools reaction create

* Usage: `!roletools reaction create <message> <emoji> <role>`
* Restricted to: `ADMIN`
* Aliases: `make and setup`

Create a reaction role\
\
can be the channel\_id-message\_id pair\
from copying message ID while holding SHIFT or a message link\
The emoji you want people to react with to get the role.\
The role you want people to receive for reacting.

### roletools selfadd

* Usage: `!roletools selfadd [true_or_false=None] <role>`
* Restricted to: `ADMIN`

Set whether or not a user can apply the role to themselves.\
\
\[true\_or\_false] optional boolean of what to set the setting to.\
If not provided the current setting will be shown instead.\
The role you want to set.

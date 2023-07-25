---
description: A collection of server administration utilities
---

# 🎟 Admin

## addrole

* Usage: `!addrole <rolename> [user]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Add a role to a user.\
\
Use double quotes if the role contains spaces.\
If user is left blank it defaults to the author of the command.

## removerole

* Usage: `!removerole <rolename> [user]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Remove a role from a user.\
\
Use double quotes if the role contains spaces.\
If user is left blank it defaults to the author of the command.

## editrole

* Usage: `!editrole`
* Restricted to: `ADMIN`
* Checks: `server_only`

Edit role settings.

### editrole colour

* Usage: `!editrole colour <role> <value>`
* Aliases: `color`

Edit a role's colour.\
\
Use double quotes if the role contains spaces.\
Colour must be in hexadecimal format.\
[Online colour picker](http://www.w3schools.com/colors/colors\_picker.asp)\
\
Examples:\
!editrole colour "The Transistor" #ff0000\
!editrole colour Test #ff9900

### editrole name

* Usage: `!editrole name <role> <name>`

Edit a role's name.\
\
Use double quotes if the role or the name contain spaces.\
\
Example:\
!editrole name "The Transistor" Test

## selfrole

* Usage: `!selfrole <selfrole>`
* Checks: `server_only`

Add or remove a selfrole from yourself.\
\
Server admins must have configured the role as user settable.\
NOTE: The role is case sensitive!

### selfrole list

* Usage: `!selfrole list`

Lists all available selfroles.

## selfroleset

* Usage: `!selfroleset`
* Restricted to: `ADMIN`

Manage selfroles.

### selfroleset clear

* Usage: `!selfroleset clear`

Clear the list of available selfroles for this server.

### selfroleset add

* Usage: `!selfroleset add <roles>`

Add a role, or a selection of roles, to the list of available selfroles.\
\
NOTE: The role is case sensitive!

### selfroleset remove

* Usage: `!selfroleset remove <roles>`

Remove a role, or a selection of roles, from the list of available selfroles.\
\
NOTE: The role is case sensitive!

---
description: >-
  Save, reward, and auto-congratulate birthdays in your server! Give community
  members a birthday role if you'd like!
---

# 🎉 Birthdays

### birthdaydebug upcoming

* Usage: `!birthdaydebug upcoming`

## bdset

* Usage: `!bdset`
* Restricted to: `ADMIN`
* Checks: `server_only`

Birthday management commands for admins.\
\
Looking to set your own birthday? Use !birthday set or !bday set.

### bdset settings

* Usage: `!bdset settings`

View your current settings

### bdset msgwithyear

* Usage: `!bdset msgwithyear <message>`

Set the message to send when the user did provide a year.\
\
If you would like to mention a role, you will need to run !bdset rolemention true\
\
**Placeholders:**\
\- {name} - the user's name\
\- {mention} - an @ mention of the user\
\- {new\_age} - the user's new age\
\
All the placeholders are optional.\
\
**Examples:**\
\- !bdset msgwithyear {mention} has turned {new\_age}, happy birthday!\
\- !bdset msgwithyear {name} is {new\_age} today! Happy birthday {mention}!

### bdset time

* Usage: `!bdset time <time>`

Set the time of day for the birthday message.\
\
Minutes are ignored.\
\
**Examples:**\
\- !bdset time 7:00 - set the time to 7:45AM UTC\
\- !bdset time 12AM - set the time to midnight UTC\
\- !bdset time 3PM - set the time to 3:00PM UTC

### bdset channel

* Usage: `!bdset channel <channel>`

Set the channel where the birthday message will be sent.\
\
**Example:**\
\- !bdset channel #birthdays - set the channel to #birthdays

### bdset rolemention

* Usage: `!bdset rolemention <value>`

Choose whether or not to allow role mentions in birthday messages.\
\
By default role mentions are suppressed.\
\
To allow role mentions in the birthday message, run !bdset rolemention true.\
Disable them with !bdset rolemention true

### bdset stop

* Usage: `!bdset stop`

Stop the cog from sending birthday messages and giving roles in the server.

### bdset role

* Usage: `!bdset role <role>`

Set the role that will be given to the user on their birthday.\
\
You can give the exact name or a mention.\
\
**Example:**\
\- !bdset role @Birthday - set the role to @Birthday\
\- !bdset role Birthday - set the role to @Birthday without a mention\
\- !bdset role 418058139913063657 - set the role with an ID

### bdset interactive

* Usage: `!bdset interactive`

Start interactive setup

### bdset msgwithoutyear

* Usage: `!bdset msgwithoutyear <message>`

Set the message to send when the user did not provide a year.\
\
If you would like to mention a role, you will need to run !bdset rolemention true.\
\
**Placeholders:**\
\- {name} - the user's name\
\- {mention} - an @ mention of the user\
\
All the placeholders are optional.\
\
**Examples:**\
\- !bdset msgwithoutyear Happy birthday {mention}!\
\- !bdset msgwithoutyear {mention}'s birthday is today! Happy birthday {name}.

### bdset force

* Usage: `!bdset force <user> <birthday>`

Force-set a specific user's birthday.\
\
You can @ mention any user or type out their exact name. If you're typing out a name with\
spaces, make sure to put quotes around it (").\
\
**Examples:**\
\- !bdset set @User 1-1-2000 - set the birthday of @User to 1/1/2000\
\- !bdset set User 1/1 - set the birthday of @User to 1/1/2000\
\- !bdset set "User with spaces" 1-1 - set the birthday of @User with spaces\
to 1/1\
\-]bdset set 354125157387344896 1/1/2000 - set the birthday of @User to 1/1/2000

## birthday (Hybrid Command)

* Usage: `!birthday`
* Slash Usage: `/birthday`
* Aliases: `bday`
* Checks: `server_only`

Set and manage your birthday.

### birthday remove (Hybrid Command)

* Usage: `!birthday remove`
* Slash Usage: `/birthday remove`
* Aliases: `delete and del`

Remove your birthday.

### birthday set (Hybrid Command)

* Usage: `!birthday set <birthday>`
* Slash Usage: `/birthday set <birthday>`
* Aliases: `add`

Set your birthday.\
\
You can optionally add in the year, if you are happy to share this.\
\
If you use a date in the format xx/xx/xx or xx-xx-xx MM-DD-YYYY is assumed.\
\
**Examples:**\
\- !bday set 24th September\
\- !bday set 24th Sept 2002\
\- !bday set 9/24/2002\
\- !bday set 9-24-2002\
\- !bday set 9-24

### birthday upcoming (Hybrid Command)

* Usage: `!birthday upcoming [days=7]`
* Slash Usage: `/birthday upcoming [days=7]`

View upcoming birthdays, defaults to 7 days.\
\
**Examples:**\
\- !birthday upcoming - default of 7 days\
\- !birthday upcoming 14 - 14 days

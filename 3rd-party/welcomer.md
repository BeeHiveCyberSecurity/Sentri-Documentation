---
description: Announce when users join or leave a server.
---

# Welcomer

## welcome

* Usage: `!welcome`
* Restricted to: `ADMIN`
* Aliases: `welcomeset`
* Checks: `server_only`

Get current Welcome settings.

### welcome channel

* Usage: `!welcome channel <channel>`

Sets the channel to be used for event notices.

### welcome ban

* Usage: `!welcome ban`

Change settings for ban notices.

#### welcome ban toggledelete

* Usage: `!welcome ban toggledelete [on_off=None]`

Turns deletion of previous ban notice on or off.\
\
If on\_off is not provided, the state will be flipped.

#### welcome ban message

* Usage: `!welcome ban message`
* Aliases: `msg`

Manage ban message formats.

**welcome ban message list**

* Usage: `!welcome ban message list`
* Aliases: `ls`

Lists the available ban message formats.

**welcome ban message delete**

* Usage: `!welcome ban message delete`
* Aliases: `del`

Delete an existing ban message format from the list.

**welcome ban message add**

* Usage: `!welcome ban message add <msg_format>`

Add a new ban message format to be chosen.\
\
Allows for the following customizations:\
{member} is the banned member\
{server} is the server\
{count} is the number of members who have been banned today\
{plural} is an 's' if count is not 1, and nothing if it is\
{roles} is a list of all the roles that the member has at the time\
\
For example:\
{member.name} was banned... What did you do???\
A member of {server.name} has been banned! {member.name}#{member.discriminator} - {member.id}\
Someone has been banned. Good riddance!

#### welcome ban toggle

* Usage: `!welcome ban toggle [on_off=None]`

Turns ban notices on or off.\
\
If on\_off is not provided, the state will be flipped.

#### welcome ban channel

* Usage: `!welcome ban channel [channel=None]`

Sets the channel to be used specifically for ban notices.\
\
If channel is not provided, the ban-specific channel is cleared.

### welcome unban

* Usage: `!welcome unban`

Change settings for unban notices.

#### welcome unban toggle

* Usage: `!welcome unban toggle [on_off=None]`

Turns unban notices on or off.\
\
If on\_off is not provided, the state will be flipped.

#### welcome unban channel

* Usage: `!welcome unban channel [channel=None]`

Sets the channel to be used specifically for unban notices.\
\
If channel is not provided, the unban-specific channel is cleared.

#### welcome unban toggledelete

* Usage: `!welcome unban toggledelete [on_off=None]`

Turns deletion of previous unban notice on or off.\
\
If on\_off is not provided, the state will be flipped.

#### welcome unban message

* Usage: `!welcome unban message`
* Aliases: `msg`

Manage unban message formats.

**welcome unban message delete**

* Usage: `!welcome unban message delete`
* Aliases: `del`

Delete an existing unban message format from the list.

**welcome unban message list**

* Usage: `!welcome unban message list`
* Aliases: `ls`

Lists the available unban message formats.

**welcome unban message add**

* Usage: `!welcome unban message add <msg_format>`

Add a new unban message format to be chosen.\
\
Allows for the following customizations:\
{member} is the unbanned member\
{server} is the server\
{count} is the number of members who have been unbanned today\
{plural} is an 's' if count is not 1, and nothing if it is\
{roles} is a list of all the roles that the member has at the time\
\
For example:\
{member.name} was unbanned... Did you learn your lesson???\
A member of {server.name} has been unbanned! {member.name}#{member.discriminator} - {member.id}\
Someone has been unbanned. Don't waste your second chance!

### welcome toggle

* Usage: `!welcome toggle [on_off=None]`

Turns Welcome on or off.\
\
If on\_off is not provided, the state will be flipped.

### welcome join

* Usage: `!welcome join`

Change settings for join notices.

#### welcome join botmessage

* Usage: `!welcome join botmessage [msg_format]`
* Aliases: `botmsg`

Sets the message format to use for join notices for bots.\
\
Supply no format to use normal join message formats for bots.\
Allows for the following customizations:\
{bot} is the bot\
{server} is the server\
{count} is the number of members who have joined today\
{plural} is an 's' if count is not 1, and nothing if it is\
\
For example:\
{bot.mention} beep boop.

#### welcome join message

* Usage: `!welcome join message`
* Aliases: `msg`

Manage join message formats.

**welcome join message add**

* Usage: `!welcome join message add <msg_format>`

Add a new join message format to be chosen.\
\
Allows for the following customizations:\
{member} is the new member\
{server} is the server\
{count} is the number of members who have joined today\
{plural} is an 's' if count is not 1, and nothing if it is\
{roles} is a list of all the roles that the member has at the time\
\
For example:\
{member.mention}... What are you doing here???\
{server.name} has a new member! {member.name}#{member.discriminator} - {member.id}\
Someone new has joined! Who is it?! D: IS HE HERE TO HURT US?!

**welcome join message list**

* Usage: `!welcome join message list`
* Aliases: `ls`

Lists the available join message formats.

**welcome join message delete**

* Usage: `!welcome join message delete`
* Aliases: `del`

Delete an existing join message format from the list.

#### welcome join channel

* Usage: `!welcome join channel [channel=None]`

Sets the channel to be used specifically for join notices.\
\
If channel is not provided, the join-specific channel is cleared.

#### welcome join toggledelete

* Usage: `!welcome join toggledelete [on_off=None]`

Turns deletion of previous join notice on or off.\
\
If on\_off is not provided, the state will be flipped.

#### welcome join whisper

* Usage: `!welcome join whisper`

Change settings for join whispers.

**welcome join whisper type**

* Usage: `!welcome join whisper type <choice>`

Set if a DM is sent to the new member.\
\
Options:\
off - no DM is sent\
only - only send a DM to the member, do not send a message to the channel\
both - send a DM to the member and a message to the channel\
fall - send a DM to the member, if it fails send the whisper message to the channel instead

**welcome join whisper message**

* Usage: `!welcome join whisper message <msg_format>`
* Aliases: `msg`

Set the message DM'd to new members when they join.\
\
Allows for the following customizations:\
{member} is the member who joined\
{server} is the server

#### welcome join toggle

* Usage: `!welcome join toggle [on_off=None]`

Turns join notices on or off.\
\
If on\_off is not provided, the state will be flipped.

### welcome leave

* Usage: `!welcome leave`

Change settings for leave notices.

#### welcome leave toggle

* Usage: `!welcome leave toggle [on_off=None]`

Turns leave notices on or off.\
\
If on\_off is not provided, the state will be flipped.

#### welcome leave channel

* Usage: `!welcome leave channel [channel=None]`

Sets the channel to be used specifically for leave notices.\
\
If channel is not provided, the leave-specific channel is cleared.

#### welcome leave toggledelete

* Usage: `!welcome leave toggledelete [on_off=None]`

Turns deletion of previous leave notice on or off.\
\
If on\_off is not provided, the state will be flipped.

#### welcome leave message

* Usage: `!welcome leave message`
* Aliases: `msg`

Manage leave message formats.

**welcome leave message delete**

* Usage: `!welcome leave message delete`
* Aliases: `del`

Delete an existing leave message format from the list.

**welcome leave message list**

* Usage: `!welcome leave message list`
* Aliases: `ls`

Lists the available leave message formats.

**welcome leave message add**

* Usage: `!welcome leave message add <msg_format>`

Add a new leave message format to be chosen.\
\
Allows for the following customizations:\
{member} is the member who left\
{server} is the server\
{count} is the number of members who have left today\
{plural} is an 's' if count is not 1, and nothing if it is\
{roles} is a list of all the roles that the member has at the time\
\
For example:\
{member.name}... Why did you leave???\
{server.name} has lost a member! {member.name}#{member.discriminator} - {member.id}\
Someone has left... Aww... Bye :(

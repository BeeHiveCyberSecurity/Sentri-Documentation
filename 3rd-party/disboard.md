---
description: Set a reminder to bump on Disboard.
---

# DISBOARD

## bumpreminder

* Usage: `!bumpreminder`
* Restricted to: `ADMIN`
* Aliases: `bprm`
* Checks: `server_only`

Set a reminder to bump on Disboard.\
\
This sends a reminder to bump in a specified channel 2 hours after someone successfully bumps, thus making it more accurate than a repeating schedule.

### bumpreminder message

* Usage: `!bumpreminder message [message]`

Change the message used for reminders. Providing no message will reset to the default message.

### bumpreminder channel

* Usage: `!bumpreminder channel [channel=None]`

Set the channel to send bump reminders to.\
\
This also works as a toggle, so if no channel is provided, it will disable reminders for this server.

### bumpreminder clean

* Usage: `!bumpreminder clean [true_or_false=None]`

Toggle whether Sentri should keep the bump channel "clean."\
\
Sentri will remove all failed invoke messages by Disboard.

### bumpreminder thankyou

* Usage: `!bumpreminder thankyou [message]`
* Aliases: `ty`

Change the message used for 'Thank You' messages. Providing no message will reset to the default message.\
\
The thank you message supports TagScript blocks which can customize the message and even add an embed!\
[View the TagScript documentation here.](https://phen-cogs.readthedocs.io/en/latest/index.html)\
\
Variables:\
{member} - [The user who bumped](https://phen-cogs.readthedocs.io/en/latest/tags/default\_variables.html#author-block)\
{server} - [This server](https://phen-cogs.readthedocs.io/en/latest/tags/default\_variables.html#server-block)\
\
Blocks:\
embed - [Embed to be sent in the thank you message](https://phen-cogs.readthedocs.io/en/latest/tags/parsing\_blocks.html#embed-block)\
\
**Examples:**\
\> !bprm ty Thanks {member} for bumping! You earned 10 brownie points from phen!\
\> !bprm ty {embed(description):{member(mention)}, thank you for bumping! Make sure to vote for **{server}** on [our voting page](https://disboard.org/server/%7Bserver\(id\)%7D).}

### bumpreminder pingrole

* Usage: `!bumpreminder pingrole [role=None]`

Set a role to ping for bump reminders.\
\
If no role is provided, it will clear the current role.

### bumpreminder lock

* Usage: `!bumpreminder lock [true_or_false=None]`

Toggle whether the bot should automatically lock/unlock the bump channel.

### bumpreminder settings

* Usage: `!bumpreminder settings`

Show your Bump Reminder settings.

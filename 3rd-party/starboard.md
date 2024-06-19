---
description: >-
  Vote to preserve your communities most iconic chat messages in a rolling
  channel for all to review and laugh at.
---

# Starboard

## starboard

* Usage: `!starboard`
* Restricted to: `ADMIN`
* Checks: `server_only`

Commands for managing the starboard

### starboard channel

* Usage: `!starboard channel <starboard> <channel>`
* Aliases: `channels`

Change the channel that the starboard gets posted to\
\
is the name of the starboard to adjust\
The channel of the starboard.

### starboard blocklist

* Usage: `!starboard blocklist`
* Aliases: `blacklist`

Add/Remove channels/roles from the blocklist

#### starboard blocklist add

* Usage: `!starboard blocklist add <starboard> <channel_or_role>`

Add a channel to the starboard blocklist\
\
is the name of the starboard to adjust\
\<channel\_or\_role> is the channel or role you would like to add to the blocklist

#### starboard blocklist remove

* Usage: `!starboard blocklist remove <starboard> <channel_or_role>`

Remove a channel to the starboard blocklist\
\
is the name of the starboard to adjust\
\<channel\_or\_role> is the channel or role you would like to remove from the blocklist

### starboard selfstar

* Usage: `!starboard selfstar <starboard>`

Toggle whether or not a user can star their own post\
\
is the name of the starboard to toggle

### starboard emoji

* Usage: `!starboard emoji <starboard> <emoji>`

Set the emoji for the starboard\
\
is the name of the starboard to change the emoji for\
must be an emoji on the server or a default emoji

### starboard cleanup

* Usage: `!starboard cleanup`

Cleanup stored deleted channels or roles in the blocklist/allowlist

### starboard toggle

* Usage: `!starboard toggle <starboard>`

Toggle a starboard on/off\
\
is the name of the starboard to toggle

### starboard remove

* Usage: `!starboard remove <starboard>`
* Aliases: `delete and del`

Remove a starboard from the server\
\
is the name for the starboard and will be lowercase only

### starboard threshold

* Usage: `!starboard threshold <starboard> <threshold>`

Set the threshold before posting to the starboard\
\
is the name of the starboard to change the threshold for\
must be a number of reactions before a post gets\
moved to the starboard

### starboard create

* Usage: `!starboard create <name> [channel=None] [emoji=⭐]`
* Aliases: `add`

Create a starboard on this server\
\
is the name for the starboard and will be lowercase only\
\[channel] is the channel where posts will be made defaults to current channel\
\[emoji=⭐] is the emoji that will be used to add to the starboard defaults to ⭐

### starboard autostar

* Usage: `!starboard autostar <starboard>`

Toggle whether or not the bot will add the emoji automatically to the starboard message.\
\
is the name of the starboard to toggle

### starboard colour

* Usage: `!starboard colour <starboard> <colour>`
* Aliases: `color`

Change the default colour for a starboard\
\
is the name of the starboard to toggle\
The colour to use for the starboard embed\
This can be a hexcode or integer for colour or author/member/user to use\
the original posters colour or bot to use the bots colour.\
Colour also accepts names from\
[discord.py](https://discordpy.readthedocs.io/en/latest/api.html#colour)

### starboard inherit

* Usage: `!starboard inherit <starboard>`

Set whether to inherit the parent channels blocklist/allowlist settings.\
If this is enabled then starred messages in threads and forum channels\
will be filtered based on their parent channels blocklist/allowlist settings.\
e.g. if a message is starred in a thread and the parent channel is in the blocklist\
the message will not be starred.\
\
is the name of the starboard to adjust

### starboard info

* Usage: `!starboard info`
* Aliases: `list`

Display info on starboards setup on the server.

### starboard allowlist

* Usage: `!starboard allowlist`
* Aliases: `whitelist`

Add/Remove channels/roles from the allowlist

#### starboard allowlist remove

* Usage: `!starboard allowlist remove <starboard> <channel_or_role>`

Remove a channel to the starboard allowlist\
\
is the name of the starboard to adjust\
\<channel\_or\_role> is the channel or role you would like to remove from the allowlist

#### starboard allowlist add

* Usage: `!starboard allowlist add <starboard> <channel_or_role>`

Add a channel to the starboard allowlist\
\
is the name of the starboard to adjust\
\<channel\_or\_role> is the channel or role you would like to add to the allowlist

## star

* Usage: `!star <starboard> <message>`
* Checks: `server_only`

Manually star a message\
\
is the name of the starboard you would like to add the message to\
is the message ID, channel\_id-message\_id, or a message link\
of the message you want to star

## unstar

* Usage: `!unstar <starboard> <message>`
* Checks: `server_only`

Manually unstar a message\
\
is the name of the starboard you would like to add the message to\
is the message ID, channe\_id-message\_id, or a message link\
of the message you want to unstar

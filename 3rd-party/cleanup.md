---
description: Tools for cleaning up messages within your server
---

# Cleanup



## cleanup

* Usage: `!cleanup`

Base command for deleting messages.

### cleanup messages

* Usage: `!cleanup messages <number> [delete_pinned=False]`
* Restricted to: `MOD`
* Checks: `server_only`

Delete the last X messages in the current channel.\
\
Example:\
\- !cleanup messages 26\
\
**Arguments:**\
\
\- The max number of messages to cleanup. Must be a positive integer.\
\- \<delete\_pinned> Whether to delete pinned messages or not. Defaults to False

### cleanup user

* Usage: `!cleanup user <user> <number> [delete_pinned=False]`
* Restricted to: `MOD`
* Checks: `server_only`

Delete the last X messages from a specified user in the current channel.\
\
Examples:\
\- !cleanup user @Twentysix 2\
\- !cleanup user Red 6\
\
**Arguments:**\
\
\- The user whose messages are to be cleaned up.\
\- The max number of messages to cleanup. Must be a positive integer.\
\- \<delete\_pinned> Whether to delete pinned messages or not. Defaults to False

### cleanup between

* Usage: `!cleanup between <one> <two> [delete_pinned=False]`
* Restricted to: `MOD`
* Checks: `server_only`

Delete the messages between Message One and Message Two, providing the messages IDs.\
\
The first message ID should be the older message and the second one the newer.\
\
Example:\
\- !cleanup between 123456789123456789 987654321987654321\
\
**Arguments:**\
\
\- The id of the message to cleanup after. This message won't be deleted.\
\- The id of the message to cleanup before. This message won't be deleted.\
\- \<delete\_pinned> Whether to delete pinned messages or not. Defaults to False

### cleanup text

* Usage: `!cleanup text <text> <number> [delete_pinned=False]`
* Restricted to: `MOD`
* Checks: `server_only`

Delete the last X messages matching the specified text in the current channel.\
\
Example:\
\- !cleanup text "test" 5\
\
Remember to use double quotes.\
\
**Arguments:**\
\
\- The max number of messages to cleanup. Must be a positive integer.\
\- \<delete\_pinned> Whether to delete pinned messages or not. Defaults to False

### cleanup self

* Usage: `!cleanup self <number> [match_pattern=None] [delete_pinned=False]`

Clean up messages owned by the bot in the current channel.\
\
By default, all messages are cleaned. If a second argument is specified,\
it is used for pattern matching - only messages containing the given text will be deleted.\
\
Examples:\
\- !cleanup self 6\
\- !cleanup self 10 Pong\
\- !cleanup self 7 "" True\
\
**Arguments:**\
\
\- The max number of messages to cleanup. Must be a positive integer.\
\- \<match\_pattern> The text that messages must contain to be deleted. Use "" to skip this.\
\- \<delete\_pinned> Whether to delete pinned messages or not. Defaults to False

### cleanup bot

* Usage: `!cleanup bot <number> [delete_pinned=False]`
* Restricted to: `MOD`
* Checks: `server_only`

Clean up command messages and messages from the bot in the current channel.\
\
Can only cleanup custom commands and alias commands if those cogs are loaded.\
\
**Arguments:**\
\
\- The max number of messages to cleanup. Must be a positive integer.\
\- \<delete\_pinned> Whether to delete pinned messages or not. Defaults to False

### cleanup duplicates

* Usage: `!cleanup duplicates [number=50]`
* Restricted to: `MOD`
* Aliases: `spam`
* Checks: `server_only`

Deletes duplicate messages in the channel from the last X messages and keeps only one copy.\
\
Defaults to 50.\
\
**Arguments:**\
\
\- The number of messages to check for duplicates. Must be a positive integer.

### cleanup after

* Usage: `!cleanup after <message_id> [delete_pinned=False]`
* Restricted to: `MOD`
* Checks: `server_only`

Delete all messages after a specified message.\
\
To get a message id, enable developer mode in Discord's\
settings, 'appearance' tab. Then right click a message\
and copy its id.\
Replying to a message will cleanup all messages after it.\
\
**Arguments:**\
\
\- \<message\_id> The id of the message to cleanup after. This message won't be deleted.\
\- \<delete\_pinned> Whether to delete pinned messages or not. Defaults to False

### cleanup before

* Usage: `!cleanup before <message_id> <number> [delete_pinned=False]`
* Restricted to: `MOD`
* Checks: `server_only`

Deletes X messages before the specified message.\
\
To get a message id, enable developer mode in Discord's\
settings, 'appearance' tab. Then right click a message\
and copy its id.\
Replying to a message will cleanup all messages before it.\
\
**Arguments:**\
\
\- \<message\_id> The id of the message to cleanup before. This message won't be deleted.\
\- The max number of messages to cleanup. Must be a positive integer.\
\- \<delete\_pinned> Whether to delete pinned messages or not. Defaults to False

## cleanupset

* Usage: `!cleanupset`
* Restricted to: `ADMIN`

Manage the settings for the cleanup command.

### cleanupset notify

* Usage: `!cleanupset notify`
* Checks: `server_only`

Toggle clean up notification settings.\
\
When enabled, a message will be sent per cleanup, showing how many messages were deleted.\
This message will be deleted after 5 seconds.

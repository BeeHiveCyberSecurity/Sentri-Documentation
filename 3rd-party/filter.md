---
description: >-
  This cog is designed for "filtering" unwanted words and phrases from a server.
  It provides tools to manage a list of words or sentences, and to customize
  automatic actions to be taken against.
---

# Filter

## filterset

* Usage: `!filterset`
* Restricted to: `ADMIN`
* Checks: `server_only`

Base command to manage filter settings.

### filterset ban

* Usage: `!filterset ban <count> <timeframe>`

Set the filter's autoban conditions.\
\
Users will be banned if they send filtered words in\
seconds.\
\
Set both to zero to disable autoban.\
\
Examples:\
\- !filterset ban 5 5 - Ban users who say 5 filtered words in 5 seconds.\
\- !filterset ban 2 20 - Ban users who say 2 filtered words in 20 seconds.\
\
**Arguments:**\
\
\- The amount of filtered words required to trigger a ban.\
\- The period of time in which too many filtered words will trigger a ban.

### filterset defaultname

* Usage: `!filterset defaultname <name>`

Set the nickname for users with a filtered name.\
\
Note that this has no effect if filtering names is disabled\
(to toggle, run !filter names).\
\
The default name used is _John Doe_.\
\
Example:\
\- !filterset defaultname Missingno\
\
**Arguments:**\
\
\- The new nickname to assign.

## filter

* Usage: `!filter`
* Restricted to: `MOD`
* Checks: `server_only`

Base command to add or remove words from the server filter.\
\
Use double quotes to add or remove sentences.

### filter channel

* Usage: `!filter channel`

Base command to add or remove words from the channel filter.\
\
Use double quotes to add or remove sentences.

#### filter channel delete

* Usage: `!filter channel delete <channel> <words>`
* Aliases: `remove and del`

Remove words from the filter.\
\
Use double quotes to remove sentences.\
\
Examples:\
\- !filter channel remove #channel word1 word2 word3\
\- !filter channel remove #channel "This is a sentence"\
\
**Arguments:**\
\
\- The text, voice, stage, or forum channel to add filtered words to.\
\- \[words...] The words or sentences to no longer filter.

#### filter channel clear

* Usage: `!filter channel clear`

Clears this channel's filter list.

#### filter channel list

* Usage: `!filter channel list`

Send a list of the channel's filtered words.

#### filter channel add

* Usage: `!filter channel add <channel> <words>`

Add words to the filter.\
\
Use double quotes to add sentences.\
\
Examples:\
\- !filter channel add #channel word1 word2 word3\
\- !filter channel add #channel "This is a sentence"\
\
**Arguments:**\
\
\- The text, voice, stage, or forum channel to add filtered words to.\
\- \[words...] The words or sentences to filter.

### filter list

* Usage: `!filter list`

Send a list of this server's filtered words.

### filter add

* Usage: `!filter add <words>`

Add words to the filter.\
\
Use double quotes to add sentences.\
\
Examples:\
\- !filter add word1 word2 word3\
\- !filter add "This is a sentence"\
\
**Arguments:**\
\
\- \[words...] The words or sentences to filter.

### filter delete

* Usage: `!filter delete <words>`
* Aliases: `remove and del`

Remove words from the filter.\
\
Use double quotes to remove sentences.\
\
Examples:\
\- !filter remove word1 word2 word3\
\- !filter remove "This is a sentence"\
\
**Arguments:**\
\
\- \[words...] The words or sentences to no longer filter.

### filter clear

* Usage: `!filter clear`

Clears this server's filter list.

### filter names

* Usage: `!filter names`

Toggle name and nickname filtering.\
\
This is disabled by default.

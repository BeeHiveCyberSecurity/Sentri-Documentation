---
description: Protects users against phishing attacks
---

# 🐟 AntiPhishing

## checkphish

* Usage: `!checkphish [url=None]`
* Aliases: `checkforphish, checkscam, checkforscam, and checkphishing`

Check if a url is a phishing scam.\
\
You can either provide a url or reply to a message containing a url.

## antiphishing

* Usage: `!antiphishing`
* Restricted to: `ADMIN`
* Aliases: `antiphish`
* Checks: `server_only`

Settings to set up the anti-phishing integration.

### antiphishing action

* Usage: `!antiphishing action <action>`

Choose the action that occurs when a user sends a phishing scam.\
\
Options:\
ignore - Disables the anti-phishing integration (default)\
notify - Sends a message to the channel and says it's a phishing scam\
delete - Deletes the message\
kick - Kicks the author (also deletes the message)\
ban - Bans the author (also deletes the message)

### antiphishing stats

* Usage: `!antiphishing stats`

Shows the current stats for the anti-phishing integration.

---
description: >-
  Guard users from malicious links and phishing attempts with customizable
  protection options.
---

# AntiPhishing

## checkphish

* Usage: `!checkphish [url=None]`
* Aliases: `checkforphish, checkscam, checkforscam, and checkphishing`

Check if a url is a phishing scam.\
\
You can either provide a url or reply to a message containing a url.

## antiphishing

* Usage: `!antiphishing`
* Aliases: `antiphish`
* Checks: `server_only`

Settings to configure phishing protection in this server.

### antiphishing action

* Usage: `!antiphishing action <action>`

Choose the action that occurs when a user sends a phishing scam.\
\
Options:\
**ignore** - Disables phishing protection\
**notify** - Alerts in channel when malicious links detected (default)\
**delete** - Deletes the message\
**kick** - Delete message and kick sender\
**ban** - Delete message and ban sender (recommended)

### antiphishing stats

* Usage: `!antiphishing stats`

Check protection statistics for this server

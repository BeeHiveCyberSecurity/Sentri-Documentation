---
description: >-
  Stop members from clogging your channels with pointless rich presence
  interactions
---

# 🔆 AntiRichPresence

## antirp

* Usage: `!antirp`
* Restricted to: `ADMIN`

Manage the settings for AntiRP

### antirp whitelist

* Usage: `!antirp whitelist`

Manage the application whitelist for AntiRP\
\
When an application is added to the whitelist,\
any other applications not matching the name will be removed.\
Regardless if the permissions are valid.\
\
Even though Spotify isn't an application it can be added as a whitelisted application

#### antirp whitelist list

* Usage: `!antirp whitelist list`

List all the whitelisted applications

#### antirp whitelist add

* Usage: `!antirp whitelist add <application_name>`

Add a new whitelisted application

#### antirp whitelist remove

* Usage: `!antirp whitelist remove <application_name>`

Remove a whitelisted application

#### antirp whitelist clear

* Usage: `!antirp whitelist clear`

Remove all whitelisted applications

### antirp grabname

* Usage: `!antirp grabname <channel> <messageID>`

Grab an application name via RP Invite

### antirp toggle

* Usage: `!antirp toggle [true_or_false=None]`

Toggle AntiRP on or off

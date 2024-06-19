---
description: Create user reports that server staff can respond to.
---

# 📧 Reports

Report system\
\
Members can type `[p]report <user> <reason>` and it'll show up in your selected channel!

## reportdm

* Usage: `!reportdm`
* Cooldown: `1 per 15.0 seconds`
* Checks: `server_only`

Enables/Disables the messages the bot sends on report\
\
By default this changes depending on your current setting.

## report

* Usage: `!report <member> <reason>`
* Cooldown: `2 per 15.0 seconds`
* Checks: `server_only`

Report a member\
\
Example: !report @SharkyTheKing#0001 Not being fishy enough.\
\
Arguments:\
member: The Discord member you want to report\
reason: The reason for the report

## reportset

* Usage: `!reportset`
* Restricted to: `MOD`

Manage reports system

### reportset channel

* Usage: `!reportset channel <channel>`

Sets the channel where reports will be posted into

### reportset list

* Usage: `!reportset list`

Displays report settings

### reportset emotes

* Usage: `!reportset emotes <toggle>`

Sets it whether the bot automatically puts reactions for each report sent\
\
Up is confirming it's a valid report\
Down is confirming it's not a valid report\
Question means you're unsure of the report or are in question of it\
X means it's been too long to look into

### reportset reportclaim

* Usage: `!reportset reportclaim <toggle>`

Toggle report to be claimed.\
\
If this is toggled on, any reaction on any reports is immediately claimed by the moderator.

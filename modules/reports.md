---
description: Create user reports that server staff can respond to.
---

# 📧 Reports

### Usage[¶](broken-reference)

Users can open reports using `[p]report`. These are then sent to a channel in the server for staff, and the report creator gets a DM. Both can be used to communicate.

### Commands[¶](broken-reference)

## reportset

* Usage: `!reportset`
* Restricted to: `ADMIN`
* Checks: `server_only`

Manage Reports.

### reportset output

* Usage: `!reportset output <channel>`
* Restricted to: `ADMIN`

Set the channel where reports will be sent.

### reportset toggle

* Usage: `!reportset toggle`
* Restricted to: `ADMIN`
* Aliases: `toggleactive`

Enable or disable reporting for this server.

## report

* Usage: `!report [_report]`

Send a report.\
\
Use without arguments for interactive reporting, or do\
!report \[text] to use it non-interactively.

### report interact

* Usage: `!report interact <ticket_number>`
* Restricted to: `MOD`
* Checks: `server_only`

Open a message tunnel.\
\
This tunnel will forward things you say in this channel or thread\
to the ticket opener's direct messages.\
\
Tunnels do not persist across bot restarts.

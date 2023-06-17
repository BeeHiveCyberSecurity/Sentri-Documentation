---
description: Issue timeouts to individual members or entire roles
---

# 🕐 Timeout

## timeout

* Usage: `!timeout <member_or_role> [time=None] [reason]`
* Restricted to: `ADMIN`
* Aliases: `tt`
* Cooldown: `1 per 1.0 second`
* Checks: `server_only`

Timeout users.\
\
\<member\_or\_role> is the username/rolename, ID or mention. If provided a role,\
everyone with that role will be timedout.\
\[time] is the time to mute for. Time is any valid time length such as 45 minutes\
or 3 days. If nothing is provided the timeout will be 60 seconds default.\
\[reason] is the reason for the timeout. Defaults to None if nothing is provided.\
\
Examples:\
!timeout @member 5m talks too much\
!timeout @member 10m

## untimeout

* Usage: `!untimeout <member_or_role> [reason]`
* Restricted to: `ADMIN`
* Aliases: `utt`
* Cooldown: `1 per 1.0 second`
* Checks: `server_only`

Untimeout users.\
\
\<member\_or\_role> is the username/rolename, ID or mention. If\
provided a role, everyone with that role will be untimed.\
\[reason] is the reason for the untimeout. Defaults to None\
if nothing is provided.

## timeoutset

* Usage: `!timeoutset`
* Restricted to: `ADMIN`
* Checks: `server_only`

Manage timeout settings.

### timeoutset showmoderator

* Usage: `!timeoutset showmoderator`
* Aliases: `showmod`

Change whether to show moderator on DM's or not.

### timeoutset dm

* Usage: `!timeoutset dm`

Change whether to DM the user when they are timed out.

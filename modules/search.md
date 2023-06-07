---
description: Search your entire Discord, customizably.
---

# 🔍 Search

## discordsearch (Hybrid Command)

* Usage: `!discordsearch <channel> <args>`
* Slash Usage: `/discordsearch <channel> <args>`
* Restricted to: `ADMIN`
* Aliases: `dsearch`
* Cooldown: `3 per 30.0 seconds`
* Checks: `server_only`

Search for a message on Discord in a channel.\
\
Warning: The bot uses the api for each search.\
Arguments:\
\--author @user1 --author user2#1234 --author 0123456789\
\--mention @user1 --mention user2#1234 --mention 0123456789\
\--before now\
\--after "25/12/2000 00h00"\
\--pinned true\
\--content "super important secrets"\
\--regex "\[p]"\
\--contain link --contain embed --contain file\
\--limit 100

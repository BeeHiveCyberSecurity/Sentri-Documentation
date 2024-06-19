---
description: Customizable per-server suggestions capabilities
---

# IdeaBoard

## idea (Hybrid Command)

* Usage: `!idea <content>`
* Slash Usage: `/idea <content>`
* Aliases: `suggest`
* Checks: `bot_has_server_permissions and server_only`

Share an idea/make a suggestion.

## ideastats (Hybrid Command)

* Usage: `!ideastats [member]`
* Slash Usage: `/ideastats [member]`
* Checks: `server_only`

Display your current profile stats for suggestions and votes.

## ideaset

* Usage: `!ideaset`
* Restricted to: `ADMIN`
* Aliases: `ideaboard`

Manage IdeaBoard settings

### ideaset userblacklist

* Usage: `!ideaset userblacklist <member>`
* Aliases: `blacklistuser and userbl`

Add/remove a user to/from the user blacklist

### ideaset upvoteemoji

* Usage: `!ideaset upvoteemoji <emoji>`
* Aliases: `upvote and up`

Set the upvote emoji

### ideaset voterole

* Usage: `!ideaset voterole <role>`

Add/remove a role to the voting role whitelist

### ideaset cooldown

* Usage: `!ideaset cooldown <cooldown>`
* Aliases: `cd`

Set the base cooldown for making suggestions

### ideaset toggledm

* Usage: `!ideaset toggledm`
* Aliases: `dm`

Toggle DMing users the results of suggestions they made

### ideaset suggestrole

* Usage: `!ideaset suggestrole <role>`

Add/remove a role to the suggest role whitelist

### ideaset roleblacklist

* Usage: `!ideaset roleblacklist <role>`
* Aliases: `blacklistrole and rolebl`

Add/remove a role to/from the role blacklist

### ideaset view

* Usage: `!ideaset view`

View IdeaBoard settings

### ideaset toggleanonymous

* Usage: `!ideaset toggleanonymous`
* Aliases: `toggleanon, anonymous, and anon`

Toggle allowing anonymous suggestions

### ideaset jointime

* Usage: `!ideaset jointime <to_vote> <to_suggest>`

Set the minimum time a user must be in the server to vote and suggest.\
\
Args:\
to\_vote: Minimum time in hours required to vote.\
to\_suggest: Minimum time in hours required to suggest.

### ideaset togglereveal

* Usage: `!ideaset togglereveal`
* Aliases: `reveal`

Toggle reveal suggestion author on approval\
\
Approved suggestions are ALWAYS revealed regardless of this setting.

### ideaset downvoteemoji

* Usage: `!ideaset downvoteemoji <emoji>`
* Aliases: `downvote and down`

Set the downvote emoji

### ideaset togglevotecount

* Usage: `!ideaset togglevotecount`
* Aliases: `votecount`

Toggle showing vote counts on suggestions

### ideaset accountage

* Usage: `!ideaset accountage <to_vote> <to_suggest>`

Set the minimum account age required to vote and suggest.\
\
Args:\
to\_vote: Minimum age in hours required to vote.\
to\_suggest: Minimum age in hours required to suggest.

### ideaset approverole

* Usage: `!ideaset approverole <role>`

Add/remove a role to the approver role list

### ideaset channel

* Usage: `!ideaset channel <channel> <channel_type>`

Set the approved, rejected, or pending channels for IdeaBoard

### ideaset minplaytime

* Usage: `!ideaset minplaytime <to_vote> <to_suggest>`

Set the ArkTools integration minimum playtime required to vote and suggest.\
\
Args:\
to\_vote: Minimum playtime in hours required to vote.\
to\_suggest: Minimum playtime in hours required to suggest.

### ideaset minlevel

* Usage: `!ideaset minlevel <to_vote> <to_suggest>`

Set the LevelUp integration minimum level required to vote and suggest.\
\
Args:\
to\_vote: Minimum level required to vote.\
to\_suggest: Minimum level required to suggest.

### ideaset rolecooldown

* Usage: `!ideaset rolecooldown <role> <cooldown>`
* Aliases: `rolecd`

Set the suggestion cooldown for a specific role\
\
To remove a role cooldown, specify 0 as the cooldown.

## approve (Hybrid Command)

* Usage: `!approve <number> [reason]`
* Slash Usage: `/approve <number> [reason]`
* Checks: `server_only`

Approve an idea/suggestion.

## reject (Hybrid Command)

* Usage: `!reject <number> [reason]`
* Slash Usage: `/reject <number> [reason]`
* Checks: `server_only`

Reject an idea/suggestion.

## viewvotes (Hybrid Command)

* Usage: `!viewvotes <number>`
* Slash Usage: `/viewvotes <number>`
* Checks: `server_only`

View the list of who has upvoted and who has downvoted a suggestion.

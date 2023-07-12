---
description: Get RSS feeds inside your server.
---

# \* RSS

## rss

* Usage: `!rss`
* Restricted to: `MOD`
* Checks: `server_only`

RSS feed stuff.

### rss listall

* Usage: `!rss listall`

List all saved feeds for this server.

### rss limit

* Usage: `!rss limit <feed_name> [channel=None] [character_limit=None]`

Set a character limit for feed posts. Use 0 for unlimited.\
\
RSS posts are naturally split at around 2000 characters to fit within the Discord character limit per message.\
If you only want the first embed or first message in a post feed to show, use 2000 or less characters for this setting.\
\
Note that this setting applies the character limit to the entire post, for all template values on the feed together.\
For example, if the template is $title\n$content\n$link, and title + content + link is longer than the limit, the link will not show.

### rss find

* Usage: `!rss find <website_url>`

Attempts to find RSS feeds from a URL/website.\
\
The site must have identified their feed in the html of the page based on RSS feed type standards.

### rss force

* Usage: `!rss force <feed_name> [channel=None]`

Forces a feed alert.

### rss listtags

* Usage: `!rss listtags <feed_name> [channel=None]`

List the tags available from a specific feed.

### rss add

* Usage: `!rss add <feed_name> [channel=None] <url>`

Add an RSS feed to a channel.\
\
Defaults to the current channel if no channel is specified.

### rss list

* Usage: `!rss list [channel=None]`

List saved feeds for this channel or a specific channel.

### rss showtemplate

* Usage: `!rss showtemplate <feed_name> [channel=None]`

Show the template in use for a specific feed.

### rss remove

* Usage: `!rss remove <feed_name> [channel=None]`
* Aliases: `delete and del`

Removes a feed from a channel.\
\
Defaults to the current channel if no channel is specified.

### rss tag

* Usage: `!rss tag`

RSS post tag qualification.

#### rss tag allow

* Usage: `!rss tag allow <feed_name> [channel=None] [tag]`

Set an allowed tag for a feed to be posted. The tag must match exactly (without regard to title casing).\
No regex or placeholder qualification.\
\
Tags can be found in !rss listtags under $tags or $tags\_list (if tags are present in the feed - not all feeds have tags).

#### rss tag allowlist

* Usage: `!rss tag allowlist <feed_name> [channel=None]`

List allowed tags for feed post qualification.

#### rss tag remove

* Usage: `!rss tag remove <feed_name> [channel=None] [tag]`
* Aliases: `delete`

Remove a tag from the allow list. The tag must match exactly (without regard to title casing).\
No regex or placeholder qualification.

### rss embed

* Usage: `!rss embed`

Embed feed settings.

#### rss embed toggle

* Usage: `!rss embed toggle <feed_name> [channel=None]`

Toggle whether a feed is sent in an embed or not.\
\
If the bot doesn't have permissions to post embeds,\
the feed will always be plain text, even if the embed\
toggle is set.

#### rss embed thumbnail

* Usage: `!rss embed thumbnail <feed_name> [channel=None] [thumbnail_tag_name=None]`

Set a tag to be a thumbnail image.\
\
This thumbnail will be applied to the first embed in the paginated list.\
Use this command with no thumbnail\_tag\_name to clear the embed thumbnail.

#### rss embed color

* Usage: `!rss embed color <feed_name> [channel=None] [color]`
* Aliases: `colour`

Set an embed color for a feed.\
\
Use this command with no color to reset to the default.\
color must be a hex code like #990000, a [Discord color name](https://discordpy.readthedocs.io/en/latest/api.html#colour),\
or a [CSS3 color name](https://www.w3.org/TR/2018/REC-css-color-3-20180619/#svg-color).

#### rss embed image

* Usage: `!rss embed image <feed_name> [channel=None] [image_tag_name=None]`

Set a tag to be a large embed image.\
\
This image will be applied to the last embed in the paginated list.\
Use this command with no image\_tag\_name to clear the embed image.

### rss template

* Usage: `!rss template <feed_name> [channel=None] [template]`

Set a template for the feed alert.\
\
Each variable must start with $, valid variables can be found with !rss listtags.



## rssnotifier

* Usage: `!rssnotifier`
* Checks: `server_only`

RSSNotifier settings.

### rssnotifier listroles

* Usage: `!rssnotifier listroles <feed_name> [channel=None]`

List role mentions list for the given feed name.\
\
Use !rss list for the list of available feeds.

### rssnotifier optin

* Usage: `!rssnotifier optin <feed_name> [channel=None]`
* Checks: `single_user_pings_enabled`

Opt-in receiving notifications for the given feed name.\
\
Use !rss list for the list of available feeds.

### rssnotifier addroles

* Usage: `!rssnotifier addroles <feed_name> <channel> <roles>`
* Aliases: `addrole`

Add roles that should be mentioned when new message for given feed is sent.\
\
Use !rss list for the list of available feeds.

### rssnotifier removeroles

* Usage: `!rssnotifier removeroles <feed_name> <channel> <roles>`
* Aliases: `removerole`

Remove roles that should be mentioned when new message for given feed is sent.\
\
Use !rss list for the list of available feeds.

### rssnotifier optout

* Usage: `!rssnotifier optout <feed_name> [channel=None]`
* Checks: `single_user_pings_enabled`

Opt-out of receiving notifications for the given feed name.\
\
Use !rss list for the list of available feeds.

### rssnotifier usermentions

* Usage: `!rssnotifier usermentions [state=None]`

Set whether users can opt-in receiving notifications.\
\
**NOTE:** Generally, it is better to use role mentions\
and allow the users to self-assign the set role\
rather than have the bot send a lot of single user mentions.\
\
This setting applies to whole server.\
\
When this is enabled, users can use !rssnotifier optin/optout\
to opt-in/opt-out of receiving notifications for given rss feed.\
\
When this is disabled, cog will ignore any users who have previously opted-in\
and only mention the roles set by server admins.\
\
By default this is disabled\
and only the roles set by server admins will be mentioned.

### rssnotifier adminoptout

* Usage: `!rssnotifier adminoptout <feed_name> <channel> <user_ids>`

Force opt-out the users with given IDs from the given feed.\
\
This can be useful, when the user is no longer in server, for example.\
\
Use !rss list for the list of available feeds.

---
description: Listen to great quality music thru Sentri!
---

# 🎧 Music

## queue

* Usage: `!queue [page]`
* Checks: `bot_can_react and server_only`

List the songs in the queue.

### queue clean

* Usage: `!queue clean`

Removes songs from the queue if the requester is not in the voice channel.

### queue shuffle

* Usage: `!queue shuffle`
* Cooldown: `1 per 30.0 seconds`

Shuffles the queue.

### queue cleanself

* Usage: `!queue cleanself`

Removes all tracks you requested from the queue.

### queue clear

* Usage: `!queue clear`

Clears the queue.

### queue search

* Usage: `!queue search <search_words>`

Search the queue.

## playlist

* Usage: `!playlist`
* Checks: `bot_can_react and server_only`

Playlist configuration options.\
\
Scope info:\
​ ​ ​ ​ **Global**:\
​ ​ ​ ​ ​ ​ ​ ​ Visible to all users of this bot.\
​ ​ ​ ​ ​ ​ ​ ​ Only editable by bot owner.\
​ ​ ​ ​ **Guild**:\
​ ​ ​ ​ ​ ​ ​ ​ Visible to all users in this server.\
​ ​ ​ ​ ​ ​ ​ ​ Editable by bot owner, server owner, server admins, server mods, DJ role and playlist creator.\
​ ​ ​ ​ **User**:\
​ ​ ​ ​ ​ ​ ​ ​ Visible to all bot users, if --author is passed.\
​ ​ ​ ​ ​ ​ ​ ​ Editable by bot owner and the playlist creator.

### playlist create

* Usage: `!playlist create <playlist_name> [scope_data]`

Create an empty playlist.\
\
**Usage**:\
​ ​ ​ ​ !playlist create playlist\_name \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist create MyGuildPlaylist\
​ ​ ​ ​ !playlist create MyGlobalPlaylist --scope Global\
​ ​ ​ ​ !playlist create MyPersonalPlaylist --scope User

### playlist remove

* Usage: `!playlist remove <playlist_matches> <url> [scope_data]`

Remove a track from a playlist by url.\
\
**Usage**:\
​ ​ ​ ​ !playlist remove playlist\_name\_OR\_id url \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist remove MyGuildPlaylist https://www.youtube.com/watch?v=MN3x-kAbgFU\
​ ​ ​ ​ !playlist remove MyGlobalPlaylist https://www.youtube.com/watch?v=MN3x-kAbgFU --scope Global\
​ ​ ​ ​ !playlist remove MyPersonalPlaylist https://www.youtube.com/watch?v=MN3x-kAbgFU --scope User

### playlist rename

* Usage: `!playlist rename <playlist_matches> <new_name> [scope_data]`
* Cooldown: `1 per 60.0 seconds`

Rename an existing playlist.\
\
**Usage**:\
​ ​ ​ ​ !playlist rename playlist\_name\_OR\_id new\_name \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist rename MyGuildPlaylist RenamedGuildPlaylist\
​ ​ ​ ​ !playlist rename MyGlobalPlaylist RenamedGlobalPlaylist --scope Global\
​ ​ ​ ​ !playlist rename MyPersonalPlaylist RenamedPersonalPlaylist --scope User

### playlist append

* Usage: `!playlist append <playlist_matches> <query> [scope_data]`

Add a track URL, playlist link, or quick search to a playlist.\
\
The track(s) will be appended to the end of the playlist.\
\
**Usage**:\
​ ​ ​ ​ !playlist append playlist\_name\_OR\_id track\_name\_OR\_url \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist append MyGuildPlaylist Hello by Adele\
​ ​ ​ ​ !playlist append MyGlobalPlaylist Hello by Adele --scope Global\
​ ​ ​ ​ !playlist append MyGlobalPlaylist Hello by Adele --scope Global --Author Draper#6666

### playlist update

* Usage: `!playlist update <playlist_matches> [scope_data]`
* Cooldown: `1 per 60.0 seconds`

Updates all tracks in a playlist.\
\
**Usage**:\
​ ​ ​ ​ !playlist update playlist\_name\_OR\_id \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist update MyGuildPlaylist\
​ ​ ​ ​ !playlist update MyGlobalPlaylist --scope Global\
​ ​ ​ ​ !playlist update MyPersonalPlaylist --scope User

### playlist list

* Usage: `!playlist list [scope_data]`
* Cooldown: `1 per 15.0 seconds`

List saved playlists.\
\
**Usage**:\
​ ​ ​ ​ !playlist list \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist list\
​ ​ ​ ​ !playlist list --scope Global\
​ ​ ​ ​ !playlist list --scope User

### playlist info

* Usage: `!playlist info <playlist_matches> [scope_data]`
* Cooldown: `1 per 10.0 seconds`

Retrieve information from a saved playlist.\
\
**Usage**:\
​ ​ ​ ​ !playlist info playlist\_name\_OR\_id \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist info MyGuildPlaylist\
​ ​ ​ ​ !playlist info MyGlobalPlaylist --scope Global\
​ ​ ​ ​ !playlist info MyPersonalPlaylist --scope User

### playlist start

* Usage: `!playlist start <playlist_matches> [scope_data]`
* Aliases: `play`
* Cooldown: `1 per 30.0 seconds`

Load a playlist into the queue.\
\
**Usage**:\
​ ​ ​ ​ !playlist start playlist\_name\_OR\_id \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist start MyGuildPlaylist\
​ ​ ​ ​ !playlist start MyGlobalPlaylist --scope Global\
​ ​ ​ ​ !playlist start MyPersonalPlaylist --scope User

### playlist delete

* Usage: `!playlist delete <playlist_matches> [scope_data]`
* Aliases: `del`

Delete a saved playlist.\
\
**Usage**:\
​ ​ ​ ​ !playlist delete playlist\_name\_OR\_id \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist delete MyGuildPlaylist\
​ ​ ​ ​ !playlist delete MyGlobalPlaylist --scope Global\
​ ​ ​ ​ !playlist delete MyPersonalPlaylist --scope User

### playlist copy

* Usage: `!playlist copy <playlist_matches> [scope_data]`
* Cooldown: `1 per 150.0 seconds`

Copy a playlist from one scope to another.\
\
**Usage**:\
​ ​ ​ ​ !playlist copy playlist\_name\_OR\_id \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --from-scope\
​ ​ ​ ​ ​ ​ ​ ​ --from-author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --from-server \[server] **Only the bot owner can use this**\
\
​ ​ ​ ​ ​ ​ ​ ​ --to-scope\
​ ​ ​ ​ ​ ​ ​ ​ --to-author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --to-server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist copy MyGuildPlaylist --from-scope Guild --to-scope Global\
​ ​ ​ ​ !playlist copy MyGlobalPlaylist --from-scope Global --to-author Draper#6666 --to-scope User\
​ ​ ​ ​ !playlist copy MyPersonalPlaylist --from-scope user --to-author Draper#6666 --to-scope Guild --to-server Red - Discord Bot

### playlist save

* Usage: `!playlist save <playlist_name> <playlist_url> [scope_data]`
* Cooldown: `1 per 60.0 seconds`

Save a playlist from a url.\
\
**Usage**:\
​ ​ ​ ​ !playlist save name url \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist save MyGuildPlaylist https://www.youtube.com/playlist?list=PLx0sYbCqOb8Q\_CLZC2BdBSKEEB59BOPUM\
​ ​ ​ ​ !playlist save MyGlobalPlaylist https://www.youtube.com/playlist?list=PLx0sYbCqOb8Q\_CLZC2BdBSKEEB59BOPUM --scope Global\
​ ​ ​ ​ !playlist save MyPersonalPlaylist https://open.spotify.com/playlist/1RyeIbyFeIJVnNzlGr5KkR --scope User

### playlist queue

* Usage: `!playlist queue <playlist_name> [scope_data]`
* Cooldown: `1 per 300.0 seconds`

Save the queue to a playlist.\
\
**Usage**:\
​ ​ ​ ​ !playlist queue playlist\_name \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist queue MyGuildPlaylist\
​ ​ ​ ​ !playlist queue MyGlobalPlaylist --scope Global\
​ ​ ​ ​ !playlist queue MyPersonalPlaylist --scope User

### playlist dedupe

* Usage: `!playlist dedupe <playlist_matches> [scope_data]`
* Cooldown: `1 per 30.0 seconds`

Remove duplicate tracks from a saved playlist.\
\
**Usage**:\
​ ​ ​ ​ !playlist dedupe playlist\_name\_OR\_id \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​ ​ ​ ​ Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !playlist dedupe MyGuildPlaylist\
​ ​ ​ ​ !playlist dedupe MyGlobalPlaylist --scope Global\
​ ​ ​ ​ !playlist dedupe MyPersonalPlaylist --scope User

## play

* Usage: `!play <query>`
* Checks: `server_only`

Play the specified track or search for a close match.\
\
To play a local track, the query should be \<filename>.\
If you are the bot owner, use !audioset info to display your localtracks path.

## bumpplay

* Usage: `!bumpplay [play_now=False] <query>`
* Checks: `server_only`

Force play a URL or search for a track.

## genre

* Usage: `!genre`
* Checks: `server_only`

Pick a Spotify playlist from a list of categories to start playing.

## autoplay

* Usage: `!autoplay`
* Restricted to: `MOD`
* Checks: `server_only`

Starts auto play.

## search

* Usage: `!search <query>`
* Checks: `bot_can_react and server_only`

Pick a track with a search.\
\
Use !search list to queue all tracks found on YouTube. Use !search sc\
to search on SoundCloud instead of YouTube.

## sing

* Usage: `!sing`
* Checks: `server_only`

Make Red sing one of her songs.

## percent

* Usage: `!percent`
* Checks: `server_only`

Queue percentage.

## local

* Usage: `!local`
* Checks: `bot_can_react and server_only`

Local playback commands.

### local folder

* Usage: `!local folder [folder]`
* Aliases: `start`

Play all songs in a localtracks folder.\
\
**Usage**:\
​ ​ ​ ​ !local folder\
​ ​ ​ ​ ​ ​ ​ ​ Open a menu to pick a folder to queue.\
\
​ ​ !local folder folder\_name\
​ ​ ​ ​ ​ ​ ​ ​ Queues all of the tracks inside the folder\_name folder.

### local search

* Usage: `!local search <search_words>`

Search for songs across all localtracks folders.

### local play

* Usage: `!local play`

Play a local track.\
\
To play a local track, either use the menu to choose a track or enter in the track path directly with the play command.\
To play an entire folder, use !help local folder for instructions.\
\
**Usage**:\
​ ​ ​ ​ !local play\
​ ​ ​ ​ ​ ​ ​ ​ Open a menu to pick a track.\
\
​ ​ ​ ​ !play localtracks\album\_folder\song\_name.mp3\
​ ​ ​ ​ !play album\_folder\song\_name.mp3\
​ ​ ​ ​ ​ ​ ​ ​ Use a direct link relative to the localtracks folder.

## eq

* Usage: `!eq`
* Cooldown: `1 per 15.0 seconds`
* Checks: `bot_can_react and server_only`

Equalizer management.\
\
Band positions are 1-15 and values have a range of -0.25 to 1.0.\
Band names are 25, 40, 63, 100, 160, 250, 400, 630, 1k, 1.6k, 2.5k, 4k,\
6.3k, 10k, and 16k Hz.\
Setting a band value to -0.25 nullifies it while +0.25 is double.

### eq save

* Usage: `!eq save [eq_preset=None]`
* Cooldown: `1 per 15.0 seconds`

Save the current eq settings to a preset.

### eq list

* Usage: `!eq list`

List saved eq presets.

### eq set

* Usage: `!eq set <band_name_or_position> <band_value>`

Set an eq band with a band number or name and value.\
\
Band positions are 1-15 and values have a range of -0.25 to 1.0.\
Band names are 25, 40, 63, 100, 160, 250, 400, 630, 1k, 1.6k, 2.5k, 4k,\
6.3k, 10k, and 16k Hz.\
Setting a band value to -0.25 nullifies it while +0.25 is double.

### eq load

* Usage: `!eq load <eq_preset>`

Load a saved eq preset.

### eq delete

* Usage: `!eq delete <eq_preset>`
* Aliases: `del and remove`

Delete a saved eq preset.

### eq reset

* Usage: `!eq reset`

Reset the eq to 0 across all bands.

## disconnect

* Usage: `!disconnect`
* Checks: `server_only`

Disconnect from the voice channel.

## now

* Usage: `!now`
* Checks: `bot_can_react and server_only`

Now playing.

## pause

* Usage: `!pause`
* Checks: `server_only`

Pause or resume a playing track.

## prev

* Usage: `!prev`
* Checks: `server_only`

Skip to the start of the previously played track.

## seek

* Usage: `!seek <seconds>`
* Checks: `server_only`

Seek ahead or behind on a track by seconds or to a specific time.\
\
Accepts seconds or a value formatted like 00:00:00 (hh:mm:ss) or 00:00 (mm:ss).

## shuffle

* Usage: `!shuffle`
* Checks: `server_only`

Toggle shuffle.

### shuffle bumped

* Usage: `!shuffle bumped`
* Checks: `server_only`

Toggle bumped track shuffle.\
\
Set this to disabled if you wish to avoid bumped songs being shuffled. This takes priority\
over !shuffle.

## skip

* Usage: `!skip [skip_to_track=None]`
* Checks: `server_only`

Skip to the next track, or to a given track number.

## stop

* Usage: `!stop`
* Checks: `server_only`

Stop playback and clear the queue.

## summon

* Usage: `!summon`
* Cooldown: `1 per 15.0 seconds`
* Checks: `server_only`

Summon the bot to a voice channel.

## volume

* Usage: `!volume [vol=None]`
* Checks: `server_only`

Set the volume, 1% - 150%.

## repeat

* Usage: `!repeat`
* Checks: `server_only`

Toggle repeat.

## remove

* Usage: `!remove <index_or_url>`
* Checks: `server_only`

Remove a specific track number from the queue.

## bump

* Usage: `!bump <index>`
* Checks: `server_only`

Bump a track number to the top of the queue.

## audioset

* Usage: `!audioset`

Music configuration options.

### audioset autodeafen

* Usage: `!audioset autodeafen`
* Restricted to: `MOD`
* Checks: `server_only`

Toggle whether the bot will be auto deafened upon joining the voice channel.

### audioset role

* Usage: `!audioset role <role_name>`
* Restricted to: `ADMIN`
* Checks: `server_only`

Set the role to use for DJ mode.

### audioset settings

* Usage: `!audioset settings`
* Aliases: `info`
* Checks: `server_only`

Show the current settings.

### audioset dailyqueue

* Usage: `!audioset dailyqueue`
* Restricted to: `ADMIN`
* Checks: `server_only`

Toggle daily queues.\
\
Daily queues creates a playlist for all tracks played today.

### audioset dc

* Usage: `!audioset dc`
* Restricted to: `MOD`
* Checks: `server_only`

Toggle the bot auto-disconnecting when done playing.\
\
This setting takes precedence over !audioset emptydisconnect.

### audioset thumbnail

* Usage: `!audioset thumbnail`
* Restricted to: `MOD`
* Checks: `server_only`

Toggle displaying a thumbnail on audio messages.

### audioset dj

* Usage: `!audioset dj`
* Restricted to: `ADMIN`
* Checks: `server_only`

Toggle DJ mode.\
\
DJ mode allows users with the DJ role to use audio commands.

### audioset vote

* Usage: `!audioset vote <percent>`
* Restricted to: `MOD`
* Checks: `server_only`

Percentage needed for non-mods to skip tracks, 0 to disable.

### audioset emptydisconnect

* Usage: `!audioset emptydisconnect <seconds>`
* Restricted to: `MOD`
* Checks: `server_only`

Auto-disconnect from channel when bot is alone in it for x seconds, 0 to disable.\
\
!audioset dc takes precedence over this setting.

### audioset emptypause

* Usage: `!audioset emptypause <seconds>`
* Restricted to: `MOD`
* Checks: `server_only`

Auto-pause after x seconds when room is empty, 0 to disable.

### audioset lyrics

* Usage: `!audioset lyrics`
* Restricted to: `MOD`
* Checks: `server_only`

Prioritise tracks with lyrics.

### audioset countrycode

* Usage: `!audioset countrycode <country>`
* Restricted to: `MOD`
* Checks: `server_only`

Set the country code for Spotify searches.

### audioset jukebox

* Usage: `!audioset jukebox <price>`
* Restricted to: `MOD`
* Checks: `server_only`

Set a price for queueing tracks for non-mods, 0 to disable.

### audioset autoplay

* Usage: `!audioset autoplay`
* Restricted to: `MOD`
* Checks: `server_only`

Change auto-play setting.

#### audioset autoplay playlist

* Usage: `!audioset autoplay playlist <playlist_matches> [scope_data]`
* Checks: `bot_can_react`

Set a playlist to auto-play songs from.\
\
**Usage**:\
​ ​ ​ ​ !audioset autoplay playlist playlist\_name\_OR\_id \[args]\
\
**Args**:\
​ ​ ​ ​ The following are all optional:\
​ ​ ​ ​ ​ ​ ​ ​ --scope\
​ ​ ​ ​ ​ ​ ​ ​ --author \[user]\
​ ​ ​ ​ ​ ​ ​ ​ --server \[server] **Only the bot owner can use this**\
\
**Scope** is one of the following:\
​Global\
​ ​ ​ ​ Guild\
​ ​ ​ ​ User\
\
**Author** can be one of the following:\
​ ​ ​ ​ User ID\
​ ​ ​ ​ User Mention\
​ ​ ​ ​ User Name#123\
\
**Guild** can be one of the following:\
​ ​ ​ ​ Guild ID\
​ ​ ​ ​ Exact server name\
\
Example use:\
​ ​ ​ ​ !audioset autoplay playlist MyGuildPlaylist\
​ ​ ​ ​ !audioset autoplay playlist MyGlobalPlaylist --scope Global\
​ ​ ​ ​ !audioset autoplay playlist PersonalPlaylist --scope User --author Draper

#### audioset autoplay toggle

* Usage: `!audioset autoplay toggle`

Toggle auto-play when there no songs in queue.

#### audioset autoplay reset

* Usage: `!audioset autoplay reset`

Resets auto-play to the default playlist.

### audioset maxvolume

* Usage: `!audioset maxvolume <max_volume>`
* Restricted to: `ADMIN`
* Checks: `server_only`

Set the maximum volume allowed in this server.

### audioset mycountrycode

* Usage: `!audioset mycountrycode <country>`
* Checks: `server_only`

Set the country code for Spotify searches.

### audioset persistqueue

* Usage: `!audioset persistqueue`
* Restricted to: `ADMIN`

Toggle persistent queues.\
\
Persistent queues allows the current queue to be restored when the queue closes.

### audioset maxlength

* Usage: `!audioset maxlength <seconds>`
* Restricted to: `MOD`
* Checks: `server_only`

Max length of a track to queue in seconds, 0 to disable.\
\
Accepts seconds or a value formatted like 00:00:00 (hh:mm:ss) or 00:00 (mm:ss). Invalid\
input will turn the max length setting off.

### audioset notify

* Usage: `!audioset notify`
* Restricted to: `MOD`
* Checks: `server_only`

Toggle track announcement and other bot messages.

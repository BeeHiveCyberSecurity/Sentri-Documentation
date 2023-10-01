---
description: A pretty fantastic leveling and prestige system
---

# ↗ Leveling

Earn experience by chatting in text and voice channels, compare levels with your friends, customize your profile and view various leaderboards!

## stars

* Usage: `!stars <user>`
* Aliases: `givestar, addstar, and thanks`
* Checks: `server_only`

Reward a good noodle\
Give a star to a user for being a good noodle

## myprofile

* Usage: `!myprofile`
* Aliases: `mypf and pfset`
* Checks: `server_only`

Customize your profile colors\
\
Here is a link to google's color picker:\
[**Hex Color Picker**](https://htmlcolorcodes.com/)

### myprofile blur

* Usage: `!myprofile blur`

Toggle a slight blur effect on the background image where the text is displayed.

### myprofile type

* Usage: `!myprofile type`

Toggle your profile image type (full/slim)\
\
Full size includes your balance, role icon and prestige icon\
Slim is a smaller slimmed down version

### myprofile statcolor

* Usage: `!myprofile statcolor <hex_color>`
* Aliases: `stat`

Set a hex color for your server stats\
\
Here is a link to google's color picker:\
[**Hex Color Picker**](https://htmlcolorcodes.com/)\
\
Set to default to randomize your name color each time you run the command

### myprofile background

* Usage: `!myprofile background [image_url=None]`
* Aliases: `bg`
* Cooldown: `1 per 30.0 seconds`

Set a background for your profile\
\
This will override your profile banner as the background\
\
**WARNING**\
Profile backgrounds are wide landscapes (1050 by 450 pixels) with an aspect ratio of 21:9\
Using portrait images will be cropped.\
\
Tip: Googling "dual monitor backgrounds" gives good results for the right images\
\
Here are some good places to look.\
[dualmonitorbackgrounds](https://www.dualmonitorbackgrounds.com/)\
[setaswall](https://www.setaswall.com/dual-monitor-wallpapers/)\
[pexels](https://www.pexels.com/photo/panoramic-photography-of-trees-and-lake-358482/)\
[teahub](https://www.teahub.io/searchw/dual-monitor/)\
\
**Additional Options**\
\- Leave image\_url blank to reset back to using your profile banner (or random if you don't have one)\
\- random will randomly select from a pool of default backgrounds each time\
\- filename run !mypf backgrounds to view default options you can use by including their filename

### myprofile font

* Usage: `!myprofile font <font_name>`

Set a font for your profile\
\
To view available fonts, type !myprofile fonts\
To revert to the default font, use default for the font\_name argument

### myprofile namecolor

* Usage: `!myprofile namecolor <hex_color>`
* Aliases: `name`

Set a hex color for your username\
\
Here is a link to google's color picker:\
[**Hex Color Picker**](https://htmlcolorcodes.com/)\
\
Set to default to randomize your name color each time you run the command

### myprofile backgrounds

* Usage: `!myprofile backgrounds`
* Cooldown: `1 per 30.0 seconds`

View the default backgrounds

### myprofile levelbar

* Usage: `!myprofile levelbar <hex_color>`
* Aliases: `lvlbar and bar`

Set a hex color for your level bar\
\
Here is a link to google's color picker:\
[**Hex Color Picker**](https://htmlcolorcodes.com/)\
\
Set to default to randomize your name color each time you run the command

### myprofile fonts

* Usage: `!myprofile fonts`
* Cooldown: `1 per 30.0 seconds`

View available fonts to use

## pf

* Usage: `!pf [user]`
* Cooldown: `1 per 5.0 seconds`
* Checks: `server_only`

View your profile

## prestige

* Usage: `!prestige`
* Checks: `server_only`

Prestige your rank!\
Once you have reached this servers prestige level requirement, you can\
reset your level and experience to gain a prestige level and any perks associated with it\
\
If you are over level and xp when you prestige, your xp and levels will carry over

## lvltop

* Usage: `!lvltop <stat>`
* Aliases: `topstats, membertop, and topranks`
* Checks: `server_only`

View the Leaderboard\
\
**Arguments**\
stat: What kind of stat to display the weekly leaderboard for\
Valid options are exp, messages, and voice\
Abbreviations of those arguments may also be used

## startop

* Usage: `!startop`
* Aliases: `starlb`
* Checks: `server_only`

View the star leaderboard

## weekly

* Usage: `!weekly <stat>`
* Checks: `server_only`

View the weekly leaderboard\
\
**Arguments**\
stat: What kind of stat to display the weekly leaderboard for\
Valid options are exp, messages, stars, and voice\
Abbreviations of those arguments may also be used

## lastweekly

* Usage: `!lastweekly`
* Checks: `server_only`

View the last weekly embed

## lvlset

* Usage: `!lvlset`
* Aliases: `lset and levelup`
* Checks: `server_only`

Access LevelUp setting commands

### lvlset admin

* Usage: `!lvlset admin`
* Restricted to: `GUILD_OWNER`

Cog admin commands\
\
Reset levels, backup and restore cog data

#### lvlset admin statreset

* Usage: `!lvlset admin statreset`

Reset everyone's exp and level

#### lvlset admin importamari

* Usage: `!lvlset admin importamari <import_by> <replace> <i_agree> <api_key>`
* Restricted to: `GUILD_OWNER`

Import levels and exp from AmariBot\
\
**Arguments**\
import\_by - which stat to prioritize (level or exp)\
If exp is entered, it will import their experience and base their new level off of that.\
If level is entered, it will import their level and calculate their exp based off of that.\
replace - (True/False) if True, it will replace the user's exp or level, otherwise it will add it\
i\_agree - (Yes/No) Just an extra option to make sure you want to execute this command\
api\_key - Your [AmariBot API Key](https://docs.google.com/forms/d/e/1FAIpQLScQDCsIqaTb1QR9BfzbeohlUJYA3Etwr-iSb0CRKbgjA-fq7Q/viewform?usp=send\_form)\
\
**Note**\
Instead of typing true/false\
1 = True\
0 = False

#### lvlset admin serverrestore

* Usage: `!lvlset admin serverrestore`
* Restricted to: `GUILD_OWNER`

Restore a server backup\
\
Attach the .json file to the command message to import

#### lvlset admin importpolaris

* Usage: `!lvlset admin importpolaris <replace> <include_settings> <i_agree>`
* Restricted to: `GUILD_OWNER`

Import levels and exp from [Polaris](https://gdcolon.com/polaris/)\
\
**Make sure your server's leaderboard is public!**\
\
**Arguments**\
replace - (True/False) if True, it will replace the user's exp, otherwise it will add it\
include\_settings - (True/False) import level roles and exp settings from Polaris\
i\_agree - (Yes/No) Just an extra option to make sure you want to execute this command\
\
**Note**\
Instead of typing true/false\
1 = True\
0 = False

#### lvlset admin cleanup

* Usage: `!lvlset admin cleanup`
* Restricted to: `GUILD_OWNER`

Delete users no longer in the server\
\
Also cleans up any missing keys or discrepancies in the config

#### lvlset admin view

* Usage: `!lvlset admin view`

View current loop times and cached data

#### lvlset admin serverreset

* Usage: `!lvlset admin serverreset`

Reset cog data for this server

#### lvlset admin serverbackup

* Usage: `!lvlset admin serverbackup`
* Restricted to: `GUILD_OWNER`

Create a backup of the LevelUp config

#### lvlset admin importmee6

* Usage: `!lvlset admin importmee6 <import_by> <replace> <include_settings> <i_agree>`
* Restricted to: `GUILD_OWNER`

Import levels and exp from MEE6\
\
**Make sure your server's leaderboard is public!**\
\
**Arguments**\
import\_by - which stat to prioritize (level or exp)\
If exp is entered, it will import their experience and base their new level off of that.\
If level is entered, it will import their level and calculate their exp based off of that.\
replace - (True/False) if True, it will replace the user's exp or level, otherwise it will add it\
include\_settings - (True/False) import level roles and exp settings from MEE6\
i\_agree - (Yes/No) Just an extra option to make sure you want to execute this command\
\
**Note**\
Instead of typing true/false\
1 = True\
0 = False

### lvlset dm

* Usage: `!lvlset dm`

Toggle DM notifications\
Toggle whether LevelUp messages are DM'd to the user

### lvlset barlength

* Usage: `!lvlset barlength <bar_length>`

Set the progress bar length for embed profiles

### lvlset voice

* Usage: `!lvlset voice`

Voice settings

#### lvlset voice rolebonus

* Usage: `!lvlset voice rolebonus <role> <min_xp> <max_xp>`

Add a range of bonus XP to apply to certain roles\
\
This bonus applies to voice time xp\
\
Set both min and max to 0 to remove the role bonus

#### lvlset voice invisible

* Usage: `!lvlset voice invisible`

Ignore invisible voice users\
Toggle whether invisible users in a voice channel can gain voice XP

#### lvlset voice xp

* Usage: `!lvlset voice xp <voice_xp>`

Set voice XP gain\
Sets the amount of XP gained per minute in a voice channel (default is 2)

#### lvlset voice streambonus

* Usage: `!lvlset voice streambonus <min_xp> <max_xp>`

Add a range of bonus XP to users who are Discord streaming\
\
This bonus applies to voice time xp\
\
Set both min and max to 0 to remove the bonus

#### lvlset voice channelbonus

* Usage: `!lvlset voice channelbonus <channel> <min_xp> <max_xp>`

Add a range of bonus XP to apply to certain channels\
\
This bonus applies to voice time xp\
\
Set both min and max to 0 to remove the role bonus

#### lvlset voice muted

* Usage: `!lvlset voice muted`

Ignore muted voice users\
Toggle whether self-muted users in a voice channel can gain voice XP

#### lvlset voice solo

* Usage: `!lvlset voice solo`

Ignore solo voice users\
Toggle whether solo users in a voice channel can gain voice XP

#### lvlset voice deafened

* Usage: `!lvlset voice deafened`

Ignore deafened voice users\
Toggle whether deafened users in a voice channel can gain voice XP

### lvlset starmention

* Usage: `!lvlset starmention`

Toggle star reaction mentions\
Toggle whether the bot mentions that a user reacted to a message with a star

### lvlset setprestige

* Usage: `!lvlset setprestige <user> <prestige>`

Set a user to a specific prestige level\
\
Prestige roles will need to be manually added/removed when using this command

### lvlset ignored

* Usage: `!lvlset ignored`

Base command for all ignore lists

#### lvlset ignored member

* Usage: `!lvlset ignored member <member>`

Add/Remove a member from the ignore list\
Members in the ignore list don't gain XP\
\
Use the command with a member already in the ignore list to remove them

#### lvlset ignored channel

* Usage: `!lvlset ignored channel <channel>`

Add/Remove a channel in the ignore list\
Channels in the ignore list don't gain XP\
\
Use the command with a channel already in the ignore list to remove it

#### lvlset ignored role

* Usage: `!lvlset ignored role <role>`

Add/Remove a role from the ignore list\
Roles in the ignore list don't gain XP\
\
Use the command with a role already in the ignore list to remove it

### lvlset embeds

* Usage: `!lvlset embeds`

Toggle using embeds or generated pics

### lvlset messages

* Usage: `!lvlset messages`
* Aliases: `message and msg`

Message settings

#### lvlset messages channelbonus

* Usage: `!lvlset messages channelbonus <channel> <min_xp> <max_xp>`

Add a range of bonus XP to apply to certain channels\
\
This bonus applies to message xp\
\
Set both min and max to 0 to remove the role bonus

#### lvlset messages xp

* Usage: `!lvlset messages xp [min_xp=3] [max_xp=6]`

Set message XP range\
Set the Min and Max amount of XP that a message can gain

#### lvlset messages rolebonus

* Usage: `!lvlset messages rolebonus <role> <min_xp> <max_xp>`

Add a range of bonus XP to apply to certain roles\
\
This bonus applies to message xp\
\
Set both min and max to 0 to remove the role bonus

#### lvlset messages cooldown

* Usage: `!lvlset messages cooldown <cooldown>`

Cooldown threshold for message XP\
\
When a user sends a message they will have to wait X seconds before their message\
counts as XP gained

#### lvlset messages length

* Usage: `!lvlset messages length <minimum_length>`

Set minimum message length for XP\
Minimum length a message must be to count towards XP gained\
\
Set to 0 to disable

### lvlset showbalance

* Usage: `!lvlset showbalance`

Toggle whether to show user's economy credit balance in their profile

### lvlset starmentiondelete

* Usage: `!lvlset starmentiondelete <deleted_after>`

Toggle whether the bot auto-deletes the star mentions\
Set to 0 to disable auto-delete

### lvlset addxp

* Usage: `!lvlset addxp <user_or_role> <xp>`

Add XP to a user or role

### lvlset setlevel

* Usage: `!lvlset setlevel <user> <level>`

Set a user to a specific level

### lvlset view

* Usage: `!lvlset view`

View all LevelUP settings

### lvlset levelnotify

* Usage: `!lvlset levelnotify`

Toggle the level up message when a user levels up

### lvlset levelchannel

* Usage: `!lvlset levelchannel [levelup_channel=None]`

Set LevelUP message channel\
Set a channel for all level up messages to send to

### lvlset prestige

* Usage: `!lvlset prestige`

Level Prestige Settings

#### lvlset prestige del

* Usage: `!lvlset prestige del <prestige_level>`

Delete a prestige level role

#### lvlset prestige add

* Usage: `!lvlset prestige add <prestige_level> <role> <emoji>`

Add a prestige level role\
Add a role and emoji associated with a specific prestige level\
\
When a user prestiges, they will get that role and the emoji will show on their profile

#### lvlset prestige level

* Usage: `!lvlset prestige level <level>`

Set the level required to prestige\
Set to 0 to disable prestige

#### lvlset prestige autoremove

* Usage: `!lvlset prestige autoremove`

Automatic removal of previous prestige level roles

### lvlset seelevels

* Usage: `!lvlset seelevels`

Test the level algorithm\
View the first 20 levels using the current algorithm to test experience curve

### lvlset mention

* Usage: `!lvlset mention`

Toggle levelup mentions\
Toggle whether the user in mentioned in LevelUp messages

### lvlset roles

* Usage: `!lvlset roles`
* Restricted to: `ADMIN`

Level role assignment

#### lvlset roles autoremove

* Usage: `!lvlset roles autoremove`

Automatic removal of previous level roles

#### lvlset roles del

* Usage: `!lvlset roles del <level>`

Unassign a role from a level

#### lvlset roles add

* Usage: `!lvlset roles add <level> <role>`

Assign a role to a level

#### lvlset roles initialize

* Usage: `!lvlset roles initialize`

Initialize level roles\
\
This command is for if you added level roles after users have achieved that level,\
it will apply all necessary roles to a user according to their level and prestige

### lvlset algorithm

* Usage: `!lvlset algorithm`

Customize the leveling algorithm for your server

#### lvlset algorithm base

* Usage: `!lvlset algorithm base <base_multiplier>`

Base multiplier for the leveling algorithm\
\
Affects leveling on a more linear scale(higher values makes leveling take longer)

#### lvlset algorithm exp

* Usage: `!lvlset algorithm exp <exponent_multiplier>`

Exponent multiplier for the leveling algorithm\
\
Affects leveling on an exponential scale(higher values makes leveling take exponentially longer)

### lvlset starcooldown

* Usage: `!lvlset starcooldown <time_in_seconds>`

Set the star cooldown\
\
Users can give another user a star every X seconds

## weeklyset

* Usage: `!weeklyset`
* Aliases: `wset`
* Checks: `server_only`

Access the weekly settings for levelUp

### weeklyset day

* Usage: `!weeklyset day <day_of_the_week>`

What day of the week the weekly stats reset\
Set the day of the week (0 - 6 = Monday - Sunday) for weekly reset to take place

### weeklyset roleall

* Usage: `!weeklyset roleall`

Toggle whether to give the weekly winner role to all winners or only 1st place

### weeklyset hour

* Usage: `!weeklyset hour <hour>`

What hour the weekly stats reset\
Set the hour (0 - 23 in UTC) for the weekly reset to take place

### weeklyset autoreset

* Usage: `!weeklyset autoreset`

Toggle weekly auto-reset

### weeklyset view

* Usage: `!weeklyset view`

View the current weekly settings

### weeklyset role

* Usage: `!weeklyset role <role>`

Weekly winner role reward\
Set the role awarded to the top member of the weekly leaderboard

### weeklyset autoremove

* Usage: `!weeklyset autoremove`

One role holder at a time\
Toggle whether the winner role is removed from the previous holder when a new winner is selected

### weeklyset bonus

* Usage: `!weeklyset bonus <exp_bonus>`

Weekly winners bonus experience points\
Set to 0 to disable exp bonus

### weeklyset toggle

* Usage: `!weeklyset toggle`

Toggle weekly stat tracking

### weeklyset top

* Usage: `!weeklyset top <top_count>`

Top weekly member count\
Set amount of members to include in the weekly top leaderboard

### weeklyset reset

* Usage: `!weeklyset reset <yes_or_no>`

Reset the weekly leaderboard manually and announce winners

### weeklyset channel

* Usage: `!weeklyset channel <channel>`

Weekly winner announcement channel\
set the channel for weekly winners to be announced in when auto-reset is enabled

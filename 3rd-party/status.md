---
description: Automatically check for status updates.
---

# Status

When there is one, it will send the update to all channels that\
have registered to recieve updates from that service.\
\
There's also the `status` command which anyone can use to check\
updates wherever they want.

## statusset

* Usage: `!statusset`
* Restricted to: `ADMIN`
* Checks: `server_only`

Get automatic status updates in a channel, eg Discord.\
\
Get started with !statusset preview to see what they look like,\
then !statusset add to set up automatic updates.

### statusset preview

* Usage: `!statusset preview <service> <mode> <webhook>`

Preview what status updates will look like.\
\
You can also see this at https://go.vexcodes.com/c/statusref\
\
The service you want to preview. There's a list of available services in the\
!help statusset command.\
\
\
**all**: Every time the service posts an update on an incident, I will send\
a new message containing the previous updates as well as the new update. Best\
used in a fast-moving channel with other users.\
\
**latest**: Every time the service posts an update on an incident, I will send\
a new message containing only the latest update. Best used in a dedicated status\
channel.\
\
**edit**: Naturally, edit mode can't have a preview so won't work with this command.\
The message content is the same as the all mode.\
When a new incident is created, I will sent a new message. When this\
incident is updated, I will then add the update to the original message. Best\
used in a dedicated status channel.\
\
\
\
Using a webhook means that the status updates will be sent with the avatar\
as the service's logo and the name will be \[service] Status Update, instead\
of my avatar and name.\
\
**Examples:**\
\- !statusset preview discord all true\
\- !statusset preview discord latest false

### statusset remove

* Usage: `!statusset remove <service> [chan=None]`
* Aliases: `del and delete`

Stop status updates for a specific service in this server.\
\
If you don't specify a channel, I will use the current channel.\
\
**Examples:**\
\- !statusset remove discord #testing\
\- !statusset remove discord (for using current channel)

### statusset clear

* Usage: `!statusset clear <chan>`
* Aliases: `erase`

Remove all feeds from a channel.\
\
If you don't specify a channel, I will use the current channel\
\
**Examples:**\
\- !statusset clear #testing\
\- !statusset clear (for using current channel)

### statusset list

* Usage: `!statusset list <service>`
* Aliases: `show and settings`

List that available services and ones are used in this server.\
\
Optionally add a service at the end of the command to view detailed settings for that\
service.\
\
**Examples:**\
\- !statusset list discord\
\- !statusset list

### statusset edit

* Usage: `!statusset edit`

Edit services you've already set up.

#### statusset edit webhook

* Usage: `!statusset edit webhook <chan> <service> <webhook>`

Set whether or not to use webhooks for status updates.\
\
Using a webhook means that the status updates will be sent with the avatar as the service's\
logo and the name will be \[service] Status Update, instead of my avatar and name.\
\
If you don't specify a channel, I will use the current channel.\
\
**Examples:**\
\- !statusset edit webhook #testing discord true\
\- !statusset edit webhook discord false (for current channel)

#### statusset edit restrict

* Usage: `!statusset edit restrict <chan> <service> <restrict>`

Restrict access to the service in the status command.\
\
Enabling this will reduce spam. Instead of sending the whole update\
(if there's an incident) members will instead be redirected to channels\
that automatically receive the status updates, that they have permission to to view.\
\
**Examples:**\
\- !statusset edit restrict #testing discord true\
\- !statusset edit restrict discord false (for current channel)

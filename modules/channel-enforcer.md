# 🚩 Channel Enforcer

#### Enforcer

This module allows you to enforce certain characteristics on a channel.

`[p]enforcer`

There are numerous attributes than can be used to restrict messages/content into a channel.

While some attributes are available in discord via role-based permissions, sometimes a bot may be better off enforcing content in a pinch.

**Configure Enforcer**

`[p]enforcer configure <channel> <attribute> [value]`

Example:

* `[p]enforcer configure #channel enabled true`

| Attribute           | Type   | Description                                                                                                      |
| ------------------- | ------ | ---------------------------------------------------------------------------------------------------------------- |
| `enabled`           | `bool` | Whether to enable enforcements on a channel                                                                      |
| `minchars`          | `int`  | The minimum number of characters a message must contain to be allowed into the channel                           |
| `maxchars`          | `int`  | The maximum number of characters a message may contain to be allowed into the channel                            |
| `notext`            | `bool` | The sent message must have _no_ text, i.e. should be an image-only message                                       |
| `requiremedia`      | `bool` | The sent message must contain an attached image                                                                  |
| `nomedia`           | `bool` | The sent message must **not** contain an attached image                                                          |
| `minimumguildage`   | `int`  | How old a server member must be part of the guild, in seconds, before they are able to contribute to the channel |
| `minimumdiscordage` | `int`  | How old a member's discord account must be, in seconds, before they are able to contribute to the channel        |

An example enforcement would be a channel to show off server pictures. In which case, you could allow members to post a set of images with a description of their setup.

In which case, the following would be appropriate

```
[p]enforcer logchannel #admin-log
[p]enforcer configure #serverpics requiremedia true
[p]enforcer configure #serverpics minimumguildage 600
[p]enforcer configure #serverpics minchars 20
[p]enforcer configure #serverpics maxchars 300
[p]enforcer configure enabled true
```

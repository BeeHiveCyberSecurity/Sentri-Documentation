# 👋 Introduction

Defender is a comprehensive set of tools designed to ensure the safety and security of your Discord community. The core functionalities of Defender are split into two modules:

* Automated modules, which includes automated moderation and monitoring features that operate without any manual intervention.
* Manual modules, which contains various tools that you can use as per your requirements.

Each module is optional and can be customized, which means you can enable or disable specific functionalities based on your preferences.

\
Despite being designed to counter serious threats, Defender can also be a very valuable tool for smaller communities with less traffic.

| Module           | Description                                                                                                                                                                                                                                             |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Invite filter    | Identifies and responds to unsolicited Discord invites that are shared within your community.                                                                                                                                                           |
| Join monitor     | Detects sudden influxes of user accounts joining your server and promptly notifies your staff about them. Additionally, it can dynamically increase your server's verification level should it detect a raid.                                           |
| Raider detection | Also commonly referred as antispam / antiraid, it takes action on users spamming messages.                                                                                                                                                              |
| Comment analysis | Leverages the power of machine learning to detect a wide range of potentially unwanted messages.                                                                                                                                                        |
| Warden           | A complex module that lets you define _rules_. Rules are sets of _conditions_ and _actions_ that you can define to automate moderation, monitoring and much more. If something isn't covered by the other modules, it can probably be done with Warden. |

| Module   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Alert    | Enables your helper roles to report any threats to the staff without revealing the issue publicly. When the helper roles report an emergency, the staff is discreetly notified with comprehensive context about the location of the incident. Moreover, this module can be customized to activate specific modules such as voteout when there is no staff activity within a certain period of time, hence putting the server in a state of emergency. |
| Vaporize | Particularly effective against raids. It provides a quick way to ban vast amounts of new users without creating new mod-log entries.                                                                                                                                                                                                                                                                                                                  |
| Silence  | Upon activation, it is able to instantly delete messages from certain ranks. This is particularly useful when a raid is in progress.                                                                                                                                                                                                                                                                                                                  |
| Voteout  | Starts a voting session to expel a user. This module was designed specifically for emergency mode so that when the staff is absent helper roles are still able to take care of things by themselves.                                                                                                                                                                                                                                                  |

All these modules deliver notifications to your designed Defender _notification channel_.

### Ranks <a href="#ranks" id="ranks"></a>

Defender segregates your userbase into distinct ranks, starting from Rank 1 (comprising your trusted users) to Rank 4 (consisting of new users with negligible activity on your server). With this classification, you can configure each Defender module to target users below (or within) a specific rank, thereby ensuring that regular users are exempted from unnecessary safety measures.

A regular user can only rank up to Rank 2, while Rank 1 is considered a special category that can be attained via designated roles or by having staff member status.

| Rank | Description                                                                              |
| ---- | ---------------------------------------------------------------------------------------- |
| 1    | Staff, trusted roles and helper roles                                                    |
| 2    | Regular users who don't fit in any of the lower ranks                                    |
| 3    | Users who joined less than X days ago. Configurable.                                     |
| 4    | Users who joined less than X days ago and have sent fewer than Y messages. Configurable. |

{% hint style="info" %}
Want to know which Rank a particular user is? Use `[p]def identify <user>`
{% endhint %}

### Emergency mode <a href="#emergency-mode" id="emergency-mode"></a>

Emergency mode is a critical feature of Defender that comes into play when none of your staff members are available to attend a situation. You can activate this mode using the Alert manual module, which triggers an emergency notification to your designated helper roles.

While setting up emergency mode, you can assign manual modules that must be activated in case of an emergency. Once your helper roles initiate an alert, Defender will wait for your staff team to respond for a specific time.

If your staff team fails to respond within the specified time, emergency mode will be triggered, and users with helper roles can use emergency modules to take appropriate action against the situation. The level of access to these modules depends on which modules you have chosen.

Defender continues to monitor staff activity for re-engagement, and after detecting any activity, it deactivates emergency mode.

### Quick actions <a href="#quick-actions" id="quick-actions"></a>

It is possible to act on Defender's standard notifications by reacting on them. It is also possible to make Warden rules that support this.

| Emoji             | Action                             |
| ----------------- | ---------------------------------- |
| 🔨 `:hammer:`     | Ban                                |
| 🔂 `:repeat_one:` | Ban with 24 hours message deletion |
| 💨 `:dash:`       | Softban                            |
| 👢 `:boot:`       | Kick                               |
| 👊 `:punch:`      | Punish                             |


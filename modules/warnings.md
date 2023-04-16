# ⚠ Warnings

### Usage[¶](broken-reference)

Warn misbehaving users and take automated actions.

### Commands[¶](broken-reference)

#### actionlist[¶](broken-reference)

**Syntax**

**Description**

List all configured automated actions for Warnings.

#### mywarnings[¶](broken-reference)

**Syntax**

**Description**

List warnings for yourself.

#### reasonlist[¶](broken-reference)

**Syntax**

**Description**

List all configured reasons for Warnings.

#### unwarn[¶](broken-reference)

**Syntax**

```
[p]unwarn <member> <warn_id> [reason]
```

**Description**

Remove a warning from a member.

**Arguments**

* `<member>`: The member to remove the warning from. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname enclosed in quotes if there are spaces.
* `<warn_id>`: The warning ID to remove from the member.
* `[reason]`: The reason for unwarning this member.

#### warn[¶](broken-reference)

**Syntax**

```
[p]warn <member> [points=1] <reason>
```

**Description**

Warn the user for the specified reason.

**Arguments**

* `<member>`: The member to warn. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname enclosed in quotes if there are spaces.
* `[points]`: The number of points the warning should be for. If no number is supplied, 1 point will be given. Pre-set warnings disregard this.
* `<reason>`: The reason for the warning. This can be a registered reason, or a custom reason if `[p]warningset allowcustomreasons` is set.

#### warnaction[¶](broken-reference)

**Syntax**

**Description**

Manage automated actions for Warnings.

Actions are essentially command macros. Any command can be run when the action is initially triggered, and/or when the action is lifted.

Actions must be given a name and a points threshold. When a user is warned enough so that their points go over this threshold, the action will be executed.

**warnaction add**[**¶**](broken-reference)

**Syntax**

```
[p]warnaction add <name> <points>
```

**Description**

Create an automated action.

Duplicate action names are not allowed.

**Arguments**

* `<name>`: The name of the action.
* `<points>`: The number of points for this action.

**warnaction delete**[**¶**](broken-reference)

**Syntax**

```
[p]warnaction delete <action_name>
```

**Description**

Delete the action with the specified name.

**Arguments**

* `<action_name>`: The name of the action to delete.

#### warnings[¶](broken-reference)

**Syntax**

**Description**

List the warnings for the specified member.

**Arguments**

* `<member>`: The member to get the warnings for. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname.

#### warningset[¶](broken-reference)

**Syntax**

**Description**

Manage settings for Warnings.

**warningset allowcustomreasons**[**¶**](broken-reference)

**Syntax**

```
[p]warningset allowcustomreasons <true_or_false>
```

**Description**

Enable or disable custom reasons for a warning.

**Arguments**

* `<true_or_false>`: You should provide either ‘true’ or ‘false’.

**warningset senddm**[**¶**](broken-reference)

**Syntax**

```
[p]warningset senddm <true_or_false>
```

**Description**

Set whether warnings should be sent to users in DMs.

**Arguments**

* `<true_or_false>`: You should provide either ‘true’ or ‘false’.

**warningset showmoderator**[**¶**](broken-reference)

**Syntax**

```
[p]warningset showmoderator <true_or_false>
```

**Description**

Decide whether the name of the moderator warning a user should be included in the DM to that user.

**Arguments**

* `<true_or_false>`: You should provide either ‘true’ or ‘false’.

**warningset usewarnchannel**[**¶**](broken-reference)

**Syntax**

```
[p]warningset usewarnchannel <true_or_false>
```

**Description**

Set if warnings should be sent to a channel set with `[p]warningset warnchannel`.

**Arguments**

* `<true_or_false>`: You should provide either ‘true’ or ‘false’.

**warningset warnchannel**[**¶**](broken-reference)

**Syntax**

```
[p]warningset warnchannel [channel]
```

**Description**

Set the channel where warnings should be sent to.

**Arguments**

* `[channel]`: You can either mention the channel, provide its exact name or its ID. Leave empty to use the channel `[p]warn` command was called in.

#### warnreason[¶](broken-reference)

**Syntax**

**Description**

Manage warning reasons.

Reasons must be given a name, description and points value. The name of the reason must be given when a user is warned.

**warnreason create**[**¶**](broken-reference)

**Syntax**

```
[p]warnreason create <name> <points> <description>
```

Tip

Alias: `warnreason add`

**Description**

Create a warning reason.

**Arguments**

* `<name>`: The name for the new reason.
* `<points>`: The number of points with the new reason.
* `<description>`: The description of the new warn reason.

**warnreason delete**[**¶**](broken-reference)

**Syntax**

```
[p]warnreason delete <reason_name>
```

**Description**

Delete a warning reason.

**Arguments**

* `<reason_name>`: The name of the reason to delete

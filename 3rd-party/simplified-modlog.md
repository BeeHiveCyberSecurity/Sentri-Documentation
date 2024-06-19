# Simplified ModLog

### Usage[¶](broken-reference)

Manage log channels for moderation actions.

### Commands[¶](broken-reference)

#### case[¶](broken-reference)

**Syntax**

**Description**

Show the specified case.

**Arguments**

* `<case>`: The case number to get information for.

#### casesfor[¶](broken-reference)

**Syntax**

**Description**

Display cases for the specified member.

**Arguments**

* `<member>`: The member to get cases for. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname.

#### listcases[¶](broken-reference)

**Syntax**

**Description**

List cases for the specified member.

**Arguments**

* `<member>`: The member to get cases for. You can either mention the member, provide their ID, their exact name with the tag or not, or their nickname.

#### modlogset[¶](broken-reference)

**Syntax**

**Description**

Manage modlog settings.

**modlogset cases**[**¶**](broken-reference)

**Syntax**

```
[p]modlogset cases [action]
```

**Description**

Enable or disable case creation for a mod action.

**Arguments**

* `[action]`: The action to enable or disable case creation for.

**modlogset modlog**[**¶**](broken-reference)

**Syntax**

```
[p]modlogset modlog [channel]
```

Tip

Alias: `modlogset channel`

**Description**

Set a channel as the modlog.

**Arguments**

* `[channel]`: The channel to set as the modlog. If omitted, the modlog will be disabled.

**modlogset resetcases**[**¶**](broken-reference)

**Syntax**

**Description**

Reset all modlog cases in this server.

#### reason[¶](broken-reference)

**Syntax**

```
[p]reason [case] <reason>
```

**Description**

Specify a reason for a modlog case.

Please note that you can only edit cases you are the owner of unless you are a mod, admin or server owner.

**Arguments**

* `[case]`: The case number to update the reason for.
* `<reason>`: The new reason for the specified case.

Note

If no case number is specified, the latest case will be used

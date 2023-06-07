# 📧 Reports

### Usage[¶](broken-reference)

Create user reports that server staff can respond to.

Users can open reports using `[p]report`. These are then sent to a channel in the server for staff, and the report creator gets a DM. Both can be used to communicate.

### Commands[¶](broken-reference)

#### report[¶](broken-reference)

**Syntax**

**Description**

Send a report.

Use without arguments for interactive reporting, or do `[p]report [text]` to use it non-interactively.

**Arguments**

* `[text]`: The content included within the report.

**report interact**[**¶**](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

```
[p]report interact <ticket_number>
```

**Description**

Open a message tunnel.

This tunnel will forward things you say in this channel to the ticket opener’s direct messages.

Tunnels do not persist across bot restarts.

**Arguments**

* `<ticket_number>`: The ticket number to open the tunnel in.

#### reportset[¶](broken-reference)

**Syntax**

**Description**

Manage Reports.

**reportset output**[**¶**](broken-reference)

**Syntax**

```
[p]reportset output <channel>
```

**Description**

Set the channel where reports will be sent.

**Arguments**

* `<channel>`: You can either mention the channel, provide its exact name or its ID.

**reportset toggle**[**¶**](broken-reference)

**Syntax**

**Description**

Enable or disable reporting for this server

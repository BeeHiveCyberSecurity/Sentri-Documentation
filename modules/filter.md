# 📁 Filter

### Usage[¶](broken-reference)

This module is designed for “filtering” unwanted words and phrases from a server.

It provides tools to manage a list of words or sentences, and to customize automatic actions to be taken against users who use those words in channels or in their name/nickname.

This can be used to prevent inappropriate language, off-topic discussions, invite links, and more.

### Commands[¶](broken-reference)

#### filter[¶](broken-reference)

Note

This command is locked to the mod role.

**Syntax**

**Description**

Base command to add or remove words from the server filter.

Use double quotes to add or remove sentences.

**filter add**[**¶**](broken-reference)

**Syntax**

**Description**

Add words to the filter.

Use double quotes to add sentences.

Examples:

* `[p]filter add word1 word2 word3`
* `[p]filter add "This is a sentence"`

**Arguments:**

* `[words...]` The words or sentences to filter.

**filter channel**[**¶**](broken-reference)

**Syntax**

**Description**

Base command to add or remove words from the channel filter.

Use double quotes to add or remove sentences.

**filter channel add**[**¶**](broken-reference)

**Syntax**

```
[p]filter channel add [words...]
```

**Description**

Add words to the filter.

Use double quotes to add sentences.

Examples:

* `[p]filter channel add word1 word2 word3`
* `[p]filter channel add "This is a sentence"`

**Arguments:**

* `[words...]` The words or sentences to filter.

**filter channel clear**[**¶**](broken-reference)

**Syntax**

**Description**

Clears this channel’s filter list.

**filter channel list**[**¶**](broken-reference)

**Syntax**

**Description**

Send a list of the channel’s filtered words.

**filter channel remove**[**¶**](broken-reference)

**Syntax**

```
[p]filter channel remove [words...]
```

**Description**

Remove words from the filter.

Use double quotes to remove sentences.

Examples:

* `[p]filter channel remove word1 word2 word3`
* `[p]filter channel remove "This is a sentence"`

**Arguments:**

* `[words...]` The words or sentences to no longer filter.

**filter clear**[**¶**](broken-reference)

**Syntax**

**Description**

Clears this server’s filter list.

**filter delete**[**¶**](broken-reference)

**Syntax**

```
[p]filter delete [words...]
```

Tip

Aliases: `filter remove`, `filter del`

**Description**

Remove words from the filter.

Use double quotes to remove sentences.

Examples:

* `[p]filter remove word1 word2 word3`
* `[p]filter remove "This is a sentence"`

**Arguments:**

* `[words...]` The words or sentences to no longer filter.

**filter list**[**¶**](broken-reference)

**Syntax**

**Description**

Send a list of this server’s filtered words.

**filter names**[**¶**](broken-reference)

**Syntax**

**Description**

Toggle name and nickname filtering.

This is disabled by default.

#### filterset[¶](broken-reference)

**Syntax**

**Description**

Base command to manage filter settings.

**filterset ban**[**¶**](broken-reference)

**Syntax**

```
[p]filterset ban <count> <timeframe>
```

**Description**

Set the filter’s autoban conditions.

Users will be banned if they send `<count>` filtered words in `<timeframe>` seconds.

Set both to zero to disable autoban.

Examples:

* `[p]filterset ban 5 5` - Ban users who say 5 filtered words in 5 seconds.
* `[p]filterset ban 2 20` - Ban users who say 2 filtered words in 20 seconds.

**Arguments:**

* `<count>` The amount of filtered words required to trigger a ban.
* `<timeframe>` The period of time in which too many filtered words will trigger a ban.

**filterset defaultname**[**¶**](broken-reference)

**Syntax**

```
[p]filterset defaultname <name>
```

**Description**

Set the nickname for users with a filtered name.

Note that this has no effect if filtering names is disabled (to toggle, run `[p]filter names`).

The default name used is _John Doe_.

Example:

* `[p]filterset defaultname Missingno`

**Arguments:**

* `<name>` The new nickname to assign

---
id: "CommandContext"
title: "Interface: CommandContext"
sidebar_label: "CommandContext"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- `Record`<`PropertyKey`, `unknown`\>

  ↳ **`CommandContext`**

## Properties

### commandName

• **commandName**: `string`

The alias used to run this command.

#### Defined in

[projects/framework/src/lib/structures/Command.ts:523](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L523)

___

### commandPrefix

• **commandPrefix**: `string`

The matched prefix, this will always be the same as [CommandContext.prefix](CommandContext#prefix) if it was a string, otherwise it is
the result of doing `prefix.exec(content)[0]`.

#### Defined in

[projects/framework/src/lib/structures/Command.ts:528](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L528)

___

### prefix

• **prefix**: `string` \| [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

The prefix used to run this command.

This is a string for the mention and default prefix, and a RegExp for the `regexPrefix`.

#### Defined in

[projects/framework/src/lib/structures/Command.ts:519](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L519)

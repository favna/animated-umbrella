---
id: "ArgumentContext"
title: "Interface: ArgumentContext<T>"
sidebar_label: "ArgumentContext"
sidebar_position: 0
custom_edit_url: null
---

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `unknown` |

## Hierarchy

- `Record`<`PropertyKey`, `unknown`\>

  ↳ **`ArgumentContext`**

  ↳↳ [`ExtendedArgumentContext`](ExtendedArgumentContext)

## Properties

### args

• **args**: [`Args`](../classes/Args)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:116](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L116)

___

### argument

• **argument**: [`IArgument`](IArgument)<`T`\>

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:115](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L115)

___

### command

• **command**: [`Command`](../classes/Command)<[`Args`](../classes/Args), [`CommandOptions`](CommandOptions)\>

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:118](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L118)

___

### commandContext

• **commandContext**: [`CommandContext`](CommandContext)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:119](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L119)

___

### inclusive

• `Optional` **inclusive**: `boolean`

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:122](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L122)

___

### maximum

• `Optional` **maximum**: `number`

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:121](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L121)

___

### message

• **message**: [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:117](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L117)

___

### minimum

• `Optional` **minimum**: `number`

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:120](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L120)

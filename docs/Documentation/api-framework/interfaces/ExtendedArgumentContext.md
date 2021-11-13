---
id: "ExtendedArgumentContext"
title: "Interface: ExtendedArgumentContext"
sidebar_label: "ExtendedArgumentContext"
sidebar_position: 0
custom_edit_url: null
---

**`deprecated`** [ExtendedArgument](../classes/ExtendedArgument) is deprecated and will be removed in v3.0.0.

## Hierarchy

- [`ArgumentContext`](ArgumentContext)

  ↳ **`ExtendedArgumentContext`**

## Properties

### args

• **args**: [`Args`](../classes/Args)

#### Inherited from

[ArgumentContext](ArgumentContext).[args](ArgumentContext#args)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:116](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L116)

___

### argument

• **argument**: [`IArgument`](IArgument)<`unknown`\>

#### Inherited from

[ArgumentContext](ArgumentContext).[argument](ArgumentContext#argument)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:115](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L115)

___

### command

• **command**: [`Command`](../classes/Command)<[`Args`](../classes/Args), [`CommandOptions`](CommandOptions)\>

#### Inherited from

[ArgumentContext](ArgumentContext).[command](ArgumentContext#command)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:118](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L118)

___

### commandContext

• **commandContext**: [`CommandContext`](CommandContext)

#### Inherited from

[ArgumentContext](ArgumentContext).[commandContext](ArgumentContext#commandcontext)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:119](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L119)

___

### inclusive

• `Optional` **inclusive**: `boolean`

#### Inherited from

[ArgumentContext](ArgumentContext).[inclusive](ArgumentContext#inclusive)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:122](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L122)

___

### maximum

• `Optional` **maximum**: `number`

#### Inherited from

[ArgumentContext](ArgumentContext).[maximum](ArgumentContext#maximum)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:121](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L121)

___

### message

• **message**: [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

#### Inherited from

[ArgumentContext](ArgumentContext).[message](ArgumentContext#message)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:117](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L117)

___

### minimum

• `Optional` **minimum**: `number`

#### Inherited from

[ArgumentContext](ArgumentContext).[minimum](ArgumentContext#minimum)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:120](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L120)

___

### parameter

• **parameter**: `string`

The canonical parameter specified by the user in the command, as
a string, equivalent to the first parameter of {@link Argument#run}.
This allows {@link ExtendedArgument#handle} to access the original
argument, which is useful for returning {@link Argument#error} so
that you don't have to convert the parsed argument back into a
string.

#### Defined in

[projects/framework/src/lib/structures/ExtendedArgument.ts:115](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/ExtendedArgument.ts#L115)

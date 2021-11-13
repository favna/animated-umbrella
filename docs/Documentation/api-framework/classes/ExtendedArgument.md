---
id: "ExtendedArgument"
title: "Class: ExtendedArgument<K, T>"
sidebar_label: "ExtendedArgument"
sidebar_position: 0
custom_edit_url: null
---

**`deprecated`** [ExtendedArgument](ExtendedArgument) is deprecated and will be removed in v3.0.0.
Use [Argument](Argument) instead, and abstract the resolving of the argument data to an external resolver.
---
The extended argument class. This class is abstract and is to be extended by subclasses which
will implement the {@link ExtendedArgument#handle} method.
Much like the [Argument](Argument) class, this class handles parsing user-specified command arguments
into typed command parameters. However, this class can be used to expand upon an existing
argument in order to process its transformed value rather than just the argument string.

**`example`**
```typescript
// TypeScript:
import { ApplyOptions } from '@sapphire/decorators';
import { ArgumentResult, ExtendedArgument, ExtendedArgumentContext, ExtendedArgumentOptions } from '@sapphire/framework';
import type { Channel, TextChannel } from 'discord.js';

// Just like with `Argument`, you can use `export default` or `export =` too.
(at)ApplyOptions<ExtendedArgumentOptions>({
  name: 'textChannel',
  baseArgument: 'channel'
})
export class TextChannelArgument extends ExtendedArgument<'channel', TextChannel> {
  public handle(parsed: Channel, { argument }: ExtendedArgumentContext): ArgumentResult<TextChannel> {
    return parsed.type === 'text'
      ? this.ok(parsed as TextChannel)
      : this.error({ identifier: 'ArgumentTextChannelInvalidTextChannel', message: 'The argument did not resolve to a text channel.' });
  }
}
```

**`example`**
```javascript
// JavaScript:
const { ExtendedArgument } = require('@sapphire/framework');

module.exports = class TextChannelArgument extends ExtendedArgument {
  constructor(context) {
    super(context, { name: 'textChannel', baseArgument: 'channel' });
  }

  handle(parsed, { argument }) {
    return parsed.type === 'text'
      ? this.ok(parsed)
      : this.error({ identifier: 'ArgumentTextChannelInvalidTextChannel', message: 'The argument did not resolve to a text channel' });
  }
}
```

## Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](../interfaces/ArgType) |
| `T` | `T` |

## Hierarchy

- [`Argument`](Argument)<`T`\>

  ↳ **`ExtendedArgument`**

## Constructors

### constructor

• **new ExtendedArgument**<`K`, `T`\>(`context`, `options`)

**`deprecated`** [ExtendedArgument](ExtendedArgument) is deprecated and will be removed in v3.0.0.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](../interfaces/ArgType) |
| `T` | `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `context` | [`PieceContext`](../interfaces/PieceContext) |
| `options` | [`ExtendedArgumentOptions`](../interfaces/ExtendedArgumentOptions)<`K`\> |

#### Overrides

[Argument](Argument).[constructor](Argument#constructor)

#### Defined in

[projects/framework/src/lib/structures/ExtendedArgument.ts:61](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/ExtendedArgument.ts#L61)

## Properties

### aliases

• **aliases**: readonly `string`[]

The aliases for the piece.

#### Inherited from

[Argument](Argument).[aliases](Argument#aliases)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:670

___

### baseArgument

• **baseArgument**: `K`

#### Defined in

[projects/framework/src/lib/structures/ExtendedArgument.ts:56](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/ExtendedArgument.ts#L56)

___

### enabled

• **enabled**: `boolean`

Whether or not the piece is enabled.

#### Inherited from

[Argument](Argument).[enabled](Argument#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:432

___

### location

• `Readonly` **location**: `PieceLocation`

The location metadata for the piece's file.

#### Inherited from

[Argument](Argument).[location](Argument#location)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:424

___

### name

• `Readonly` **name**: `string`

The name of the piece.

#### Inherited from

[Argument](Argument).[name](Argument#name)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:428

___

### options

• `Readonly` **options**: [`ArgumentOptions`](../interfaces/ArgumentOptions)

The raw options passed to this [Piece](Piece)

#### Inherited from

[Argument](Argument).[options](Argument#options)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:436

___

### store

• `Readonly` **store**: [`Store`](Store)<[`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions)\>\>

The store that contains the piece.

#### Inherited from

[Argument](Argument).[store](Argument#store)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:420

## Accessors

### base

• `get` **base**(): [`IArgument`](../interfaces/IArgument)<[`ArgType`](../interfaces/ArgType)[`K`]\>

Represents the underlying argument that transforms the raw argument
into the value used to compute the extended argument's value.

**`deprecated`** [ExtendedArgument](ExtendedArgument) is deprecated and will be removed in v3.0.0.

#### Returns

[`IArgument`](../interfaces/IArgument)<[`ArgType`](../interfaces/ArgType)[`K`]\>

#### Defined in

[projects/framework/src/lib/structures/ExtendedArgument.ts:71](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/ExtendedArgument.ts#L71)

___

### container

• `get` **container**(): `Container`

A reference to the {@link Container} object for ease of use.

**`see`** container

#### Returns

`Container`

#### Inherited from

Argument.container

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:442

## Methods

### error

▸ **error**(`options`): [`ArgumentResult`](../#argumentresult)<`T`\>

Constructs an [ArgumentError](ArgumentError) with a custom type.

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `Omit`<[`Options`](../interfaces/ArgumentError.Options)<`T`\>, ``"argument"``\> |

#### Returns

[`ArgumentResult`](../#argumentresult)<`T`\>

#### Inherited from

[Argument](Argument).[error](Argument#error)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:107](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L107)

___

### handle

▸ `Abstract` **handle**(`parsed`, `context`): [`ArgumentResult`](../#argumentresult)<`T`\>

**`deprecated`** [ExtendedArgument](ExtendedArgument) is deprecated and will be removed in v3.0.0.

#### Parameters

| Name | Type |
| :------ | :------ |
| `parsed` | [`ArgType`](../interfaces/ArgType)[`K`] |
| `context` | [`ExtendedArgumentContext`](../interfaces/ExtendedArgumentContext) |

#### Returns

[`ArgumentResult`](../#argumentresult)<`T`\>

#### Defined in

[projects/framework/src/lib/structures/ExtendedArgument.ts:89](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/ExtendedArgument.ts#L89)

___

### ok

▸ **ok**(`value`): [`ArgumentResult`](../#argumentresult)<`T`\>

Wraps a value into a successful value.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `T` | The value to wrap. |

#### Returns

[`ArgumentResult`](../#argumentresult)<`T`\>

#### Inherited from

[Argument](Argument).[ok](Argument#ok)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:97](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L97)

___

### onLoad

▸ **onLoad**(): `unknown`

Per-piece listener that is called when the piece is loaded into the store.
Useful to set-up asynchronous initialization tasks.

#### Returns

`unknown`

#### Inherited from

[Argument](Argument).[onLoad](Argument#onload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:447

___

### onUnload

▸ **onUnload**(): `unknown`

Per-piece listener that is called when the piece is unloaded from the store.
Useful to set-up clean-up tasks.

#### Returns

`unknown`

#### Inherited from

[Argument](Argument).[onUnload](Argument#onunload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:452

___

### reload

▸ **reload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Reloads the piece by loading the same path in the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Argument](Argument).[reload](Argument#reload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:460

___

### run

▸ **run**(`parameter`, `context`): [`AsyncArgumentResult`](../#asyncargumentresult)<`T`\>

**`deprecated`** [ExtendedArgument](ExtendedArgument) is deprecated and will be removed in v3.0.0.

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `context` | [`ArgumentContext`](../interfaces/ArgumentContext)<`T`\> |

#### Returns

[`AsyncArgumentResult`](../#asyncargumentresult)<`T`\>

#### Overrides

[Argument](Argument).[run](Argument#run)

#### Defined in

[projects/framework/src/lib/structures/ExtendedArgument.ts:78](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/ExtendedArgument.ts#L78)

___

### toJSON

▸ **toJSON**(): `AliasPieceJSON`

Defines the `JSON.stringify` behavior of this alias piece.

#### Returns

`AliasPieceJSON`

#### Inherited from

[Argument](Argument).[toJSON](Argument#tojson)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:675

___

### unload

▸ **unload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Unloads and disables the piece.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Argument](Argument).[unload](Argument#unload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:456

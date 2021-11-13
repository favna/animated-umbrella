---
id: "Argument"
title: "Class: Argument<T, O>"
sidebar_label: "Argument"
sidebar_position: 0
custom_edit_url: null
---

The base argument class. This class is abstract and is to be extended by subclasses implementing the methods. In
Sapphire's workflow, arguments are called when using [Args](Args)'s methods (usually used inside [Command](Command)s by default).

**`example`**
```typescript
// TypeScript:
import { Argument, ArgumentResult, PieceContext } from '@sapphire/framework';
import { URL } from 'url';

// Define a class extending `Argument`, then export it.
// NOTE: You can use `export default` or `export =` too.
export class CoreArgument extends Argument<URL> {
  public constructor(context: PieceContext) {
    super(context, { name: 'hyperlink', aliases: ['url'] });
  }

  public run(argument: string): ArgumentResult<URL> {
    try {
      return this.ok(new URL(argument));
    } catch {
      return this.error(argument, 'ArgumentHyperlinkInvalidURL', 'The argument did not resolve to a valid URL.');
    }
  }
}

// Augment the ArgType structure so `args.pick('url')`, `args.repeat('url')`
// and others have a return type of `URL`.
declare module '@sapphire/framework' {
  export interface ArgType {
    url: URL;
  }
}
```

**`example`**
```javascript
// JavaScript:
const { Argument } = require('@sapphire/framework');

// Define a class extending `Argument`, then export it.
module.exports = class CoreArgument extends Argument {
  constructor(context) {
    super(context, { name: 'hyperlink', aliases: ['url'] });
  }

  run(argument) {
    try {
      return this.ok(new URL(argument));
    } catch {
      return this.error(argument, 'ArgumentHyperlinkInvalidURL', 'The argument did not resolve to a valid URL.');
    }
  }
}
```

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `unknown` |
| `O` | extends [`ArgumentOptions`](../interfaces/ArgumentOptions)[`ArgumentOptions`](../interfaces/ArgumentOptions) |

## Hierarchy

- [`AliasPiece`](AliasPiece)<`O`\>

  ↳ **`Argument`**

  ↳↳ [`ExtendedArgument`](ExtendedArgument)

## Implements

- [`IArgument`](../interfaces/IArgument)<`T`\>

## Constructors

### constructor

• **new Argument**<`T`, `O`\>(`context`, `options?`)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `unknown` |
| `O` | extends [`ArgumentOptions`](../interfaces/ArgumentOptions)[`ArgumentOptions`](../interfaces/ArgumentOptions) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `context` | [`PieceContext`](../interfaces/PieceContext) |
| `options?` | [`AliasPieceOptions`](../interfaces/AliasPieceOptions) |

#### Inherited from

[AliasPiece](AliasPiece).[constructor](AliasPiece#constructor)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:671

## Properties

### aliases

• **aliases**: readonly `string`[]

The aliases for the piece.

#### Inherited from

[AliasPiece](AliasPiece).[aliases](AliasPiece#aliases)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:670

___

### enabled

• **enabled**: `boolean`

Whether or not the piece is enabled.

#### Inherited from

[AliasPiece](AliasPiece).[enabled](AliasPiece#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:432

___

### location

• `Readonly` **location**: `PieceLocation`

The location metadata for the piece's file.

#### Inherited from

[AliasPiece](AliasPiece).[location](AliasPiece#location)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:424

___

### name

• `Readonly` **name**: `string`

The name of the piece.

#### Implementation of

[IArgument](../interfaces/IArgument).[name](../interfaces/IArgument#name)

#### Inherited from

[AliasPiece](AliasPiece).[name](AliasPiece#name)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:428

___

### options

• `Readonly` **options**: `O`

The raw options passed to this [Piece](Piece)

#### Inherited from

[AliasPiece](AliasPiece).[options](AliasPiece#options)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:436

___

### store

• `Readonly` **store**: [`Store`](Store)<[`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions)\>\>

The store that contains the piece.

#### Inherited from

[AliasPiece](AliasPiece).[store](AliasPiece#store)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:420

## Accessors

### container

• `get` **container**(): `Container`

A reference to the {@link Container} object for ease of use.

**`see`** container

#### Returns

`Container`

#### Inherited from

AliasPiece.container

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

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:107](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L107)

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

[AliasPiece](AliasPiece).[onLoad](AliasPiece#onload)

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

[AliasPiece](AliasPiece).[onUnload](AliasPiece#onunload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:452

___

### reload

▸ **reload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Reloads the piece by loading the same path in the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[AliasPiece](AliasPiece).[reload](AliasPiece#reload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:460

___

### run

▸ `Abstract` **run**(`parameter`, `context`): [`ArgumentResult`](../#argumentresult)<`T`\>

The method which is called when invoking the argument.

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `context` | [`ArgumentContext`](../interfaces/ArgumentContext)<`T`\> |

#### Returns

[`ArgumentResult`](../#argumentresult)<`T`\>

#### Implementation of

[IArgument](../interfaces/IArgument).[run](../interfaces/IArgument#run)

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:91](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L91)

___

### toJSON

▸ **toJSON**(): `AliasPieceJSON`

Defines the `JSON.stringify` behavior of this alias piece.

#### Returns

`AliasPieceJSON`

#### Inherited from

[AliasPiece](AliasPiece).[toJSON](AliasPiece#tojson)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:675

___

### unload

▸ **unload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Unloads and disables the piece.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[AliasPiece](AliasPiece).[unload](AliasPiece#unload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:456

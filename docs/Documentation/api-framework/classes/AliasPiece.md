---
id: "AliasPiece"
title: "Class: AliasPiece<O>"
sidebar_label: "AliasPiece"
sidebar_position: 0
custom_edit_url: null
---

The piece to be stored in [AliasStore](AliasStore) instances.

## Type parameters

| Name | Type |
| :------ | :------ |
| `O` | extends [`AliasPieceOptions`](../interfaces/AliasPieceOptions)[`AliasPieceOptions`](../interfaces/AliasPieceOptions) |

## Hierarchy

- [`Piece`](Piece)<`O`\>

  ↳ **`AliasPiece`**

  ↳↳ [`Argument`](Argument)

  ↳↳ [`Command`](Command)

## Constructors

### constructor

• **new AliasPiece**<`O`\>(`context`, `options?`)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `O` | extends [`AliasPieceOptions`](../interfaces/AliasPieceOptions)[`AliasPieceOptions`](../interfaces/AliasPieceOptions) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `context` | [`PieceContext`](../interfaces/PieceContext) |
| `options?` | [`AliasPieceOptions`](../interfaces/AliasPieceOptions) |

#### Overrides

[Piece](Piece).[constructor](Piece#constructor)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:671

## Properties

### aliases

• **aliases**: readonly `string`[]

The aliases for the piece.

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:670

___

### enabled

• **enabled**: `boolean`

Whether or not the piece is enabled.

#### Inherited from

[Piece](Piece).[enabled](Piece#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:432

___

### location

• `Readonly` **location**: `PieceLocation`

The location metadata for the piece's file.

#### Inherited from

[Piece](Piece).[location](Piece#location)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:424

___

### name

• `Readonly` **name**: `string`

The name of the piece.

#### Inherited from

[Piece](Piece).[name](Piece#name)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:428

___

### options

• `Readonly` **options**: `O`

The raw options passed to this [Piece](Piece)

#### Inherited from

[Piece](Piece).[options](Piece#options)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:436

___

### store

• `Readonly` **store**: [`Store`](Store)<[`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions)\>\>

The store that contains the piece.

#### Inherited from

[Piece](Piece).[store](Piece#store)

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

Piece.container

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:442

## Methods

### onLoad

▸ **onLoad**(): `unknown`

Per-piece listener that is called when the piece is loaded into the store.
Useful to set-up asynchronous initialization tasks.

#### Returns

`unknown`

#### Inherited from

[Piece](Piece).[onLoad](Piece#onload)

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

[Piece](Piece).[onUnload](Piece#onunload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:452

___

### reload

▸ **reload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Reloads the piece by loading the same path in the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Piece](Piece).[reload](Piece#reload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:460

___

### toJSON

▸ **toJSON**(): `AliasPieceJSON`

Defines the `JSON.stringify` behavior of this alias piece.

#### Returns

`AliasPieceJSON`

#### Overrides

[Piece](Piece).[toJSON](Piece#tojson)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:675

___

### unload

▸ **unload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Unloads and disables the piece.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Piece](Piece).[unload](Piece#unload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:456

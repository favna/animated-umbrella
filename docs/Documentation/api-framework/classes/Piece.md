---
id: "Piece"
title: "Class: Piece<O>"
sidebar_label: "Piece"
sidebar_position: 0
custom_edit_url: null
---

The piece to be stored in [Store](Store) instances.

## Type parameters

| Name | Type |
| :------ | :------ |
| `O` | extends [`PieceOptions`](../interfaces/PieceOptions)[`PieceOptions`](../interfaces/PieceOptions) |

## Hierarchy

- **`Piece`**

  ↳ [`AliasPiece`](AliasPiece)

  ↳ [`Listener`](Listener)

  ↳ [`Precondition`](Precondition)

## Constructors

### constructor

• **new Piece**<`O`\>(`context`, `options?`)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `O` | extends [`PieceOptions`](../interfaces/PieceOptions)[`PieceOptions`](../interfaces/PieceOptions) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `context` | [`PieceContext`](../interfaces/PieceContext) |
| `options?` | [`PieceOptions`](../interfaces/PieceOptions) |

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:437

## Properties

### enabled

• **enabled**: `boolean`

Whether or not the piece is enabled.

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:432

___

### location

• `Readonly` **location**: `PieceLocation`

The location metadata for the piece's file.

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:424

___

### name

• `Readonly` **name**: `string`

The name of the piece.

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:428

___

### options

• `Readonly` **options**: `O`

The raw options passed to this [Piece](Piece)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:436

___

### store

• `Readonly` **store**: [`Store`](Store)<[`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions)\>\>

The store that contains the piece.

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:420

## Accessors

### container

• `get` **container**(): `Container`

A reference to the {@link Container} object for ease of use.

**`see`** container

#### Returns

`Container`

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:442

## Methods

### onLoad

▸ **onLoad**(): `unknown`

Per-piece listener that is called when the piece is loaded into the store.
Useful to set-up asynchronous initialization tasks.

#### Returns

`unknown`

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:447

___

### onUnload

▸ **onUnload**(): `unknown`

Per-piece listener that is called when the piece is unloaded from the store.
Useful to set-up clean-up tasks.

#### Returns

`unknown`

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:452

___

### reload

▸ **reload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Reloads the piece by loading the same path in the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:460

___

### toJSON

▸ **toJSON**(): `PieceJSON`

Defines the `JSON.stringify` behavior of this piece.

#### Returns

`PieceJSON`

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:464

___

### unload

▸ **unload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Unloads and disables the piece.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:456

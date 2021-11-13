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
| `options` | [`PieceOptions`](../interfaces/PieceOptions) |

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:78](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L78)

## Properties

### enabled

• **enabled**: `boolean`

Whether or not the piece is enabled.

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:71](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L71)

___

### location

• `Readonly` **location**: [`PieceLocation`](PieceLocation)

The location metadata for the piece's file.

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:61](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L61)

___

### name

• `Readonly` **name**: `string`

The name of the piece.

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:66](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L66)

___

### options

• `Readonly` **options**: `O`

The raw options passed to this [Piece](Piece)

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:76](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L76)

___

### store

• `Readonly` **store**: [`Store`](Store)<[`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions)\>\>

The store that contains the piece.

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:56](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L56)

## Accessors

### container

• `get` **container**(): [`Container`](../interfaces/Container)

A reference to the [Container](../interfaces/Container) object for ease of use.

**`see`** container

#### Returns

[`Container`](../interfaces/Container)

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:90](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L90)

## Methods

### onLoad

▸ **onLoad**(): `unknown`

Per-piece listener that is called when the piece is loaded into the store.
Useful to set-up asynchronous initialization tasks.

#### Returns

`unknown`

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:98](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L98)

___

### onUnload

▸ **onUnload**(): `unknown`

Per-piece listener that is called when the piece is unloaded from the store.
Useful to set-up clean-up tasks.

#### Returns

`unknown`

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:106](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L106)

___

### reload

▸ **reload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Reloads the piece by loading the same path in the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:121](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L121)

___

### toJSON

▸ **toJSON**(): [`PieceJSON`](../interfaces/PieceJSON)

Defines the `JSON.stringify` behavior of this piece.

#### Returns

[`PieceJSON`](../interfaces/PieceJSON)

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:128](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L128)

___

### unload

▸ **unload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Unloads and disables the piece.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:113](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L113)

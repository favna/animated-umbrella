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
| `options` | [`AliasPieceOptions`](../interfaces/AliasPieceOptions) |

#### Overrides

[Piece](Piece).[constructor](Piece#constructor)

#### Defined in

[projects/pieces/src/lib/structures/AliasPiece.ts:20](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/AliasPiece.ts#L20)

## Properties

### aliases

• **aliases**: readonly `string`[]

The aliases for the piece.

#### Defined in

[projects/pieces/src/lib/structures/AliasPiece.ts:18](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/AliasPiece.ts#L18)

___

### enabled

• **enabled**: `boolean`

Whether or not the piece is enabled.

#### Inherited from

[Piece](Piece).[enabled](Piece#enabled)

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:71](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L71)

___

### location

• `Readonly` **location**: [`PieceLocation`](PieceLocation)

The location metadata for the piece's file.

#### Inherited from

[Piece](Piece).[location](Piece#location)

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:61](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L61)

___

### name

• `Readonly` **name**: `string`

The name of the piece.

#### Inherited from

[Piece](Piece).[name](Piece#name)

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:66](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L66)

___

### options

• `Readonly` **options**: `O`

The raw options passed to this [Piece](Piece)

#### Inherited from

[Piece](Piece).[options](Piece#options)

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:76](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L76)

___

### store

• `Readonly` **store**: [`Store`](Store)<[`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions)\>\>

The store that contains the piece.

#### Inherited from

[Piece](Piece).[store](Piece#store)

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:56](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L56)

## Accessors

### container

• `get` **container**(): [`Container`](../interfaces/Container)

A reference to the [Container](../interfaces/Container) object for ease of use.

**`see`** container

#### Returns

[`Container`](../interfaces/Container)

#### Inherited from

Piece.container

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:90](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L90)

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

[projects/pieces/src/lib/structures/Piece.ts:98](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L98)

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

[projects/pieces/src/lib/structures/Piece.ts:106](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L106)

___

### reload

▸ **reload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Reloads the piece by loading the same path in the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Piece](Piece).[reload](Piece#reload)

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:121](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L121)

___

### toJSON

▸ **toJSON**(): [`AliasPieceJSON`](../interfaces/AliasPieceJSON)

Defines the `JSON.stringify` behavior of this alias piece.

#### Returns

[`AliasPieceJSON`](../interfaces/AliasPieceJSON)

#### Overrides

[Piece](Piece).[toJSON](Piece#tojson)

#### Defined in

[projects/pieces/src/lib/structures/AliasPiece.ts:28](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/AliasPiece.ts#L28)

___

### unload

▸ **unload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Unloads and disables the piece.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Piece](Piece).[unload](Piece#unload)

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:113](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L113)

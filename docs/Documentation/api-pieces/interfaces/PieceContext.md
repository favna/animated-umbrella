---
id: "PieceContext"
title: "Interface: PieceContext"
sidebar_label: "PieceContext"
sidebar_position: 0
custom_edit_url: null
---

The context for the piece, contains extra information from the store,
the piece's path, and the store that loaded it.

## Properties

### name

• `Readonly` **name**: `string`

The module's name extracted from the path.

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:24](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L24)

___

### path

• `Readonly` **path**: `string`

The path the module was loaded from, relative to [PieceContext.root](PieceContext#root).

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:19](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L19)

___

### root

• `Readonly` **root**: `string`

The root directory the piece was loaded from.

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:14](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L14)

___

### store

• `Readonly` **store**: [`Store`](../classes/Store)<[`Piece`](../classes/Piece)<[`PieceOptions`](PieceOptions)\>\>

The store that loaded the piece.

#### Defined in

[projects/pieces/src/lib/structures/Piece.ts:29](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Piece.ts#L29)

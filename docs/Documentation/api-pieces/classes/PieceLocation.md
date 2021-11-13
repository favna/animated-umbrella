---
id: "PieceLocation"
title: "Class: PieceLocation"
sidebar_label: "PieceLocation"
sidebar_position: 0
custom_edit_url: null
---

The metadata class used for [Piece](Piece)s.

## Constructors

### constructor

• **new PieceLocation**(`full`, `root`)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `full` | `string` | The full path to the file. |
| `root` | `string` | The root directory the file was found from. |

#### Defined in

[projects/pieces/src/lib/structures/PieceLocation.ts:21](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/PieceLocation.ts#L21)

## Properties

### full

• `Readonly` **full**: `string`

The full path to the file.

#### Defined in

[projects/pieces/src/lib/structures/PieceLocation.ts:10](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/PieceLocation.ts#L10)

___

### root

• `Readonly` **root**: `string`

The root directory the file was found from.

#### Defined in

[projects/pieces/src/lib/structures/PieceLocation.ts:15](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/PieceLocation.ts#L15)

## Accessors

### directories

• `get` **directories**(): `string`[]

The names of the directories that separate [PieceLocation.root](PieceLocation#root) and [PieceLocation.full](PieceLocation#full).

**`example`**
```typescript
const location = new PieceLocation(
	'/usr/src/app/commands',
	'/usr/src/app/commands/games/multiplayer/connect-four.js'
);

console.log(location.directories);
// → ['games', 'multiplayer']
```

#### Returns

`string`[]

#### Defined in

[projects/pieces/src/lib/structures/PieceLocation.ts:56](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/PieceLocation.ts#L56)

___

### name

• `get` **name**(): `string`

The name and extension of the file that was loaded, extracted from [PieceLocation.full](PieceLocation#full).

**`example`**
```typescript
const location = new PieceLocation(
	'/usr/src/app/commands',
	'/usr/src/app/commands/games/multiplayer/connect-four.js'
);

console.log(location.name);
// → 'connect-four.js'
```

#### Returns

`string`

#### Defined in

[projects/pieces/src/lib/structures/PieceLocation.ts:73](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/PieceLocation.ts#L73)

___

### relative

• `get` **relative**(): `string`

The relative path between [PieceLocation.root](PieceLocation#root) and [PieceLocation.full](PieceLocation#full).

**`example`**
```typescript
const location = new PieceLocation(
	'/usr/src/app/commands',
	'/usr/src/app/commands/general/ping.js'
);

console.log(location.relative);
// → 'general/ping.js'
```

#### Returns

`string`

#### Defined in

[projects/pieces/src/lib/structures/PieceLocation.ts:39](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/PieceLocation.ts#L39)

## Methods

### toJSON

▸ **toJSON**(): [`PieceLocationJSON`](../interfaces/PieceLocationJSON)

Defines the `JSON.stringify` behavior of this structure.

#### Returns

[`PieceLocationJSON`](../interfaces/PieceLocationJSON)

#### Defined in

[projects/pieces/src/lib/structures/PieceLocation.ts:80](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/PieceLocation.ts#L80)

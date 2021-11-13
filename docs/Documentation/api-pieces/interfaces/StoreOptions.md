---
id: "StoreOptions"
title: "Interface: StoreOptions<T>"
sidebar_label: "StoreOptions"
sidebar_position: 0
custom_edit_url: null
---

The options for the store, this features both hooks (changes the behaviour) and handlers (similar to event listeners).

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Piece`](../classes/Piece) |

## Properties

### name

• `Readonly` **name**: `string`

The name for this store.

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:18](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L18)

___

### paths

• `Optional` `Readonly` **paths**: readonly `string`[]

The paths to load pieces from, should be absolute.

**`default`** []

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:24](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L24)

___

### strategy

• `Optional` `Readonly` **strategy**: [`ILoaderStrategy`](ILoaderStrategy)<`T`\>

The strategy to be used for the loader.

**`default`** Store.defaultStrategy

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:30](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L30)

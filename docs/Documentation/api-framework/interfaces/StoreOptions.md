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

node_modules/@sapphire/pieces/dist/index.d.ts:251

___

### paths

• `Optional` `Readonly` **paths**: readonly `string`[]

The paths to load pieces from, should be absolute.

**`default`** []

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:256

___

### strategy

• `Optional` `Readonly` **strategy**: `ILoaderStrategy`<`T`\>

The strategy to be used for the loader.

**`default`** Store.defaultStrategy

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:261

---
id: "PreconditionOptions"
title: "Interface: PreconditionOptions"
sidebar_label: "PreconditionOptions"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`PieceOptions`](PieceOptions)

  ↳ **`PreconditionOptions`**

## Properties

### enabled

• `Optional` `Readonly` **enabled**: `boolean`

Whether or not the piece should be enabled. If set to false, the piece will be unloaded.

**`default`** true

#### Inherited from

[PieceOptions](PieceOptions).[enabled](PieceOptions#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:411

___

### name

• `Optional` `Readonly` **name**: `string`

The name for the piece.

**`default`** ''

#### Inherited from

[PieceOptions](PieceOptions).[name](PieceOptions#name)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:406

___

### position

• `Optional` **position**: ``null`` \| `number`

The position for the precondition to be set at in the global precondition list. If set to `null`, this
precondition will not be set as a global one.

**`default`** null

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:114](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L114)

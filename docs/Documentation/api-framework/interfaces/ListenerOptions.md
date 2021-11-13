---
id: "ListenerOptions"
title: "Interface: ListenerOptions"
sidebar_label: "ListenerOptions"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`PieceOptions`](PieceOptions)

  ↳ **`ListenerOptions`**

## Properties

### emitter

• `Optional` `Readonly` **emitter**: `EventEmitter` \| keyof [`Client`](https://discord.js.org/#/docs/main/stable/class/Client)<`boolean`\>

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:136](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L136)

___

### enabled

• `Optional` `Readonly` **enabled**: `boolean`

Whether or not the piece should be enabled. If set to false, the piece will be unloaded.

**`default`** true

#### Inherited from

[PieceOptions](PieceOptions).[enabled](PieceOptions#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:411

___

### event

• `Optional` `Readonly` **event**: `string`

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:137](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L137)

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

### once

• `Optional` `Readonly` **once**: `boolean`

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:138](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L138)

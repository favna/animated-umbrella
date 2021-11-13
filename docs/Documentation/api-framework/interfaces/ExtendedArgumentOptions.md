---
id: "ExtendedArgumentOptions"
title: "Interface: ExtendedArgumentOptions<K>"
sidebar_label: "ExtendedArgumentOptions"
sidebar_position: 0
custom_edit_url: null
---

**`deprecated`** [ExtendedArgument](../classes/ExtendedArgument) is deprecated and will be removed in v3.0.0.

## Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](ArgType) |

## Hierarchy

- [`ArgumentOptions`](ArgumentOptions)

  ↳ **`ExtendedArgumentOptions`**

## Properties

### aliases

• `Optional` `Readonly` **aliases**: readonly `string`[]

The aliases for the piece.

**`default`** []

#### Inherited from

[ArgumentOptions](ArgumentOptions).[aliases](ArgumentOptions#aliases)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:661

___

### baseArgument

• **baseArgument**: `K`

The name of the underlying argument whose value is used to compute
the extended argument value; see [ArgType](ArgType) for valid keys.

#### Defined in

[projects/framework/src/lib/structures/ExtendedArgument.ts:100](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/ExtendedArgument.ts#L100)

___

### enabled

• `Optional` `Readonly` **enabled**: `boolean`

Whether or not the piece should be enabled. If set to false, the piece will be unloaded.

**`default`** true

#### Inherited from

[ArgumentOptions](ArgumentOptions).[enabled](ArgumentOptions#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:411

___

### name

• `Optional` `Readonly` **name**: `string`

The name for the piece.

**`default`** ''

#### Inherited from

[ArgumentOptions](ArgumentOptions).[name](ArgumentOptions#name)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:406

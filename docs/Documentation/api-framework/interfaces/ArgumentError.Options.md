---
id: "ArgumentError.Options"
title: "Interface: Options<T>"
sidebar_label: "ArgumentError.Options"
custom_edit_url: null
---

[ArgumentError](../namespaces/ArgumentError).Options

The options for [ArgumentError](../classes/ArgumentError).

**`since`** 1.0.0

## Type parameters

| Name |
| :------ |
| `T` |

## Hierarchy

- `Omit`<[`Options`](UserError.Options), ``"identifier"``\>

  ↳ **`Options`**

## Properties

### argument

• **argument**: [`IArgument`](IArgument)<`T`\>

The argument that caused the error.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/errors/ArgumentError.ts:36](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/ArgumentError.ts#L36)

___

### context

• `Optional` **context**: `unknown`

The extra context to provide more information about this error.

**`since`** 1.0.0

**`default`** null

#### Inherited from

Omit.context

#### Defined in

[projects/framework/src/lib/errors/UserError.ts:57](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/UserError.ts#L57)

___

### identifier

• `Optional` **identifier**: `string`

The identifier.

**`since`** 1.0.0

**`default`** argument.name

#### Defined in

[projects/framework/src/lib/errors/ArgumentError.ts:49](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/ArgumentError.ts#L49)

___

### message

• `Optional` **message**: `string`

The message to be passed to the Error constructor.

**`since`** 1.0.0

#### Inherited from

Omit.message

#### Defined in

[projects/framework/src/lib/errors/UserError.ts:50](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/UserError.ts#L50)

___

### parameter

• **parameter**: `string`

The parameter that failed to be parsed.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/errors/ArgumentError.ts:42](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/ArgumentError.ts#L42)

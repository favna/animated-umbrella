---
id: "PreconditionError.Options"
title: "Interface: Options"
sidebar_label: "PreconditionError.Options"
custom_edit_url: null
---

[PreconditionError](../namespaces/PreconditionError).Options

The options for [PreconditionError](../classes/PreconditionError).

**`since`** 1.0.0

## Hierarchy

- `Omit`<[`Options`](UserError.Options), ``"identifier"``\>

  ↳ **`Options`**

## Properties

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

**`default`** precondition.name

#### Defined in

[projects/framework/src/lib/errors/PreconditionError.ts:40](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/PreconditionError.ts#L40)

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

### precondition

• **precondition**: [`Precondition`](../classes/Precondition)<[`PreconditionOptions`](PreconditionOptions)\>

The precondition that caused the error.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/errors/PreconditionError.ts:33](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/PreconditionError.ts#L33)

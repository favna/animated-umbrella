---
id: "MissingExportsError"
title: "Class: MissingExportsError"
sidebar_label: "MissingExportsError"
sidebar_position: 0
custom_edit_url: null
---

Describes a [LoaderErrorType.EmptyModule](../enums/LoaderErrorType#emptymodule) loader error and adds a path for easy identification.

## Hierarchy

- [`LoaderError`](LoaderError)

  ↳ **`MissingExportsError`**

## Constructors

### constructor

• **new MissingExportsError**(`path`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `path` | `string` |

#### Overrides

[LoaderError](LoaderError).[constructor](LoaderError#constructor)

#### Defined in

[projects/pieces/src/lib/errors/MissingExportsError.ts:12](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/errors/MissingExportsError.ts#L12)

## Properties

### message

• **message**: `string`

#### Inherited from

[LoaderError](LoaderError).[message](LoaderError#message)

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:974

___

### path

• `Readonly` **path**: `string`

The path of the module that did not have exports.

#### Defined in

[projects/pieces/src/lib/errors/MissingExportsError.ts:10](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/errors/MissingExportsError.ts#L10)

___

### stack

• `Optional` **stack**: `string`

#### Inherited from

[LoaderError](LoaderError).[stack](LoaderError#stack)

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:975

___

### type

• `Readonly` **type**: [`LoaderErrorType`](../enums/LoaderErrorType)

The type of the error that was thrown.

#### Inherited from

[LoaderError](LoaderError).[type](LoaderError#type)

#### Defined in

[projects/pieces/src/lib/errors/LoaderError.ts:14](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/errors/LoaderError.ts#L14)

___

### prepareStackTrace

▪ `Static` `Optional` **prepareStackTrace**: (`err`: `Error`, `stackTraces`: `CallSite`[]) => `any`

#### Type declaration

▸ (`err`, `stackTraces`): `any`

Optional override for formatting stack traces

**`see`** https://v8.dev/docs/stack-trace-api#customizing-stack-traces

##### Parameters

| Name | Type |
| :------ | :------ |
| `err` | `Error` |
| `stackTraces` | `CallSite`[] |

##### Returns

`any`

#### Inherited from

[LoaderError](LoaderError).[prepareStackTrace](LoaderError#preparestacktrace)

#### Defined in

node_modules/@types/node/globals.d.ts:11

___

### stackTraceLimit

▪ `Static` **stackTraceLimit**: `number`

#### Inherited from

[LoaderError](LoaderError).[stackTraceLimit](LoaderError#stacktracelimit)

#### Defined in

node_modules/@types/node/globals.d.ts:13

## Accessors

### name

• `get` **name**(): `string`

#### Returns

`string`

#### Inherited from

LoaderError.name

#### Defined in

[projects/pieces/src/lib/errors/LoaderError.ts:21](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/errors/LoaderError.ts#L21)

## Methods

### captureStackTrace

▸ `Static` **captureStackTrace**(`targetObject`, `constructorOpt?`): `void`

Create .stack property on a target object

#### Parameters

| Name | Type |
| :------ | :------ |
| `targetObject` | `object` |
| `constructorOpt?` | `Function` |

#### Returns

`void`

#### Inherited from

[LoaderError](LoaderError).[captureStackTrace](LoaderError#capturestacktrace)

#### Defined in

node_modules/@types/node/globals.d.ts:4

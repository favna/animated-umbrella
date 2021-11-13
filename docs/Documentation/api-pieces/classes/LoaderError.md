---
id: "LoaderError"
title: "Class: LoaderError"
sidebar_label: "LoaderError"
sidebar_position: 0
custom_edit_url: null
---

Describes a loader error with a type for easy indentification.

## Hierarchy

- [`Error`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error)

  ↳ **`LoaderError`**

  ↳↳ [`MissingExportsError`](MissingExportsError)

## Constructors

### constructor

• **new LoaderError**(`type`, `message`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `type` | [`LoaderErrorType`](../enums/LoaderErrorType) |
| `message` | `string` |

#### Overrides

Error.constructor

#### Defined in

[projects/pieces/src/lib/errors/LoaderError.ts:16](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/errors/LoaderError.ts#L16)

## Properties

### message

• **message**: `string`

#### Inherited from

Error.message

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:974

___

### stack

• `Optional` **stack**: `string`

#### Inherited from

Error.stack

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:975

___

### type

• `Readonly` **type**: [`LoaderErrorType`](../enums/LoaderErrorType)

The type of the error that was thrown.

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

Error.prepareStackTrace

#### Defined in

node_modules/@types/node/globals.d.ts:11

___

### stackTraceLimit

▪ `Static` **stackTraceLimit**: `number`

#### Inherited from

Error.stackTraceLimit

#### Defined in

node_modules/@types/node/globals.d.ts:13

## Accessors

### name

• `get` **name**(): `string`

#### Returns

`string`

#### Overrides

Error.name

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

Error.captureStackTrace

#### Defined in

node_modules/@types/node/globals.d.ts:4

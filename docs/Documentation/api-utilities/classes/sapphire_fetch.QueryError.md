---
id: "sapphire_fetch.QueryError"
title: "Class: QueryError"
sidebar_label: "QueryError"
custom_edit_url: null
---

[@sapphire/fetch](../modules/sapphire_fetch).QueryError

The QueryError class which is thrown by the `fetch` method

## Hierarchy

- [`Error`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error)

  ↳ **`QueryError`**

## Constructors

### constructor

• **new QueryError**(`url`, `code`, `response`, `body`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` |
| `code` | `number` |
| `response` | `Response` |
| `body` | `string` |

#### Overrides

Error.constructor

#### Defined in

[projects/utilities/packages/fetch/src/lib/QueryError.ts:19](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/QueryError.ts#L19)

## Properties

### #json

• `Private` **#json**: `unknown`

#### Defined in

[projects/utilities/packages/fetch/src/lib/QueryError.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/QueryError.ts#L17)

___

### body

• `Readonly` **body**: `string`

The returned response body as a string

#### Defined in

[projects/utilities/packages/fetch/src/lib/QueryError.ts:13](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/QueryError.ts#L13)

___

### code

• `Readonly` **code**: `number`

The HTTP status code.

#### Defined in

[projects/utilities/packages/fetch/src/lib/QueryError.ts:11](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/QueryError.ts#L11)

___

### message

• **message**: `string`

#### Inherited from

Error.message

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:974

___

### name

• **name**: `string`

#### Inherited from

Error.name

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:973

___

### response

• `Readonly` **response**: `Response`

The original {@link Response} object

#### Defined in

[projects/utilities/packages/fetch/src/lib/QueryError.ts:15](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/QueryError.ts#L15)

___

### stack

• `Optional` **stack**: `string`

#### Inherited from

Error.stack

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:975

___

### url

• `Readonly` **url**: `string`

The requested url.

#### Defined in

[projects/utilities/packages/fetch/src/lib/QueryError.ts:9](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/QueryError.ts#L9)

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

## Methods

### toJSON

▸ **toJSON**(): `any`

#### Returns

`any`

#### Defined in

[projects/utilities/packages/fetch/src/lib/QueryError.ts:28](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/QueryError.ts#L28)

___

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

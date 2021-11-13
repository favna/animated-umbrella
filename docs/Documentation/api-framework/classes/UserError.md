---
id: "UserError"
title: "Class: UserError"
sidebar_label: "UserError"
sidebar_position: 0
custom_edit_url: null
---

The UserError class to be emitted in the pieces.

**`property`** name This will be `'UserError'` and can be used to distinguish the type of error when any error gets thrown

## Hierarchy

- [`Error`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error)

  ↳ **`UserError`**

  ↳↳ [`ArgumentError`](ArgumentError)

  ↳↳ [`PreconditionError`](PreconditionError)

## Constructors

### constructor

• **new UserError**(`options`)

Constructs an UserError.

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | [`Options`](../interfaces/UserError.Options) |

#### Overrides

Error.constructor

#### Defined in

[projects/framework/src/lib/errors/UserError.ts:21](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/UserError.ts#L21)

## Properties

### context

• `Readonly` **context**: `unknown`

User-provided context.

#### Defined in

[projects/framework/src/lib/errors/UserError.ts:14](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/UserError.ts#L14)

___

### identifier

• `Readonly` **identifier**: `string`

An identifier, useful to localize emitted errors.

#### Defined in

[projects/framework/src/lib/errors/UserError.ts:9](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/UserError.ts#L9)

___

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

[projects/framework/src/lib/errors/UserError.ts:28](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/UserError.ts#L28)

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

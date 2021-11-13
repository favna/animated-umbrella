---
id: "ArgumentError"
title: "Class: ArgumentError<T>"
sidebar_label: "ArgumentError"
sidebar_position: 0
custom_edit_url: null
---

Errors thrown by the argument parser

**`since`** 1.0.0

**`property`** name This will be `'ArgumentError'` and can be used to distinguish the type of error when any error gets thrown

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `unknown` |

## Hierarchy

- [`UserError`](UserError)

  ↳ **`ArgumentError`**

## Constructors

### constructor

• **new ArgumentError**<`T`\>(`options`)

Constructs an UserError.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `unknown` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | [`Options`](../interfaces/ArgumentError.Options)<`T`\> |

#### Overrides

[UserError](UserError).[constructor](UserError#constructor)

#### Defined in

[projects/framework/src/lib/errors/ArgumentError.ts:13](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/ArgumentError.ts#L13)

## Properties

### argument

• `Readonly` **argument**: [`IArgument`](../interfaces/IArgument)<`T`\>

#### Defined in

[projects/framework/src/lib/errors/ArgumentError.ts:10](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/ArgumentError.ts#L10)

___

### context

• `Readonly` **context**: `unknown`

User-provided context.

#### Inherited from

[UserError](UserError).[context](UserError#context)

#### Defined in

[projects/framework/src/lib/errors/UserError.ts:14](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/UserError.ts#L14)

___

### identifier

• `Readonly` **identifier**: `string`

An identifier, useful to localize emitted errors.

#### Inherited from

[UserError](UserError).[identifier](UserError#identifier)

#### Defined in

[projects/framework/src/lib/errors/UserError.ts:9](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/UserError.ts#L9)

___

### message

• **message**: `string`

#### Inherited from

[UserError](UserError).[message](UserError#message)

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:974

___

### parameter

• `Readonly` **parameter**: `string`

#### Defined in

[projects/framework/src/lib/errors/ArgumentError.ts:11](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/ArgumentError.ts#L11)

___

### stack

• `Optional` **stack**: `string`

#### Inherited from

[UserError](UserError).[stack](UserError#stack)

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:975

___

### prepareStackTrace

▪ `Static` `Optional` **prepareStackTrace**: (`err`: `Error`, `stackTraces`: `CallSite`[]) => `any`

Optional override for formatting stack traces

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

[UserError](UserError).[prepareStackTrace](UserError#preparestacktrace)

#### Defined in

node_modules/@types/node/globals.d.ts:11

___

### stackTraceLimit

▪ `Static` **stackTraceLimit**: `number`

#### Inherited from

[UserError](UserError).[stackTraceLimit](UserError#stacktracelimit)

#### Defined in

node_modules/@types/node/globals.d.ts:13

## Accessors

### name

• `get` **name**(): `string`

#### Returns

`string`

#### Overrides

UserError.name

#### Defined in

[projects/framework/src/lib/errors/ArgumentError.ts:20](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/errors/ArgumentError.ts#L20)

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

[UserError](UserError).[captureStackTrace](UserError#capturestacktrace)

#### Defined in

node_modules/@types/node/globals.d.ts:4

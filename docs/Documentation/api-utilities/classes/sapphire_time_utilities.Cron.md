---
id: "sapphire_time_utilities.Cron"
title: "Class: Cron"
sidebar_label: "Cron"
custom_edit_url: null
---

[@sapphire/time-utilities](../modules/sapphire_time_utilities).Cron

Handles Cron strings and generates dates based on the cron string provided.

**`see`** https://en.wikipedia.org/wiki/Cron

## Constructors

### constructor

• **new Cron**(`cron`)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `cron` | `string` | The cron pattern to use |

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:21](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L21)

## Properties

### cron

• **cron**: `string`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:10](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L10)

___

### days

• **days**: `number`[]

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:14](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L14)

___

### dows

• **dows**: `number`[]

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:16](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L16)

___

### hours

• **hours**: `number`[]

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:13](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L13)

___

### minutes

• **minutes**: `number`[]

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:12](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L12)

___

### months

• **months**: `number`[]

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:15](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L15)

___

### normalized

• **normalized**: `string`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:11](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L11)

## Methods

### next

▸ **next**(`outset?`, `origin?`): `Date`

Get the next date that matches with the current pattern

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `outset` | `Date` | `undefined` | The Date instance to compare with |
| `origin` | `boolean` | `true` | Whether this next call is origin |

#### Returns

`Date`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:32](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L32)

___

### normalize

▸ `Static` `Private` **normalize**(`cron`): `string`

Normalize the pattern

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `cron` | `string` | The pattern to normalize |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:55](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L55)

___

### parsePart

▸ `Static` `Private` **parsePart**(`cronPart`, `id`): `number`[]

Parse the current part

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `cronPart` | `string` | The part of the pattern to parse |
| `id` | `number` | The id that identifies the current part |

#### Returns

`number`[]

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:101](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L101)

___

### parseString

▸ `Static` `Private` **parseString**(`cron`): `number`[][]

Parse the pattern

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `cron` | `string` | The pattern to parse |

#### Returns

`number`[][]

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Cron.ts:90](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Cron.ts#L90)

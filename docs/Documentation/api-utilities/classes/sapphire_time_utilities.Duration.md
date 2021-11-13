---
id: "sapphire_time_utilities.Duration"
title: "Class: Duration"
sidebar_label: "Duration"
custom_edit_url: null
---

[@sapphire/time-utilities](../modules/sapphire_time_utilities).Duration

Converts duration strings into ms and future dates

## Constructors

### constructor

• **new Duration**(`pattern`)

Create a new Duration instance

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pattern` | `string` | The string to parse |

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Duration.ts:64](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Duration.ts#L64)

## Properties

### offset

• **offset**: `number`

The offset

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Duration.ts:58](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Duration.ts#L58)

___

### kAanRegex

▪ `Static` `Private` `Readonly` **kAanRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

The RegExp used for replacing a/an with 1

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Duration.ts:96](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Duration.ts#L96)

___

### kCommaRegex

▪ `Static` `Private` `Readonly` **kCommaRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

The RegExp used for removing commas

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Duration.ts:91](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Duration.ts#L91)

___

### kPatternRegex

▪ `Static` `Private` `Readonly` **kPatternRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

The RegExp used for the pattern parsing

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Duration.ts:86](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Duration.ts#L86)

## Accessors

### fromNow

• `get` **fromNow**(): `Date`

Get the date from now

#### Returns

`Date`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Duration.ts:71](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Duration.ts#L71)

## Methods

### dateFrom

▸ **dateFrom**(`date`): `Date`

Get the date from

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `date` | `Date` | The Date instance to get the date from |

#### Returns

`Date`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Duration.ts:79](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Duration.ts#L79)

___

### parse

▸ `Static` `Private` **parse**(`pattern`): `number`

Parse the pattern

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pattern` | `string` | The pattern to parse |

#### Returns

`number`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Duration.ts:102](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Duration.ts#L102)

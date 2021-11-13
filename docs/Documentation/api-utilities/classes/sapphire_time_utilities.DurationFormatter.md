---
id: "sapphire_time_utilities.DurationFormatter"
title: "Class: DurationFormatter"
sidebar_label: "DurationFormatter"
custom_edit_url: null
---

[@sapphire/time-utilities](../modules/sapphire_time_utilities).DurationFormatter

Display the duration

**`param`** The duration in milliseconds to parse and display

**`param`** The language assets

## Constructors

### constructor

• **new DurationFormatter**(`units?`)

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `units` | [`DurationFormatAssetsTime`](../interfaces/sapphire_time_utilities.DurationFormatAssetsTime) | `DEFAULT_UNITS` |

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/DurationFormatter.ts:23](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/DurationFormatter.ts#L23)

## Properties

### units

• **units**: [`DurationFormatAssetsTime`](../interfaces/sapphire_time_utilities.DurationFormatAssetsTime) = `DEFAULT_UNITS`

## Methods

### format

▸ **format**(`duration`, `precision?`): `string`

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `duration` | `number` | `undefined` |
| `precision` | `number` | `7` |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/DurationFormatter.ts:25](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/DurationFormatter.ts#L25)

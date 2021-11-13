---
id: "sapphire_time_utilities.Timestamp"
title: "Class: Timestamp"
sidebar_label: "Timestamp"
custom_edit_url: null
---

[@sapphire/time-utilities](../modules/sapphire_time_utilities).Timestamp

Timestamp class, parses the pattern once, displays the desired Date or UNIX timestamp with the selected pattern.

## Constructors

### constructor

• **new Timestamp**(`pattern`)

Starts a new Timestamp and parses the pattern.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pattern` | `string` | The pattern to parse |

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:142](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L142)

## Properties

### pattern

• **pattern**: `string`

The raw pattern

**`since`** 1.0.0

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:130](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L130)

___

### template

• `Private` **template**: [`TimestampTemplateEntry`](../interfaces/sapphire_time_utilities.TimestampTemplateEntry)[]

**`since`** 1.0.0

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:135](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L135)

## Methods

### display

▸ **display**(`time?`): `string`

Display the current date with the current pattern.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `time` | [`TimeResolvable`](../modules/sapphire_time_utilities#timeresolvable) | The time to display |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:152](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L152)

___

### displayUTC

▸ **displayUTC**(`time?`): `string`

Display the current date utc with the current pattern.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `time?` | [`TimeResolvable`](../modules/sapphire_time_utilities#timeresolvable) | The time to display in utc |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:161](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L161)

___

### edit

▸ **edit**(`pattern`): [`Timestamp`](sapphire_time_utilities.Timestamp)

Edits the current pattern.

**`since`** 1.0.0

**`chainable`**

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pattern` | `string` | The new pattern for this instance |

#### Returns

[`Timestamp`](sapphire_time_utilities.Timestamp)

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:171](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L171)

___

### toString

▸ **toString**(): `string`

Defines the toString behavior of Timestamp.

#### Returns

`string`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:180](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L180)

___

### display

▸ `Static` `Private` **display**(`template`, `time`): `string`

Display the current date with the current pattern.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `template` | [`TimestampTemplateEntry`](../interfaces/sapphire_time_utilities.TimestampTemplateEntry)[] | The pattern to parse |
| `time` | `string` \| `number` \| `Date` | The time to display |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:220](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L220)

___

### displayArbitrary

▸ `Static` **displayArbitrary**(`pattern`, `time?`): `string`

Display the current date with the current pattern.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pattern` | `string` | The pattern to parse |
| `time` | [`TimeResolvable`](../modules/sapphire_time_utilities#timeresolvable) | The time to display |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:190](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L190)

___

### displayUTCArbitrary

▸ `Static` **displayUTCArbitrary**(`pattern`, `time?`): `string`

Display the current date utc with the current pattern.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pattern` | `string` | The pattern to parse |
| `time` | [`TimeResolvable`](../modules/sapphire_time_utilities#timeresolvable) | The time to display |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:200](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L200)

___

### parse

▸ `Static` `Private` **parse**(`pattern`): [`TimestampTemplateEntry`](../interfaces/sapphire_time_utilities.TimestampTemplateEntry)[]

Parses the pattern.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pattern` | `string` | The pattern to parse |

#### Returns

[`TimestampTemplateEntry`](../interfaces/sapphire_time_utilities.TimestampTemplateEntry)[]

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:232](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L232)

___

### resolveDate

▸ `Static` `Private` **resolveDate**(`time`): `Date`

Resolves a date.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `time` | [`TimeResolvable`](../modules/sapphire_time_utilities#timeresolvable) | The time to parse |

#### Returns

`Date`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:261](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L261)

___

### utc

▸ `Static` **utc**(`time?`): `Date`

Creates a UTC Date object to work with.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `time` | `string` \| `number` \| `Date` | The date to convert to utc |

#### Returns

`Date`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/Timestamp.ts:209](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/Timestamp.ts#L209)

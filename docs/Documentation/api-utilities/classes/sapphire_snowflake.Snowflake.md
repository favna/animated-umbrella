---
id: "sapphire_snowflake.Snowflake"
title: "Class: Snowflake"
sidebar_label: "Snowflake"
custom_edit_url: null
---

[@sapphire/snowflake](../modules/sapphire_snowflake).Snowflake

A class for parsing snowflake ids

## Hierarchy

- **`Snowflake`**

  ↳ [`DiscordSnowflake`](sapphire_snowflake.DiscordSnowflake)

  ↳ [`TwitterSnowflake`](sapphire_snowflake.TwitterSnowflake)

## Constructors

### constructor

• **new Snowflake**(`epoch`)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `epoch` | `number` \| `bigint` \| `Date` | the epoch to use |

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:28](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L28)

## Properties

### #epoch

• `Private` **#epoch**: `bigint`

Internal reference of the epoch passed in the constructor

**`internal`**

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L17)

___

### #increment

• `Private` **#increment**: `bigint`

Internal incrementor for generating snowflakes

**`internal`**

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:11](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L11)

___

### decode

• **decode**: (`id`: `string` \| `bigint`) => [`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

#### Type declaration

▸ (`id`): [`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

Deconstructs a snowflake given a snowflake ID

**`example`**
```typescript
const epoch = new Date('2000-01-01T00:00:00.000Z');
const snowflake = new Snowflake(epoch).deconstruct('3971046231244935168');
```

##### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` \| `bigint` | the snowflake to deconstruct |

##### Returns

[`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

a deconstructed snowflake

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:23](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L23)

## Methods

### deconstruct

▸ **deconstruct**(`id`): [`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

Deconstructs a snowflake given a snowflake ID

**`example`**
```typescript
const epoch = new Date('2000-01-01T00:00:00.000Z');
const snowflake = new Snowflake(epoch).deconstruct('3971046231244935168');
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` \| `bigint` | the snowflake to deconstruct |

#### Returns

[`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

a deconstructed snowflake

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:79](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L79)

___

### generate

▸ **generate**(`options?`): `bigint`

Generates a snowflake given an epoch and optionally a timestamp

**`example`**
```typescript
const epoch = new Date('2000-01-01T00:00:00.000Z');
const snowflake = new Snowflake(epoch).generate();
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`SnowflakeGenerateOptions`](../interfaces/sapphire_snowflake.SnowflakeGenerateOptions) | options to pass into the generator, see [SnowflakeGenerateOptions](../interfaces/sapphire_snowflake.SnowflakeGenerateOptions)  **note** when increment is not provided it defaults to the private increment of the instance |

#### Returns

`bigint`

A unique snowflake

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:44](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L44)

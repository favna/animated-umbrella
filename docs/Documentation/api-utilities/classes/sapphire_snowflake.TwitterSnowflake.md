---
id: "sapphire_snowflake.TwitterSnowflake"
title: "Class: TwitterSnowflake"
sidebar_label: "TwitterSnowflake"
custom_edit_url: null
---

[@sapphire/snowflake](../modules/sapphire_snowflake).TwitterSnowflake

A class for parsing snowflake ids using Twitter's snowflake epoch

Which is 2006-03-21 at 20:50:14.000 UTC+0, the time and date of the first tweet ever made [https://twitter.com/jack/status/20](https://twitter.com/jack/status/20)

## Hierarchy

- [`Snowflake`](sapphire_snowflake.Snowflake)

  ↳ **`TwitterSnowflake`**

## Constructors

### constructor

• **new TwitterSnowflake**()

#### Overrides

[Snowflake](sapphire_snowflake.Snowflake).[constructor](sapphire_snowflake.Snowflake#constructor)

#### Defined in

[projects/utilities/packages/snowflake/src/lib/TwitterSnowflake.ts:9](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/TwitterSnowflake.ts#L9)

## Properties

### #epoch

• `Private` **#epoch**: `bigint`

Internal reference of the epoch passed in the constructor

**`internal`**

#### Inherited from

[Snowflake](sapphire_snowflake.Snowflake).[#epoch](sapphire_snowflake.Snowflake##epoch)

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L17)

___

### #increment

• `Private` **#increment**: `bigint`

Internal incrementor for generating snowflakes

**`internal`**

#### Inherited from

[Snowflake](sapphire_snowflake.Snowflake).[#increment](sapphire_snowflake.Snowflake##increment)

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

#### Inherited from

[Snowflake](sapphire_snowflake.Snowflake).[decode](sapphire_snowflake.Snowflake#decode)

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:23](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L23)

___

### Epoch

▪ `Static` `Readonly` **Epoch**: `1142974214000n`

Twitter epoch (`2006-03-21T20:50:14.000Z`)

**`see`** [https://twitter.com/jack/status/20](https://twitter.com/jack/status/20), first tweet ever made

#### Defined in

[projects/utilities/packages/snowflake/src/lib/TwitterSnowflake.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/TwitterSnowflake.ts#L17)

___

### decode

▪ `Static` **decode**: (`id`: `string` \| `bigint`) => [`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake) = `TwitterSnowflake.deconstruct`

#### Type declaration

▸ (`id`): [`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

Deconstructs a snowflake given a snowflake ID

**`example`**
```typescript
const snowflake = TwitterSnowflake.deconstruct('3971046231244935168');
```

##### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` \| `bigint` | the snowflake to deconstruct |

##### Returns

[`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

a deconstructed snowflake

#### Defined in

[projects/utilities/packages/snowflake/src/lib/TwitterSnowflake.ts:29](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/TwitterSnowflake.ts#L29)

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

#### Inherited from

[Snowflake](sapphire_snowflake.Snowflake).[deconstruct](sapphire_snowflake.Snowflake#deconstruct)

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

#### Inherited from

[Snowflake](sapphire_snowflake.Snowflake).[generate](sapphire_snowflake.Snowflake#generate)

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:44](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L44)

___

### deconstruct

▸ `Static` **deconstruct**(`id`): [`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

Deconstructs a snowflake given a snowflake ID

**`example`**
```typescript
const snowflake = TwitterSnowflake.deconstruct('3971046231244935168');
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` \| `bigint` | the snowflake to deconstruct |

#### Returns

[`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

a deconstructed snowflake

#### Defined in

[projects/utilities/packages/snowflake/src/lib/TwitterSnowflake.ts:40](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/TwitterSnowflake.ts#L40)

___

### generate

▸ `Static` **generate**(`options?`): `bigint`

Generates a snowflake given an epoch and optionally a timestamp

**`example`**
```typescript
const snowflake = TwitterSnowflake.generate();
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`SnowflakeGenerateOptions`](../interfaces/sapphire_snowflake.SnowflakeGenerateOptions) | options to pass into the generator, see [SnowflakeGenerateOptions](../interfaces/sapphire_snowflake.SnowflakeGenerateOptions)  **note** when increment is not provided it defaults to `0n` |

#### Returns

`bigint`

A unique snowflake

#### Defined in

[projects/utilities/packages/snowflake/src/lib/TwitterSnowflake.ts:55](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/TwitterSnowflake.ts#L55)

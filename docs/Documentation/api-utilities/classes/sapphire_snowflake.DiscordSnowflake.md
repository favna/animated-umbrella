---
id: "sapphire_snowflake.DiscordSnowflake"
title: "Class: DiscordSnowflake"
sidebar_label: "DiscordSnowflake"
custom_edit_url: null
---

[@sapphire/snowflake](../modules/sapphire_snowflake).DiscordSnowflake

A class for parsing snowflake ids using Discord's snowflake epoch

Which is 2015-01-01 at 00:00:00.000 UTC+0, [https://discord.com/developers/docs/reference#snowflakes](https://discord.com/developers/docs/reference#snowflakes)

## Hierarchy

- [`Snowflake`](sapphire_snowflake.Snowflake)

  ↳ **`DiscordSnowflake`**

## Constructors

### constructor

• **new DiscordSnowflake**()

#### Overrides

[Snowflake](sapphire_snowflake.Snowflake).[constructor](sapphire_snowflake.Snowflake#constructor)

#### Defined in

[projects/utilities/packages/snowflake/src/lib/DiscordSnowflake.ts:9](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/DiscordSnowflake.ts#L9)

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

Alias for [deconstruct](sapphire_snowflake.DiscordSnowflake#deconstruct)

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

▪ `Static` `Readonly` **Epoch**: `1420070400000n`

Discord epoch (`2015-01-01T00:00:00.000Z`)

**`see`** [https://discord.com/developers/docs/reference#snowflakes](https://discord.com/developers/docs/reference#snowflakes)

#### Defined in

[projects/utilities/packages/snowflake/src/lib/DiscordSnowflake.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/DiscordSnowflake.ts#L17)

___

### decode

▪ `Static` **decode**: (`id`: `string` \| `bigint`) => [`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake) = `DiscordSnowflake.deconstruct`

#### Type declaration

▸ (`id`): [`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

Deconstructs a snowflake given a snowflake ID

**`example`**
```typescript
const snowflake = DiscordSnowflake.deconstruct('3971046231244935168');
```

##### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` \| `bigint` | the snowflake to deconstruct |

##### Returns

[`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

a deconstructed snowflake

#### Defined in

[projects/utilities/packages/snowflake/src/lib/DiscordSnowflake.ts:29](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/DiscordSnowflake.ts#L29)

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
const snowflake = DiscordSnowflake.deconstruct('3971046231244935168');
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` \| `bigint` | the snowflake to deconstruct |

#### Returns

[`DeconstructedSnowflake`](../interfaces/sapphire_snowflake.DeconstructedSnowflake)

a deconstructed snowflake

#### Defined in

[projects/utilities/packages/snowflake/src/lib/DiscordSnowflake.ts:40](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/DiscordSnowflake.ts#L40)

___

### generate

▸ `Static` **generate**(`options?`): `bigint`

Generates a snowflake given an epoch and optionally a timestamp

**`example`**
```typescript
const snowflake = DiscordSnowflake.generate();
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`SnowflakeGenerateOptions`](../interfaces/sapphire_snowflake.SnowflakeGenerateOptions) | [SnowflakeGenerateOptions](../interfaces/sapphire_snowflake.SnowflakeGenerateOptions) to pass into the generator  **note** when increment is not provided it defaults to `0n` |

#### Returns

`bigint`

A unique snowflake

#### Defined in

[projects/utilities/packages/snowflake/src/lib/DiscordSnowflake.ts:55](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/DiscordSnowflake.ts#L55)

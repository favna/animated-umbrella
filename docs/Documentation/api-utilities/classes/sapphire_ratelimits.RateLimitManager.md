---
id: "sapphire_ratelimits.RateLimitManager"
title: "Class: RateLimitManager<K>"
sidebar_label: "RateLimitManager"
custom_edit_url: null
---

[@sapphire/ratelimits](../modules/sapphire_ratelimits).RateLimitManager

## Type parameters

| Name | Type |
| :------ | :------ |
| `K` | `string` |

## Hierarchy

- [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<`K`, [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>\>

  ↳ **`RateLimitManager`**

## Constructors

### constructor

• **new RateLimitManager**<`K`\>(`time`, `limit?`)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | `string` |

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `time` | `number` | `undefined` | The amount of milliseconds for the ratelimits from this manager to expire. |
| `limit` | `number` | `1` | The amount of times a [RateLimit](sapphire_ratelimits.RateLimit) can drip before it's limited. |

#### Overrides

Map&lt;K, RateLimit&lt;K\&gt;\&gt;.constructor

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimitManager.ts:24](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimitManager.ts#L24)

## Properties

### [toStringTag]

• `Readonly` **[toStringTag]**: `string`

#### Inherited from

Map.\_\_@toStringTag@548780

#### Defined in

node_modules/typescript/lib/lib.es2015.symbol.wellknown.d.ts:135

___

### limit

• `Readonly` **limit**: `number`

The amount of times a [RateLimit](sapphire_ratelimits.RateLimit) can drip before it's limited.

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimitManager.ts:13](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimitManager.ts#L13)

___

### size

• `Readonly` **size**: `number`

#### Inherited from

Map.size

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:28

___

### sweepInterval

• `Private` **sweepInterval**: ``null`` \| `Timer`

The interval to sweep expired [ratelimits](sapphire_ratelimits.RateLimit).

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimitManager.ts:18](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimitManager.ts#L18)

___

### time

• `Readonly` **time**: `number`

The amount of milliseconds for the [ratelimits](sapphire_ratelimits.RateLimit) from this manager to expire.

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimitManager.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimitManager.ts#L8)

___

### [species]

▪ `Static` `Readonly` **[species]**: `MapConstructor`

#### Inherited from

Map.\_\_@species@549343

#### Defined in

node_modules/typescript/lib/lib.es2015.symbol.wellknown.d.ts:317

___

### sweepIntervalDuration

▪ `Static` **sweepIntervalDuration**: `number` = `30_000`

The delay in milliseconds for [RateLimitManager.sweepInterval](sapphire_ratelimits.RateLimitManager#sweepinterval).

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimitManager.ts:76](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimitManager.ts#L76)

## Methods

### [iterator]

▸ **[iterator]**(): `IterableIterator`<[`K`, [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>]\>

Returns an iterable of entries in the map.

#### Returns

`IterableIterator`<[`K`, [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>]\>

#### Inherited from

Map.\_\_@iterator@548837

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:121

___

### acquire

▸ **acquire**(`id`): [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

Gets a [RateLimit](sapphire_ratelimits.RateLimit) from this manager or creates it if it does not exist.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `K` | The id for the [RateLimit](sapphire_ratelimits.RateLimit) |

#### Returns

[`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimitManager.ts:35](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimitManager.ts#L35)

___

### clear

▸ **clear**(): `void`

#### Returns

`void`

#### Inherited from

Map.clear

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:22

___

### create

▸ **create**(`id`): [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

Creates a [RateLimit](sapphire_ratelimits.RateLimit) for this manager.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `K` | The id the [RateLimit](sapphire_ratelimits.RateLimit) belongs to |

#### Returns

[`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimitManager.ts:43](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimitManager.ts#L43)

___

### delete

▸ **delete**(`key`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `K` |

#### Returns

`boolean`

#### Inherited from

Map.delete

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:23

___

### entries

▸ **entries**(): `IterableIterator`<[`K`, [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>]\>

Returns an iterable of key, value pairs for every entry in the map.

#### Returns

`IterableIterator`<[`K`, [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>]\>

#### Inherited from

Map.entries

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:126

___

### forEach

▸ **forEach**(`callbackfn`, `thisArg?`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `callbackfn` | (`value`: [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>, `key`: `K`, `map`: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<`K`, [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>\>) => `void` |
| `thisArg?` | `any` |

#### Returns

`void`

#### Inherited from

Map.forEach

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:24

___

### get

▸ **get**(`key`): `undefined` \| [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `K` |

#### Returns

`undefined` \| [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

#### Inherited from

Map.get

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:25

___

### has

▸ **has**(`key`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `K` |

#### Returns

`boolean`

#### Inherited from

Map.has

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:26

___

### keys

▸ **keys**(): `IterableIterator`<`K`\>

Returns an iterable of keys in the map

#### Returns

`IterableIterator`<`K`\>

#### Inherited from

Map.keys

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:131

___

### set

▸ **set**(`id`, `value`): [`RateLimitManager`](sapphire_ratelimits.RateLimitManager)<`K`\>

Wraps Collection's set method to set interval to sweep inactive [RateLimit](sapphire_ratelimits.RateLimit)s.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `K` | The id the [RateLimit](sapphire_ratelimits.RateLimit) belongs to |
| `value` | [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\> | The [RateLimit](sapphire_ratelimits.RateLimit) to set |

#### Returns

[`RateLimitManager`](sapphire_ratelimits.RateLimitManager)<`K`\>

#### Overrides

Map.set

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimitManager.ts:54](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimitManager.ts#L54)

___

### sweep

▸ **sweep**(): `void`

Wraps Collection's sweep method to clear the interval when this manager is empty.

#### Returns

`void`

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimitManager.ts:62](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimitManager.ts#L62)

___

### values

▸ **values**(): `IterableIterator`<[`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>\>

Returns an iterable of values in the map

#### Returns

`IterableIterator`<[`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>\>

#### Inherited from

Map.values

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:136

---
id: "sapphire_ratelimits.RateLimit"
title: "Class: RateLimit<K>"
sidebar_label: "RateLimit"
custom_edit_url: null
---

[@sapphire/ratelimits](../modules/sapphire_ratelimits).RateLimit

## Type parameters

| Name |
| :------ |
| `K` |

## Constructors

### constructor

• **new RateLimit**<`K`\>(`manager`)

#### Type parameters

| Name |
| :------ |
| `K` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `manager` | [`RateLimitManager`](sapphire_ratelimits.RateLimitManager)<`K`\> | The manager for this entry. |

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:22](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L22)

## Properties

### expires

• **expires**: `number`

The timestamp that represents when this entry will reset back to a available state.

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:12](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L12)

___

### manager

• `Private` **manager**: [`RateLimitManager`](sapphire_ratelimits.RateLimitManager)<`K`\>

The [RateLimitManager](sapphire_ratelimits.RateLimitManager) this entry is for.

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L17)

___

### remaining

• **remaining**: `number`

The remaining amount of times this entry can be dripped before the bucket is empty.

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L7)

## Accessors

### expired

• `get` **expired**(): `boolean`

Whether this entry is expired or not, allowing the bucket to be reset.

#### Returns

`boolean`

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:30](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L30)

___

### limited

• `get` **limited**(): `boolean`

Whether this entry is limited or not.

#### Returns

`boolean`

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:37](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L37)

___

### remainingTime

• `get` **remainingTime**(): `number`

The remaining time in milliseconds before resetting.

#### Returns

`number`

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:44](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L44)

## Methods

### consume

▸ **consume**(): [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

Consumes [RateLimit.remaining](sapphire_ratelimits.RateLimit#remaining) by one if it's not limited, calling [RateLimit.reset](sapphire_ratelimits.RateLimit#reset) first if [RateLimit.expired](sapphire_ratelimits.RateLimit#expired) is true.

#### Returns

[`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:51](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L51)

___

### reset

▸ **reset**(): [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

Resets the entry back to it's full state.

#### Returns

[`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:62](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L62)

___

### resetRemaining

▸ **resetRemaining**(): [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

Resets the entry's [RateLimit.remaining](sapphire_ratelimits.RateLimit#remaining) uses back to full state.

#### Returns

[`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:69](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L69)

___

### resetTime

▸ **resetTime**(): [`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

Resets the entry's [RateLimit.expires](sapphire_ratelimits.RateLimit#expires) to the current time plus [RateLimitManager.time](sapphire_ratelimits.RateLimitManager#time).

#### Returns

[`RateLimit`](sapphire_ratelimits.RateLimit)<`K`\>

#### Defined in

[projects/utilities/packages/ratelimits/src/lib/RateLimit.ts:77](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/ratelimits/src/lib/RateLimit.ts#L77)

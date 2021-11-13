---
id: "sapphire_time_utilities.TimerManager"
title: "Class: TimerManager"
sidebar_label: "TimerManager"
custom_edit_url: null
---

[@sapphire/time-utilities](../modules/sapphire_time_utilities).TimerManager

Manages timers so that this application can be cleanly exited

## Hierarchy

- `any`

  ↳ **`TimerManager`**

## Constructors

### constructor

• **new TimerManager**()

#### Inherited from

null.constructor

## Properties

### storedIntervals

▪ `Static` `Private` **storedIntervals**: [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)<`Timeout`\>

A set of intervals to clear on destroy

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/TimerManager.ts:13](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/TimerManager.ts#L13)

___

### storedTimeouts

▪ `Static` `Private` **storedTimeouts**: [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)<`Timeout`\>

A set of timeouts to clear on destroy

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/TimerManager.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/TimerManager.ts#L8)

## Methods

### clearInterval

▸ `Static` **clearInterval**(`interval`): `void`

Clears an internal created through this class

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `interval` | `Timeout` | The interval to clear |

#### Returns

`void`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/TimerManager.ts:55](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/TimerManager.ts#L55)

___

### clearTimeout

▸ `Static` **clearTimeout**(`timeout`): `void`

Clears a timeout created through this class

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `timeout` | `Timeout` | The timeout to clear |

#### Returns

`void`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/TimerManager.ts:34](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/TimerManager.ts#L34)

___

### destroy

▸ `Static` **destroy**(): `void`

Clears running timeouts and intervals created through this class so NodeJS can gracefully exit

#### Returns

`void`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/TimerManager.ts:63](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/TimerManager.ts#L63)

___

### setInterval

▸ `Static` **setInterval**<`A`\>(`fn`, `delay`, ...`args`): `Timeout`

Creates an interval gets cleared when destroyed

#### Type parameters

| Name | Type |
| :------ | :------ |
| `A` | `unknown` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (...`args`: `A`[]) => `void` | callback function |
| `delay` | `number` | amount of time before running the callback |
| `...args` | `A`[] | additional arguments to pass back to the callback |

#### Returns

`Timeout`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/TimerManager.ts:45](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/TimerManager.ts#L45)

___

### setTimeout

▸ `Static` **setTimeout**<`A`\>(`fn`, `delay`, ...`args`): `Timeout`

Creates a timeout gets cleared when destroyed

#### Type parameters

| Name | Type |
| :------ | :------ |
| `A` | `unknown` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (...`args`: `A`[]) => `void` | callback function |
| `delay` | `number` | amount of time before running the callback |
| `...args` | `A`[] | additional arguments to pass back to the callback |

#### Returns

`Timeout`

#### Defined in

[projects/utilities/packages/time-utilities/src/lib/TimerManager.ts:21](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/time-utilities/src/lib/TimerManager.ts#L21)

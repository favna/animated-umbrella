---
id: "sapphire_stopwatch.Stopwatch"
title: "Class: Stopwatch"
sidebar_label: "Stopwatch"
custom_edit_url: null
---

[@sapphire/stopwatch](../modules/sapphire_stopwatch).Stopwatch

Stopwatch class, uses native node to replicate/extend performance-now dependency.

## Constructors

### constructor

• **new Stopwatch**(`digits?`)

Starts a new stopwatch

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `digits` | `number` | `2` |

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:27](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L27)

## Properties

### #end

• `Private` **#end**: ``null`` \| `number`

The end time of this stopwatch

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:22](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L22)

___

### #start

• `Private` **#start**: `number`

The start time of this stopwatch

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:16](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L16)

___

### digits

• **digits**: `number`

The number of digits to appear after the decimal point when returning the friendly duration.

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:10](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L10)

## Accessors

### duration

• `get` **duration**(): `number`

The duration of this stopwatch since start or start to end if this stopwatch has stopped.

#### Returns

`number`

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:36](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L36)

___

### running

• `get` **running**(): `boolean`

If the stopwatch is running or not.

#### Returns

`boolean`

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:43](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L43)

## Methods

### reset

▸ **reset**(): [`Stopwatch`](sapphire_stopwatch.Stopwatch)

Resets the Stopwatch to 0 duration (Returns a stopped state)

#### Returns

[`Stopwatch`](sapphire_stopwatch.Stopwatch)

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:59](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L59)

___

### restart

▸ **restart**(): [`Stopwatch`](sapphire_stopwatch.Stopwatch)

Restarts the stopwatch (Returns a running state)

#### Returns

[`Stopwatch`](sapphire_stopwatch.Stopwatch)

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:50](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L50)

___

### start

▸ **start**(): [`Stopwatch`](sapphire_stopwatch.Stopwatch)

Starts the Stopwatch

#### Returns

[`Stopwatch`](sapphire_stopwatch.Stopwatch)

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:68](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L68)

___

### stop

▸ **stop**(): [`Stopwatch`](sapphire_stopwatch.Stopwatch)

Stops the Stopwatch, freezing the duration

#### Returns

[`Stopwatch`](sapphire_stopwatch.Stopwatch)

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:80](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L80)

___

### toString

▸ **toString**(): `string`

Defines toString behavior

#### Returns

`string`

#### Defined in

[projects/utilities/packages/stopwatch/src/index.ts:88](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/stopwatch/src/index.ts#L88)

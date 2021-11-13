---
id: "sapphire_event_iterator.EventIterator"
title: "Class: EventIterator<V>"
sidebar_label: "EventIterator"
custom_edit_url: null
---

[@sapphire/event-iterator](../modules/sapphire_event_iterator).EventIterator

An EventIterator, used for asynchronously iterating over received values.

## Type parameters

| Name | Type |
| :------ | :------ |
| `V` | extends `unknown`[] |

## Implements

- `AsyncIterableIterator`<`V`\>

## Constructors

### constructor

• **new EventIterator**<`V`\>(`emitter`, `event`, `options?`)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V` | extends `unknown`[] |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `emitter` | `EventEmitter` | The event emitter to listen to. |
| `event` | `string` | The event we're listening for to receives values from. |
| `options` | [`EventIteratorOptions`](../interfaces/sapphire_event_iterator.EventIteratorOptions)<`V`\> | Any extra options. |

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:89](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L89)

## Properties

### #ended

• `Private` **#ended**: `boolean` = `false`

Whether or not the EventIterator has ended.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:51](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L51)

___

### #idle

• `Private` `Optional` **#idle**: `number`

The amount of idle time in ms before moving on.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:56](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L56)

___

### #idleTimer

• `Private` **#idleTimer**: ``null`` \| `Timer` = `null`

The timer to track when this will idle out.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:76](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L76)

___

### #limit

• `Private` **#limit**: `number`

The limit before ending the EventIterator.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:71](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L71)

___

### #passed

• `Private` **#passed**: `number` = `0`

The amount of events that have passed the filter.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:66](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L66)

___

### #push

• `Private` **#push**: (...`value`: `V`) => `void`

#### Type declaration

▸ (...`value`): `void`

The push handler with context bound to the instance.

##### Parameters

| Name | Type |
| :------ | :------ |
| `...value` | `V` |

##### Returns

`void`

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:81](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L81)

___

### #queue

• `Private` **#queue**: `V`[] = `[]`

The queue of received values.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:61](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L61)

___

### emitter

• `Readonly` **emitter**: `EventEmitter`

The emitter to listen to.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:36](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L36)

___

### event

• `Readonly` **event**: `string`

The event the event iterator is listening for to receive values from.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:41](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L41)

___

### filter

• **filter**: [`EventIteratorFilter`](../modules/sapphire_event_iterator#eventiteratorfilter)<`V`\>

The filter used to filter out values.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:46](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L46)

## Accessors

### ended

• `get` **ended**(): `boolean`

Whether or not the EventIterator has ended.

#### Returns

`boolean`

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:111](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L111)

## Methods

### [asyncIterator]

▸ **[asyncIterator]**(): `AsyncIterableIterator`<`V`\>

The symbol allowing EventIterators to be used in for-await-of loops.

#### Returns

`AsyncIterableIterator`<`V`\>

#### Implementation of

AsyncIterableIterator.\_\_@asyncIterator@382229

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:189](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L189)

___

### end

▸ **end**(): `void`

Ends the EventIterator.

#### Returns

`void`

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:118](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L118)

___

### next

▸ **next**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`IteratorResult`<`V`, `any`\>\>

The next value that's received from the EventEmitter.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`IteratorResult`<`V`, `any`\>\>

#### Implementation of

AsyncIterableIterator.next

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:132](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L132)

___

### push

▸ `Protected` **push**(...`value`): `void`

Pushes a value into the queue.

#### Parameters

| Name | Type |
| :------ | :------ |
| `...value` | `V` |

#### Returns

`void`

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:196](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L196)

___

### return

▸ **return**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`IteratorResult`<`V`, `any`\>\>

Handles what happens when you break or return from a loop.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`IteratorResult`<`V`, `any`\>\>

#### Implementation of

AsyncIterableIterator.return

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:173](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L173)

___

### throw

▸ **throw**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`IteratorResult`<`V`, `any`\>\>

Handles what happens when you encounter an error in a loop.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`IteratorResult`<`V`, `any`\>\>

#### Implementation of

AsyncIterableIterator.throw

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:181](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L181)

---
id: "sapphire_async_queue.AsyncQueue"
title: "Class: AsyncQueue"
sidebar_label: "AsyncQueue"
custom_edit_url: null
---

[@sapphire/async-queue](../modules/sapphire_async_queue).AsyncQueue

The AsyncQueue class used to sequentialize burst requests

## Constructors

### constructor

• **new AsyncQueue**()

## Properties

### promises

• `Private` **promises**: `InternalAsyncQueueDeferredPromise`[] = `[]`

The promises array

#### Defined in

[projects/utilities/packages/async-queue/src/lib/AsyncQueue.ts:15](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/async-queue/src/lib/AsyncQueue.ts#L15)

## Accessors

### remaining

• `get` **remaining**(): `number`

The remaining amount of queued promises

#### Returns

`number`

#### Defined in

[projects/utilities/packages/async-queue/src/lib/AsyncQueue.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/async-queue/src/lib/AsyncQueue.ts#L8)

## Methods

### shift

▸ **shift**(): `void`

Frees the queue's lock for the next item to process

#### Returns

`void`

#### Defined in

[projects/utilities/packages/async-queue/src/lib/AsyncQueue.ts:56](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/async-queue/src/lib/AsyncQueue.ts#L56)

___

### wait

▸ **wait**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Waits for last promise and queues a new one

**`example`**
```typescript
const queue = new AsyncQueue();
async function request(url, options) {
    await queue.wait();
    try {
        const result = await fetch(url, options);
        // Do some operations with 'result'
    } finally {
        // Remove first entry from the queue and resolve for the next entry
        queue.shift();
    }
}

request(someUrl1, someOptions1); // Will call fetch() immediately
request(someUrl2, someOptions2); // Will call fetch() after the first finished
request(someUrl3, someOptions3); // Will call fetch() after the second finished
```

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Defined in

[projects/utilities/packages/async-queue/src/lib/AsyncQueue.ts:38](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/async-queue/src/lib/AsyncQueue.ts#L38)

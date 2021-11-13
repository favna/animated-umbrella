---
id: "Listener"
title: "Class: Listener<E, O>"
sidebar_label: "Listener"
sidebar_position: 0
custom_edit_url: null
---

The base event class. This class is abstract and is to be extended by subclasses, which should implement the methods. In
Sapphire's workflow, listeners are called when the emitter they listen on emits a new message with the same event name.

**`example`**
```typescript
// TypeScript:
import { Events, Listener, PieceContext } from '@sapphire/framework';

// Define a class extending `Listener`, then export it.
// NOTE: You can use `export default` or `export =` too.
export class CoreListener extends Listener<typeof Events.Ready> {
  public constructor(context: PieceContext) {
    super(context, { event: Events.Ready, once: true });
  }

  public run() {
    this.container.client.id ??= this.container.client.user?.id ?? null;
  }
}
```

**`example`**
```javascript
// JavaScript:
const { Events, Listener } = require('@sapphire/framework');

// Define a class extending `Listener`, then export it.
module.exports = class CoreListener extends Listener {
  constructor(context) {
    super(context, { event: Events.Ready, once: true });
  }

  run() {
    this.container.client.id ??= this.container.client.user?.id ?? null;
  }
}
```

## Type parameters

| Name | Type |
| :------ | :------ |
| `E` | extends keyof `ClientEvents` \| `symbol```""`` |
| `O` | extends [`ListenerOptions`](../interfaces/ListenerOptions)[`ListenerOptions`](../interfaces/ListenerOptions) |

## Hierarchy

- [`Piece`](Piece)<`O`\>

  ↳ **`Listener`**

## Constructors

### constructor

• **new Listener**<`E`, `O`\>(`context`, `options?`)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `E` | extends `symbol` \| keyof `ClientEvents```""`` |
| `O` | extends [`ListenerOptions`](../interfaces/ListenerOptions)[`ListenerOptions`](../interfaces/ListenerOptions) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `context` | [`PieceContext`](../interfaces/PieceContext) |
| `options` | [`ListenerOptions`](../interfaces/ListenerOptions) |

#### Overrides

[Piece](Piece).[constructor](Piece#constructor)

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:67](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L67)

## Properties

### \_listener

• `Private` **\_listener**: ``null`` \| (...`args`: `any`[]) => `void`

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:65](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L65)

___

### emitter

• `Readonly` **emitter**: ``null`` \| `EventEmitter`

The emitter, if any.

**`since`** 2.0.0

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:51](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L51)

___

### enabled

• **enabled**: `boolean`

Whether or not the piece is enabled.

#### Inherited from

[Piece](Piece).[enabled](Piece#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:432

___

### event

• `Readonly` **event**: `string`

The name of the event the listener listens to.

**`since`** 2.0.0

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:57](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L57)

___

### location

• `Readonly` **location**: `PieceLocation`

The location metadata for the piece's file.

#### Inherited from

[Piece](Piece).[location](Piece#location)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:424

___

### name

• `Readonly` **name**: `string`

The name of the piece.

#### Inherited from

[Piece](Piece).[name](Piece#name)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:428

___

### once

• `Readonly` **once**: `boolean`

Whether or not the listener will be unloaded after the first run.

**`since`** 2.0.0

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:63](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L63)

___

### options

• `Readonly` **options**: `O`

The raw options passed to this [Piece](Piece)

#### Inherited from

[Piece](Piece).[options](Piece#options)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:436

___

### store

• `Readonly` **store**: [`Store`](Store)<[`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions)\>\>

The store that contains the piece.

#### Inherited from

[Piece](Piece).[store](Piece#store)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:420

## Accessors

### container

• `get` **container**(): `Container`

A reference to the {@link Container} object for ease of use.

**`see`** container

#### Returns

`Container`

#### Inherited from

Piece.container

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:442

## Methods

### \_run

▸ `Private` **_run**(...`args`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `...args` | `unknown`[] |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:122](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L122)

___

### \_runOnce

▸ `Private` **_runOnce**(...`args`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `...args` | `unknown`[] |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:129](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L129)

___

### onLoad

▸ **onLoad**(): `unknown`

Per-piece listener that is called when the piece is loaded into the store.
Useful to set-up asynchronous initialization tasks.

#### Returns

`unknown`

#### Overrides

[Piece](Piece).[onLoad](Piece#onload)

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:86](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L86)

___

### onUnload

▸ **onUnload**(): `unknown`

Per-piece listener that is called when the piece is unloaded from the store.
Useful to set-up clean-up tasks.

#### Returns

`unknown`

#### Overrides

[Piece](Piece).[onUnload](Piece#onunload)

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:99](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L99)

___

### reload

▸ **reload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Reloads the piece by loading the same path in the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Piece](Piece).[reload](Piece#reload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:460

___

### run

▸ `Abstract` **run**(...`args`): `unknown`

#### Parameters

| Name | Type |
| :------ | :------ |
| `...args` | `E` extends keyof `ClientEvents` ? `ClientEvents`[`E`] : `unknown`[] |

#### Returns

`unknown`

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:84](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L84)

___

### toJSON

▸ **toJSON**(): [`ListenerJSON`](../interfaces/ListenerJSON)

Defines the `JSON.stringify` behavior of this piece.

#### Returns

[`ListenerJSON`](../interfaces/ListenerJSON)

#### Overrides

[Piece](Piece).[toJSON](Piece#tojson)

#### Defined in

[projects/framework/src/lib/structures/Listener.ts:114](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Listener.ts#L114)

___

### unload

▸ **unload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Unloads and disables the piece.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Piece](Piece).[unload](Piece#unload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:456

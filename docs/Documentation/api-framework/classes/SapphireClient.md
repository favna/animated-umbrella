---
id: "SapphireClient"
title: "Class: SapphireClient<Ready>"
sidebar_label: "SapphireClient"
sidebar_position: 0
custom_edit_url: null
---

The base {@link Client} extension that makes Sapphire work. When building a Discord bot with the framework, the developer
must either use this class, or extend it.

Sapphire also automatically detects the folders to scan for pieces, please read [StoreRegistry.registerPath](StoreRegistry#registerpath)
for reference. This method is called at the start of the [SapphireClient.login](SapphireClient#login) method.

**`see`** [SapphireClientOptions](../interfaces/SapphireClientOptions) for all options available to the Sapphire Client. You can also provide all of discord.js' [ClientOptions](https://discord.js.org/#/docs/main/stable/typedef/ClientOptions)

**`since`** 1.0.0

**`example`**
```typescript
const client = new SapphireClient({
  presence: {
    activity: {
      name: 'for commands!',
      type: 'LISTENING'
    }
  }
});

client.login(process.env.DISCORD_TOKEN)
  .catch(console.error);
```

**`example`**
```typescript
// Automatically scan from a specific directory, e.g. the main
// file is at `/home/me/bot/index.js` and all your pieces are at
// `/home/me/bot/pieces` (e.g. `/home/me/bot/pieces/commands/MyCommand.js`):
const client = new SapphireClient({
  baseUserDirectory: join(__dirname, 'pieces'),
  // More options...
});
```

**`example`**
```typescript
// Opt-out automatic scanning:
const client = new SapphireClient({
  baseUserDirectory: null,
  // More options...
});
```

## Type parameters

| Name | Type |
| :------ | :------ |
| `Ready` | extends `boolean``boolean` |

## Hierarchy

- [`Client`](https://discord.js.org/#/docs/main/stable/class/Client)<`Ready`\>

  ↳ **`SapphireClient`**

## Constructors

### constructor

• **new SapphireClient**<`Ready`\>(`options`)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `Ready` | extends `boolean``boolean` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `ClientOptions` |

#### Overrides

Client&lt;Ready\&gt;.constructor

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:220](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L220)

## Properties

### application

• **application**: `If`<`Ready`, [`ClientApplication`](https://discord.js.org/#/docs/main/stable/class/ClientApplication), ``null``\>

#### Inherited from

Client.application

#### Defined in

node_modules/discord.js/typings/index.d.ts:472

___

### channels

• **channels**: [`ChannelManager`](https://discord.js.org/#/docs/main/stable/class/ChannelManager)

#### Inherited from

Client.channels

#### Defined in

node_modules/discord.js/typings/index.d.ts:473

___

### emojis

• `Readonly` **emojis**: [`BaseGuildEmojiManager`](https://discord.js.org/#/docs/main/stable/class/BaseGuildEmojiManager)

#### Inherited from

Client.emojis

#### Defined in

node_modules/discord.js/typings/index.d.ts:474

___

### fetchPrefix

• **fetchPrefix**: [`SapphirePrefixHook`](../interfaces/SapphirePrefixHook)

The method to be overriden by the developer.

**`since`** 1.0.0

**`returns`** A string for a single prefix, an array of strings for matching multiple, or null for no match (mention prefix only).

**`example`**
```typescript
// Return always the same prefix (unconfigurable):
client.fetchPrefix = () => '!';
```

**`example`**
```typescript
// Retrieving the prefix from a SQL database:
client.fetchPrefix = async (message) => {
  // note: driver is something generic and depends on how you connect to your database
  const guild = await driver.getOne('SELECT prefix FROM public.guild WHERE id = $1', [message.guild.id]);
  return guild?.prefix ?? '!';
};
```

**`example`**
```typescript
// Retrieving the prefix from an ORM:
client.fetchPrefix = async (message) => {
  // note: driver is something generic and depends on how you connect to your database
  const guild = await driver.getRepository(GuildEntity).findOne({ id: message.guild.id });
  return guild?.prefix ?? '!';
};
```

#### Overrides

Client.fetchPrefix

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:205](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L205)

___

### guilds

• **guilds**: [`GuildManager`](https://discord.js.org/#/docs/main/stable/class/GuildManager)

#### Inherited from

Client.guilds

#### Defined in

node_modules/discord.js/typings/index.d.ts:475

___

### id

• **id**: ``null`` \| `string` = `null`

The client's ID, used for the user prefix.

**`since`** 1.0.0

#### Overrides

Client.id

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:175](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L175)

___

### logger

• **logger**: [`ILogger`](../interfaces/ILogger)

The logger to be used by the framework and plugins. By default, a [Logger](Logger) instance is used, which emits the
messages to the console.

**`since`** 1.0.0

#### Overrides

Client.logger

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:212](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L212)

___

### options

• **options**: `ClientOptions`

#### Inherited from

Client.options

#### Defined in

node_modules/discord.js/typings/index.d.ts:476

___

### readyAt

• **readyAt**: `If`<`Ready`, `Date`, ``null``\>

#### Inherited from

Client.readyAt

#### Defined in

node_modules/discord.js/typings/index.d.ts:477

___

### readyTimestamp

• `Readonly` **readyTimestamp**: `If`<`Ready`, `number`, ``null``\>

#### Inherited from

Client.readyTimestamp

#### Defined in

node_modules/discord.js/typings/index.d.ts:478

___

### shard

• **shard**: ``null`` \| [`ShardClientUtil`](https://discord.js.org/#/docs/main/stable/class/ShardClientUtil)

#### Inherited from

Client.shard

#### Defined in

node_modules/discord.js/typings/index.d.ts:479

___

### stores

• **stores**: [`StoreRegistry`](StoreRegistry)

The registered stores.

**`since`** 1.0.0

#### Overrides

Client.stores

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:218](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L218)

___

### token

• **token**: `If`<`Ready`, `string`, ``null`` \| `string`\>

#### Inherited from

Client.token

#### Defined in

node_modules/discord.js/typings/index.d.ts:480

___

### uptime

• **uptime**: `If`<`Ready`, `number`, ``null``\>

#### Inherited from

Client.uptime

#### Defined in

node_modules/discord.js/typings/index.d.ts:481

___

### user

• **user**: `If`<`Ready`, [`ClientUser`](https://discord.js.org/#/docs/main/stable/class/ClientUser), ``null``\>

#### Inherited from

Client.user

#### Defined in

node_modules/discord.js/typings/index.d.ts:482

___

### users

• **users**: [`UserManager`](https://discord.js.org/#/docs/main/stable/class/UserManager)

#### Inherited from

Client.users

#### Defined in

node_modules/discord.js/typings/index.d.ts:483

___

### voice

• **voice**: [`ClientVoiceManager`](https://discord.js.org/#/docs/main/stable/class/ClientVoiceManager)

#### Inherited from

Client.voice

#### Defined in

node_modules/discord.js/typings/index.d.ts:484

___

### ws

• **ws**: [`WebSocketManager`](https://discord.js.org/#/docs/main/stable/class/WebSocketManager)

#### Inherited from

Client.ws

#### Defined in

node_modules/discord.js/typings/index.d.ts:485

___

### captureRejectionSymbol

▪ `Static` `Readonly` **captureRejectionSymbol**: typeof [`captureRejectionSymbol`](SapphireClient#capturerejectionsymbol)

#### Inherited from

Client.captureRejectionSymbol

#### Defined in

node_modules/@types/node/events.d.ts:273

___

### captureRejections

▪ `Static` **captureRejections**: `boolean`

Sets or gets the default captureRejection value for all emitters.

#### Inherited from

Client.captureRejections

#### Defined in

node_modules/@types/node/events.d.ts:278

___

### defaultMaxListeners

▪ `Static` **defaultMaxListeners**: `number`

#### Inherited from

Client.defaultMaxListeners

#### Defined in

node_modules/@types/node/events.d.ts:279

___

### errorMonitor

▪ `Static` `Readonly` **errorMonitor**: typeof [`errorMonitor`](SapphireClient#errormonitor)

This symbol shall be used to install a listener for only monitoring `'error'`
events. Listeners installed using this symbol are called before the regular
`'error'` listeners are called.

Installing a listener using this symbol does not change the behavior once an
`'error'` event is emitted, therefore the process will still crash if no
regular `'error'` listener is installed.

#### Inherited from

Client.errorMonitor

#### Defined in

node_modules/@types/node/events.d.ts:272

___

### plugins

▪ `Static` **plugins**: [`PluginManager`](PluginManager)

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:291](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L291)

## Methods

### addListener

▸ **addListener**(`eventName`, `listener`): [`SapphireClient`](SapphireClient)<`Ready`\>

Alias for `emitter.on(eventName, listener)`.

**`since`** v0.1.26

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName` | `string` \| `symbol` |
| `listener` | (...`args`: `any`[]) => `void` |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.addListener

#### Defined in

node_modules/@types/node/events.d.ts:299

___

### destroy

▸ **destroy**(): `void`

#### Returns

`void`

#### Inherited from

Client.destroy

#### Defined in

node_modules/discord.js/typings/index.d.ts:486

___

### emit

▸ **emit**<`K`\>(`event`, ...`args`): `boolean`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof `ClientEvents` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `event` | `K` |
| `...args` | `ClientEvents`[`K`] |

#### Returns

`boolean`

#### Inherited from

Client.emit

#### Defined in

node_modules/discord.js/typings/index.d.ts:513

▸ **emit**<`S`\>(`event`, ...`args`): `boolean`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `S` | extends `string` \| `symbol` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `event` | `Exclude`<`S`, keyof `ClientEvents`\> |
| `...args` | `unknown`[] |

#### Returns

`boolean`

#### Inherited from

Client.emit

#### Defined in

node_modules/discord.js/typings/index.d.ts:514

___

### eventNames

▸ **eventNames**(): (`string` \| `symbol`)[]

Returns an array listing the events for which the emitter has registered
listeners. The values in the array are strings or `Symbol`s.

```js
const EventEmitter = require('events');
const myEE = new EventEmitter();
myEE.on('foo', () => {});
myEE.on('bar', () => {});

const sym = Symbol('symbol');
myEE.on(sym, () => {});

console.log(myEE.eventNames());
// Prints: [ 'foo', 'bar', Symbol(symbol) ]
```

**`since`** v6.0.0

#### Returns

(`string` \| `symbol`)[]

#### Inherited from

Client.eventNames

#### Defined in

node_modules/@types/node/events.d.ts:614

___

### fetchGuildPreview

▸ **fetchGuildPreview**(`guild`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`GuildPreview`](https://discord.js.org/#/docs/main/stable/class/GuildPreview)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `guild` | `GuildResolvable` |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`GuildPreview`](https://discord.js.org/#/docs/main/stable/class/GuildPreview)\>

#### Inherited from

Client.fetchGuildPreview

#### Defined in

node_modules/discord.js/typings/index.d.ts:487

___

### fetchGuildTemplate

▸ **fetchGuildTemplate**(`template`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`GuildTemplate`](https://discord.js.org/#/docs/main/stable/class/GuildTemplate)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `template` | `string` |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`GuildTemplate`](https://discord.js.org/#/docs/main/stable/class/GuildTemplate)\>

#### Inherited from

Client.fetchGuildTemplate

#### Defined in

node_modules/discord.js/typings/index.d.ts:489

___

### fetchGuildWidget

▸ **fetchGuildWidget**(`guild`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Widget`](https://discord.js.org/#/docs/main/stable/class/Widget)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `guild` | `GuildResolvable` |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Widget`](https://discord.js.org/#/docs/main/stable/class/Widget)\>

#### Inherited from

Client.fetchGuildWidget

#### Defined in

node_modules/discord.js/typings/index.d.ts:494

___

### fetchInvite

▸ **fetchInvite**(`invite`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Invite`](https://discord.js.org/#/docs/main/stable/class/Invite)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `invite` | `string` |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Invite`](https://discord.js.org/#/docs/main/stable/class/Invite)\>

#### Inherited from

Client.fetchInvite

#### Defined in

node_modules/discord.js/typings/index.d.ts:488

___

### fetchPremiumStickerPacks

▸ **fetchPremiumStickerPacks**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Collection`<`string`, [`StickerPack`](https://discord.js.org/#/docs/main/stable/class/StickerPack)\>\>

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Collection`<`string`, [`StickerPack`](https://discord.js.org/#/docs/main/stable/class/StickerPack)\>\>

#### Inherited from

Client.fetchPremiumStickerPacks

#### Defined in

node_modules/discord.js/typings/index.d.ts:492

___

### fetchSticker

▸ **fetchSticker**(`id`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Sticker`](https://discord.js.org/#/docs/main/stable/class/Sticker)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `string` |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Sticker`](https://discord.js.org/#/docs/main/stable/class/Sticker)\>

#### Inherited from

Client.fetchSticker

#### Defined in

node_modules/discord.js/typings/index.d.ts:491

___

### fetchVoiceRegions

▸ **fetchVoiceRegions**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Collection`<`string`, [`VoiceRegion`](https://discord.js.org/#/docs/main/stable/class/VoiceRegion)\>\>

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Collection`<`string`, [`VoiceRegion`](https://discord.js.org/#/docs/main/stable/class/VoiceRegion)\>\>

#### Inherited from

Client.fetchVoiceRegions

#### Defined in

node_modules/discord.js/typings/index.d.ts:490

___

### fetchWebhook

▸ **fetchWebhook**(`id`, `token?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Webhook`](https://discord.js.org/#/docs/main/stable/class/Webhook)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `string` |
| `token?` | `string` |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Webhook`](https://discord.js.org/#/docs/main/stable/class/Webhook)\>

#### Inherited from

Client.fetchWebhook

#### Defined in

node_modules/discord.js/typings/index.d.ts:493

___

### generateInvite

▸ **generateInvite**(`options?`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | `InviteGenerationOptions` |

#### Returns

`string`

#### Inherited from

Client.generateInvite

#### Defined in

node_modules/discord.js/typings/index.d.ts:495

___

### getMaxListeners

▸ **getMaxListeners**(): `number`

Returns the current max listener value for the `EventEmitter` which is either
set by `emitter.setMaxListeners(n)` or defaults to [defaultMaxListeners](SapphireClient#defaultmaxlisteners).

**`since`** v1.0.0

#### Returns

`number`

#### Inherited from

Client.getMaxListeners

#### Defined in

node_modules/@types/node/events.d.ts:471

___

### isReady

▸ **isReady**(): this is Client<true\>

#### Returns

this is Client<true\>

#### Inherited from

Client.isReady

#### Defined in

node_modules/discord.js/typings/index.d.ts:497

___

### listenerCount

▸ **listenerCount**(`eventName`): `number`

Returns the number of listeners listening to the event named `eventName`.

**`since`** v3.2.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `eventName` | `string` \| `symbol` | The name of the event being listened for |

#### Returns

`number`

#### Inherited from

Client.listenerCount

#### Defined in

node_modules/@types/node/events.d.ts:561

___

### listeners

▸ **listeners**(`eventName`): `Function`[]

Returns a copy of the array of listeners for the event named `eventName`.

```js
server.on('connection', (stream) => {
  console.log('someone connected!');
});
console.log(util.inspect(server.listeners('connection')));
// Prints: [ [Function] ]
```

**`since`** v0.1.26

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName` | `string` \| `symbol` |

#### Returns

`Function`[]

#### Inherited from

Client.listeners

#### Defined in

node_modules/@types/node/events.d.ts:484

___

### login

▸ **login**(`token?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`string`\>

Loads all pieces, then logs the client in, establishing a websocket connection to Discord.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `token?` | `string` | Token of the account to log in with. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`string`\>

Token of the account used.

#### Overrides

Client.login

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:266](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L266)

___

### off

▸ **off**<`K`\>(`event`, `listener`): [`SapphireClient`](SapphireClient)<`Ready`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof `ClientEvents` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `event` | `K` |
| `listener` | (...`args`: `ClientEvents`[`K`]) => `Awaitable`<`void`\> |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.off

#### Defined in

node_modules/discord.js/typings/index.d.ts:516

▸ **off**<`S`\>(`event`, `listener`): [`SapphireClient`](SapphireClient)<`Ready`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `S` | extends `string` \| `symbol` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `event` | `Exclude`<`S`, keyof `ClientEvents`\> |
| `listener` | (...`args`: `any`[]) => `Awaitable`<`void`\> |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.off

#### Defined in

node_modules/discord.js/typings/index.d.ts:517

___

### on

▸ **on**<`K`\>(`event`, `listener`): [`SapphireClient`](SapphireClient)<`Ready`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof `ClientEvents` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `event` | `K` |
| `listener` | (...`args`: `ClientEvents`[`K`]) => `Awaitable`<`void`\> |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.on

#### Defined in

node_modules/discord.js/typings/index.d.ts:501

▸ **on**<`S`\>(`event`, `listener`): [`SapphireClient`](SapphireClient)<`Ready`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `S` | extends `string` \| `symbol` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `event` | `Exclude`<`S`, keyof `ClientEvents`\> |
| `listener` | (...`args`: `any`[]) => `Awaitable`<`void`\> |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.on

#### Defined in

node_modules/discord.js/typings/index.d.ts:502

___

### once

▸ **once**<`K`\>(`event`, `listener`): [`SapphireClient`](SapphireClient)<`Ready`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof `ClientEvents` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `event` | `K` |
| `listener` | (...`args`: `ClientEvents`[`K`]) => `Awaitable`<`void`\> |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.once

#### Defined in

node_modules/discord.js/typings/index.d.ts:507

▸ **once**<`S`\>(`event`, `listener`): [`SapphireClient`](SapphireClient)<`Ready`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `S` | extends `string` \| `symbol` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `event` | `Exclude`<`S`, keyof `ClientEvents`\> |
| `listener` | (...`args`: `any`[]) => `Awaitable`<`void`\> |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.once

#### Defined in

node_modules/discord.js/typings/index.d.ts:508

___

### prependListener

▸ **prependListener**(`eventName`, `listener`): [`SapphireClient`](SapphireClient)<`Ready`\>

Adds the `listener` function to the _beginning_ of the listeners array for the
event named `eventName`. No checks are made to see if the `listener` has
already been added. Multiple calls passing the same combination of `eventName`and `listener` will result in the `listener` being added, and called, multiple
times.

```js
server.prependListener('connection', (stream) => {
  console.log('someone connected!');
});
```

Returns a reference to the `EventEmitter`, so that calls can be chained.

**`since`** v6.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `eventName` | `string` \| `symbol` | The name of the event. |
| `listener` | (...`args`: `any`[]) => `void` | The callback function |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.prependListener

#### Defined in

node_modules/@types/node/events.d.ts:579

___

### prependOnceListener

▸ **prependOnceListener**(`eventName`, `listener`): [`SapphireClient`](SapphireClient)<`Ready`\>

Adds a **one-time**`listener` function for the event named `eventName` to the_beginning_ of the listeners array. The next time `eventName` is triggered, this
listener is removed, and then invoked.

```js
server.prependOnceListener('connection', (stream) => {
  console.log('Ah, we have our first user!');
});
```

Returns a reference to the `EventEmitter`, so that calls can be chained.

**`since`** v6.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `eventName` | `string` \| `symbol` | The name of the event. |
| `listener` | (...`args`: `any`[]) => `void` | The callback function |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.prependOnceListener

#### Defined in

node_modules/@types/node/events.d.ts:595

___

### rawListeners

▸ **rawListeners**(`eventName`): `Function`[]

Returns a copy of the array of listeners for the event named `eventName`,
including any wrappers (such as those created by `.once()`).

```js
const emitter = new EventEmitter();
emitter.once('log', () => console.log('log once'));

// Returns a new Array with a function `onceWrapper` which has a property
// `listener` which contains the original listener bound above
const listeners = emitter.rawListeners('log');
const logFnWrapper = listeners[0];

// Logs "log once" to the console and does not unbind the `once` event
logFnWrapper.listener();

// Logs "log once" to the console and removes the listener
logFnWrapper();

emitter.on('log', () => console.log('log persistently'));
// Will return a new Array with a single function bound by `.on()` above
const newListeners = emitter.rawListeners('log');

// Logs "log persistently" twice
newListeners[0]();
emitter.emit('log');
```

**`since`** v9.4.0

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName` | `string` \| `symbol` |

#### Returns

`Function`[]

#### Inherited from

Client.rawListeners

#### Defined in

node_modules/@types/node/events.d.ts:514

___

### removeAllListeners

▸ **removeAllListeners**<`K`\>(`event?`): [`SapphireClient`](SapphireClient)<`Ready`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof `ClientEvents` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `event?` | `K` |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.removeAllListeners

#### Defined in

node_modules/discord.js/typings/index.d.ts:522

▸ **removeAllListeners**<`S`\>(`event?`): [`SapphireClient`](SapphireClient)<`Ready`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `S` | extends `string` \| `symbol` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `event?` | `Exclude`<`S`, keyof `ClientEvents`\> |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.removeAllListeners

#### Defined in

node_modules/discord.js/typings/index.d.ts:523

___

### removeListener

▸ **removeListener**(`eventName`, `listener`): [`SapphireClient`](SapphireClient)<`Ready`\>

Removes the specified `listener` from the listener array for the event named`eventName`.

```js
const callback = (stream) => {
  console.log('someone connected!');
};
server.on('connection', callback);
// ...
server.removeListener('connection', callback);
```

`removeListener()` will remove, at most, one instance of a listener from the
listener array. If any single listener has been added multiple times to the
listener array for the specified `eventName`, then `removeListener()` must be
called multiple times to remove each instance.

Once an event is emitted, all listeners attached to it at the
time of emitting are called in order. This implies that any`removeListener()` or `removeAllListeners()` calls _after_ emitting and_before_ the last listener finishes execution will
not remove them from`emit()` in progress. Subsequent events behave as expected.

```js
const myEmitter = new MyEmitter();

const callbackA = () => {
  console.log('A');
  myEmitter.removeListener('event', callbackB);
};

const callbackB = () => {
  console.log('B');
};

myEmitter.on('event', callbackA);

myEmitter.on('event', callbackB);

// callbackA removes listener callbackB but it will still be called.
// Internal listener array at time of emit [callbackA, callbackB]
myEmitter.emit('event');
// Prints:
//   A
//   B

// callbackB is now removed.
// Internal listener array [callbackA]
myEmitter.emit('event');
// Prints:
//   A
```

Because listeners are managed using an internal array, calling this will
change the position indices of any listener registered _after_ the listener
being removed. This will not impact the order in which listeners are called,
but it means that any copies of the listener array as returned by
the `emitter.listeners()` method will need to be recreated.

When a single function has been added as a handler multiple times for a single
event (as in the example below), `removeListener()` will remove the most
recently added instance. In the example the `once('ping')`listener is removed:

```js
const ee = new EventEmitter();

function pong() {
  console.log('pong');
}

ee.on('ping', pong);
ee.once('ping', pong);
ee.removeListener('ping', pong);

ee.emit('ping');
ee.emit('ping');
```

Returns a reference to the `EventEmitter`, so that calls can be chained.

**`since`** v0.1.26

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName` | `string` \| `symbol` |
| `listener` | (...`args`: `any`[]) => `void` |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.removeListener

#### Defined in

node_modules/@types/node/events.d.ts:439

___

### setMaxListeners

▸ **setMaxListeners**(`n`): [`SapphireClient`](SapphireClient)<`Ready`\>

By default `EventEmitter`s will print a warning if more than `10` listeners are
added for a particular event. This is a useful default that helps finding
memory leaks. The `emitter.setMaxListeners()` method allows the limit to be
modified for this specific `EventEmitter` instance. The value can be set to`Infinity` (or `0`) to indicate an unlimited number of listeners.

Returns a reference to the `EventEmitter`, so that calls can be chained.

**`since`** v0.3.5

#### Parameters

| Name | Type |
| :------ | :------ |
| `n` | `number` |

#### Returns

[`SapphireClient`](SapphireClient)<`Ready`\>

#### Inherited from

Client.setMaxListeners

#### Defined in

node_modules/@types/node/events.d.ts:465

___

### sweepMessages

▸ **sweepMessages**(`lifetime?`): `number`

#### Parameters

| Name | Type |
| :------ | :------ |
| `lifetime?` | `number` |

#### Returns

`number`

#### Inherited from

Client.sweepMessages

#### Defined in

node_modules/discord.js/typings/index.d.ts:498

___

### toJSON

▸ **toJSON**(): `unknown`

#### Returns

`unknown`

#### Inherited from

Client.toJSON

#### Defined in

node_modules/discord.js/typings/index.d.ts:499

___

### getEventListeners

▸ `Static` **getEventListeners**(`emitter`, `name`): `Function`[]

Returns a copy of the array of listeners for the event named `eventName`.

For `EventEmitter`s this behaves exactly the same as calling `.listeners` on
the emitter.

For `EventTarget`s this is the only way to get the event listeners for the
event target. This is useful for debugging and diagnostic purposes.

```js
const { getEventListeners, EventEmitter } = require('events');

{
  const ee = new EventEmitter();
  const listener = () => console.log('Events are fun');
  ee.on('foo', listener);
  getEventListeners(ee, 'foo'); // [listener]
}
{
  const et = new EventTarget();
  const listener = () => console.log('Events are fun');
  et.addEventListener('foo', listener);
  getEventListeners(et, 'foo'); // [listener]
}
```

**`since`** v15.2.0

#### Parameters

| Name | Type |
| :------ | :------ |
| `emitter` | `EventEmitter` \| `DOMEventTarget` |
| `name` | `string` \| `symbol` |

#### Returns

`Function`[]

#### Inherited from

Client.getEventListeners

#### Defined in

node_modules/@types/node/events.d.ts:262

___

### listenerCount

▸ `Static` **listenerCount**(`emitter`, `eventName`): `number`

A class method that returns the number of listeners for the given `eventName`registered on the given `emitter`.

```js
const { EventEmitter, listenerCount } = require('events');
const myEmitter = new EventEmitter();
myEmitter.on('event', () => {});
myEmitter.on('event', () => {});
console.log(listenerCount(myEmitter, 'event'));
// Prints: 2
```

**`since`** v0.9.12

**`deprecated`** Since v3.2.0 - Use `listenerCount` instead.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `emitter` | `EventEmitter` | The emitter to query |
| `eventName` | `string` \| `symbol` | The event name |

#### Returns

`number`

#### Inherited from

Client.listenerCount

#### Defined in

node_modules/@types/node/events.d.ts:234

___

### on

▸ `Static` **on**(`emitter`, `eventName`, `options?`): `AsyncIterableIterator`<`any`\>

```js
const { on, EventEmitter } = require('events');

(async () => {
  const ee = new EventEmitter();

  // Emit later on
  process.nextTick(() => {
    ee.emit('foo', 'bar');
    ee.emit('foo', 42);
  });

  for await (const event of on(ee, 'foo')) {
    // The execution of this inner block is synchronous and it
    // processes one event at a time (even with await). Do not use
    // if concurrent execution is required.
    console.log(event); // prints ['bar'] [42]
  }
  // Unreachable here
})();
```

Returns an `AsyncIterator` that iterates `eventName` events. It will throw
if the `EventEmitter` emits `'error'`. It removes all listeners when
exiting the loop. The `value` returned by each iteration is an array
composed of the emitted event arguments.

An `AbortSignal` can be used to cancel waiting on events:

```js
const { on, EventEmitter } = require('events');
const ac = new AbortController();

(async () => {
  const ee = new EventEmitter();

  // Emit later on
  process.nextTick(() => {
    ee.emit('foo', 'bar');
    ee.emit('foo', 42);
  });

  for await (const event of on(ee, 'foo', { signal: ac.signal })) {
    // The execution of this inner block is synchronous and it
    // processes one event at a time (even with await). Do not use
    // if concurrent execution is required.
    console.log(event); // prints ['bar'] [42]
  }
  // Unreachable here
})();

process.nextTick(() => ac.abort());
```

**`since`** v13.6.0, v12.16.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `emitter` | `EventEmitter` | - |
| `eventName` | `string` | The name of the event being listened for |
| `options?` | `StaticEventEmitterOptions` | - |

#### Returns

`AsyncIterableIterator`<`any`\>

that iterates `eventName` events emitted by the `emitter`

#### Inherited from

Client.on

#### Defined in

node_modules/@types/node/events.d.ts:217

___

### once

▸ `Static` **once**(`emitter`, `eventName`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`any`[]\>

Creates a `Promise` that is fulfilled when the `EventEmitter` emits the given
event or that is rejected if the `EventEmitter` emits `'error'` while waiting.
The `Promise` will resolve with an array of all the arguments emitted to the
given event.

This method is intentionally generic and works with the web platform [EventTarget](https://dom.spec.whatwg.org/#interface-eventtarget) interface, which has no special`'error'` event
semantics and does not listen to the `'error'` event.

```js
const { once, EventEmitter } = require('events');

async function run() {
  const ee = new EventEmitter();

  process.nextTick(() => {
    ee.emit('myevent', 42);
  });

  const [value] = await once(ee, 'myevent');
  console.log(value);

  const err = new Error('kaboom');
  process.nextTick(() => {
    ee.emit('error', err);
  });

  try {
    await once(ee, 'myevent');
  } catch (err) {
    console.log('error happened', err);
  }
}

run();
```

The special handling of the `'error'` event is only used when `events.once()`is used to wait for another event. If `events.once()` is used to wait for the
'`error'` event itself, then it is treated as any other kind of event without
special handling:

```js
const { EventEmitter, once } = require('events');

const ee = new EventEmitter();

once(ee, 'error')
  .then(([err]) => console.log('ok', err.message))
  .catch((err) => console.log('error', err.message));

ee.emit('error', new Error('boom'));

// Prints: ok boom
```

An `AbortSignal` can be used to cancel waiting for the event:

```js
const { EventEmitter, once } = require('events');

const ee = new EventEmitter();
const ac = new AbortController();

async function foo(emitter, event, signal) {
  try {
    await once(emitter, event, { signal });
    console.log('event emitted!');
  } catch (error) {
    if (error.name === 'AbortError') {
      console.error('Waiting for the event was canceled!');
    } else {
      console.error('There was an error', error.message);
    }
  }
}

foo(ee, 'foo', ac.signal);
ac.abort(); // Abort waiting for the event
ee.emit('foo'); // Prints: Waiting for the event was canceled!
```

**`since`** v11.13.0, v10.16.0

#### Parameters

| Name | Type |
| :------ | :------ |
| `emitter` | `NodeEventTarget` |
| `eventName` | `string` \| `symbol` |
| `options?` | `StaticEventEmitterOptions` |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`any`[]\>

#### Inherited from

Client.once

#### Defined in

node_modules/@types/node/events.d.ts:157

▸ `Static` **once**(`emitter`, `eventName`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`any`[]\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `emitter` | `DOMEventTarget` |
| `eventName` | `string` |
| `options?` | `StaticEventEmitterOptions` |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`any`[]\>

#### Inherited from

Client.once

#### Defined in

node_modules/@types/node/events.d.ts:158

___

### use

▸ `Static` **use**(`plugin`): typeof [`SapphireClient`](SapphireClient)

#### Parameters

| Name | Type |
| :------ | :------ |
| `plugin` | typeof [`Plugin`](Plugin) |

#### Returns

typeof [`SapphireClient`](SapphireClient)

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:293](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L293)

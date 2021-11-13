---
id: "Precondition"
title: "Class: Precondition<O>"
sidebar_label: "Precondition"
sidebar_position: 0
custom_edit_url: null
---

## Type parameters

| Name | Type |
| :------ | :------ |
| `O` | extends [`PreconditionOptions`](../interfaces/PreconditionOptions)[`PreconditionOptions`](../interfaces/PreconditionOptions) |

## Hierarchy

- [`Piece`](Piece)<`O`\>

  ↳ **`Precondition`**

  ↳↳ [`ClientPermissions`](CorePreconditions.ClientPermissions)

  ↳↳ [`Cooldown`](CorePreconditions.Cooldown)

  ↳↳ [`DMOnly`](CorePreconditions.DMOnly)

  ↳↳ [`Enabled`](CorePreconditions.Enabled)

  ↳↳ [`GuildNewsOnly`](CorePreconditions.GuildNewsOnly)

  ↳↳ [`GuildNewsThreadOnly`](CorePreconditions.GuildNewsThreadOnly)

  ↳↳ [`GuildOnly`](CorePreconditions.GuildOnly)

  ↳↳ [`GuildPrivateThreadOnly`](CorePreconditions.GuildPrivateThreadOnly)

  ↳↳ [`GuildPublicThreadOnly`](CorePreconditions.GuildPublicThreadOnly)

  ↳↳ [`GuildTextOnly`](CorePreconditions.GuildTextOnly)

  ↳↳ [`GuildThreadOnly`](CorePreconditions.GuildThreadOnly)

  ↳↳ [`NSFW`](CorePreconditions.NSFW)

  ↳↳ [`UserPermissions`](CorePreconditions.UserPermissions)

## Constructors

### constructor

• **new Precondition**<`O`\>(`context`, `options?`)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `O` | extends [`PreconditionOptions`](../interfaces/PreconditionOptions)[`PreconditionOptions`](../interfaces/PreconditionOptions) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `context` | [`PieceContext`](../interfaces/PieceContext) |
| `options` | [`PreconditionOptions`](../interfaces/PreconditionOptions) |

#### Overrides

[Piece](Piece).[constructor](Piece#constructor)

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:16](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L16)

## Properties

### enabled

• **enabled**: `boolean`

Whether or not the piece is enabled.

#### Inherited from

[Piece](Piece).[enabled](Piece#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:432

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

### options

• `Readonly` **options**: `O`

The raw options passed to this [Piece](Piece)

#### Inherited from

[Piece](Piece).[options](Piece#options)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:436

___

### position

• `Readonly` **position**: ``null`` \| `number`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:14](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L14)

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

### error

▸ **error**(`options?`): [`PreconditionResult`](../#preconditionresult)

Constructs a [PreconditionError](PreconditionError) with the precondition parameter set to `this`.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | `Omit`<[`Options`](../interfaces/PreconditionError.Options), ``"precondition"``\> | The information. |

#### Returns

[`PreconditionResult`](../#preconditionresult)

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:31](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L31)

___

### ok

▸ **ok**(): [`PreconditionResult`](../#preconditionresult)

#### Returns

[`PreconditionResult`](../#preconditionresult)

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:23](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L23)

___

### onLoad

▸ **onLoad**(): `unknown`

Per-piece listener that is called when the piece is loaded into the store.
Useful to set-up asynchronous initialization tasks.

#### Returns

`unknown`

#### Inherited from

[Piece](Piece).[onLoad](Piece#onload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:447

___

### onUnload

▸ **onUnload**(): `unknown`

Per-piece listener that is called when the piece is unloaded from the store.
Useful to set-up clean-up tasks.

#### Returns

`unknown`

#### Inherited from

[Piece](Piece).[onUnload](Piece#onunload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:452

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

▸ `Abstract` **run**(`message`, `command`, `context`): [`PreconditionResult`](../#preconditionresult)

#### Parameters

| Name | Type |
| :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> |
| `command` | [`Command`](Command)<[`Args`](Args), [`CommandOptions`](../interfaces/CommandOptions)\> |
| `context` | [`PreconditionContext`](../interfaces/PreconditionContext) |

#### Returns

[`PreconditionResult`](../#preconditionresult)

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:21](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L21)

___

### toJSON

▸ **toJSON**(): `PieceJSON`

Defines the `JSON.stringify` behavior of this piece.

#### Returns

`PieceJSON`

#### Inherited from

[Piece](Piece).[toJSON](Piece#tojson)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:464

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

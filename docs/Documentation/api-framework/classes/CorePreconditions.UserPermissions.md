---
id: "CorePreconditions.UserPermissions"
title: "Class: UserPermissions"
sidebar_label: "CorePreconditions.UserPermissions"
custom_edit_url: null
---

[CorePreconditions](../namespaces/CorePreconditions).UserPermissions

## Hierarchy

- [`Precondition`](Precondition)

  ↳ **`UserPermissions`**

## Constructors

### constructor

• **new UserPermissions**(`context`, `options?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `context` | [`PieceContext`](../interfaces/PieceContext) |
| `options` | [`PreconditionOptions`](../interfaces/PreconditionOptions) |

#### Inherited from

[Precondition](Precondition).[constructor](Precondition#constructor)

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:16](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L16)

## Properties

### dmChannelPermissions

• `Private` `Readonly` **dmChannelPermissions**: `Readonly`<[`BitField`](https://discord.js.org/#/docs/main/stable/class/BitField)<`PermissionString`, `bigint`\>\>

#### Defined in

[projects/framework/src/preconditions/UserPermissions.ts:8](https://github.com/sapphiredev/framework/blob/5a4898f6/src/preconditions/UserPermissions.ts#L8)

___

### enabled

• **enabled**: `boolean`

Whether or not the piece is enabled.

#### Inherited from

[Precondition](Precondition).[enabled](Precondition#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:432

___

### location

• `Readonly` **location**: `PieceLocation`

The location metadata for the piece's file.

#### Inherited from

[Precondition](Precondition).[location](Precondition#location)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:424

___

### name

• `Readonly` **name**: `string`

The name of the piece.

#### Inherited from

[Precondition](Precondition).[name](Precondition#name)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:428

___

### options

• `Readonly` **options**: [`PreconditionOptions`](../interfaces/PreconditionOptions)

The raw options passed to this [Piece](Piece)

#### Inherited from

[Precondition](Precondition).[options](Precondition#options)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:436

___

### position

• `Readonly` **position**: ``null`` \| `number`

#### Inherited from

[Precondition](Precondition).[position](Precondition#position)

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:14](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L14)

___

### store

• `Readonly` **store**: [`Store`](Store)<[`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions)\>\>

The store that contains the piece.

#### Inherited from

[Precondition](Precondition).[store](Precondition#store)

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

Precondition.container

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

#### Inherited from

[Precondition](Precondition).[error](Precondition#error)

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:31](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L31)

___

### ok

▸ **ok**(): [`PreconditionResult`](../#preconditionresult)

#### Returns

[`PreconditionResult`](../#preconditionresult)

#### Inherited from

[Precondition](Precondition).[ok](Precondition#ok)

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

[Precondition](Precondition).[onLoad](Precondition#onload)

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

[Precondition](Precondition).[onUnload](Precondition#onunload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:452

___

### reload

▸ **reload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Reloads the piece by loading the same path in the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Precondition](Precondition).[reload](Precondition#reload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:460

___

### run

▸ **run**(`message`, `_command`, `context`): [`PreconditionResult`](../#preconditionresult)

#### Parameters

| Name | Type |
| :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> |
| `_command` | [`Command`](Command)<[`Args`](Args), [`CommandOptions`](../interfaces/CommandOptions)\> |
| `context` | [`PreconditionContext`](../interfaces/PreconditionContext) |

#### Returns

[`PreconditionResult`](../#preconditionresult)

#### Overrides

[Precondition](Precondition).[run](Precondition#run)

#### Defined in

[projects/framework/src/preconditions/UserPermissions.ts:22](https://github.com/sapphiredev/framework/blob/5a4898f6/src/preconditions/UserPermissions.ts#L22)

___

### toJSON

▸ **toJSON**(): `PieceJSON`

Defines the `JSON.stringify` behavior of this piece.

#### Returns

`PieceJSON`

#### Inherited from

[Precondition](Precondition).[toJSON](Precondition#tojson)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:464

___

### unload

▸ **unload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Unloads and disables the piece.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Precondition](Precondition).[unload](Precondition#unload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:456

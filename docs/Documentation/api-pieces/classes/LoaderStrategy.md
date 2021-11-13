---
id: "LoaderStrategy"
title: "Class: LoaderStrategy<T>"
sidebar_label: "LoaderStrategy"
sidebar_position: 0
custom_edit_url: null
---

A multi-purpose feature-complete loader strategy supporting multi-piece modules as well as supporting both ECMAScript
Modules and CommonJS with reloading support.

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Piece`](Piece) |

## Implements

- [`ILoaderStrategy`](../interfaces/ILoaderStrategy)<`T`\>

## Constructors

### constructor

• **new LoaderStrategy**<`T`\>()

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions), `T`\> |

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:21](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L21)

## Properties

### clientUsesESModules

• **clientUsesESModules**: `boolean`

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:17](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L17)

___

### filterDtsFiles

• `Private` `Readonly` **filterDtsFiles**: `boolean` = `false`

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:19](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L19)

___

### supportedExtensions

• **supportedExtensions**: `string`[]

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:18](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L18)

## Methods

### filter

▸ **filter**(`path`): [`FilterResult`](../#filterresult)

Retrieves the name and the extension of the specified file path.

#### Parameters

| Name | Type |
| :------ | :------ |
| `path` | `string` |

#### Returns

[`FilterResult`](../#filterresult)

A [ModuleData](../interfaces/ModuleData) on success, otherwise `null` to stop the store from processing the path.

#### Implementation of

[ILoaderStrategy](../interfaces/ILoaderStrategy).[filter](../interfaces/ILoaderStrategy#filter)

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:36](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L36)

___

### load

▸ **load**(`store`, `file`): [`ILoaderResult`](../#iloaderresult)<`T`\>

The load hook, use this to override the loader.

#### Parameters

| Name | Type |
| :------ | :------ |
| `store` | [`Store`](Store)<`T`\> |
| `file` | [`ModuleData`](../interfaces/ModuleData) |

#### Returns

[`ILoaderResult`](../#iloaderresult)<`T`\>

#### Implementation of

[ILoaderStrategy](../interfaces/ILoaderStrategy).[load](../interfaces/ILoaderStrategy#load)

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:65](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L65)

___

### onError

▸ **onError**(`error`, `path`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `error` | `Error` |
| `path` | `string` |

#### Returns

`void`

#### Implementation of

[ILoaderStrategy](../interfaces/ILoaderStrategy).[onError](../interfaces/ILoaderStrategy#onerror)

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:104](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L104)

___

### onLoad

▸ **onLoad**(): `unknown`

Called after a piece has been loaded, but before [Piece.onLoad](Piece#onload) and [Store.set](Store#set).

#### Returns

`unknown`

#### Implementation of

[ILoaderStrategy](../interfaces/ILoaderStrategy).[onLoad](../interfaces/ILoaderStrategy#onload)

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:88](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L88)

___

### onLoadAll

▸ **onLoadAll**(): `unknown`

Called after all pieces have been loaded.

#### Returns

`unknown`

#### Implementation of

[ILoaderStrategy](../interfaces/ILoaderStrategy).[onLoadAll](../interfaces/ILoaderStrategy#onloadall)

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:92](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L92)

___

### onUnload

▸ **onUnload**(): `unknown`

Called after a piece has been unloaded or overwritten by a newly loaded piece.

#### Returns

`unknown`

#### Implementation of

[ILoaderStrategy](../interfaces/ILoaderStrategy).[onUnload](../interfaces/ILoaderStrategy#onunload)

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:96](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L96)

___

### onUnloadAll

▸ **onUnloadAll**(): `unknown`

Called after all pieces have been unloaded.

#### Returns

`unknown`

#### Implementation of

[ILoaderStrategy](../interfaces/ILoaderStrategy).[onUnloadAll](../interfaces/ILoaderStrategy#onunloadall)

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:100](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L100)

___

### preload

▸ **preload**(`file`): [`AsyncPreloadResult`](../#asyncpreloadresult)<`T`\>

The pre-load hook, use this to override the loader.

#### Parameters

| Name | Type |
| :------ | :------ |
| `file` | [`ModuleData`](../interfaces/ModuleData) |

#### Returns

[`AsyncPreloadResult`](../#asyncpreloadresult)<`T`\>

#### Implementation of

[ILoaderStrategy](../interfaces/ILoaderStrategy).[preload](../interfaces/ILoaderStrategy#preload)

#### Defined in

[projects/pieces/src/lib/strategies/LoaderStrategy.ts:51](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/LoaderStrategy.ts#L51)

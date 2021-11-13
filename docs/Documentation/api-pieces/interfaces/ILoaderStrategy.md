---
id: "ILoaderStrategy"
title: "Interface: ILoaderStrategy<T>"
sidebar_label: "ILoaderStrategy"
sidebar_position: 0
custom_edit_url: null
---

An abstracted loader strategy interface.

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Piece`](../classes/Piece) |

## Implemented by

- [`LoaderStrategy`](../classes/LoaderStrategy)

## Methods

### filter

▸ **filter**(`path`): [`FilterResult`](../#filterresult)

Retrieves the name and the extension of the specified file path.

**`example`**
```typescript
// ts-node support
class MyStrategy extends LoaderStrategy {
  filter(path) {
    const extension = extname(path);
    if (!['.js', '.ts'].includes(extension)) return null;
    const name = basename(path, extension);
    return { extension, name };
  }
}
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `path` | `string` | The path of the file to be processed. |

#### Returns

[`FilterResult`](../#filterresult)

A [ModuleData](ModuleData) on success, otherwise `null` to stop the store from processing the path.

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:81](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L81)

___

### load

▸ **load**(`store`, `file`): [`ILoaderResult`](../#iloaderresult)<`T`\>

The load hook, use this to override the loader.

**`example`**
```typescript
class MyStrategy extends LoaderStrategy {
  load(store, file) {
    // ...
  }
}
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `store` | [`Store`](../classes/Store)<`T`\> |
| `file` | [`HydratedModuleData`](HydratedModuleData) |

#### Returns

[`ILoaderResult`](../#iloaderresult)<`T`\>

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:117](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L117)

___

### onError

▸ **onError**(`error`, `path`): `void`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `error` | `Error` | The error that was thrown. |
| `path` | `string` | The path of the file that caused the error to be thrown. |

#### Returns

`void`

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:149](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L149)

___

### onLoad

▸ **onLoad**(`store`, `piece`): `unknown`

Called after a piece has been loaded, but before [Piece.onLoad](../classes/Piece#onload) and [Store.set](../classes/Store#set).

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `store` | [`Store`](../classes/Store)<`T`\> | The store that holds the piece. |
| `piece` | `T` | The piece that was loaded. |

#### Returns

`unknown`

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:124](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L124)

___

### onLoadAll

▸ **onLoadAll**(`store`): `unknown`

Called after all pieces have been loaded.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `store` | [`Store`](../classes/Store)<`T`\> | The store that loaded all pieces. |

#### Returns

`unknown`

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:130](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L130)

___

### onUnload

▸ **onUnload**(`store`, `piece`): `unknown`

Called after a piece has been unloaded or overwritten by a newly loaded piece.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `store` | [`Store`](../classes/Store)<`T`\> | The store that held the piece. |
| `piece` | `T` | The piece that was unloaded. |

#### Returns

`unknown`

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:137](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L137)

___

### onUnloadAll

▸ **onUnloadAll**(`store`): `unknown`

Called after all pieces have been unloaded.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `store` | [`Store`](../classes/Store)<`T`\> | The store that unloaded all pieces. |

#### Returns

`unknown`

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:143](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L143)

___

### preload

▸ **preload**(`file`): [`PreloadResult`](../#preloadresult)<`T`\>

The pre-load hook, use this to override the loader.

**`example`**
```typescript
// CommonJS support:
class MyStrategy extends LoaderStrategy {
  preload(path) {
    return require(path);
  }
}
```

**`example`**
```typescript
// ESM support:
class MyStrategy extends LoaderStrategy {
  preload(file) {
    return import(file.path);
  }
}
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `file` | [`ModuleData`](ModuleData) |

#### Returns

[`PreloadResult`](../#preloadresult)<`T`\>

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:104](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L104)

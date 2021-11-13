---
id: "index"
title: "@sapphire/pieces"
slug: "/Documentation/api-pieces/"
sidebar_label: "Exports"
sidebar_position: 0.5
custom_edit_url: null
---

## Namespaces

- [AliasPiece](namespaces/AliasPiece)
- [Piece](namespaces/Piece)

## Enumerations

- [LoaderErrorType](enums/LoaderErrorType)

## Classes

- [AliasPiece](classes/AliasPiece)
- [AliasStore](classes/AliasStore)
- [LoaderError](classes/LoaderError)
- [LoaderStrategy](classes/LoaderStrategy)
- [MissingExportsError](classes/MissingExportsError)
- [Piece](classes/Piece)
- [PieceLocation](classes/PieceLocation)
- [Store](classes/Store)
- [StoreRegistry](classes/StoreRegistry)

## Interfaces

- [AliasPieceJSON](interfaces/AliasPieceJSON)
- [AliasPieceOptions](interfaces/AliasPieceOptions)
- [Container](interfaces/Container)
- [HydratedModuleData](interfaces/HydratedModuleData)
- [ILoaderStrategy](interfaces/ILoaderStrategy)
- [ModuleData](interfaces/ModuleData)
- [PieceContext](interfaces/PieceContext)
- [PieceJSON](interfaces/PieceJSON)
- [PieceLocationJSON](interfaces/PieceLocationJSON)
- [PieceOptions](interfaces/PieceOptions)
- [RootData](interfaces/RootData)
- [StoreLogger](interfaces/StoreLogger)
- [StoreOptions](interfaces/StoreOptions)
- [StoreRegistryEntries](interfaces/StoreRegistryEntries)

## Type aliases

### AsyncPreloadResult

Ƭ **AsyncPreloadResult**<`T`\>: [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Constructor`<`T`\> & `Record`<`PropertyKey`, `unknown`\>\>

Represents the return data from [ILoaderStrategy.preload](interfaces/ILoaderStrategy#preload)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Piece`](classes/Piece) |

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:48](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L48)

___

### FilterResult

Ƭ **FilterResult**: [`ModuleData`](interfaces/ModuleData) \| ``null``

The result from the filter.

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:38](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L38)

___

### ILoaderResult

Ƭ **ILoaderResult**<`T`\>: `AsyncIterableIterator`<[`ILoaderResultEntry`](#iloaderresultentry)<`T`\>\>

Represents the return data from [ILoaderStrategy.load](interfaces/ILoaderStrategy#load).

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Piece`](classes/Piece) |

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:58](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L58)

___

### ILoaderResultEntry

Ƭ **ILoaderResultEntry**<`T`\>: `Ctor`<`ConstructorParameters`<typeof [`Piece`](classes/Piece)\>, `T`\>

Represents an entry from [ILoaderResult](#iloaderresult).

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Piece`](classes/Piece) |

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:53](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L53)

___

### PreloadResult

Ƭ **PreloadResult**<`T`\>: `Awaitable`<`Constructor`<`T`\> & `Record`<`PropertyKey`, `unknown`\>\>

Represents the return data from [ILoaderStrategy.preload](interfaces/ILoaderStrategy#preload)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Piece`](classes/Piece) |

#### Defined in

[projects/pieces/src/lib/strategies/ILoaderStrategy.ts:43](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/strategies/ILoaderStrategy.ts#L43)

## Variables

### container

• **container**: [`Container`](interfaces/Container)

The injected variables that will be accessible to any place. To add an extra property, simply add a property with a
regular assignment, and it will be available in all places simultaneously.

**`example`**
```typescript
// Add a reference to the Client:
import { container } from '@sapphire/pieces';

export class SapphireClient extends Client {
  constructor(options) {
    super(options);

    container.client = this;
  }
}

// Can be placed anywhere in a TypeScript file, for JavaScript projects,
// you can create an `augments.d.ts` and place the code there.
declare module '@sapphire/pieces' {
  interface Container {
    client: SapphireClient;
  }
}

// In any piece, core, plugin, or custom:
export class UserCommand extends Command {
  public run(message, args) {
    // The injected client is available here:
    const { client } = this.container;

    // ...
  }
}
```

**`example`**
```typescript
// In a plugin's context, e.g. API:
class Api extends Plugin {
  static [postInitialization]() {
    const server = new Server(this);
    container.server = server;

    // ...
  }
}

declare module '@sapphire/pieces' {
  interface Container {
    server: Server;
  }
}

// In any piece, even those that aren't routes nor middlewares:
export class UserRoute extends Route {
  public [methods.POST](message, args) {
    // The injected server is available here:
    const { server } = this.container;

    // ...
  }
}
```

#### Defined in

[projects/pieces/src/lib/shared/Container.ts:84](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/shared/Container.ts#L84)

## Functions

### getRootData

▸ **getRootData**(): [`RootData`](interfaces/RootData)

#### Returns

[`RootData`](interfaces/RootData)

#### Defined in

[projects/pieces/src/lib/internal/RootScan.ts:5](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/internal/RootScan.ts#L5)

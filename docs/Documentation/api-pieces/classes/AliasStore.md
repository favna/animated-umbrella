---
id: "AliasStore"
title: "Class: AliasStore<T>"
sidebar_label: "AliasStore"
sidebar_position: 0
custom_edit_url: null
---

The store class which contains [AliasPiece](AliasPiece)s.

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`AliasPiece`](AliasPiece) |

## Hierarchy

- [`Store`](Store)<`T`\>

  ↳ **`AliasStore`**

## Constructors

### constructor

• **new AliasStore**<`T`\>(`constructor`, `options`)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`AliasPiece`](AliasPiece)<[`AliasPieceOptions`](../interfaces/AliasPieceOptions), `T`\> |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `constructor` | `Constructor`<`T`\> | The piece constructor this store loads. |
| `options` | [`StoreOptions`](../interfaces/StoreOptions)<`T`\> | The options for the store. |

#### Inherited from

[Store](Store).[constructor](Store#constructor)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:61](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L61)

## Properties

### Constructor

• `Readonly` **Constructor**: `Constructor`<`T`\>

#### Inherited from

[Store](Store).[Constructor](Store#constructor)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:52](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L52)

___

### [toStringTag]

• `Readonly` **[toStringTag]**: `string`

#### Inherited from

[Store](Store).[[toStringTag]](Store#[tostringtag])

#### Defined in

node_modules/typescript/lib/lib.es2015.symbol.wellknown.d.ts:135

___

### aliases

• `Readonly` **aliases**: `Collection`<`string`, `T`\>

The aliases referencing to pieces.

#### Defined in

[projects/pieces/src/lib/structures/AliasStore.ts:12](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/AliasStore.ts#L12)

___

### constructor

• **constructor**: `CollectionConstructor`

#### Inherited from

Store.constructor

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:17

___

### name

• `Readonly` **name**: `string`

#### Inherited from

[Store](Store).[name](Store#name)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:53](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L53)

___

### paths

• `Readonly` **paths**: [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)<`string`\>

#### Inherited from

[Store](Store).[paths](Store#paths)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:54](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L54)

___

### size

• `Readonly` **size**: `number`

#### Inherited from

[Store](Store).[size](Store#size)

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:28

___

### strategy

• `Readonly` **strategy**: [`ILoaderStrategy`](../interfaces/ILoaderStrategy)<`T`\>

#### Inherited from

[Store](Store).[strategy](Store#strategy)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:55](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L55)

___

### [species]

▪ `Static` `Readonly` **[species]**: `MapConstructor`

#### Inherited from

[Store](Store).[[species]](Store#[species])

#### Defined in

node_modules/typescript/lib/lib.es2015.symbol.wellknown.d.ts:317

___

### default

▪ `Static` `Readonly` **default**: typeof `Collection`

#### Inherited from

[Store](Store).[default](Store#default)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:24

___

### defaultStrategy

▪ `Static` **defaultStrategy**: [`ILoaderStrategy`](../interfaces/ILoaderStrategy)<`any`\>

The default strategy, defaults to [LoaderStrategy](LoaderStrategy), which is constructed on demand when a store is constructed,
when none was set beforehand.

#### Inherited from

[Store](Store).[defaultStrategy](Store#defaultstrategy)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:300](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L300)

___

### logger

▪ `Static` **logger**: ``null`` \| [`StoreLogger`](../interfaces/StoreLogger) = `null`

The default logger, defaults to `null`.

#### Inherited from

[Store](Store).[logger](Store#logger)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:305](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L305)

## Accessors

### container

• `get` **container**(): [`Container`](../interfaces/Container)

A reference to the [Container](../interfaces/Container) object for ease of use.

**`see`** container

#### Returns

[`Container`](../interfaces/Container)

#### Inherited from

Store.container

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:73](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L73)

## Methods

### [iterator]

▸ **[iterator]**(): `IterableIterator`<[`string`, `T`]\>

Returns an iterable of entries in the map.

#### Returns

`IterableIterator`<[`string`, `T`]\>

#### Inherited from

[Store](Store).[[iterator]](Store#[iterator])

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:121

___

### at

▸ **at**(`index?`): `undefined` \| `T`

Identical to [Array.at()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/at).
Returns the item at a given index, allowing for positive and negative integers.
Negative integers count back from the last item in the collection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `index?` | `number` | The index of the element to obtain |

#### Returns

`undefined` \| `T`

#### Inherited from

[Store](Store).[at](Store#at)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:87

___

### clear

▸ **clear**(): `void`

#### Returns

`void`

#### Inherited from

[Store](Store).[clear](Store#clear)

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:22

___

### clone

▸ **clone**(): `Collection`<`string`, `T`\>

Creates an identical shallow copy of this collection.

**`example`**
const newColl = someColl.clone();

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[clone](Store#clone)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:301

___

### concat

▸ **concat**(...`collections`): `Collection`<`string`, `T`\>

Combines this collection with others into a new collection. None of the source collections are modified.

**`example`**
const newColl = someColl.concat(someOtherColl, anotherColl, ohBoyAColl);

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...collections` | `Collection`<`string`, `T`\>[] | Collections to merge |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[concat](Store#concat)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:310

___

### construct

▸ **construct**(`Ctor`, `data`): `T`

Constructs a [Piece](Piece) instance.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `Ctor` | [`ILoaderResultEntry`](../#iloaderresultentry)<`T`\> | The [Piece](Piece)'s constructor used to build the instance. |
| `data` | [`HydratedModuleData`](../interfaces/HydratedModuleData) | The module's information |

#### Returns

`T`

An instance of the constructed piece.

#### Inherited from

[Store](Store).[construct](Store#construct)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:237](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L237)

___

### delete

▸ **delete**(`key`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `string` |

#### Returns

`boolean`

#### Inherited from

[Store](Store).[delete](Store#delete)

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:23

___

### difference

▸ **difference**(`other`): `Collection`<`string`, `T`\>

The difference method returns a new structure containing items where the key is present in one of the original structures but not the other.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `other` | `Collection`<`string`, `T`\> | The other Collection to filter against |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[difference](Store#difference)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:344

___

### each

▸ **each**(`fn`): [`AliasStore`](AliasStore)<`T`\>

Identical to
[Map.forEach()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/forEach),
but returns the collection instead of undefined.

**`example`**
collection
 .each(user => console.log(user.username))
 .filter(user => user.bot)
 .each(user => console.log(user.username));

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `void` | Function to execute for each element |

#### Returns

[`AliasStore`](AliasStore)<`T`\>

#### Inherited from

[Store](Store).[each](Store#each)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:279

▸ **each**<`T`\>(`fn`, `thisArg`): [`AliasStore`](AliasStore)<`T`\>

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `void` |
| `thisArg` | `T` |

#### Returns

[`AliasStore`](AliasStore)<`T`\>

#### Inherited from

[Store](Store).[each](Store#each)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:280

___

### entries

▸ **entries**(): `IterableIterator`<[`string`, `T`]\>

Returns an iterable of key, value pairs for every entry in the map.

#### Returns

`IterableIterator`<[`string`, `T`]\>

#### Inherited from

[Store](Store).[entries](Store#entries)

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:126

___

### equals

▸ **equals**(`collection`): `boolean`

Checks if this collection shares identical items with another.
This is different to checking for equality using equal-signs, because
the collections may be different objects, but contain the same data.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `collection` | `Collection`<`string`, `T`\> | Collection to compare with |

#### Returns

`boolean`

Whether the collections have identical contents

#### Inherited from

[Store](Store).[equals](Store#equals)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:320

___

### every

▸ **every**<`K2`\>(`fn`): this is Collection<K2, T\>

Checks if all items passes a test. Identical in behavior to
[Array.every()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every).

**`example`**
collection.every(user => !user.bot);

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K2` | extends `string` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => key is K2 | Function used to test (should return a boolean) |

#### Returns

this is Collection<K2, T\>

#### Inherited from

[Store](Store).[every](Store#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:247

▸ **every**<`V2`\>(`fn`): this is Collection<string, V2\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V2` | extends [`AliasPiece`](AliasPiece)<[`AliasPieceOptions`](../interfaces/AliasPieceOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => value is V2 |

#### Returns

this is Collection<string, V2\>

#### Inherited from

[Store](Store).[every](Store#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:248

▸ **every**(`fn`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |

#### Returns

`boolean`

#### Inherited from

[Store](Store).[every](Store#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:249

▸ **every**<`This`, `K2`\>(`fn`, `thisArg`): this is Collection<K2, T\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends `string` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => key is K2 |
| `thisArg` | `This` |

#### Returns

this is Collection<K2, T\>

#### Inherited from

[Store](Store).[every](Store#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:250

▸ **every**<`This`, `V2`\>(`fn`, `thisArg`): this is Collection<string, V2\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends [`AliasPiece`](AliasPiece)<[`AliasPieceOptions`](../interfaces/AliasPieceOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => value is V2 |
| `thisArg` | `This` |

#### Returns

this is Collection<string, V2\>

#### Inherited from

[Store](Store).[every](Store#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:251

▸ **every**<`This`\>(`fn`, `thisArg`): `boolean`

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |
| `thisArg` | `This` |

#### Returns

`boolean`

#### Inherited from

[Store](Store).[every](Store#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:252

___

### filter

▸ **filter**<`K2`\>(`fn`): `Collection`<`K2`, `T`\>

Identical to
[Array.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter),
but returns a Collection instead of an Array.

**`example`**
collection.filter(user => user.username === 'Bob');

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K2` | extends `string` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => key is K2 | The function to test with (should return boolean) |

#### Returns

`Collection`<`K2`, `T`\>

#### Inherited from

[Store](Store).[filter](Store#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:167

▸ **filter**<`V2`\>(`fn`): `Collection`<`string`, `V2`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V2` | extends [`AliasPiece`](AliasPiece)<[`AliasPieceOptions`](../interfaces/AliasPieceOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => value is V2 |

#### Returns

`Collection`<`string`, `V2`\>

#### Inherited from

[Store](Store).[filter](Store#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:168

▸ **filter**(`fn`): `Collection`<`string`, `T`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[filter](Store#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:169

▸ **filter**<`This`, `K2`\>(`fn`, `thisArg`): `Collection`<`K2`, `T`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends `string` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => key is K2 |
| `thisArg` | `This` |

#### Returns

`Collection`<`K2`, `T`\>

#### Inherited from

[Store](Store).[filter](Store#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:170

▸ **filter**<`This`, `V2`\>(`fn`, `thisArg`): `Collection`<`string`, `V2`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends [`AliasPiece`](AliasPiece)<[`AliasPieceOptions`](../interfaces/AliasPieceOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => value is V2 |
| `thisArg` | `This` |

#### Returns

`Collection`<`string`, `V2`\>

#### Inherited from

[Store](Store).[filter](Store#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:171

▸ **filter**<`This`\>(`fn`, `thisArg`): `Collection`<`string`, `T`\>

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |
| `thisArg` | `This` |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[filter](Store#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:172

___

### find

▸ **find**<`V2`\>(`fn`): `undefined` \| `V2`

Searches for a single item where the given function returns a truthy value. This behaves like
[Array.find()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find).
<warn>All collections used in Discord.js are mapped using their `id` property, and if you want to find by id you
should use the `get` method. See
[MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/get) for details.</warn>

**`example`**
collection.find(user => user.username === 'Bob');

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V2` | extends [`AliasPiece`](AliasPiece)<[`AliasPieceOptions`](../interfaces/AliasPieceOptions), `V2`\> |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => value is V2 | The function to test with (should return boolean) |

#### Returns

`undefined` \| `V2`

#### Inherited from

[Store](Store).[find](Store#find)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:127

▸ **find**(`fn`): `undefined` \| `T`

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |

#### Returns

`undefined` \| `T`

#### Inherited from

[Store](Store).[find](Store#find)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:128

▸ **find**<`This`, `V2`\>(`fn`, `thisArg`): `undefined` \| `V2`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends [`AliasPiece`](AliasPiece)<[`AliasPieceOptions`](../interfaces/AliasPieceOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => value is V2 |
| `thisArg` | `This` |

#### Returns

`undefined` \| `V2`

#### Inherited from

[Store](Store).[find](Store#find)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:129

▸ **find**<`This`\>(`fn`, `thisArg`): `undefined` \| `T`

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |
| `thisArg` | `This` |

#### Returns

`undefined` \| `T`

#### Inherited from

[Store](Store).[find](Store#find)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:130

___

### findKey

▸ **findKey**<`K2`\>(`fn`): `undefined` \| `K2`

Searches for the key of a single item where the given function returns a truthy value. This behaves like
[Array.findIndex()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex),
but returns the key rather than the positional index.

**`example`**
collection.findKey(user => user.username === 'Bob');

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K2` | extends `string` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => key is K2 | The function to test with (should return boolean) |

#### Returns

`undefined` \| `K2`

#### Inherited from

[Store](Store).[findKey](Store#findkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:142

▸ **findKey**(`fn`): `undefined` \| `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |

#### Returns

`undefined` \| `string`

#### Inherited from

[Store](Store).[findKey](Store#findkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:143

▸ **findKey**<`This`, `K2`\>(`fn`, `thisArg`): `undefined` \| `K2`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends `string` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => key is K2 |
| `thisArg` | `This` |

#### Returns

`undefined` \| `K2`

#### Inherited from

[Store](Store).[findKey](Store#findkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:144

▸ **findKey**<`This`\>(`fn`, `thisArg`): `undefined` \| `string`

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |
| `thisArg` | `This` |

#### Returns

`undefined` \| `string`

#### Inherited from

[Store](Store).[findKey](Store#findkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:145

___

### first

▸ **first**(): `undefined` \| `T`

Obtains the first value(s) in this collection.

#### Returns

`undefined` \| `T`

A single value if no amount is provided or an array of values, starting from the end if amount is negative

#### Inherited from

[Store](Store).[first](Store#first)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:48

▸ **first**(`amount`): `T`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

`T`[]

#### Inherited from

[Store](Store).[first](Store#first)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:49

___

### firstKey

▸ **firstKey**(): `undefined` \| `string`

Obtains the first key(s) in this collection.

#### Returns

`undefined` \| `string`

A single key if no amount is provided or an array of keys, starting from the end if
amount is negative

#### Inherited from

[Store](Store).[firstKey](Store#firstkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:58

▸ **firstKey**(`amount`): `string`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

`string`[]

#### Inherited from

[Store](Store).[firstKey](Store#firstkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:59

___

### flatMap

▸ **flatMap**<`T`\>(`fn`): `Collection`<`string`, `T`\>

Maps each item into a Collection, then joins the results into a single Collection. Identical in behavior to
[Array.flatMap()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/flatMap).

**`example`**
collection.flatMap(guild => guild.members.cache);

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `Collection`<`string`, `T`\> | Function that produces a new Collection |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[flatMap](Store#flatmap)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:199

▸ **flatMap**<`T`, `This`\>(`fn`, `thisArg`): `Collection`<`string`, `T`\>

#### Type parameters

| Name |
| :------ |
| `T` |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `Collection`<`string`, `T`\> |
| `thisArg` | `This` |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[flatMap](Store#flatmap)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:200

___

### forEach

▸ **forEach**(`callbackfn`, `thisArg?`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `callbackfn` | (`value`: `T`, `key`: `string`, `map`: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<`string`, `T`\>) => `void` |
| `thisArg?` | `any` |

#### Returns

`void`

#### Inherited from

[Store](Store).[forEach](Store#foreach)

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:24

___

### get

▸ **get**(`key`): `undefined` \| `T`

Looks up the name by the store, falling back to an alias lookup.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `string` | The key to look for. |

#### Returns

`undefined` \| `T`

#### Overrides

[Store](Store).[get](Store#get)

#### Defined in

[projects/pieces/src/lib/structures/AliasStore.ts:18](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/AliasStore.ts#L18)

___

### has

▸ **has**(`key`): `boolean`

Checks whether a key is in the store, or is an alias

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `string` | The key to check |

#### Returns

`boolean`

#### Overrides

[Store](Store).[has](Store#has)

#### Defined in

[projects/pieces/src/lib/structures/AliasStore.ts:26](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/AliasStore.ts#L26)

___

### hasAll

▸ **hasAll**(...`keys`): `boolean`

Checks if all of the elements exist in the collection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...keys` | `string`[] | The keys of the elements to check for |

#### Returns

`boolean`

`true` if all of the elements exist, `false` if at least one does not exist.

#### Inherited from

[Store](Store).[hasAll](Store#hasall)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:32

___

### hasAny

▸ **hasAny**(...`keys`): `boolean`

Checks if any of the elements exist in the collection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...keys` | `string`[] | The keys of the elements to check for |

#### Returns

`boolean`

`true` if any of the elements exist, `false` if none exist.

#### Inherited from

[Store](Store).[hasAny](Store#hasany)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:40

___

### insert

▸ **insert**(`piece`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

Inserts a piece into the store, and adds all the aliases.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `piece` | `T` | The piece to be inserted into the store. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

The inserted piece.

#### Overrides

[Store](Store).[insert](Store#insert)

#### Defined in

[projects/pieces/src/lib/structures/AliasStore.ts:53](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/AliasStore.ts#L53)

___

### intersect

▸ **intersect**(`other`): `Collection`<`string`, `T`\>

The intersect method returns a new structure containing items where the keys are present in both original structures.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `other` | `Collection`<`string`, `T`\> | The other Collection to filter against |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[intersect](Store#intersect)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:338

___

### keyAt

▸ **keyAt**(`index?`): `undefined` \| `string`

Identical to [Array.at()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/at).
Returns the key at a given index, allowing for positive and negative integers.
Negative integers count back from the last item in the collection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `index?` | `number` | The index of the key to obtain |

#### Returns

`undefined` \| `string`

#### Inherited from

[Store](Store).[keyAt](Store#keyat)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:95

___

### keys

▸ **keys**(): `IterableIterator`<`string`\>

Returns an iterable of keys in the map

#### Returns

`IterableIterator`<`string`\>

#### Inherited from

[Store](Store).[keys](Store#keys)

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:131

___

### last

▸ **last**(): `undefined` \| `T`

Obtains the last value(s) in this collection.

#### Returns

`undefined` \| `T`

A single value if no amount is provided or an array of values, starting from the start if
amount is negative

#### Inherited from

[Store](Store).[last](Store#last)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:68

▸ **last**(`amount`): `T`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

`T`[]

#### Inherited from

[Store](Store).[last](Store#last)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:69

___

### lastKey

▸ **lastKey**(): `undefined` \| `string`

Obtains the last key(s) in this collection.

#### Returns

`undefined` \| `string`

A single key if no amount is provided or an array of keys, starting from the start if
amount is negative

#### Inherited from

[Store](Store).[lastKey](Store#lastkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:78

▸ **lastKey**(`amount`): `string`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

`string`[]

#### Inherited from

[Store](Store).[lastKey](Store#lastkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:79

___

### load

▸ **load**(`root`, `path`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`[]\>

Loads one or more pieces from a path.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `root` | `string` | The root directory the file is from. |
| `path` | `string` | The path of the file to load, relative to the `root`. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`[]\>

All the loaded pieces.

#### Inherited from

[Store](Store).[load](Store#load)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:99](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L99)

___

### loadAll

▸ **loadAll**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Loads all pieces from all directories specified by [paths](AliasStore#paths).

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[Store](Store).[loadAll](Store#loadall)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:154](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L154)

___

### map

▸ **map**<`T`\>(`fn`): `T`[]

Maps each item to another value into an array. Identical in behavior to
[Array.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map).

**`example`**
collection.map(user => user.tag);

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `T` | Function that produces an element of the new array, taking three arguments |

#### Returns

`T`[]

#### Inherited from

[Store](Store).[map](Store#map)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:211

▸ **map**<`This`, `T`\>(`fn`, `thisArg`): `T`[]

#### Type parameters

| Name |
| :------ |
| `This` |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `T` |
| `thisArg` | `This` |

#### Returns

`T`[]

#### Inherited from

[Store](Store).[map](Store#map)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:212

___

### mapValues

▸ **mapValues**<`T`\>(`fn`): `Collection`<`string`, `T`\>

Maps each item to another value into a collection. Identical in behavior to
[Array.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map).

**`example`**
collection.mapValues(user => user.tag);

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `T` | Function that produces an element of the new collection, taking three arguments |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[mapValues](Store#mapvalues)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:223

▸ **mapValues**<`This`, `T`\>(`fn`, `thisArg`): `Collection`<`string`, `T`\>

#### Type parameters

| Name |
| :------ |
| `This` |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `T` |
| `thisArg` | `This` |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[mapValues](Store#mapvalues)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:224

___

### partition

▸ **partition**<`K2`\>(`fn`): [`Collection`<`K2`, `T`\>, `Collection`<`Exclude`<`string`, `K2`\>, `T`\>]

Partitions the collection into two collections where the first collection
contains the items that passed and the second contains the items that failed.

**`example`**
const [big, small] = collection.partition(guild => guild.memberCount > 250);

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K2` | extends `string` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => key is K2 | Function used to test (should return a boolean) |

#### Returns

[`Collection`<`K2`, `T`\>, `Collection`<`Exclude`<`string`, `K2`\>, `T`\>]

#### Inherited from

[Store](Store).[partition](Store#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:183

▸ **partition**<`V2`\>(`fn`): [`Collection`<`string`, `V2`\>, `Collection`<`string`, `Exclude`<`T`, `V2`\>\>]

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V2` | extends [`AliasPiece`](AliasPiece)<[`AliasPieceOptions`](../interfaces/AliasPieceOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => value is V2 |

#### Returns

[`Collection`<`string`, `V2`\>, `Collection`<`string`, `Exclude`<`T`, `V2`\>\>]

#### Inherited from

[Store](Store).[partition](Store#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:184

▸ **partition**(`fn`): [`Collection`<`string`, `T`\>, `Collection`<`string`, `T`\>]

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |

#### Returns

[`Collection`<`string`, `T`\>, `Collection`<`string`, `T`\>]

#### Inherited from

[Store](Store).[partition](Store#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:185

▸ **partition**<`This`, `K2`\>(`fn`, `thisArg`): [`Collection`<`K2`, `T`\>, `Collection`<`Exclude`<`string`, `K2`\>, `T`\>]

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends `string` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => key is K2 |
| `thisArg` | `This` |

#### Returns

[`Collection`<`K2`, `T`\>, `Collection`<`Exclude`<`string`, `K2`\>, `T`\>]

#### Inherited from

[Store](Store).[partition](Store#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:186

▸ **partition**<`This`, `V2`\>(`fn`, `thisArg`): [`Collection`<`string`, `V2`\>, `Collection`<`string`, `Exclude`<`T`, `V2`\>\>]

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends [`AliasPiece`](AliasPiece)<[`AliasPieceOptions`](../interfaces/AliasPieceOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => value is V2 |
| `thisArg` | `This` |

#### Returns

[`Collection`<`string`, `V2`\>, `Collection`<`string`, `Exclude`<`T`, `V2`\>\>]

#### Inherited from

[Store](Store).[partition](Store#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:187

▸ **partition**<`This`\>(`fn`, `thisArg`): [`Collection`<`string`, `T`\>, `Collection`<`string`, `T`\>]

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |
| `thisArg` | `This` |

#### Returns

[`Collection`<`string`, `T`\>, `Collection`<`string`, `T`\>]

#### Inherited from

[Store](Store).[partition](Store#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:188

___

### random

▸ **random**(): `undefined` \| `T`

Obtains unique random value(s) from this collection.

#### Returns

`undefined` \| `T`

A single value if no amount is provided or an array of values

#### Inherited from

[Store](Store).[random](Store#random)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:103

▸ **random**(`amount`): `T`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

`T`[]

#### Inherited from

[Store](Store).[random](Store#random)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:104

___

### randomKey

▸ **randomKey**(): `undefined` \| `string`

Obtains unique random key(s) from this collection.

#### Returns

`undefined` \| `string`

A single key if no amount is provided or an array

#### Inherited from

[Store](Store).[randomKey](Store#randomkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:112

▸ **randomKey**(`amount`): `string`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

`string`[]

#### Inherited from

[Store](Store).[randomKey](Store#randomkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:113

___

### reduce

▸ **reduce**<`T`\>(`fn`, `initialValue?`): `T`

Applies a function to produce a single value. Identical in behavior to
[Array.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce).

**`example`**
collection.reduce((acc, guild) => acc + guild.memberCount, 0);

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`accumulator`: `T`, `value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `T` | Function used to reduce, taking four arguments; `accumulator`, `currentValue`, `currentKey`, and `collection` |
| `initialValue?` | `T` | Starting value for the accumulator |

#### Returns

`T`

#### Inherited from

[Store](Store).[reduce](Store#reduce)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:264

___

### registerPath

▸ **registerPath**(`path`): [`AliasStore`](AliasStore)<`T`\>

Registers a directory into the store.

**`example`**
```typescript
store
  .registerPath(resolve('commands'))
  .registerPath(resolve('third-party', 'commands'));
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `path` | `string` | The path to be added. |

#### Returns

[`AliasStore`](AliasStore)<`T`\>

#### Inherited from

[Store](Store).[registerPath](Store#registerpath)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:87](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L87)

___

### resolve

▸ **resolve**(`name`): `T`

Resolves a piece by its name or its instance.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `name` | `string` \| `T` | The name of the piece or the instance itself. |

#### Returns

`T`

The resolved piece.

#### Inherited from

[Store](Store).[resolve](Store#resolve)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:184](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L184)

___

### set

▸ **set**(`key`, `value`): [`AliasStore`](AliasStore)<`T`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `string` |
| `value` | `T` |

#### Returns

[`AliasStore`](AliasStore)<`T`\>

#### Inherited from

[Store](Store).[set](Store#set)

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:27

___

### some

▸ **some**(`fn`): `boolean`

Checks if there exists an item that passes a test. Identical in behavior to
[Array.some()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some).

**`example`**
collection.some(user => user.discriminator === '0000');

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` | Function used to test (should return a boolean) |

#### Returns

`boolean`

#### Inherited from

[Store](Store).[some](Store#some)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:235

▸ **some**<`T`\>(`fn`, `thisArg`): `boolean`

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |
| `thisArg` | `T` |

#### Returns

`boolean`

#### Inherited from

[Store](Store).[some](Store#some)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:236

___

### sort

▸ **sort**(`compareFunction?`): [`AliasStore`](AliasStore)<`T`\>

The sort method sorts the items of a collection in place and returns it.
The sort is not necessarily stable in Node 10 or older.
The default sort order is according to string Unicode code points.

**`example`**
collection.sort((userA, userB) => userA.createdTimestamp - userB.createdTimestamp);

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `compareFunction?` | `Comparator`<`string`, `T`\> | Specifies a function that defines the sort order. If omitted, the collection is sorted according to each character's Unicode code point value, according to the string conversion of each element. |

#### Returns

[`AliasStore`](AliasStore)<`T`\>

#### Inherited from

[Store](Store).[sort](Store#sort)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:332

___

### sorted

▸ **sorted**(`compareFunction?`): `Collection`<`string`, `T`\>

The sorted method sorts the items of a collection and returns it.
The sort is not necessarily stable in Node 10 or older.
The default sort order is according to string Unicode code points.

**`example`**
collection.sorted((userA, userB) => userA.createdTimestamp - userB.createdTimestamp);

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `compareFunction?` | `Comparator`<`string`, `T`\> | Specifies a function that defines the sort order. If omitted, the collection is sorted according to each character's Unicode code point value, according to the string conversion of each element. |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[Store](Store).[sorted](Store#sorted)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:357

___

### sweep

▸ **sweep**(`fn`): `number`

Removes items that satisfy the provided filter function.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` | Function used to test (should return a boolean) |

#### Returns

`number`

The number of removed entries

#### Inherited from

[Store](Store).[sweep](Store#sweep)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:154

▸ **sweep**<`T`\>(`fn`, `thisArg`): `number`

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `T`, `key`: `string`, `collection`: [`AliasStore`](AliasStore)<`T`\>) => `boolean` |
| `thisArg` | `T` |

#### Returns

`number`

#### Inherited from

[Store](Store).[sweep](Store#sweep)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:155

___

### tap

▸ **tap**(`fn`): [`AliasStore`](AliasStore)<`T`\>

Runs a function on the collection and returns the collection.

**`example`**
collection
 .tap(coll => console.log(coll.size))
 .filter(user => user.bot)
 .tap(coll => console.log(coll.size))

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`collection`: [`AliasStore`](AliasStore)<`T`\>) => `void` | Function to execute |

#### Returns

[`AliasStore`](AliasStore)<`T`\>

#### Inherited from

[Store](Store).[tap](Store#tap)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:293

▸ **tap**<`T`\>(`fn`, `thisArg`): [`AliasStore`](AliasStore)<`T`\>

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`collection`: [`AliasStore`](AliasStore)<`T`\>) => `void` |
| `thisArg` | `T` |

#### Returns

[`AliasStore`](AliasStore)<`T`\>

#### Inherited from

[Store](Store).[tap](Store#tap)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:294

___

### toJSON

▸ **toJSON**(): `T`[]

#### Returns

`T`[]

#### Inherited from

[Store](Store).[toJSON](Store#tojson)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:358

___

### unload

▸ **unload**(`name`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

Unloads a piece given its instance or its name, and removes all the aliases.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `name` | `string` \| `T` | The name of the file to load. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

Returns the piece that was unloaded.

#### Overrides

[Store](Store).[unload](Store#unload)

#### Defined in

[projects/pieces/src/lib/structures/AliasStore.ts:35](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/AliasStore.ts#L35)

___

### unloadAll

▸ **unloadAll**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`[]\>

Unloads all pieces from the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`[]\>

#### Inherited from

[Store](Store).[unloadAll](Store#unloadall)

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:138](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L138)

___

### values

▸ **values**(): `IterableIterator`<`T`\>

Returns an iterable of values in the map

#### Returns

`IterableIterator`<`T`\>

#### Inherited from

[Store](Store).[values](Store#values)

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:136

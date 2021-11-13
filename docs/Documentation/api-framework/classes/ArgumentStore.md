---
id: "ArgumentStore"
title: "Class: ArgumentStore"
sidebar_label: "ArgumentStore"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`AliasStore`](AliasStore)<[`Argument`](Argument)\>

  ↳ **`ArgumentStore`**

## Constructors

### constructor

• **new ArgumentStore**()

#### Overrides

[AliasStore](AliasStore).[constructor](AliasStore#constructor)

#### Defined in

[projects/framework/src/lib/structures/ArgumentStore.ts:5](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/ArgumentStore.ts#L5)

## Properties

### Constructor

• `Readonly` **Constructor**: `Constructor`<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[Constructor](AliasStore#constructor)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:281

___

### [toStringTag]

• `Readonly` **[toStringTag]**: `string`

#### Inherited from

[AliasStore](AliasStore).[[toStringTag]](AliasStore#[tostringtag])

#### Defined in

node_modules/typescript/lib/lib.es2015.symbol.wellknown.d.ts:135

___

### aliases

• `Readonly` **aliases**: `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

The aliases referencing to pieces.

#### Inherited from

[AliasStore](AliasStore).[aliases](AliasStore#aliases)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:692

___

### constructor

• **constructor**: `CollectionConstructor`

#### Inherited from

AliasStore.constructor

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:17

___

### name

• `Readonly` **name**: `string`

#### Inherited from

[AliasStore](AliasStore).[name](AliasStore#name)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:282

___

### paths

• `Readonly` **paths**: [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)<`string`\>

#### Inherited from

[AliasStore](AliasStore).[paths](AliasStore#paths)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:283

___

### size

• `Readonly` **size**: `number`

#### Inherited from

[AliasStore](AliasStore).[size](AliasStore#size)

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:28

___

### strategy

• `Readonly` **strategy**: `ILoaderStrategy`<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[strategy](AliasStore#strategy)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:284

___

### [species]

▪ `Static` `Readonly` **[species]**: `MapConstructor`

#### Inherited from

[AliasStore](AliasStore).[[species]](AliasStore#[species])

#### Defined in

node_modules/typescript/lib/lib.es2015.symbol.wellknown.d.ts:317

___

### default

▪ `Static` `Readonly` **default**: typeof `Collection`

#### Inherited from

[AliasStore](AliasStore).[default](AliasStore#default)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:24

___

### defaultStrategy

▪ `Static` **defaultStrategy**: `ILoaderStrategy`<`any`\>

The default strategy, defaults to {@link LoaderStrategy}, which is constructed on demand when a store is constructed,
when none was set beforehand.

#### Inherited from

[AliasStore](AliasStore).[defaultStrategy](AliasStore#defaultstrategy)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:369

___

### logger

▪ `Static` **logger**: ``null`` \| `StoreLogger`

The default logger, defaults to `null`.

#### Inherited from

[AliasStore](AliasStore).[logger](AliasStore#logger)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:373

## Accessors

### container

• `get` **container**(): `Container`

A reference to the {@link Container} object for ease of use.

**`see`** container

#### Returns

`Container`

#### Inherited from

AliasStore.container

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:294

## Methods

### [iterator]

▸ **[iterator]**(): `IterableIterator`<[`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>]\>

Returns an iterable of entries in the map.

#### Returns

`IterableIterator`<[`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>]\>

#### Inherited from

[AliasStore](AliasStore).[[iterator]](AliasStore#[iterator])

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:121

___

### at

▸ **at**(`index?`): `undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

Identical to [Array.at()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/at).
Returns the item at a given index, allowing for positive and negative integers.
Negative integers count back from the last item in the collection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `index?` | `number` | The index of the element to obtain |

#### Returns

`undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

#### Inherited from

[AliasStore](AliasStore).[at](AliasStore#at)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:87

___

### clear

▸ **clear**(): `void`

#### Returns

`void`

#### Inherited from

[AliasStore](AliasStore).[clear](AliasStore#clear)

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:22

___

### clone

▸ **clone**(): `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

Creates an identical shallow copy of this collection.

**`example`**
const newColl = someColl.clone();

#### Returns

`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[clone](AliasStore#clone)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:301

___

### concat

▸ **concat**(...`collections`): `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

Combines this collection with others into a new collection. None of the source collections are modified.

**`example`**
const newColl = someColl.concat(someOtherColl, anotherColl, ohBoyAColl);

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...collections` | `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>[] | Collections to merge |

#### Returns

`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[concat](AliasStore#concat)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:310

___

### construct

▸ **construct**(`Ctor`, `data`): [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

Constructs a [Piece](Piece) instance.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `Ctor` | `ILoaderResultEntry`<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\> | The [Piece](Piece)'s constructor used to build the instance. |
| `data` | `HydratedModuleData` | The module's information |

#### Returns

[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

An instance of the constructed piece.

#### Inherited from

[AliasStore](AliasStore).[construct](AliasStore#construct)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:345

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

[AliasStore](AliasStore).[delete](AliasStore#delete)

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:23

___

### difference

▸ **difference**(`other`): `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

The difference method returns a new structure containing items where the key is present in one of the original structures but not the other.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `other` | `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\> | The other Collection to filter against |

#### Returns

`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[difference](AliasStore#difference)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:344

___

### each

▸ **each**(`fn`): [`ArgumentStore`](ArgumentStore)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `void` | Function to execute for each element |

#### Returns

[`ArgumentStore`](ArgumentStore)

#### Inherited from

[AliasStore](AliasStore).[each](AliasStore#each)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:279

▸ **each**<`T`\>(`fn`, `thisArg`): [`ArgumentStore`](ArgumentStore)

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `void` |
| `thisArg` | `T` |

#### Returns

[`ArgumentStore`](ArgumentStore)

#### Inherited from

[AliasStore](AliasStore).[each](AliasStore#each)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:280

___

### entries

▸ **entries**(): `IterableIterator`<[`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>]\>

Returns an iterable of key, value pairs for every entry in the map.

#### Returns

`IterableIterator`<[`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>]\>

#### Inherited from

[AliasStore](AliasStore).[entries](AliasStore#entries)

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
| `collection` | `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\> | Collection to compare with |

#### Returns

`boolean`

Whether the collections have identical contents

#### Inherited from

[AliasStore](AliasStore).[equals](AliasStore#equals)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:320

___

### every

▸ **every**<`K2`\>(`fn`): this is Collection<K2, Argument<unknown, ArgumentOptions\>\>

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => key is K2 | Function used to test (should return a boolean) |

#### Returns

this is Collection<K2, Argument<unknown, ArgumentOptions\>\>

#### Inherited from

[AliasStore](AliasStore).[every](AliasStore#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:247

▸ **every**<`V2`\>(`fn`): this is Collection<string, V2\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V2` | extends [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => value is V2 |

#### Returns

this is Collection<string, V2\>

#### Inherited from

[AliasStore](AliasStore).[every](AliasStore#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:248

▸ **every**(`fn`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |

#### Returns

`boolean`

#### Inherited from

[AliasStore](AliasStore).[every](AliasStore#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:249

▸ **every**<`This`, `K2`\>(`fn`, `thisArg`): this is Collection<K2, Argument<unknown, ArgumentOptions\>\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends `string` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => key is K2 |
| `thisArg` | `This` |

#### Returns

this is Collection<K2, Argument<unknown, ArgumentOptions\>\>

#### Inherited from

[AliasStore](AliasStore).[every](AliasStore#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:250

▸ **every**<`This`, `V2`\>(`fn`, `thisArg`): this is Collection<string, V2\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => value is V2 |
| `thisArg` | `This` |

#### Returns

this is Collection<string, V2\>

#### Inherited from

[AliasStore](AliasStore).[every](AliasStore#every)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |
| `thisArg` | `This` |

#### Returns

`boolean`

#### Inherited from

[AliasStore](AliasStore).[every](AliasStore#every)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:252

___

### filter

▸ **filter**<`K2`\>(`fn`): `Collection`<`K2`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => key is K2 | The function to test with (should return boolean) |

#### Returns

`Collection`<`K2`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[filter](AliasStore#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:167

▸ **filter**<`V2`\>(`fn`): `Collection`<`string`, `V2`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V2` | extends [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => value is V2 |

#### Returns

`Collection`<`string`, `V2`\>

#### Inherited from

[AliasStore](AliasStore).[filter](AliasStore#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:168

▸ **filter**(`fn`): `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |

#### Returns

`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[filter](AliasStore#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:169

▸ **filter**<`This`, `K2`\>(`fn`, `thisArg`): `Collection`<`K2`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends `string` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => key is K2 |
| `thisArg` | `This` |

#### Returns

`Collection`<`K2`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[filter](AliasStore#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:170

▸ **filter**<`This`, `V2`\>(`fn`, `thisArg`): `Collection`<`string`, `V2`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => value is V2 |
| `thisArg` | `This` |

#### Returns

`Collection`<`string`, `V2`\>

#### Inherited from

[AliasStore](AliasStore).[filter](AliasStore#filter)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:171

▸ **filter**<`This`\>(`fn`, `thisArg`): `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |
| `thisArg` | `This` |

#### Returns

`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[filter](AliasStore#filter)

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
| `V2` | extends [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions), `V2`\> |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => value is V2 | The function to test with (should return boolean) |

#### Returns

`undefined` \| `V2`

#### Inherited from

[AliasStore](AliasStore).[find](AliasStore#find)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:127

▸ **find**(`fn`): `undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |

#### Returns

`undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

#### Inherited from

[AliasStore](AliasStore).[find](AliasStore#find)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:128

▸ **find**<`This`, `V2`\>(`fn`, `thisArg`): `undefined` \| `V2`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => value is V2 |
| `thisArg` | `This` |

#### Returns

`undefined` \| `V2`

#### Inherited from

[AliasStore](AliasStore).[find](AliasStore#find)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:129

▸ **find**<`This`\>(`fn`, `thisArg`): `undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |
| `thisArg` | `This` |

#### Returns

`undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

#### Inherited from

[AliasStore](AliasStore).[find](AliasStore#find)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => key is K2 | The function to test with (should return boolean) |

#### Returns

`undefined` \| `K2`

#### Inherited from

[AliasStore](AliasStore).[findKey](AliasStore#findkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:142

▸ **findKey**(`fn`): `undefined` \| `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |

#### Returns

`undefined` \| `string`

#### Inherited from

[AliasStore](AliasStore).[findKey](AliasStore#findkey)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => key is K2 |
| `thisArg` | `This` |

#### Returns

`undefined` \| `K2`

#### Inherited from

[AliasStore](AliasStore).[findKey](AliasStore#findkey)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |
| `thisArg` | `This` |

#### Returns

`undefined` \| `string`

#### Inherited from

[AliasStore](AliasStore).[findKey](AliasStore#findkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:145

___

### first

▸ **first**(): `undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

Obtains the first value(s) in this collection.

#### Returns

`undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

A single value if no amount is provided or an array of values, starting from the end if amount is negative

#### Inherited from

[AliasStore](AliasStore).[first](AliasStore#first)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:48

▸ **first**(`amount`): [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]

#### Inherited from

[AliasStore](AliasStore).[first](AliasStore#first)

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

[AliasStore](AliasStore).[firstKey](AliasStore#firstkey)

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

[AliasStore](AliasStore).[firstKey](AliasStore#firstkey)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `Collection`<`string`, `T`\> | Function that produces a new Collection |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[AliasStore](AliasStore).[flatMap](AliasStore#flatmap)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `Collection`<`string`, `T`\> |
| `thisArg` | `This` |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[AliasStore](AliasStore).[flatMap](AliasStore#flatmap)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:200

___

### forEach

▸ **forEach**(`callbackfn`, `thisArg?`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `callbackfn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `map`: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>) => `void` |
| `thisArg?` | `any` |

#### Returns

`void`

#### Inherited from

[AliasStore](AliasStore).[forEach](AliasStore#foreach)

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:24

___

### get

▸ **get**(`key`): `undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

Looks up the name by the store, falling back to an alias lookup.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `string` | The key to look for. |

#### Returns

`undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

#### Inherited from

[AliasStore](AliasStore).[get](AliasStore#get)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:697

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

#### Inherited from

[AliasStore](AliasStore).[has](AliasStore#has)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:702

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

[AliasStore](AliasStore).[hasAll](AliasStore#hasall)

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

[AliasStore](AliasStore).[hasAny](AliasStore#hasany)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:40

___

### insert

▸ **insert**(`piece`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

Inserts a piece into the store, and adds all the aliases.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `piece` | [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\> | The piece to be inserted into the store. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

The inserted piece.

#### Inherited from

[AliasStore](AliasStore).[insert](AliasStore#insert)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:714

___

### intersect

▸ **intersect**(`other`): `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

The intersect method returns a new structure containing items where the keys are present in both original structures.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `other` | `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\> | The other Collection to filter against |

#### Returns

`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[intersect](AliasStore#intersect)

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

[AliasStore](AliasStore).[keyAt](AliasStore#keyat)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:95

___

### keys

▸ **keys**(): `IterableIterator`<`string`\>

Returns an iterable of keys in the map

#### Returns

`IterableIterator`<`string`\>

#### Inherited from

[AliasStore](AliasStore).[keys](AliasStore#keys)

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:131

___

### last

▸ **last**(): `undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

Obtains the last value(s) in this collection.

#### Returns

`undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

A single value if no amount is provided or an array of values, starting from the start if
amount is negative

#### Inherited from

[AliasStore](AliasStore).[last](AliasStore#last)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:68

▸ **last**(`amount`): [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]

#### Inherited from

[AliasStore](AliasStore).[last](AliasStore#last)

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

[AliasStore](AliasStore).[lastKey](AliasStore#lastkey)

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

[AliasStore](AliasStore).[lastKey](AliasStore#lastkey)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:79

___

### load

▸ **load**(`root`, `path`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]\>

Loads one or more pieces from a path.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `root` | `string` | The root directory the file is from. |
| `path` | `string` | The path of the file to load, relative to the `root`. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]\>

All the loaded pieces.

#### Inherited from

[AliasStore](AliasStore).[load](AliasStore#load)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:312

___

### loadAll

▸ **loadAll**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Loads all pieces from all directories specified by [paths](AliasStore#paths).

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[AliasStore](AliasStore).[loadAll](AliasStore#loadall)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:326

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `T` | Function that produces an element of the new array, taking three arguments |

#### Returns

`T`[]

#### Inherited from

[AliasStore](AliasStore).[map](AliasStore#map)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `T` |
| `thisArg` | `This` |

#### Returns

`T`[]

#### Inherited from

[AliasStore](AliasStore).[map](AliasStore#map)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `T` | Function that produces an element of the new collection, taking three arguments |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[AliasStore](AliasStore).[mapValues](AliasStore#mapvalues)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `T` |
| `thisArg` | `This` |

#### Returns

`Collection`<`string`, `T`\>

#### Inherited from

[AliasStore](AliasStore).[mapValues](AliasStore#mapvalues)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:224

___

### partition

▸ **partition**<`K2`\>(`fn`): [`Collection`<`K2`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>, `Collection`<`Exclude`<`string`, `K2`\>, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>]

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => key is K2 | Function used to test (should return a boolean) |

#### Returns

[`Collection`<`K2`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>, `Collection`<`Exclude`<`string`, `K2`\>, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>]

#### Inherited from

[AliasStore](AliasStore).[partition](AliasStore#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:183

▸ **partition**<`V2`\>(`fn`): [`Collection`<`string`, `V2`\>, `Collection`<`string`, `Exclude`<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `V2`\>\>]

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V2` | extends [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => value is V2 |

#### Returns

[`Collection`<`string`, `V2`\>, `Collection`<`string`, `Exclude`<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `V2`\>\>]

#### Inherited from

[AliasStore](AliasStore).[partition](AliasStore#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:184

▸ **partition**(`fn`): [`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>, `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>]

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |

#### Returns

[`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>, `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>]

#### Inherited from

[AliasStore](AliasStore).[partition](AliasStore#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:185

▸ **partition**<`This`, `K2`\>(`fn`, `thisArg`): [`Collection`<`K2`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>, `Collection`<`Exclude`<`string`, `K2`\>, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>]

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends `string` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => key is K2 |
| `thisArg` | `This` |

#### Returns

[`Collection`<`K2`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>, `Collection`<`Exclude`<`string`, `K2`\>, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>]

#### Inherited from

[AliasStore](AliasStore).[partition](AliasStore#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:186

▸ **partition**<`This`, `V2`\>(`fn`, `thisArg`): [`Collection`<`string`, `V2`\>, `Collection`<`string`, `Exclude`<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `V2`\>\>]

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions), `V2`\> |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => value is V2 |
| `thisArg` | `This` |

#### Returns

[`Collection`<`string`, `V2`\>, `Collection`<`string`, `Exclude`<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `V2`\>\>]

#### Inherited from

[AliasStore](AliasStore).[partition](AliasStore#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:187

▸ **partition**<`This`\>(`fn`, `thisArg`): [`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>, `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>]

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |
| `thisArg` | `This` |

#### Returns

[`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>, `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>]

#### Inherited from

[AliasStore](AliasStore).[partition](AliasStore#partition)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:188

___

### random

▸ **random**(): `undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

Obtains unique random value(s) from this collection.

#### Returns

`undefined` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

A single value if no amount is provided or an array of values

#### Inherited from

[AliasStore](AliasStore).[random](AliasStore#random)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:103

▸ **random**(`amount`): [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]

#### Inherited from

[AliasStore](AliasStore).[random](AliasStore#random)

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

[AliasStore](AliasStore).[randomKey](AliasStore#randomkey)

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

[AliasStore](AliasStore).[randomKey](AliasStore#randomkey)

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
| `fn` | (`accumulator`: `T`, `value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `T` | Function used to reduce, taking four arguments; `accumulator`, `currentValue`, `currentKey`, and `collection` |
| `initialValue?` | `T` | Starting value for the accumulator |

#### Returns

`T`

#### Inherited from

[AliasStore](AliasStore).[reduce](AliasStore#reduce)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:264

___

### registerPath

▸ **registerPath**(`path`): [`ArgumentStore`](ArgumentStore)

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

[`ArgumentStore`](ArgumentStore)

#### Inherited from

[AliasStore](AliasStore).[registerPath](AliasStore#registerpath)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:305

___

### resolve

▸ **resolve**(`name`): [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

Resolves a piece by its name or its instance.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `name` | `string` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\> | The name of the piece or the instance itself. |

#### Returns

[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>

The resolved piece.

#### Inherited from

[AliasStore](AliasStore).[resolve](AliasStore#resolve)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:332

___

### set

▸ **set**(`key`, `value`): [`ArgumentStore`](ArgumentStore)

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `string` |
| `value` | [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\> |

#### Returns

[`ArgumentStore`](ArgumentStore)

#### Inherited from

[AliasStore](AliasStore).[set](AliasStore#set)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` | Function used to test (should return a boolean) |

#### Returns

`boolean`

#### Inherited from

[AliasStore](AliasStore).[some](AliasStore#some)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |
| `thisArg` | `T` |

#### Returns

`boolean`

#### Inherited from

[AliasStore](AliasStore).[some](AliasStore#some)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:236

___

### sort

▸ **sort**(`compareFunction?`): [`ArgumentStore`](ArgumentStore)

The sort method sorts the items of a collection in place and returns it.
The sort is not necessarily stable in Node 10 or older.
The default sort order is according to string Unicode code points.

**`example`**
collection.sort((userA, userB) => userA.createdTimestamp - userB.createdTimestamp);

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `compareFunction?` | `Comparator`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\> | Specifies a function that defines the sort order. If omitted, the collection is sorted according to each character's Unicode code point value, according to the string conversion of each element. |

#### Returns

[`ArgumentStore`](ArgumentStore)

#### Inherited from

[AliasStore](AliasStore).[sort](AliasStore#sort)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:332

___

### sorted

▸ **sorted**(`compareFunction?`): `Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

The sorted method sorts the items of a collection and returns it.
The sort is not necessarily stable in Node 10 or older.
The default sort order is according to string Unicode code points.

**`example`**
collection.sorted((userA, userB) => userA.createdTimestamp - userB.createdTimestamp);

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `compareFunction?` | `Comparator`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\> | Specifies a function that defines the sort order. If omitted, the collection is sorted according to each character's Unicode code point value, according to the string conversion of each element. |

#### Returns

`Collection`<`string`, [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[sorted](AliasStore#sorted)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:357

___

### sweep

▸ **sweep**(`fn`): `number`

Removes items that satisfy the provided filter function.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` | Function used to test (should return a boolean) |

#### Returns

`number`

The number of removed entries

#### Inherited from

[AliasStore](AliasStore).[sweep](AliasStore#sweep)

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
| `fn` | (`value`: [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>, `key`: `string`, `collection`: [`ArgumentStore`](ArgumentStore)) => `boolean` |
| `thisArg` | `T` |

#### Returns

`number`

#### Inherited from

[AliasStore](AliasStore).[sweep](AliasStore#sweep)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:155

___

### tap

▸ **tap**(`fn`): [`ArgumentStore`](ArgumentStore)

Runs a function on the collection and returns the collection.

**`example`**
collection
 .tap(coll => console.log(coll.size))
 .filter(user => user.bot)
 .tap(coll => console.log(coll.size))

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`collection`: [`ArgumentStore`](ArgumentStore)) => `void` | Function to execute |

#### Returns

[`ArgumentStore`](ArgumentStore)

#### Inherited from

[AliasStore](AliasStore).[tap](AliasStore#tap)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:293

▸ **tap**<`T`\>(`fn`, `thisArg`): [`ArgumentStore`](ArgumentStore)

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`collection`: [`ArgumentStore`](ArgumentStore)) => `void` |
| `thisArg` | `T` |

#### Returns

[`ArgumentStore`](ArgumentStore)

#### Inherited from

[AliasStore](AliasStore).[tap](AliasStore#tap)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:294

___

### toJSON

▸ **toJSON**(): [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]

#### Returns

[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]

#### Inherited from

[AliasStore](AliasStore).[toJSON](AliasStore#tojson)

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:358

___

### unload

▸ **unload**(`name`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

Unloads a piece given its instance or its name, and removes all the aliases.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `name` | `string` \| [`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\> | The name of the file to load. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

Returns the piece that was unloaded.

#### Inherited from

[AliasStore](AliasStore).[unload](AliasStore#unload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:708

___

### unloadAll

▸ **unloadAll**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]\>

Unloads all pieces from the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>[]\>

#### Inherited from

[AliasStore](AliasStore).[unloadAll](AliasStore#unloadall)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:322

___

### values

▸ **values**(): `IterableIterator`<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

Returns an iterable of values in the map

#### Returns

`IterableIterator`<[`Argument`](Argument)<`unknown`, [`ArgumentOptions`](../interfaces/ArgumentOptions)\>\>

#### Inherited from

[AliasStore](AliasStore).[values](AliasStore#values)

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:136

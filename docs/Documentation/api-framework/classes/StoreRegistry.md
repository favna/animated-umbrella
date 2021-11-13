---
id: "StoreRegistry"
title: "Class: StoreRegistry"
sidebar_label: "StoreRegistry"
sidebar_position: 0
custom_edit_url: null
---

A strict-typed store registry. This is available in [container](AliasPiece#container).

**`since`** 2.1.0

**`example`**
```typescript
// Adding new stores

// Register the store:
container.stores.register(new RouteStore());

// Augment Sapphire to add the new store, in case of a JavaScript
// project, this can be moved to an `Augments.d.ts` (or any other name)
// file somewhere:
declare module '@sapphire/pieces' {
  export interface StoreRegistryEntries {
    routes: RouteStore;
  }
}
```

## Hierarchy

- `Collection`<`Key`, `Value`\>

  ↳ **`StoreRegistry`**

## Constructors

### constructor

• **new StoreRegistry**(`entries?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `entries?` | ``null`` \| readonly readonly [keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`][] |

#### Inherited from

Collection<Key, Value\>.constructor

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:33

• **new StoreRegistry**(`iterable`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `iterable` | `Iterable`<readonly [keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`]\> |

#### Inherited from

Collection<Key, Value\>.constructor

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:160

## Properties

### [toStringTag]

• `Readonly` **[toStringTag]**: `string`

#### Inherited from

Collection.\_\_@toStringTag@332

#### Defined in

node_modules/typescript/lib/lib.es2015.symbol.wellknown.d.ts:135

___

### constructor

• **constructor**: `CollectionConstructor`

#### Inherited from

Collection.constructor

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:17

___

### size

• `Readonly` **size**: `number`

#### Inherited from

Collection.size

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:28

___

### [species]

▪ `Static` `Readonly` **[species]**: `MapConstructor`

#### Inherited from

Collection.\_\_@species@358

#### Defined in

node_modules/typescript/lib/lib.es2015.symbol.wellknown.d.ts:317

___

### default

▪ `Static` `Readonly` **default**: typeof `Collection`

#### Inherited from

Collection.default

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:24

## Methods

### [iterator]

▸ **[iterator]**(): `IterableIterator`<[keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`]\>

Returns an iterable of entries in the map.

#### Returns

`IterableIterator`<[keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`]\>

#### Inherited from

Collection.\_\_@iterator@378

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:121

___

### at

▸ **at**(`index?`): `undefined` \| `Value`

Identical to [Array.at()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/at).
Returns the item at a given index, allowing for positive and negative integers.
Negative integers count back from the last item in the collection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `index?` | `number` | The index of the element to obtain |

#### Returns

`undefined` \| `Value`

#### Inherited from

Collection.at

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:87

___

### clear

▸ **clear**(): `void`

#### Returns

`void`

#### Inherited from

Collection.clear

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:22

___

### clone

▸ **clone**(): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

Creates an identical shallow copy of this collection.

**`example`**
const newColl = someColl.clone();

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

#### Inherited from

Collection.clone

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:301

___

### concat

▸ **concat**(...`collections`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

Combines this collection with others into a new collection. None of the source collections are modified.

**`example`**
const newColl = someColl.concat(someOtherColl, anotherColl, ohBoyAColl);

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...collections` | `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>[] | Collections to merge |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

#### Inherited from

Collection.concat

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:310

___

### delete

▸ **delete**(`key`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Returns

`boolean`

#### Inherited from

Collection.delete

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:23

___

### deregister

▸ **deregister**<`T`\>(`store`): [`StoreRegistry`](StoreRegistry)

Deregisters a store.

**`since`** 2.1.0

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions), `T`\> |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `store` | [`Store`](Store)<`T`\> | The store to deregister. |

#### Returns

[`StoreRegistry`](StoreRegistry)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:540

___

### difference

▸ **difference**(`other`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

The difference method returns a new structure containing items where the key is present in one of the original structures but not the other.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `other` | `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\> | The other Collection to filter against |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

#### Inherited from

Collection.difference

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:344

___

### each

▸ **each**(`fn`): [`StoreRegistry`](StoreRegistry)

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
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `void` | Function to execute for each element |

#### Returns

[`StoreRegistry`](StoreRegistry)

#### Inherited from

Collection.each

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:279

▸ **each**<`T`\>(`fn`, `thisArg`): [`StoreRegistry`](StoreRegistry)

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `void` |
| `thisArg` | `T` |

#### Returns

[`StoreRegistry`](StoreRegistry)

#### Inherited from

Collection.each

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:280

___

### entries

▸ **entries**(): `IterableIterator`<[keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`]\>

Returns an iterable of key, value pairs for every entry in the map.

#### Returns

`IterableIterator`<[keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`]\>

#### Inherited from

Collection.entries

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
| `collection` | `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\> | Collection to compare with |

#### Returns

`boolean`

Whether the collections have identical contents

#### Inherited from

Collection.equals

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:320

___

### every

▸ **every**<`K2`\>(`fn`): this is Collection<K2, Value\>

Checks if all items passes a test. Identical in behavior to
[Array.every()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every).

**`example`**
collection.every(user => !user.bot);

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K2` | extends keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => key is K2 | Function used to test (should return a boolean) |

#### Returns

this is Collection<K2, Value\>

#### Inherited from

Collection.every

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:247

▸ **every**<`V2`\>(`fn`): this is Collection<keyof StoreRegistryEntries, V2\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V2` | extends `Value` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => value is V2 |

#### Returns

this is Collection<keyof StoreRegistryEntries, V2\>

#### Inherited from

Collection.every

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:248

▸ **every**(`fn`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |

#### Returns

`boolean`

#### Inherited from

Collection.every

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:249

▸ **every**<`This`, `K2`\>(`fn`, `thisArg`): this is Collection<K2, Value\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => key is K2 |
| `thisArg` | `This` |

#### Returns

this is Collection<K2, Value\>

#### Inherited from

Collection.every

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:250

▸ **every**<`This`, `V2`\>(`fn`, `thisArg`): this is Collection<keyof StoreRegistryEntries, V2\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends `Value` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => value is V2 |
| `thisArg` | `This` |

#### Returns

this is Collection<keyof StoreRegistryEntries, V2\>

#### Inherited from

Collection.every

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
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |
| `thisArg` | `This` |

#### Returns

`boolean`

#### Inherited from

Collection.every

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:252

___

### filter

▸ **filter**<`K2`\>(`fn`): `Collection`<`K2`, `Value`\>

Identical to
[Array.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter),
but returns a Collection instead of an Array.

**`example`**
collection.filter(user => user.username === 'Bob');

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K2` | extends keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => key is K2 | The function to test with (should return boolean) |

#### Returns

`Collection`<`K2`, `Value`\>

#### Inherited from

Collection.filter

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:167

▸ **filter**<`V2`\>(`fn`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `V2`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V2` | extends `Value` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => value is V2 |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `V2`\>

#### Inherited from

Collection.filter

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:168

▸ **filter**(`fn`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

#### Inherited from

Collection.filter

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:169

▸ **filter**<`This`, `K2`\>(`fn`, `thisArg`): `Collection`<`K2`, `Value`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => key is K2 |
| `thisArg` | `This` |

#### Returns

`Collection`<`K2`, `Value`\>

#### Inherited from

Collection.filter

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:170

▸ **filter**<`This`, `V2`\>(`fn`, `thisArg`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `V2`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends `Value` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => value is V2 |
| `thisArg` | `This` |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `V2`\>

#### Inherited from

Collection.filter

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:171

▸ **filter**<`This`\>(`fn`, `thisArg`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |
| `thisArg` | `This` |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

#### Inherited from

Collection.filter

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
| `V2` | extends `Value` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => value is V2 | The function to test with (should return boolean) |

#### Returns

`undefined` \| `V2`

#### Inherited from

Collection.find

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:127

▸ **find**(`fn`): `undefined` \| `Value`

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |

#### Returns

`undefined` \| `Value`

#### Inherited from

Collection.find

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:128

▸ **find**<`This`, `V2`\>(`fn`, `thisArg`): `undefined` \| `V2`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends `Value` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => value is V2 |
| `thisArg` | `This` |

#### Returns

`undefined` \| `V2`

#### Inherited from

Collection.find

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:129

▸ **find**<`This`\>(`fn`, `thisArg`): `undefined` \| `Value`

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |
| `thisArg` | `This` |

#### Returns

`undefined` \| `Value`

#### Inherited from

Collection.find

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
| `K2` | extends keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => key is K2 | The function to test with (should return boolean) |

#### Returns

`undefined` \| `K2`

#### Inherited from

Collection.findKey

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:142

▸ **findKey**(`fn`): `undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |

#### Returns

`undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

#### Inherited from

Collection.findKey

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:143

▸ **findKey**<`This`, `K2`\>(`fn`, `thisArg`): `undefined` \| `K2`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => key is K2 |
| `thisArg` | `This` |

#### Returns

`undefined` \| `K2`

#### Inherited from

Collection.findKey

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:144

▸ **findKey**<`This`\>(`fn`, `thisArg`): `undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |
| `thisArg` | `This` |

#### Returns

`undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

#### Inherited from

Collection.findKey

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:145

___

### first

▸ **first**(): `undefined` \| `Value`

Obtains the first value(s) in this collection.

#### Returns

`undefined` \| `Value`

A single value if no amount is provided or an array of values, starting from the end if amount is negative

#### Inherited from

Collection.first

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:48

▸ **first**(`amount`): `Value`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

`Value`[]

#### Inherited from

Collection.first

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:49

___

### firstKey

▸ **firstKey**(): `undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

Obtains the first key(s) in this collection.

#### Returns

`undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

A single key if no amount is provided or an array of keys, starting from the end if
amount is negative

#### Inherited from

Collection.firstKey

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:58

▸ **firstKey**(`amount`): keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)[]

#### Inherited from

Collection.firstKey

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:59

___

### flatMap

▸ **flatMap**<`T`\>(`fn`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `T`\>

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
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `T`\> | Function that produces a new Collection |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `T`\>

#### Inherited from

Collection.flatMap

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:199

▸ **flatMap**<`T`, `This`\>(`fn`, `thisArg`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `T`\>

#### Type parameters

| Name |
| :------ |
| `T` |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `T`\> |
| `thisArg` | `This` |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `T`\>

#### Inherited from

Collection.flatMap

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:200

___

### forEach

▸ **forEach**(`callbackfn`, `thisArg?`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `callbackfn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `map`: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>) => `void` |
| `thisArg?` | `any` |

#### Returns

`void`

#### Inherited from

Collection.forEach

#### Defined in

node_modules/typescript/lib/lib.es2015.collection.d.ts:24

___

### get

▸ **get**<`K`\>(`key`): [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)[`K`]

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `K` |

#### Returns

[`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)[`K`]

#### Inherited from

Collection.get

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:543

▸ **get**(`key`): `undefined`

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `string` |

#### Returns

`undefined`

#### Inherited from

Collection.get

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:544

___

### has

▸ **has**(`key`): ``true``

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Returns

``true``

#### Inherited from

Collection.has

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:545

▸ **has**(`key`): ``false``

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `string` |

#### Returns

``false``

#### Inherited from

Collection.has

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:546

___

### hasAll

▸ **hasAll**(...`keys`): `boolean`

Checks if all of the elements exist in the collection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...keys` | keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)[] | The keys of the elements to check for |

#### Returns

`boolean`

`true` if all of the elements exist, `false` if at least one does not exist.

#### Inherited from

Collection.hasAll

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:32

___

### hasAny

▸ **hasAny**(...`keys`): `boolean`

Checks if any of the elements exist in the collection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...keys` | keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)[] | The keys of the elements to check for |

#### Returns

`boolean`

`true` if any of the elements exist, `false` if none exist.

#### Inherited from

Collection.hasAny

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:40

___

### intersect

▸ **intersect**(`other`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

The intersect method returns a new structure containing items where the keys are present in both original structures.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `other` | `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\> | The other Collection to filter against |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

#### Inherited from

Collection.intersect

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:338

___

### keyAt

▸ **keyAt**(`index?`): `undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

Identical to [Array.at()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/at).
Returns the key at a given index, allowing for positive and negative integers.
Negative integers count back from the last item in the collection.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `index?` | `number` | The index of the key to obtain |

#### Returns

`undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

#### Inherited from

Collection.keyAt

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:95

___

### keys

▸ **keys**(): `IterableIterator`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)\>

Returns an iterable of keys in the map

#### Returns

`IterableIterator`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)\>

#### Inherited from

Collection.keys

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:131

___

### last

▸ **last**(): `undefined` \| `Value`

Obtains the last value(s) in this collection.

#### Returns

`undefined` \| `Value`

A single value if no amount is provided or an array of values, starting from the start if
amount is negative

#### Inherited from

Collection.last

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:68

▸ **last**(`amount`): `Value`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

`Value`[]

#### Inherited from

Collection.last

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:69

___

### lastKey

▸ **lastKey**(): `undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

Obtains the last key(s) in this collection.

#### Returns

`undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

A single key if no amount is provided or an array of keys, starting from the start if
amount is negative

#### Inherited from

Collection.lastKey

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:78

▸ **lastKey**(`amount`): keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)[]

#### Inherited from

Collection.lastKey

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:79

___

### load

▸ **load**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Loads all the registered stores.

**`since`** 2.1.0

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:503

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
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `T` | Function that produces an element of the new array, taking three arguments |

#### Returns

`T`[]

#### Inherited from

Collection.map

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
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `T` |
| `thisArg` | `This` |

#### Returns

`T`[]

#### Inherited from

Collection.map

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:212

___

### mapValues

▸ **mapValues**<`T`\>(`fn`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `T`\>

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
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `T` | Function that produces an element of the new collection, taking three arguments |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `T`\>

#### Inherited from

Collection.mapValues

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:223

▸ **mapValues**<`This`, `T`\>(`fn`, `thisArg`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `T`\>

#### Type parameters

| Name |
| :------ |
| `This` |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `T` |
| `thisArg` | `This` |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `T`\>

#### Inherited from

Collection.mapValues

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:224

___

### partition

▸ **partition**<`K2`\>(`fn`): [`Collection`<`K2`, `Value`\>, `Collection`<`Exclude`<``"arguments"``, `K2`\> \| `Exclude`<``"commands"``, `K2`\> \| `Exclude`<``"listeners"``, `K2`\> \| `Exclude`<``"preconditions"``, `K2`\>, `Value`\>]

Partitions the collection into two collections where the first collection
contains the items that passed and the second contains the items that failed.

**`example`**
const [big, small] = collection.partition(guild => guild.memberCount > 250);

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K2` | extends keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => key is K2 | Function used to test (should return a boolean) |

#### Returns

[`Collection`<`K2`, `Value`\>, `Collection`<`Exclude`<``"arguments"``, `K2`\> \| `Exclude`<``"commands"``, `K2`\> \| `Exclude`<``"listeners"``, `K2`\> \| `Exclude`<``"preconditions"``, `K2`\>, `Value`\>]

#### Inherited from

Collection.partition

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:183

▸ **partition**<`V2`\>(`fn`): [`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `V2`\>, `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Exclude`<[`ArgumentStore`](ArgumentStore), `V2`\> \| `Exclude`<[`CommandStore`](CommandStore), `V2`\> \| `Exclude`<[`ListenerStore`](ListenerStore), `V2`\> \| `Exclude`<[`PreconditionStore`](PreconditionStore), `V2`\>\>]

#### Type parameters

| Name | Type |
| :------ | :------ |
| `V2` | extends `Value` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => value is V2 |

#### Returns

[`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `V2`\>, `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Exclude`<[`ArgumentStore`](ArgumentStore), `V2`\> \| `Exclude`<[`CommandStore`](CommandStore), `V2`\> \| `Exclude`<[`ListenerStore`](ListenerStore), `V2`\> \| `Exclude`<[`PreconditionStore`](PreconditionStore), `V2`\>\>]

#### Inherited from

Collection.partition

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:184

▸ **partition**(`fn`): [`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>, `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>]

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |

#### Returns

[`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>, `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>]

#### Inherited from

Collection.partition

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:185

▸ **partition**<`This`, `K2`\>(`fn`, `thisArg`): [`Collection`<`K2`, `Value`\>, `Collection`<`Exclude`<``"arguments"``, `K2`\> \| `Exclude`<``"commands"``, `K2`\> \| `Exclude`<``"listeners"``, `K2`\> \| `Exclude`<``"preconditions"``, `K2`\>, `Value`\>]

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `K2` | extends keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => key is K2 |
| `thisArg` | `This` |

#### Returns

[`Collection`<`K2`, `Value`\>, `Collection`<`Exclude`<``"arguments"``, `K2`\> \| `Exclude`<``"commands"``, `K2`\> \| `Exclude`<``"listeners"``, `K2`\> \| `Exclude`<``"preconditions"``, `K2`\>, `Value`\>]

#### Inherited from

Collection.partition

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:186

▸ **partition**<`This`, `V2`\>(`fn`, `thisArg`): [`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `V2`\>, `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Exclude`<[`ArgumentStore`](ArgumentStore), `V2`\> \| `Exclude`<[`CommandStore`](CommandStore), `V2`\> \| `Exclude`<[`ListenerStore`](ListenerStore), `V2`\> \| `Exclude`<[`PreconditionStore`](PreconditionStore), `V2`\>\>]

#### Type parameters

| Name | Type |
| :------ | :------ |
| `This` | `This` |
| `V2` | extends `Value` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => value is V2 |
| `thisArg` | `This` |

#### Returns

[`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `V2`\>, `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Exclude`<[`ArgumentStore`](ArgumentStore), `V2`\> \| `Exclude`<[`CommandStore`](CommandStore), `V2`\> \| `Exclude`<[`ListenerStore`](ListenerStore), `V2`\> \| `Exclude`<[`PreconditionStore`](PreconditionStore), `V2`\>\>]

#### Inherited from

Collection.partition

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:187

▸ **partition**<`This`\>(`fn`, `thisArg`): [`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>, `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>]

#### Type parameters

| Name |
| :------ |
| `This` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |
| `thisArg` | `This` |

#### Returns

[`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>, `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>]

#### Inherited from

Collection.partition

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:188

___

### random

▸ **random**(): `undefined` \| `Value`

Obtains unique random value(s) from this collection.

#### Returns

`undefined` \| `Value`

A single value if no amount is provided or an array of values

#### Inherited from

Collection.random

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:103

▸ **random**(`amount`): `Value`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

`Value`[]

#### Inherited from

Collection.random

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:104

___

### randomKey

▸ **randomKey**(): `undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

Obtains unique random key(s) from this collection.

#### Returns

`undefined` \| keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)

A single key if no amount is provided or an array

#### Inherited from

Collection.randomKey

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:112

▸ **randomKey**(`amount`): keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `number` |

#### Returns

keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries)[]

#### Inherited from

Collection.randomKey

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
| `fn` | (`accumulator`: `T`, `value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `T` | Function used to reduce, taking four arguments; `accumulator`, `currentValue`, `currentKey`, and `collection` |
| `initialValue?` | `T` | Starting value for the accumulator |

#### Returns

`T`

#### Inherited from

Collection.reduce

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:264

___

### register

▸ **register**<`T`\>(`store`): [`StoreRegistry`](StoreRegistry)

Registers a store.

**`since`** 2.1.0

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions), `T`\> |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `store` | [`Store`](Store)<`T`\> | The store to register. |

#### Returns

[`StoreRegistry`](StoreRegistry)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:534

___

### registerPath

▸ **registerPath**(`rootDirectory?`): `void`

Registers all user directories from the process working directory, the default value is obtained by assuming
CommonJS (high accuracy) but with fallback for ECMAScript Modules (reads package.json's `main` entry, fallbacks
to `process.cwd()`).

By default, if you have this folder structure:
```
/home/me/my-bot
├─ src
│  ├─ commands
│  ├─ events
│  └─ main.js
└─ package.json
```

And you run `node src/main.js`, the directories `/home/me/my-bot/src/commands` and `/home/me/my-bot/src/events` will
be registered for the commands and events stores respectively, since both directories are located in the same
directory as your main file.

**Note**: this also registers directories for all other stores, even if they don't have a folder, this allows you
to create new pieces and hot-load them later anytime.

**`since`** 2.1.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `rootDirectory?` | `string` | The root directory to register pieces at. |

#### Returns

`void`

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:528

___

### set

▸ **set**(`key`, `value`): [`StoreRegistry`](StoreRegistry)

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries) |
| `value` | `Value` |

#### Returns

[`StoreRegistry`](StoreRegistry)

#### Inherited from

Collection.set

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
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` | Function used to test (should return a boolean) |

#### Returns

`boolean`

#### Inherited from

Collection.some

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
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |
| `thisArg` | `T` |

#### Returns

`boolean`

#### Inherited from

Collection.some

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:236

___

### sort

▸ **sort**(`compareFunction?`): [`StoreRegistry`](StoreRegistry)

The sort method sorts the items of a collection in place and returns it.
The sort is not necessarily stable in Node 10 or older.
The default sort order is according to string Unicode code points.

**`example`**
collection.sort((userA, userB) => userA.createdTimestamp - userB.createdTimestamp);

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `compareFunction?` | `Comparator`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\> | Specifies a function that defines the sort order. If omitted, the collection is sorted according to each character's Unicode code point value, according to the string conversion of each element. |

#### Returns

[`StoreRegistry`](StoreRegistry)

#### Inherited from

Collection.sort

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:332

___

### sorted

▸ **sorted**(`compareFunction?`): `Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

The sorted method sorts the items of a collection and returns it.
The sort is not necessarily stable in Node 10 or older.
The default sort order is according to string Unicode code points.

**`example`**
collection.sorted((userA, userB) => userA.createdTimestamp - userB.createdTimestamp);

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `compareFunction?` | `Comparator`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\> | Specifies a function that defines the sort order. If omitted, the collection is sorted according to each character's Unicode code point value, according to the string conversion of each element. |

#### Returns

`Collection`<keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `Value`\>

#### Inherited from

Collection.sorted

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:357

___

### sweep

▸ **sweep**(`fn`): `number`

Removes items that satisfy the provided filter function.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` | Function used to test (should return a boolean) |

#### Returns

`number`

The number of removed entries

#### Inherited from

Collection.sweep

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
| `fn` | (`value`: `Value`, `key`: keyof [`StoreRegistryEntries`](../interfaces/StoreRegistryEntries), `collection`: [`StoreRegistry`](StoreRegistry)) => `boolean` |
| `thisArg` | `T` |

#### Returns

`number`

#### Inherited from

Collection.sweep

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:155

___

### tap

▸ **tap**(`fn`): [`StoreRegistry`](StoreRegistry)

Runs a function on the collection and returns the collection.

**`example`**
collection
 .tap(coll => console.log(coll.size))
 .filter(user => user.bot)
 .tap(coll => console.log(coll.size))

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | (`collection`: [`StoreRegistry`](StoreRegistry)) => `void` | Function to execute |

#### Returns

[`StoreRegistry`](StoreRegistry)

#### Inherited from

Collection.tap

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:293

▸ **tap**<`T`\>(`fn`, `thisArg`): [`StoreRegistry`](StoreRegistry)

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `fn` | (`collection`: [`StoreRegistry`](StoreRegistry)) => `void` |
| `thisArg` | `T` |

#### Returns

[`StoreRegistry`](StoreRegistry)

#### Inherited from

Collection.tap

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:294

___

### toJSON

▸ **toJSON**(): `Value`[]

#### Returns

`Value`[]

#### Inherited from

Collection.toJSON

#### Defined in

node_modules/@discordjs/collection/dist/index.d.ts:358

___

### values

▸ **values**(): `IterableIterator`<`Value`\>

Returns an iterable of values in the map

#### Returns

`IterableIterator`<`Value`\>

#### Inherited from

Collection.values

#### Defined in

node_modules/typescript/lib/lib.es2015.iterable.d.ts:136

---
id: "sapphire_utilities"
title: "Module: @sapphire/utilities"
sidebar_label: "@sapphire/utilities"
sidebar_position: 0
custom_edit_url: null
---

## Interfaces

- [DebounceSettings](../interfaces/sapphire_utilities.DebounceSettings)
- [DebouncedFunc](../interfaces/sapphire_utilities.DebouncedFunc)
- [NonNullObject](../interfaces/sapphire_utilities.NonNullObject)
- [Thenable](../interfaces/sapphire_utilities.Thenable)

## References

### filterNullAndUndefined

Renames and re-exports [filterNullish](sapphire_utilities#filternullish)

___

### filterNullAndUndefinedAndEmpty

Renames and re-exports [filterNullishOrEmpty](sapphire_utilities#filternullishorempty)

___

### filterNullAndUndefinedAndZero

Renames and re-exports [filterNullishOrZero](sapphire_utilities#filternullishorzero)

___

### isNullOrUndefined

Renames and re-exports [isNullish](sapphire_utilities#isnullish)

___

### isNullOrUndefinedOrEmpty

Renames and re-exports [isNullishOrEmpty](sapphire_utilities#isnullishorempty)

___

### isNullOrUndefinedOrZero

Renames and re-exports [isNullishOrZero](sapphire_utilities#isnullishorzero)

## Type aliases

### AbstractConstructor

Ƭ **AbstractConstructor**<`T`\>: (...`args`: `any`[]) => `T`

#### Type parameters

| Name |
| :------ |
| `T` |

#### Type declaration

• (...`args`)

A generic abstract constructor without parameters

##### Parameters

| Name | Type |
| :------ | :------ |
| `...args` | `any`[] |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:64](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L64)

___

### AbstractCtor

Ƭ **AbstractCtor**<`A`, `R`\>: (...`args`: `A`) => `R`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `A` | extends [`Arr`](sapphire_utilities#arr)readonly `any`[] |
| `R` | `any` |

#### Type declaration

• (...`args`)

A generic abstract constructor with parameters

##### Parameters

| Name | Type |
| :------ | :------ |
| `...args` | `A` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:54](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L54)

___

### ArgumentTypes

Ƭ **ArgumentTypes**<`F`\>: `F` extends (...`args`: infer A) => `any` ? `A` : `never`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `F` | extends (...`args`: `any`[]) => `unknown` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:38](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L38)

___

### Arr

Ƭ `Private` **Arr**: readonly `any`[]

A readonly array of any values.

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:44](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L44)

___

### ArrayElementType

Ƭ **ArrayElementType**<`T`\>: `T` extends infer K[] ? `K` : `T` extends readonly infer RK[] ? `RK` : `T`

Gets a union type of all the keys that are in an array.

**`example`**
```typescript
const sample = [1, 2, '3', true];

type arrayUnion = ArrayElementType<typeof sample>;
// Expected: string | number | boolean
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:175](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L175)

___

### Awaitable

Ƭ **Awaitable**<`T`\>: `PromiseLike`<`T`\> \| `T`

ReturnType for a function that can return either a value or a `Promise` with that value

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:79](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L79)

___

### Builtin

Ƭ **Builtin**: [`Primitive`](sapphire_utilities#primitive) \| `Function` \| `Date` \| `Error` \| `RegExp`

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:4](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L4)

___

### Constructor

Ƭ **Constructor**<`T`\>: (...`args`: `any`[]) => `T`

#### Type parameters

| Name |
| :------ |
| `T` |

#### Type declaration

• (...`args`)

A generic constructor without parameters

##### Parameters

| Name | Type |
| :------ | :------ |
| `...args` | `any`[] |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:59](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L59)

___

### Ctor

Ƭ **Ctor**<`A`, `R`\>: (...`args`: `A`) => `R`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `A` | extends [`Arr`](sapphire_utilities#arr)readonly `any`[] |
| `R` | `any` |

#### Type declaration

• (...`args`)

A generic constructor with parameters

##### Parameters

| Name | Type |
| :------ | :------ |
| `...args` | `A` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:49](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L49)

___

### DeepPartial

Ƭ **DeepPartial**<`T`\>: { [P in keyof T]?: T[P] extends infer U[] ? DeepPartial<U\>[] : T[P] extends ReadonlyArray<infer U\> ? ReadonlyArray<DeepPartial<U\>\> : DeepPartial<T[P]\> }

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:30](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L30)

___

### DeepRequired

Ƭ **DeepRequired**<`T`\>: `T` extends [`Builtin`](sapphire_utilities#builtin) ? `NonNullable`<`T`\> : `T` extends [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<infer K, infer V\> ? [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<[`DeepRequired`](sapphire_utilities#deeprequired)<`K`\>, [`DeepRequired`](sapphire_utilities#deeprequired)<`V`\>\> : `T` extends `ReadonlyMap`<infer K, infer V\> ? `ReadonlyMap`<[`DeepRequired`](sapphire_utilities#deeprequired)<`K`\>, [`DeepRequired`](sapphire_utilities#deeprequired)<`V`\>\> : `T` extends [`WeakMap`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)<infer K, infer V\> ? [`WeakMap`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)<[`DeepRequired`](sapphire_utilities#deeprequired)<`K`\>, [`DeepRequired`](sapphire_utilities#deeprequired)<`V`\>\> : `T` extends [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)<infer U\> ? [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)<[`DeepRequired`](sapphire_utilities#deeprequired)<`U`\>\> : `T` extends `ReadonlySet`<infer U\> ? `ReadonlySet`<[`DeepRequired`](sapphire_utilities#deeprequired)<`U`\>\> : `T` extends [`WeakSet`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet)<infer U\> ? [`WeakSet`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet)<[`DeepRequired`](sapphire_utilities#deeprequired)<`U`\>\> : `T` extends [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<infer U\> ? [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`DeepRequired`](sapphire_utilities#deeprequired)<`U`\>\> : `T` extends {} ? { [K in keyof T]-?: DeepRequired<T[K]\> } : `NonNullable`<`T`\>

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:6](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L6)

___

### FirstArgument

Ƭ **FirstArgument**<`T`\>: `T` extends (`arg1`: infer U, ...`args`: `unknown`[]) => `unknown` ? `U` : `unknown`

Gets the first argument of any given function

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:69](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L69)

___

### Mutable

Ƭ **Mutable**<`T`\>: { -readonly [P in keyof T]: T[P] extends unknown[] \| NonNullObject ? Mutable<T[P]\> : T[P] }

Transforms a `readonly` type to be mutable

**`example`**
```typescript
interface Sample {
	id: string;
	hobbies: readonly string[];
}

type BB = Mutable<Sample>;
// Expected:
// {
//    id: string;
//    hobbies: string[];
// }
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:138](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L138)

___

### NonNullableProperties

Ƭ **NonNullableProperties**<`T`\>: { [P in keyof T]: NonNullable<T[P]\> }

Similar to the built in {@link NonNullable}, but properly removes `null` from all keys in the class or interface
This does not recurse deeply, for that use [DeepRequired](sapphire_utilities#deeprequired)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `unknown` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:90](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L90)

___

### Nullish

Ƭ **Nullish**: ``null`` \| `undefined`

Type union for the full 2 billion dollar mistake in the JavaScript ecosystem

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:84](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L84)

___

### PartialRequired

Ƭ **PartialRequired**<`T`, `K`\>: `Partial`<`Omit`<`T`, `K`\>\> & `Required`<`Pick`<`T`, `K`\>\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `T` |
| `K` | extends keyof `T` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:28](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L28)

___

### PickByValue

Ƭ **PickByValue**<`T`, `V`\>: { [P in keyof T]: T[P] extends V ? P : never }[keyof `T`] & keyof `T`

Gets all the keys (as a string union) from a type `T` that match value `V`

**`example`**
```typescript
interface Sample {
	id: string;
	name: string | null;
	middleName?: string;
	lastName: string;
	hobbies: readonly string[];
}

type BB = PickByValue<Sample, string>;
// Expected:
// "id" | "lastName"
```

#### Type parameters

| Name |
| :------ |
| `T` |
| `V` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:116](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L116)

___

### Primitive

Ƭ **Primitive**: `string` \| `number` \| `boolean` \| `bigint` \| `symbol` \| `undefined` \| ``null``

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:1](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L1)

___

### RequiredExcept

Ƭ **RequiredExcept**<`T`, `K`\>: `Partial`<`Pick`<`T`, `K`\>\> & `Required`<`Omit`<`T`, `K`\>\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `T` |
| `K` | extends keyof `T` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:26](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L26)

___

### SecondArgument

Ƭ **SecondArgument**<`T`\>: `T` extends (`arg1`: `unknown`, `arg2`: infer U, ...`args`: `unknown`[]) => `unknown` ? `U` : `unknown`

Gets the second argument of any given function

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:74](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L74)

___

### StrictRequired

Ƭ **StrictRequired**<`T`\>: { [P in keyof T]-?: NonNullable<T[P]\> }

Transforms every key in an object to be strictly required, essentially removing `undefined` and `null` from the type.

**`example`**
```typescript
interface Sample {
	id: string;
	name: string | null;
	middleName?: string;
}

type BB = StrictRequired<Sample>;
// Expected:
// {
//    id: string;
//    name: string;
//    middleName: string;
// }
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[projects/utilities/packages/utilities/src/lib/utilityTypes.ts:161](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/utilityTypes.ts#L161)

## Functions

### arrayStrictEquals

▸ **arrayStrictEquals**<`T`\>(`arr1`, `arr2`): `boolean`

Compare if both arrays are strictly equal

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends readonly `unknown`[] |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `arr1` | `T` | The array to compare to |
| `arr2` | `T` | The array to compare with |

#### Returns

`boolean`

#### Defined in

[projects/utilities/packages/utilities/src/lib/arrayStrictEquals.ts:6](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/arrayStrictEquals.ts#L6)

___

### chunk

▸ **chunk**<`T`\>(`array`, `chunkSize`): `T`[][]

Splits up an array into chunks

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `array` | readonly `T`[] | The array to chunk up |
| `chunkSize` | `number` | The size of each individual chunk |

#### Returns

`T`[][]

#### Defined in

[projects/utilities/packages/utilities/src/lib/chunk.ts:6](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/chunk.ts#L6)

___

### classExtends

▸ **classExtends**<`T`\>(`value`, `base`): value is T

Checks whether or not the value class extends the base class.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Ctor`](sapphire_utilities#ctor)<readonly `any`[], `any`\> |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | [`Ctor`](sapphire_utilities#ctor)<readonly `any`[], `any`\> | The constructor to be checked against. |
| `base` | `T` | The base constructor. |

#### Returns

value is T

#### Defined in

[projects/utilities/packages/utilities/src/lib/classExtends.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/classExtends.ts#L8)

___

### codeBlock

▸ **codeBlock**<`T`\>(`language`, `expression`): `string`

Wraps text in a markdown codeblock with optionally a language indicator for syntax highlighting

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `language` | `string` | The codeblock language |
| `expression` | `T` | The expression to be wrapped in the codeblock |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/utilities/src/lib/codeBlock.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/codeBlock.ts#L8)

___

### cutText

▸ **cutText**(`str`, `length`): `string`

Split a text by its latest space character in a range from the character 0 to the selected one.

**`copyright`** 2019 Antonio Román

**`license`** Apache-2.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `str` | `string` | The text to split. |
| `length` | `number` | The length of the desired string. |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/utilities/src/lib/cutText.ts:10](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/cutText.ts#L10)

___

### debounce

▸ **debounce**<`FnArgumentsType`, `FnReturnType`\>(`func`, `options?`): [`DebouncedFunc`](../interfaces/sapphire_utilities.DebouncedFunc)<`FnArgumentsType`, `FnReturnType`\>

Creates a debounced function that delays invoking func until after wait milliseconds have elapsed since
the last time the debounced function was invoked. The debounced function comes with a cancel method to
cancel delayed invocations and a flush method to immediately invoke them. Provide an options object to
indicate that func should be invoked on the leading and/or trailing edge of the wait timeout. Subsequent
calls to the debounced function return the result of the last func invocation.

Note: If leading and trailing options are true, func is invoked on the trailing edge of the timeout only
if the the debounced function is invoked more than once during the wait timeout.

See David Corbacho’s article for details over the differences between _.debounce and _.throttle.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `FnArgumentsType` | extends `any`[] |
| `FnReturnType` | `FnReturnType` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `func` | (...`args`: `FnArgumentsType`) => `FnReturnType` | The function to debounce. |
| `options` | [`DebounceSettings`](../interfaces/sapphire_utilities.DebounceSettings) | The options object. |

#### Returns

[`DebouncedFunc`](../interfaces/sapphire_utilities.DebouncedFunc)<`FnArgumentsType`, `FnReturnType`\>

Returns the new debounced function.

#### Defined in

[projects/utilities/packages/utilities/src/lib/debounce/index.ts:68](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/debounce/index.ts#L68)

___

### deepClone

▸ **deepClone**<`T`\>(`source`): `T`

Deep clone an object

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `source` | `T` | The object to clone |

#### Returns

`T`

#### Defined in

[projects/utilities/packages/utilities/src/lib/deepClone.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/deepClone.ts#L7)

___

### filterNullish

▸ **filterNullish**<`TValue`\>(`value`): value is TValue

Checks whether a value is not `null` nor `undefined`.
This can be used in {@link Array.filter} to remove `null` and `undefined` from the array type

**`example`**
```typescript
// TypeScript Type: (string | undefined | null)[]
const someArray = ['one', 'two', undefined, null, 'five'];

// TypeScript Type: string[]
const filteredArray = someArray.filter(filterNullAndUndefined);
// Result: ['one', 'two', 'five']
```

#### Type parameters

| Name |
| :------ |
| `TValue` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `TValue` \| [`Nullish`](sapphire_utilities#nullish) | The value to verify that is neither `null` nor `undefined` |

#### Returns

value is TValue

A boolean that is `true` if the value is neither `null` nor `undefined`, false otherwise.

#### Defined in

[projects/utilities/packages/utilities/src/lib/filterNullAndUndefined.ts:19](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/filterNullAndUndefined.ts#L19)

___

### filterNullishOrEmpty

▸ **filterNullishOrEmpty**<`TValue`\>(`value`): value is TValue

Checks whether a value is not `null` nor `undefined` nor `''` (empty string).
This can be used in {@link Array.filter} to remove `null`, `undefined` from the array type

**`example`**
```typescript
// TypeScript Type: (string | undefined | null)[]
const someArray = ['one', 'two', undefined, null, ''];

// TypeScript Type: string[]
const filteredArray = someArray.filter(filterNullAndUndefinedAndEmpty);
// Result: ['one', 'two']
```

#### Type parameters

| Name |
| :------ |
| `TValue` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | ``""`` \| [`Nullish`](sapphire_utilities#nullish) \| `TValue` | The value to verify that is neither `null`, `undefined` nor `''` (empty string) |

#### Returns

value is TValue

A boolean that is `true` if the value is neither `null`, `undefined` nor `''` (empty string), false otherwise.

#### Defined in

[projects/utilities/packages/utilities/src/lib/filterNullAndUndefinedAndEmpty.ts:19](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/filterNullAndUndefinedAndEmpty.ts#L19)

___

### filterNullishOrZero

▸ **filterNullishOrZero**<`TValue`\>(`value`): value is TValue

Checks whether a value is not `null` nor `undefined` nor `0`.
This can be used in {@link Array.filter} to remove `null`, `undefined` from the array type

**`example`**
```typescript
// TypeScript Type: (string | number | undefined | null)[]
const someArray = ['one', 'two', undefined, null, 0, 1];

// TypeScript Type: (string | number)[]
const filteredArray = someArray.filter(filterNullAndUndefinedAndZero);
// Result: ['one', 'two', 1]
```

#### Type parameters

| Name |
| :------ |
| `TValue` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | ``0`` \| [`Nullish`](sapphire_utilities#nullish) \| `TValue` | The value to verify that is neither `null`, `undefined` nor `0` |

#### Returns

value is TValue

A boolean that is `true` if the value is neither `null`, `undefined` nor `0`, false otherwise.

#### Defined in

[projects/utilities/packages/utilities/src/lib/filterNullAndUndefinedAndZero.ts:19](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/filterNullAndUndefinedAndZero.ts#L19)

___

### hasAtLeastOneKeyInMap

▸ **hasAtLeastOneKeyInMap**<`T`\>(`map`, `keys`): `boolean`

Checks whether any of the [keys](../classes/sapphire_ratelimits.RateLimitManager#keys) are in the {@link map}

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `map` | `ReadonlyMap`<`T`, `any`\> | The map to check |
| `keys` | readonly `T`[] | The keys to find in the map |

#### Returns

`boolean`

`true` if at least one of the [keys](../classes/sapphire_ratelimits.RateLimitManager#keys) is in the {@link map}, `false` otherwise.

#### Defined in

[projects/utilities/packages/utilities/src/lib/hasAtLeastOneKeyInMap.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/hasAtLeastOneKeyInMap.ts#L7)

___

### inlineCodeBlock

▸ **inlineCodeBlock**(`input`): `string`

Wraps text in a markdown inline codeblock

#### Parameters

| Name | Type |
| :------ | :------ |
| `input` | `string` |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/utilities/src/lib/inlineCodeBlock.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/inlineCodeBlock.ts#L7)

___

### isClass

▸ **isClass**(`input`): input is Ctor<readonly any[], any\>

Verify if the input is a class constructor.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `input` | `unknown` | The function to verify |

#### Returns

input is Ctor<readonly any[], any\>

#### Defined in

[projects/utilities/packages/utilities/src/lib/isClass.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/isClass.ts#L7)

___

### isFunction

▸ **isFunction**(`input`): input is Function

Verify if the input is a function.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `input` | `unknown` | The function to verify |

#### Returns

input is Function

#### Defined in

[projects/utilities/packages/utilities/src/lib/isFunction.ts:6](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/isFunction.ts#L6)

___

### isNullish

▸ **isNullish**(`value`): value is Nullish

Checks whether or not a value is `null` or `undefined`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `unknown` | The value to check |

#### Returns

value is Nullish

#### Defined in

[projects/utilities/packages/utilities/src/lib/isNullOrUndefined.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/isNullOrUndefined.ts#L7)

___

### isNullishOrEmpty

▸ **isNullishOrEmpty**(`value`): value is "" \| Nullish

Checks whether or not a value is `null`, `undefined` or `''`, `[]`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `unknown` | The value to check |

#### Returns

value is "" \| Nullish

#### Defined in

[projects/utilities/packages/utilities/src/lib/isNullOrUndefinedOrEmpty.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/isNullOrUndefinedOrEmpty.ts#L8)

___

### isNullishOrZero

▸ **isNullishOrZero**(`value`): value is 0 \| Nullish

Checks whether or not a value is `null`, `undefined` or `0`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `unknown` | The value to check |

#### Returns

value is 0 \| Nullish

#### Defined in

[projects/utilities/packages/utilities/src/lib/isNullOrUndefinedOrZero.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/isNullOrUndefinedOrZero.ts#L8)

___

### isNumber

▸ **isNumber**(`input`): input is number

Verify if a number is a finite number.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `input` | `unknown` | The number to verify |

#### Returns

input is number

#### Defined in

[projects/utilities/packages/utilities/src/lib/isNumber.ts:5](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/isNumber.ts#L5)

___

### isObject

▸ **isObject**(`input`): input is object \| Record<PropertyKey, unknown\>

Verify if the input is an object literal (or class).

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `input` | `unknown` | The object to verify |

#### Returns

input is object \| Record<PropertyKey, unknown\>

#### Defined in

[projects/utilities/packages/utilities/src/lib/isObject.ts:6](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/isObject.ts#L6)

___

### isPrimitive

▸ **isPrimitive**(`input`): input is string \| number \| bigint \| boolean

Check whether a value is a primitive

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `input` | `unknown` | The input to check |

#### Returns

input is string \| number \| bigint \| boolean

#### Defined in

[projects/utilities/packages/utilities/src/lib/isPrimitive.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/isPrimitive.ts#L7)

___

### isThenable

▸ **isThenable**(`input`): input is Thenable

Verify if an object is a promise.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `input` | `unknown` | The promise to verify |

#### Returns

input is Thenable

#### Defined in

[projects/utilities/packages/utilities/src/lib/isThenable.ts:21](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/isThenable.ts#L21)

___

### makeObject

▸ **makeObject**(`path`, `value`, `obj?`): `Record`<`string`, `unknown`\>

Turn a dotted path into a json object.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `path` | `string` | The dotted path |
| `value` | `unknown` | The value |
| `obj` | `Record`<`string`, `unknown`\> | The object to edit |

#### Returns

`Record`<`string`, `unknown`\>

#### Defined in

[projects/utilities/packages/utilities/src/lib/makeObject.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/makeObject.ts#L7)

___

### mergeDefault

▸ **mergeDefault**<`A`, `B`\>(`base`, `overwrites?`): [`DeepRequired`](sapphire_utilities#deeprequired)<`A` & `B`\>

Deep merges 2 objects. Properties from the second parameter are applied to the first.

**`remark`** `overwrites` is also mutated!

**`remark`** If the value of a key in `overwrites` is `undefined` then the value of that same key in `base` is used instead!

**`remark`** This is essentially `{ ...base, ...overwrites }` but recursively

**`example`**
```typescript
const base = { a: 0, b: 1 };
const overwrites = {}; // will be { a: 0, b: 1 } after merge
mergeDefault(base, overwrites) // { a: 0, b: 1 }
```

**`example`**
```typescript
const base = { a: 0, b: 1 };
const overwrites = { a: 2, i: 3 };
mergeDefault(base, overwrites) // { a: 2, i: 3, b: 1 };
```

**`example`**
```typescript
const base = { a: 0, b: 1 };
const overwrites = { a: null };
mergeDefault(base, overwrites) // { a: null, b: 1 };
```

**`example`**
```typescript
const base = { a: 0, b: 1 };
const overwrites = { a: undefined };
mergeDefault(base, overwrites) // { a: 0, b: 1 };
```

**`example`**
```typescript
const base = { a: null };
const overwrites = { a: { b: 5 } };
mergeDefault(base, overwrites) // { a: { b: 5 } };
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `A` | extends [`NonNullObject`](../interfaces/sapphire_utilities.NonNullObject) |
| `B` | extends `Partial`<`A`\> |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `base` | `A` | Base object |
| `overwrites?` | `B` | Overwrites to apply |

#### Returns

[`DeepRequired`](sapphire_utilities#deeprequired)<`A` & `B`\>

#### Defined in

[projects/utilities/packages/utilities/src/lib/mergeDefault.ts:43](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/mergeDefault.ts#L43)

___

### mergeObjects

▸ **mergeObjects**<`A`, `B`\>(`objTarget`, `objSource`): `A` & `B`

Merges two objects

#### Type parameters

| Name | Type |
| :------ | :------ |
| `A` | extends `object` |
| `B` | extends `object` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `objTarget` | `A` | The object to be merged |
| `objSource` | `Readonly`<`B`\> | The object to merge |

#### Returns

`A` & `B`

#### Defined in

[projects/utilities/packages/utilities/src/lib/mergeObjects.ts:9](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/mergeObjects.ts#L9)

___

### noop

▸ **noop**(): `void`

#### Returns

`void`

#### Defined in

[projects/utilities/packages/utilities/src/lib/noop.ts:2](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/noop.ts#L2)

___

### objectToTuples

▸ **objectToTuples**(`original`, `prefix?`): [`string`, `unknown`][]

Convert an object to a tuple

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `original` | `Record`<`string`, `unknown`\> | `undefined` | - |
| `prefix` | `string` | `''` | The prefix for the key |

#### Returns

[`string`, `unknown`][]

#### Defined in

[projects/utilities/packages/utilities/src/lib/objectToTuples.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/objectToTuples.ts#L8)

___

### parseURL

▸ **parseURL**(`url`): `URL` \| ``null``

Parses an URL, returns null if invalid.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `url` | `string` | The url to parse |

#### Returns

`URL` \| ``null``

#### Defined in

[projects/utilities/packages/utilities/src/lib/parseUrl.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/parseUrl.ts#L7)

___

### range

▸ **range**(`min`, `max`, `step`): `number`[]

Get an array of numbers with the selected range

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `min` | `number` | The minimum value |
| `max` | `number` | The maximum value |
| `step` | `number` | The step value |

#### Returns

`number`[]

#### Defined in

[projects/utilities/packages/utilities/src/lib/range.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/range.ts#L7)

___

### regExpEsc

▸ **regExpEsc**(`str`): `string`

Cleans a string from regex injection

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `str` | `string` | The string to clean |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/utilities/src/lib/regExpEsc.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/regExpEsc.ts#L8)

___

### roundNumber

▸ **roundNumber**(`num`, `scale?`): `number`

Properly rounds up or down a number.
Also supports strings using an exponent to indicate large or small numbers.

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `num` | `string` \| `number` | `undefined` | The number to round off |
| `scale` | `number` | `0` | The amount of decimals to retain |

#### Returns

`number`

#### Defined in

[projects/utilities/packages/utilities/src/lib/roundNumber.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/roundNumber.ts#L7)

___

### splitText

▸ **splitText**(`str`, `length`, `char?`): `string`

Split a string by its latest space character in a range from the character 0 to the selected one.

**`copyright`** 2019 Antonio Román

**`license`** Apache-2.0

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `str` | `string` | `undefined` | The text to split. |
| `length` | `number` | `undefined` | The length of the desired string. |
| `char` | `string` | `' '` | The character to split with |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/utilities/src/lib/splitText.ts:9](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/splitText.ts#L9)

___

### toTitleCase

▸ **toTitleCase**(`str`): `string`

Converts a string to Title Case

**`description`** This is designed to also ensure common Discord PascalCased strings
				are put in their TitleCase titleCaseVariants. See below for the full list.

**`terms`**
This table lists how certain terms are converted, these are case insensitive.
Any terms not included are converted to regular Titlecase.

     | Term            |    Converted To |
     |-----------------|-----------------|
     | textchannel     |     TextChannel |
     | voicechannel    |    VoiceChannel |
     | categorychannel | CategoryChannel |
     | guildmember     |     GuildMember |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `str` | `string` | The string to title case |

#### Returns

`string`

#### Defined in

[projects/utilities/packages/utilities/src/lib/toTitleCase.ts:26](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/toTitleCase.ts#L26)

___

### tryParse

▸ **tryParse**(`value`): `object` \| `string`

Try parse a stringified JSON string.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `string` | The value to parse |

#### Returns

`object` \| `string`

#### Defined in

[projects/utilities/packages/utilities/src/lib/tryParse.ts:6](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/tryParse.ts#L6)

---
id: "sapphire_utilities.DebouncedFunc"
title: "Interface: DebouncedFunc<FnArgumentsType, FnReturnType>"
sidebar_label: "DebouncedFunc"
custom_edit_url: null
---

[@sapphire/utilities](../modules/sapphire_utilities).DebouncedFunc

## Type parameters

| Name | Type |
| :------ | :------ |
| `FnArgumentsType` | extends `any`[] |
| `FnReturnType` | `FnReturnType` |

## Callable

### DebouncedFunc

▸ **DebouncedFunc**(...`args`): `undefined` \| `FnReturnType`

Call the original function, but applying the debounce rules.

If the debounced function can be run immediately, this calls it and returns its return
value.

Otherwise, it returns the return value of the last invokation, or undefined if the debounced
function was not invoked yet.

#### Parameters

| Name | Type |
| :------ | :------ |
| `...args` | `FnArgumentsType` |

#### Returns

`undefined` \| `FnReturnType`

#### Defined in

[projects/utilities/packages/utilities/src/lib/debounce/index.ts:34](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/debounce/index.ts#L34)

## Methods

### cancel

▸ **cancel**(): `void`

Throw away any pending invokation of the debounced function.

#### Returns

`void`

#### Defined in

[projects/utilities/packages/utilities/src/lib/debounce/index.ts:39](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/debounce/index.ts#L39)

___

### flush

▸ **flush**(): `undefined` \| `FnReturnType`

If there is a pending invokation of the debounced function, invoke it immediately and return
its return value.

Otherwise, return the value from the last invokation, or undefined if the debounced function
was never invoked.

#### Returns

`undefined` \| `FnReturnType`

#### Defined in

[projects/utilities/packages/utilities/src/lib/debounce/index.ts:48](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/utilities/src/lib/debounce/index.ts#L48)

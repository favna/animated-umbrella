---
id: "StoreLogger"
title: "Interface: StoreLogger"
sidebar_label: "StoreLogger"
sidebar_position: 0
custom_edit_url: null
---

## Callable

### StoreLogger

▸ **StoreLogger**(`value`): `void`

An interface representing a logger function.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `string` | The string to print. All strings will be formatted with the format `[STORE => ${name}] [${type}] ${content}`, where the content may have identifiers (values or names of methods) surrounded by `'`. For example:  - `[STORE => commands] [LOAD] Skipped piece '/home/user/bot/src/commands/foo.js' as 'LoaderStrategy#filter' returned 'null'.` - `[STORE => commands] [INSERT] Unloaded new piece 'foo' due to 'enabled' being 'false'.` - `[STORE => commands] [UNLOAD] Unloaded piece 'foo'.` |

#### Returns

`void`

#### Defined in

[projects/pieces/src/lib/structures/Store.ts:45](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/structures/Store.ts#L45)

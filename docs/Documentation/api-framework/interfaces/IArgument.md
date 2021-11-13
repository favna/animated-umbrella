---
id: "IArgument"
title: "Interface: IArgument<T>"
sidebar_label: "IArgument"
sidebar_position: 0
custom_edit_url: null
---

## Type parameters

| Name |
| :------ |
| `T` |

## Implemented by

- [`Argument`](../classes/Argument)

## Properties

### name

• `Readonly` **name**: `string`

The name of the argument, this is used to make the identification of an argument easier.

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:24](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L24)

## Methods

### run

▸ **run**(`parameter`, `context`): [`ArgumentResult`](../#argumentresult)<`T`\>

The method which is called when invoking the argument.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `parameter` | `string` | The string parameter to parse. |
| `context` | [`ArgumentContext`](ArgumentContext)<`T`\> | The context for the method call, contains the message, command, and other options. |

#### Returns

[`ArgumentResult`](../#argumentresult)<`T`\>

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:31](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L31)

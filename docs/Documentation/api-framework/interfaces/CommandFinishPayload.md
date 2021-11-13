---
id: "CommandFinishPayload"
title: "Interface: CommandFinishPayload<T>"
sidebar_label: "CommandFinishPayload"
sidebar_position: 0
custom_edit_url: null
---

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Args`](../classes/Args)[`Args`](../classes/Args) |

## Hierarchy

- [`CommandRunPayload`](CommandRunPayload)<`T`\>

  ↳ **`CommandFinishPayload`**

## Properties

### args

• **args**: `T`

#### Inherited from

[CommandRunPayload](CommandRunPayload).[args](CommandRunPayload#args)

#### Defined in

[projects/framework/src/lib/types/Events.ts:119](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L119)

___

### command

• **command**: [`Command`](../classes/Command)<[`Args`](../classes/Args), [`CommandOptions`](CommandOptions)\>

#### Inherited from

[CommandRunPayload](CommandRunPayload).[command](CommandRunPayload#command)

#### Defined in

[projects/framework/src/lib/types/Events.ts:103](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L103)

___

### context

• **context**: [`CommandContext`](CommandContext)

#### Inherited from

[CommandRunPayload](CommandRunPayload).[context](CommandRunPayload#context)

#### Defined in

[projects/framework/src/lib/types/Events.ts:115](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L115)

___

### message

• **message**: [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

#### Inherited from

[CommandRunPayload](CommandRunPayload).[message](CommandRunPayload#message)

#### Defined in

[projects/framework/src/lib/types/Events.ts:102](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L102)

___

### parameters

• **parameters**: `string`

#### Inherited from

[CommandRunPayload](CommandRunPayload).[parameters](CommandRunPayload#parameters)

#### Defined in

[projects/framework/src/lib/types/Events.ts:114](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L114)

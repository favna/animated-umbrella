---
id: "CommandRunPayload"
title: "Interface: CommandRunPayload<T>"
sidebar_label: "CommandRunPayload"
sidebar_position: 0
custom_edit_url: null
---

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`Args`](../classes/Args)[`Args`](../classes/Args) |

## Hierarchy

- [`CommandAcceptedPayload`](CommandAcceptedPayload)

  ↳ **`CommandRunPayload`**

  ↳↳ [`CommandFinishPayload`](CommandFinishPayload)

  ↳↳ [`CommandErrorPayload`](CommandErrorPayload)

  ↳↳ [`CommandSuccessPayload`](CommandSuccessPayload)

  ↳↳ [`CommandTypingErrorPayload`](CommandTypingErrorPayload)

## Properties

### args

• **args**: `T`

#### Defined in

[projects/framework/src/lib/types/Events.ts:119](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L119)

___

### command

• **command**: [`Command`](../classes/Command)<[`Args`](../classes/Args), [`CommandOptions`](CommandOptions)\>

#### Inherited from

[CommandAcceptedPayload](CommandAcceptedPayload).[command](CommandAcceptedPayload#command)

#### Defined in

[projects/framework/src/lib/types/Events.ts:103](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L103)

___

### context

• **context**: [`CommandContext`](CommandContext)

#### Inherited from

[CommandAcceptedPayload](CommandAcceptedPayload).[context](CommandAcceptedPayload#context)

#### Defined in

[projects/framework/src/lib/types/Events.ts:115](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L115)

___

### message

• **message**: [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

#### Inherited from

[CommandAcceptedPayload](CommandAcceptedPayload).[message](CommandAcceptedPayload#message)

#### Defined in

[projects/framework/src/lib/types/Events.ts:102](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L102)

___

### parameters

• **parameters**: `string`

#### Inherited from

[CommandAcceptedPayload](CommandAcceptedPayload).[parameters](CommandAcceptedPayload#parameters)

#### Defined in

[projects/framework/src/lib/types/Events.ts:114](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L114)

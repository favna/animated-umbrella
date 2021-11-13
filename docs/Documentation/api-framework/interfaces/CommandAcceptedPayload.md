---
id: "CommandAcceptedPayload"
title: "Interface: CommandAcceptedPayload"
sidebar_label: "CommandAcceptedPayload"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`ICommandPayload`](ICommandPayload)

  ↳ **`CommandAcceptedPayload`**

  ↳↳ [`CommandRunPayload`](CommandRunPayload)

## Properties

### command

• **command**: [`Command`](../classes/Command)<[`Args`](../classes/Args), [`CommandOptions`](CommandOptions)\>

#### Inherited from

[ICommandPayload](ICommandPayload).[command](ICommandPayload#command)

#### Defined in

[projects/framework/src/lib/types/Events.ts:103](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L103)

___

### context

• **context**: [`CommandContext`](CommandContext)

#### Defined in

[projects/framework/src/lib/types/Events.ts:115](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L115)

___

### message

• **message**: [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

#### Inherited from

[ICommandPayload](ICommandPayload).[message](ICommandPayload#message)

#### Defined in

[projects/framework/src/lib/types/Events.ts:102](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L102)

___

### parameters

• **parameters**: `string`

#### Defined in

[projects/framework/src/lib/types/Events.ts:114](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L114)

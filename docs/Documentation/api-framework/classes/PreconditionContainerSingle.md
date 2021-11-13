---
id: "PreconditionContainerSingle"
title: "Class: PreconditionContainerSingle"
sidebar_label: "PreconditionContainerSingle"
sidebar_position: 0
custom_edit_url: null
---

An [IPreconditionContainer](../interfaces/IPreconditionContainer) which runs a single precondition from {@link SapphireClient.preconditions}.

**`since`** 1.0.0

## Implements

- [`IPreconditionContainer`](../interfaces/IPreconditionContainer)

## Constructors

### constructor

• **new PreconditionContainerSingle**(`data`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | [`PreconditionSingleResolvable`](../#preconditionsingleresolvable) |

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerSingle.ts:64](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerSingle.ts#L64)

## Properties

### context

• `Readonly` **context**: `Record`<`PropertyKey`, `unknown`\>

The context to be used when calling [Precondition.run](Precondition#run). This will always be an empty object (`{}`) when the
container was constructed with a string, otherwise it is a direct reference to the value from
[PreconditionSingleResolvableDetails.context](../interfaces/PreconditionSingleResolvableDetails#context).

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerSingle.ts:56](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerSingle.ts#L56)

___

### name

• `Readonly` **name**: `string`

The name of the precondition to run.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerSingle.ts:62](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerSingle.ts#L62)

## Methods

### run

▸ **run**(`message`, `command`, `context?`): [`PreconditionResult`](../#preconditionresult)

Runs the container.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> | The message that ran this precondition. |
| `command` | [`Command`](Command)<[`Args`](Args), [`CommandOptions`](../interfaces/CommandOptions)\> | The command the message invoked. |
| `context` | [`PreconditionContext`](../interfaces/PreconditionContext) | - |

#### Returns

[`PreconditionResult`](../#preconditionresult)

#### Implementation of

[IPreconditionContainer](../interfaces/IPreconditionContainer).[run](../interfaces/IPreconditionContainer#run)

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerSingle.ts:80](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerSingle.ts#L80)

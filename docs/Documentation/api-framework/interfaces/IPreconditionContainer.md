---
id: "IPreconditionContainer"
title: "Interface: IPreconditionContainer"
sidebar_label: "IPreconditionContainer"
sidebar_position: 0
custom_edit_url: null
---

An abstracted precondition container to be implemented by classes.

**`since`** 1.0.0

## Implemented by

- [`PreconditionContainerArray`](../classes/PreconditionContainerArray)
- [`PreconditionContainerSingle`](../classes/PreconditionContainerSingle)

## Methods

### run

▸ **run**(`message`, `command`, `context?`): [`PreconditionContainerReturn`](../#preconditioncontainerreturn)

Runs a precondition container.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> | The message that ran this precondition. |
| `command` | [`Command`](../classes/Command)<[`Args`](../classes/Args), [`CommandOptions`](CommandOptions)\> | The command the message invoked. |
| `context?` | [`PreconditionContext`](PreconditionContext) | - |

#### Returns

[`PreconditionContainerReturn`](../#preconditioncontainerreturn)

#### Defined in

[projects/framework/src/lib/utils/preconditions/IPreconditionContainer.ts:37](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/IPreconditionContainer.ts#L37)

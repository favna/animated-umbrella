---
id: "IPreconditionCondition"
title: "Interface: IPreconditionCondition"
sidebar_label: "IPreconditionCondition"
sidebar_position: 0
custom_edit_url: null
---

Defines the condition for [PreconditionContainerArray](../classes/PreconditionContainerArray)s to run.

**`since`** 1.0.0

## Methods

### parallel

▸ **parallel**(`message`, `command`, `entries`, `context`): [`PreconditionContainerReturn`](../#preconditioncontainerreturn)

Runs all the containers using `Promise.all`, then checks the results once all tasks finished running.

**`seealso`** {@link PreconditionRunMode.parallel}

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> | The message that ran this precondition. |
| `command` | [`Command`](../classes/Command)<[`Args`](../classes/Args), [`CommandOptions`](CommandOptions)\> | The command the message invoked. |
| `entries` | readonly [`IPreconditionContainer`](IPreconditionContainer)[] | The containers to run. |
| `context` | [`PreconditionContext`](PreconditionContext) | - |

#### Returns

[`PreconditionContainerReturn`](../#preconditioncontainerreturn)

#### Defined in

[projects/framework/src/lib/utils/preconditions/conditions/IPreconditionCondition.ts:34](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/conditions/IPreconditionCondition.ts#L34)

___

### sequential

▸ **sequential**(`message`, `command`, `entries`, `context`): [`PreconditionContainerReturn`](../#preconditioncontainerreturn)

Runs the containers one by one.

**`seealso`** {@link PreconditionRunMode.sequential}

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> | The message that ran this precondition. |
| `command` | [`Command`](../classes/Command)<[`Args`](../classes/Args), [`CommandOptions`](CommandOptions)\> | The command the message invoked. |
| `entries` | readonly [`IPreconditionContainer`](IPreconditionContainer)[] | The containers to run. |
| `context` | [`PreconditionContext`](PreconditionContext) | - |

#### Returns

[`PreconditionContainerReturn`](../#preconditioncontainerreturn)

#### Defined in

[projects/framework/src/lib/utils/preconditions/conditions/IPreconditionCondition.ts:19](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/conditions/IPreconditionCondition.ts#L19)

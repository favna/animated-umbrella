---
id: "PreconditionSingleResolvableDetails"
title: "Interface: PreconditionSingleResolvableDetails<K>"
sidebar_label: "PreconditionSingleResolvableDetails"
sidebar_position: 0
custom_edit_url: null
---

Defines the detailed options for the [PreconditionContainerSingle](../classes/PreconditionContainerSingle), where both the [PreconditionContext](PreconditionContext) and the
name of the precondition can be defined.

**`since`** 1.0.0

## Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends [`PreconditionKeys`](../#preconditionkeys)[`PreconditionKeys`](../#preconditionkeys) |

## Implemented by

- [`ClientPermissionsPrecondition`](../classes/ClientPermissionsPrecondition)
- [`UserPermissionsPrecondition`](../classes/UserPermissionsPrecondition)

## Properties

### context

• **context**: [`Preconditions`](Preconditions)[`K`]

The context to be set at [PreconditionContainerSingle.context](../classes/PreconditionContainerSingle#context).

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerSingle.ts:36](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerSingle.ts#L36)

___

### name

• **name**: `K`

The name of the precondition to retrieve from {@link SapphireClient.preconditions}.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerSingle.ts:30](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerSingle.ts#L30)

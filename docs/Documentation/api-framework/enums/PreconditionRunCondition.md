---
id: "PreconditionRunCondition"
title: "Enumeration: PreconditionRunCondition"
sidebar_label: "PreconditionRunCondition"
sidebar_position: 0
custom_edit_url: null
---

The condition for a [PreconditionContainerArray](../classes/PreconditionContainerArray).

## Enumeration members

### And

• **And** = `0`

Defines a condition where all the entries must pass. This uses [PreconditionConditionAnd](../#preconditionconditionand).

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:43](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L43)

___

### Or

• **Or** = `1`

Defines a condition where at least one entry must pass. This uses [PreconditionConditionOr](../#preconditionconditionor).

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:49](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L49)

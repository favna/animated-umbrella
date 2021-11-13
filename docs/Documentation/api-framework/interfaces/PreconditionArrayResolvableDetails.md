---
id: "PreconditionArrayResolvableDetails"
title: "Interface: PreconditionArrayResolvableDetails"
sidebar_label: "PreconditionArrayResolvableDetails"
sidebar_position: 0
custom_edit_url: null
---

Defines the detailed options for the [PreconditionContainerArray](../classes/PreconditionContainerArray), where both the [PreconditionRunMode](../enums/PreconditionRunMode) and the
entries can be defined.

**`since`** 1.0.0

## Properties

### entries

• **entries**: readonly [`PreconditionEntryResolvable`](../#preconditionentryresolvable)[]

The data that will be used to resolve [IPreconditionContainer](IPreconditionContainer) dependent of this one.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:62](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L62)

___

### mode

• **mode**: [`PreconditionRunMode`](../enums/PreconditionRunMode)

The mode the [PreconditionContainerArray](../classes/PreconditionContainerArray) will run.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:68](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L68)

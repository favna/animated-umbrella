---
id: "PreconditionRunMode"
title: "Enumeration: PreconditionRunMode"
sidebar_label: "PreconditionRunMode"
sidebar_position: 0
custom_edit_url: null
---

The run mode for a [PreconditionContainerArray](../classes/PreconditionContainerArray).

**`since`** 1.0.0

## Enumeration members

### Parallel

• **Parallel** = `1`

All entries are run in parallel using `Promise.all`, then the results are processed after all of them have
completed.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:32](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L32)

___

### Sequential

• **Sequential** = `0`

The entries are run sequentially, this is the default behaviour and can be slow when doing long asynchronous
tasks, but is performance savvy.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:25](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L25)

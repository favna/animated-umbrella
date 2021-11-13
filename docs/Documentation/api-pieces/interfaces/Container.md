---
id: "Container"
title: "Interface: Container"
sidebar_label: "Container"
sidebar_position: 0
custom_edit_url: null
---

Represents the type of the properties injected into the container, which is available at [container](../#container).

Because Sapphire works as a standalone framework (independent of external libraries), there is a need to pass data
from one place to another, which would vary depending on the user and their use-cases.

Furthermore, plugins may use this structure to add properties referencing to the plugin's objects so they can be
accessed by both the user and the plugin at any moment and at any place.

Finally, both library developers and bot developers should augment the Container interface from this module using
[module augmentation](https://www.typescriptlang.org/docs/handbook/declaration-merging.html#module-augmentation).

## Properties

### stores

• **stores**: [`StoreRegistry`](../classes/StoreRegistry)

#### Defined in

[projects/pieces/src/lib/shared/Container.ts:16](https://github.com/sapphiredev/pieces/blob/04481a2/src/lib/shared/Container.ts#L16)

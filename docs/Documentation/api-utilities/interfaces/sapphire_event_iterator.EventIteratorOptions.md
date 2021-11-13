---
id: "sapphire_event_iterator.EventIteratorOptions"
title: "Interface: EventIteratorOptions<V>"
sidebar_label: "EventIteratorOptions"
custom_edit_url: null
---

[@sapphire/event-iterator](../modules/sapphire_event_iterator).EventIteratorOptions

Options to be passed to an EventIterator.

## Type parameters

| Name |
| :------ |
| `V` |

## Properties

### filter

• `Optional` **filter**: [`EventIteratorFilter`](../modules/sapphire_event_iterator#eventiteratorfilter)<`V`\>

The filter.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:16](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L16)

___

### idle

• `Optional` **idle**: `number`

The timeout in ms before ending the EventIterator.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:21](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L21)

___

### limit

• `Optional` **limit**: `number`

The limit of events that pass the filter to iterate.

#### Defined in

[projects/utilities/packages/event-iterator/src/index.ts:26](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/event-iterator/src/index.ts#L26)

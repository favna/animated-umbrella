---
id: "sapphire_discord_js_utilities.PaginatedMessageAction"
title: "Interface: PaginatedMessageAction"
sidebar_label: "PaginatedMessageAction"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).PaginatedMessageAction

To utilize actions you can use the [PaginatedMessageAction](sapphire_discord_js_utilities.PaginatedMessageAction) by implementing it into a class.

**`example`**
```typescript
class ForwardAction implements IPaginatedMessageAction {
  public id = '▶️';

  public run({ handler }) {
    if (handler.index !== handler.pages.length - 1) ++handler.index;
  }
}

// You can also give the object directly.

const StopAction: IPaginatedMessageAction {
  customId: 'CustomStopAction',
  emoji: '⏹️',
  run: ({ collector }) => {
    collector.stop();
  }
}
```

## Hierarchy

- `Omit`<`InteractionButtonOptions`, ``"customId"`` \| ``"style"``\>

- `Omit`<`MessageSelectMenuOptions`, ``"customId"``\>

  ↳ **`PaginatedMessageAction`**

## Properties

### customId

• **customId**: `string`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:48](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L48)

___

### disabled

• `Optional` **disabled**: `boolean`

#### Inherited from

Omit.disabled

#### Defined in

node_modules/discord.js/typings/index.d.ts:4460

___

### emoji

• `Optional` **emoji**: `EmojiIdentifierResolvable`

#### Inherited from

Omit.emoji

#### Defined in

node_modules/discord.js/typings/index.d.ts:4461

___

### label

• `Optional` **label**: `string`

#### Inherited from

Omit.label

#### Defined in

node_modules/discord.js/typings/index.d.ts:4462

___

### maxValues

• `Optional` **maxValues**: `number`

#### Inherited from

Omit.maxValues

#### Defined in

node_modules/discord.js/typings/index.d.ts:4641

___

### minValues

• `Optional` **minValues**: `number`

#### Inherited from

Omit.minValues

#### Defined in

node_modules/discord.js/typings/index.d.ts:4642

___

### options

• `Optional` **options**: `MessageSelectOptionData`[]

#### Inherited from

Omit.options

#### Defined in

node_modules/discord.js/typings/index.d.ts:4643

___

### placeholder

• `Optional` **placeholder**: `string`

#### Inherited from

Omit.placeholder

#### Defined in

node_modules/discord.js/typings/index.d.ts:4644

___

### style

• `Optional` **style**: `ExcludeEnum`<typeof `MessageButtonStyles`, ``"LINK"``\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:50](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L50)

___

### type

• **type**: `MessageComponentTypes`

#### Overrides

Omit.type

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:49](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L49)

## Methods

### run

▸ **run**(`context`): `unknown`

#### Parameters

| Name | Type |
| :------ | :------ |
| `context` | [`PaginatedMessageActionContext`](sapphire_discord_js_utilities.PaginatedMessageActionContext) |

#### Returns

`unknown`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:51](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L51)

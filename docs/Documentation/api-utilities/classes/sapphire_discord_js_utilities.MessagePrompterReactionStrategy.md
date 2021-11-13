---
id: "sapphire_discord_js_utilities.MessagePrompterReactionStrategy"
title: "Class: MessagePrompterReactionStrategy"
sidebar_label: "MessagePrompterReactionStrategy"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).MessagePrompterReactionStrategy

## Hierarchy

- [`MessagePrompterBaseStrategy`](sapphire_discord_js_utilities.MessagePrompterBaseStrategy)

  ↳ **`MessagePrompterReactionStrategy`**

## Implements

- [`MessagePrompterReactionStrategy`](sapphire_discord_js_utilities.MessagePrompterReactionStrategy)

## Implemented by

- [`MessagePrompterReactionStrategy`](sapphire_discord_js_utilities.MessagePrompterReactionStrategy)

## Constructors

### constructor

• **new MessagePrompterReactionStrategy**(`message`, `options`)

Constructor for the [MessagePrompterReactionStrategy](sapphire_discord_js_utilities.MessagePrompterReactionStrategy) class

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | `string` \| `MessageOptions` \| [`MessagePayload`](https://discord.js.org/#/docs/main/stable/class/MessagePayload) | - |
| `options` | [`IMessagePrompterReactionStrategyOptions`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterReactionStrategyOptions) | Overrideable options if needed. |

#### Overrides

MessagePrompterBaseStrategy.constructor

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterReactionStrategy.ts:18](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterReactionStrategy.ts#L18)

## Properties

### appliedMessage

• **appliedMessage**: ``null`` \| [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> = `null`

The message that has been sent in [MessagePrompter.run](sapphire_discord_js_utilities.MessagePrompter#run)

#### Implementation of

MessagePrompterReactionStrategy.appliedMessage

#### Inherited from

MessagePrompterBaseStrategy.appliedMessage

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:27](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L27)

___

### editMessage

• **editMessage**: `undefined` \| [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

The message the bot will edit to send its prompt in [MessagePrompter.run](sapphire_discord_js_utilities.MessagePrompter#run)

#### Implementation of

MessagePrompterReactionStrategy.editMessage

#### Inherited from

MessagePrompterBaseStrategy.editMessage

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:37](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L37)

___

### explicitReturn

• **explicitReturn**: `boolean`

Whether to return an explicit object with data, or the strategies' default

#### Implementation of

MessagePrompterReactionStrategy.explicitReturn

#### Inherited from

MessagePrompterBaseStrategy.explicitReturn

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:22](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L22)

___

### message

• **message**: `string` \| `MessageOptions` \| [`MessagePayload`](https://discord.js.org/#/docs/main/stable/class/MessagePayload)

The message that will be sent in [MessagePrompter.run](sapphire_discord_js_utilities.MessagePrompter#run)

#### Implementation of

MessagePrompterReactionStrategy.message

#### Inherited from

MessagePrompterBaseStrategy.message

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:32](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L32)

___

### reactions

• **reactions**: `EmojiIdentifierResolvable`[]

The emojis used

#### Implementation of

MessagePrompterReactionStrategy.reactions

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterReactionStrategy.ts:11](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterReactionStrategy.ts#L11)

___

### timeout

• **timeout**: `number`

The timeout that was used in the collector

#### Implementation of

MessagePrompterReactionStrategy.timeout

#### Inherited from

MessagePrompterBaseStrategy.timeout

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L17)

___

### type

• **type**: `string`

The type of strategy that was used

#### Implementation of

MessagePrompterReactionStrategy.type

#### Inherited from

MessagePrompterBaseStrategy.type

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:12](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L12)

___

### defaultStrategyOptions

▪ `Static` **defaultStrategyOptions**: [`IMessagePrompterStrategyOptions`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions)

The default strategy options

#### Inherited from

MessagePrompterBaseStrategy.defaultStrategyOptions

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:128](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L128)

## Methods

### collectReactions

▸ `Protected` **collectReactions**(`channel`, `authorOrFilter`, `reactions`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`IMessagePrompterExplicitReturnBase`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitReturnBase)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `channel` | [`MessagePrompterChannelTypes`](../modules/sapphire_discord_js_utilities#messageprompterchanneltypes) |
| `authorOrFilter` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) \| [`CollectorFilter`](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter)<[[`MessageReaction`](https://discord.js.org/#/docs/main/stable/class/MessageReaction), [`User`](https://discord.js.org/#/docs/main/stable/class/User)]\> |
| `reactions` | `string`[] \| `EmojiIdentifierResolvable`[] |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`IMessagePrompterExplicitReturnBase`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitReturnBase)\>

#### Implementation of

MessagePrompterReactionStrategy.collectReactions

#### Inherited from

MessagePrompterBaseStrategy.collectReactions

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:54](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L54)

___

### createReactionPromptFilter

▸ `Protected` **createReactionPromptFilter**(`reactions`, `authorOrFilter`): [`CollectorOptions`](https://discord.js.org/#/docs/main/stable/typedef/CollectorOptions)<[[`MessageReaction`](https://discord.js.org/#/docs/main/stable/class/MessageReaction), [`User`](https://discord.js.org/#/docs/main/stable/class/User)]\>

Creates a filter for the collector to filter on

#### Parameters

| Name | Type |
| :------ | :------ |
| `reactions` | `string`[] \| `EmojiIdentifierResolvable`[] |
| `authorOrFilter` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) \| [`CollectorFilter`](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter)<[[`MessageReaction`](https://discord.js.org/#/docs/main/stable/class/MessageReaction), [`User`](https://discord.js.org/#/docs/main/stable/class/User)]\> |

#### Returns

[`CollectorOptions`](https://discord.js.org/#/docs/main/stable/typedef/CollectorOptions)<[[`MessageReaction`](https://discord.js.org/#/docs/main/stable/class/MessageReaction), [`User`](https://discord.js.org/#/docs/main/stable/class/User)]\>

The filter for awaitReactions function

#### Implementation of

MessagePrompterReactionStrategy.createReactionPromptFilter

#### Inherited from

MessagePrompterBaseStrategy.createReactionPromptFilter

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:113](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L113)

___

### run

▸ **run**(`channel`, `authorOrFilter`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`IMessagePrompterExplicitReturnBase`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitReturnBase) \| `EmojiResolvable`\>

This executes the [MessagePrompterReactionStrategy](sapphire_discord_js_utilities.MessagePrompterReactionStrategy) and sends the message.
The handler will wait for one (1) reaction.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`MessagePrompterChannelTypes`](../modules/sapphire_discord_js_utilities#messageprompterchanneltypes) | The channel to use. |
| `authorOrFilter` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) \| [`CollectorFilter`](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter)<[[`MessageReaction`](https://discord.js.org/#/docs/main/stable/class/MessageReaction), [`User`](https://discord.js.org/#/docs/main/stable/class/User)]\> | An author object to validate or a [CollectorFilter](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter) predicate callback. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`IMessagePrompterExplicitReturnBase`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitReturnBase) \| `EmojiResolvable`\>

A promise that resolves to the reaction object.

#### Implementation of

MessagePrompterReactionStrategy.run

#### Overrides

MessagePrompterBaseStrategy.run

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterReactionStrategy.ts:31](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterReactionStrategy.ts#L31)

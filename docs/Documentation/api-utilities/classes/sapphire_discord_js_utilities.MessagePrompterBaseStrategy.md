---
id: "sapphire_discord_js_utilities.MessagePrompterBaseStrategy"
title: "Class: MessagePrompterBaseStrategy"
sidebar_label: "MessagePrompterBaseStrategy"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).MessagePrompterBaseStrategy

## Hierarchy

- **`MessagePrompterBaseStrategy`**

  ↳ [`MessagePrompterConfirmStrategy`](sapphire_discord_js_utilities.MessagePrompterConfirmStrategy)

  ↳ [`MessagePrompterMessageStrategy`](sapphire_discord_js_utilities.MessagePrompterMessageStrategy)

  ↳ [`MessagePrompterNumberStrategy`](sapphire_discord_js_utilities.MessagePrompterNumberStrategy)

  ↳ [`MessagePrompterReactionStrategy`](sapphire_discord_js_utilities.MessagePrompterReactionStrategy)

## Constructors

### constructor

• **new MessagePrompterBaseStrategy**(`type`, `message`, `options?`)

Constructor for the [MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy) class

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | `string` | - |
| `message` | `string` \| `MessageOptions` \| [`MessagePayload`](https://discord.js.org/#/docs/main/stable/class/MessagePayload) | - |
| `options?` | [`IMessagePrompterStrategyOptions`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions) | Overrideable options if needed. |

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:44](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L44)

## Properties

### appliedMessage

• **appliedMessage**: ``null`` \| [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> = `null`

The message that has been sent in [MessagePrompter.run](sapphire_discord_js_utilities.MessagePrompter#run)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:27](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L27)

___

### editMessage

• **editMessage**: `undefined` \| [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

The message the bot will edit to send its prompt in [MessagePrompter.run](sapphire_discord_js_utilities.MessagePrompter#run)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:37](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L37)

___

### explicitReturn

• **explicitReturn**: `boolean`

Whether to return an explicit object with data, or the strategies' default

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:22](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L22)

___

### message

• **message**: `string` \| `MessageOptions` \| [`MessagePayload`](https://discord.js.org/#/docs/main/stable/class/MessagePayload)

The message that will be sent in [MessagePrompter.run](sapphire_discord_js_utilities.MessagePrompter#run)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:32](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L32)

___

### timeout

• **timeout**: `number`

The timeout that was used in the collector

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L17)

___

### type

• **type**: `string`

The type of strategy that was used

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:12](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L12)

___

### defaultStrategyOptions

▪ `Static` **defaultStrategyOptions**: [`IMessagePrompterStrategyOptions`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions)

The default strategy options

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

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:113](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L113)

___

### run

▸ `Abstract` **run**(`channel`, `authorOrFilter`): `unknown`

#### Parameters

| Name | Type |
| :------ | :------ |
| `channel` | [`MessagePrompterChannelTypes`](../modules/sapphire_discord_js_utilities#messageprompterchanneltypes) |
| `authorOrFilter` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) \| [`CollectorFilter`](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter)<`unknown`[]\> |

#### Returns

`unknown`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:52](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L52)

---
id: "sapphire_discord_js_utilities.MessagePrompterMessageStrategy"
title: "Class: MessagePrompterMessageStrategy"
sidebar_label: "MessagePrompterMessageStrategy"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).MessagePrompterMessageStrategy

## Hierarchy

- [`MessagePrompterBaseStrategy`](sapphire_discord_js_utilities.MessagePrompterBaseStrategy)

  ↳ **`MessagePrompterMessageStrategy`**

## Implements

- [`IMessagePrompterStrategyOptions`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions)

## Constructors

### constructor

• **new MessagePrompterMessageStrategy**(`message`, `options`)

Constructor for the [MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy) class

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | `string` \| `MessageOptions` \| [`MessagePayload`](https://discord.js.org/#/docs/main/stable/class/MessagePayload) | - |
| `options` | [`IMessagePrompterStrategyOptions`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions) | Overrideable options if needed. |

#### Overrides

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[constructor](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#constructor)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterMessageStrategy.ts:15](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterMessageStrategy.ts#L15)

## Properties

### appliedMessage

• **appliedMessage**: ``null`` \| [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> = `null`

The message that has been sent in [MessagePrompter.run](sapphire_discord_js_utilities.MessagePrompter#run)

#### Inherited from

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[appliedMessage](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#appliedmessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:27](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L27)

___

### editMessage

• **editMessage**: `undefined` \| [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

The message the bot will edit to send its prompt in [MessagePrompter.run](sapphire_discord_js_utilities.MessagePrompter#run)

#### Implementation of

[IMessagePrompterStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions).[editMessage](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions#editmessage)

#### Inherited from

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[editMessage](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#editmessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:37](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L37)

___

### explicitReturn

• **explicitReturn**: `boolean`

Whether to return an explicit object with data, or the strategies' default

#### Implementation of

[IMessagePrompterStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions).[explicitReturn](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions#explicitreturn)

#### Inherited from

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[explicitReturn](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#explicitreturn)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:22](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L22)

___

### message

• **message**: `string` \| `MessageOptions` \| [`MessagePayload`](https://discord.js.org/#/docs/main/stable/class/MessagePayload)

The message that will be sent in [MessagePrompter.run](sapphire_discord_js_utilities.MessagePrompter#run)

#### Inherited from

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[message](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#message)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:32](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L32)

___

### timeout

• **timeout**: `number`

The timeout that was used in the collector

#### Implementation of

[IMessagePrompterStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions).[timeout](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions#timeout)

#### Inherited from

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[timeout](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#timeout)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L17)

___

### type

• **type**: `string`

The type of strategy that was used

#### Inherited from

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[type](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#type)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:12](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L12)

___

### defaultStrategyOptions

▪ `Static` **defaultStrategyOptions**: [`IMessagePrompterStrategyOptions`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions)

The default strategy options

#### Inherited from

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[defaultStrategyOptions](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#defaultstrategyoptions)

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

#### Inherited from

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[collectReactions](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#collectreactions)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:54](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L54)

___

### createMessagePromptFilter

▸ `Private` **createMessagePromptFilter**(`authorOrFilter`): [`CollectorOptions`](https://discord.js.org/#/docs/main/stable/typedef/CollectorOptions)<[[`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>]\>

Creates a filter for the collector to filter on

#### Parameters

| Name | Type |
| :------ | :------ |
| `authorOrFilter` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) \| [`CollectorFilter`](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter)<[[`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>]\> |

#### Returns

[`CollectorOptions`](https://discord.js.org/#/docs/main/stable/typedef/CollectorOptions)<[[`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>]\>

The filter for awaitMessages function

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterMessageStrategy.ts:66](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterMessageStrategy.ts#L66)

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

#### Inherited from

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[createReactionPromptFilter](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#createreactionpromptfilter)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:113](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L113)

___

### run

▸ **run**(`channel`, `authorOrFilter`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> \| [`IMessagePrompterExplicitMessageReturn`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitMessageReturn)\>

This executes the [MessagePrompter](sapphire_discord_js_utilities.MessagePrompter) and sends the message if {@link IMessagePrompterOptions.type} equals message.
The handler will wait for one (1) message.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`MessagePrompterChannelTypes`](../modules/sapphire_discord_js_utilities#messageprompterchanneltypes) | The channel to use. |
| `authorOrFilter` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) \| [`CollectorFilter`](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter)<[[`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>]\> | An author object to validate or a [CollectorFilter](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter) predicate callback. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> \| [`IMessagePrompterExplicitMessageReturn`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitMessageReturn)\>

A promise that resolves to the message object received.

#### Overrides

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[run](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#run)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterMessageStrategy.ts:26](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterMessageStrategy.ts#L26)

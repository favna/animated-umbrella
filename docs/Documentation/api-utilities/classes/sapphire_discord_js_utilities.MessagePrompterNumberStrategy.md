---
id: "sapphire_discord_js_utilities.MessagePrompterNumberStrategy"
title: "Class: MessagePrompterNumberStrategy"
sidebar_label: "MessagePrompterNumberStrategy"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).MessagePrompterNumberStrategy

## Hierarchy

- [`MessagePrompterBaseStrategy`](sapphire_discord_js_utilities.MessagePrompterBaseStrategy)

  ↳ **`MessagePrompterNumberStrategy`**

## Implements

- [`IMessagePrompterNumberStrategyOptions`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions)

## Constructors

### constructor

• **new MessagePrompterNumberStrategy**(`message`, `options`)

Constructor for the [MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy) class

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | `string` \| `MessageOptions` \| [`MessagePayload`](https://discord.js.org/#/docs/main/stable/class/MessagePayload) | - |
| `options` | [`IMessagePrompterNumberStrategyOptions`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions) | Overrideable options if needed. |

#### Overrides

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[constructor](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#constructor)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts:26](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts#L26)

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

[IMessagePrompterNumberStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions).[editMessage](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions#editmessage)

#### Inherited from

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[editMessage](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#editmessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts:37](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterBaseStrategy.ts#L37)

___

### end

• **end**: `number`

The available number emojis

#### Implementation of

[IMessagePrompterNumberStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions).[end](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions#end)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts:19](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts#L19)

___

### explicitReturn

• **explicitReturn**: `boolean`

Whether to return an explicit object with data, or the strategies' default

#### Implementation of

[IMessagePrompterNumberStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions).[explicitReturn](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions#explicitreturn)

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

### numberEmojis

• **numberEmojis**: `EmojiIdentifierResolvable`[]

The available number emojis

#### Implementation of

[IMessagePrompterNumberStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions).[numberEmojis](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions#numberemojis)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts:11](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts#L11)

___

### start

• **start**: `number`

The available number emojis

#### Implementation of

[IMessagePrompterNumberStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions).[start](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions#start)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts:15](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts#L15)

___

### timeout

• **timeout**: `number`

The timeout that was used in the collector

#### Implementation of

[IMessagePrompterNumberStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions).[timeout](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions#timeout)

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

___

### numberEmojis

▪ `Static` **numberEmojis**: `string`[]

The default available number emojis

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts:63](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts#L63)

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

▸ **run**(`channel`, `authorOrFilter`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`number` \| [`IMessagePrompterExplicitNumberReturn`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitNumberReturn)\>

This executes the [MessagePrompter](sapphire_discord_js_utilities.MessagePrompter) and sends the message if {@link IMessagePrompterOptions.type} equals number.
The handler will wait for one (1) reaction.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`MessagePrompterChannelTypes`](../modules/sapphire_discord_js_utilities#messageprompterchanneltypes) | The channel to use. |
| `authorOrFilter` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) \| [`CollectorFilter`](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter)<[[`MessageReaction`](https://discord.js.org/#/docs/main/stable/class/MessageReaction), [`User`](https://discord.js.org/#/docs/main/stable/class/User)]\> | An author object to validate or a [CollectorFilter](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter) predicate callback. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`number` \| [`IMessagePrompterExplicitNumberReturn`](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitNumberReturn)\>

A promise that resolves to the selected number within the range.

#### Overrides

[MessagePrompterBaseStrategy](sapphire_discord_js_utilities.MessagePrompterBaseStrategy).[run](sapphire_discord_js_utilities.MessagePrompterBaseStrategy#run)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts:41](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/strategies/MessagePrompterNumberStrategy.ts#L41)

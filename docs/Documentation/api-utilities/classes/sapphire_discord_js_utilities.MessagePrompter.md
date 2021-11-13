---
id: "sapphire_discord_js_utilities.MessagePrompter"
title: "Class: MessagePrompter<S>"
sidebar_label: "MessagePrompter"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).MessagePrompter

This is a [MessagePrompter](sapphire_discord_js_utilities.MessagePrompter), a utility that sends a message, prompting for user input. The prompt can resolve to any kind of input.
There are several specifiable types to prompt for user input, and they are as follows:
- Confirm
  This will send a simple Yes/No prompt, using reactions.
- Number
  This will prompt for an integer. By default it will be a number between 0 and 10 (inclusive), however you can also specify your own custom range (inclusive).
- Reactions
  This can be any kind of reaction emoji that Discord supports, and as many as you want. This type will return that reaction instead of a boolean.
- Message
  This will prompt the user and require a response in the form of a message. This can be helpful if you require a user to upload an image for example, or give text input.

You must either use this class directly or extend it.

[MessagePrompter](sapphire_discord_js_utilities.MessagePrompter) uses reactions to prompt for a yes/no answer and returns it.
You can modify the confirm and cancel reaction used for each message, or use the {@link MessagePrompter.defaultPrompts}.
{@link MessagePrompter.defaultPrompts} is also static so you can modify these directly.

**`example`**
```typescript
const { MessagePrompter } = require('@sapphire/discord.js-utilities');

const handler = new MessagePrompter('Are you sure you want to continue?');
const result = await handler.run(channel, author);
```

**`example`**
```typescript
const { MessagePrompter, MessagePrompterStrategies } = require('@sapphire/discord.js-utilities');

const handler = new MessagePrompter('Choose a number between 5 and 10?', MessagePrompterStrategies.Number, {
		start: 5,
		end: 10
});
const result = await handler.run(channel, author);
```

**`example`**
```typescript
const { MessagePrompter, MessagePrompterStrategies } = require('@sapphire/discord.js-utilities');

const handler = new MessagePrompter('Are you happy or sad?', MessagePrompterStrategies.Reaction, {
		reactions: ['🙂', '🙁']
});
const result = await handler.run(channel, author);
```

**`example`**
```typescript
const { MessagePrompter, MessagePrompterStrategies } = require('@sapphire/discord.js-utilities');

const handler = new MessagePrompter('Do you love me?', MessagePrompterStrategies.Message);
const result = await handler.run(channel, author);
```

## Type parameters

| Name | Type |
| :------ | :------ |
| `S` | extends keyof [`StrategyReturns`](../interfaces/sapphire_discord_js_utilities.StrategyReturns)``"confirm"`` |

## Constructors

### constructor

• **new MessagePrompter**<`S`\>(`message`, `strategy?`, `strategyOptions?`)

Constructor for the [MessagePrompter](sapphire_discord_js_utilities.MessagePrompter) class

#### Type parameters

| Name | Type |
| :------ | :------ |
| `S` | extends keyof [`StrategyReturns`](../interfaces/sapphire_discord_js_utilities.StrategyReturns)``"confirm"`` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | `string` \| `MessageOptions` \| [`MessagePrompterBaseStrategy`](sapphire_discord_js_utilities.MessagePrompterBaseStrategy) \| [`MessagePayload`](https://discord.js.org/#/docs/main/stable/class/MessagePayload) | The message to send. |
| `strategy?` | `S` | The strategy name or Instance to use |
| `strategyOptions?` | `S` extends keyof [`StrategyOptions`](../interfaces/sapphire_discord_js_utilities.StrategyOptions) ? [`StrategyOptions`](../interfaces/sapphire_discord_js_utilities.StrategyOptions)[`S`] : `never` | The options that are passed to the strategy |

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/MessagePrompter.ts:110](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/MessagePrompter.ts#L110)

## Properties

### strategy

• **strategy**: [`MessagePrompterBaseStrategy`](sapphire_discord_js_utilities.MessagePrompterBaseStrategy)

The strategy used in [MessagePrompter.run](sapphire_discord_js_utilities.MessagePrompter#run)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/MessagePrompter.ts:102](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/MessagePrompter.ts#L102)

___

### defaultStrategy

▪ `Static` **defaultStrategy**: keyof [`StrategyReturns`](../interfaces/sapphire_discord_js_utilities.StrategyReturns) = `'confirm'`

The default strategy to use

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/MessagePrompter.ts:169](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/MessagePrompter.ts#L169)

___

### strategies

▪ `Static` **strategies**: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<keyof [`StrategyReturns`](../interfaces/sapphire_discord_js_utilities.StrategyReturns), `Ctor`<[message: string \| MessageOptions \| MessagePayload, options?: IMessagePrompterConfirmStrategyOptions] \| [message: string \| MessageOptions \| MessagePayload, options: IMessagePrompterNumberStrategyOptions] \| [message: string \| MessageOptions \| MessagePayload, options: IMessagePrompterReactionStrategyOptions] \| [message: string \| MessageOptions \| MessagePayload, options: IMessagePrompterStrategyOptions], [`MessagePrompterConfirmStrategy`](sapphire_discord_js_utilities.MessagePrompterConfirmStrategy) \| [`MessagePrompterNumberStrategy`](sapphire_discord_js_utilities.MessagePrompterNumberStrategy) \| [`MessagePrompterReactionStrategy`](sapphire_discord_js_utilities.MessagePrompterReactionStrategy) \| [`MessagePrompterMessageStrategy`](sapphire_discord_js_utilities.MessagePrompterMessageStrategy)\>\>

The available strategies

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/MessagePrompter.ts:149](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/MessagePrompter.ts#L149)

## Methods

### run

▸ **run**<`Filter`\>(`channel`, `authorOrFilter`): `S` extends keyof [`StrategyReturns`](../interfaces/sapphire_discord_js_utilities.StrategyReturns) ? [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`StrategyReturns`](../interfaces/sapphire_discord_js_utilities.StrategyReturns)[`S`]\> : `never`

This executes the [MessagePrompter](sapphire_discord_js_utilities.MessagePrompter) and sends the message.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `Filter` | extends [[`MessageReaction`](https://discord.js.org/#/docs/main/stable/class/MessageReaction), [`User`](https://discord.js.org/#/docs/main/stable/class/User)] \| [[`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>] |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`MessagePrompterChannelTypes`](../modules/sapphire_discord_js_utilities#messageprompterchanneltypes) | The channel to use. |
| `authorOrFilter` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) \| [`CollectorFilter`](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter)<`Filter`\> | An author object to validate or a [CollectorFilter](https://discord.js.org/#/docs/main/stable/typedef/CollectorFilter) predicate callback. |

#### Returns

`S` extends keyof [`StrategyReturns`](../interfaces/sapphire_discord_js_utilities.StrategyReturns) ? [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`StrategyReturns`](../interfaces/sapphire_discord_js_utilities.StrategyReturns)[`S`]\> : `never`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/MessagePrompter.ts:137](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/MessagePrompter.ts#L137)

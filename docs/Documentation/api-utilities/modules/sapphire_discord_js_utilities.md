---
id: "sapphire_discord_js_utilities"
title: "Module: @sapphire/discord.js-utilities"
sidebar_label: "@sapphire/discord.js-utilities"
custom_edit_url: null
---

## Classes

- [LazyPaginatedMessage](../classes/sapphire_discord_js_utilities.LazyPaginatedMessage)
- [MessageBuilder](../classes/sapphire_discord_js_utilities.MessageBuilder)
- [MessagePrompter](../classes/sapphire_discord_js_utilities.MessagePrompter)
- [MessagePrompterBaseStrategy](../classes/sapphire_discord_js_utilities.MessagePrompterBaseStrategy)
- [MessagePrompterConfirmStrategy](../classes/sapphire_discord_js_utilities.MessagePrompterConfirmStrategy)
- [MessagePrompterMessageStrategy](../classes/sapphire_discord_js_utilities.MessagePrompterMessageStrategy)
- [MessagePrompterNumberStrategy](../classes/sapphire_discord_js_utilities.MessagePrompterNumberStrategy)
- [MessagePrompterReactionStrategy](../classes/sapphire_discord_js_utilities.MessagePrompterReactionStrategy)
- [PaginatedFieldMessageEmbed](../classes/sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)
- [PaginatedMessage](../classes/sapphire_discord_js_utilities.PaginatedMessage)

## Interfaces

- [IMessagePrompterConfirmStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterConfirmStrategyOptions)
- [IMessagePrompterExplicitConfirmReturn](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitConfirmReturn)
- [IMessagePrompterExplicitMessageReturn](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitMessageReturn)
- [IMessagePrompterExplicitNumberReturn](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitNumberReturn)
- [IMessagePrompterExplicitReturnBase](../interfaces/sapphire_discord_js_utilities.IMessagePrompterExplicitReturnBase)
- [IMessagePrompterNumberStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterNumberStrategyOptions)
- [IMessagePrompterReactionStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterReactionStrategyOptions)
- [IMessagePrompterStrategyOptions](../interfaces/sapphire_discord_js_utilities.IMessagePrompterStrategyOptions)
- [PaginatedMessageAction](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction)
- [PaginatedMessageActionContext](../interfaces/sapphire_discord_js_utilities.PaginatedMessageActionContext)
- [PaginatedMessageInternationalizationContext](../interfaces/sapphire_discord_js_utilities.PaginatedMessageInternationalizationContext)
- [PaginatedMessageOptions](../interfaces/sapphire_discord_js_utilities.PaginatedMessageOptions)
- [StrategyFilters](../interfaces/sapphire_discord_js_utilities.StrategyFilters)
- [StrategyOptions](../interfaces/sapphire_discord_js_utilities.StrategyOptions)
- [StrategyReturns](../interfaces/sapphire_discord_js_utilities.StrategyReturns)

## Type aliases

### ChannelTypeString

Ƭ **ChannelTypeString**: [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes)[``"type"``] \| ``"UNKNOWN"``

The types of a channel, with the addition of `'UNKNOWN'`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utility-types.ts:65](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utility-types.ts#L65)

___

### ChannelTypes

Ƭ **ChannelTypes**: `CategoryChannel` \| `DMChannel` \| `PartialDMChannel` \| `NewsChannel` \| `StageChannel` \| `StoreChannel` \| `TextChannel` \| `ThreadChannel` \| `VoiceChannel` \| `GuildChannel` \| `Channel`

A union of all the various types of channels that Discord.js has

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utility-types.ts:19](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utility-types.ts#L19)

___

### GuildBasedChannelTypes

Ƭ **GuildBasedChannelTypes**: [`NonThreadGuildBasedChannelTypes`](sapphire_discord_js_utilities#nonthreadguildbasedchanneltypes) \| `ThreadChannel`

A union of all the channel types that belong to a guild, including {@link ThreadChannel}

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utility-types.ts:50](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utility-types.ts#L50)

___

### GuildTextBasedChannelTypes

Ƭ **GuildTextBasedChannelTypes**: [`NonThreadGuildTextBasedChannelTypes`](sapphire_discord_js_utilities#nonthreadguildtextbasedchanneltypes) \| `ThreadChannel`

A union of guild based message channels, including {@link ThreadChannel}

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utility-types.ts:60](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utility-types.ts#L60)

___

### MessageBuilderFileResolvable

Ƭ **MessageBuilderFileResolvable**: `NonNullable`<`MessageOptions`[``"files"``]\>[`number`]

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:3](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L3)

___

### MessageBuilderResolvable

Ƭ **MessageBuilderResolvable**: `Omit`<`MessageOptions`, ``"embed"`` \| ``"disableMentions"`` \| ``"reply"``\> & { `embeds?`: `MessageOptions`[``"embeds"``]  }

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:4](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L4)

___

### MessagePrompterChannelTypes

Ƭ **MessagePrompterChannelTypes**: `Exclude`<[`ChannelTypes`](sapphire_discord_js_utilities#channeltypes), [`VoiceBasedChannelTypes`](sapphire_discord_js_utilities#voicebasedchanneltypes) \| `StoreChannel` \| `CategoryChannel`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/constants.ts:10](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/constants.ts#L10)

___

### MessagePrompterMessage

Ƭ **MessagePrompterMessage**: `ArgumentTypes`<`PartialTextBasedChannelFields`[``"send"``]\>[``0``]

A type to extend multiple discord types and simplify usage in [MessagePrompter](../classes/sapphire_discord_js_utilities.MessagePrompter)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/constants.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/constants.ts#L8)

___

### NonThreadGuildBasedChannelTypes

Ƭ **NonThreadGuildBasedChannelTypes**: `Extract`<[`ChannelTypes`](sapphire_discord_js_utilities#channeltypes), `GuildChannel`\>

A union of all the channel types that belong to a guild, not including {@link ThreadChannel}

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utility-types.ts:45](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utility-types.ts#L45)

___

### NonThreadGuildTextBasedChannelTypes

Ƭ **NonThreadGuildTextBasedChannelTypes**: `Extract`<[`TextBasedChannelTypes`](sapphire_discord_js_utilities#textbasedchanneltypes), `GuildChannel`\>

A union of guild based message channels, not including {@link ThreadChannel}

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utility-types.ts:55](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utility-types.ts#L55)

___

### PaginatedMessageEmbedResolvable

Ƭ **PaginatedMessageEmbedResolvable**: `MessageOptions`[``"embeds"``]

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:134](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L134)

___

### PaginatedMessageMessageOptionsUnion

Ƭ **PaginatedMessageMessageOptionsUnion**: `MessageOptions` \| `WebhookEditMessageOptions`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:136](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L136)

___

### PaginatedMessagePage

Ƭ **PaginatedMessagePage**: (`index`: `number`, `pages`: [`PaginatedMessagePage`](sapphire_discord_js_utilities#paginatedmessagepage)[], `handler`: [`PaginatedMessage`](../classes/sapphire_discord_js_utilities.PaginatedMessage)) => `Awaitable`<[`PaginatedMessageMessageOptionsUnion`](sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion)\> \| [`PaginatedMessageMessageOptionsUnion`](sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion)

The pages that are used for [PaginatedMessage.pages](../classes/sapphire_discord_js_utilities.PaginatedMessage#pages)

Pages can be either a {@link Message},
or an [Awaitable](sapphire_utilities#awaitable) function that returns a {@link Message}.

Furthermore, {@link MessageOptions} can be used to
construct the pages without state. This library also provides [MessageBuilder](../classes/sapphire_discord_js_utilities.MessageBuilder), which can be used as a chainable
alternative to raw objects, similar to how {@link MessageEmbed}
works.

Ideally, however, you should use the utility functions
[`addPageBuilder`](../classes/sapphire_discord_js_utilities.PaginatedMessage#addpagebuilder), [`addPageContent`](../classes/sapphire_discord_js_utilities.PaginatedMessage#addpagecontent), and [`addPageEmbed`](../classes/sapphire_discord_js_utilities.PaginatedMessage#addpageembed)
as opposed to manually constructing [`MessagePages`](sapphire_discord_js_utilities#paginatedmessagepage). This is because a [PaginatedMessage](../classes/sapphire_discord_js_utilities.PaginatedMessage) does a lot of post-processing
on the provided pages and we can only guarantee this will work properly when using the utility methods.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:113](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L113)

___

### PaginatedMessageSelectMenuOptionsFunction

Ƭ **PaginatedMessageSelectMenuOptionsFunction**: (`pageIndex`: `number`, `internationalizationContext`: [`PaginatedMessageInternationalizationContext`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageInternationalizationContext)) => `Awaitable`<`Omit`<`MessageSelectOptionData`, ``"value"``\>\>

#### Type declaration

▸ (`pageIndex`, `internationalizationContext`): `Awaitable`<`Omit`<`MessageSelectOptionData`, ``"value"``\>\>

The type of the custom function that can be set for the [PaginatedMessage.selectMenuOptions](../classes/sapphire_discord_js_utilities.PaginatedMessage#selectmenuoptions)

##### Parameters

| Name | Type |
| :------ | :------ |
| `pageIndex` | `number` |
| `internationalizationContext` | [`PaginatedMessageInternationalizationContext`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageInternationalizationContext) |

##### Returns

`Awaitable`<`Omit`<`MessageSelectOptionData`, ``"value"``\>\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:120](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L120)

___

### PaginatedMessageWrongUserInteractionReplyFunction

Ƭ **PaginatedMessageWrongUserInteractionReplyFunction**: (`targetUser`: `User`, `interactionUser`: `User`, `internationalizationContext`: [`PaginatedMessageInternationalizationContext`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageInternationalizationContext)) => `Awaitable`<`Parameters`<`MessageComponentInteraction`[``"reply"``]\>[``0``]\>

#### Type declaration

▸ (`targetUser`, `interactionUser`, `internationalizationContext`): `Awaitable`<`Parameters`<`MessageComponentInteraction`[``"reply"``]\>[``0``]\>

The type of the custom function that can be set for the [PaginatedMessage.wrongUserInteractionReply](../classes/sapphire_discord_js_utilities.PaginatedMessage#wronguserinteractionreply)

##### Parameters

| Name | Type |
| :------ | :------ |
| `targetUser` | `User` |
| `interactionUser` | `User` |
| `internationalizationContext` | [`PaginatedMessageInternationalizationContext`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageInternationalizationContext) |

##### Returns

`Awaitable`<`Parameters`<`MessageComponentInteraction`[``"reply"``]\>[``0``]\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:128](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L128)

___

### TextBasedChannelTypes

Ƭ **TextBasedChannelTypes**: `Message`[``"channel"``]

A union of all the channel types that a message can come from

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utility-types.ts:35](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utility-types.ts#L35)

___

### VoiceBasedChannelTypes

Ƭ **VoiceBasedChannelTypes**: `VoiceChannel` \| `StageChannel`

A union of all the voice-based channel types that Discord.js has

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utility-types.ts:40](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utility-types.ts#L40)

## Variables

### ChannelMentionRegex

• **ChannelMentionRegex**: `RegExp`

Regex that can capture the ID in Discord Channel mentions

**`raw`** `/^<#(?<id>\d{17,19})>$/`

**`remark`** Capture group 1 is the ID of the channel. It is named `id`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:6

___

### ChannelMessageRegex

• **ChannelMessageRegex**: `RegExp`

Regex that can capture the channel and message IDs in a channelId-messageId pattern
This pattern can be found when you hold Shift and hover over a message, and click the "ID" button

**`raw`** `/^(?<channelId>\d{17,19})-(?<messageId>\d{17,19})$/`

**`remark`** Capture group 1 is the ID of the channel, named `channelId`.

**`remark`** Capture group 2 is the ID of the message, named `messageId`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:14

___

### DiscordHostnameRegex

• **DiscordHostnameRegex**: `RegExp`

Regex that matches links on the known Discord host names

**`raw`** `/(?<subdomain>\w+)\.?(?<hostname>dis(?:cord)?(?:app|merch|status)?)\.(?<tld>com|g(?:d|g|ift)|(?:de(?:sign|v))|media|new|store|net)/i`

**`remark`** The regex is case insensitive

**`remark`** Capture group 1 is the subdomain for this URL. It is named `subdomain`.

**`remark`** Capture group 2 is the hostname for this URL, primarily `discord` but can also be `discordmerch`, `discordstatus`, `dis`, and `discordapp`. It is named `hostname`.

**`remark`** Capture group 3 is the Top-Level Domain *without* `.`. It is named `tld`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:23

___

### DiscordInviteLinkRegex

• **DiscordInviteLinkRegex**: `RegExp`

Regex that can can capture the code of Discord invite links

**`raw`** `/^(?:https?:\/\/)?(?:www\.)?(?:discord\.gg\/|discord(?:app)?\.com\/invite\/)?(?<code>[\w\d-]{2,})$/i`

**`remark`** Capture group 1 is the invite URL's unique code. It is named `code`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:29

___

### EmojiRegex

• **EmojiRegex**: `RegExp`

Regex that can capture the ID of any animated or non-animated custom Discord emoji

**`raw`** `/^(?:<(?<animated>a)?:(?<name>\w{2,32}):)?(?<id>\d{17,21})>?$/`

**`remark`** Capture group 1 can be used to determine whether the emoji is animated or not. It is named `animated`.

**`remark`** Capture group 2 is the name of the emoji as it is typed in a message. It is named `name`.

**`remark`** Capture group 3 is the ID of the emoji. It is named `id`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:37

___

### FormattedCustomEmoji

• **FormattedCustomEmoji**: `RegExp`

Regex that matches any animated or non-animated custom Discord emoji.
Unlike [EmojiRegex](sapphire_discord_utilities#emojiregex) It can be a substring of a larger string.

**`raw`** `/<a?:\w{2,32}:\d{17,18}>/`

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:43

___

### FormattedCustomEmojiWithGroups

• **FormattedCustomEmojiWithGroups**: `RegExp`

Regex that can capture any animated or non-animated custom Discord emoji.
Similar to [FormattedCustomEmoji](sapphire_discord_utilities#formattedcustomemoji) and unlike [EmojiRegex](sapphire_discord_utilities#emojiregex) can also be a substring of a larger string.

**`raw`** `/(?<animated>a?):(?<name>[^:]+):(?<id>\d{17,19})/`

**`remark`** Capture group 1 can be used to determine whether the emoji is animated or not. It is named `animated`.

**`remark`** Capture group 2 is the name of the emoji as it is typed in a message. It is named `name`.

**`remark`** Capture group 3 is the ID of the emoji. It is named `id`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:52

___

### HttpUrlRegex

• **HttpUrlRegex**: `RegExp`

Regex that matches any URL starting with `http` or `https`

**`raw`** `/^https?:\/\//`

**`remark`** for WebSocket URLs see {@link WebsocketGenericUrlRegex}

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:58

___

### MessageLinkRegex

• **MessageLinkRegex**: `RegExp`

Regex that can capture the Guild, Channel, and Message ID based on a shareable Discord message link.

**`raw`** `/^(?:https:\/\/)?(?:ptb\.|canary\.)?discord(?:app)?\.com\/channels\/(?<guildId>(?:\d{17,19}|@me))\/(?<channelId>\d{17,19})\/(?<messageId>\d{17,19})$/`

**`remark`** Capture group 1 is the ID of the guild the message was sent in. It is named `guildId`.

**`remark`** Capture group 2 is the ID of the channel in that guild the message was sent in. It is named `channelId`.

**`remark`** Capture group 3 is the ID of the message itself. It is named `messageId`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:66

___

### ParsedCustomEmoji

• **ParsedCustomEmoji**: `RegExp`

Regex that matches any animated or non-animated custom Discord emoji *without the wrapping `<...>` symbols.
This means that a string that matches this regex can directly be send inside a Discord message.
Other than this difference it is similar to [FormattedCustomEmoji](sapphire_discord_utilities#formattedcustomemoji).

**`raw`** `/a?:\w{2,32}:\d{17,18}/`

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:73

___

### ParsedCustomEmojiWithGroups

• **ParsedCustomEmojiWithGroups**: `RegExp`

Regex that matches any animated or non-animated custom Discord emoji *without the wrapping `<...>` symbols.
This means that a string that matches this regex can directly be send inside a Discord message.
Other than this difference it is similar to [FormattedCustomEmojiWithGroups](sapphire_discord_utilities#formattedcustomemojiwithgroups).

**`raw`** `/(?<animated>a?):(?<name>[^:]+):(?<id>\d{17,19})/`

**`remark`** Capture group 1 can be used to determine whether the emoji is animated or not. It is named `animated`.

**`remark`** Capture group 2 is the name of the emoji as it is typed in a message. It is named `name`.

**`remark`** Capture group 3 is the ID of the emoji. It is named `id`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:83

___

### RoleMentionRegex

• **RoleMentionRegex**: `RegExp`

Regex that can capture the ID in Discord Role mentions

**`raw`** `/^<@&(?<id>\d{17,19})>$/`

**`remark`** Capture group 1 is the ID of the role. It is named `id`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:89

___

### SnowflakeRegex

• **SnowflakeRegex**: `RegExp`

Regex that can capture any Discord Snowflake ID

**`raw`** `/^(?<id>\d{17,19})$/`

**`remark`** Capture group 1 is the Snowflake. It is named `id`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:95

___

### TwemojiRegex

• **TwemojiRegex**: `RegExp`

Regex that can capture a Twemoji (Twitter Emoji)

**`raw`** [See official source code](https://github.com/twitter/twemoji-parser/blob/master/src/lib/regex.js)

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:100

___

### UserOrMemberMentionRegex

• **UserOrMemberMentionRegex**: `RegExp`

Regex that can capture the ID of a user in Discord user mentions

**`raw`** `/^<@!?(?<id>\d{17,19})>$/`

**`remark`** Capture group 1 is the ID of the user. It is named `id`.

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:106

___

### WebSocketUrlRegex

• **WebSocketUrlRegex**: `RegExp`

Regex that matches any WebSocket URL starting with `ws` or `wss`

**`raw`** `/^wss?:\/\//`

**`remark`** for regular HTTP URLs see [HttpUrlRegex](sapphire_discord_utilities#httpurlregex)

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:112

___

### WebhookRegex

• **WebhookRegex**: `RegExp`

Regex that captures the Webhook ID and token from a Discord Webhook URL.

**`raw`** `/(?<url>^https:\/\/(?:(?:canary|ptb).)?discordapp.com\/api\/webhooks\/(?<id>\d+)\/(?<token>[\w-]+)\/?$)/`

**`remark`** Capture group 1 is the full URL of the Discord Webhook. It is named `url`.

**`remark`** Capture group 2 is the ID of the Discord Webhook. It is named `id`.

**`remark`** Capture group 3 is the token of the Discord Webhook. It is named `token`.

**`remark`** for regular HTTP URLs see [HttpUrlRegex](sapphire_discord_utilities#httpurlregex)

#### Defined in

node_modules/@sapphire/discord-utilities/dist/lib/regexes.d.ts:121

## Functions

### canReact

▸ **canReact**(`channel`): `boolean`

Determines whether or not we can send react to messages in a given channel.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to test the permissions from. |

#### Returns

`boolean`

Whether or not we can react to messages in the specified channel.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utilities.ts:72](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utilities.ts#L72)

___

### canReadMessages

▸ **canReadMessages**(`channel`): `boolean`

Determines whether or not we can send messages in a given channel.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to test the permissions from. |

#### Returns

`boolean`

Whether or not we can send messages in the specified channel.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utilities.ts:13](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utilities.ts#L13)

___

### canRemoveAllReactions

▸ **canRemoveAllReactions**(`channel`): `boolean`

Determines whether or not we can remove reactions from messages in a given channel.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to test the permissions from. |

#### Returns

`boolean`

Whether or not we can remove reactions from messages in the specified channel.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utilities.ts:87](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utilities.ts#L87)

___

### canSendAttachments

▸ **canSendAttachments**(`channel`): `boolean`

Determines whether or not we can send attachments in a given channel.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to test the permissions from. |

#### Returns

`boolean`

Whether or not we can send attachments in the specified channel.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utilities.ts:57](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utilities.ts#L57)

___

### canSendEmbeds

▸ **canSendEmbeds**(`channel`): `boolean`

Determines whether or not we can send embeds in a given channel.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to test the permissions from. |

#### Returns

`boolean`

Whether or not we can send embeds in the specified channel.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utilities.ts:42](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utilities.ts#L42)

___

### canSendMessages

▸ **canSendMessages**(`channel`): `boolean`

Determines whether or not we can send messages in a given channel.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to test the permissions from. |

#### Returns

`boolean`

Whether or not we can send messages in the specified channel.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/utilities.ts:27](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/utilities.ts#L27)

___

### createPartitionedMessageRow

▸ **createPartitionedMessageRow**(`components`): `MessageActionRow`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `components` | ([`MessageButton`](https://discord.js.org/#/docs/main/stable/class/MessageButton) \| [`MessageSelectMenu`](https://discord.js.org/#/docs/main/stable/class/MessageSelectMenu))[] |

#### Returns

`MessageActionRow`[]

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/utils.ts:10](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/utils.ts#L10)

___

### isCategoryChannel

▸ **isCategoryChannel**(`channel`): channel is CategoryChannel

Checks whether a given channel is a {@link CategoryChannel}

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check |

#### Returns

channel is CategoryChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:21](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L21)

___

### isDMChannel

▸ **isDMChannel**(`channel`): channel is DMChannel \| PartialDMChannel

Checks whether a given channel is a {@link DMChannel}

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check |

#### Returns

channel is DMChannel \| PartialDMChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:29](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L29)

___

### isGroupChannel

▸ **isGroupChannel**(`channel`): channel is PartialGroupDMChannel

Checks whether a given channel is a {@link PartialGroupDMChannel}

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | `PartialDMChannel` \| [`Channel`](https://discord.js.org/#/docs/main/stable/class/Channel) \| `Nullish` | The channel to check |

#### Returns

channel is PartialGroupDMChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:37](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L37)

___

### isGuildBasedChannel

▸ **isGuildBasedChannel**(`channel`): channel is GuildTextBasedChannelTypes

Checks if a channel comes from a guild.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check |

#### Returns

channel is GuildTextBasedChannelTypes

Whether or not the channel is guild-based.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:46](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L46)

___

### isGuildBasedChannelByGuildKey

▸ **isGuildBasedChannelByGuildKey**(`channel`): channel is GuildTextBasedChannelTypes

Checks whether or not a channel comes from a guild.

**`remark`** As opposed to [isGuildBasedChannel](sapphire_discord_js_utilities#isguildbasedchannel) this checks if there is `guild` property on the channel.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check. |

#### Returns

channel is GuildTextBasedChannelTypes

Whether or not the channel is guild-based.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:56](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L56)

___

### isMessageButtonInteraction

▸ **isMessageButtonInteraction**(`interaction`): interaction is InteractionButtonOptions

#### Parameters

| Name | Type |
| :------ | :------ |
| `interaction` | `InteractionButtonOptions` \| `MessageSelectMenuOptions` |

#### Returns

interaction is InteractionButtonOptions

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/utils.ts:4](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/utils.ts#L4)

___

### isNewsChannel

▸ **isNewsChannel**(`channel`): channel is NewsChannel

Checks whether a given channel is a {@link NewsChannel}.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check. |

#### Returns

channel is NewsChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:64](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L64)

___

### isNewsThreadChannel

▸ **isNewsThreadChannel**(`channel`): channel is ThreadChannel

Checks whether a given channel is a News {@link ThreadChannel}

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check. |

#### Returns

channel is ThreadChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:112](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L112)

___

### isNsfwChannel

▸ **isNsfwChannel**(`channel`): `boolean`

Checks whether a given channel allows NSFW content or not

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check. |

#### Returns

`boolean`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:146](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L146)

___

### isPrivateThreadChannel

▸ **isPrivateThreadChannel**(`channel`): channel is ThreadChannel

Checks whether a given channel is a Private {@link ThreadChannel}

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check. |

#### Returns

channel is ThreadChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:128](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L128)

___

### isPublicThreadChannel

▸ **isPublicThreadChannel**(`channel`): channel is ThreadChannel

Checks whether a given channel is a Public {@link ThreadChannel}

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check. |

#### Returns

channel is ThreadChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:120](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L120)

___

### isStageChannel

▸ **isStageChannel**(`channel`): channel is StageChannel

Checks whether a given channel is a {@link StageChannel}

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check |

#### Returns

channel is StageChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:96](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L96)

___

### isStoreChannel

▸ **isStoreChannel**(`channel`): channel is StoreChannel

Checks whether a given channel is a {@link StoreChannel}

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check |

#### Returns

channel is StoreChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:72](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L72)

___

### isTextBasedChannel

▸ **isTextBasedChannel**(`channel`): channel is DMChannel \| PartialDMChannel \| NewsChannel \| TextChannel \| ThreadChannel

Checks whether a given channel is a [TextBasedChannelTypes](sapphire_discord_js_utilities#textbasedchanneltypes). This means it has a `send` method.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check. |

#### Returns

channel is DMChannel \| PartialDMChannel \| NewsChannel \| TextChannel \| ThreadChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:136](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L136)

___

### isTextChannel

▸ **isTextChannel**(`channel`): channel is TextChannel

Checks whether a given channel is a {@link TextChannel}.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check. |

#### Returns

channel is TextChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:80](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L80)

___

### isThreadChannel

▸ **isThreadChannel**(`channel`): channel is ThreadChannel

Checks whether a given channel is a {@link ThreadChannel}

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check. |

#### Returns

channel is ThreadChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:104](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L104)

___

### isVoiceChannel

▸ **isVoiceChannel**(`channel`): channel is VoiceChannel

Checks whether a given channel is a {@link VoiceChannel}

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`ChannelTypes`](sapphire_discord_js_utilities#channeltypes) \| `Nullish` | The channel to check |

#### Returns

channel is VoiceChannel

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/type-guards.ts:88](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/type-guards.ts#L88)

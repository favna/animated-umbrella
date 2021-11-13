---
id: "sapphire_discord_utilities"
title: "Module: @sapphire/discord-utilities"
sidebar_label: "@sapphire/discord-utilities"
sidebar_position: 0
custom_edit_url: null
---

## Variables

### ChannelMentionRegex

• **ChannelMentionRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that can capture the ID in Discord Channel mentions

**`raw`** `/^<#(?<id>\d{17,19})>$/`

**`remark`** Capture group 1 is the ID of the channel. It is named `id`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L8)

___

### ChannelMessageRegex

• **ChannelMessageRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that can capture the channel and message IDs in a channelId-messageId pattern
This pattern can be found when you hold Shift and hover over a message, and click the "ID" button

**`raw`** `/^(?<channelId>\d{17,19})-(?<messageId>\d{17,19})$/`

**`remark`** Capture group 1 is the ID of the channel, named `channelId`.

**`remark`** Capture group 2 is the ID of the message, named `messageId`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L17)

___

### DiscordHostnameRegex

• **DiscordHostnameRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that matches links on the known Discord host names

**`raw`** `/(?<subdomain>\w+)\.?(?<hostname>dis(?:cord)?(?:app|merch|status)?)\.(?<tld>com|g(?:d|g|ift)|(?:de(?:sign|v))|media|new|store|net)/i`

**`remark`** The regex is case insensitive

**`remark`** Capture group 1 is the subdomain for this URL. It is named `subdomain`.

**`remark`** Capture group 2 is the hostname for this URL, primarily `discord` but can also be `discordmerch`, `discordstatus`, `dis`, and `discordapp`. It is named `hostname`.

**`remark`** Capture group 3 is the Top-Level Domain *without* `.`. It is named `tld`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:27](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L27)

___

### DiscordInviteLinkRegex

• **DiscordInviteLinkRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that can can capture the code of Discord invite links

**`raw`** `/^(?:https?:\/\/)?(?:www\.)?(?:discord\.gg\/|discord(?:app)?\.com\/invite\/)?(?<code>[\w\d-]{2,})$/i`

**`remark`** Capture group 1 is the invite URL's unique code. It is named `code`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:35](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L35)

___

### EmojiRegex

• **EmojiRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that can capture the ID of any animated or non-animated custom Discord emoji

**`raw`** `/^(?:<(?<animated>a)?:(?<name>\w{2,32}):)?(?<id>\d{17,21})>?$/`

**`remark`** Capture group 1 can be used to determine whether the emoji is animated or not. It is named `animated`.

**`remark`** Capture group 2 is the name of the emoji as it is typed in a message. It is named `name`.

**`remark`** Capture group 3 is the ID of the emoji. It is named `id`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:44](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L44)

___

### FormattedCustomEmoji

• **FormattedCustomEmoji**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that matches any animated or non-animated custom Discord emoji.
Unlike [EmojiRegex](sapphire_discord_utilities#emojiregex) It can be a substring of a larger string.

**`raw`** `/<a?:\w{2,32}:\d{17,18}>/`

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:51](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L51)

___

### FormattedCustomEmojiWithGroups

• **FormattedCustomEmojiWithGroups**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that can capture any animated or non-animated custom Discord emoji.
Similar to [FormattedCustomEmoji](sapphire_discord_utilities#formattedcustomemoji) and unlike [EmojiRegex](sapphire_discord_utilities#emojiregex) can also be a substring of a larger string.

**`raw`** `/(?<animated>a?):(?<name>[^:]+):(?<id>\d{17,19})/`

**`remark`** Capture group 1 can be used to determine whether the emoji is animated or not. It is named `animated`.

**`remark`** Capture group 2 is the name of the emoji as it is typed in a message. It is named `name`.

**`remark`** Capture group 3 is the ID of the emoji. It is named `id`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:61](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L61)

___

### HttpUrlRegex

• **HttpUrlRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that matches any URL starting with `http` or `https`

**`raw`** `/^https?:\/\//`

**`remark`** for WebSocket URLs see {@link WebsocketGenericUrlRegex}

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:68](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L68)

___

### MessageLinkRegex

• **MessageLinkRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that can capture the Guild, Channel, and Message ID based on a shareable Discord message link.

**`raw`** `/^(?:https:\/\/)?(?:ptb\.|canary\.)?discord(?:app)?\.com\/channels\/(?<guildId>(?:\d{17,19}|@me))\/(?<channelId>\d{17,19})\/(?<messageId>\d{17,19})$/`

**`remark`** Capture group 1 is the ID of the guild the message was sent in. It is named `guildId`.

**`remark`** Capture group 2 is the ID of the channel in that guild the message was sent in. It is named `channelId`.

**`remark`** Capture group 3 is the ID of the message itself. It is named `messageId`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:77](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L77)

___

### ParsedCustomEmoji

• **ParsedCustomEmoji**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that matches any animated or non-animated custom Discord emoji *without the wrapping `<...>` symbols.
This means that a string that matches this regex can directly be send inside a Discord message.
Other than this difference it is similar to [FormattedCustomEmoji](sapphire_discord_utilities#formattedcustomemoji).

**`raw`** `/a?:\w{2,32}:\d{17,18}/`

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:86](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L86)

___

### ParsedCustomEmojiWithGroups

• **ParsedCustomEmojiWithGroups**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that matches any animated or non-animated custom Discord emoji *without the wrapping `<...>` symbols.
This means that a string that matches this regex can directly be send inside a Discord message.
Other than this difference it is similar to [FormattedCustomEmojiWithGroups](sapphire_discord_utilities#formattedcustomemojiwithgroups).

**`raw`** `/(?<animated>a?):(?<name>[^:]+):(?<id>\d{17,19})/`

**`remark`** Capture group 1 can be used to determine whether the emoji is animated or not. It is named `animated`.

**`remark`** Capture group 2 is the name of the emoji as it is typed in a message. It is named `name`.

**`remark`** Capture group 3 is the ID of the emoji. It is named `id`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:97](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L97)

___

### RoleMentionRegex

• **RoleMentionRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that can capture the ID in Discord Role mentions

**`raw`** `/^<@&(?<id>\d{17,19})>$/`

**`remark`** Capture group 1 is the ID of the role. It is named `id`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:104](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L104)

___

### SnowflakeRegex

• **SnowflakeRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that can capture any Discord Snowflake ID

**`raw`** `/^(?<id>\d{17,19})$/`

**`remark`** Capture group 1 is the Snowflake. It is named `id`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:111](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L111)

___

### TwemojiRegex

• **TwemojiRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp) = `twemojiRegex`

Regex that can capture a Twemoji (Twitter Emoji)

**`raw`** [See official source code](https://github.com/twitter/twemoji-parser/blob/master/src/lib/regex.js)

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:117](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L117)

___

### UserOrMemberMentionRegex

• **UserOrMemberMentionRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that can capture the ID of a user in Discord user mentions

**`raw`** `/^<@!?(?<id>\d{17,19})>$/`

**`remark`** Capture group 1 is the ID of the user. It is named `id`.

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:124](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L124)

___

### WebSocketUrlRegex

• **WebSocketUrlRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that matches any WebSocket URL starting with `ws` or `wss`

**`raw`** `/^wss?:\/\//`

**`remark`** for regular HTTP URLs see [HttpUrlRegex](sapphire_discord_utilities#httpurlregex)

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:131](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L131)

___

### WebhookRegex

• **WebhookRegex**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

Regex that captures the Webhook ID and token from a Discord Webhook URL.

**`raw`** `/(?<url>^https:\/\/(?:(?:canary|ptb).)?discordapp.com\/api\/webhooks\/(?<id>\d+)\/(?<token>[\w-]+)\/?$)/`

**`remark`** Capture group 1 is the full URL of the Discord Webhook. It is named `url`.

**`remark`** Capture group 2 is the ID of the Discord Webhook. It is named `id`.

**`remark`** Capture group 3 is the token of the Discord Webhook. It is named `token`.

**`remark`** for regular HTTP URLs see [HttpUrlRegex](sapphire_discord_utilities#httpurlregex)

#### Defined in

[projects/utilities/packages/discord-utilities/src/lib/regexes.ts:141](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord-utilities/src/lib/regexes.ts#L141)

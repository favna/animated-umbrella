---
id: "sapphire_discord_js_utilities.PaginatedMessageActionContext"
title: "Interface: PaginatedMessageActionContext"
sidebar_label: "PaginatedMessageActionContext"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).PaginatedMessageActionContext

The context to be used in [PaginatedMessageAction](sapphire_discord_js_utilities.PaginatedMessageAction).

## Properties

### author

• **author**: [`User`](https://discord.js.org/#/docs/main/stable/class/User)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:60](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L60)

___

### channel

• **channel**: [`DMChannel`](https://discord.js.org/#/docs/main/stable/class/DMChannel) \| `PartialDMChannel` \| [`NewsChannel`](https://discord.js.org/#/docs/main/stable/class/NewsChannel) \| [`TextChannel`](https://discord.js.org/#/docs/main/stable/class/TextChannel) \| [`ThreadChannel`](https://discord.js.org/#/docs/main/stable/class/ThreadChannel)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:61](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L61)

___

### collector

• **collector**: [`InteractionCollector`](https://discord.js.org/#/docs/main/stable/class/InteractionCollector)<[`MessageComponentInteraction`](https://discord.js.org/#/docs/main/stable/class/MessageComponentInteraction)<`CacheType`\>\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:63](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L63)

___

### handler

• **handler**: [`PaginatedMessage`](../classes/sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:59](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L59)

___

### interaction

• **interaction**: [`ButtonInteraction`](https://discord.js.org/#/docs/main/stable/class/ButtonInteraction)<`CacheType`\> \| [`SelectMenuInteraction`](https://discord.js.org/#/docs/main/stable/class/SelectMenuInteraction)<`CacheType`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:58](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L58)

___

### response

• **response**: [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:62](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L62)

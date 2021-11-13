---
id: "sapphire_discord_js_utilities.PaginatedMessageInternationalizationContext"
title: "Interface: PaginatedMessageInternationalizationContext"
sidebar_label: "PaginatedMessageInternationalizationContext"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).PaginatedMessageInternationalizationContext

**`internal`** This is a duplicate of the same interface in `@sapphire/plugin-i18next`
Duplicated here for the type of the parameters in the functions

Context for {@link InternationalizationHandler.fetchLanguage} functions.
This context enables implementation of per-guild, per-channel, and per-user localization.

## Properties

### author

• **author**: ``null`` \| [`User`](https://discord.js.org/#/docs/main/stable/class/User)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:148](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L148)

___

### channel

• **channel**: ``null`` \| [`DMChannel`](https://discord.js.org/#/docs/main/stable/class/DMChannel) \| `PartialDMChannel` \| [`NewsChannel`](https://discord.js.org/#/docs/main/stable/class/NewsChannel) \| [`StageChannel`](https://discord.js.org/#/docs/main/stable/class/StageChannel) \| [`StoreChannel`](https://discord.js.org/#/docs/main/stable/class/StoreChannel) \| [`TextChannel`](https://discord.js.org/#/docs/main/stable/class/TextChannel) \| [`ThreadChannel`](https://discord.js.org/#/docs/main/stable/class/ThreadChannel) \| [`VoiceChannel`](https://discord.js.org/#/docs/main/stable/class/VoiceChannel)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:147](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L147)

___

### guild

• **guild**: ``null`` \| [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:146](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L146)

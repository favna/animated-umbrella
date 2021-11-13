---
id: "sapphire_discord_js_utilities.PaginatedMessageOptions"
title: "Interface: PaginatedMessageOptions"
sidebar_label: "PaginatedMessageOptions"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).PaginatedMessageOptions

## Properties

### actions

• `Optional` **actions**: [`PaginatedMessageAction`](sapphire_discord_js_utilities.PaginatedMessageAction)[]

Custom actions to provide when sending the paginated message

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:74](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L74)

___

### embedFooterSeparator

• `Optional` **embedFooterSeparator**: `string`

**`seealso`** [PaginatedMessage.embedFooterSeparator](../classes/sapphire_discord_js_utilities.PaginatedMessage#embedfooterseparator)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:86](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L86)

___

### pageIndexPrefix

• `Optional` **pageIndexPrefix**: `string`

**`seealso`** [PaginatedMessage.pageIndexPrefix](../classes/sapphire_discord_js_utilities.PaginatedMessage#pageindexprefix)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:82](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L82)

___

### pages

• `Optional` **pages**: [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage)[]

The pages to display in this [PaginatedMessage](../classes/sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:70](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L70)

___

### paginatedMessageData

• `Optional` **paginatedMessageData**: ``null`` \| `Omit`<[`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion), ``"components"``\>

Additional options that are applied to each message when sending it to Discord.
Be careful with using this, misusing it can cause issues, such as sending empty messages.

**`remark`** **This is for advanced usages only!**

**`default`** null

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:94](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L94)

___

### template

• `Optional` **template**: `MessageOptions` \| [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)

The {@link MessageEmbed} or {@link MessageOptions} options to apply to the entire [PaginatedMessage](../classes/sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts:78](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessageTypes.ts#L78)

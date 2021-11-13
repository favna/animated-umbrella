---
id: "Resolvers"
title: "Namespace: Resolvers"
sidebar_label: "Resolvers"
sidebar_position: 0
custom_edit_url: null
---

## Functions

### resolveBoolean

▸ **resolveBoolean**(`parameter`, `customs?`): [`Result`](../#result)<`boolean`, [`ArgumentBooleanError`](../enums/Identifiers#argumentbooleanerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `customs?` | `Object` |
| `customs.falses?` | `string`[] |
| `customs.truths?` | `string`[] |

#### Returns

[`Result`](../#result)<`boolean`, [`ArgumentBooleanError`](../enums/Identifiers#argumentbooleanerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/boolean.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/boolean.ts#L7)

___

### resolveChannel

▸ **resolveChannel**(`parameter`, `message`): [`Result`](../#result)<`ChannelTypes`, [`ArgumentChannelError`](../enums/Identifiers#argumentchannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> |

#### Returns

[`Result`](../#result)<`ChannelTypes`, [`ArgumentChannelError`](../enums/Identifiers#argumentchannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/channel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/channel.ts#L7)

___

### resolveDMChannel

▸ **resolveDMChannel**(`parameter`, `message`): [`Result`](../#result)<`DMChannel`, [`ArgumentChannelError`](../enums/Identifiers#argumentchannelerror) \| [`ArgumentDMChannelError`](../enums/Identifiers#argumentdmchannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> |

#### Returns

[`Result`](../#result)<`DMChannel`, [`ArgumentChannelError`](../enums/Identifiers#argumentchannelerror) \| [`ArgumentDMChannelError`](../enums/Identifiers#argumentdmchannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/dmChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/dmChannel.ts#L7)

___

### resolveDate

▸ **resolveDate**(`parameter`, `options?`): [`Result`](../#result)<`Date`, [`ArgumentDateError`](../enums/Identifiers#argumentdateerror) \| [`ArgumentDateTooEarly`](../enums/Identifiers#argumentdatetooearly) \| [`ArgumentDateTooFar`](../enums/Identifiers#argumentdatetoofar)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `options?` | `Object` |
| `options.maximum?` | `number` |
| `options.minimum?` | `number` |

#### Returns

[`Result`](../#result)<`Date`, [`ArgumentDateError`](../enums/Identifiers#argumentdateerror) \| [`ArgumentDateTooEarly`](../enums/Identifiers#argumentdatetooearly) \| [`ArgumentDateTooFar`](../enums/Identifiers#argumentdatetoofar)\>

#### Defined in

[projects/framework/src/lib/resolvers/date.ts:4](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/date.ts#L4)

___

### resolveFloat

▸ **resolveFloat**(`parameter`, `options?`): [`Result`](../#result)<`number`, [`ArgumentFloatError`](../enums/Identifiers#argumentfloaterror) \| [`ArgumentFloatTooSmall`](../enums/Identifiers#argumentfloattoosmall) \| [`ArgumentFloatTooLarge`](../enums/Identifiers#argumentfloattoolarge)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `options?` | `Object` |
| `options.maximum?` | `number` |
| `options.minimum?` | `number` |

#### Returns

[`Result`](../#result)<`number`, [`ArgumentFloatError`](../enums/Identifiers#argumentfloaterror) \| [`ArgumentFloatTooSmall`](../enums/Identifiers#argumentfloattoosmall) \| [`ArgumentFloatTooLarge`](../enums/Identifiers#argumentfloattoolarge)\>

#### Defined in

[projects/framework/src/lib/resolvers/float.ts:4](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/float.ts#L4)

___

### resolveGuildCategoryChannel

▸ **resolveGuildCategoryChannel**(`parameter`, `guild`): [`Result`](../#result)<`CategoryChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildCategoryChannelError`](../enums/Identifiers#argumentguildcategorychannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Result`](../#result)<`CategoryChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildCategoryChannelError`](../enums/Identifiers#argumentguildcategorychannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/guildCategoryChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/guildCategoryChannel.ts#L7)

___

### resolveGuildChannel

▸ **resolveGuildChannel**(`parameter`, `guild`): [`Result`](../#result)<`GuildBasedChannelTypes`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Result`](../#result)<`GuildBasedChannelTypes`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/guildChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/guildChannel.ts#L7)

___

### resolveGuildNewsChannel

▸ **resolveGuildNewsChannel**(`parameter`, `guild`): [`Result`](../#result)<`NewsChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildNewsChannelError`](../enums/Identifiers#argumentguildnewschannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Result`](../#result)<`NewsChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildNewsChannelError`](../enums/Identifiers#argumentguildnewschannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/guildNewsChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/guildNewsChannel.ts#L7)

___

### resolveGuildNewsThreadChannel

▸ **resolveGuildNewsThreadChannel**(`parameter`, `guild`): [`Result`](../#result)<`ThreadChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildThreadChannelError`](../enums/Identifiers#argumentguildthreadchannelerror) \| [`ArgumentGuildNewsThreadChannelError`](../enums/Identifiers#argumentguildnewsthreadchannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Result`](../#result)<`ThreadChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildThreadChannelError`](../enums/Identifiers#argumentguildthreadchannelerror) \| [`ArgumentGuildNewsThreadChannelError`](../enums/Identifiers#argumentguildnewsthreadchannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/guildNewsThreadChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/guildNewsThreadChannel.ts#L7)

___

### resolveGuildPrivateThreadChannel

▸ **resolveGuildPrivateThreadChannel**(`parameter`, `guild`): [`Result`](../#result)<`ThreadChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildThreadChannelError`](../enums/Identifiers#argumentguildthreadchannelerror) \| [`ArgumentGuildPrivateThreadChannelError`](../enums/Identifiers#argumentguildprivatethreadchannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Result`](../#result)<`ThreadChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildThreadChannelError`](../enums/Identifiers#argumentguildthreadchannelerror) \| [`ArgumentGuildPrivateThreadChannelError`](../enums/Identifiers#argumentguildprivatethreadchannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/guildPrivateThreadChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/guildPrivateThreadChannel.ts#L7)

___

### resolveGuildPublicThreadChannel

▸ **resolveGuildPublicThreadChannel**(`parameter`, `guild`): [`Result`](../#result)<`ThreadChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildThreadChannelError`](../enums/Identifiers#argumentguildthreadchannelerror) \| [`ArgumentGuildPublicThreadChannelError`](../enums/Identifiers#argumentguildpublicthreadchannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Result`](../#result)<`ThreadChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildThreadChannelError`](../enums/Identifiers#argumentguildthreadchannelerror) \| [`ArgumentGuildPublicThreadChannelError`](../enums/Identifiers#argumentguildpublicthreadchannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/guildPublicThreadChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/guildPublicThreadChannel.ts#L7)

___

### resolveGuildStageVoiceChannel

▸ **resolveGuildStageVoiceChannel**(`parameter`, `guild`): [`Result`](../#result)<`StageChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildStageVoiceChannelError`](../enums/Identifiers#argumentguildstagevoicechannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Result`](../#result)<`StageChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildStageVoiceChannelError`](../enums/Identifiers#argumentguildstagevoicechannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/guildStageVoiceChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/guildStageVoiceChannel.ts#L7)

___

### resolveGuildTextChannel

▸ **resolveGuildTextChannel**(`parameter`, `guild`): [`Result`](../#result)<`TextChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildTextChannelError`](../enums/Identifiers#argumentguildtextchannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Result`](../#result)<`TextChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildTextChannelError`](../enums/Identifiers#argumentguildtextchannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/guildTextChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/guildTextChannel.ts#L7)

___

### resolveGuildThreadChannel

▸ **resolveGuildThreadChannel**(`parameter`, `guild`): [`Result`](../#result)<`ThreadChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildThreadChannelError`](../enums/Identifiers#argumentguildthreadchannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Result`](../#result)<`ThreadChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildThreadChannelError`](../enums/Identifiers#argumentguildthreadchannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/guildThreadChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/guildThreadChannel.ts#L7)

___

### resolveGuildVoiceChannel

▸ **resolveGuildVoiceChannel**(`parameter`, `guild`): [`Result`](../#result)<`VoiceChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildVoiceChannelError`](../enums/Identifiers#argumentguildvoicechannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Result`](../#result)<`VoiceChannel`, [`ArgumentGuildChannelError`](../enums/Identifiers#argumentguildchannelerror) \| [`ArgumentGuildVoiceChannelError`](../enums/Identifiers#argumentguildvoicechannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/guildVoiceChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/guildVoiceChannel.ts#L7)

___

### resolveHyperlink

▸ **resolveHyperlink**(`parameter`): [`Result`](../#result)<`URL`, [`ArgumentHyperlinkError`](../enums/Identifiers#argumenthyperlinkerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |

#### Returns

[`Result`](../#result)<`URL`, [`ArgumentHyperlinkError`](../enums/Identifiers#argumenthyperlinkerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/hyperlink.ts:5](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/hyperlink.ts#L5)

___

### resolveInteger

▸ **resolveInteger**(`parameter`, `options?`): [`Result`](../#result)<`number`, [`ArgumentIntegerError`](../enums/Identifiers#argumentintegererror) \| [`ArgumentIntegerTooSmall`](../enums/Identifiers#argumentintegertoosmall) \| [`ArgumentIntegerTooLarge`](../enums/Identifiers#argumentintegertoolarge)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `options?` | `Object` |
| `options.maximum?` | `number` |
| `options.minimum?` | `number` |

#### Returns

[`Result`](../#result)<`number`, [`ArgumentIntegerError`](../enums/Identifiers#argumentintegererror) \| [`ArgumentIntegerTooSmall`](../enums/Identifiers#argumentintegertoosmall) \| [`ArgumentIntegerTooLarge`](../enums/Identifiers#argumentintegertoolarge)\>

#### Defined in

[projects/framework/src/lib/resolvers/integer.ts:4](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/integer.ts#L4)

___

### resolveMember

▸ **resolveMember**(`parameter`, `guild`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`GuildMember`, [`ArgumentMemberError`](../enums/Identifiers#argumentmembererror)\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`GuildMember`, [`ArgumentMemberError`](../enums/Identifiers#argumentmembererror)\>\>

#### Defined in

[projects/framework/src/lib/resolvers/member.ts:6](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/member.ts#L6)

___

### resolveMessage

▸ **resolveMessage**(`parameter`, `options`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`Message`, [`ArgumentMessageError`](../enums/Identifiers#argumentmessageerror)\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `options` | `MessageResolverOptions` |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`Message`, [`ArgumentMessageError`](../enums/Identifiers#argumentmessageerror)\>\>

#### Defined in

[projects/framework/src/lib/resolvers/message.ts:14](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/message.ts#L14)

___

### resolveNumber

▸ **resolveNumber**(`parameter`, `options?`): [`Result`](../#result)<`number`, [`ArgumentNumberError`](../enums/Identifiers#argumentnumbererror) \| [`ArgumentNumberTooSmall`](../enums/Identifiers#argumentnumbertoosmall) \| [`ArgumentNumberTooLarge`](../enums/Identifiers#argumentnumbertoolarge)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `options?` | `Object` |
| `options.maximum?` | `number` |
| `options.minimum?` | `number` |

#### Returns

[`Result`](../#result)<`number`, [`ArgumentNumberError`](../enums/Identifiers#argumentnumbererror) \| [`ArgumentNumberTooSmall`](../enums/Identifiers#argumentnumbertoosmall) \| [`ArgumentNumberTooLarge`](../enums/Identifiers#argumentnumbertoolarge)\>

#### Defined in

[projects/framework/src/lib/resolvers/number.ts:4](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/number.ts#L4)

___

### resolvePartialDMChannel

▸ **resolvePartialDMChannel**(`parameter`, `message`): [`Result`](../#result)<`DMChannel` \| `PartialDMChannel`, [`ArgumentChannelError`](../enums/Identifiers#argumentchannelerror) \| [`ArgumentDMChannelError`](../enums/Identifiers#argumentdmchannelerror)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> |

#### Returns

[`Result`](../#result)<`DMChannel` \| `PartialDMChannel`, [`ArgumentChannelError`](../enums/Identifiers#argumentchannelerror) \| [`ArgumentDMChannelError`](../enums/Identifiers#argumentdmchannelerror)\>

#### Defined in

[projects/framework/src/lib/resolvers/partialDMChannel.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/partialDMChannel.ts#L7)

___

### resolveRole

▸ **resolveRole**(`parameter`, `guild`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`Role`, [`ArgumentRoleError`](../enums/Identifiers#argumentroleerror)\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `guild` | [`Guild`](https://discord.js.org/#/docs/main/stable/class/Guild) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`Role`, [`ArgumentRoleError`](../enums/Identifiers#argumentroleerror)\>\>

#### Defined in

[projects/framework/src/lib/resolvers/role.ts:6](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/role.ts#L6)

___

### resolveString

▸ **resolveString**(`parameter`, `options?`): [`Result`](../#result)<`string`, [`ArgumentStringTooShort`](../enums/Identifiers#argumentstringtooshort) \| [`ArgumentStringTooLong`](../enums/Identifiers#argumentstringtoolong)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |
| `options?` | `Object` |
| `options.maximum?` | `number` |
| `options.minimum?` | `number` |

#### Returns

[`Result`](../#result)<`string`, [`ArgumentStringTooShort`](../enums/Identifiers#argumentstringtooshort) \| [`ArgumentStringTooLong`](../enums/Identifiers#argumentstringtoolong)\>

#### Defined in

[projects/framework/src/lib/resolvers/string.ts:4](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/string.ts#L4)

___

### resolveUser

▸ **resolveUser**(`parameter`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`User`, [`ArgumentUserError`](../enums/Identifiers#argumentusererror)\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `parameter` | `string` |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`User`, [`ArgumentUserError`](../enums/Identifiers#argumentusererror)\>\>

#### Defined in

[projects/framework/src/lib/resolvers/user.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/resolvers/user.ts#L7)

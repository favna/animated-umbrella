---
id: "sapphire_discord_js_utilities.MessageBuilder"
title: "Class: MessageBuilder"
sidebar_label: "MessageBuilder"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).MessageBuilder

A message builder class, it implements the {@link MessageOptions} interface.

## Implements

- [`MessageOptions`](https://discord.js.org/#/docs/main/stable/typedef/MessageOptions)

## Constructors

### constructor

• **new MessageBuilder**(`options?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`MessageBuilderResolvable`](../modules/sapphire_discord_js_utilities#messagebuilderresolvable) |

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:45](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L45)

## Properties

### allowedMentions

• `Optional` **allowedMentions**: `MessageMentionOptions`

Which mentions should be parsed from the message content.

#### Implementation of

MessageOptions.allowedMentions

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:37](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L37)

___

### content

• `Optional` **content**: ``null`` \| `string`

The content for the message. If set to undefined and the builder is used to edit, the content will not be
replaced.

#### Implementation of

MessageOptions.content

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:26](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L26)

___

### embeds

• `Optional` **embeds**: ([`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` \| `APIEmbed`)[]

The embeds for the message. If set to undefined and the builder is used to edit, the embed will not be replaced.

**`remark`** There is a maximum of 10 embeds in 1 message

#### Implementation of

MessageOptions.embeds

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:32](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L32)

___

### files

• `Optional` **files**: (`FileOptions` \| `BufferResolvable` \| `Stream` \| [`MessageAttachment`](https://discord.js.org/#/docs/main/stable/class/MessageAttachment))[]

Files to send with the message. This should not be set when editing a message, as Discord does not support
editing file attachments.

#### Implementation of

MessageOptions.files

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:43](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L43)

___

### nonce

• `Optional` **nonce**: `string` \| `number`

The nonce for the message.

**`default`** ''

#### Implementation of

MessageOptions.nonce

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:20](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L20)

___

### tts

• `Optional` **tts**: `boolean`

Whether or not the message should be spoken aloud.

**`default`** false

#### Implementation of

MessageOptions.tts

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:14](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L14)

___

### defaults

▪ `Static` **defaults**: [`MessageBuilderResolvable`](../modules/sapphire_discord_js_utilities#messagebuilderresolvable) = `{}`

The default values for all MessageBuilder instances.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:139](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L139)

## Methods

### addFile

▸ **addFile**(`file`): [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

Adds a new value for the [MessageBuilder.files](sapphire_discord_js_utilities.MessageBuilder#files) field array.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `file` | `FileOptions` \| `BufferResolvable` \| `Stream` \| [`MessageAttachment`](https://discord.js.org/#/docs/main/stable/class/MessageAttachment) | The file to add to the [MessageBuilder.files](sapphire_discord_js_utilities.MessageBuilder#files) field array. |

#### Returns

[`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:111](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L111)

___

### setAllowedMentions

▸ **setAllowedMentions**(`allowedMentions?`): [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

Sets the value for the [MessageBuilder.allowedMentions](sapphire_discord_js_utilities.MessageBuilder#allowedmentions) field.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `allowedMentions?` | `MessageMentionOptions` | Which mentions should be parsed from the message content. |

#### Returns

[`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:102](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L102)

___

### setContent

▸ **setContent**(`content?`): [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

Sets the value for the [MessageBuilder.content](sapphire_discord_js_utilities.MessageBuilder#content) field.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `content?` | `string` | The content for the message. If set to undefined and the builder is used to edit, the content will not be replaced. |

#### Returns

[`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:77](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L77)

___

### setEmbeds

▸ **setEmbeds**(`embeds?`): [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

Sets the value for the {@link MessageBuilder.embed} field.

**`remark`** When providing more than 10 embeds, the array will automatically be sliced down to the first 10.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `embeds?` | ([`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` \| `APIEmbed`)[] | The embeds for the message. If set to undefined and the builder is used to edit, the embed will not be replaced. There is a maximum of 10 embeds per message |

#### Returns

[`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:88](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L88)

___

### setFile

▸ **setFile**(`file`): [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

Sets a single value for the [MessageBuilder.files](sapphire_discord_js_utilities.MessageBuilder#files) field array.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `file` | `FileOptions` \| `BufferResolvable` \| `Stream` \| [`MessageAttachment`](https://discord.js.org/#/docs/main/stable/class/MessageAttachment) | The file to send with the message. This should not be set when editing a message, as Discord does not support editing file attachments. |

#### Returns

[`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:121](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L121)

___

### setFiles

▸ **setFiles**(`files?`): [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

Sets the value for the [MessageBuilder.files](sapphire_discord_js_utilities.MessageBuilder#files) field.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `files?` | (`FileOptions` \| `BufferResolvable` \| `Stream` \| [`MessageAttachment`](https://discord.js.org/#/docs/main/stable/class/MessageAttachment))[] | The files to send with the message. This should not be set when editing a message, as Discord does not support editing file attachments. |

#### Returns

[`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:131](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L131)

___

### setNonce

▸ **setNonce**(`nonce?`): [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

Sets the value for the [MessageBuilder.nonce](sapphire_discord_js_utilities.MessageBuilder#nonce) field.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `nonce?` | `string` | The nonce for the message. |

#### Returns

[`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:67](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L67)

___

### setTTS

▸ **setTTS**(`tts?`): [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

Sets the value for the [MessageBuilder.tts](sapphire_discord_js_utilities.MessageBuilder#tts) field.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tts?` | `boolean` | Whether or not the message should be spoken aloud. |

#### Returns

[`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts:58](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/builders/MessageBuilder.ts#L58)

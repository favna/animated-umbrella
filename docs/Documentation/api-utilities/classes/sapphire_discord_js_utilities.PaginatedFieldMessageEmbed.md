---
id: "sapphire_discord_js_utilities.PaginatedFieldMessageEmbed"
title: "Class: PaginatedFieldMessageEmbed<T>"
sidebar_label: "PaginatedFieldMessageEmbed"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).PaginatedFieldMessageEmbed

This is a utility of [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage), except it exclusively paginates the fields of an embed.
You must either use this class directly or extend it.

**`example`**
```typescript
import { PaginatedFieldMessageEmbed } from '@sapphire/discord.js-utilities';

new PaginatedFieldMessageEmbed()
   .setTitleField('Test pager field')
   .setTemplate({ embed })
   .setItems([
      { title: 'Sapphire Framework', value: 'discord.js Framework' },
      { title: 'Sapphire Framework 2', value: 'discord.js Framework 2' },
      { title: 'Sapphire Framework 3', value: 'discord.js Framework 3' }
    ])
   .formatItems((item) => `${item.title}\n${item.value}`)
   .setItemsPerPage(2)
   .make()
   .run(message);
```

## Type parameters

| Name |
| :------ |
| `T` |

## Hierarchy

- [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

  ↳ **`PaginatedFieldMessageEmbed`**

## Constructors

### constructor

• **new PaginatedFieldMessageEmbed**<`T`\>(`__namedParameters?`)

Constructor for the [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) class

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `__namedParameters` | [`PaginatedMessageOptions`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageOptions) | The [PaginatedMessageOptions](../interfaces/sapphire_discord_js_utilities.PaginatedMessageOptions) for this instance of the [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) class |

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[constructor](sapphire_discord_js_utilities.PaginatedMessage#constructor)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:178](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L178)

## Properties

### actions

• **actions**: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<`string`, [`PaginatedMessageAction`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction)\>

The actions which are to be used.

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[actions](sapphire_discord_js_utilities.PaginatedMessage#actions)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:131](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L131)

___

### collector

• **collector**: ``null`` \| [`InteractionCollector`](https://discord.js.org/#/docs/main/stable/class/InteractionCollector)<[`MessageComponentInteraction`](https://discord.js.org/#/docs/main/stable/class/MessageComponentInteraction)<`CacheType`\>\> = `null`

The collector used for handling button clicks.

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[collector](sapphire_discord_js_utilities.PaginatedMessage#collector)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:121](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L121)

___

### constructor

• **constructor**: typeof [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Inherited from

PaginatedMessage.constructor

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1153](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1153)

___

### embedFooterSeparator

• **embedFooterSeparator**: `string` = `PaginatedMessage.embedFooterSeparator`

Custom separator to show after the page index in the embed footer.
PaginatedMessage will automatically add a space (` `) after the given text. You do not have to add it yourself.

**`default`** ```PaginatedMessage.pageIndexPrefix``` (static property)

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[embedFooterSeparator](sapphire_discord_js_utilities.PaginatedMessage#embedfooterseparator)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:161](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L161)

___

### embedTemplate

• `Private` **embedTemplate**: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:27](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L27)

___

### fieldTitle

• `Private` **fieldTitle**: `string` = `''`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:31](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L31)

___

### hasEmittedWarning

• `Protected` **hasEmittedWarning**: `boolean` = `false`

Tracks whether a warning was already emitted for this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[hasEmittedWarning](sapphire_discord_js_utilities.PaginatedMessage#hasemittedwarning)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:172](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L172)

___

### idle

• **idle**: `number`

The amount of milliseconds to idle before the paginator is closed. Defaults to 20 minutes.

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[idle](sapphire_discord_js_utilities.PaginatedMessage#idle)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:141](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L141)

___

### index

• **index**: `number` = `0`

The handler's current page/message index.

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[index](sapphire_discord_js_utilities.PaginatedMessage#index)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:136](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L136)

___

### items

• `Private` **items**: `T`[] = `[]`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:29](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L29)

___

### itemsPerPage

• `Private` **itemsPerPage**: `number` = `10`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:30](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L30)

___

### messages

• **messages**: (``null`` \| [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage))[] = `[]`

The pages which were converted from [PaginatedMessage.pages](sapphire_discord_js_utilities.PaginatedMessage#pages)

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[messages](sapphire_discord_js_utilities.PaginatedMessage#messages)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:126](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L126)

___

### pageIndexPrefix

• **pageIndexPrefix**: `string` = `PaginatedMessage.pageIndexPrefix`

Custom text to show in front of the page index in the embed footer.
PaginatedMessage will automatically add a space (` `) after the given text. You do not have to add it yourself.

**`default`** ```PaginatedMessage.pageIndexPrefix``` (static property)

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[pageIndexPrefix](sapphire_discord_js_utilities.PaginatedMessage#pageindexprefix)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:154](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L154)

___

### pages

• **pages**: [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage)[]

The pages to be converted to [PaginatedMessage.messages](sapphire_discord_js_utilities.PaginatedMessage#messages)

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[pages](sapphire_discord_js_utilities.PaginatedMessage#pages)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:111](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L111)

___

### paginatedMessageData

• `Protected` **paginatedMessageData**: ``null`` \| `Omit`<[`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion), ``"components"``\> = `null`

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[paginatedMessageData](sapphire_discord_js_utilities.PaginatedMessage#paginatedmessagedata)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:163](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L163)

___

### response

• **response**: ``null`` \| [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> = `null`

The response message used to edit on page changes.

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[response](sapphire_discord_js_utilities.PaginatedMessage#response)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:116](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L116)

___

### selectMenuOptions

• `Protected` **selectMenuOptions**: [`PaginatedMessageSelectMenuOptionsFunction`](../modules/sapphire_discord_js_utilities#paginatedmessageselectmenuoptionsfunction) = `PaginatedMessage.selectMenuOptions`

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[selectMenuOptions](sapphire_discord_js_utilities.PaginatedMessage#selectmenuoptions)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:165](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L165)

___

### template

• **template**: [`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion)

The template for this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).
You can use templates to set defaults that will apply to each and every page in the [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[template](sapphire_discord_js_utilities.PaginatedMessage#template)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:147](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L147)

___

### totalPages

• `Private` **totalPages**: `number` = `0`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:28](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L28)

___

### wrongUserInteractionReply

• `Protected` **wrongUserInteractionReply**: [`PaginatedMessageWrongUserInteractionReplyFunction`](../modules/sapphire_discord_js_utilities#paginatedmessagewronguserinteractionreplyfunction) = `PaginatedMessage.wrongUserInteractionReply`

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[wrongUserInteractionReply](sapphire_discord_js_utilities.PaginatedMessage#wronguserinteractionreply)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:167](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L167)

___

### defaultActions

▪ `Static` **defaultActions**: [`PaginatedMessageAction`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction)[]

The default actions of this handler.

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[defaultActions](sapphire_discord_js_utilities.PaginatedMessage#defaultactions)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:952](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L952)

___

### deletionStopReasons

▪ `Static` **deletionStopReasons**: `string`[]

The reasons sent by [InteractionCollector#end](https://discord.js.org/#/docs/main/stable/class/InteractionCollector?scrollTo=e-end)
event when the message (or its owner) has been deleted.

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[deletionStopReasons](sapphire_discord_js_utilities.PaginatedMessage#deletionstopreasons)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1014](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1014)

___

### embedFooterSeparator

▪ `Static` **embedFooterSeparator**: `string` = `'•'`

Custom separator for the page index in the embed footer.

**`default`** "•"

**`remark`** To overwrite this property change it somewhere in a "setup" file, i.e. where you also call `client.login()` for your bot.
Alternatively, you can also customize it on a per-PaginatedMessage basis by passing `embedFooterSeparator` in the options of the constructor.

**`example`**
```typescript
import { PaginatedMessage } from '@sapphire/discord.js-utilities';

PaginatedMessage.embedFooterSeparator = '|';
// This will make the separator of the embed footer something like "Page 1/2 | Today at 4:20"
```

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[embedFooterSeparator](sapphire_discord_js_utilities.PaginatedMessage#embedfooterseparator)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1044](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1044)

___

### handlers

▪ `Static` `Readonly` **handlers**: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<`string`, [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)\>

The current {@link InteractionCollector} handlers that are active.
The key is the ID of of the author who sent the message that triggered this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

This is to ensure that any given author can only trigger 1 [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).
This is important for performance reasons, and users should not have more than 1 [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) open at once.

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[handlers](sapphire_discord_js_utilities.PaginatedMessage#handlers)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1062](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1062)

___

### messages

▪ `Static` `Readonly` **messages**: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<`string`, [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)\>

The messages that are currently being handled by a [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)
The key is the ID of the message that triggered this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

This is to ensure that only 1 [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) can run on a specified message at once.
This is important when having an editable commands solution.

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[messages](sapphire_discord_js_utilities.PaginatedMessage#messages)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1053](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1053)

___

### pageIndexPrefix

▪ `Static` **pageIndexPrefix**: `string` = `''`

Custom text to show in front of the page index in the embed footer.
PaginatedMessage will automatically add a space (` `) after the given text. You do not have to add it yourself.

**`default`** ""

**`remark`** To overwrite this property change it somewhere in a "setup" file, i.e. where you also call `client.login()` for your bot.

**`example`**
```typescript
import { PaginatedMessage } from '@sapphire/discord.js-utilities';

PaginatedMessage.pageIndexPrefix = 'Page';
// This will make the footer of the embed something like "Page 1/2"
```

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[pageIndexPrefix](sapphire_discord_js_utilities.PaginatedMessage#pageindexprefix)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1029](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1029)

___

### selectMenuOptions

▪ `Static` **selectMenuOptions**: [`PaginatedMessageSelectMenuOptionsFunction`](../modules/sapphire_discord_js_utilities#paginatedmessageselectmenuoptionsfunction)

A generator for {@link MessageSelectOption} that will be used to generate the options for the {@link MessageSelectMenu}.
We do not allow overwriting the {@link MessageSelectOption#value} property with this, as it is vital to how we handle
select menu interactions.

**`param`** The index of the page to add to the {@link MessageSelectMenu}. We will add 1 to this number because our pages are 0 based,
so this will represent the pages as seen by the user.

**`default`**
```ts
{
	label: `Page ${pageIndex}`
}
```

**`remark`** To overwrite this property change it in a "setup" file prior to calling `client.login()` for your bot.

**`example`**
```typescript
import { PaginatedMessage } from '@sapphire/discord.js-utilities';

PaginatedMessage.selectMenuOptions = (pageIndex) => ({
	 label: `Go to page: ${pageIndex}`,
	 description: 'This is a description'
});
```

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[selectMenuOptions](sapphire_discord_js_utilities.PaginatedMessage#selectmenuoptions)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1089](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1089)

___

### wrongUserInteractionReply

▪ `Static` **wrongUserInteractionReply**: [`PaginatedMessageWrongUserInteractionReplyFunction`](../modules/sapphire_discord_js_utilities#paginatedmessagewronguserinteractionreplyfunction)

A generator for {@link MessageComponentInteraction#reply} that will be called and sent whenever an untargeted user interacts with one of the buttons.
When modifying this it is recommended that the message is set to be ephemeral so only the user that is pressing the buttons can see them.
Furthermore, we also recommend setting `allowedMentions: { users: [], roles: [] }`, so you don't have to worry about accidentally pinging anyone.

When setting just a string, we will add `{ ephemeral: true, allowedMentions: { users: [], roles: [] } }` for you.

**`param`** The {@link User} this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) was intended for.

**`param`** The {@link User} that actually clicked the button.

**`default`**
```ts
{
	content: `Please stop clicking the buttons on this message. They are only for ${Formatters.userMention(targetUser.id)}.`,
	ephemeral: true,
	allowedMentions: { users: [], roles: [] }
}
```

**`remark`** To overwrite this property change it in a "setup" file prior to calling `client.login()` for your bot.

**`example`**
```typescript
import { PaginatedMessage } from '@sapphire/discord.js-utilities';

// We  will add ephemeral and no allowed mention for string only overwrites
PaginatedMessage.wrongUserInteractionReply = (targetUser) =>
    `These buttons are only for ${Formatters.userMention(targetUser.id)}. Press them as much as you want, but I won't do anything with your clicks.`;
```

**`example`**
```typescript
import { PaginatedMessage } from '@sapphire/discord.js-utilities';
import { Formatters } from 'discord.js';

PaginatedMessage.wrongUserInteractionReply = (targetUser) => ({
	content: `These buttons are only for ${Formatters.userMention(
		targetUser.id
	)}. Press them as much as you want, but I won't do anything with your clicks.`,
	ephemeral: true,
	allowedMentions: { users: [], roles: [] }
});
```

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[wrongUserInteractionReply](sapphire_discord_js_utilities.PaginatedMessage#wronguserinteractionreply)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1133](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1133)

## Methods

### addAction

▸ **addAction**(`action`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Adds an action to the existing ones. This will be added as the last action.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `action` | [`PaginatedMessageAction`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction) | The action to add. |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addAction](sapphire_discord_js_utilities.PaginatedMessage#addaction)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:266](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L266)

___

### addActions

▸ **addActions**(`actions`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Adds actions to the existing ones. The order given is the order they will be used.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `actions` | [`PaginatedMessageAction`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction)[] | The actions to add. |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addActions](sapphire_discord_js_utilities.PaginatedMessage#addactions)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:257](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L257)

___

### addAsyncPageBuilder

▸ **addAsyncPageBuilder**(`builder`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Adds a page to the existing ones asynchronously using a [MessageBuilder](sapphire_discord_js_utilities.MessageBuilder). This wil be added as the last page.

**`example`**
```typescript
const { PaginatedMessage } = require('@sapphire/discord.js-utilities');
const { MessageEmbed } = require('discord.js');

const paginatedMessage = new PaginatedMessage()
	.addAsyncPageBuilder(async (builder) => {
		const someRemoteData = await fetch('https://contoso.com/api/users');

		const embed = new MessageEmbed()
			.setColor('#FF0000')
			.setDescription(someRemoteData.data);

		return builder
			.setContent('example content')
			.setEmbed(embed);
});
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `builder` | [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder) \| (`builder`: [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)) => [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)\> | Either a callback whose first parameter is `new MessageBuilder()`, or an already constructed [MessageBuilder](sapphire_discord_js_utilities.MessageBuilder) |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addAsyncPageBuilder](sapphire_discord_js_utilities.PaginatedMessage#addasyncpagebuilder)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:385](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L385)

___

### addAsyncPageEmbed

▸ **addAsyncPageEmbed**(`embed`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Adds a page to the existing ones asynchronously using a {@link MessageEmbed}. This wil be added as the last page.

**`example`**
```typescript
const { PaginatedMessage } = require('@sapphire/discord.js-utilities');

const paginatedMessage = new PaginatedMessage()
	.addAsyncPageEmbed(async (embed) => {
		const someRemoteData = await fetch('https://contoso.com/api/users');

		embed
			.setColor('#FF0000')
			.setDescription(someRemoteData.data);

		return embed;
});
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `embed` | [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| (`builder`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)) => [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)\> | Either a callback whose first parameter is `new MessageEmbed()`, or an already constructed {@link MessageEmbed} |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addAsyncPageEmbed](sapphire_discord_js_utilities.PaginatedMessage#addasyncpageembed)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:455](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L455)

___

### addAsyncPageEmbeds

▸ **addAsyncPageEmbeds**(`embeds`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Adds a page to the existing ones using multiple {@link MessageEmbed}'s. This wil be added as the last page.

**`remark`** When using this with a callback this will construct 10 {@link MessageEmbed}'s in the callback parameters, regardless of how many are actually used.
If this a performance impact you do not want to cope with then it is recommended to use [PaginatedMessage.addPageBuilder](sapphire_discord_js_utilities.PaginatedMessage#addpagebuilder) instead, which will let you add
as many embeds as you want, albeit manually

**`example`**
```typescript
const { PaginatedMessage } = require('@sapphire/discord.js-utilities');

const paginatedMessage = new PaginatedMessage().addAsyncPageEmbeds(async (embed0, embed1, embed2) => {
	const someRemoteData = (await fetch('https://contoso.com/api/users')) as any;

	for (const [index, user] of Object.entries(someRemoteData.users.slice(0, 10)) as [`${0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10}`, any][]) {
		switch (index) {
			case '0': {
				embed0.setColor('#FF0000').setDescription('example description 1').setAuthor(user.name);
				break;
			}
			case '1': {
				embed1.setColor('#00FF00').setDescription('example description 2').setAuthor(user.name);
				break;
			}
			case '2': {
				embed2.setColor('#0000FF').setDescription('example description 3').setAuthor(user.name);
				break;
			}
		}
	}

	return [embed0, embed1, embed2];
});
```

**`example`**
```typescript
const { PaginatedMessage } = require('@sapphire/discord.js-utilities');

const embed1 = new MessageEmbed()
	.setColor('#FF0000')
	.setDescription('example description 1');

const embed2 = new MessageEmbed()
	.setColor('#00FF00')
	.setDescription('example description 2');

const embed3 = new MessageEmbed()
	.setColor('#0000FF')
	.setDescription('example description 3');

const paginatedMessage = new PaginatedMessage()
	.addAsyncPageEmbeds([embed1, embed2, embed3]); // You can add up to 10 embeds
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `embeds` | [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)[] \| (`embed1`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed2`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed3`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed4`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed5`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed6`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed7`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed8`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed9`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed10`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)) => [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)[]\> | Either a callback which receives 10 parameters of `new MessageEmbed()`, or an array of already constructed {@link MessageEmbed}'s |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addAsyncPageEmbeds](sapphire_discord_js_utilities.PaginatedMessage#addasyncpageembeds)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:597](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L597)

___

### addPage

▸ **addPage**(`page`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Adds a page to the existing ones. This will be added as the last page.

**`remark`** While you can use this method you should first check out
[PaginatedMessage.addPageBuilder](sapphire_discord_js_utilities.PaginatedMessage#addpagebuilder),
[PaginatedMessage.addPageContent](sapphire_discord_js_utilities.PaginatedMessage#addpagecontent) and
[PaginatedMessage.addPageEmbed](sapphire_discord_js_utilities.PaginatedMessage#addpageembed) as
these are easier functional methods of adding pages and will likely already suffice for your needs.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `page` | [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage) | The page to add. |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addPage](sapphire_discord_js_utilities.PaginatedMessage#addpage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:300](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L300)

___

### addPageBuilder

▸ **addPageBuilder**(`builder`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Adds a page to the existing ones using a [MessageBuilder](sapphire_discord_js_utilities.MessageBuilder). This will be added as the last page.

**`example`**
```typescript
const { PaginatedMessage } = require('@sapphire/discord.js-utilities');
const { MessageEmbed } = require('discord.js');

const paginatedMessage = new PaginatedMessage()
	.addPageBuilder((builder) => {
		const embed = new MessageEmbed()
			.setColor('#FF0000')
			.setDescription('example description');

		return builder
			.setContent('example content')
			.setEmbed(embed);
});
```

**`example`**
```typescript
const { MessageEmbed } = require('discord.js');
const { MessageBuilder, PaginatedMessage } = require('@sapphire/discord.js-utilities');

const embed = new MessageEmbed()
	.setColor('#FF0000')
	.setDescription('example description');

const builder = new MessageBuilder()
	.setContent('example content')
	.setEmbed(embed);

const paginatedMessage = new PaginatedMessage()
	.addPageBuilder(builder);
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `builder` | [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder) \| (`builder`: [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder)) => [`MessageBuilder`](sapphire_discord_js_utilities.MessageBuilder) | Either a callback whose first parameter is `new MessageBuilder()`, or an already constructed [MessageBuilder](sapphire_discord_js_utilities.MessageBuilder) |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addPageBuilder](sapphire_discord_js_utilities.PaginatedMessage#addpagebuilder)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:359](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L359)

___

### addPageContent

▸ **addPageContent**(`content`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Adds a page to the existing ones using simple message content. This will be added as the last page.

**`example`**
```typescript
const { PaginatedMessage } = require('@sapphire/discord.js-utilities');

const paginatedMessage = new PaginatedMessage()
	.addPageContent('example content');
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `content` | `string` | The content to set. |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addPageContent](sapphire_discord_js_utilities.PaginatedMessage#addpagecontent)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:400](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L400)

___

### addPageEmbed

▸ **addPageEmbed**(`embed`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Adds a page to the existing ones using a {@link MessageEmbed}. This wil be added as the last page.

**`example`**
```typescript
const { PaginatedMessage } = require('@sapphire/discord.js-utilities');

const paginatedMessage = new PaginatedMessage()
	.addPageEmbed((embed) => {
		embed
			.setColor('#FF0000')
			.setDescription('example description');

		return embed;
});
```

**`example`**
```typescript
const { PaginatedMessage } = require('@sapphire/discord.js-utilities');

const embed = new MessageEmbed()
	.setColor('#FF0000')
	.setDescription('example description');

const paginatedMessage = new PaginatedMessage()
	.addPageEmbed(embed);
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `embed` | [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| (`embed`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)) => [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) | Either a callback whose first parameter is `new MessageEmbed()`, or an already constructed {@link MessageEmbed} |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addPageEmbed](sapphire_discord_js_utilities.PaginatedMessage#addpageembed)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:432](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L432)

___

### addPageEmbeds

▸ **addPageEmbeds**(`embeds`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Adds a page to the existing ones asynchronously using multiple {@link MessageEmbed}'s. This wil be added as the last page.

**`remark`** When using this with a callback this will construct 10 {@link MessageEmbed}'s in the callback parameters, regardless of how many are actually used.
If this a performance impact you do not want to cope with then it is recommended to use [PaginatedMessage.addPageBuilder](sapphire_discord_js_utilities.PaginatedMessage#addpagebuilder) instead, which will let you add
as many embeds as you want, albeit manually

**`example`**
```typescript
const { PaginatedMessage } = require('@sapphire/discord.js-utilities');

const paginatedMessage = new PaginatedMessage()
	.addPageEmbeds((embed1, embed2, embed3) => { // You can add up to 10 embeds
		embed1
			.setColor('#FF0000')
			.setDescription('example description 1');

		embed2
			.setColor('#00FF00')
			.setDescription('example description 2');

		embed3
			.setColor('#0000FF')
			.setDescription('example description 3');

		return [embed1, embed2, embed3];
});
```

**`example`**
```typescript
const { PaginatedMessage } = require('@sapphire/discord.js-utilities');

const embed1 = new MessageEmbed()
	.setColor('#FF0000')
	.setDescription('example description 1');

const embed2 = new MessageEmbed()
	.setColor('#00FF00')
	.setDescription('example description 2');

const embed3 = new MessageEmbed()
	.setColor('#0000FF')
	.setDescription('example description 3');

const paginatedMessage = new PaginatedMessage()
	.addPageEmbeds([embed1, embed2, embed3]); // You can add up to 10 embeds
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `embeds` | [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)[] \| (`embed1`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed2`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed3`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed4`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed5`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed6`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed7`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed8`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed9`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed), `embed10`: [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)) => [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed)[] | Either a callback which receives 10 parameters of `new MessageEmbed()`, or an array of already constructed {@link MessageEmbed}'s |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addPageEmbeds](sapphire_discord_js_utilities.PaginatedMessage#addpageembeds)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:506](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L506)

___

### addPages

▸ **addPages**(`pages`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Add pages to the existing ones. The order given is the order they will be used.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pages` | [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage)[] | The pages to add. |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[addPages](sapphire_discord_js_utilities.PaginatedMessage#addpages)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:641](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L641)

___

### applyFooter

▸ `Protected` **applyFooter**(`message`, `index`): [`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion)

#### Parameters

| Name | Type |
| :------ | :------ |
| `message` | [`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion) |
| `index` | `number` |

#### Returns

[`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion)

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[applyFooter](sapphire_discord_js_utilities.PaginatedMessage#applyfooter)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:868](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L868)

___

### clone

▸ **clone**(): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Clones the current handler into a new instance.

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[clone](sapphire_discord_js_utilities.PaginatedMessage#clone)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:715](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L715)

___

### formatItems

▸ **formatItems**(`formatter`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Sets a format callback that will be mapped to each embed field in the array of items when the embed is paginated. This should convert each item to a format that is either text itself or can be serialized as text.

**`example`**
```typescript
import { PaginatedFieldMessageEmbed } from '@sapphire/discord.js-utilities';

new PaginatedFieldMessageEmbed()
   .setTitleField('Test field')
   .setTemplate({ embed })
   .setItems([
      { title: 'Sapphire Framework', value: 'discord.js Framework' },
      { title: 'Sapphire Framework 2', value: 'discord.js Framework 2' },
      { title: 'Sapphire Framework 3', value: 'discord.js Framework 3' }
    ])
   .formatItems((item) => `${item.title}\n${item.value}`)
   .make()
   .run(message);
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `formatter` | (`item`: `T`, `index`: `number`, `array`: `T`[]) => `any` |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:107](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L107)

___

### generatePages

▸ `Private` **generatePages**(): `void`

#### Returns

`void`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:144](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L144)

___

### handleCollect

▸ `Protected` **handleCollect**(`targetUser`, `channel`, `interaction`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Handles the `collect` event from the collector.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `targetUser` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) | The user the handler is for. |
| `channel` | [`DMChannel`](https://discord.js.org/#/docs/main/stable/class/DMChannel) \| `PartialDMChannel` \| [`NewsChannel`](https://discord.js.org/#/docs/main/stable/class/NewsChannel) \| [`TextChannel`](https://discord.js.org/#/docs/main/stable/class/TextChannel) \| [`ThreadChannel`](https://discord.js.org/#/docs/main/stable/class/ThreadChannel) | The channel the handler is running at. |
| `interaction` | [`ButtonInteraction`](https://discord.js.org/#/docs/main/stable/class/ButtonInteraction)<`CacheType`\> \| [`SelectMenuInteraction`](https://discord.js.org/#/docs/main/stable/class/SelectMenuInteraction)<`CacheType`\> | The button interaction that was received. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[handleCollect](sapphire_discord_js_utilities.PaginatedMessage#handlecollect)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:812](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L812)

___

### handleEnd

▸ `Protected` **handleEnd**(`_`, `reason`): `void`

Handles the `end` event from the collector.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_` | `Collection`<`string`, [`ButtonInteraction`](https://discord.js.org/#/docs/main/stable/class/ButtonInteraction)<`CacheType`\> \| [`SelectMenuInteraction`](https://discord.js.org/#/docs/main/stable/class/SelectMenuInteraction)<`CacheType`\>\> | - |
| `reason` | `string` | The reason for which the collector was ended. |

#### Returns

`void`

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[handleEnd](sapphire_discord_js_utilities.PaginatedMessage#handleend)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:858](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L858)

___

### handlePageLoad

▸ `Protected` **handlePageLoad**(`page`, `index`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion)\>

Handles the load of a page.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `page` | [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage) | The page to be loaded. |
| `index` | `number` | The index of the current page. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion)\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[handlePageLoad](sapphire_discord_js_utilities.PaginatedMessage#handlepageload)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:792](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L792)

___

### hasPage

▸ **hasPage**(`index`): `boolean`

Checks whether or not the handler has a specific page.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `index` | `number` | The index to check. |

#### Returns

`boolean`

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[hasPage](sapphire_discord_js_utilities.PaginatedMessage#haspage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:275](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L275)

___

### make

▸ **make**(): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Build the pages of the given array.

You must call the [PaginatedFieldMessageEmbed.make](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed#make) and [PaginatedFieldMessageEmbed.run](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed#run) methods last, in that order, for the pagination to work.

**`example`**
```typescript
import { PaginatedFieldMessageEmbed } from '@sapphire/discord.js-utilities';

new PaginatedFieldMessageEmbed()
   .setTitleField('Test field')
   .setTemplate({ embed })
   .setItems([
      { title: 'Sapphire Framework', value: 'discord.js Framework' },
      { title: 'Sapphire Framework 2', value: 'discord.js Framework 2' },
      { title: 'Sapphire Framework 3', value: 'discord.js Framework 3' }
    ])
   .formatItems((item) => `${item.title}\n${item.value}`)
   .make()
   .run(message);
```

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:134](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L134)

___

### paginateArray

▸ `Private` **paginateArray**(`items`, `currentPage`, `perPageItems`): `T`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `items` | `T`[] |
| `currentPage` | `number` |
| `perPageItems` | `number` |

#### Returns

`T`[]

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:160](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L160)

___

### resolvePage

▸ **resolvePage**(`index`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage)\>

Executed whenever an action is triggered and resolved.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `index` | `number` | The index to resolve. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage)\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[resolvePage](sapphire_discord_js_utilities.PaginatedMessage#resolvepage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:698](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L698)

___

### resolvePagesOnRun

▸ **resolvePagesOnRun**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Executed whenever [PaginatedMessage.run](sapphire_discord_js_utilities.PaginatedMessage#run) is called.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[resolvePagesOnRun](sapphire_discord_js_utilities.PaginatedMessage#resolvepagesonrun)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:690](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L690)

___

### run

▸ **run**(`message`, `target?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>\>

Executes the [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) and sends the pages corresponding with [PaginatedMessage.index](sapphire_discord_js_utilities.PaginatedMessage#index).
The handler will start collecting message button interactions.

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> | `undefined` | The message that triggered this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage). Generally this will be the command message, but it can also be another message from your client, i.e. to indicate a loading state. |
| `target` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) | `message.author` | The user who will be able to interact with the message buttons of this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage). Defaults to `message.author`. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[run](sapphire_discord_js_utilities.PaginatedMessage#run)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:653](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L653)

___

### setActions

▸ **setActions**(`actions`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Clears all current actions and sets them. The order given is the order they will be used.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `actions` | [`PaginatedMessageAction`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction)[] | The actions to set. |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[setActions](sapphire_discord_js_utilities.PaginatedMessage#setactions)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:248](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L248)

___

### setIdle

▸ **setIdle**(`idle`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Sets the amount of time to idle before the paginator is closed.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `idle` | `number` | The number to set the idle to. |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[setIdle](sapphire_discord_js_utilities.PaginatedMessage#setidle)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:239](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L239)

___

### setIndex

▸ **setIndex**(`index`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Sets the handler's current page/message index.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `index` | `number` | The number to set the index to. |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[setIndex](sapphire_discord_js_utilities.PaginatedMessage#setindex)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:230](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L230)

___

### setItems

▸ **setItems**(`items`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Set the items to paginate.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `items` | `T`[] | The pages to set |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:37](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L37)

___

### setItemsPerPage

▸ **setItemsPerPage**(`itemsPerPage`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Sets the amount of items that should be shown per page.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `itemsPerPage` | `number` | The number of items |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:55](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L55)

___

### setPages

▸ **setPages**(`pages`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Clears all current pages and messages and sets them. The order given is the order they will be used.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pages` | [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage)[] | The pages to set. |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[setPages](sapphire_discord_js_utilities.PaginatedMessage#setpages)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:283](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L283)

___

### setSelectMenuOptions

▸ **setSelectMenuOptions**(`newOptions`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Sets the [PaginatedMessage.selectMenuOptions](sapphire_discord_js_utilities.PaginatedMessage#selectmenuoptions) for this instance of [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).
This will only apply to this one instance and no others.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `newOptions` | [`PaginatedMessageSelectMenuOptionsFunction`](../modules/sapphire_discord_js_utilities#paginatedmessageselectmenuoptionsfunction) | The new options generator to set |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

The current instance of [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[setSelectMenuOptions](sapphire_discord_js_utilities.PaginatedMessage#setselectmenuoptions)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:210](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L210)

___

### setTemplate

▸ **setTemplate**(`template`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Sets the template to be used to display the embed fields as pages. This template can either be set from a template {@link MessageEmbed} instance or an object with embed options.

**`example`**
```typescript
import { PaginatedFieldMessageEmbed } from '@sapphire/discord.js-utilities';
import { MessageEmbed } from 'discord.js';

new PaginatedFieldMessageEmbed().setTemplate(new MessageEmbed().setTitle('Test pager embed')).make().run(message.author, message.channel);
```

**`example`**
```typescript
import { PaginatedFieldMessageEmbed } from '@sapphire/discord.js-utilities';
import { MessageEmbed } from 'discord.js';

new PaginatedFieldMessageEmbed().setTemplate({ title: 'Test pager embed' }).make().run(message.author, message.channel);
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `template` | [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` | MessageEmbed |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:81](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L81)

___

### setTitleField

▸ **setTitleField**(`title`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Set the title of the embed field that will be used to paginate the items.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `title` | `string` | The field title |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts:46](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedFieldMessageEmbed.ts#L46)

___

### setUpCollector

▸ `Protected` **setUpCollector**(`channel`, `targetUser`): `void`

Sets up the message's collector.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`DMChannel`](https://discord.js.org/#/docs/main/stable/class/DMChannel) \| `PartialDMChannel` \| [`NewsChannel`](https://discord.js.org/#/docs/main/stable/class/NewsChannel) \| [`TextChannel`](https://discord.js.org/#/docs/main/stable/class/TextChannel) \| [`ThreadChannel`](https://discord.js.org/#/docs/main/stable/class/ThreadChannel) | The channel the handler is running at. |
| `targetUser` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) | The user the handler is for. |

#### Returns

`void`

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[setUpCollector](sapphire_discord_js_utilities.PaginatedMessage#setupcollector)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:775](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L775)

___

### setUpMessage

▸ `Protected` **setUpMessage**(`channel`, `targetUser`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Sets up the message.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `channel` | [`DMChannel`](https://discord.js.org/#/docs/main/stable/class/DMChannel) \| `PartialDMChannel` \| [`NewsChannel`](https://discord.js.org/#/docs/main/stable/class/NewsChannel) \| [`TextChannel`](https://discord.js.org/#/docs/main/stable/class/TextChannel) \| [`ThreadChannel`](https://discord.js.org/#/docs/main/stable/class/ThreadChannel) | The channel the handler is running at. |
| `targetUser` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[setUpMessage](sapphire_discord_js_utilities.PaginatedMessage#setupmessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:728](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L728)

___

### setWrongUserInteractionReply

▸ **setWrongUserInteractionReply**(`wrongUserInteractionReply`): [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

Sets the [PaginatedMessage.wrongUserInteractionReply](sapphire_discord_js_utilities.PaginatedMessage#wronguserinteractionreply) for this instance of [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).
This will only apply to this one instance and no others.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `wrongUserInteractionReply` | [`PaginatedMessageWrongUserInteractionReplyFunction`](../modules/sapphire_discord_js_utilities#paginatedmessagewronguserinteractionreplyfunction) | The new `wrongUserInteractionReply` to set |

#### Returns

[`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)<`T`\>

The current instance of [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

#### Inherited from

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).[setWrongUserInteractionReply](sapphire_discord_js_utilities.PaginatedMessage#setwronguserinteractionreply)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:221](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L221)

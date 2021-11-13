---
id: "sapphire_discord_js_utilities.PaginatedMessage"
title: "Class: PaginatedMessage"
sidebar_label: "PaginatedMessage"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).PaginatedMessage

This is a [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage), a utility to paginate messages (usually embeds).
You must either use this class directly or extend it.

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) uses [MessageComponent](https://discord.js.org/#/docs/main/stable/typedef/MessageComponent) buttons that perform the specified action when clicked.
You can either use your own actions or the [PaginatedMessage.defaultActions](sapphire_discord_js_utilities.PaginatedMessage#defaultactions).
[PaginatedMessage.defaultActions](sapphire_discord_js_utilities.PaginatedMessage#defaultactions) is also static so you can modify these directly.

[PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) also uses pages via [Messages](https://discord.js.org/#/docs/main/stable/class/Message).

**`example`**
```typescript
const myPaginatedMessage = new PaginatedMessage();
// Once you have an instance of PaginatedMessage you can call various methods on it to add pages to it.
// For more details see each method's documentation.

myPaginatedMessage.addPageEmbed((embed) => {
		embed
			.setColor('#FF0000')
			.setDescription('example description');

		return embed;
});

myPaginatedMessage.addPageBuilder((builder) => {
		const embed = new MessageEmbed()
			.setColor('#FF0000')
			.setDescription('example description');

		return builder
			.setContent('example content')
			.setEmbed(embed);
});

myPaginatedMessage.addPageContent('Example');

myPaginatedMessage.run(message)
```

**`remark`** You can also provide a MessageEmbed template. This will be applied to every page.
If a page itself has an embed then the two will be merged, with the content of
the page's embed taking priority over the template.

Furthermore, if the template has a footer then it will be applied _after_ the page index part of the footer
with a space preceding the template. For example, when setting `- Powered by Sapphire Framework`
the resulting footer will be `1/2 - Powered by Sapphire Framework`

**`example`**
```typescript
const myPaginatedMessage = new PaginatedMessage({
	template: new MessageEmbed().setColor('#FF0000').setFooter('- Powered by Sapphire framework')
});
```

**`remark`** To utilize actions you can implement IPaginatedMessageAction into a class.

**`example`**
```typescript
class ForwardAction implements IPaginatedMessageAction {
  public id = '▶️';

  public run({ handler }) {
    if (handler.index !== handler.pages.length - 1) ++handler.index;
  }
}

// You can also give the object directly.

const StopAction: IPaginatedMessageAction = {
  customId: 'CustomStopAction',
  run: ({ collector }) => {
    collector.stop();
  }
}
```

## Hierarchy

- **`PaginatedMessage`**

  ↳ [`LazyPaginatedMessage`](sapphire_discord_js_utilities.LazyPaginatedMessage)

  ↳ [`PaginatedFieldMessageEmbed`](sapphire_discord_js_utilities.PaginatedFieldMessageEmbed)

## Constructors

### constructor

• **new PaginatedMessage**(`__namedParameters?`)

Constructor for the [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) class

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `__namedParameters` | [`PaginatedMessageOptions`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageOptions) | The [PaginatedMessageOptions](../interfaces/sapphire_discord_js_utilities.PaginatedMessageOptions) for this instance of the [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) class |

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:178](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L178)

## Properties

### actions

• **actions**: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<`string`, [`PaginatedMessageAction`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction)\>

The actions which are to be used.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:131](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L131)

___

### collector

• **collector**: ``null`` \| [`InteractionCollector`](https://discord.js.org/#/docs/main/stable/class/InteractionCollector)<[`MessageComponentInteraction`](https://discord.js.org/#/docs/main/stable/class/MessageComponentInteraction)<`CacheType`\>\> = `null`

The collector used for handling button clicks.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:121](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L121)

___

### constructor

• **constructor**: typeof [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1153](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1153)

___

### embedFooterSeparator

• **embedFooterSeparator**: `string` = `PaginatedMessage.embedFooterSeparator`

Custom separator to show after the page index in the embed footer.
PaginatedMessage will automatically add a space (` `) after the given text. You do not have to add it yourself.

**`default`** ```PaginatedMessage.pageIndexPrefix``` (static property)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:161](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L161)

___

### hasEmittedWarning

• `Protected` **hasEmittedWarning**: `boolean` = `false`

Tracks whether a warning was already emitted for this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:172](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L172)

___

### idle

• **idle**: `number`

The amount of milliseconds to idle before the paginator is closed. Defaults to 20 minutes.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:141](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L141)

___

### index

• **index**: `number` = `0`

The handler's current page/message index.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:136](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L136)

___

### messages

• **messages**: (``null`` \| [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage))[] = `[]`

The pages which were converted from [PaginatedMessage.pages](sapphire_discord_js_utilities.PaginatedMessage#pages)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:126](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L126)

___

### pageIndexPrefix

• **pageIndexPrefix**: `string` = `PaginatedMessage.pageIndexPrefix`

Custom text to show in front of the page index in the embed footer.
PaginatedMessage will automatically add a space (` `) after the given text. You do not have to add it yourself.

**`default`** ```PaginatedMessage.pageIndexPrefix``` (static property)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:154](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L154)

___

### pages

• **pages**: [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage)[]

The pages to be converted to [PaginatedMessage.messages](sapphire_discord_js_utilities.PaginatedMessage#messages)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:111](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L111)

___

### paginatedMessageData

• `Protected` **paginatedMessageData**: ``null`` \| `Omit`<[`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion), ``"components"``\> = `null`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:163](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L163)

___

### response

• **response**: ``null`` \| [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> = `null`

The response message used to edit on page changes.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:116](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L116)

___

### selectMenuOptions

• `Protected` **selectMenuOptions**: [`PaginatedMessageSelectMenuOptionsFunction`](../modules/sapphire_discord_js_utilities#paginatedmessageselectmenuoptionsfunction) = `PaginatedMessage.selectMenuOptions`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:165](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L165)

___

### template

• **template**: [`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion)

The template for this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).
You can use templates to set defaults that will apply to each and every page in the [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:147](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L147)

___

### wrongUserInteractionReply

• `Protected` **wrongUserInteractionReply**: [`PaginatedMessageWrongUserInteractionReplyFunction`](../modules/sapphire_discord_js_utilities#paginatedmessagewronguserinteractionreplyfunction) = `PaginatedMessage.wrongUserInteractionReply`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:167](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L167)

___

### defaultActions

▪ `Static` **defaultActions**: [`PaginatedMessageAction`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction)[]

The default actions of this handler.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:952](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L952)

___

### deletionStopReasons

▪ `Static` **deletionStopReasons**: `string`[]

The reasons sent by [InteractionCollector#end](https://discord.js.org/#/docs/main/stable/class/InteractionCollector?scrollTo=e-end)
event when the message (or its owner) has been deleted.

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

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1044](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1044)

___

### handlers

▪ `Static` `Readonly` **handlers**: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<`string`, [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)\>

The current {@link InteractionCollector} handlers that are active.
The key is the ID of of the author who sent the message that triggered this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

This is to ensure that any given author can only trigger 1 [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).
This is important for performance reasons, and users should not have more than 1 [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) open at once.

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1062](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1062)

___

### messages

▪ `Static` `Readonly` **messages**: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<`string`, [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)\>

The messages that are currently being handled by a [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)
The key is the ID of the message that triggered this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

This is to ensure that only 1 [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) can run on a specified message at once.
This is important when having an editable commands solution.

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

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1133](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1133)

## Methods

### addAction

▸ **addAction**(`action`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Adds an action to the existing ones. This will be added as the last action.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `action` | [`PaginatedMessageAction`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction) | The action to add. |

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:266](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L266)

___

### addActions

▸ **addActions**(`actions`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Adds actions to the existing ones. The order given is the order they will be used.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `actions` | [`PaginatedMessageAction`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction)[] | The actions to add. |

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:257](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L257)

___

### addAsyncPageBuilder

▸ **addAsyncPageBuilder**(`builder`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

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

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:385](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L385)

___

### addAsyncPageEmbed

▸ **addAsyncPageEmbed**(`embed`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

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

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:455](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L455)

___

### addAsyncPageEmbeds

▸ **addAsyncPageEmbeds**(`embeds`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

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

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:597](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L597)

___

### addPage

▸ **addPage**(`page`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

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

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:300](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L300)

___

### addPageBuilder

▸ **addPageBuilder**(`builder`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

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

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:359](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L359)

___

### addPageContent

▸ **addPageContent**(`content`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

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

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:400](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L400)

___

### addPageEmbed

▸ **addPageEmbed**(`embed`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

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

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:432](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L432)

___

### addPageEmbeds

▸ **addPageEmbeds**(`embeds`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

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

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:506](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L506)

___

### addPages

▸ **addPages**(`pages`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Add pages to the existing ones. The order given is the order they will be used.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pages` | [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage)[] | The pages to add. |

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

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

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:868](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L868)

___

### applyTemplate

▸ `Private` **applyTemplate**(`template`, `options`): [`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion)

#### Parameters

| Name | Type |
| :------ | :------ |
| `template` | [`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion) |
| `options` | [`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion) |

#### Returns

[`PaginatedMessageMessageOptionsUnion`](../modules/sapphire_discord_js_utilities#paginatedmessagemessageoptionsunion)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:885](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L885)

___

### applyTemplateEmbed

▸ `Private` **applyTemplateEmbed**(`templateEmbed`, `pageEmbeds`): `undefined` \| ([`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` \| `APIEmbed`)[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `templateEmbed` | `undefined` \| ([`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` \| `APIEmbed`)[] |
| `pageEmbeds` | `undefined` \| ([`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` \| `APIEmbed`)[] |

#### Returns

`undefined` \| ([`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` \| `APIEmbed`)[]

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:894](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L894)

___

### clone

▸ **clone**(): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Clones the current handler into a new instance.

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:715](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L715)

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

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:275](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L275)

___

### mergeArrays

▸ `Private` **mergeArrays**<`T`\>(`template?`, `array?`): `undefined` \| `T`[]

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `template?` | `T`[] |
| `array?` | `T`[] |

#### Returns

`undefined` \| `T`[]

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:937](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L937)

___

### mergeEmbeds

▸ `Private` **mergeEmbeds**(`templateEmbed`, `pageEmbeds`): ([`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` \| `APIEmbed`)[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `templateEmbed` | [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` \| `APIEmbed` |
| `pageEmbeds` | ([`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` \| `APIEmbed`)[] |

#### Returns

([`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) \| `MessageEmbedOptions` \| `APIEmbed`)[]

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:909](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L909)

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

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:698](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L698)

___

### resolvePagesOnRun

▸ **resolvePagesOnRun**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Executed whenever [PaginatedMessage.run](sapphire_discord_js_utilities.PaginatedMessage#run) is called.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:690](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L690)

___

### run

▸ **run**(`message`, `target?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)\>

Executes the [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage) and sends the pages corresponding with [PaginatedMessage.index](sapphire_discord_js_utilities.PaginatedMessage#index).
The handler will start collecting message button interactions.

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> | `undefined` | The message that triggered this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage). Generally this will be the command message, but it can also be another message from your client, i.e. to indicate a loading state. |
| `target` | [`User`](https://discord.js.org/#/docs/main/stable/class/User) | `message.author` | The user who will be able to interact with the message buttons of this [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage). Defaults to `message.author`. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:653](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L653)

___

### setActions

▸ **setActions**(`actions`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Clears all current actions and sets them. The order given is the order they will be used.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `actions` | [`PaginatedMessageAction`](../interfaces/sapphire_discord_js_utilities.PaginatedMessageAction)[] | The actions to set. |

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:248](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L248)

___

### setIdle

▸ **setIdle**(`idle`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Sets the amount of time to idle before the paginator is closed.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `idle` | `number` | The number to set the idle to. |

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:239](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L239)

___

### setIndex

▸ **setIndex**(`index`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Sets the handler's current page/message index.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `index` | `number` | The number to set the index to. |

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:230](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L230)

___

### setPages

▸ **setPages**(`pages`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Clears all current pages and messages and sets them. The order given is the order they will be used.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pages` | [`PaginatedMessagePage`](../modules/sapphire_discord_js_utilities#paginatedmessagepage)[] | The pages to set. |

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:283](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L283)

___

### setSelectMenuOptions

▸ **setSelectMenuOptions**(`newOptions`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Sets the [PaginatedMessage.selectMenuOptions](sapphire_discord_js_utilities.PaginatedMessage#selectmenuoptions) for this instance of [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).
This will only apply to this one instance and no others.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `newOptions` | [`PaginatedMessageSelectMenuOptionsFunction`](../modules/sapphire_discord_js_utilities#paginatedmessageselectmenuoptionsfunction) | The new options generator to set |

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

The current instance of [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:210](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L210)

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

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:728](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L728)

___

### setWrongUserInteractionReply

▸ **setWrongUserInteractionReply**(`wrongUserInteractionReply`): [`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

Sets the [PaginatedMessage.wrongUserInteractionReply](sapphire_discord_js_utilities.PaginatedMessage#wronguserinteractionreply) for this instance of [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage).
This will only apply to this one instance and no others.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `wrongUserInteractionReply` | [`PaginatedMessageWrongUserInteractionReplyFunction`](../modules/sapphire_discord_js_utilities#paginatedmessagewronguserinteractionreplyfunction) | The new `wrongUserInteractionReply` to set |

#### Returns

[`PaginatedMessage`](sapphire_discord_js_utilities.PaginatedMessage)

The current instance of [PaginatedMessage](sapphire_discord_js_utilities.PaginatedMessage)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:221](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L221)

___

### resolveTemplate

▸ `Static` `Private` **resolveTemplate**(`template?`): `MessageOptions`

#### Parameters

| Name | Type |
| :------ | :------ |
| `template?` | `MessageOptions` \| [`MessageEmbed`](https://discord.js.org/#/docs/main/stable/class/MessageEmbed) |

#### Returns

`MessageOptions`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts:1139](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/PaginatedMessages/PaginatedMessage.ts#L1139)

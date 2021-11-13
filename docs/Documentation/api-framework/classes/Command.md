---
id: "Command"
title: "Class: Command<T, O>"
sidebar_label: "Command"
sidebar_position: 0
custom_edit_url: null
---

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | [`Args`](Args) |
| `O` | extends [`CommandOptions`](../interfaces/CommandOptions)[`CommandOptions`](../interfaces/CommandOptions) |

## Hierarchy

- [`AliasPiece`](AliasPiece)<`O`\>

  ↳ **`Command`**

## Constructors

### constructor

• `Protected` **new Command**<`T`, `O`\>(`context`, `options?`)

**`since`** 1.0.0

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | [`Args`](Args) |
| `O` | extends [`CommandOptions`](../interfaces/CommandOptions)[`CommandOptions`](../interfaces/CommandOptions) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `context` | [`PieceContext`](../interfaces/PieceContext) | The context. |
| `options` | [`CommandOptions`](../interfaces/CommandOptions) | Optional Command settings. |

#### Overrides

[AliasPiece](AliasPiece).[constructor](AliasPiece#constructor)

#### Defined in

[projects/framework/src/lib/structures/Command.ts:64](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L64)

## Properties

### aliases

• **aliases**: readonly `string`[]

The aliases for the piece.

#### Inherited from

[AliasPiece](AliasPiece).[aliases](AliasPiece#aliases)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:670

___

### description

• **description**: `string`

A basic summary about the command

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/structures/Command.ts:15](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L15)

___

### detailedDescription

• **detailedDescription**: `string`

Longer version of command's summary and how to use it

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/structures/Command.ts:27](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L27)

___

### enabled

• **enabled**: `boolean`

Whether or not the piece is enabled.

#### Inherited from

[AliasPiece](AliasPiece).[enabled](AliasPiece#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:432

___

### fullCategory

• `Readonly` **fullCategory**: readonly `string`[]

The full category for the command. Either an array of strings that denote every (sub)folder the command is in,
or `null` if it could not be resolved automatically.

If this is `null` for how you setup your code then you can overwrite how the `fullCategory` is resolved by
extending this class and overwriting the assignment in the constructor.

**`since`** 2.0.0

#### Defined in

[projects/framework/src/lib/structures/Command.ts:37](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L37)

___

### lexer

• `Private` **lexer**: `Lexer`

The lexer to be used for command parsing

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/structures/Command.ts:57](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L57)

___

### location

• `Readonly` **location**: `PieceLocation`

The location metadata for the piece's file.

#### Inherited from

[AliasPiece](AliasPiece).[location](AliasPiece#location)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:424

___

### name

• `Readonly` **name**: `string`

The name of the piece.

#### Inherited from

[AliasPiece](AliasPiece).[name](AliasPiece#name)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:428

___

### options

• `Readonly` **options**: `O`

The raw options passed to this [Piece](Piece)

#### Inherited from

[AliasPiece](AliasPiece).[options](AliasPiece#options)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:436

___

### preconditions

• **preconditions**: [`PreconditionContainerArray`](PreconditionContainerArray)

The preconditions to be run.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/structures/Command.ts:21](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L21)

___

### store

• `Readonly` **store**: [`Store`](Store)<[`Piece`](Piece)<[`PieceOptions`](../interfaces/PieceOptions)\>\>

The store that contains the piece.

#### Inherited from

[AliasPiece](AliasPiece).[store](AliasPiece#store)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:420

___

### strategy

• **strategy**: `UnorderedStrategy`

The strategy to use for the lexer.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/structures/Command.ts:43](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L43)

___

### typing

• **typing**: `boolean`

If {@link SapphireClient.typing} is true, it can be overridden for a specific command using this property, set via its options.
Otherwise, this property will be ignored.

**`default`** true

#### Defined in

[projects/framework/src/lib/structures/Command.ts:50](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L50)

## Accessors

### category

• `get` **category**(): ``null`` \| `string`

The main category for the command, if any.

This getter retrieves the first value of [Command.fullCategory](Command#fullcategory), if it has at least one item, otherwise it
returns `null`.

**`note`** You can set [CommandOptions.fullCategory](../interfaces/CommandOptions#fullcategory) to override the built-in category resolution.

#### Returns

``null`` \| `string`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:122](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L122)

___

### container

• `get` **container**(): `Container`

A reference to the {@link Container} object for ease of use.

**`see`** container

#### Returns

`Container`

#### Inherited from

AliasPiece.container

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:442

___

### parentCategory

• `get` **parentCategory**(): ``null`` \| `string`

The parent category for the command.

This getter retrieves the last value of [Command.fullCategory](Command#fullcategory), if it has at least one item, otherwise it
returns `null`.

**`note`** You can set [CommandOptions.fullCategory](../interfaces/CommandOptions#fullcategory) to override the built-in category resolution.

#### Returns

``null`` \| `string`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:146](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L146)

___

### subCategory

• `get` **subCategory**(): ``null`` \| `string`

The sub-category for the command, if any.

This getter retrieves the second value of [Command.fullCategory](Command#fullcategory), if it has at least two items, otherwise
it returns `null`.

**`note`** You can set [CommandOptions.fullCategory](../interfaces/CommandOptions#fullcategory) to override the built-in category resolution.

#### Returns

``null`` \| `string`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:134](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L134)

## Methods

### messageRun

▸ `Abstract` **messageRun**(`message`, `args`, `context`): `unknown`

Executes the command's logic for a message.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> | The message that triggered the command. |
| `args` | `T` | The value returned by [Command.preParse](Command#preparse), by default an instance of [Args](Args). |
| `context` | [`CommandContext`](../interfaces/CommandContext) | - |

#### Returns

`unknown`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:155](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L155)

___

### onLoad

▸ **onLoad**(): `unknown`

Per-piece listener that is called when the piece is loaded into the store.
Useful to set-up asynchronous initialization tasks.

#### Returns

`unknown`

#### Inherited from

[AliasPiece](AliasPiece).[onLoad](AliasPiece#onload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:447

___

### onUnload

▸ **onUnload**(): `unknown`

Per-piece listener that is called when the piece is unloaded from the store.
Useful to set-up clean-up tasks.

#### Returns

`unknown`

#### Inherited from

[AliasPiece](AliasPiece).[onUnload](AliasPiece#onunload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:452

___

### parseConstructorPreConditions

▸ `Protected` **parseConstructorPreConditions**(`options`): `void`

Parses the command's options and processes them, calling {@link Command#parseConstructorPreConditionsRunIn},
{@link Command#parseConstructorPreConditionsNsfw},
{@link Command#parseConstructorPreConditionsRequiredClientPermissions}, and
{@link Command#parseConstructorPreConditionsCooldown}.

**`since`** 2.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`CommandOptions`](../interfaces/CommandOptions) | The command options given from the constructor. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:177](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L177)

___

### parseConstructorPreConditionsCooldown

▸ `Protected` **parseConstructorPreConditionsCooldown**(`options`): `void`

Appends the `Cooldown` precondition when [CommandOptions.cooldownLimit](../interfaces/CommandOptions#cooldownlimit) and
[CommandOptions.cooldownDelay](../interfaces/CommandOptions#cooldowndelay) are both non-zero.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`CommandOptions`](../interfaces/CommandOptions) | The command options given from the constructor. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:233](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L233)

___

### parseConstructorPreConditionsNsfw

▸ `Protected` **parseConstructorPreConditionsNsfw**(`options`): `void`

Appends the `NSFW` precondition if [CommandOptions.nsfw](../interfaces/CommandOptions#nsfw) is set to true.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`CommandOptions`](../interfaces/CommandOptions) | The command options given from the constructor. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:189](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L189)

___

### parseConstructorPreConditionsRequiredClientPermissions

▸ `Protected` **parseConstructorPreConditionsRequiredClientPermissions**(`options`): `void`

Appends the `ClientPermissions` precondition when [CommandOptions.requiredClientPermissions](../interfaces/CommandOptions#requiredclientpermissions) resolves to a
non-zero bitfield.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`CommandOptions`](../interfaces/CommandOptions) | The command options given from the constructor. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:209](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L209)

___

### parseConstructorPreConditionsRequiredUserPermissions

▸ `Protected` **parseConstructorPreConditionsRequiredUserPermissions**(`options`): `void`

Appends the `UserPermissions` precondition when [CommandOptions.requiredUserPermissions](../interfaces/CommandOptions#requireduserpermissions) resolves to a
non-zero bitfield.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`CommandOptions`](../interfaces/CommandOptions) | The command options given from the constructor. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:221](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L221)

___

### parseConstructorPreConditionsRunIn

▸ `Protected` **parseConstructorPreConditionsRunIn**(`options`): `void`

Appends the `DMOnly`, `GuildOnly`, `NewsOnly`, and `TextOnly` preconditions based on the values passed in
[CommandOptions.runIn](../interfaces/CommandOptions#runin), optimizing in specific cases (`NewsOnly` + `TextOnly` = `GuildOnly`; `DMOnly` +
`GuildOnly` = `null`), defaulting to `null`, which doesn't add a precondition.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`CommandOptions`](../interfaces/CommandOptions) | The command options given from the constructor. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:199](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L199)

___

### preParse

▸ **preParse**(`message`, `parameters`, `context`): [`Awaitable`](../#awaitable)<`T`\>

The pre-parse method. This method can be overridden by plugins to define their own argument parser.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> | The message that triggered the command. |
| `parameters` | `string` | The raw parameters as a single string. |
| `context` | [`CommandContext`](../interfaces/CommandContext) | The command-context used in this execution. |

#### Returns

[`Awaitable`](../#awaitable)<`T`\>

#### Defined in

[projects/framework/src/lib/structures/Command.ts:108](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L108)

___

### reload

▸ **reload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Reloads the piece by loading the same path in the store.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[AliasPiece](AliasPiece).[reload](AliasPiece#reload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:460

___

### resolveConstructorPreConditionsRunType

▸ `Private` **resolveConstructorPreConditionsRunType**(`runIn`): ``null`` \| [`PreconditionContainerArray`](PreconditionContainerArray) \| [`CommandPreConditions`](../enums/CommandPreConditions)

#### Parameters

| Name | Type |
| :------ | :------ |
| `runIn` | `undefined` \| ``null`` \| [`CommandOptionsRunType`](../#commandoptionsruntype) \| [`CommandOptionsRunTypeEnum`](../enums/CommandOptionsRunTypeEnum) \| readonly ([`CommandOptionsRunType`](../#commandoptionsruntype) \| [`CommandOptionsRunTypeEnum`](../enums/CommandOptionsRunTypeEnum))[] |

#### Returns

``null`` \| [`PreconditionContainerArray`](PreconditionContainerArray) \| [`CommandPreConditions`](../enums/CommandPreConditions)

#### Defined in

[projects/framework/src/lib/structures/Command.ts:253](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L253)

___

### run

▸ `Optional` **run**(`message`, `args`, `context`): `unknown`

Executes the command's logic.

**`deprecated`** Use `messageRun` instead.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> | The message that triggered the command. |
| `args` | `T` | The value returned by [Command.preParse](Command#preparse), by default an instance of [Args](Args). |
| `context` | [`CommandContext`](../interfaces/CommandContext) | - |

#### Returns

`unknown`

#### Defined in

[projects/framework/src/lib/structures/Command.ts:337](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L337)

___

### toJSON

▸ **toJSON**(): [`CommandJSON`](../interfaces/CommandJSON)

Defines the JSON.stringify behavior of the command.

#### Returns

[`CommandJSON`](../interfaces/CommandJSON)

#### Overrides

[AliasPiece](AliasPiece).[toJSON](AliasPiece#tojson)

#### Defined in

[projects/framework/src/lib/structures/Command.ts:160](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L160)

___

### unload

▸ **unload**(): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

Unloads and disables the piece.

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`void`\>

#### Inherited from

[AliasPiece](AliasPiece).[unload](AliasPiece#unload)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:456

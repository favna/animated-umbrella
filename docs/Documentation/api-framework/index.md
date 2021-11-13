---
id: "index"
title: "@sapphire/framework"
slug: "/Documentation/api-framework/"
sidebar_label: "Exports"
sidebar_position: 0.5
custom_edit_url: null
---

## Namespaces

- [ArgumentError](namespaces/ArgumentError)
- [CorePreconditions](namespaces/CorePreconditions)
- [Precondition](namespaces/Precondition)
- [PreconditionError](namespaces/PreconditionError)
- [Resolvers](namespaces/Resolvers)
- [UserError](namespaces/UserError)

## Enumerations

- [BucketScope](enums/BucketScope)
- [CommandOptionsRunTypeEnum](enums/CommandOptionsRunTypeEnum)
- [CommandPreConditions](enums/CommandPreConditions)
- [CooldownLevel](enums/CooldownLevel)
- [Identifiers](enums/Identifiers)
- [LogLevel](enums/LogLevel)
- [PluginHook](enums/PluginHook)
- [PreconditionRunCondition](enums/PreconditionRunCondition)
- [PreconditionRunMode](enums/PreconditionRunMode)

## Classes

- [AliasPiece](classes/AliasPiece)
- [AliasStore](classes/AliasStore)
- [Args](classes/Args)
- [Argument](classes/Argument)
- [ArgumentError](classes/ArgumentError)
- [ArgumentStore](classes/ArgumentStore)
- [ClientPermissionsPrecondition](classes/ClientPermissionsPrecondition)
- [Command](classes/Command)
- [CommandStore](classes/CommandStore)
- [ExtendedArgument](classes/ExtendedArgument)
- [Listener](classes/Listener)
- [ListenerStore](classes/ListenerStore)
- [LoaderError](classes/LoaderError)
- [Logger](classes/Logger)
- [MissingExportsError](classes/MissingExportsError)
- [Piece](classes/Piece)
- [Plugin](classes/Plugin)
- [PluginManager](classes/PluginManager)
- [Precondition](classes/Precondition)
- [PreconditionContainerArray](classes/PreconditionContainerArray)
- [PreconditionContainerSingle](classes/PreconditionContainerSingle)
- [PreconditionError](classes/PreconditionError)
- [PreconditionStore](classes/PreconditionStore)
- [SapphireClient](classes/SapphireClient)
- [Store](classes/Store)
- [StoreRegistry](classes/StoreRegistry)
- [UserError](classes/UserError)
- [UserPermissionsPrecondition](classes/UserPermissionsPrecondition)

## Interfaces

- [AliasPieceOptions](interfaces/AliasPieceOptions)
- [ArgOptions](interfaces/ArgOptions)
- [ArgType](interfaces/ArgType)
- [ArgsNextCallback](interfaces/ArgsNextCallback)
- [ArgumentContext](interfaces/ArgumentContext)
- [ArgumentOptions](interfaces/ArgumentOptions)
- [ClientLoggerOptions](interfaces/ClientLoggerOptions)
- [CommandAcceptedPayload](interfaces/CommandAcceptedPayload)
- [CommandContext](interfaces/CommandContext)
- [CommandDeniedPayload](interfaces/CommandDeniedPayload)
- [CommandErrorPayload](interfaces/CommandErrorPayload)
- [CommandFinishPayload](interfaces/CommandFinishPayload)
- [CommandJSON](interfaces/CommandJSON)
- [CommandOptions](interfaces/CommandOptions)
- [CommandRunPayload](interfaces/CommandRunPayload)
- [CommandSuccessPayload](interfaces/CommandSuccessPayload)
- [CommandTypingErrorPayload](interfaces/CommandTypingErrorPayload)
- [CooldownContext](interfaces/CooldownContext)
- [CooldownOptions](interfaces/CooldownOptions)
- [ExtendedArgumentContext](interfaces/ExtendedArgumentContext)
- [ExtendedArgumentOptions](interfaces/ExtendedArgumentOptions)
- [IArgument](interfaces/IArgument)
- [ICommandPayload](interfaces/ICommandPayload)
- [ILogger](interfaces/ILogger)
- [IPieceError](interfaces/IPieceError)
- [IPreconditionCondition](interfaces/IPreconditionCondition)
- [IPreconditionContainer](interfaces/IPreconditionContainer)
- [ListenerErrorPayload](interfaces/ListenerErrorPayload)
- [ListenerJSON](interfaces/ListenerJSON)
- [ListenerOptions](interfaces/ListenerOptions)
- [PieceContext](interfaces/PieceContext)
- [PieceOptions](interfaces/PieceOptions)
- [PreCommandRunPayload](interfaces/PreCommandRunPayload)
- [PreconditionArrayResolvableDetails](interfaces/PreconditionArrayResolvableDetails)
- [PreconditionContext](interfaces/PreconditionContext)
- [PreconditionOptions](interfaces/PreconditionOptions)
- [PreconditionSingleResolvableDetails](interfaces/PreconditionSingleResolvableDetails)
- [Preconditions](interfaces/Preconditions)
- [RepeatArgOptions](interfaces/RepeatArgOptions)
- [SapphireClientOptions](interfaces/SapphireClientOptions)
- [SapphirePluginAsyncHook](interfaces/SapphirePluginAsyncHook)
- [SapphirePluginHook](interfaces/SapphirePluginHook)
- [SapphirePluginHookEntry](interfaces/SapphirePluginHookEntry)
- [SapphirePrefixHook](interfaces/SapphirePrefixHook)
- [SimplePreconditionSingleResolvableDetails](interfaces/SimplePreconditionSingleResolvableDetails)
- [StoreOptions](interfaces/StoreOptions)
- [StoreRegistryEntries](interfaces/StoreRegistryEntries)
- [UnknownCommandNamePayload](interfaces/UnknownCommandNamePayload)
- [UnknownCommandPayload](interfaces/UnknownCommandPayload)

## References

### ClientPermissionsCorePrecondition

Renames and re-exports [ClientPermissions](classes/CorePreconditions.ClientPermissions)

## Type aliases

### ArgumentResult

Ƭ **ArgumentResult**<`T`\>: [`Awaitable`](#awaitable)<[`Result`](#result)<`T`, [`UserError`](classes/UserError)\>\>

Defines a synchronous result of an [Argument](classes/Argument), check [AsyncArgumentResult](#asyncargumentresult) for the asynchronous version.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:13](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L13)

___

### AsyncArgumentResult

Ƭ **AsyncArgumentResult**<`T`\>: [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](#result)<`T`, [`UserError`](classes/UserError)\>\>

Defines an asynchronous result of an [Argument](classes/Argument), check [ArgumentResult](#argumentresult) for the synchronous version.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[projects/framework/src/lib/structures/Argument.ts:18](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Argument.ts#L18)

___

### AsyncPluginHooks

Ƭ **AsyncPluginHooks**: [`PreLogin`](enums/PluginHook#prelogin) \| [`PostLogin`](enums/PluginHook#postlogin)

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:8](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L8)

___

### AsyncPreconditionContainerReturn

Ƭ **AsyncPreconditionContainerReturn**: [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`PreconditionContainerResult`](#preconditioncontainerresult)\>

Async-only version of [PreconditionContainerReturn](#preconditioncontainerreturn), to be used when the run method is async.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/IPreconditionContainer.ts:24](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/IPreconditionContainer.ts#L24)

___

### AsyncPreconditionResult

Ƭ **AsyncPreconditionResult**: [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](#result)<`unknown`, [`UserError`](classes/UserError)\>\>

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:11](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L11)

___

### Awaitable

Ƭ **Awaitable**<`T`\>: `PromiseLike`<`T`\> \| `T`

ReturnType for a function that can return either a value or a `Promise` with that value

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

node_modules/@sapphire/utilities/dist/lib/utilityTypes.d.ts:44

___

### CommandOptionsRunType

Ƭ **CommandOptionsRunType**: ``"DM"`` \| ``"GUILD_TEXT"`` \| ``"GUILD_NEWS"`` \| ``"GUILD_NEWS_THREAD"`` \| ``"GUILD_PUBLIC_THREAD"`` \| ``"GUILD_PRIVATE_THREAD"`` \| ``"GUILD_ANY"``

The allowed values for [CommandOptions.runIn](interfaces/CommandOptions#runin).

**`remark`** It is discouraged to use this type, we recommend using [CommandOptionsRunTypeEnum](enums/CommandOptionsRunTypeEnum) instead.

**`since`** 2.0.0

#### Defined in

[projects/framework/src/lib/structures/Command.ts:345](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L345)

___

### Err

Ƭ **Err**<`E`\>: `Lexure.Err`<`E`\>

The computation failed.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `E` | Type of errors. |

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:21](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L21)

___

### LogMethods

Ƭ **LogMethods**: ``"trace"`` \| ``"debug"`` \| ``"info"`` \| ``"warn"`` \| ``"error"``

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:54](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L54)

___

### Maybe

Ƭ **Maybe**<`T`\>: [`Some`](#some)<`T`\> \| [`None`](#none)

A type used to express a value that may or may not exist.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | The value's type. |

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:7](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L7)

___

### None

Ƭ **None**: `option.None`

An empty value.

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:18](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L18)

___

### Ok

Ƭ **Ok**<`T`\>: `Lexure.Ok`<`T`\>

The computation is successful.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | Type of results. |

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:15](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L15)

___

### PreconditionArrayResolvable

Ƭ **PreconditionArrayResolvable**: readonly [`PreconditionEntryResolvable`](#preconditionentryresolvable)[] \| [`PreconditionArrayResolvableDetails`](interfaces/PreconditionArrayResolvableDetails)

Defines the data accepted by [PreconditionContainerArray](classes/PreconditionContainerArray)'s constructor.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:75](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L75)

___

### PreconditionContainerResult

Ƭ **PreconditionContainerResult**: [`Result`](#result)<`unknown`, [`UserError`](classes/UserError)\>

Defines the result's value for a PreconditionContainer.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/IPreconditionContainer.ts:12](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/IPreconditionContainer.ts#L12)

___

### PreconditionContainerReturn

Ƭ **PreconditionContainerReturn**: [`Awaitable`](#awaitable)<[`PreconditionContainerResult`](#preconditioncontainerresult)\>

Defines the return type of the generic [IPreconditionContainer.run](interfaces/IPreconditionContainer#run).

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/IPreconditionContainer.ts:18](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/IPreconditionContainer.ts#L18)

___

### PreconditionEntryResolvable

Ƭ **PreconditionEntryResolvable**: [`PreconditionSingleResolvable`](#preconditionsingleresolvable) \| [`PreconditionArrayResolvable`](#preconditionarrayresolvable)

Defines the data accepted for each entry of the array.

**`since`** 1.0.0

**`seealso`** [PreconditionArrayResolvable](#preconditionarrayresolvable)

**`seealso`** [PreconditionArrayResolvableDetails.entries](interfaces/PreconditionArrayResolvableDetails#entries)

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:83](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L83)

___

### PreconditionKeys

Ƭ **PreconditionKeys**: keyof [`Preconditions`](interfaces/Preconditions)

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:103](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L103)

___

### PreconditionResult

Ƭ **PreconditionResult**: [`Awaitable`](#awaitable)<[`Result`](#result)<`unknown`, [`UserError`](classes/UserError)\>\>

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:10](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L10)

___

### PreconditionSingleResolvable

Ƭ **PreconditionSingleResolvable**: [`SimplePreconditionKeys`](#simplepreconditionkeys) \| [`SimplePreconditionSingleResolvableDetails`](interfaces/SimplePreconditionSingleResolvableDetails) \| [`PreconditionSingleResolvableDetails`](interfaces/PreconditionSingleResolvableDetails)

Defines the data accepted by [PreconditionContainerSingle](classes/PreconditionContainerSingle)'s constructor.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerSingle.ts:43](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerSingle.ts#L43)

___

### Result

Ƭ **Result**<`T`, `E`\>: [`Ok`](#ok)<`T`\> \| [`Err`](#err)<`E`\>

A type used to express computations that can fail.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | The result's type. |
| `E` | The error's type. |

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:9](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L9)

___

### SapphirePrefix

Ƭ **SapphirePrefix**: `string` \| readonly `string`[] \| ``null``

A valid prefix in Sapphire.
* `string`: a single prefix, e.g. `'!'`.
* `string[]`: an array of prefixes, e.g. `['!', '.']`.
* `null`: disabled prefix, locks the bot's command usage to mentions only.

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:22](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L22)

___

### SimplePreconditionKeys

Ƭ **SimplePreconditionKeys**: { [K in PreconditionKeys]: Preconditions[K] extends never ? K : never }[[`PreconditionKeys`](#preconditionkeys)]

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:104](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L104)

___

### Some

Ƭ **Some**<`T`\>: `option.Some`<`T`\>

A value that exists.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | The value's type. |

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:13](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L13)

___

### SyncPluginHooks

Ƭ **SyncPluginHooks**: `Exclude`<[`PluginHook`](enums/PluginHook), [`AsyncPluginHooks`](#asyncpluginhooks)\>

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:13](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L13)

## Variables

### Events

• **Events**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `ChannelCreate` | ``"channelCreate"`` |
| `ChannelDelete` | ``"channelDelete"`` |
| `ChannelPinsUpdate` | ``"channelPinsUpdate"`` |
| `ChannelUpdate` | ``"channelUpdate"`` |
| `ClientReady` | ``"ready"`` |
| `CommandAccepted` | ``"commandAccepted"`` |
| `CommandDenied` | ``"commandDenied"`` |
| `CommandError` | ``"commandError"`` |
| `CommandFinish` | ``"commandFinish"`` |
| `CommandRun` | ``"commandRun"`` |
| `CommandSuccess` | ``"commandSuccess"`` |
| `CommandTypingError` | ``"commandTypingError"`` |
| `Debug` | ``"debug"`` |
| `Error` | ``"error"`` |
| `GuildBanAdd` | ``"guildBanAdd"`` |
| `GuildBanRemove` | ``"guildBanRemove"`` |
| `GuildCreate` | ``"guildCreate"`` |
| `GuildDelete` | ``"guildDelete"`` |
| `GuildEmojiCreate` | ``"emojiCreate"`` |
| `GuildEmojiDelete` | ``"emojiDelete"`` |
| `GuildEmojiUpdate` | ``"emojiUpdate"`` |
| `GuildIntegrationsUpdate` | ``"guildIntegrationsUpdate"`` |
| `GuildMemberAdd` | ``"guildMemberAdd"`` |
| `GuildMemberAvailable` | ``"guildMemberAvailable"`` |
| `GuildMemberRemove` | ``"guildMemberRemove"`` |
| `GuildMemberUpdate` | ``"guildMemberUpdate"`` |
| `GuildMembersChunk` | ``"guildMembersChunk"`` |
| `GuildRoleCreate` | ``"roleCreate"`` |
| `GuildRoleDelete` | ``"roleDelete"`` |
| `GuildRoleUpdate` | ``"roleUpdate"`` |
| `GuildUnavailable` | ``"guildUnavailable"`` |
| `GuildUpdate` | ``"guildUpdate"`` |
| `Invalidated` | ``"invalidated"`` |
| `InviteCreate` | ``"inviteCreate"`` |
| `InviteDelete` | ``"inviteDelete"`` |
| `ListenerError` | ``"listenerError"`` |
| `MentionPrefixOnly` | ``"mentionPrefixOnly"`` |
| `MessageBulkDelete` | ``"messageDeleteBulk"`` |
| `MessageCreate` | ``"messageCreate"`` |
| `MessageDelete` | ``"messageDelete"`` |
| `MessageReactionAdd` | ``"messageReactionAdd"`` |
| `MessageReactionRemove` | ``"messageReactionRemove"`` |
| `MessageReactionRemoveAll` | ``"messageReactionRemoveAll"`` |
| `MessageUpdate` | ``"messageUpdate"`` |
| `NonPrefixedMessage` | ``"nonPrefixedMessage"`` |
| `PiecePostLoad` | ``"piecePostLoad"`` |
| `PieceUnload` | ``"pieceUnload"`` |
| `PluginLoaded` | ``"pluginLoaded"`` |
| `PreCommandRun` | ``"preCommandRun"`` |
| `PreMessageParsed` | ``"preMessageParsed"`` |
| `PrefixedMessage` | ``"prefixedMessage"`` |
| `PresenceUpdate` | ``"presenceUpdate"`` |
| `RateLimit` | ``"rateLimit"`` |
| `Raw` | ``"raw"`` |
| `ShardDisconnect` | ``"shardDisconnect"`` |
| `ShardError` | ``"shardError"`` |
| `ShardReady` | ``"shardReady"`` |
| `ShardReconnecting` | ``"shardReconnecting"`` |
| `ShardResume` | ``"shardResume"`` |
| `TypingStart` | ``"typingStart"`` |
| `UnknownCommand` | ``"unknownCommand"`` |
| `UnknownCommandName` | ``"unknownCommandName"`` |
| `UserUpdate` | ``"userUpdate"`` |
| `VoiceStateUpdate` | ``"voiceStateUpdate"`` |
| `Warn` | ``"warn"`` |
| `WebhooksUpdate` | ``"webhookUpdate"`` |

#### Defined in

[projects/framework/src/lib/types/Events.ts:9](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/types/Events.ts#L9)

___

### PreconditionConditionAnd

• **PreconditionConditionAnd**: [`IPreconditionCondition`](interfaces/IPreconditionCondition)

An [IPreconditionCondition](interfaces/IPreconditionCondition) which runs all containers similarly to doing (V0 && V1 [&& V2 [&& V3 ...]]).

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/conditions/PreconditionConditionAnd.ts:8](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/conditions/PreconditionConditionAnd.ts#L8)

___

### PreconditionConditionOr

• **PreconditionConditionOr**: [`IPreconditionCondition`](interfaces/IPreconditionCondition)

An [IPreconditionCondition](interfaces/IPreconditionCondition) which runs all containers similarly to doing (V0 || V1 [|| V2 [|| V3 ...]]).

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/conditions/PreconditionConditionOr.ts:9](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/conditions/PreconditionConditionOr.ts#L9)

___

### container

• **container**: `Container`

The injected variables that will be accessible to any place. To add an extra property, simply add a property with a
regular assignment, and it will be available in all places simultaneously.

**`example`**
```typescript
// Add a reference to the Client:
import { container } from '@sapphire/pieces';

export class SapphireClient extends Client {
  constructor(options) {
    super(options);

    container.client = this;
  }
}

// Can be placed anywhere in a TypeScript file, for JavaScript projects,
// you can create an `augments.d.ts` and place the code there.
declare module '@sapphire/pieces' {
  interface Container {
    client: SapphireClient;
  }
}

// In any piece, core, plugin, or custom:
export class UserCommand extends Command {
  public run(message, args) {
    // The injected client is available here:
    const { client } = this.container;

    // ...
  }
}
```

**`example`**
```typescript
// In a plugin's context, e.g. API:
class Api extends Plugin {
  static [postInitialization]() {
    const server = new Server(this);
    container.server = server;

    // ...
  }
}

declare module '@sapphire/pieces' {
  interface Container {
    server: Server;
  }
}

// In any piece, even those that aren't routes nor middlewares:
export class UserRoute extends Route {
  public [methods.POST](message, args) {
    // The injected server is available here:
    const { server } = this.container;

    // ...
  }
}
```

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:635

___

### postInitialization

• **postInitialization**: unique `symbol`

#### Defined in

[projects/framework/src/lib/plugins/symbols.ts:3](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/symbols.ts#L3)

___

### postLogin

• **postLogin**: unique `symbol`

#### Defined in

[projects/framework/src/lib/plugins/symbols.ts:6](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/symbols.ts#L6)

___

### preGenericsInitialization

• **preGenericsInitialization**: unique `symbol`

#### Defined in

[projects/framework/src/lib/plugins/symbols.ts:1](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/symbols.ts#L1)

___

### preInitialization

• **preInitialization**: unique `symbol`

#### Defined in

[projects/framework/src/lib/plugins/symbols.ts:2](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/symbols.ts#L2)

___

### preLogin

• **preLogin**: unique `symbol`

#### Defined in

[projects/framework/src/lib/plugins/symbols.ts:5](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/symbols.ts#L5)

___

### version

• **version**: `string` = `'[VI]{version}[/VI]'`

The [@sapphire/framework](https://github.com/sapphiredev/framework) version that you are currently using.
An example use of this is showing it of in a bot information command.

Note to Sapphire developers: This needs to explicitly be `string` so it is not typed as the string that gets replaced by Rollup

#### Defined in

[projects/framework/src/index.ts:65](https://github.com/sapphiredev/framework/blob/5a4898f6/src/index.ts#L65)

## Functions

### err

▸ **err**(): [`Err`](#err)<`unknown`\>

Creates an Err with no error.

#### Returns

[`Err`](#err)<`unknown`\>

An erroneous Result.

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:43](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L43)

▸ **err**<`E`\>(`x`): [`Err`](#err)<`E`\>

Creates an Err.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `E` | The error's type. |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `E` | Value to use. |

#### Returns

[`Err`](#err)<`E`\>

An erroneous Result.

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:50](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L50)

___

### from

▸ **from**<`T`, `E`\>(`cb`): [`Result`](#result)<`T`, `E`\>

Creates a [Result](#result) out of a callback.

#### Type parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `T` | `T` | The result's type. |
| `E` | `unknown` | The error's type. |

#### Parameters

| Name | Type |
| :------ | :------ |
| `cb` | (...`args`: `unknown`[]) => `T` |

#### Returns

[`Result`](#result)<`T`, `E`\>

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:78](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L78)

___

### fromAsync

▸ **fromAsync**<`T`, `E`\>(`promiseOrCb`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](#result)<`T`, `E`\>\>

Creates a [Result](#result) out of a promise or async callback.

#### Type parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `T` | `T` | The result's type. |
| `E` | `unknown` | The error's type. |

#### Parameters

| Name | Type |
| :------ | :------ |
| `promiseOrCb` | [`Awaitable`](#awaitable)<`T`\> \| (...`args`: `unknown`[]) => [`Awaitable`](#awaitable)<`T`\> |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](#result)<`T`, `E`\>\>

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:91](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L91)

___

### isErr

▸ **isErr**<`T`, `E`\>(`x`): x is Err<E\>

Determines whether or not a result is an Err.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | The result's type. |
| `E` | The error's type. |

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | [`Result`](#result)<`T`, `E`\> |

#### Returns

x is Err<E\>

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:69](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L69)

___

### isMaybe

▸ **isMaybe**<`T`\>(`x`): ``true``

Type-safe helper to preserve the type parameter's type.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | [`Maybe`](#maybe)<`T`\> | The value to check. |

#### Returns

``true``

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:88](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L88)

▸ **isMaybe**<`T`\>(`x`): x is Maybe<T\>

Determines whether or not an arbitrary value is a Maybe.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `unknown` | The value to check. |

#### Returns

x is Maybe<T\>

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:93](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L93)

___

### isNone

▸ **isNone**<`T`\>(`x`): x is None

Determines whether or not a Maybe is a None.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | The value's type. |

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | [`Maybe`](#maybe)<`T`\> |

#### Returns

x is None

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:80](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L80)

___

### isOk

▸ **isOk**<`T`, `E`\>(`x`): x is Ok<T\>

Determines whether or not a result is an Ok.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | The result's type. |
| `E` | The error's type. |

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | [`Result`](#result)<`T`, `E`\> |

#### Returns

x is Ok<T\>

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:60](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L60)

___

### isSome

▸ **isSome**<`T`\>(`x`): x is Some<T\>

Determines whether or not a Maybe is a Some.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | The value's type. |

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | [`Maybe`](#maybe)<`T`\> |

#### Returns

x is Some<T\>

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:72](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L72)

___

### maybe

▸ **maybe**<`T`, `V`\>(`value`): `V`

Returns the maybe itself.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `T` |
| `V` | extends [`Maybe`](#maybe)<`T`\> |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `V` | The value to convert. |

#### Returns

`V`

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:24](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L24)

▸ **maybe**(`value`): [`None`](#none)

Creates a [None](#none) from an existing [None](#none) or a `null`.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | ``null`` \| `None` | The value to convert. |

#### Returns

[`None`](#none)

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:29](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L29)

▸ **maybe**<`T`\>(`value`): [`Maybe`](#maybe)<`T`\>

Creates a [Some](#some) from a non-null value or an existing [Some](#some), or a [None](#none) otherwise.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | ``null`` \| `T` \| [`Maybe`](#maybe)<`T`\> | The value to convert. |

#### Returns

[`Maybe`](#maybe)<`T`\>

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:34](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L34)

▸ **maybe**<`T`\>(`value`): [`Some`](#some)<`T`\>

Creates a [Some](#some) from a non-null value or an existing [Some](#some).

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `T` \| [`Some`](#some)<`T`\> | The value to convert. |

#### Returns

[`Some`](#some)<`T`\>

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:39](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L39)

___

### none

▸ **none**(): [`None`](#none)

Creates a None value.

#### Returns

[`None`](#none)

A non-existing Maybe.

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:64](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L64)

___

### ok

▸ **ok**(): [`Ok`](#ok)<`unknown`\>

Creates an Ok with no value.

#### Returns

[`Ok`](#ok)<`unknown`\>

A successful Result.

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:27](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L27)

▸ **ok**<`T`\>(`x`): [`Ok`](#ok)<`T`\>

Creates an Ok.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | The result's type. |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `T` | Value to use. |

#### Returns

[`Ok`](#ok)<`T`\>

A successful Result.

#### Defined in

[projects/framework/src/lib/parsers/Result.ts:34](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Result.ts#L34)

___

### some

▸ **some**(): [`Some`](#some)<`unknown`\>

Creates a None with no value.

#### Returns

[`Some`](#some)<`unknown`\>

An existing Maybe.

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:48](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L48)

▸ **some**<`T`\>(`x`): [`Some`](#some)<`T`\>

Creates a None with a value.

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | The value's type. |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `T` | Value to use. |

#### Returns

[`Some`](#some)<`T`\>

An existing Maybe.

#### Defined in

[projects/framework/src/lib/parsers/Maybe.ts:55](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Maybe.ts#L55)

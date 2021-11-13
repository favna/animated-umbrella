---
id: "SapphireClientOptions"
title: "Interface: SapphireClientOptions"
sidebar_label: "SapphireClientOptions"
sidebar_position: 0
custom_edit_url: null
---

## Properties

### baseUserDirectory

• `Optional` **baseUserDirectory**: ``null`` \| `string`

The base user directory, if set to `null`, Sapphire will not call [StoreRegistry.registerPath](../classes/StoreRegistry#registerpath),
meaning that you will need to manually set each folder for each store. Please read the aforementioned method's
documentation for more information.

**`since`** 1.0.0

**`default`** undefined

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:36](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L36)

___

### caseInsensitiveCommands

• `Optional` **caseInsensitiveCommands**: ``null`` \| `boolean`

Whether commands can be case insensitive

**`since`** 1.0.0

**`default`** false

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:43](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L43)

___

### caseInsensitivePrefixes

• `Optional` **caseInsensitivePrefixes**: ``null`` \| `boolean`

Whether prefixes can be case insensitive

**`since`** 1.0.0

**`default`** false

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:50](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L50)

___

### defaultCooldown

• `Optional` **defaultCooldown**: [`CooldownOptions`](CooldownOptions)

Sets the default cooldown time for all commands.

**`default`** "No cooldown options"

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:122](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L122)

___

### defaultPrefix

• `Optional` **defaultPrefix**: [`SapphirePrefix`](../#sapphireprefix)

The default prefix, in case of `null`, only mention prefix will trigger the bot's commands.

**`since`** 1.0.0

**`default`** null

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:57](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L57)

___

### enableLoaderTraceLoggings

• `Optional` **enableLoaderTraceLoggings**: `boolean`

Whether or not trace logging should be enabled.

**`since`** 2.0.0

**`default`** container.logger.has(LogLevel.Trace)

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:103](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L103)

___

### fetchPrefix

• `Optional` **fetchPrefix**: [`SapphirePrefixHook`](SapphirePrefixHook)

The prefix hook, by default it is a callback function that returns [SapphireClientOptions.defaultPrefix](SapphireClientOptions#defaultprefix).

**`since`** 1.0.0

**`default`** () => client.options.defaultPrefix

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:82](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L82)

___

### id

• `Optional` **id**: `string`

The client's ID, this is automatically set by the CoreReady event.

**`since`** 1.0.0

**`default`** this.client.user?.id ?? null

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:89](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L89)

___

### loadDefaultErrorListeners

• `Optional` **loadDefaultErrorListeners**: `boolean`

If Sapphire should load our pre-included error event listeners that log any encountered errors to the [SapphireClient.logger](../classes/SapphireClient#logger) instance

**`since`** 1.0.0

**`default`** true

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:110](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L110)

___

### logger

• `Optional` **logger**: [`ClientLoggerOptions`](ClientLoggerOptions)

The logger options, defaults to an instance of [Logger](../classes/Logger) when [ClientLoggerOptions.instance](ClientLoggerOptions#instance) is not specified.

**`since`** 1.0.0

**`default`** { instance: new Logger(LogLevel.Info) }

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:96](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L96)

___

### regexPrefix

• `Optional` **regexPrefix**: [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

The regex prefix, an alternative to a mention or regular prefix to allow creating natural language command messages

**`since`** 1.0.0

**`example`**
```typescript
/^(hey +)?bot[,! ]/i

// Matches:
// - hey bot,
// - hey bot!
// - hey bot
// - bot,
// - bot!
// - bot
```

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:75](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L75)

___

### typing

• `Optional` **typing**: `boolean`

Controls whether the bot will automatically appear to be typing when a command is accepted.

**`default`** false

#### Defined in

[projects/framework/src/lib/SapphireClient.ts:116](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/SapphireClient.ts#L116)

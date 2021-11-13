---
id: "CommandOptions"
title: "Interface: CommandOptions"
sidebar_label: "CommandOptions"
sidebar_position: 0
custom_edit_url: null
---

The [Command](../classes/Command) options.

**`since`** 1.0.0

## Hierarchy

- [`AliasPieceOptions`](AliasPieceOptions)

- `FlagStrategyOptions`

  ↳ **`CommandOptions`**

## Properties

### aliases

• `Optional` `Readonly` **aliases**: readonly `string`[]

The aliases for the piece.

**`default`** []

#### Inherited from

[AliasPieceOptions](AliasPieceOptions).[aliases](AliasPieceOptions#aliases)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:661

___

### cooldownDelay

• `Optional` **cooldownDelay**: `number`

The time in milliseconds for the cooldown entries to reset, if set to a non-zero value alongside [CommandOptions.cooldownLimit](CommandOptions#cooldownlimit), the `Cooldown` precondition will be added to the list.

**`since`** 2.0.0

**`default`** 0

#### Defined in

[projects/framework/src/lib/structures/Command.ts:467](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L467)

___

### cooldownFilteredUsers

• `Optional` **cooldownFilteredUsers**: `string`[]

The users that are exempt from the Cooldown precondition.
Use this to filter out someone like a bot owner

**`since`** 2.0.0

**`default`** undefined

#### Defined in

[projects/framework/src/lib/structures/Command.ts:482](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L482)

___

### cooldownLimit

• `Optional` **cooldownLimit**: `number`

The amount of entries the cooldown can have before filling up, if set to a non-zero value alongside [CommandOptions.cooldownDelay](CommandOptions#cooldowndelay), the `Cooldown` precondition will be added to the list.

**`since`** 2.0.0

**`default`** 1

#### Defined in

[projects/framework/src/lib/structures/Command.ts:460](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L460)

___

### cooldownScope

• `Optional` **cooldownScope**: [`BucketScope`](../enums/BucketScope)

The scope of the cooldown entries.

**`since`** 2.0.0

**`default`** BucketScope.User

#### Defined in

[projects/framework/src/lib/structures/Command.ts:474](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L474)

___

### description

• `Optional` **description**: `string`

The description for the command.

**`since`** 1.0.0

**`default`** ''

#### Defined in

[projects/framework/src/lib/structures/Command.ts:404](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L404)

___

### detailedDescription

• `Optional` **detailedDescription**: `string`

The detailed description for the command.

**`since`** 1.0.0

**`default`** ''

#### Defined in

[projects/framework/src/lib/structures/Command.ts:411](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L411)

___

### enabled

• `Optional` `Readonly` **enabled**: `boolean`

Whether or not the piece should be enabled. If set to false, the piece will be unloaded.

**`default`** true

#### Inherited from

[AliasPieceOptions](AliasPieceOptions).[enabled](AliasPieceOptions#enabled)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:411

___

### flags

• `Optional` **flags**: `boolean` \| readonly `string`[]

The accepted flags. Flags are key-only identifiers that can be placed anywhere in the command. Two different types are accepted:
* An array of strings, e.g. [`silent`].
* A boolean defining whether the strategy should accept all keys (`true`) or none at all (`false`).

**`default`** []

#### Inherited from

FlagStrategyOptions.flags

#### Defined in

[projects/framework/src/lib/utils/strategies/FlagUnorderedStrategy.ts:13](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/strategies/FlagUnorderedStrategy.ts#L13)

___

### fullCategory

• `Optional` **fullCategory**: `string`[]

The full category path for the command

**`since`** 2.0.0

**`default`** 'An array of folder names that lead back to the folder that is registered for in the commands store'

**`example`**
```typescript
// Given a file named `ping.js` at the path of `commands/General/ping.js`
['General']

// Given a file named `info.js` at the path of `commands/General/About/ping.js`
['General', 'About']
```

#### Defined in

[projects/framework/src/lib/structures/Command.ts:426](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L426)

___

### generateDashLessAliases

• `Optional` **generateDashLessAliases**: `boolean`

Whether to add aliases for commands with dashes in them

**`since`** 1.0.0

**`default`** false

#### Defined in

[projects/framework/src/lib/structures/Command.ts:397](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L397)

___

### name

• `Optional` `Readonly` **name**: `string`

The name for the piece.

**`default`** ''

#### Inherited from

[AliasPieceOptions](AliasPieceOptions).[name](AliasPieceOptions#name)

#### Defined in

node_modules/@sapphire/pieces/dist/index.d.ts:406

___

### nsfw

• `Optional` **nsfw**: `boolean`

Sets whether or not the command should be treated as NSFW. If set to true, the `NSFW` precondition will be added to the list.

**`since`** 2.0.0

**`default`** false

#### Defined in

[projects/framework/src/lib/structures/Command.ts:453](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L453)

___

### options

• `Optional` **options**: `boolean` \| readonly `string`[]

The accepted options. Options are key-value identifiers that can be placed anywhere in the command. Two different types are accepted:
* An array of strings, e.g. [`silent`].
* A boolean defining whether the strategy should accept all keys (`true`) or none at all (`false`).

**`default`** []

#### Inherited from

FlagStrategyOptions.options

#### Defined in

[projects/framework/src/lib/utils/strategies/FlagUnorderedStrategy.ts:21](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/strategies/FlagUnorderedStrategy.ts#L21)

___

### preconditions

• `Optional` **preconditions**: readonly [`PreconditionEntryResolvable`](../#preconditionentryresolvable)[]

The [Precondition](../classes/Precondition)s to be run, accepts an array of their names.

**`seealso`** [PreconditionContainerArray](../classes/PreconditionContainerArray)

**`since`** 1.0.0

**`default`** []

#### Defined in

[projects/framework/src/lib/structures/Command.ts:434](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L434)

___

### prefixes

• `Optional` **prefixes**: `string`[]

The prefixes for both flags and options.

**`default`** ['--', '-', '—']

#### Inherited from

FlagStrategyOptions.prefixes

#### Defined in

[projects/framework/src/lib/utils/strategies/FlagUnorderedStrategy.ts:27](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/strategies/FlagUnorderedStrategy.ts#L27)

___

### quotes

• `Optional` **quotes**: [`string`, `string`][]

The quotes accepted by this command, pass `[]` to disable them.

**`since`** 1.0.0

**`default`**
[
  ['"', '"'], // Double quotes
  ['“', '”'], // Fancy quotes (on iOS)
  ['「', '」'] // Corner brackets (CJK)
]

#### Defined in

[projects/framework/src/lib/structures/Command.ts:446](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L446)

___

### requiredClientPermissions

• `Optional` **requiredClientPermissions**: `PermissionResolvable`

The required permissions for the client.

**`since`** 2.0.0

**`default`** 0

#### Defined in

[projects/framework/src/lib/structures/Command.ts:489](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L489)

___

### requiredUserPermissions

• `Optional` **requiredUserPermissions**: `PermissionResolvable`

The required permissions for the user.

**`since`** 2.0.0

**`default`** 0

#### Defined in

[projects/framework/src/lib/structures/Command.ts:496](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L496)

___

### runIn

• `Optional` **runIn**: ``null`` \| [`CommandOptionsRunType`](../#commandoptionsruntype) \| [`CommandOptionsRunTypeEnum`](../enums/CommandOptionsRunTypeEnum) \| readonly ([`CommandOptionsRunType`](../#commandoptionsruntype) \| [`CommandOptionsRunTypeEnum`](../enums/CommandOptionsRunTypeEnum))[]

The channels the command should run in. If set to `null`, no precondition entry will be added. Some optimizations are applied when given an array to reduce the amount of preconditions run (e.g. `'text'` and `'news'` becomes `'guild'`, and if both `'dm'` and `'guild'` are defined, then no precondition entry is added as it runs in all channels).

**`since`** 2.0.0

**`default`** null

#### Defined in

[projects/framework/src/lib/structures/Command.ts:503](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L503)

___

### separators

• `Optional` **separators**: `string`[]

The flag separators.

**`default`** ['=', ':']

#### Inherited from

FlagStrategyOptions.separators

#### Defined in

[projects/framework/src/lib/utils/strategies/FlagUnorderedStrategy.ts:33](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/strategies/FlagUnorderedStrategy.ts#L33)

___

### typing

• `Optional` **typing**: `boolean`

If {@link SapphireClient.typing} is true, this option will override it.
Otherwise, this option has no effect - you may call {@link Channel#sendTyping}` in the run method if you want specific commands to display the typing status.

**`default`** true

#### Defined in

[projects/framework/src/lib/structures/Command.ts:510](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Command.ts#L510)

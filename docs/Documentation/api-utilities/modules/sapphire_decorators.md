---
id: "sapphire_decorators"
title: "Module: @sapphire/decorators"
sidebar_label: "@sapphire/decorators"
sidebar_position: 0
custom_edit_url: null
---

## Enumerations

- [DecoratorIdentifiers](../enums/sapphire_decorators.DecoratorIdentifiers)

## Interfaces

- [FunctionFallback](../interfaces/sapphire_decorators.FunctionFallback)
- [FunctionPrecondition](../interfaces/sapphire_decorators.FunctionPrecondition)

## Functions

### ApplyOptions

▸ **ApplyOptions**<`T`\>(`optionsOrFn`): `ClassDecorator`

Decorator function that applies given options to any Sapphire piece

**`example`**
```typescript
import { ApplyOptions } from '@sapphire/decorators';
import { Command, CommandOptions } from '@sapphire/framework';
import type { Message } from 'discord.js';

(at)ApplyOptions<CommandOptions>({
	description: 'ping pong',
	enabled: true
})
export class UserCommand extends Command {
	public async messageRun(message: Message) {
		const msg = await message.channel.send('Ping?');

		return msg.edit(
			`Pong! Client Latency ${Math.round(this.context.client.ws.ping)}ms. API Latency ${msg.createdTimestamp - message.createdTimestamp}ms.`
		);
	}
}
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends `PieceOptions` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `optionsOrFn` | `T` \| (`context`: `PieceContext`) => `T` |

#### Returns

`ClassDecorator`

#### Defined in

[projects/utilities/packages/decorators/src/piece-decorators.ts:29](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/piece-decorators.ts#L29)

___

### Enumerable

▸ **Enumerable**(`value`): (`target`: `unknown`, `key`: `string`) => `void`

Decorator that sets the enumerable property of a class field to the desired value.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `boolean` | Whether the property should be enumerable or not |

#### Returns

`fn`

▸ (`target`, `key`): `void`

##### Parameters

| Name | Type |
| :------ | :------ |
| `target` | `unknown` |
| `key` | `string` |

##### Returns

`void`

#### Defined in

[projects/utilities/packages/decorators/src/base-decorators.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/base-decorators.ts#L8)

___

### EnumerableMethod

▸ **EnumerableMethod**(`value`): `MethodDecorator`

Decorator that sets the enumerable property of a class method to the desired value.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `boolean` | Whether the method should be enumerable or not |

#### Returns

`MethodDecorator`

#### Defined in

[projects/utilities/packages/decorators/src/base-decorators.ts:36](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/base-decorators.ts#L36)

___

### RequiresClientPermissions

▸ `Const` **RequiresClientPermissions**(...`permissionsResolvable`): `MethodDecorator`

Allows you to set permissions required for individual methods. This is particularly useful for subcommands that require specific permissions.

**`remark`** This decorator applies to the client that is to execute the command. For setting permissions required user of the command see [RequiresUserPermissions](sapphire_decorators#requiresuserpermissions)

**`remark`** This decorator makes the decorated function asynchronous, so any result should be `await`ed.

**`example`**
```typescript
import { ApplyOptions, RequiresClientPermissions } from '@sapphire/decorators';
import { SubCommandPluginCommand, SubCommandPluginCommandOptions } from '@sapphire/plugin-subcommands';
import type { Message } from 'discord.js';

(at)ApplyOptions<SubCommandPluginCommandOptions>({
	aliases: ['cws'],
	description: 'A basic command with some subcommands',
	subCommands: ['add', 'remove', 'reset', { input: 'show', default: true }]
})
export default class extends SubCommandPluginCommand {
    // Anyone should be able to view the result, but not modify
	public async show(message: Message) {
		return message.channel.send('Showing!');
	}

	(at)RequiresClientPermissions('BAN_MEMBERS') // This subcommand requires the client to be able to ban members.
	public async add(message: Message) {
		return message.channel.send('Adding!');
	}

	(at)RequiresClientPermissions('BAN_MEMBERS') // This subcommand requires the client to be able to ban members.
	public async remove(message: Message) {
		return message.channel.send('Removing!');
	}

	(at)RequiresClientPermissions('BAN_MEMBERS') // This subcommand requires the client to be able to ban members.
	public async reset(message: Message) {
		return message.channel.send('Resetting!');
	}
}
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...permissionsResolvable` | `PermissionResolvable`[] | Permissions that the method should have. |

#### Returns

`MethodDecorator`

#### Defined in

[projects/utilities/packages/decorators/src/djs-decorators.ts:79](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/djs-decorators.ts#L79)

___

### RequiresDMContext

▸ **RequiresDMContext**(`fallback?`): `MethodDecorator`

Requires the message to be run in a dm context, this decorator requires the first argument to be a `Message` instance

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fallback` | [`FunctionFallback`](../interfaces/sapphire_decorators.FunctionFallback) | The fallback value passed to `createFunctionInhibitor` |

#### Returns

`MethodDecorator`

#### Defined in

[projects/utilities/packages/decorators/src/djs-decorators.ts:192](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/djs-decorators.ts#L192)

___

### RequiresGuildContext

▸ **RequiresGuildContext**(`fallback?`): `MethodDecorator`

Requires the message to be run in a guild context, this decorator requires the first argument to be a `Message` instance

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fallback` | [`FunctionFallback`](../interfaces/sapphire_decorators.FunctionFallback) | The fallback value passed to `createFunctionInhibitor` |

#### Returns

`MethodDecorator`

#### Defined in

[projects/utilities/packages/decorators/src/djs-decorators.ts:183](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/djs-decorators.ts#L183)

___

### RequiresUserPermissions

▸ `Const` **RequiresUserPermissions**(...`permissionsResolvable`): `MethodDecorator`

Allows you to set permissions required for individual methods. This is particularly useful for subcommands that require specific permissions.

**`remark`** This decorator applies to the user of the command. For setting permissions required for the client see [RequiresClientPermissions](sapphire_decorators#requiresclientpermissions)

**`remark`** This decorator makes the decorated function asynchronous, so any result should be `await`ed.

**`example`**
```typescript
import { ApplyOptions, RequiresUserPermissions } from '@sapphire/decorators';
import { SubCommandPluginCommand, SubCommandPluginCommandOptions } from '@sapphire/plugin-subcommands';
import type { Message } from 'discord.js';

(at)ApplyOptions<SubCommandPluginCommandOptions>({
	aliases: ['cws'],
	description: 'A basic command with some subcommands',
	subCommands: ['add', 'remove', 'reset', { input: 'show', default: true }]
})
export default class extends SubCommandPluginCommand {
    // Anyone should be able to view the result, but not modify
	public async show(message: Message) {
		return message.channel.send('Showing!');
	}

	(at)RequiresUserPermissions('BAN_MEMBERS') // This subcommand requires the user of the command to be able to ban members.
	public async add(message: Message) {
		return message.channel.send('Adding!');
	}

	(at)RequiresUserPermissions('BAN_MEMBERS') // This subcommand requires the user of the command to be able to ban members.
	public async remove(message: Message) {
		return message.channel.send('Removing!');
	}

	(at)RequiresUserPermissions('BAN_MEMBERS') // This subcommand requires the user of the command to be able to ban members.
	public async reset(message: Message) {
		return message.channel.send('Resetting!');
	}
}
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...permissionsResolvable` | `PermissionResolvable`[] | Permissions that the method should have. |

#### Returns

`MethodDecorator`

#### Defined in

[projects/utilities/packages/decorators/src/djs-decorators.ts:148](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/djs-decorators.ts#L148)

___

### createClassDecorator

▸ **createClassDecorator**<`TFunction`\>(`fn`): `ClassDecorator`

Utility to make a class decorator with lighter syntax and inferred types.

**`see`** [ApplyOptions](sapphire_decorators#applyoptions)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `TFunction` | extends (...`args`: `any`[]) => `void` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | `TFunction` | The class to decorate |

#### Returns

`ClassDecorator`

#### Defined in

[projects/utilities/packages/decorators/src/utils.ts:43](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/utils.ts#L43)

___

### createFunctionPrecondition

▸ **createFunctionPrecondition**(`precondition`, `fallback?`): `MethodDecorator`

Utility to make function preconditions.

```typescript
// No fallback (returns undefined)
function requireGuild(value: number) {
  return createFunctionPrecondition((message: Message) =>
    message.guild !== null
  );
}

// With fallback
function requireGuild(
  value: number,
  fallback: () => unknown = () => undefined
) {
  return createFunctionPrecondition(
    (message: Message) => message.guild !== null,
    fallback
  );
}
```

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `precondition` | [`FunctionPrecondition`](../interfaces/sapphire_decorators.FunctionPrecondition) | The function that defines whether or not the function should be run, returning the returned value from fallback |
| `fallback` | [`FunctionFallback`](../interfaces/sapphire_decorators.FunctionFallback) | The fallback value that defines what the method should return in case the precondition fails |

#### Returns

`MethodDecorator`

#### Defined in

[projects/utilities/packages/decorators/src/utils.ts:73](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/utils.ts#L73)

___

### createMethodDecorator

▸ **createMethodDecorator**(`fn`): `MethodDecorator`

Utility to make a method decorator with lighter syntax and inferred types.

```typescript
// Enumerable function
	function enumerableMethod(value: boolean) {
		return createMethodDecorator((_target, _propertyKey, descriptor) => {
			descriptor.enumerable = value;
		});
	}
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fn` | `MethodDecorator` | The method to decorate |

#### Returns

`MethodDecorator`

#### Defined in

[projects/utilities/packages/decorators/src/utils.ts:34](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/utils.ts#L34)

___

### enumerable

▸ `Const` **enumerable**(`value`): (`target`: `unknown`, `key`: `string`) => `void`

Decorator that sets the enumerable property of a class field to the desired value.

**`deprecated`** Use `@Enumerable` instead.
The lowercased decorator will be removed in the next major version of `@sapphire/decorators`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `boolean` | Whether the property should be enumerable or not |

#### Returns

`fn`

▸ (`target`, `key`): `void`

##### Parameters

| Name | Type |
| :------ | :------ |
| `target` | `unknown` |
| `key` | `string` |

##### Returns

`void`

#### Defined in

[projects/utilities/packages/decorators/src/base-decorators.ts:30](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/base-decorators.ts#L30)

___

### enumerableMethod

▸ `Const` **enumerableMethod**(`value`): `MethodDecorator`

Decorator that sets the enumerable property of a class method to the desired value.

**`deprecated`** Use `@EnumerableMethod` instead.
The lowercased decorator will be removed in the next major version of `@sapphire/decorators`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `boolean` | Whether the method should be enumerable or not |

#### Returns

`MethodDecorator`

#### Defined in

[projects/utilities/packages/decorators/src/base-decorators.ts:48](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/decorators/src/base-decorators.ts#L48)

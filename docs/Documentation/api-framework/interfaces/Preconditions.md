---
id: "Preconditions"
title: "Interface: Preconditions"
sidebar_label: "Preconditions"
sidebar_position: 0
custom_edit_url: null
---

The registered preconditions and their contexts, if any. When registering new ones, it is recommended to use
[module augmentation](https://www.typescriptlang.org/docs/handbook/declaration-merging.html#module-augmentation) so
custom ones are registered.

When a key's value is `never`, it means that it does not take any context, which allows you to pass its identifier as
a bare string (e.g. `preconditions: ['NSFW']`), however, if context is required, a non-`never` type should be passed,
which will type {@link PreconditionContainerArray#append} and require an object with the name and a `context` with
the defined type.

**`example`**
```typescript
declare module '@sapphire/framework' {
  interface Preconditions {
    // A precondition named `Moderator` which does not read `context`:
    Moderator: never;

    // A precondition named `ChannelPermissions` which does read `context`:
    ChannelPermissions: {
      permissions: Permissions;
    };
  }
}

// [✔] These are valid:
preconditions.append('Moderator');
preconditions.append({ name: 'Moderator' });
preconditions.append({
  name: 'ChannelPermissions',
  context: { permissions: new Permissions(8) }
});

// [X] These are invalid:
preconditions.append({ name: 'Moderator', context: {} });
// ➡ `never` keys do not accept `context`.

preconditions.append('ChannelPermissions');
// ➡ non-`never` keys always require `context`, a string cannot be used.

preconditions.append({
  name: 'ChannelPermissions',
  context: { unknownProperty: 1 }
});
// ➡ mismatching `context` properties, `{ unknownProperty: number }` is not
// assignable to `{ permissions: Permissions }`.
```

## Properties

### ClientPermissions

• **ClientPermissions**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `permissions` | [`Permissions`](https://discord.js.org/#/docs/main/stable/class/Permissions) |

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:95](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L95)

___

### Cooldown

• **Cooldown**: [`CooldownContext`](CooldownContext)

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:84](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L84)

___

### DMOnly

• **DMOnly**: `never`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:85](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L85)

___

### Enabled

• **Enabled**: `never`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:86](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L86)

___

### GuildNewsOnly

• **GuildNewsOnly**: `never`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:87](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L87)

___

### GuildNewsThreadOnly

• **GuildNewsThreadOnly**: `never`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:88](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L88)

___

### GuildOnly

• **GuildOnly**: `never`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:89](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L89)

___

### GuildPrivateThreadOnly

• **GuildPrivateThreadOnly**: `never`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:90](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L90)

___

### GuildPublicThreadOnly

• **GuildPublicThreadOnly**: `never`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:91](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L91)

___

### GuildTextOnly

• **GuildTextOnly**: `never`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:92](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L92)

___

### GuildThreadOnly

• **GuildThreadOnly**: `never`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:93](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L93)

___

### NSFW

• **NSFW**: `never`

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:94](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L94)

___

### UserPermissions

• **UserPermissions**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `permissions` | [`Permissions`](https://discord.js.org/#/docs/main/stable/class/Permissions) |

#### Defined in

[projects/framework/src/lib/structures/Precondition.ts:98](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/structures/Precondition.ts#L98)

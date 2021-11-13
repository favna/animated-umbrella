---
id: "ClientPermissionsPrecondition"
title: "Class: ClientPermissionsPrecondition"
sidebar_label: "ClientPermissionsPrecondition"
sidebar_position: 0
custom_edit_url: null
---

Constructs a contextful permissions precondition requirement.

**`since`** 1.0.0

**`example`**
```typescript
export class CoreCommand extends Command {
  public constructor(context: PieceContext) {
    super(context, {
      preconditions: [
        'GuildOnly',
        new ClientPermissionsPrecondition('ADD_REACTIONS')
      ]
    });
  }

  public messageRun(message: Message, args: Args) {
    // ...
  }
}
```

## Implements

- [`PreconditionSingleResolvableDetails`](../interfaces/PreconditionSingleResolvableDetails)<``"ClientPermissions"``\>

## Constructors

### constructor

• **new ClientPermissionsPrecondition**(`permissions`)

Constructs a precondition container entry.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `permissions` | `PermissionResolvable` | The permissions that will be required by this command. |

#### Defined in

[projects/framework/src/lib/utils/preconditions/containers/ClientPermissionsPrecondition.ts:33](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/containers/ClientPermissionsPrecondition.ts#L33)

## Properties

### context

• **context**: `Object`

The context to be set at [PreconditionContainerSingle.context](PreconditionContainerSingle#context).

#### Type declaration

| Name | Type |
| :------ | :------ |
| `permissions` | [`Permissions`](https://discord.js.org/#/docs/main/stable/class/Permissions) |

#### Implementation of

[PreconditionSingleResolvableDetails](../interfaces/PreconditionSingleResolvableDetails).[context](../interfaces/PreconditionSingleResolvableDetails#context)

#### Defined in

[projects/framework/src/lib/utils/preconditions/containers/ClientPermissionsPrecondition.ts:27](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/containers/ClientPermissionsPrecondition.ts#L27)

___

### name

• **name**: ``"ClientPermissions"``

The name of the precondition to retrieve from {@link SapphireClient.preconditions}.

#### Implementation of

[PreconditionSingleResolvableDetails](../interfaces/PreconditionSingleResolvableDetails).[name](../interfaces/PreconditionSingleResolvableDetails#name)

#### Defined in

[projects/framework/src/lib/utils/preconditions/containers/ClientPermissionsPrecondition.ts:26](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/containers/ClientPermissionsPrecondition.ts#L26)

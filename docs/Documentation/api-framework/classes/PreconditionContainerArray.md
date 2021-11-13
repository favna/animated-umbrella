---
id: "PreconditionContainerArray"
title: "Class: PreconditionContainerArray"
sidebar_label: "PreconditionContainerArray"
sidebar_position: 0
custom_edit_url: null
---

An [IPreconditionContainer](../interfaces/IPreconditionContainer) that defines an array of multiple [IPreconditionContainer](../interfaces/IPreconditionContainer)s.

By default, array containers run either of two conditions: AND and OR ([PreconditionRunCondition](../enums/PreconditionRunCondition)), the top level
will always default to AND, where the nested one flips the logic (OR, then children arrays are AND, then OR...).

This allows `['Connect', ['Moderator', ['DJ', 'SongAuthor']]]` to become a thrice-nested precondition container, where:
- Level 1: [Single(Connect), Array] runs AND, both containers must return a successful value.
- Level 2: [Single(Moderator), Array] runs OR, either container must return a successful value.
- Level 3: [Single(DJ), Single(SongAuthor)] runs AND, both containers must return a successful value.

In other words, it is identical to doing:
```typescript
Connect && (Moderator || (DJ && SongAuthor));
```

**`remark`** More advanced logic can be accomplished by adding more [IPreconditionCondition](../interfaces/IPreconditionCondition)s (e.g. other operators),
see [PreconditionContainerArray.conditions](PreconditionContainerArray#conditions) for more information.

**`since`** 1.0.0

## Implements

- [`IPreconditionContainer`](../interfaces/IPreconditionContainer)

## Constructors

### constructor

• **new PreconditionContainerArray**(`data?`, `parent?`)

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `data` | [`PreconditionArrayResolvable`](../#preconditionarrayresolvable) | `[]` |
| `parent` | ``null`` \| [`PreconditionContainerArray`](PreconditionContainerArray) | `null` |

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:127](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L127)

## Properties

### entries

• `Readonly` **entries**: [`IPreconditionContainer`](../interfaces/IPreconditionContainer)[]

The [IPreconditionContainer](../interfaces/IPreconditionContainer)s the array holds.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:119](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L119)

___

### mode

• `Readonly` **mode**: [`PreconditionRunMode`](../enums/PreconditionRunMode)

The mode at which this precondition will run.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:113](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L113)

___

### runCondition

• `Readonly` **runCondition**: [`PreconditionRunCondition`](../enums/PreconditionRunCondition)

The [PreconditionRunCondition](../enums/PreconditionRunCondition) that defines how entries must be handled.

**`since`** 1.0.0

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:125](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L125)

___

### conditions

▪ `Static` `Readonly` **conditions**: `Collection`<[`PreconditionRunCondition`](../enums/PreconditionRunCondition), [`IPreconditionCondition`](../interfaces/IPreconditionCondition)\>

The preconditions to be run. Extra ones can be added by augmenting [PreconditionRunCondition](../enums/PreconditionRunCondition) and then
inserting [IPreconditionCondition](../interfaces/IPreconditionCondition)s.

**`since`** 1.0.0

**`example`**
```typescript
// Adding more kinds of conditions

// Set the new condition:
PreconditionContainerArray.conditions.set(2, PreconditionConditionRandom);

// Augment Sapphire to add the new condition, in case of a JavaScript
// project, this can be moved to an `Augments.d.ts` (or any other name)
// file somewhere:
declare module '@sapphire/framework' {
  export enum PreconditionRunCondition {
    Random = 2
  }
}
```

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:219](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L219)

## Accessors

### condition

• `Protected` `get` **condition**(): [`IPreconditionCondition`](../interfaces/IPreconditionCondition)

Retrieves a condition from [PreconditionContainerArray.conditions](PreconditionContainerArray#conditions), assuming existence.

**`since`** 1.0.0

#### Returns

[`IPreconditionCondition`](../interfaces/IPreconditionCondition)

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:194](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L194)

## Methods

### add

▸ **add**(`entry`): [`PreconditionContainerArray`](PreconditionContainerArray)

Adds a new entry to the array.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `entry` | [`IPreconditionContainer`](../interfaces/IPreconditionContainer) | The value to add to the entries. |

#### Returns

[`PreconditionContainerArray`](PreconditionContainerArray)

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:149](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L149)

___

### append

▸ **append**(`keyOrEntries`): [`PreconditionContainerArray`](PreconditionContainerArray)

#### Parameters

| Name | Type |
| :------ | :------ |
| `keyOrEntries` | [`PreconditionContainerArray`](PreconditionContainerArray) \| [`SimplePreconditionKeys`](../#simplepreconditionkeys) \| [`SimplePreconditionSingleResolvableDetails`](../interfaces/SimplePreconditionSingleResolvableDetails) |

#### Returns

[`PreconditionContainerArray`](PreconditionContainerArray)

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:154](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L154)

▸ **append**<`K`\>(`entry`): [`PreconditionContainerArray`](PreconditionContainerArray)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`Preconditions`](../interfaces/Preconditions) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `entry` | [`PreconditionSingleResolvableDetails`](../interfaces/PreconditionSingleResolvableDetails)<`K`\> |

#### Returns

[`PreconditionContainerArray`](PreconditionContainerArray)

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:155](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L155)

___

### parse

▸ `Protected` **parse**(`entries`): [`PreconditionContainerArray`](PreconditionContainerArray)

Parses the precondition entry resolvables, and adds them to the entries.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `entries` | `Iterable`<[`PreconditionEntryResolvable`](../#preconditionentryresolvable)\> | The entries to parse. |

#### Returns

[`PreconditionContainerArray`](PreconditionContainerArray)

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:178](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L178)

___

### run

▸ **run**(`message`, `command`, `context?`): [`PreconditionContainerReturn`](../#preconditioncontainerreturn)

Runs the container.

**`since`** 1.0.0

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> | The message that ran this precondition. |
| `command` | [`Command`](Command)<[`Args`](Args), [`CommandOptions`](../interfaces/CommandOptions)\> | The command the message invoked. |
| `context` | [`PreconditionContext`](../interfaces/PreconditionContext) | - |

#### Returns

[`PreconditionContainerReturn`](../#preconditioncontainerreturn)

#### Implementation of

[IPreconditionContainer](../interfaces/IPreconditionContainer).[run](../interfaces/IPreconditionContainer#run)

#### Defined in

[projects/framework/src/lib/utils/preconditions/PreconditionContainerArray.ts:167](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/preconditions/PreconditionContainerArray.ts#L167)

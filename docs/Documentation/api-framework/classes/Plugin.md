---
id: "Plugin"
title: "Class: Plugin"
sidebar_label: "Plugin"
sidebar_position: 0
custom_edit_url: null
---

## Constructors

### constructor

• **new Plugin**()

## Properties

### [postInitialization]

▪ `Static` `Optional` **[postInitialization]**: (`options`: `ClientOptions`) => `void`

#### Type declaration

▸ (`options`): `void`

##### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `ClientOptions` |

##### Returns

`void`

#### Defined in

[projects/framework/src/lib/plugins/Plugin.ts:10](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/Plugin.ts#L10)

___

### [postLogin]

▪ `Static` `Optional` **[postLogin]**: (`options`: `ClientOptions`) => [`Awaitable`](../#awaitable)<`void`\>

#### Type declaration

▸ (`options`): [`Awaitable`](../#awaitable)<`void`\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `ClientOptions` |

##### Returns

[`Awaitable`](../#awaitable)<`void`\>

#### Defined in

[projects/framework/src/lib/plugins/Plugin.ts:12](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/Plugin.ts#L12)

___

### [preGenericsInitialization]

▪ `Static` `Optional` **[preGenericsInitialization]**: (`options`: `ClientOptions`) => `void`

#### Type declaration

▸ (`options`): `void`

##### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `ClientOptions` |

##### Returns

`void`

#### Defined in

[projects/framework/src/lib/plugins/Plugin.ts:8](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/Plugin.ts#L8)

___

### [preInitialization]

▪ `Static` `Optional` **[preInitialization]**: (`options`: `ClientOptions`) => `void`

#### Type declaration

▸ (`options`): `void`

##### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `ClientOptions` |

##### Returns

`void`

#### Defined in

[projects/framework/src/lib/plugins/Plugin.ts:9](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/Plugin.ts#L9)

___

### [preLogin]

▪ `Static` `Optional` **[preLogin]**: (`options`: `ClientOptions`) => [`Awaitable`](../#awaitable)<`void`\>

#### Type declaration

▸ (`options`): [`Awaitable`](../#awaitable)<`void`\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `ClientOptions` |

##### Returns

[`Awaitable`](../#awaitable)<`void`\>

#### Defined in

[projects/framework/src/lib/plugins/Plugin.ts:11](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/Plugin.ts#L11)

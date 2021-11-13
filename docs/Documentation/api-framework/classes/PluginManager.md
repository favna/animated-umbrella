---
id: "PluginManager"
title: "Class: PluginManager"
sidebar_label: "PluginManager"
sidebar_position: 0
custom_edit_url: null
---

## Constructors

### constructor

• **new PluginManager**()

## Properties

### registry

• `Readonly` **registry**: [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)<[`SapphirePluginHookEntry`](../interfaces/SapphirePluginHookEntry)<[`SapphirePluginAsyncHook`](../interfaces/SapphirePluginAsyncHook) \| [`SapphirePluginHook`](../interfaces/SapphirePluginHook)\>\>

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:25](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L25)

## Methods

### registerHook

▸ **registerHook**(`hook`, `type`, `name?`): [`PluginManager`](PluginManager)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hook` | [`SapphirePluginHook`](../interfaces/SapphirePluginHook) |
| `type` | [`SyncPluginHooks`](../#syncpluginhooks) |
| `name?` | `string` |

#### Returns

[`PluginManager`](PluginManager)

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:27](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L27)

▸ **registerHook**(`hook`, `type`, `name?`): [`PluginManager`](PluginManager)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hook` | [`SapphirePluginAsyncHook`](../interfaces/SapphirePluginAsyncHook) |
| `type` | [`AsyncPluginHooks`](../#asyncpluginhooks) |
| `name?` | `string` |

#### Returns

[`PluginManager`](PluginManager)

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:28](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L28)

___

### registerPostInitializationHook

▸ **registerPostInitializationHook**(`hook`, `name?`): [`PluginManager`](PluginManager)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hook` | [`SapphirePluginHook`](../interfaces/SapphirePluginHook) |
| `name?` | `string` |

#### Returns

[`PluginManager`](PluginManager)

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:43](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L43)

___

### registerPostLoginHook

▸ **registerPostLoginHook**(`hook`, `name?`): [`PluginManager`](PluginManager)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hook` | [`SapphirePluginAsyncHook`](../interfaces/SapphirePluginAsyncHook) |
| `name?` | `string` |

#### Returns

[`PluginManager`](PluginManager)

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:51](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L51)

___

### registerPreGenericsInitializationHook

▸ **registerPreGenericsInitializationHook**(`hook`, `name?`): [`PluginManager`](PluginManager)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hook` | [`SapphirePluginHook`](../interfaces/SapphirePluginHook) |
| `name?` | `string` |

#### Returns

[`PluginManager`](PluginManager)

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:35](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L35)

___

### registerPreInitializationHook

▸ **registerPreInitializationHook**(`hook`, `name?`): [`PluginManager`](PluginManager)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hook` | [`SapphirePluginHook`](../interfaces/SapphirePluginHook) |
| `name?` | `string` |

#### Returns

[`PluginManager`](PluginManager)

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:39](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L39)

___

### registerPreLoginHook

▸ **registerPreLoginHook**(`hook`, `name?`): [`PluginManager`](PluginManager)

#### Parameters

| Name | Type |
| :------ | :------ |
| `hook` | [`SapphirePluginAsyncHook`](../interfaces/SapphirePluginAsyncHook) |
| `name?` | `string` |

#### Returns

[`PluginManager`](PluginManager)

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:47](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L47)

___

### use

▸ **use**(`plugin`): [`PluginManager`](PluginManager)

#### Parameters

| Name | Type |
| :------ | :------ |
| `plugin` | typeof [`Plugin`](Plugin) |

#### Returns

[`PluginManager`](PluginManager)

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:55](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L55)

___

### values

▸ **values**(): [`Generator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator)<[`SapphirePluginHookEntry`](../interfaces/SapphirePluginHookEntry)<[`SapphirePluginAsyncHook`](../interfaces/SapphirePluginAsyncHook) \| [`SapphirePluginHook`](../interfaces/SapphirePluginHook)\>, `void`, `unknown`\>

#### Returns

[`Generator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator)<[`SapphirePluginHookEntry`](../interfaces/SapphirePluginHookEntry)<[`SapphirePluginAsyncHook`](../interfaces/SapphirePluginAsyncHook) \| [`SapphirePluginHook`](../interfaces/SapphirePluginHook)\>, `void`, `unknown`\>

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:71](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L71)

▸ **values**(`hook`): [`Generator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator)<[`SapphirePluginHookEntry`](../interfaces/SapphirePluginHookEntry)<[`SapphirePluginHook`](../interfaces/SapphirePluginHook)\>, `void`, `unknown`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `hook` | [`SyncPluginHooks`](../#syncpluginhooks) |

#### Returns

[`Generator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator)<[`SapphirePluginHookEntry`](../interfaces/SapphirePluginHookEntry)<[`SapphirePluginHook`](../interfaces/SapphirePluginHook)\>, `void`, `unknown`\>

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:72](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L72)

▸ **values**(`hook`): [`Generator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator)<[`SapphirePluginHookEntry`](../interfaces/SapphirePluginHookEntry)<[`SapphirePluginAsyncHook`](../interfaces/SapphirePluginAsyncHook)\>, `void`, `unknown`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `hook` | [`AsyncPluginHooks`](../#asyncpluginhooks) |

#### Returns

[`Generator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator)<[`SapphirePluginHookEntry`](../interfaces/SapphirePluginHookEntry)<[`SapphirePluginAsyncHook`](../interfaces/SapphirePluginAsyncHook)\>, `void`, `unknown`\>

#### Defined in

[projects/framework/src/lib/plugins/PluginManager.ts:73](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/plugins/PluginManager.ts#L73)

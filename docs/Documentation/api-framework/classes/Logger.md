---
id: "Logger"
title: "Class: Logger"
sidebar_label: "Logger"
sidebar_position: 0
custom_edit_url: null
---

## Implements

- [`ILogger`](../interfaces/ILogger)

## Constructors

### constructor

• **new Logger**(`level`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `level` | [`LogLevel`](../enums/LogLevel) |

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:6](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L6)

## Properties

### level

• **level**: [`LogLevel`](../enums/LogLevel)

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:4](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L4)

___

### levels

▪ `Static` `Protected` `Readonly` **levels**: [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)<[`LogLevel`](../enums/LogLevel), [`LogMethods`](../#logmethods)\>

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:44](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L44)

## Methods

### debug

▸ **debug**(...`values`): `void`

Alias of [ILogger.write](../interfaces/ILogger#write) with [LogLevel.Debug](../enums/LogLevel#debug) as level.

#### Parameters

| Name | Type |
| :------ | :------ |
| `...values` | readonly `unknown`[] |

#### Returns

`void`

#### Implementation of

[ILogger](../interfaces/ILogger).[debug](../interfaces/ILogger#debug)

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:18](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L18)

___

### error

▸ **error**(...`values`): `void`

Alias of [ILogger.write](../interfaces/ILogger#write) with [LogLevel.Error](../enums/LogLevel#error) as level.

#### Parameters

| Name | Type |
| :------ | :------ |
| `...values` | readonly `unknown`[] |

#### Returns

`void`

#### Implementation of

[ILogger](../interfaces/ILogger).[error](../interfaces/ILogger#error)

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:30](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L30)

___

### fatal

▸ **fatal**(...`values`): `void`

Alias of [ILogger.write](../interfaces/ILogger#write) with [LogLevel.Fatal](../enums/LogLevel#fatal) as level.

#### Parameters

| Name | Type |
| :------ | :------ |
| `...values` | readonly `unknown`[] |

#### Returns

`void`

#### Implementation of

[ILogger](../interfaces/ILogger).[fatal](../interfaces/ILogger#fatal)

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:34](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L34)

___

### has

▸ **has**(`level`): `boolean`

Checks whether a level is supported.

#### Parameters

| Name | Type |
| :------ | :------ |
| `level` | [`LogLevel`](../enums/LogLevel) |

#### Returns

`boolean`

#### Implementation of

[ILogger](../interfaces/ILogger).[has](../interfaces/ILogger#has)

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:10](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L10)

___

### info

▸ **info**(...`values`): `void`

Alias of [ILogger.write](../interfaces/ILogger#write) with [LogLevel.Info](../enums/LogLevel#info) as level.

#### Parameters

| Name | Type |
| :------ | :------ |
| `...values` | readonly `unknown`[] |

#### Returns

`void`

#### Implementation of

[ILogger](../interfaces/ILogger).[info](../interfaces/ILogger#info)

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:22](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L22)

___

### trace

▸ **trace**(...`values`): `void`

Alias of [ILogger.write](../interfaces/ILogger#write) with [LogLevel.Trace](../enums/LogLevel#trace) as level.

#### Parameters

| Name | Type |
| :------ | :------ |
| `...values` | readonly `unknown`[] |

#### Returns

`void`

#### Implementation of

[ILogger](../interfaces/ILogger).[trace](../interfaces/ILogger#trace)

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:14](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L14)

___

### warn

▸ **warn**(...`values`): `void`

Alias of [ILogger.write](../interfaces/ILogger#write) with [LogLevel.Warn](../enums/LogLevel#warn) as level.

#### Parameters

| Name | Type |
| :------ | :------ |
| `...values` | readonly `unknown`[] |

#### Returns

`void`

#### Implementation of

[ILogger](../interfaces/ILogger).[warn](../interfaces/ILogger#warn)

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:26](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L26)

___

### write

▸ **write**(`level`, ...`values`): `void`

Writes the log message given a level and the value(s).

#### Parameters

| Name | Type |
| :------ | :------ |
| `level` | [`LogLevel`](../enums/LogLevel) |
| `...values` | readonly `unknown`[] |

#### Returns

`void`

#### Implementation of

[ILogger](../interfaces/ILogger).[write](../interfaces/ILogger#write)

#### Defined in

[projects/framework/src/lib/utils/logger/Logger.ts:38](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/Logger.ts#L38)

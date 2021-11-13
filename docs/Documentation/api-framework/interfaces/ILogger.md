---
id: "ILogger"
title: "Interface: ILogger"
sidebar_label: "ILogger"
sidebar_position: 0
custom_edit_url: null
---

## Implemented by

- [`Logger`](../classes/Logger)

## Methods

### debug

▸ **debug**(...`values`): `void`

Alias of [ILogger.write](ILogger#write) with [LogLevel.Debug](../enums/LogLevel#debug) as level.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...values` | readonly `unknown`[] | The values to log. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/utils/logger/ILogger.ts:58](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/ILogger.ts#L58)

___

### error

▸ **error**(...`values`): `void`

Alias of [ILogger.write](ILogger#write) with [LogLevel.Error](../enums/LogLevel#error) as level.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...values` | readonly `unknown`[] | The values to log. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/utils/logger/ILogger.ts:76](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/ILogger.ts#L76)

___

### fatal

▸ **fatal**(...`values`): `void`

Alias of [ILogger.write](ILogger#write) with [LogLevel.Fatal](../enums/LogLevel#fatal) as level.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...values` | readonly `unknown`[] | The values to log. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/utils/logger/ILogger.ts:82](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/ILogger.ts#L82)

___

### has

▸ **has**(`level`): `boolean`

Checks whether a level is supported.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `level` | [`LogLevel`](../enums/LogLevel) | The level to check. |

#### Returns

`boolean`

#### Defined in

[projects/framework/src/lib/utils/logger/ILogger.ts:46](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/ILogger.ts#L46)

___

### info

▸ **info**(...`values`): `void`

Alias of [ILogger.write](ILogger#write) with [LogLevel.Info](../enums/LogLevel#info) as level.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...values` | readonly `unknown`[] | The values to log. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/utils/logger/ILogger.ts:64](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/ILogger.ts#L64)

___

### trace

▸ **trace**(...`values`): `void`

Alias of [ILogger.write](ILogger#write) with [LogLevel.Trace](../enums/LogLevel#trace) as level.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...values` | readonly `unknown`[] | The values to log. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/utils/logger/ILogger.ts:52](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/ILogger.ts#L52)

___

### warn

▸ **warn**(...`values`): `void`

Alias of [ILogger.write](ILogger#write) with [LogLevel.Warn](../enums/LogLevel#warn) as level.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...values` | readonly `unknown`[] | The values to log. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/utils/logger/ILogger.ts:70](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/ILogger.ts#L70)

___

### write

▸ **write**(`level`, ...`values`): `void`

Writes the log message given a level and the value(s).

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `level` | [`LogLevel`](../enums/LogLevel) | The log level. |
| `...values` | readonly `unknown`[] | The values to log. |

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/utils/logger/ILogger.ts:89](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/utils/logger/ILogger.ts#L89)

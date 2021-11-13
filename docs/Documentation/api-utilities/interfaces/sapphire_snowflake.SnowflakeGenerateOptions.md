---
id: "sapphire_snowflake.SnowflakeGenerateOptions"
title: "Interface: SnowflakeGenerateOptions"
sidebar_label: "SnowflakeGenerateOptions"
custom_edit_url: null
---

[@sapphire/snowflake](../modules/sapphire_snowflake).SnowflakeGenerateOptions

Options for Snowflake#generate

## Properties

### increment

• `Optional` **increment**: `bigint`

The increment to use

**`default`** 0n

**`remark`** keep in mind that this bigint is auto-incremented between generate calls

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:107](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L107)

___

### processID

• `Optional` **processID**: `bigint`

The process ID to use

**`default`** 1n

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:119](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L119)

___

### timestamp

• `Optional` **timestamp**: `number` \| `bigint` \| `Date`

Timestamp or date of the snowflake to generate

**`default`** Date.now()

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:100](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L100)

___

### workerID

• `Optional` **workerID**: `bigint`

The worker ID to use

**`default`** 1n

#### Defined in

[projects/utilities/packages/snowflake/src/lib/Snowflake.ts:113](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/snowflake/src/lib/Snowflake.ts#L113)

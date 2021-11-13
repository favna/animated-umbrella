---
id: "sapphire_fetch.FetchResultTypes"
title: "Enumeration: FetchResultTypes"
sidebar_label: "FetchResultTypes"
custom_edit_url: null
---

[@sapphire/fetch](../modules/sapphire_fetch).FetchResultTypes

The supported return types for the `fetch` method

## Enumeration members

### Blob

• **Blob** = `"blob"`

Returns only the body, as a [`Blob`](https://developer.mozilla.org/en-US/docs/Web/API/Blob).

**`remark`** For NodeJS environment other `FetchResultTypes` are recommended, but you can use a Blob if you want to.

#### Defined in

[projects/utilities/packages/fetch/src/lib/types.ts:22](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/types.ts#L22)

___

### Buffer

• **Buffer** = `"buffer"`

Returns only the body, as a [Buffer](https://nodejs.org/api/buffer.html).

**`remark`** Does not work in a Browser environment. For browsers use [FetchResultTypes.Blob](sapphire_fetch.FetchResultTypes#blob) instead.
If you use this type in a Browsers environment a {@link ReferenceError `ReferenceError: Buffer is not defined`} will be thrown!

#### Defined in

[projects/utilities/packages/fetch/src/lib/types.ts:17](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/types.ts#L17)

___

### JSON

• **JSON** = `"json"`

Returns only the body, as JSON. Similar to [`Body.json()`](https://developer.mozilla.org/en-US/docs/Web/API/Body/json).

You should provide your own type cast (either through the generic return type, or with `as <type>`) to the response to define
the JSON structure, otherwise the result will be `unknown`.

#### Defined in

[projects/utilities/packages/fetch/src/lib/types.ts:11](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/types.ts#L11)

___

### Result

• **Result** = `"result"`

Returns the entire response and doesn't parse the `body` in any way.

#### Defined in

[projects/utilities/packages/fetch/src/lib/types.ts:30](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/types.ts#L30)

___

### Text

• **Text** = `"text"`

Returns only the body, as plain text. Similar to [`Body.text()`](https://developer.mozilla.org/en-US/docs/Web/API/Body/text).

#### Defined in

[projects/utilities/packages/fetch/src/lib/types.ts:26](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/types.ts#L26)

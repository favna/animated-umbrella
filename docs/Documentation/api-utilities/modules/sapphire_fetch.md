---
id: "sapphire_fetch"
title: "Module: @sapphire/fetch"
sidebar_label: "@sapphire/fetch"
sidebar_position: 0
custom_edit_url: null
---

## Enumerations

- [FetchMethods](../enums/sapphire_fetch.FetchMethods)
- [FetchResultTypes](../enums/sapphire_fetch.FetchResultTypes)

## Classes

- [QueryError](../classes/sapphire_fetch.QueryError)

## Functions

### fetch

▸ **fetch**<`R`\>(`url`, `type?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`R`\>

Performs an HTTP(S) fetch

#### Type parameters

| Name |
| :------ |
| `R` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `url` | `string` \| `URL` | The URL to send the request to. Can be either a `string` or an `URL` object. `url` should be an absolute url, such as `https://example.com/`. A path-relative URL (`/file/under/root`) or protocol-relative URL (`//can-be-http-or-https.com/`) will result in a rejected `Promise`. |
| `type?` | [`JSON`](../enums/sapphire_fetch.FetchResultTypes#json) | Only needs to be provided if the second parameter are [Request options](https://developer.mozilla.org/en-US/docs/Web/API/Request) ({@link RequestInit} for TypeScript). One of the [FetchResultTypes](../enums/sapphire_fetch.FetchResultTypes) that will determine how the result is returned. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`R`\>

The return type is determined by the provided `type`.
- When using `FetchResultTypes.JSON` then the return type is `unknown` by default. The type should be specified by filling in the generic type of the function, or casting the result.
- When using `FetchResultTypes.Buffer` the return type will be [`Buffer`](https://nodejs.org/api/buffer.html).
- When using `FetchResultTypes.Blob` the return type will be a [`Blob`](https://developer.mozilla.org/en-US/docs/Web/API/Blob).
- When using `FetchResultTypes.Text` the return type will be a `string`
- When using `FetchResultTypes.Result` the return type will be a [`Response`](https://developer.mozilla.org/en-US/docs/Web/API/Response) ({@link Response} in typescript)

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:21](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L21)

▸ **fetch**<`R`\>(`url`, `options`, `type?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`R`\>

#### Type parameters

| Name |
| :------ |
| `R` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` \| `URL` |
| `options` | `RequestInit` |
| `type?` | [`JSON`](../enums/sapphire_fetch.FetchResultTypes#json) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`R`\>

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:22](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L22)

▸ **fetch**(`url`, `type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Buffer`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` \| `URL` |
| `type` | [`Buffer`](../enums/sapphire_fetch.FetchResultTypes#buffer) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Buffer`\>

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:23](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L23)

▸ **fetch**(`url`, `options`, `type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Buffer`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` \| `URL` |
| `options` | `RequestInit` |
| `type` | [`Buffer`](../enums/sapphire_fetch.FetchResultTypes#buffer) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Buffer`\>

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:24](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L24)

▸ **fetch**(`url`, `type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Blob`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` \| `URL` |
| `type` | [`Blob`](../enums/sapphire_fetch.FetchResultTypes#blob) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Blob`\>

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:25](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L25)

▸ **fetch**(`url`, `options`, `type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Blob`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` \| `URL` |
| `options` | `RequestInit` |
| `type` | [`Blob`](../enums/sapphire_fetch.FetchResultTypes#blob) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Blob`\>

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:26](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L26)

▸ **fetch**(`url`, `type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`string`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` \| `URL` |
| `type` | [`Text`](../enums/sapphire_fetch.FetchResultTypes#text) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`string`\>

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:27](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L27)

▸ **fetch**(`url`, `options`, `type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`string`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` \| `URL` |
| `options` | `RequestInit` |
| `type` | [`Text`](../enums/sapphire_fetch.FetchResultTypes#text) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`string`\>

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:28](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L28)

▸ **fetch**(`url`, `type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Response`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` \| `URL` |
| `type` | [`Result`](../enums/sapphire_fetch.FetchResultTypes#result) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Response`\>

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:29](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L29)

▸ **fetch**(`url`, `options`, `type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Response`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` \| `URL` |
| `options` | `RequestInit` |
| `type` | [`Result`](../enums/sapphire_fetch.FetchResultTypes#result) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Response`\>

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:30](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L30)

▸ **fetch**<`R`\>(`url`, `options`, `type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Response` \| `Blob` \| `Buffer` \| `string` \| `R`\>

#### Type parameters

| Name |
| :------ |
| `R` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` \| `URL` |
| `options` | `RequestInit` |
| `type` | [`FetchResultTypes`](../enums/sapphire_fetch.FetchResultTypes) |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`Response` \| `Blob` \| `Buffer` \| `string` \| `R`\>

#### Defined in

[projects/utilities/packages/fetch/src/lib/fetch.ts:31](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/fetch/src/lib/fetch.ts#L31)

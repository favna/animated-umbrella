---
id: "sapphire_embed_jsx.EmbedJsx"
title: "Namespace: EmbedJsx"
sidebar_label: "EmbedJsx"
custom_edit_url: null
---

[@sapphire/embed-jsx](../modules/sapphire_embed_jsx).EmbedJsx

The namespace to import for embed-jsx

**`example`**
```typescriptreact
import { EmbedJsx } from '@sapphire/embed-jsx';

const embed = (
  <embed color="RED">
	   <title>New Embed</title>
	   <description>Hello!</description>
  </embed>
)
```

## Functions

### make

▸ **make**(`type`, ...`data`): `EmbedData` \| `MessageEmbed`

The behind the scenes function that TS uses to turn JSX into proper JS

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | ``"embed"`` \| ``"title"`` \| ``"field"`` \| ``"timestamp"`` \| ``"footer"`` \| ``"description"`` \| ``"image"`` \| ``"thumbnail"`` \| ``"author"`` | The embed type being created |
| `...data` | `EmbedInformation` \| `EmbedInitialInformation` | The data emitted along with |

#### Returns

`EmbedData` \| `MessageEmbed`

The embed defined with jsx

#### Defined in

[projects/utilities/packages/embed-jsx/src/lib/EmbedJsx.ts:82](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/embed-jsx/src/lib/EmbedJsx.ts#L82)

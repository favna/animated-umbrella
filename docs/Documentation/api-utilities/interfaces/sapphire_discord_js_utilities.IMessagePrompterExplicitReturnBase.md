---
id: "sapphire_discord_js_utilities.IMessagePrompterExplicitReturnBase"
title: "Interface: IMessagePrompterExplicitReturnBase"
sidebar_label: "IMessagePrompterExplicitReturnBase"
custom_edit_url: null
---

[@sapphire/discord.js-utilities](../modules/sapphire_discord_js_utilities).IMessagePrompterExplicitReturnBase

## Hierarchy

- **`IMessagePrompterExplicitReturnBase`**

  ↳ [`IMessagePrompterExplicitConfirmReturn`](sapphire_discord_js_utilities.IMessagePrompterExplicitConfirmReturn)

  ↳ [`IMessagePrompterExplicitNumberReturn`](sapphire_discord_js_utilities.IMessagePrompterExplicitNumberReturn)

  ↳ [`IMessagePrompterExplicitMessageReturn`](sapphire_discord_js_utilities.IMessagePrompterExplicitMessageReturn)

## Properties

### appliedMessage

• **appliedMessage**: [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/ExplicitReturnTypes.ts:9](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/ExplicitReturnTypes.ts#L9)

___

### emoji

• `Optional` **emoji**: [`GuildEmoji`](https://discord.js.org/#/docs/main/stable/class/GuildEmoji) \| [`ReactionEmoji`](https://discord.js.org/#/docs/main/stable/class/ReactionEmoji)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/ExplicitReturnTypes.ts:6](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/ExplicitReturnTypes.ts#L6)

___

### message

• **message**: `string` \| `MessageOptions` \| [`MessagePayload`](https://discord.js.org/#/docs/main/stable/class/MessagePayload)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/ExplicitReturnTypes.ts:10](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/ExplicitReturnTypes.ts#L10)

___

### reaction

• `Optional` **reaction**: `EmojiIdentifierResolvable`

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/ExplicitReturnTypes.ts:7](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/ExplicitReturnTypes.ts#L7)

___

### strategy

• **strategy**: [`MessagePrompterBaseStrategy`](../classes/sapphire_discord_js_utilities.MessagePrompterBaseStrategy)

#### Defined in

[projects/utilities/packages/discord.js-utilities/src/lib/MessagePrompter/ExplicitReturnTypes.ts:8](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/discord.js-utilities/src/lib/MessagePrompter/ExplicitReturnTypes.ts#L8)

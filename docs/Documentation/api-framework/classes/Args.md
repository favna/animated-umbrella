---
id: "Args"
title: "Class: Args"
sidebar_label: "Args"
sidebar_position: 0
custom_edit_url: null
---

The argument parser to be used in [Command](Command).

## Constructors

### constructor

• **new Args**(`message`, `command`, `parser`, `context`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> |
| `command` | [`Command`](Command)<[`Args`](Args), [`CommandOptions`](../interfaces/CommandOptions)\> |
| `parser` | `Args` |
| `context` | [`CommandContext`](../interfaces/CommandContext) |

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:57](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L57)

## Properties

### command

• `Readonly` **command**: [`Command`](Command)<[`Args`](Args), [`CommandOptions`](../interfaces/CommandOptions)\>

The command that is being run.

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:38](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L38)

___

### commandContext

• `Readonly` **commandContext**: [`CommandContext`](../interfaces/CommandContext)

The context of the command being run.

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:43](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L43)

___

### message

• `Readonly` **message**: [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\>

The original message that triggered the command.

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:33](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L33)

___

### parser

• `Protected` `Readonly` **parser**: `Args`

The internal Lexure parser.

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:48](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L48)

___

### states

• `Private` `Readonly` **states**: `ArgsState`[] = `[]`

The states stored in the args.

**`see`** Args#save

**`see`** Args#restore

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:55](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L55)

## Accessors

### finished

• `get` **finished**(): `boolean`

Whether all arguments have been consumed.

#### Returns

`boolean`

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:627](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L627)

## Methods

### getFlags

▸ **getFlags**(...`keys`): `boolean`

Checks if one or more flag were given.

**`example`**
```typescript
// Suppose args are from '--f --g'.
console.log(args.getFlags('f'));
// >>> true

console.log(args.getFlags('g', 'h'));
// >>> true

console.log(args.getFlags('h'));
// >>> false
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...keys` | readonly `string`[] | The name(s) of the flag. |

#### Returns

`boolean`

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:564](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L564)

___

### getOption

▸ **getOption**(...`keys`): ``null`` \| `string`

Gets the last value of one or more options.

**`example`**
```typescript
// Suppose args are from '--a=1 --b=2 --c=3'.
console.log(args.getOption('a'));
// >>> '1'

console.log(args.getOption('b', 'c'));
// >>> '2'

console.log(args.getOption('d'));
// >>> null
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...keys` | readonly `string`[] | The name(s) of the option. |

#### Returns

``null`` \| `string`

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:584](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L584)

___

### getOptions

▸ **getOptions**(...`keys`): ``null`` \| `string`[]

Gets all the values of one or more option.

**`example`**
```typescript
// Suppose args are from '--a=1 --a=1 --b=2 --c=3'.
console.log(args.getOptions('a'));
// >>> ['1', '1']

console.log(args.getOptions('b', 'c'));
// >>> ['2', '3']

console.log(args.getOptions('d'));
// >>> null
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...keys` | readonly `string`[] | The name(s) of the option. |

#### Returns

``null`` \| `string`[]

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:604](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L604)

___

### missingArguments

▸ `Protected` **missingArguments**(): [`Err`](../#err)<[`UserError`](UserError)\>

#### Returns

[`Err`](../#err)<[`UserError`](UserError)\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:649](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L649)

___

### next

▸ **next**(): `string`

Similar to [Args.nextMaybe](Args#nextmaybe) but returns the value on success, null otherwise.

**`example`**
```typescript
// !numbers 1 2 3

console.log(args.next());
// -> '1'
```

#### Returns

`string`

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:525](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L525)

▸ **next**<`T`\>(`cb`): `T`

Similar to [Args.nextMaybe](Args#nextmaybe) but returns the value on success, null otherwise.

**`example`**
```typescript
// !numbers 1 2 3
const parse = (x: string) => {
  const n = Number(x);
  return Number.isNaN(n) ? none() : some(n);
};

console.log(args.nextMaybe(parse));
// -> 1
```

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | Output type of the [callback](../interfaces/ArgsNextCallback). |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `cb` | [`ArgsNextCallback`](../interfaces/ArgsNextCallback)<`T`\> | Gives an option of either the resulting value, or nothing if failed. |

#### Returns

`T`

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:542](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L542)

___

### nextMaybe

▸ **nextMaybe**(): [`Maybe`](../#maybe)<`string`\>

Retrieves the next raw argument from the parser.

**`example`**
```typescript
// !numbers 1 2 3

console.log(args.nextMaybe());
// -> { exists: true, value: '1' }
```

#### Returns

[`Maybe`](../#maybe)<`string`\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:492](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L492)

▸ **nextMaybe**<`T`\>(`cb`): [`Maybe`](../#maybe)<`T`\>

Retrieves the value of the next unused ordered token, but only if it could be transformed.
That token will now be consider used if the transformation succeeds.

**`example`**
```typescript
// !numbers 1 2 3
const parse = (x: string) => {
  const n = Number(x);
  return Number.isNaN(n) ? none() : some(n);
};

console.log(args.nextMaybe(parse));
// -> { exists: true, value: 1 }
```

#### Type parameters

| Name | Description |
| :------ | :------ |
| `T` | Output type of the [callback](../interfaces/ArgsNextCallback). |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `cb` | [`ArgsNextCallback`](../interfaces/ArgsNextCallback)<`T`\> | Gives an option of either the resulting value, or nothing if failed. |

#### Returns

[`Maybe`](../#maybe)<`T`\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:510](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L510)

___

### peek

▸ **peek**<`T`\>(`type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

Similar to [Args.peekResult](Args#peekresult) but returns the value on success, throwing otherwise.

**`example`**
```typescript
// !bigintsumthensquarefirst 25 50 75
const resolver = Args.make((arg) => {
  try {
    return ok(BigInt(arg));
  } catch {
    return err(new UserError('InvalidBigInt', 'You must specify a valid number for a bigint.'));
  }
});

const peeked = await args.peek(() => args.repeatResult(resolver));
await message.channel.send(`Sum: **${peeked.reduce((x, y) => x + y, 0)}**`); // Sum: 150

const first = await args.pick(resolver);
await message.channel.send(`First bigint squared: ${first**2n}`); // First bigint squared: 625
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | () => [`ArgumentResult`](../#argumentresult)<`T`\> | The function, custom argument, or argument name. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:436](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L436)

▸ **peek**<`T`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

Similar to [Args.peekResult](Args#peekresult) but returns the value on success, throwing otherwise.

**`example`**
```typescript
// !createdat 730159185517477900
const snowflakeResolver = Args.make((arg) =>
	 SnowflakeRegex.test(arg) ? ok(BigInt(arg)) : err(new UserError('InvalidSnowflake', 'You must specify a valid snowflake.'));
);

const snowflake = await args.peek(snowflakeResolver);
const timestamp = Number((snowflake >> 22n) + DiscordSnowflake.Epoch);
const createdAt = new Date(timestamp);

await message.channel.send(
  `The snowflake ${snowflake} was registered on ${createdAt.toUTCString()}.`
); // The snowflake 730159185517477900 was registered on Tue, 07 Jul 2020 20:31:55 GMT.

const id = await args.pick('string');
await message.channel.send(`Your ID, reversed: ${id.split('').reverse().join('')}`); // Your ID, reversed: 009774715581951037
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | [`IArgument`](../interfaces/IArgument)<`T`\> | The function, custom argument, or argument name. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:459](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L459)

▸ **peek**<`K`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`ArgType`](../interfaces/ArgType)[`K`]\>

Similar to [Args.peekResult](Args#peekresult) but returns the value on success, throwing otherwise.

**`example`**
```typescript
// !messagelink https://discord.com/channels/737141877803057244/737142209639350343/791843123898089483
const remoteMessage = await args.peek('message');
await message.channel.send(
  `${remoteMessage.author.tag}: ${remoteMessage.content}`
); // RealShadowNova#7462: Yeah, Sapphire has been a great experience so far, especially being able to help and contribute.

const url = await args.pick('hyperlink');
await message.channel.send(`Hostname: ${url.hostname}`); // Hostname: discord.com
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](../interfaces/ArgType) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | `K` \| () => [`ArgumentResult`](../#argumentresult)<[`ArgType`](../interfaces/ArgType)[`K`]\> | The function, custom argument, or argument name. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`ArgType`](../interfaces/ArgType)[`K`]\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:475](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L475)

___

### peekResult

▸ **peekResult**<`T`\>(`type`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`T`, [`UserError`](UserError)\>\>

Peeks the following parameter(s) without advancing the parser's state.
Passing a function as a parameter allows for returning [Args.pickResult](Args#pickresult), [Args.repeatResult](Args#repeatresult),
or [Args.restResult](Args#restresult); otherwise, passing the custom argument or the argument type with options
will use [Args.pickResult](Args#pickresult) and only peek a single argument.

**`example`**
```typescript
// !reversedandscreamfirst hello world
const resolver = Args.make((arg) => ok(arg.split('').reverse().join('')));

const result = await args.peekResult(() => args.repeatResult(resolver));
if (isOk(result)) await message.channel.send(
  `Reversed ${result.value.length} word(s): ${result.value.join(' ')}`
); // Reversed 2 word(s): olleh dlrow

const firstWord = await args.pickResult('string');
if (isOk(firstWord)) await message.channel.send(firstWord.value.toUpperCase()); // HELLO
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | () => [`ArgumentResult`](../#argumentresult)<`T`\> | The function, custom argument, or argument name. |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`T`, [`UserError`](UserError)\>\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:362](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L362)

▸ **peekResult**<`T`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`T`, [`UserError`](UserError)\>\>

Peeks the following parameter(s) without advancing the parser's state.
Passing a function as a parameter allows for returning [Args.pickResult](Args#pickresult), [Args.repeatResult](Args#repeatresult),
or [Args.restResult](Args#restresult); otherwise, passing the custom argument or the argument type with options
will use [Args.pickResult](Args#pickresult) and only peek a single argument.

**`example`**
```typescript
// !reverseandscreamfirst sapphire community
const resolver = Args.make((arg) => ok(arg.split('').reverse().join('')));

const peekedWord = await args.peekResult(resolver);
if (isOk(peekedWord)) await message.channel.send(peekedWord.value); // erihppas

const firstWord = await args.pickResult('string');
if (isOk(firstWord)) await message.channel.send(firstWord.value.toUpperCase()); // SAPPHIRE
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | [`IArgument`](../interfaces/IArgument)<`T`\> | The function, custom argument, or argument name. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`T`, [`UserError`](UserError)\>\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:381](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L381)

▸ **peekResult**<`K`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<[`ArgType`](../interfaces/ArgType)[`K`], [`UserError`](UserError)\>\>

Peeks the following parameter(s) without advancing the parser's state.
Passing a function as a parameter allows for returning [Args.pickResult](Args#pickresult), [Args.repeatResult](Args#repeatresult),
or [Args.restResult](Args#restresult); otherwise, passing the custom argument or the argument type with options
will use [Args.pickResult](Args#pickresult) and only peek a single argument.

**`example`**
```typescript
// !datethenaddtwo 1608867472611
const date = await args.peekResult('date');
if (isOk(date)) await message.channel.send(
  `Your date (in UTC): ${date.value.toUTCString()}`
); // Your date (in UTC): Fri, 25 Dec 2020 03:37:52 GMT

const result = await args.pickResult('number', { maximum: Number.MAX_SAFE_INTEGER - 2 });
if (isOk(result)) await message.channel.send(`Your number plus two: ${result.value + 2}`); // Your number plus two: 1608867472613
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](../interfaces/ArgType) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | `K` \| () => [`ArgumentResult`](../#argumentresult)<[`ArgType`](../interfaces/ArgType)[`K`]\> | The function, custom argument, or argument name. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<[`ArgType`](../interfaces/ArgType)[`K`], [`UserError`](UserError)\>\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:400](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L400)

___

### pick

▸ **pick**<`T`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

Similar to [Args.pickResult](Args#pickresult) but returns the value on success, throwing otherwise.

**`example`**
```typescript
// !square 5
const resolver = Args.make((arg) => {
  const parsed = Number(argument);
  if (Number.isNaN(parsed)) return err(new UserError('ArgumentNumberNaN', 'You must write a valid number.'));
  return ok(parsed);
});
const a = await args.pick(resolver);

await message.channel.send(`The result is: ${a ** 2}!`);
// Sends "The result is: 25"
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | [`IArgument`](../interfaces/IArgument)<`T`\> | The type of the argument. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:148](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L148)

▸ **pick**<`K`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`ArgType`](../interfaces/ArgType)[`K`]\>

Similar to [Args.pickResult](Args#pickresult) but returns the value on success, throwing otherwise.

**`example`**
```typescript
// !add 1 2
const a = await args.pick('integer');
const b = await args.pick('integer');
await message.channel.send(`The result is: ${a + b}!`);
// Sends "The result is: 3"
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](../interfaces/ArgType) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | `K` | The type of the argument. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`ArgType`](../interfaces/ArgType)[`K`]\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:161](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L161)

___

### pickResult

▸ **pickResult**<`T`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`T`, [`UserError`](UserError)\>\>

Retrieves the next parameter and parses it. Advances index on success.

**`example`**
```typescript
// !square 5
const resolver = Args.make((arg) => {
  const parsed = Number(argument);
  if (Number.isNaN(parsed)) return err(new UserError('ArgumentNumberNaN', 'You must write a valid number.'));
  return ok(parsed);
});
const a = await args.pickResult(resolver);
if (!a.success) throw new UserError('ArgumentNumberNaN', 'You must write a valid number.');

await message.channel.send(`The result is: ${a.value ** 2}!`);
// Sends "The result is: 25"
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | [`IArgument`](../interfaces/IArgument)<`T`\> | The type of the argument. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`T`, [`UserError`](UserError)\>\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:94](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L94)

▸ **pickResult**<`K`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<[`ArgType`](../interfaces/ArgType)[`K`], [`UserError`](UserError)\>\>

Retrieves the next parameter and parses it. Advances index on success.

**`example`**
```typescript
// !add 1 2
const a = await args.pickResult('integer');
if (!a.success) throw new UserError('AddArgumentError', 'You must write two numbers, but the first one did not match.');

const b = await args.pickResult('integer');
if (!b.success) throw new UserError('AddArgumentError', 'You must write two numbers, but the second one did not match.');

await message.channel.send(`The result is: ${a.value + b.value}!`);
// Sends "The result is: 3"
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](../interfaces/ArgType) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | `K` | The type of the argument. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<[`ArgType`](../interfaces/ArgType)[`K`], [`UserError`](UserError)\>\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:111](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L111)

___

### repeat

▸ **repeat**<`T`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`[]\>

Similar to [Args.repeatResult](Args#repeatresult) but returns the value on success, throwing otherwise.

**`example`**
```typescript
// !reverse-each 2 Hello World!
const resolver = Args.make((arg) => ok(arg.split('').reverse()));
const result = await args.repeat(resolver, { times: 5 });
await message.channel.send(`You have written ${result.length} word(s): ${result.join(' ')}`);
// Sends "You have written 2 word(s): Hello World!"
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | [`IArgument`](../interfaces/IArgument)<`T`\> | The type of the argument. |
| `options?` | [`RepeatArgOptions`](../interfaces/RepeatArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`[]\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:323](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L323)

▸ **repeat**<`K`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`ArgType`](../interfaces/ArgType)[`K`][]\>

Similar to [Args.repeatResult](Args#repeatresult) but returns the value on success, throwing otherwise.

**`example`**
```typescript
// !add 2 Hello World!
const words = await args.repeat('string', { times: 5 });
await message.channel.send(`You have written ${words.length} word(s): ${words.join(' ')}`);
// Sends "You have written 2 word(s): Hello World!"
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](../interfaces/ArgType) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | `K` | The type of the argument. |
| `options?` | [`RepeatArgOptions`](../interfaces/RepeatArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`ArgType`](../interfaces/ArgType)[`K`][]\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:335](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L335)

___

### repeatResult

▸ **repeatResult**<`T`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`T`[], [`UserError`](UserError)\>\>

Retrieves all the following arguments.

**`example`**
```typescript
// !add 2 Hello World!
const resolver = Args.make((arg) => ok(arg.split('').reverse()));
const result = await args.repeatResult(resolver, { times: 5 });
if (!result.success) throw new UserError('CountArgumentError', 'You must write up to 5 words.');

await message.channel.send(`You have written ${result.value.length} word(s): ${result.value.join(' ')}`);
// Sends "You have written 2 word(s): olleH !dlroW"
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | [`IArgument`](../interfaces/IArgument)<`T`\> | The type of the argument. |
| `options?` | [`RepeatArgOptions`](../interfaces/RepeatArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`T`[], [`UserError`](UserError)\>\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:267](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L267)

▸ **repeatResult**<`K`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<[`ArgType`](../interfaces/ArgType)[`K`][], [`UserError`](UserError)\>\>

Retrieves all the following arguments.

**`example`**
```typescript
// !reverse-each 2 Hello World!
const result = await args.repeatResult('string', { times: 5 });
if (!result.success) throw new UserError('CountArgumentError', 'You must write up to 5 words.');

await message.channel.send(`You have written ${result.value.length} word(s): ${result.value.join(' ')}`);
// Sends "You have written 2 word(s): Hello World!"
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](../interfaces/ArgType) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | `K` | The type of the argument. |
| `options?` | [`RepeatArgOptions`](../interfaces/RepeatArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<[`ArgType`](../interfaces/ArgType)[`K`][], [`UserError`](UserError)\>\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:281](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L281)

___

### resolveArgument

▸ `Private` **resolveArgument**<`T`\>(`arg`): `undefined` \| [`IArgument`](../interfaces/IArgument)<`T`\>

Resolves an argument.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `arg` | keyof [`ArgType`](../interfaces/ArgType) \| [`IArgument`](../interfaces/IArgument)<`T`\> | The argument name or [IArgument](../interfaces/IArgument) instance. |

#### Returns

`undefined` \| [`IArgument`](../interfaces/IArgument)<`T`\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:657](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L657)

___

### rest

▸ **rest**<`T`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

Similar to [Args.restResult](Args#restresult) but returns the value on success, throwing otherwise.

**`example`**
```typescript
// !reverse Hello world!
const resolver = Args.make((arg) => ok(arg.split('').reverse()));
const a = await args.rest(resolver);
await message.channel.send(`The reversed value is... ${a}`);
// Sends "The reversed value is... !dlrow olleH"
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | [`IArgument`](../interfaces/IArgument)<`T`\> | The type of the argument. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<`T`\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:233](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L233)

▸ **rest**<`K`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`ArgType`](../interfaces/ArgType)[`K`]\>

Similar to [Args.restResult](Args#restresult) but returns the value on success, throwing otherwise.

**`example`**
```typescript
// !add 2 Hello World!
const a = await args.pick('integer');
const b = await args.rest('string', { minimum: 1 });
await message.channel.send(`The repeated value is... ${b.repeat(a)}!`);
// Sends "The repeated value is... Hello World!Hello World!"
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](../interfaces/ArgType) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | `K` | The type of the argument. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`ArgType`](../interfaces/ArgType)[`K`]\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:246](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L246)

___

### restResult

▸ **restResult**<`T`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`T`, [`UserError`](UserError)\>\>

Retrieves all the following arguments.

**`example`**
```typescript
// !reverse Hello world!
const resolver = Args.make((arg) => ok(arg.split('').reverse()));
const a = await args.restResult(resolver);
if (!a.success) throw new UserError('AddArgumentError', 'You must write some text.');

await message.channel.send(`The reversed value is... ${a.value}`);
// Sends "The reversed value is... !dlrow olleH"
```

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | [`IArgument`](../interfaces/IArgument)<`T`\> | The type of the argument. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<`T`, [`UserError`](UserError)\>\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:182](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L182)

▸ **restResult**<`K`\>(`type`, `options?`): [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<[`ArgType`](../interfaces/ArgType)[`K`], [`UserError`](UserError)\>\>

Retrieves all the following arguments.

**`example`**
```typescript
// !add 2 Hello World!
const a = await args.pickResult('integer');
if (!a.success) throw new UserError('AddArgumentError', 'You must write a number and a text, but the former did not match.');

const b = await args.restResult('string', { minimum: 1 });
if (!b.success) throw new UserError('AddArgumentError', 'You must write a number and a text, but the latter did not match.');

await message.channel.send(`The repeated value is... ${b.value.repeat(a.value)}!`);
// Sends "The repeated value is... Hello World!Hello World!"
```

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`ArgType`](../interfaces/ArgType) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | `K` | The type of the argument. |
| `options?` | [`ArgOptions`](../interfaces/ArgOptions) | - |

#### Returns

[`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[`Result`](../#result)<[`ArgType`](../interfaces/ArgType)[`K`], [`UserError`](UserError)\>\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:199](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L199)

___

### restore

▸ **restore**(): `void`

Restores the previously saved state from the stack.

**`see`** Args#save

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:620](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L620)

___

### save

▸ **save**(): `void`

Saves the current state into the stack following a FILO strategy (first-in, last-out).

**`see`** Args#restore

#### Returns

`void`

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:612](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L612)

___

### start

▸ **start**(): [`Args`](Args)

Sets the parser to the first token.

#### Returns

[`Args`](Args)

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:67](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L67)

___

### toJSON

▸ **toJSON**(): `Object`

Defines the `JSON.stringify` override.

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `command` | [`Command`](Command)<[`Args`](Args), [`CommandOptions`](../interfaces/CommandOptions)\> |
| `commandContext` | [`CommandContext`](../interfaces/CommandContext) |
| `message` | [`Message`](https://discord.js.org/#/docs/main/stable/class/Message)<`boolean`\> |

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:634](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L634)

___

### unavailableArgument

▸ `Protected` **unavailableArgument**<`T`\>(`type`): [`Err`](../#err)<[`UserError`](UserError)\>

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `type` | `string` \| [`IArgument`](../interfaces/IArgument)<`T`\> |

#### Returns

[`Err`](../#err)<[`UserError`](UserError)\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:638](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L638)

___

### error

▸ `Static` **error**<`T`\>(`options`): [`Err`](../#err)<[`ArgumentError`](ArgumentError)<`T`\>\>

Constructs an [Err](../#err) result containing an [ArgumentError](ArgumentError).

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`Options`](../interfaces/ArgumentError.Options)<`T`\> | The options for the argument error. |

#### Returns

[`Err`](../#err)<[`ArgumentError`](ArgumentError)<`T`\>\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:682](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L682)

___

### make

▸ `Static` **make**<`T`\>(`cb`, `name?`): [`IArgument`](../interfaces/IArgument)<`T`\>

Converts a callback into an usable argument.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `cb` | (`parameter`: `string`, `context`: [`ArgumentContext`](../interfaces/ArgumentContext)<`T`\>) => [`ArgumentResult`](../#argumentresult)<`T`\> | `undefined` | The callback to convert into an [IArgument](../interfaces/IArgument). |
| `name` | `string` | `''` | - |

#### Returns

[`IArgument`](../interfaces/IArgument)<`T`\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:666](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L666)

___

### ok

▸ `Static` **ok**<`T`\>(`value`): [`Ok`](../#ok)<`T`\>

Constructs an [Ok](../#ok) result.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `T` | The value to pass. |

#### Returns

[`Ok`](../#ok)<`T`\>

#### Defined in

[projects/framework/src/lib/parsers/Args.ts:674](https://github.com/sapphiredev/framework/blob/5a4898f6/src/lib/parsers/Args.ts#L674)

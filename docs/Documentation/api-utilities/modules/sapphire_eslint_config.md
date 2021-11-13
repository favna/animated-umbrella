---
id: "sapphire_eslint_config"
title: "Module: @sapphire/eslint-config"
sidebar_label: "@sapphire/eslint-config"
sidebar_position: 0
custom_edit_url: null
---

## References

### default

Renames and re-exports [eslintConfig](sapphire_eslint_config#eslintconfig)

## Variables

### eslintConfig

• **eslintConfig**: `Object`

Default ESLint configuration for Sapphire Communitys

**`example`**
```json
{
  "extends": "@sapphire"
}
```

#### Type declaration

| Name | Type |
| :------ | :------ |
| `env` | `Object` |
| `env.browser` | `boolean` |
| `env.commonjs` | `boolean` |
| `env.es2017` | `boolean` |
| `env.es2020` | `boolean` |
| `env.es6` | `boolean` |
| `env.jest` | `boolean` |
| `env.node` | `boolean` |
| `extends` | `string`[] |
| `parser` | `string` |
| `parserOptions` | `Object` |
| `parserOptions.ecmaVersion` | `number` |
| `parserOptions.extraFileExtensions` | `string`[] |
| `parserOptions.project` | `string` |
| `parserOptions.sourceType` | `string` |
| `parserOptions.warnOnUnsupportedTypeScriptVersion` | `boolean` |
| `root` | `boolean` |
| `rules` | `Object` |
| `rules.@typescript-eslint/adjacent-overload-signatures` | `string` |
| `rules.@typescript-eslint/array-type` | `string` |
| `rules.@typescript-eslint/await-thenable` | `string` |
| `rules.@typescript-eslint/ban-ts-comment` | (`string` \| { `minimumDescriptionLength`: `number` = 3; `ts-check`: `boolean` = true; `ts-expect-error`: `string` = 'allow-with-description'; `ts-ignore`: `string` = 'allow-with-description'; `ts-nocheck`: `boolean` = true })[] |
| `rules.@typescript-eslint/class-literal-property-style` | `string` |
| `rules.@typescript-eslint/consistent-type-definitions` | `string` |
| `rules.@typescript-eslint/default-param-last` | `string` |
| `rules.@typescript-eslint/dot-notation` | (`string` \| { `allowKeywords`: `boolean` = true; `allowPattern`: `string` = '(^[A-Z])\|(^[a-z]+(\_[a-z]+)+$)'; `allowPrivateClassPropertyAccess`: `boolean` = true })[] |
| `rules.@typescript-eslint/explicit-function-return-type` | `string` |
| `rules.@typescript-eslint/explicit-member-accessibility` | `string` |
| `rules.@typescript-eslint/explicit-module-boundary-types` | `string` |
| `rules.@typescript-eslint/init-declarations` | `string` |
| `rules.@typescript-eslint/member-ordering` | (`string` \| { `default`: `string`[]  })[] |
| `rules.@typescript-eslint/no-base-to-string` | `string` |
| `rules.@typescript-eslint/no-dupe-class-members` | `string` |
| `rules.@typescript-eslint/no-empty-interface` | `string` |
| `rules.@typescript-eslint/no-explicit-any` | `string` |
| `rules.@typescript-eslint/no-extra-non-null-assertion` | `string` |
| `rules.@typescript-eslint/no-extraneous-class` | `string` |
| `rules.@typescript-eslint/no-floating-promises` | `string` |
| `rules.@typescript-eslint/no-for-in-array` | `string` |
| `rules.@typescript-eslint/no-implied-eval` | `string` |
| `rules.@typescript-eslint/no-invalid-this` | `string` |
| `rules.@typescript-eslint/no-invalid-void-type` | `string` |
| `rules.@typescript-eslint/no-misused-new` | `string` |
| `rules.@typescript-eslint/no-namespace` | `string` |
| `rules.@typescript-eslint/no-non-null-asserted-optional-chain` | `string` |
| `rules.@typescript-eslint/no-non-null-assertion` | `string` |
| `rules.@typescript-eslint/no-throw-literal` | `string` |
| `rules.@typescript-eslint/no-unnecessary-boolean-literal-compare` | `string` |
| `rules.@typescript-eslint/no-unnecessary-qualifier` | `string` |
| `rules.@typescript-eslint/no-unsafe-assignment` | `string` |
| `rules.@typescript-eslint/no-unsafe-call` | `string` |
| `rules.@typescript-eslint/no-unsafe-member-access` | `string` |
| `rules.@typescript-eslint/no-unsafe-return` | `string` |
| `rules.@typescript-eslint/no-unused-vars` | `string` |
| `rules.@typescript-eslint/no-use-before-define` | `string` |
| `rules.@typescript-eslint/no-useless-constructor` | `string` |
| `rules.@typescript-eslint/no-var-requires` | `string` |
| `rules.@typescript-eslint/prefer-as-const` | `string` |
| `rules.@typescript-eslint/prefer-for-of` | `string` |
| `rules.@typescript-eslint/prefer-includes` | `string` |
| `rules.@typescript-eslint/prefer-reduce-type-parameter` | `string` |
| `rules.@typescript-eslint/prefer-string-starts-ends-with` | `string` |
| `rules.@typescript-eslint/promise-function-async` | `string` |
| `rules.@typescript-eslint/require-await` | `string` |
| `rules.@typescript-eslint/restrict-plus-operands` | `string` |
| `rules.@typescript-eslint/switch-exhaustiveness-check` | `string` |
| `rules.@typescript-eslint/unbound-method` | `string` |
| `rules.@typescript-eslint/unified-signatures` | `string` |
| `rules.accessor-pairs` | `string` |
| `rules.array-callback-return` | `string` |
| `rules.block-scoped-var` | `string` |
| `rules.callback-return` | `string` |
| `rules.capitalized-comments` | `string` |
| `rules.class-methods-use-this` | `string` |
| `rules.complexity` | `string` |
| `rules.consistent-return` | `string` |
| `rules.consistent-this` | `string`[] |
| `rules.constructor-super` | `string` |
| `rules.default-case` | `string` |
| `rules.dot-notation` | `string` |
| `rules.eqeqeq` | `string`[] |
| `rules.for-direction` | `string` |
| `rules.func-name-matching` | `string`[] |
| `rules.func-names` | `string`[] |
| `rules.func-style` | `string` |
| `rules.global-require` | `string` |
| `rules.guard-for-in` | `string` |
| `rules.handle-callback-err` | `string` |
| `rules.id-blacklist` | `string` |
| `rules.id-length` | `string` |
| `rules.id-match` | `string` |
| `rules.init-declarations` | `string` |
| `rules.line-comment-position` | `string` |
| `rules.lines-between-class-members` | (`string` \| { `exceptAfterSingleLine`: `boolean` = true })[] |
| `rules.max-depth` | `string` |
| `rules.max-lines` | `string` |
| `rules.max-nested-callbacks` | `string` |
| `rules.max-params` | `string` |
| `rules.max-statements` | `string` |
| `rules.max-statements-per-line` | (`string` \| { `max`: `number` = 1 })[] |
| `rules.multiline-comment-style` | `string` |
| `rules.new-cap` | `string` |
| `rules.no-alert` | `string` |
| `rules.no-array-constructor` | `string` |
| `rules.no-await-in-loop` | `string` |
| `rules.no-bitwise` | `string` |
| `rules.no-buffer-constructor` | `string` |
| `rules.no-caller` | `string` |
| `rules.no-case-declarations` | `string` |
| `rules.no-catch-shadow` | `string` |
| `rules.no-class-assign` | `string` |
| `rules.no-compare-neg-zero` | `string` |
| `rules.no-cond-assign` | `string` |
| `rules.no-console` | `string` |
| `rules.no-const-assign` | `string` |
| `rules.no-constant-condition` | `string` |
| `rules.no-control-regex` | `string` |
| `rules.no-debugger` | `string` |
| `rules.no-delete-var` | `string` |
| `rules.no-div-regex` | `string` |
| `rules.no-dupe-args` | `string` |
| `rules.no-dupe-class-members` | `string` |
| `rules.no-dupe-keys` | `string` |
| `rules.no-duplicate-case` | `string` |
| `rules.no-duplicate-imports` | (`string` \| { `includeExports`: `boolean` = false })[] |
| `rules.no-else-return` | `string` |
| `rules.no-empty` | `string` |
| `rules.no-empty-character-class` | `string` |
| `rules.no-empty-function` | `string` |
| `rules.no-empty-pattern` | `string` |
| `rules.no-eq-null` | `string` |
| `rules.no-eval` | `string` |
| `rules.no-ex-assign` | `string` |
| `rules.no-extend-native` | `string` |
| `rules.no-extra-bind` | `string` |
| `rules.no-extra-boolean-cast` | `string` |
| `rules.no-extra-label` | `string` |
| `rules.no-fallthrough` | `string` |
| `rules.no-func-assign` | `string` |
| `rules.no-global-assign` | `string` |
| `rules.no-implicit-coercion` | `string` |
| `rules.no-implicit-globals` | `string` |
| `rules.no-implied-eval` | `string` |
| `rules.no-import-assign` | `string` |
| `rules.no-inline-comments` | `string` |
| `rules.no-inner-declarations` | `string` |
| `rules.no-invalid-regexp` | `string` |
| `rules.no-invalid-this` | `string` |
| `rules.no-irregular-whitespace` | (`string` \| { `skipComments`: `boolean` = true; `skipRegExps`: `boolean` = true; `skipStrings`: `boolean` = true; `skipTemplates`: `boolean` = true })[] |
| `rules.no-iterator` | `string` |
| `rules.no-label-var` | `string` |
| `rules.no-labels` | `string` |
| `rules.no-lone-blocks` | `string` |
| `rules.no-lonely-if` | `string` |
| `rules.no-loop-func` | `string` |
| `rules.no-magic-numbers` | `string` |
| `rules.no-mixed-requires` | `string` |
| `rules.no-multi-assign` | `string` |
| `rules.no-multi-str` | `string` |
| `rules.no-negated-condition` | `string` |
| `rules.no-nested-ternary` | `string` |
| `rules.no-new` | `string` |
| `rules.no-new-func` | `string` |
| `rules.no-new-object` | `string` |
| `rules.no-new-require` | `string` |
| `rules.no-new-symbol` | `string` |
| `rules.no-new-wrappers` | `string` |
| `rules.no-obj-calls` | `string` |
| `rules.no-octal` | `string` |
| `rules.no-octal-escape` | `string` |
| `rules.no-param-reassign` | `string` |
| `rules.no-path-concat` | `string` |
| `rules.no-plusplus` | `string` |
| `rules.no-process-env` | `string` |
| `rules.no-process-exit` | `string` |
| `rules.no-proto` | `string` |
| `rules.no-prototype-builtins` | `string` |
| `rules.no-redeclare` | `string` |
| `rules.no-regex-spaces` | `string` |
| `rules.no-restricted-globals` | `string` |
| `rules.no-restricted-imports` | `string` |
| `rules.no-restricted-modules` | `string` |
| `rules.no-restricted-properties` | `string` |
| `rules.no-restricted-syntax` | `string` |
| `rules.no-return-assign` | `string` |
| `rules.no-return-await` | `string` |
| `rules.no-script-url` | `string` |
| `rules.no-self-assign` | `string` |
| `rules.no-self-compare` | `string` |
| `rules.no-setter-return` | `string` |
| `rules.no-shadow` | `string` |
| `rules.no-shadow-restricted-names` | `string` |
| `rules.no-sparse-arrays` | `string` |
| `rules.no-sync` | `string` |
| `rules.no-template-curly-in-string` | `string` |
| `rules.no-ternary` | `string` |
| `rules.no-this-before-super` | `string` |
| `rules.no-throw-literal` | `string` |
| `rules.no-undef` | `string` |
| `rules.no-undef-init` | `string` |
| `rules.no-undefined` | `string` |
| `rules.no-underscore-dangle` | `string` |
| `rules.no-unmodified-loop-condition` | `string` |
| `rules.no-unneeded-ternary` | `string` |
| `rules.no-unreachable` | `string` |
| `rules.no-unsafe-finally` | `string` |
| `rules.no-unsafe-negation` | `string` |
| `rules.no-unused-expressions` | `string` |
| `rules.no-unused-labels` | `string` |
| `rules.no-unused-vars` | `string` |
| `rules.no-use-before-define` | `string` |
| `rules.no-useless-call` | `string` |
| `rules.no-useless-computed-key` | `string` |
| `rules.no-useless-concat` | `string` |
| `rules.no-useless-constructor` | `string` |
| `rules.no-useless-escape` | `string` |
| `rules.no-useless-rename` | `string` |
| `rules.no-useless-return` | `string` |
| `rules.no-var` | `string` |
| `rules.no-void` | `string` |
| `rules.no-warning-comments` | `string` |
| `rules.no-with` | `string` |
| `rules.object-shorthand` | `string`[] |
| `rules.one-var` | `string`[] |
| `rules.operator-assignment` | `string`[] |
| `rules.padding-line-between-statements` | `string` |
| `rules.prefer-const` | (`string` \| { `destructuring`: `string` = 'all' })[] |
| `rules.prefer-destructuring` | (`string` \| { `AssignmentExpression`: { `array`: `boolean` = true; `object`: `boolean` = false } ; `VariableDeclarator`: { `array`: `boolean` = false; `object`: `boolean` = true }  })[] |
| `rules.prefer-numeric-literals` | `string` |
| `rules.prefer-promise-reject-errors` | `string` |
| `rules.prefer-rest-params` | `string` |
| `rules.prefer-spread` | `string` |
| `rules.prefer-template` | `string` |
| `rules.radix` | `string` |
| `rules.require-await` | `string` |
| `rules.require-jsdoc` | `string` |
| `rules.require-yield` | `string` |
| `rules.sort-imports` | `string` |
| `rules.sort-keys` | `string` |
| `rules.sort-vars` | `string` |
| `rules.spaced-comment` | `string`[] |
| `rules.strict` | `string`[] |
| `rules.symbol-description` | `string` |
| `rules.use-isnan` | `string` |
| `rules.valid-jsdoc` | `string` |
| `rules.valid-typeof` | `string` |
| `rules.vars-on-top` | `string` |
| `rules.yoda` | `string` |

#### Defined in

[projects/utilities/packages/eslint-config/src/index.ts:10](https://github.com/sapphiredev/utilities/blob/8a451b58/packages/eslint-config/src/index.ts#L10)

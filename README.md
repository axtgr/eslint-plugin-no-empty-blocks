# eslint-plugin-no-empty-blocks

An [ESLint](http://eslint.org/) rule for eliminating empty block statements. It is an extended version of the [`no-empty`](http://eslint.org/docs/rules/no-empty) rule that adds an option to allow empty catch blocks.

## Why Use It

ESLint has the built-in `no-empty` rule that is aimed at eliminating empty block statements. It throws a warning at empty catch blocks such as this one:

```javascript
try {
  doSomething();
} catch(e) {}
```

But this technique can be useful for ignoring errors, and this plugin provides an option to allow it.

## Configuration

Add `no-empty-blocks` to the `plugins` section of your `.eslintrc`:

```json
{
  "plugins": [
    "no-empty-blocks"
  ]
}
```

If you don't add anything to the `rules` section, the default config will be used (*prohibit empty blocks except catches*):

```json
{
  "rules": {
    "no-empty-blocks": [2, "allowCatch"]
  }
}
```

Without the `allowCatch` option the rule behaves identically to the built-in `no-empty` rule.

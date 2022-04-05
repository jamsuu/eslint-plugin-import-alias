# @limegrass/eslint-plugin-import-alias

Encourage use of defined aliases in TSConfig/JSConfig through ESLint.

## Why

-   Automatic imports by tsserver resolve to relative paths that can be normalized.
-   It's easier to refactor by finding and replacing an absolute module path
    without worrying about crafting the regex for `../` and `./`

## Requirements

-   Node 14+

## Install

```shell
npm install --save-dev eslint-plugin-import-alias eslint
```

This plugin relies on an alias configuration in `tsconfig.json`, `jsconfig.json`,
or a config with the same schema and a path given as `aliasConfigPath` in its rules
settings. See the [rules documentation][docs-import-alias] for more detail.

## Configuration

The following is the most basic configuration.
Check the [rules documentation][docs-import-alias] for further configuration.

```jsonc
// .eslintrc
{
    "rules": {
        "self/import-alias": "error"
    }
}
```

This configuration is also turned on automatically if you extend `eslint:recommended`.

[docs-import-alias]: (docs/rules/import-alias.md)

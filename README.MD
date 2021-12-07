# Fix All JSON

Simple VSCode extension for fixing almost all annoying JSON (and even JSONC!) problems.

- supports virtual workspaces and web
- small and no dependencies
- simple and fast as it uses prepared diagnostics

<!-- TODO about code fixes -->

## What fixes

All these fixes are configurable and can be disabled in settings:

| Error Message                                   | Action                                               |
| ----------------------------------------------- | ---------------------------------------------------- |
| Expected comma                                  | Insert missing comma                                 |
| Trailing comma                                  | Remove trailing comma                                |
| Comments are not permitted in JSON. (json only) | Remove the whole comment (**disabled by default**)   |
| Property keys must be doublequoted              | Remove quotes (if have `'` or **`**) and doublequote |

> Note: missing commas just placed before the error range. Its assumed you have autoformatter enabled to handle the "right placing"
> In other words, it would run formatter on each save, but you can disable it via setting

Note 2: this extension though doesn't autoquoting, there is [vscode-fix-json](https://github.com/oliversturm/vscode-fix-json) for that.

## Why not Prettier?

[Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) as formatter does great work on fixing trailing semicolons and quotes problems, however this extension is much faster and more aggressive overall.

- Note: you can disable autofixing on save and instead run command whenever you want
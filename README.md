# Xain Torras 26 Theme Pack

Light themes for Cursor/VS Code based on the `xain-torras-26` palette.

## Included themes

- `xain-torras-26`
- `xain-torras-26 High Contrast Light`

## Local test

1. Open this folder in Cursor/VS Code.
2. Press `F5` to run Extension Development Host.
3. Select one of the themes from `Preferences: Color Theme`.

## Publish to Cursor ecosystem (Open VSX)

Cursor installs extensions from Open VSX.

1. Create a publisher namespace on [open-vsx.org](https://open-vsx.org/).
2. Ensure `publisher` in `package.json` matches your Open VSX namespace.
3. Publish:

```bash
npx ovsx publish -p <OPEN_VSX_TOKEN>
```

## Optional: Publish to VS Code Marketplace

```bash
npx @vscode/vsce publish
```

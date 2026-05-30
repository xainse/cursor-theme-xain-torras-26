# XAIN Torras 26 Theme Pack

Light themes for Cursor/VS Code based on the `xain-torras-26` palette.

## Included themes

- `xain-torras-26`
- `xain-torras-26 High Contrast Light`

## Install via Cursor Agent (one-click prompt)

Open Cursor, start a new chat, and paste the prompt below. The agent will install the theme from [Open VSX](https://open-vsx.org/extension/xainse/xain-torras-26-theme) and activate it for you.

```text
Install the "Xain Torras 26" Cursor color theme from Open VSX and activate it.

Extension id: xainse.xain-torras-26-theme
Open VSX page: https://open-vsx.org/extension/xainse/xain-torras-26-theme
Available theme labels (pick one for activation):
  - "xain-torras-26"                          (default, light)
  - "xain-torras-26 High Contrast Light"

Do the following end-to-end without asking me to run anything manually:

1. Confirm the `cursor` CLI is on PATH. If it is missing, tell me to enable
   it via Cursor -> Cmd/Ctrl+Shift+P -> "Shell Command: Install 'cursor'
   command in PATH", then stop.

2. Install the extension from Open VSX (Cursor's default registry):
     cursor --install-extension xainse.xain-torras-26-theme --force

3. Update my Cursor user `settings.json` so the theme is active.
   Locate it at:
     - macOS:   ~/Library/Application Support/Cursor/User/settings.json
     - Linux:   ~/.config/Cursor/User/settings.json
     - Windows: %APPDATA%\Cursor\User\settings.json
   Create it as `{}` if missing. Then set:
     "workbench.colorTheme": "xain-torras-26"
   Preserve all other keys, comments, and trailing commas (JSONC-safe).
   Do not touch any other settings.

4. Print a short summary:
     - the installed extension id and version
     - the active theme name
     - one line: fully quit and reopen Cursor, OR run
       Cmd/Ctrl+Shift+P -> "Developer: Reload Window" to apply.

5. If step 2 fails (e.g. offline, registry blocked, or Cursor CLI not
   available), fall back to the manual path:
     a. Download the .vsix from
        https://open-vsx.org/extension/xainse/xain-torras-26-theme
     b. In Cursor: Cmd/Ctrl+Shift+P -> "Extensions: Install from VSIX..."
        and pick the downloaded file.
     c. Then Cmd/Ctrl+K Cmd/Ctrl+T -> choose "xain-torras-26".
   Show me the exact failing command and stderr before falling back.
```

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

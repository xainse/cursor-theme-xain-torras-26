# XAIN Torras 26 Theme Pack

[![Publish](https://github.com/xainse/cursor-theme-xain-torras-26/actions/workflows/publish.yml/badge.svg)](https://github.com/xainse/cursor-theme-xain-torras-26/actions/workflows/publish.yml)
[![Open VSX Version](https://img.shields.io/open-vsx/v/xainse/xain-torras-26-theme?label=Open%20VSX&color=c160ef)](https://open-vsx.org/extension/xainse/xain-torras-26-theme)
[![Open VSX Downloads](https://img.shields.io/open-vsx/dt/xainse/xain-torras-26-theme?label=downloads&color=ff7a1a)](https://open-vsx.org/extension/xainse/xain-torras-26-theme)
[![Open VSX Rating](https://img.shields.io/open-vsx/rating/xainse/xain-torras-26-theme?label=rating)](https://open-vsx.org/extension/xainse/xain-torras-26-theme/reviews)
[![License: MIT](https://img.shields.io/github/license/xainse/cursor-theme-xain-torras-26?color=blue)](./LICENSE)
[![Last commit](https://img.shields.io/github/last-commit/xainse/cursor-theme-xain-torras-26)](https://github.com/xainse/cursor-theme-xain-torras-26/commits/main)

Light themes for Cursor/VS Code based on the `xain-torras-26` palette.

## Preview

![XAIN Torras 26 theme — Cursor preview](./xain-cursor-theme-26.png)

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

### Automated release (recommended)

Releases are published automatically by [`.github/workflows/publish.yml`](.github/workflows/publish.yml) when a `v*.*.*` tag is pushed. The workflow packages the `.vsix`, publishes it to Open VSX and attaches the artifact to a GitHub Release.

One-time setup:

1. Create a Personal Access Token on [open-vsx.org](https://open-vsx.org/user-settings/tokens).
2. In the repo go to **Settings → Secrets and variables → Actions → New repository secret** and add:
   - Name: `OVSX_PAT`
   - Value: your Open VSX token

Cutting a release:

```bash
npm version patch   # or minor / major — bumps package.json and creates a tag
git push --follow-tags
```

You can also trigger the workflow manually from the **Actions** tab (use the `dry_run` input to only build the `.vsix` without publishing).

### Manual publish

```bash
npx ovsx publish -p <OPEN_VSX_TOKEN>
```

## Optional: Publish to VS Code Marketplace

```bash
npx @vscode/vsce publish
```

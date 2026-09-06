# Changelog

All notable changes to the **XAIN Torras 26 Theme Pack** are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Calendar Versioning (CalVer)](https://calver.org/) (`YYYY.M.PATCH`, no leading zeros — required by VS Code/Open VSX).

## [Unreleased]

## [2026.9.1] - 2026-09-06

### Added
- `xain-torras-26 Dark` — navy dark theme from the Torras dark reference, with the same orange accent `#FC703C`, in the existing theme pack alongside light and high-contrast light.
- Dark theme preview screenshot (`xain-cursor-dark-theme-26.png`) as the primary README preview; light preview kept at the bottom.
- README badges: GitHub Release, Stars, VS Code `^1.80.0`, and Cursor theme.

### Changed
- Sidebars and tabs use blue-violet navy from the dark reference; terminal/panel match the status bar (`#22283A`).

## [0.0.5] - 2026-05-30

### Changed
- Expanded the Cursor agent one-click install prompt in `README.md` with a preferred **PATH A** that installs the extension directly from the Open VSX `.vsix` (no `cursor` CLI required) and a CLI-based **PATH B** fallback that locates the bundled `cursor` binary across macOS/Linux/Windows install paths.
- Hardened `.github/workflows/publish.yml`:
  - The "Publish to Open VSX" step is now idempotent — if the target version is already published on Open VSX the step emits a warning and exits successfully instead of failing the workflow (fixes spurious failures on manual `workflow_dispatch` re-runs of an already-released tag).
  - Bumped the workflow's `node-version` from `20` to `22` (Active LTS).
  - Opted in to the Node.js 24 runtime for JavaScript actions via `FORCE_JAVASCRIPT_ACTIONS_TO_NODE24=true`, ahead of GitHub's 2026-06-16 forced cutover.
- Version bumped to `0.0.5` for automated release publish.

## [0.0.4] - 2026-05-30

### Added
- Extension icon at `images/icon.png` declared via the `icon` field in `package.json`, so the extension shows a logo on the Open VSX listing and in the VS Code/Cursor Extensions panel.

### Changed
- Refreshed documentation preview assets and related `README.md` references.
- Version bumped to `0.0.4` for automated release publish.

## [0.0.3] - 2026-05-30

### Added
- Hero preview screenshot in `README.md` showing the theme applied in Cursor.
- Status badges in `README.md`: Publish workflow status, Open VSX version, downloads and rating, MIT license, last commit.
- GitHub Actions workflow `.github/workflows/publish.yml` that, on a `v*.*.*` tag push (or manual `workflow_dispatch`):
  - verifies the tag matches `package.json` version,
  - packages the extension with `@vscode/vsce`,
  - uploads the `.vsix` as a workflow artifact,
  - publishes to Open VSX using the `OVSX_PAT` secret,
  - creates a GitHub Release with the `.vsix` attached and auto-generated notes.
- `dry_run` input on the publish workflow to package without publishing.

### Changed
- `.vscodeignore` now excludes `.github/**` so workflow files are not bundled into the published `.vsix`.
- Version bumped to `0.0.3` for automated release publish.

## [0.0.2] - 2026-05-30

### Added
- `repository`, `homepage` and `bugs` fields in `package.json` so the Open VSX listing links back to the GitHub repository.
- `.vscodeignore` to keep `.gitignore`, `.DS_Store` and packaging artifacts out of the published `.vsix`.
- One-click Cursor agent install prompt in `README.md` that drives the Cursor agent to install the extension from Open VSX and activate the theme via `settings.json`, with a manual VSIX fallback.

### Changed
- Version bumped to `0.0.2` and republished on Open VSX with corrected metadata.
- Title in `README.md` uppercased to **XAIN** for brand consistency.

### Fixed
- Copyright holder spelling in `LICENSE` corrected from "Serhii Xholin" to "Serhii Xolin".

## [0.0.1] - 2026-05-29

### Added
- Initial release of the theme pack with two light themes:
  - `xain-torras-26` — default light theme based on the Torras palette with orange accents.
  - `xain-torras-26 High Contrast Light` — high-contrast variant for accessibility.
- `package.json` extension manifest declaring both themes under the `Themes` category.
- MIT `LICENSE`.
- Initial `README.md` with installation and local-test instructions.

[Unreleased]: https://github.com/xainse/cursor-theme-xain-torras-26/compare/v2026.9.1...HEAD
[2026.9.1]: https://github.com/xainse/cursor-theme-xain-torras-26/compare/v0.0.5...v2026.9.1
[0.0.5]: https://github.com/xainse/cursor-theme-xain-torras-26/compare/v0.0.4...v0.0.5
[0.0.4]: https://github.com/xainse/cursor-theme-xain-torras-26/compare/v0.0.3...v0.0.4
[0.0.3]: https://github.com/xainse/cursor-theme-xain-torras-26/compare/v0.0.2...v0.0.3
[0.0.2]: https://github.com/xainse/cursor-theme-xain-torras-26/compare/756f749...v0.0.2
[0.0.1]: https://github.com/xainse/cursor-theme-xain-torras-26/tree/756f749

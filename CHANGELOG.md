# Changelog

All notable changes to the **XAIN Torras 26 Theme Pack** are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Changed
- Refreshed documentation preview assets and related `README.md` references.

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

[Unreleased]: https://github.com/xainse/cursor-theme-xain-torras-26/compare/v0.0.3...HEAD
[0.0.3]: https://github.com/xainse/cursor-theme-xain-torras-26/compare/v0.0.2...v0.0.3
[0.0.2]: https://github.com/xainse/cursor-theme-xain-torras-26/compare/756f749...v0.0.2
[0.0.1]: https://github.com/xainse/cursor-theme-xain-torras-26/tree/756f749

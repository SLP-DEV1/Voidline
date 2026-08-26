# Changelog

All notable repository and binary-release changes should be documented here.

The format follows the spirit of [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Application version metadata should be aligned with Git tags in a future compiled release.

## Unreleased

### Repository

- Reworked the README into a download-first binary release landing page.
- Clarified that Voidline is intentionally distributed as a binary-only project.
- Added direct release-download and SHA-256 verification guidance.
- Added contribution and security guidance for runtime/documentation reports.
- Added issue and pull-request templates.
- Added repository hygiene rules and a lightweight health workflow.
- Updated repository health checks to require the published EXE/DLL bundle.
- Added automated packaging for future `v*` tags.
- Added versioned release ZIPs and `SHA256SUMS.txt` generation.
- Removed committed local ImGui window state.
- Removed unsupported anti-cheat safety claims from project documentation.

## v3 - 2026-07-25

- Published the current prebuilt Voidline runtime bundle.
- Added the v3 GitHub release/tag.
- Added a versioned `Voidline-v3.zip` release asset.
- Added `SHA256SUMS.txt` for archive and core-binary verification.

### Distribution notes

- Source code is intentionally not published.
- Runtime package metadata identifies the application as `Voidline/1.0.0`, which does not match the `v3` Git tag.
- Third-party dependencies remain subject to their respective licenses.

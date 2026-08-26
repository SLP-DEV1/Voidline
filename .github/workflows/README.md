# Repository automation

- `repo-health.yml` checks the binary-only repository structure and documentation.
- `publish-release.yml` packages future `v*` tags into a versioned ZIP and publishes SHA-256 checksums.
- `bootstrap-v3-release-assets.yml` is a one-time workflow used to attach packaged assets to the existing v3 release and can be removed after it succeeds.

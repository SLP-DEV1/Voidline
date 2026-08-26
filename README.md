# Voidline

> A Windows/.NET 9 external CS2 research overlay and tooling bundle with an ImGui-based interface.

[![Release](https://img.shields.io/github/v/release/SLP-DEV1/Voidline?display_name=tag)](https://github.com/SLP-DEV1/Voidline/releases)
[![Repository health](https://github.com/SLP-DEV1/Voidline/actions/workflows/repo-health.yml/badge.svg)](https://github.com/SLP-DEV1/Voidline/actions/workflows/repo-health.yml)
[![Stars](https://img.shields.io/github/stars/SLP-DEV1/Voidline?style=flat)](https://github.com/SLP-DEV1/Voidline/stargazers)
[![Windows](https://img.shields.io/badge/platform-Windows-0078D4)](https://www.microsoft.com/windows)
[![.NET 9](https://img.shields.io/badge/.NET-9.0-512BD4)](https://dotnet.microsoft.com/)

Voidline is a prebuilt Windows runtime bundle focused on overlay rendering, game-state visualization, configurable input automation, map helpers, and profile-based configuration.

## Repository status

**Important:** the current `main` branch contains the **published runtime bundle**, not the C# source tree. The repository therefore cannot currently be built from source or meaningfully code-reviewed.

| Item | Status |
| --- | --- |
| Current GitHub release | `v3` |
| Runtime | .NET 9.0 + Windows Desktop |
| Source code | Not currently published in this repository |
| Build-from-source | Not currently available |
| Open-source license | Not currently included |
| Distribution | Prebuilt executable + runtime dependencies |

If the goal is to grow this into a real open-source project, publishing the source under `src/`, adding an explicit license, and producing binaries through GitHub Releases are the highest-impact next steps.

## Highlights

Voidline currently exposes a broad set of modules through a modern ImGui UI:

- **Overlay visualization** — player boxes, skeletons, health/armor, tracers, world entities, radar, spectator information, C4 status, and configurable colors/effects.
- **Aim and input tooling** — configurable aim assistance, recoil compensation, trigger behavior, FOV controls, and movement helpers intended for local/offline testing.
- **Geometry-aware helpers** — map geometry, visibility checks, ray intersection, and grenade lineup storage.
- **Feedback tools** — hit feedback, sounds, counters, and configurable overlays.
- **Profiles and settings** — JSON-backed configuration and UI/performance settings.
- **Rendering stack** — ImGui.NET, ClickableTransparentOverlay, Direct3D/Vortice, ImageSharp, NAudio, and SharpGLTF dependencies.

## Runtime requirements

- Windows 10 or Windows 11
- .NET 9 Desktop Runtime
- Counter-Strike 2 for the game-specific runtime integration

The checked-in runtime configuration targets both `Microsoft.NETCore.App` 9.0 and `Microsoft.WindowsDesktop.App` 9.0.

## Getting the current build

The current repository is a runtime bundle. For local/offline testing:

1. Install the .NET 9 Desktop Runtime.
2. Download the repository or the tagged GitHub release.
3. Keep `Voidline.exe`, `Voidline.dll`, the dependency DLLs, and `runtimes/` together.
4. Run the application only in an environment where you are authorized to test it.

The `v3` GitHub release currently points at the repository state and has no separately uploaded release assets, so the repository archive is effectively the distribution at the moment.

## Repository layout

The current tree is a **published application layout**, not the source layout:

```text
Voidline/
├── Voidline.exe
├── Voidline.dll
├── Voidline.deps.json
├── Voidline.runtimeconfig.json
├── *.dll                     # managed dependencies
├── runtimes/                 # native runtime dependencies
├── README.md
├── CONTRIBUTING.md
├── SECURITY.md
├── CHANGELOG.md
└── .github/
```

A future source-based layout should instead keep generated binaries out of the repository root, for example:

```text
Voidline/
├── src/
│   └── Voidline/
├── tests/
├── docs/
├── .github/
└── README.md
```

Release binaries should then be attached to versioned GitHub Releases rather than committed as the primary project contents.

## Versioning note

There is currently a version mismatch worth fixing in the next product release:

- Git tag/release: `v3`
- Runtime package metadata in `Voidline.deps.json`: `Voidline/1.0.0`

Aligning the assembly/package version with the Git tag will make diagnostics, bug reports, and release notes much clearer.

## Project roadmap

The most valuable repository improvements from here are:

1. Publish the actual C# source under `src/`.
2. Add a clear open-source license after choosing the intended license terms.
3. Move compiled binaries and third-party DLLs into GitHub Release assets.
4. Add a real build/test workflow once the source is available.
5. Add screenshots or a short GIF of the UI so visitors understand the project in seconds.
6. Add checksums for downloadable release artifacts.
7. Keep release tags, assembly versions, and changelog entries in sync.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

Until the source is published, useful contributions are primarily documentation fixes, reproducible runtime bug reports, packaging improvements, and repository maintenance suggestions.

## Security and responsible use

Voidline does **not** make any guarantee that a build is safe from anti-cheat detection, bans, incompatibilities, or future game updates. Claims such as “VAC secure” are intentionally avoided because they cannot be guaranteed.

Use the project only in environments where you have permission to test. Do not use it to disrupt public matches or other players.

For security-reporting guidance, see [SECURITY.md](SECURITY.md).

## Dependencies and credits

The runtime bundle includes or references components such as:

- [ClickableTransparentOverlay](https://github.com/zaafar/ClickableTransparentOverlay)
- [ImGui.NET](https://github.com/ImGuiNET/ImGui.NET)
- [NAudio](https://github.com/naudio/NAudio)
- [Newtonsoft.Json](https://www.newtonsoft.com/json)
- [SixLabors.ImageSharp](https://github.com/SixLabors/ImageSharp)
- [Vortice.Windows](https://github.com/amerkoleci/Vortice.Windows)
- [SharpGLTF](https://github.com/vpenades/SharpGLTF)

Third-party components remain subject to their own licenses and terms.

## License

No open-source license is currently included in this repository. Until an explicit license is added, normal copyright restrictions apply.

---

If this project is useful to you, starring the repository helps others discover it and makes it easier to gauge interest in a source-code release.
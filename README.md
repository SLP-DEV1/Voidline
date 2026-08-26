<div align="center">

# Voidline

**Binary-only Windows/.NET 9 distribution for local/offline and otherwise authorized testing.**

[![Release](https://img.shields.io/github/v/release/SLP-DEV1/Voidline?display_name=tag)](https://github.com/SLP-DEV1/Voidline/releases/latest)
[![Repository health](https://github.com/SLP-DEV1/Voidline/actions/workflows/repo-health.yml/badge.svg)](https://github.com/SLP-DEV1/Voidline/actions/workflows/repo-health.yml)
[![Stars](https://img.shields.io/github/stars/SLP-DEV1/Voidline?style=flat)](https://github.com/SLP-DEV1/Voidline/stargazers)
[![Windows](https://img.shields.io/badge/platform-Windows-0078D4)](https://www.microsoft.com/windows)
[![.NET 9](https://img.shields.io/badge/.NET-9.0-512BD4)](https://dotnet.microsoft.com/)
![Distribution](https://img.shields.io/badge/distribution-binary--only-444444)

### [Download Voidline v3](https://github.com/SLP-DEV1/Voidline/releases/download/v3/Voidline-v3.zip) · [SHA-256 checksums](https://github.com/SLP-DEV1/Voidline/releases/download/v3/SHA256SUMS.txt) · [All releases](https://github.com/SLP-DEV1/Voidline/releases)

</div>

Voidline is distributed as a **prebuilt application bundle**. The repository intentionally contains the executable, application assembly, managed dependencies, native runtime files, and documentation needed to use the published build.

> **Binary-only by design:** the C# source code is not published and is not part of the distribution plan.

## At a glance

| | |
| --- | --- |
| **Distribution** | Binary-only |
| **Current release** | `v3` |
| **Main executable** | `Voidline.exe` |
| **Application assembly** | `Voidline.dll` |
| **Runtime** | .NET 9.0 + Windows Desktop |
| **Supported OS** | Windows 10 / 11 |
| **Build from source** | Not available |
| **Release integrity** | Versioned ZIP + SHA-256 checksums |

## Highlights

The current build provides an ImGui-based interface with configurable runtime modules grouped around visualization, input, map assistance, feedback, and profiles.

| Area | Included capabilities |
| --- | --- |
| **Overlay & visualization** | Player/world information, skeleton/box overlays, tracers, health/armor information, C4 status and configurable visual styling |
| **Radar & awareness** | Radar, spectator information, distance/ping and world-entity information |
| **Input tooling** | Configurable aim/input helpers, recoil-related controls and movement helpers for authorized testing |
| **Map helpers** | Geometry/visibility helpers and grenade-lineup storage |
| **Feedback** | Hit feedback, sounds, counters and configurable overlays |
| **Profiles** | JSON-backed configuration plus UI and performance settings |
| **Rendering stack** | ImGui.NET, ClickableTransparentOverlay, Direct3D/Vortice, ImageSharp, NAudio and SharpGLTF |

## Quick start

1. Download **`Voidline-v3.zip`** from the latest release.
2. Extract the entire archive to one folder.
3. Install the **.NET 9 Desktop Runtime** if it is not already installed.
4. Keep `Voidline.exe`, `Voidline.dll`, all dependency DLLs, runtime JSON files and `runtimes/` together.
5. Start `Voidline.exe` only in an environment where you are authorized to test it.

> Do not copy only the EXE. Voidline depends on the accompanying assemblies and runtime files.

## Verify your download

Every packaged release is accompanied by `SHA256SUMS.txt`.

On PowerShell:

```powershell
Get-FileHash .\Voidline-v3.zip -Algorithm SHA256
```

Compare the returned hash with the `Voidline-v3.zip` entry in `SHA256SUMS.txt` from the same GitHub Release.

## Requirements

- Windows 10 or Windows 11
- .NET 9 Desktop Runtime
- Counter-Strike 2 for game-specific integration

The included runtime configuration targets both `Microsoft.NETCore.App` 9.0 and `Microsoft.WindowsDesktop.App` 9.0.

## Binary-only by design

This repository is a **release/download repository**, not a source-code project.

The runtime bundle is intentionally committed so a tagged Git revision contains the same binary payload that is packaged into its release archive. Source-code pull requests are therefore not expected.

## Repository layout

```text
Voidline/
├── Voidline.exe
├── Voidline.dll
├── Voidline.deps.json
├── Voidline.runtimeconfig.json
├── *.dll                     # managed dependencies
├── runtimes/                 # native runtime dependencies
├── README.md
├── SECURITY.md
├── CHANGELOG.md
└── .github/
```

Generated local state such as `imgui.ini` is intentionally excluded from version control.

## Releases

Tagged releases are packaged automatically as:

```text
Voidline-vX.Y.Z.zip
SHA256SUMS.txt
```

The release workflow validates that the core runtime files exist, creates a clean archive from the tracked runtime payload, generates SHA-256 hashes for the archive and core binaries, and uploads them to the matching GitHub Release.

### Versioning note

The current GitHub release/tag is `v3`, while `Voidline.deps.json` still identifies the application package as `Voidline/1.0.0`. Aligning the compiled application metadata with future Git tags will make diagnostics and bug reports clearer.

## Bug reports and suggestions

Issues are welcome for reproducible runtime problems, startup failures, dependency/compatibility issues, packaging problems, documentation corrections, UI/UX feedback and feature suggestions.

Because Voidline is binary-only, documentation and repository-maintenance pull requests are welcome; source-code pull requests are not expected.

## Security and responsible use

Voidline does **not** guarantee that a build is safe from anti-cheat detection, bans, incompatibilities or future game updates. No anti-cheat bypass or detection-avoidance guarantee is made.

Use the project only in environments where you have permission to test it. Do not use it to disrupt public matches or other players.

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

No open-source source-code license is provided because the application source is not published. Third-party libraries remain subject to their respective licenses.

---

<div align="center">

**If Voidline is useful to you, a ⭐ helps other users discover the project.**

</div>

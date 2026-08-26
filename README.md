# Voidline

> Binary-only Windows/.NET 9 distribution of Voidline for local/offline and otherwise authorized testing.

[![Release](https://img.shields.io/github/v/release/SLP-DEV1/Voidline?display_name=tag)](https://github.com/SLP-DEV1/Voidline/releases)
[![Repository health](https://github.com/SLP-DEV1/Voidline/actions/workflows/repo-health.yml/badge.svg)](https://github.com/SLP-DEV1/Voidline/actions/workflows/repo-health.yml)
[![Stars](https://img.shields.io/github/stars/SLP-DEV1/Voidline?style=flat)](https://github.com/SLP-DEV1/Voidline/stargazers)
[![Windows](https://img.shields.io/badge/platform-Windows-0078D4)](https://www.microsoft.com/windows)
[![.NET 9](https://img.shields.io/badge/.NET-9.0-512BD4)](https://dotnet.microsoft.com/)
![Distribution](https://img.shields.io/badge/distribution-binary--only-444444)

Voidline is distributed as a **prebuilt application bundle**. This repository intentionally contains the executable, application DLL, required managed dependencies, native runtime files, and project documentation.

## Binary-only by design

The C# source code is **not published in this repository and is not part of the distribution plan**.

| Item | Status |
| --- | --- |
| Distribution model | Binary-only |
| Main executable | `Voidline.exe` |
| Application assembly | `Voidline.dll` |
| Runtime | .NET 9.0 + Windows Desktop |
| Supported OS | Windows 10 / 11 |
| Source code | Not published |
| Build-from-source | Not available |
| Current GitHub release | `v3` |

This repository should therefore be treated as a **release/download repository**, not as a source-code project.

## Highlights

The current build includes an ImGui-based interface and a broad collection of configurable visualization, input, map-helper, feedback, profile, and runtime modules.

Notable areas include:

- configurable overlay visualization
- player/world information rendering
- radar and spectator information
- map and geometry helpers
- input and recoil-related tooling
- grenade-lineup storage
- hit feedback and audio
- JSON-backed profiles and UI settings
- Direct3D/ImGui-based rendering

## Requirements

- Windows 10 or Windows 11
- .NET 9 Desktop Runtime
- Counter-Strike 2 for game-specific integration

The included runtime configuration targets both `Microsoft.NETCore.App` 9.0 and `Microsoft.WindowsDesktop.App` 9.0.

## Download and run

1. Download the latest repository/release archive.
2. Keep `Voidline.exe`, `Voidline.dll`, all dependency DLLs, JSON runtime files, and `runtimes/` together.
3. Install the .NET 9 Desktop Runtime if it is not already installed.
4. Run `Voidline.exe` only in an environment where you are authorized to test it.

Do not copy only the EXE by itself. The application depends on the accompanying assemblies and runtime files.

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

The repository currently uses the `v3` tag/release. For future releases, the most useful improvements are distribution-focused rather than source-focused:

- attach a clean versioned ZIP to each GitHub Release
- publish SHA-256 checksums for downloadable archives
- keep Git tags and application version metadata aligned
- include concise release notes and compatibility notes
- add screenshots or a short GIF of the UI
- keep old builds available through GitHub Releases when practical

### Versioning note

The current release/tag is `v3`, while the runtime dependency metadata still identifies the application package as `Voidline/1.0.0`. Aligning these values in a future compiled build would make diagnostics and bug reports clearer.

## Bug reports and suggestions

Issues are welcome for:

- reproducible crashes or startup failures
- runtime/dependency problems
- Windows/.NET compatibility issues
- packaging problems
- documentation corrections
- UI/UX feedback
- feature suggestions

Because the project is binary-only, source-code pull requests are not expected. Documentation and repository-maintenance pull requests may still be useful.

## Security and responsible use

Voidline does **not** make any guarantee that a build is safe from anti-cheat detection, bans, incompatibilities, or future game updates. Claims such as “VAC secure” or “undetectable” are intentionally avoided because they cannot be guaranteed.

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

If Voidline is useful to you, starring the repository helps others find the project and shows interest in future binary releases.
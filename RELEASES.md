# Voidline Releases

Voidline is distributed as a binary-only Windows/.NET bundle.

## Release contents

Each automated tagged release should contain:

- `Voidline-vX.Y.Z.zip` — complete tracked runtime payload
- `SHA256SUMS.txt` — SHA-256 hashes for the ZIP, `Voidline.exe`, and `Voidline.dll`

The ZIP contains the executable, application assembly, managed dependency DLLs, runtime JSON files, and native files under `runtimes/`.

## Verify a release

### PowerShell

```powershell
Get-FileHash .\Voidline-vX.Y.Z.zip -Algorithm SHA256
```

Compare the returned hash with the matching ZIP entry in `SHA256SUMS.txt` from the same GitHub Release.

### Linux / WSL

```bash
sha256sum Voidline-vX.Y.Z.zip
```

## Packaging policy

- Release archives are built only from files already tracked in the tagged repository state.
- Generated local UI state such as `imgui.ini` is excluded.
- Release packaging does not publish source code.
- The runtime bundle should be extracted completely; do not copy only `Voidline.exe`.

## Versioning

Git tags identify public binary releases. Application metadata should be kept aligned with future release tags where practical.

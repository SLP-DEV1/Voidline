# Binary Release Checklist

Use this checklist before publishing a new Voidline binary tag.

- Confirm `Voidline.exe` and `Voidline.dll` are the intended build.
- Confirm `Voidline.deps.json` and `Voidline.runtimeconfig.json` match the bundle.
- Keep required dependency DLLs and `runtimes/` files together.
- Update `CHANGELOG.md` with user-visible changes.
- Align application version metadata with the Git tag when possible.
- Tag the release with a `v*` tag.
- Confirm the release workflow uploads `Voidline-vX.Y.Z.zip` and `SHA256SUMS.txt`.
- Verify the ZIP hash against `SHA256SUMS.txt`.
- Test the extracted ZIP on a clean Windows environment with the .NET 9 Desktop Runtime.
- Add a real UI screenshot/GIF to the README when one is available.

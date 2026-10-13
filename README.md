# Redock Update Repository

This repository hosts **release assets** for the Redock auto-updater.

## How It Works

When Redock launches it checks this repository's latest release tag against the local `version.txt`. If a newer version is available, it prompts the user and downloads only the changed assets from the release.

## For Maintainers

See the [setup guide](https://github.com/reganktn/RedockUpdate) for instructions on:
- Versioning convention (`v1.0.0`, `v1.1.0`, etc.)
- Which files to attach as release assets
- How to create a new release

## File Layout (Release Assets)

| File | Purpose |
|---|---|
| `Redock.exe` | Main application |
| `OverlayDLL.dll` | Overlay rendering DLL |
| `dlls/*.dll` | Runtime dependencies (OpenCV, ONNX Runtime, Qt, DirectML) |
| `dlls/cuda/*.dll` | CUDA/TensorRT runtime (optional, for CUDA mode) |
| `dlls/platforms/qwindows.dll` | Qt platform plugin |

> Large binaries are attached as **release assets** only — they are not stored in the git tree.

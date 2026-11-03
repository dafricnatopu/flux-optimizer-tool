<div align="center">
  <img src="./flux-logo.svg" alt="Flux" width="72" height="72" />

  # Flux

  **Find common PC slowdowns, review Windows problems and maintain your system.**

  [![Latest release](https://img.shields.io/github/v/release/dafricnatopu/flux-optimizer-tool)](https://github.com/dafricnatopu/flux-optimizer-tool/releases/latest)
  [![Downloads](https://img.shields.io/github/downloads/dafricnatopu/flux-optimizer-tool/total)](https://github.com/dafricnatopu/flux-optimizer-tool/releases)
  [![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-blue)](https://github.com/dafricnatopu/flux-optimizer-tool/releases/latest)
</div>

## Download Flux 1.3.0

[**Download the Windows x64 installer**](https://github.com/dafricnatopu/flux-optimizer-tool/releases/download/v1.3.0/FluxOptimizer-Setup-v1.3.0.exe)

Run `FluxOptimizer-Setup-v1.3.0.exe`. The `.blockmap` and `latest.yml` assets are for the updater; download the `.exe` to install Flux.

If the installer cannot close an existing Flux instance, save your work and fully quit Flux from its tray menu before retrying. Very old builds using the previous update feed should be updated manually.

## New in 1.3.0

- **Game mode:** supported-game detection, temporary power/gaming settings, optional automatic activation and restoration of saved originals.
- **Crashes & restarts:** grouped Windows event records, graphics-driver resets, readable error explanations and copyable details.
- **Share your setup:** a previewable hardware card, saved as PNG without automatic personal names or serial numbers.
- **A new look:** F logo, six Flux Fold wallpapers, wallpaper downloads, local fonts and a calmer startup screen.
- **Clearer Overview:** compact live readings, explanations, stale-check indicators and changes since the previous check.
- Searchable startup apps, more informative disk health and quieter update notifications in the sidebar.

See the [full changelog](CHANGELOG.md).

## Other tools

- Read-only checks for common slowdowns, Windows security and available hardware sensors.
- Grouped running apps with CPU/memory readings and confirmation before closing supported user apps.
- Cleaner with conservative defaults and actual cleanup results; optional caches, logs and Recycle Bin cleanup.
- Connection quality and DNS lookup tests, plus per-adapter DNS changes with saved originals.
- Supported registry adjustments with original-value backups, startup controls and Windows restore-point tools.
- Local activity history and shortcuts to Windows maintenance tools.

## Verification and limits

93 automated tests pass on Windows. The renderer and x64 installer are built locally, and packaged files and updater hashes are checked before publication. SHA-256 checksums are included with the downloads.

Game mode does not promise an FPS increase. Windows events, network measurements and disk counters are diagnostic observations; missing readings remain unknown. Automatic closure during an in-place upgrade has not been verified for this release. These checks do not replace testing across every Windows version and hardware configuration.

System changes can require administrator permission. Review the action and create a restore point when appropriate. Deleted files cannot be recovered through Flux; supported setting restoration requires originals saved by Flux.

## Community and support

- [Report an issue](https://github.com/dafricnatopu/flux-optimizer-tool/issues)
- [Discord community](https://discord.gg/KzadbwmfMz)
- [All releases](https://github.com/dafricnatopu/flux-optimizer-tool/releases)

This public repository contains downloads and release documentation. Application source is maintained separately.

Made by Dafric.

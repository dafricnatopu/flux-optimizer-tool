<div align="center">
  <img src="./flux-logo.svg" alt="Flux" width="72" height="72" />

  # Flux

  **See what’s slowing down your PC. You decide what changes.**

  [![Latest release](https://img.shields.io/github/v/release/dafricnatopu/flux-optimizer-tool)](https://github.com/dafricnatopu/flux-optimizer-tool/releases/latest)
  [![Downloads](https://img.shields.io/github/downloads/dafricnatopu/flux-optimizer-tool/total)](https://github.com/dafricnatopu/flux-optimizer-tool/releases)
  [![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-blue)](https://github.com/dafricnatopu/flux-optimizer-tool/releases/latest)
</div>

## Download Flux 1.4.0

[**Download the Windows x64 installer**](https://github.com/dafricnatopu/flux-optimizer-tool/releases/download/v1.4.0/FluxOptimizer-Setup-v1.4.0.exe)

Run `FluxOptimizer-Setup-v1.4.0.exe` on Windows 10 or 11. The `.blockmap` and `latest.yml` files are for the updater. Use `SHA256SUMS.txt` to verify the download.

If setup asks you to close Flux, select **Quit Flux** from the tray menu and then retry. Very old builds using the previous update feed should be updated manually.

## New in 1.4.0

- **Ask Flux AI** answers PC and Windows questions and can open the relevant Flux page. Open it from the title bar or press Ctrl+K. Sign-in is required and a daily question limit applies.
- **Optional account** with Discord or Google sign-in. Local diagnostics and maintenance are available without an account.
- **Five interface languages** in the sidebar account menu. Choose English, Czech, Slovak, German or Polish. Some diagnostic text remains in English.
- **Network diagnostics** add longer stability tests, an internet speed test and Wi-Fi details. DNS presets support IPv6 where available, and Flux can restore the saved IPv4 and IPv6 settings.
- **Game mode** has better detection and artwork for supported games, including Valorant and Phasmophobia. Flux restores saved Windows settings before an in-app update starts.
- **Clearer diagnostics and cleanup** with more informative memory readings, check results and confirmed cleanup totals.

See the [1.4.0 release notes](https://github.com/dafricnatopu/flux-optimizer-tool/releases/tag/v1.4.0) and the [changelog for earlier versions](CHANGELOG.md).

## Other tools

- Read-only checks for common slowdowns, Windows security and available hardware sensors.
- Grouped running apps with CPU/memory readings and confirmation before closing supported user apps.
- Cleaner with conservative defaults and actual cleanup results; optional caches, logs and Recycle Bin cleanup.
- Connection quality and DNS lookup tests, plus per-adapter DNS changes with saved originals.
- Supported registry adjustments with original-value backups, startup controls and Windows restore-point tools.
- Local activity history and shortcuts to Windows maintenance tools.

## Verification and limits

252 automated tests passed for 1.4.0 on Windows. The installer contents and updater metadata were verified before publication, and SHA-256 checksums are available with the release.

Windows events, network measurements and disk counters describe what was observed. Missing readings stay unknown. Game mode changes supported Windows settings for the duration of a game, and its effect on performance varies by system.

System changes can require administrator permission. Review the action and create a restore point when appropriate. Deleted files cannot be recovered through Flux; supported setting restoration requires originals saved by Flux.

## Community and support

- [Report an issue](https://github.com/dafricnatopu/flux-optimizer-tool/issues)
- [Discord community](https://discord.gg/KzadbwmfMz)
- [All releases](https://github.com/dafricnatopu/flux-optimizer-tool/releases)

This public repository contains downloads and release documentation. Application source is maintained separately.

Made by Dafric.

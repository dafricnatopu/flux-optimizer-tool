<div align="center">
  <img src="./flux_optimizer_readme_banner.svg" alt="Flux Optimizer" width="100%" />

  **A Windows maintenance and system-inspection app.**

  [![Latest release](https://img.shields.io/github/v/release/dafricnatopu/flux-optimizer-tool)](https://github.com/dafricnatopu/flux-optimizer-tool/releases/latest)
  [![Downloads](https://img.shields.io/github/downloads/dafricnatopu/flux-optimizer-tool/total)](https://github.com/dafricnatopu/flux-optimizer-tool/releases)
  [![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-blue)](https://github.com/dafricnatopu/flux-optimizer-tool/releases/latest)
</div>

## Download Flux 1.2.1

[**Download the Windows x64 installer**](https://github.com/dafricnatopu/flux-optimizer-tool/releases/download/v1.2.1/FluxOptimizer-Setup-v1.2.1.exe)

Run `FluxOptimizer-Setup-v1.2.1.exe`. Administrator permission is requested when a selected system operation needs it.

**Updating from 1.0.1? Install 1.2.1 manually.** Older builds may use the previous update feed. This release uses the public release feed in this repository.

The `.blockmap` and `latest.yml` release assets support the app updater; download the `.exe` to install Flux.

## New in 1.2.1

- Installer shutdown fix with exit verification and retry/cancel handling.
- Background update progress, clearer notifications and reorganised Settings.
- Refreshable disk health, expanded Top apps and activity problem filtering.
- Regional date/time formatting, About links and recoverable page errors.
- Native clipboard and reused monitoring queries.

## Features

- **Live overview:** CPU, GPU, memory, system-drive storage and labelled download/upload rates, with clear high-usage states and review actions.
- **Personal appearance:** custom image/GIF backgrounds, blur, dimming and accent colors.
- **Diagnostics:** available CPU/GPU temperatures and clocks, recent load balance and a read-only Windows security overview, including third-party antivirus detection.
- **System check:** specific findings with verified-check coverage. Unsupported sensors and unsuccessful Windows queries remain unverified.
- **Running apps:** grouped CPU/memory usage and confirmation before closing a user app; protected Windows/Flux processes cannot be ended here.
- **Cleaner:** scan selected categories, preserve recent files, pinned jump lists and unfinished downloads, and report actual cleanup results. Emptying the Recycle Bin requires separate confirmation.
- **Startup and DNS:** review startup registry entries; change IPv4 DNS on a selected adapter and restore its original automatic/manual configuration.
- **Registry adjustments:** inspect supported settings, save original values and restore them instead of guessing defaults.
- **Activity and recovery:** local action history, Windows utilities and restore-point tools.

See the [1.2.1 changelog and verification limits](CHANGELOG.md) and [all releases](https://github.com/dafricnatopu/flux-optimizer-tool/releases).

## Verification

50 automated tests passed. The renderer and Windows x64 installer are built locally; release downloads include checksums. See the changelog for limitations. Device health counters and network measurements are diagnostic observations, not guarantees.

## Before changing Windows

Create a restore point and review the selected action. Cleanup deletes files permanently; registry/DNS restoration requires an original configuration saved by Flux. A load imbalance alone does not establish a gaming bottleneck, and Flux does not promise an FPS increase.

Automated tests and local checks do not replace exhaustive Windows 10/11 VM testing. Hardware sensors and Windows services may not expose every reading.

## Community and support

- [Report an issue](https://github.com/dafricnatopu/flux-optimizer-tool/issues)
- [Discord community](https://discord.gg/KzadbwmfMz)

This public repository contains downloads and release documentation. Application source is maintained separately.

Made by Dafric.

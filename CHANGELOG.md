# Flux 1.1.0

Released 2026-10-31.

## What's new

- Redesigned dashboard and navigation with clearer live CPU, GPU, memory, storage and network metrics.
- Custom image/GIF backgrounds, blur, dimming and accent colors.
- CPU/GPU temperatures and clocks where the hardware exposes them.
- Read-only Windows security overview with third-party antivirus detection and on-demand update checks.
- System check with specific findings and verified-check coverage.
- Running apps grouped by CPU/memory use, with protected system processes and confirmation before closing an app.
- Local activity history that distinguishes success, partial completion, failure and native tools being opened.

## Reliability changes

- Supported registry tweaks save original values before applying changes and restore those values on request.
- DNS changes target a selected adapter and can restore the original automatic/manual configuration.
- Cleanup keeps recent files, pinned jump lists and in-progress downloads, avoids junctions, and reports actual results and partial failures. Recycle Bin deletion has separate confirmation.
- Stronger IPC validation, strict PowerShell error handling, and elevation only when an operation needs it.
- Driver information is an installed inventory. Load balance is a recent-load indication, not a proven gaming bottleneck or an FPS promise.

## Download and update

Download `FluxOptimizer-Setup-v1.1.0.exe` from this release. `latest.yml` and the `.blockmap` file support application updates and are not installers.

**Upgrading from 1.0.1:** install this version manually. Older builds can point to the previous update feed; 1.1.0 uses the public `dafricnatopu/flux-optimizer-tool` release feed.

## Verification and limits

- Production renderer build and Windows x64 NSIS installer build.
- 26 automated tests passed, including isolated system-action, process, appearance, telemetry and security-state checks.
- React Doctor: 100/100 for changed code.
- Hardware sensors and Windows security/update queries can be unavailable. Unknown results remain labelled as unverified.
- Exhaustive Windows 10/11 VM testing and an end-to-end upgrade from an installed older version have not been completed. Create a restore point before changing Windows settings.

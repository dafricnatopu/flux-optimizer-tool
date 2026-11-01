## [1.2.1] - 2026-11-01

### Added
- Settings shows who made Flux, with links to GitHub, Discord and release notes.
- A recovery screen when a page fails to load, with Try again and Copy error, instead of an empty window.
- Disk health can be checked again at any time and shows when it was last read.
- Activity can show only problems (failed or partly completed actions).
- Top apps can show more than six apps.

### Changed
- Notifications have a calmer, readable design: errors stay on screen longer, hovering pauses them and at most three are shown at once.
- Dates and times follow your Windows region: 24-hour clock in Czechia and most of Europe, 12-hour in the US.
- Settings is reorganised: updates and appearance first, then startup and window, privacy, support, and advanced settings collapsed at the bottom. Debug tools are hidden in the installed app.
- The analytics setting explains exactly what is sent when it is turned on (it stays off by default).
- The license card no longer promises features that don't exist: everything in Flux works without one.
- Diagnostics names its two checks clearly: "Why is my PC slow?" for slowness, and Quick check for a fast overview.
- The update window matches the rest of the app, and "Download in the background" now stays in the background as a small progress pill.

### Fixed
- The installer force-closes Flux without killing its updater child process, then verifies it has exited and keeps the retry prompt if it cannot be closed.
- The update dialog keeps keyboard focus inside it, supports Escape, and reports failures to start a download.
- Settings notifications describe the setting that actually changed.
- Downloading an update in the background no longer reopens the update window on every progress step.
- "Start minimized" only applies when Flux starts with Windows; opening Flux yourself always shows the window.
- Windows Updates page no longer crashes when an update comes without a description.
- "Require administrator" no longer closes Flux for good when the relaunch fails or is declined.
- Live monitoring uses one long-lived PowerShell instead of starting a new one every few seconds, and reads disk usage at most every 30 seconds, which lowers Flux's own CPU use while it is open.
- Flux denies camera, microphone, location and notification requests and blocks redirects to untrusted pages.
- Copy report uses the Windows clipboard directly, so it works reliably.
- The Tweaks confirmation for risky changes shows the right button text.

See [release notes and verification limits](https://github.com/dafricnatopu/flux-optimizer-tool/releases/tag/v1.2.1).

## [1.2.0] - 2026-11-01

### Added
- **Why is my PC slow? (Diagnostics):** a 5-second, read-only check of the usual causes: battery saver, power plan and power mode, CPU throttling or overheating, full memory, low disk space, HDD instead of SSD, a busy disk, a missing or broken graphics driver, two graphics chips on laptops, a pending restart, long uptime and too many startup apps. Shows only what it actually found, ordered by impact, with a fix or the right place to fix it.
- **Disk health (Diagnostics):** shows what Windows knows about each drive (healthy, needs attention or at risk), with SSD life left, temperature, power-on time and uncorrectable errors after an optional administrator read. A failing system disk is also reported by the slow-PC check.
- **Copy report:** copies a plain-text summary of the PC, what slows it down and disk health, ready to paste into Discord when asking someone for help.
- **Network page, rebuilt:** shows the connection actually in use (Wi-Fi or cable, link speed, Wi-Fi signal, IP, router and which DNS is really used).
- **Connection quality test:** pings your router and the internet at the same time and measures ping, jitter and packet loss, then says whether lag comes from your Wi-Fi, your provider, or neither.
- **DNS speed test:** measures real lookup speed for your current DNS and public resolvers instead of ICMP ping, and marks the fastest.
- **Big items (Cleaner):** old large downloads (moved to the Recycle Bin, never deleted outright), the hibernation file (with advice for desktops vs laptops, and a way to turn it back on), leftover NVIDIA/AMD driver installers and Windows' own update-component cleanup.
- **Automatic cleanup:** a shortcut to Windows Storage Sense instead of a duplicate background cleaner.
- **Toolbox:** Fix Windows Update (resets update services and renames the update cache instead of deleting it), Test memory (Windows Memory Diagnostic), Check disk for errors (read-only online scan) and Battery report.
- **Tweaks:** Show file extensions, Show hidden files and End task on the taskbar (Windows 11), all reversible.
- Tweaks: a "My changes" view and links from Activity to the matching restore tools.

### Changed
- Settings has an Updates card: shows your version, checks GitHub with a short scan, and says plainly whether you're up to date or a newer version is ready to download.
- Live metrics keep updating while Flux is visible but unfocused (e.g. on a second monitor during a game) and pause only when it is minimized, in the tray or explicitly hidden. Top apps refresh less often while Flux is not focused.
- Monitoring queries run only on pages that show them, one request at a time.
- Every page uses the same width, header and icon sizes.
- Clicking into the Cleaner no longer shows a "Scan complete" notification every time.

### Fixed
- Window buttons no longer show a focus outline when Flux starts.
- Saved registry originals are validated before restoration is offered.
- Unknown drive-health readings are not shown as healthy, and unavailable disk-error counters are not reported as zero.
- Windows Update repair restarts previously running services even when a cache rename fails.
- Settings shows the installed app version instead of a cached version from a previous installation.

## Verification and limitations

- 49 automated tests passed, including disk-health assessment, report formatting, monitoring lifecycle, input validation and isolated restoration/cleanup tests.
- Windows PowerShell syntax checks cover the new collectors and utility scripts. Windows Update repair failure handling is tested using fake service/filesystem commands, without changing actual Windows services.
- Production renderer and Windows x64 NSIS installer builds.
- Hardware health/SSD wear readings are device-reported estimates and may be unavailable, including after elevation. They do not guarantee future disk reliability.
- Connection-quality results are diagnostic indications, not proof that a specific ISP or device is faulty.
- Full Windows 10/11 VM compatibility testing and an installed-version auto-update round trip have not been completed.

## Installation and updates

Download `FluxOptimizer-Setup-v1.2.0.exe`. The `.blockmap`, `latest.yml` and `SHA256SUMS.txt` files support updates and file verification; they are not installers.

Users on 1.1.0 can check for updates through the existing public release feed. Builds on an older feed (including some 1.0.1 installs) may require a manual installation of this version.


---

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

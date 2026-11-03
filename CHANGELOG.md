## [Unreleased]

## [1.3.0] - 2026-11-03

### Added
- **Game mode:** detect supported running games, temporarily enable Windows Game Mode and High performance when available, then restore the saved settings. Includes optional automatic activation, per-game GPU preferences and a game card with artwork on Overview.
- **Crashes & restarts:** read Windows events from the last 7 or 30 days. Repeated app crashes and hangs are grouped by app, module and code; graphics-driver resets, blue screens, restarts and hardware reports have separate categories. Copy details includes recorded times without full file paths.
- **Share your setup:** preview and save a 1200 × 675 PNG with hardware specs and a Flux wallpaper. Includes an optional title, reported VRAM and RAM details; excludes automatic personal names, IP addresses and serial numbers.
- **Six Flux Fold wallpapers:** Dark, Light, Petrol, Sand, Plum and Rose, with a first-start appearance picker and an option to save the original JPG for your desktop.
- Repeated system checks show resolved issues and measurable changes. Startup apps now has search and All / Enabled / Disabled filters.

### Changed
- New F logo, application/tray icons, Archivo SemiExpanded headings and reorganised navigation. Game mode has its own section; startup apps, Tweaks and Network sit under Optimize.
- Overview puts findings and next steps first, with a compact live-metrics strip, clearer RAM/storage/network values, metric explanations and Windows-process labels in Top apps.
- Clearer disk health details explain SSD endurance, operating hours and errors. Missing readings stay unknown; HDDs are not given a remaining-life percentage.
- A wallpaper-backed startup screen waits for initial readings with a time limit. Fonts ship with Flux instead of loading from Google Fonts, charts use a consistent scale, and pages reuse their last readings while refreshing.
- Update availability, download progress and restart prompts appear quietly in the sidebar. Details open when selected.
- Cleaner defaults to temporary files; caches, crash logs and the Recycle Bin are separate options. "Big items" is now "Large files and optional cleanup" and no longer calls downloads safe to remove. Shorter text and clearer empty/error states throughout.

### Fixed
- Game mode verifies changes and restoration, retains its backup when restoration fails and offers retry. Manual stop pauses automatic activation for the current game; GPU preferences restore their previous values.
- Background selection and desktop validation use the same catalog; retired presets migrate without losing appearance preferences.
- Old system-check results are marked as outdated after time or relevant Flux changes. Live readings recover when an independent query fails instead of blocking behind a shared PowerShell process.
- Starting with Windows no longer briefly shows the window before it hides to the tray. Startup apps tells a failed load (with Try again) apart from an empty list, and errors are shown in plain words.

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

## [1.1.0] - 2026-10-31

- Replace fake update results and animated health scores with actual results and explicit errors.
- Redesign overview, navigation, network settings, tweaks and toolbox; add local activity history.
- Unify welcome identity, compact empty activity, increase dashboard contrast and add actionable high-usage states with explicit download/upload units.
- Add read-only security status, hardware temperatures/clocks, sampled load balance and shared system check results with verified coverage.
- Add custom image/GIF backgrounds, background blur/dimming and accent-color settings.
- Add grouped CPU/memory process inspection with protected system processes and confirmation before closing an app.
- Recognize third-party antivirus providers and preserve pinned jump lists and in-progress downloads during cleanup.
- Capture original registry values and DNS configuration before changes, verify writes and support restoration.
- Restrict cleanup defaults, keep recent temporary files and report partial results; require separate Recycle Bin confirmation.
- Preserve startup entry scope/type and label driver data as inventory.
- Validate IPC senders and DNS inputs; use a strict PowerShell runner with on-demand elevation.
- Point update publishing to the public distribution repository.
- Add isolated regression tests and document required Windows VM checks before release.

## [1.0.2] - 2026-06-16

### Added
- **Dashboard:** Added a massive 2-column Discord Community Banner alongside the Smart Assistant to drive community growth.
- **Installer:** Added `installer.nsh` to forcefully kill any running Flux.exe instances before uninstallation, guaranteeing a 100% clean wipe.

### Changed
- **Application:** Increased default starting window resolution from `1300x850` to `1350x900` to perfectly showcase the new Dashboard banners without requiring the user to scroll.
- **UI:** Re-engineered the Sidebar circular gauges and text layout to prevent vertical UI jumping/shifting between Idle, Analyzing, and Optimized states.
- **UI:** Replaced the generic CSS spinner on the Dashboard loading screen with a custom, glowing pulse-and-fade animation that matches the app's premium aesthetic.
- **UI:** Added a smooth, continuous "Hyper-Scan" spinning animation to the Sidebar gauges during optimization.
- **UI:** Completely redesigned the Update Banner into a full-screen, blurred modal with animated download progress embedded directly into the download button.

### Fixed
- **UI:** Fixed an issue where the Deep System Optimization in the Sidebar would flash a visible PowerShell window on the screen when requesting administrator privileges.
- **UI:** Fixed the Deep System Scan logic in the Sidebar. The "Optimize" button no longer fakes the score to 100; instead, it performs a genuine background rescan to show your true system health after optimization.
- **UI:** Fixed a bug in the Network page where the live speed graph tooltips incorrectly displayed values as percentages instead of actual speeds (KB/s and MB/s).
- **Performance:** Optimized state management in Backup and Settings pages. Grouped related data updates together to eliminate micro-stuttering and prevent unnecessary UI re-renders, making the app feel snappier.

---

## [1.0.1] - 2026-06-15

### Added
- **Toolbox:** Reset Windows Store Cache — fixes MS Store download issues (`wsreset.exe`)
- **Toolbox:** Reset Network Stack — deep Winsock + TCP/IP reset for stubborn internet problems
- **Tweaks:** Ultimate Performance Power Plan — hidden Windows power plan with zero throttling
- **Tweaks:** Disable Fast Startup — fixes boot issues, dual-boot problems, and forced update installs
- **Tweaks:** Disable Web Search in Start Menu — removes Bing results from Start search
- **Tweaks:** Disable Lock Screen Ads — removes tips, tricks, and spotlight ads from lock screen
- **Settings:** Fully implemented all 4 toggle options that previously had no effect:
  - **Require Administrator:** App will automatically relaunch and request UAC if enabled
  - **Debug Mode:** Automatically opens Chrome DevTools and logs configurations on startup
  - **Action Toasts:** Toggling this setting now correctly hides success notifications
  - **Driver Updates:** Automatically checks for >3 year old drivers 10 seconds after startup and warns via toast
  - **Analytics Opt-in:** Toggle privacy settings for anonymous telemetry
  - **Close to Tray:** App now minimizes to system tray instead of closing completely
  - **Auto-check Updates:** Background update checking toggle
- **Settings:** Added "Reset to Defaults" functionality to restore all preferences to default
- **Settings:** Added "Restart required" red warning labels for settings that need app reload

### Fixed
- Fixed Backup & Restore "Create Restore Point" spawning visible PowerShell windows and hanging
- Bypassed Windows 24-hour restore point limitation (`SystemRestorePointCreationFrequency = 0`)
- Fixed Backup UI aggressively prompting for UAC on page load. Now gracefully displays an "Administrator Privileges Required" banner when running as a normal user.
- Fixed React double-render bug causing duplicate UAC elevation prompts for fetching restore points.
- Fixed app failing to start in development mode due to `start-minimized` configuration.
- Fixed "Start on boot" setting not correctly registering/unregistering the app in the Windows Startup Manager.
- Fixed Restart Graphics crash in Toolbox (broken PowerShell escaping replaced with Base64-encoded command)
- Restart Graphics Driver no longer opens a visible PowerShell window
- Restart Graphics Driver no longer requires administrator privileges (uses native Win+Ctrl+Shift+B shortcut)

### Changed
- UI: Cleaned up Backup & Restore points list icons (removed background, simplified Restore button)
- UI: Improved Settings menu icons (`Eye` for Privacy, `Wrench` for Advanced) and simplified Reset button style

### Changed
- CPU info now shows physical cores and threads (e.g. 6C / 12T)
- Removed ambient glow effect from Dashboard stat cards for a cleaner look

---

## [1.0.0] - 2026-06-13 🎉 First Release

### Added
- Initial public release of Flux Optimizer
- Real-time Dashboard with CPU, GPU, RAM, Disk and Network charts
- Performance Tweaks page
- Junk Cleaner
- Network tools (DNS switcher, ping test)
- Startup Manager
- Windows Update history
- System Toolbox (SFC scan, disk cleanup, GPU/audio restart, etc.)
- Automatic update notifications via GitHub Releases
- Dynamic version number in sidebar (reads from package.json)

# Changelog

All notable changes to Home2Bridge will be documented in this file.

## [1.4.0] - 2026-03-19

### Fixed
- **Plugin update timeout** — Plugin updates now use a dedicated 5-minute timeout session instead of the default 10 seconds. npm install on Raspberry Pi can take 30–300 seconds, causing all updates to silently fail with a timeout error.
- **Plugin update URL with trailing slash** — If the server URL was entered with a trailing slash (e.g. `http://rpi4.local:8581/`), the update request URL contained a double slash (`//api/...`) causing a 404. Fixed by using proper URL path building.
- **Refresh interval not applied immediately** — Changing the refresh interval in Settings now takes effect immediately without requiring a reconnect.
- **Launch at Login toggle infinite loop** — Fixed a potential loop where a failed SMAppService registration/unregistration would repeatedly toggle the setting.

### Changed
- Plugin update requests now use a separate URL session with extended timeouts, keeping regular API calls fast (10s) while allowing plugin installs to complete.

## [1.3.0] - 2026-01-10

### Added
- **Auto-Reconnect After Sleep** — App now automatically reconnects to Homebridge when Mac wakes from sleep
- **Update Checker Restart** — Periodic update check timer restarts automatically after wake
- **Secure Auto-Updates** — Ed25519 signature verification for update packages; SHA-256 hash verification for downloaded DMGs

### Fixed
- App failed to reconnect after Mac sleep/wake cycle
- Update checker timer stopped working after sleep

## [1.2.0] - 2026-01-05

### Added
- **Plugin Update Functionality** - Update individual plugins or all plugins at once directly from the app
- **Update Progress Tracking** - Visual feedback showing which plugin is being updated
- **Restart Wait Logic** - App waits for Homebridge restart after plugin updates and refreshes data automatically
- **Server Status Protection** - Update buttons are disabled when Homebridge server is down

### Changed
- Improved status detection using `isRunning` property (handles both "up" and "ok" status)
- Enhanced connectivity verification after server restart
- Better error handling for plugin update failures

### Fixed
- Fixed "Waiting for restart..." getting stuck when server was already up
- Fixed dashboard not refreshing after plugin updates

## [1.1.0] - 2026-01-05

### Added
- Initial plugin management view with list of installed plugins
- Plugin sorting (updates first, then alphabetical)
- Plugin homepage links
- Disabled plugin indicators

## [1.0.0] - 2026-01-05

### Added
- Initial release
- Menu bar app with Homebridge status monitoring
- Connection settings with server URL, username, and password
- Dashboard overview showing server status, uptime, CPU, and memory
- Auto-refresh every 30 seconds
- Secure credential storage in macOS Keychain
- Automatic update checking with signed releases

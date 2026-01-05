# Changelog

All notable changes to Home2Bridge will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2026-01-05

### Added
- **Notifications System** — Get notified about important Homebridge events:
  - Plugin updates available (click to open Plugins window)
  - Homebridge update available
  - Homebridge UI update available
  - Node.js update available
  - Homebridge down/unresponsive
  - High CPU usage (>80%)
  - Low memory (<20% free)
- **Notifications Settings Tab** — Configure which notifications you want to receive
- Notification cooldown (5 minutes) to prevent spam
- Authorization status display in Settings

### Improved
- Settings window layout and sizing
- Visual alignment of toggle switches
- App icon display in About tab

---

## [1.0.0] - 2026-01-04

### Added
- Initial release
- Menu bar CPU usage display
- Real-time Homebridge status monitoring
- CPU, RAM, and uptime statistics
- Plugin list with update notifications
- Server control (restart Homebridge, restart service, restart/shutdown host)
- Logs viewer
- Config viewer (read-only)
- System information display
- Pairing info with HomeKit PIN
- Settings panel with:
  - Server connection configuration
  - 2FA support
  - Configurable refresh interval (5s, 15s, 30s, 60s)
  - Temperature unit toggle (Celsius/Fahrenheit)
  - Launch at login option
  - Automatic update checks
- Secure credential storage in macOS Keychain
- Ed25519 signature verification for updates
- Universal Binary (Apple Silicon + Intel)

### Security
- Credentials stored in macOS Keychain
- HTTPS support for server connections
- Cryptographic signature verification for updates

---

[1.1.0]: https://github.com/panjakubpl/Home2Bridge/releases/tag/v1.1.0
[1.0.0]: https://github.com/panjakubpl/Home2Bridge/releases/tag/v1.0.0

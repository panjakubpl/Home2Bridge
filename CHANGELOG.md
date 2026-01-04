# Changelog

All notable changes to Home2Bridge will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2025-01-05

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

[1.0.0]: https://github.com/panjakubpl/Home2Bridge/releases/tag/v1.0.0

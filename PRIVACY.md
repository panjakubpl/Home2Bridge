# Privacy Policy

**Last updated: January 2025**

Home2Bridge is designed with privacy as a core principle. This document explains what data the app accesses and how it's handled.

## Data Collection

### What We DON'T Collect

- **No telemetry** — We don't track how you use the app
- **No analytics** — No usage statistics are collected
- **No crash reports** — We don't automatically send crash data
- **No personal information** — We don't collect names, emails, or identifiers
- **No location data** — We don't access your location
- **No browsing history** — We don't track your activity

### What the App Accesses

Home2Bridge only accesses data necessary for its core functionality:

1. **Homebridge Server Data**
   - CPU, memory, and uptime statistics
   - Plugin list and update status
   - Server configuration (read-only)
   - Log files (read-only)
   - Pairing information

2. **Network Access**
   - Communication with your Homebridge server only
   - Update checks to GitHub (can be disabled)

## Data Storage

### Local Storage Only

All data is stored locally on your Mac:

- **Credentials** — Stored securely in macOS Keychain
- **Settings** — Stored in UserDefaults (local preferences)
- **Cached data** — Temporary, cleared on quit

### No Cloud Sync

- Your data is never uploaded to any server
- Your credentials never leave your Mac
- We have no access to your Homebridge server

## Network Communication

### Homebridge Server

- Direct connection to your specified server URL
- Uses your provided credentials
- Supports HTTPS for encrypted connections

### Update Checks

- Checks GitHub for new versions (optional)
- Only downloads version metadata
- Ed25519 signature verification for security
- Can be disabled in Settings

## Third-Party Services

Home2Bridge uses **zero** third-party analytics, tracking, or advertising services.

The only external connections are:
- Your Homebridge server (required)
- GitHub releases API (optional, for updates)

## Your Rights

You have complete control over your data:

- **Access** — All data is stored locally and visible to you
- **Delete** — Uninstalling the app removes all data
- **Disable** — You can disable auto-update checks

## Security Measures

- Keychain storage for credentials (Apple's secure enclave)
- Ed25519 cryptographic signatures for updates
- SHA256 hash verification for downloads
- No plain-text password storage

## Children's Privacy

Home2Bridge does not collect any personal information and is safe for users of all ages.

## Changes to This Policy

We may update this privacy policy from time to time. Changes will be noted in the changelog and the "Last updated" date above.

## Contact

For privacy-related questions, please [open an issue](https://github.com/panjakubpl/Home2Bridge/issues) on GitHub.

---

**Summary**: Home2Bridge collects no personal data, stores everything locally, and only communicates with your Homebridge server and GitHub for updates.

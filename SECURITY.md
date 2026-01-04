# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |

## Security Features

### Credential Storage

- All credentials stored in **macOS Keychain**
- Uses Apple's secure enclave technology
- No plain-text password storage
- Credentials never transmitted except to your Homebridge server

### Update Security

Home2Bridge implements multiple layers of security for updates:

1. **Ed25519 Signatures** — All releases are cryptographically signed
2. **SHA256 Verification** — Downloaded files are hash-verified
3. **HTTPS Only** — Update checks use secure connections
4. **Manual Downloads** — You control when to download and install

### Network Security

- Supports HTTPS connections to Homebridge
- No third-party network connections (except GitHub for updates)
- No data exfiltration or telemetry

### Code Security

- Native Swift/SwiftUI application
- Zero third-party dependencies
- Apple's App Transport Security (ATS) enforced

## Reporting a Vulnerability

If you discover a security vulnerability, please report it responsibly:

1. **DO NOT** open a public issue
2. Email details to: [create a private security advisory](https://github.com/panjakubpl/Home2Bridge/security/advisories/new)
3. Include:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)

### Response Timeline

- **Acknowledgment**: Within 48 hours
- **Initial Assessment**: Within 7 days
- **Fix Timeline**: Depends on severity
  - Critical: 24-72 hours
  - High: 1-2 weeks
  - Medium: 2-4 weeks
  - Low: Next release

## Security Best Practices

When using Home2Bridge:

1. **Use HTTPS** for your Homebridge server when possible
2. **Use strong passwords** for your Homebridge account
3. **Keep macOS updated** for latest security patches
4. **Verify downloads** — only download from official GitHub releases
5. **Enable 2FA** on your Homebridge if supported

## Verification

To verify a downloaded DMG:

```bash
# Check SHA256 hash (compare with version.json)
shasum -a 256 Home2Bridge-x.x.x.dmg
```

The expected hash is published in each release's `version.json`.

## Disclaimer

Home2Bridge is provided "as is" without warranty. While we strive to maintain security, users are responsible for:

- Securing their Homebridge server
- Using secure network connections
- Keeping their systems updated

---

For general support questions, please use [GitHub Issues](https://github.com/panjakubpl/Home2Bridge/issues).

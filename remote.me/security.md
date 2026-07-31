# Remote.Me Security Overview

Last updated: July 31, 2026

Remote.Me is designed for direct Mac-to-Mac sessions on networks the user or
organization controls. Discovery is not authorization: finding a Mac through
Bonjour does not grant access to its screen or input.

## Security boundaries

- The host user must approve an untrusted incoming connection.
- Session key agreement uses ephemeral Curve25519 keys and HKDF-SHA256.
- Session messages are authenticated and encrypted with AES-GCM.
- Capture and remote input remain unavailable until session approval.
- Pairing codes and session secrets must not be written to connection logs.
- macOS separately controls Screen & System Audio Recording and Accessibility.
- Remote.Me cannot silently grant itself macOS privacy permissions.

## Local network model

Remote.Me uses Bonjour/mDNS for discovery and a direct TCP connection for the
session. Bonjour advertisements expose limited discovery metadata to devices on
the same local network. Treat an untrusted Wi-Fi or shared VLAN as hostile and
approve connections only from a recognized Mac.

Remote.Me is not a VPN, firewall, zero-trust gateway, or internet relay. Network
segmentation, firewall policy, endpoint security, device management, and physical
security remain customer responsibilities.

## Secure operation

1. Keep macOS and Remote.Me updated.
2. Use trusted networks and managed network segmentation where appropriate.
3. Approve only expected connection requests and disconnect unknown sessions.
4. Grant Screen Recording and Accessibility only on Macs intended to be hosts.
5. Review connection history and enterprise policy regularly.
6. Remove obsolete identity groups and revoke Microsoft consent when no longer
   required.
7. Avoid exposing the Remote.Me listener directly to the public internet.

## Vulnerability reporting

Follow the repository-wide [Security Policy](../SECURITY.md). Never place exploit
details or secrets in a public support issue.

## Related guidance

- [Network and protocol security](network-and-protocol-security.md)
- [Permissions guide](permissions.md)
- [Data handling and retention](data-handling-and-retention.md)
- [Enterprise security](enterprise-security.md)

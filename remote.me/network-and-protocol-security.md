# Remote.Me Network and Protocol Security

Last updated: July 31, 2026

## Discovery and transport

Remote.Me advertises and browses the `_remoteme._tcp` Bonjour service on the local
network. Bonjour resolves a host and dynamically selected TCP port; it does not
authenticate the peer. RMP performs the session handshake and encryption after the
TCP connection opens.

Enterprise networks may block multicast DNS, isolate wireless clients, or deny
peer-to-peer traffic. Administrators should permit only the required local traffic
between approved network segments. Remote.Me does not require a fixed public port
for local Bonjour operation.

## RMP session protection

The implemented RMP profile exchanges ephemeral Curve25519 public keys, derives a
verification code and 256-bit session key with HKDF-SHA256, and requires host
approval. Subsequent protocol messages are encrypted and authenticated with
AES-GCM. Random nonces, bounded message sizes, sequencing, and session-state checks
are used to reject malformed or out-of-state traffic.

Video compression is not encryption. H.264, HEVC, JPEG, VideoToolbox, and Metal
describe capture, compression, decoding, or presentation; RMP encryption protects
the encoded traffic in transit.

## Administrator checklist

- Keep the listener reachable only from intended LAN/VLAN segments.
- Do not create unrestricted internet-facing port-forwarding rules.
- Preserve mDNS only where discovery is required; use network policy to limit scope.
- Monitor endpoint and firewall events without capturing screen contents or secrets.
- Test connection approval, input permission, disconnect, and revocation behavior.
- Treat host names and local addresses as operational data when exporting logs.

## Limitations

Direct local connectivity does not provide centralized relay controls, DDoS
protection, or a cloud access proxy. Customers needing those controls must supply
them through their network and endpoint architecture.

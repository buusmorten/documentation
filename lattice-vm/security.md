# Lattice-VM Security

Last updated: July 31, 2026

## Current support status

Lattice-VM is an early developer preview with no supported binary release. Security
fixes target the latest development branch. Development builds should be evaluated in
isolated, backed-up environments.

## Report vulnerabilities privately

Use GitHub private vulnerability reporting in the
[Lattice-VM Security tab](https://github.com/buusmorten/Lattice-VM/security). Do not
publish exploit details, guest data, credentials, or unsafe VM images in an issue.

Reports should identify the affected commit, backend, Apple platform, guest type,
impact, reproduction steps, and suggested mitigation. Issues originating in UTM,
QEMU, SPICE, or another dependency may also need to follow the upstream project's
security process.

## Security boundaries

- Virtualization reduces risk but does not make an untrusted guest harmless.
- Shared folders, clipboard, USB, networking, port forwarding, and guest-agent
  commands intentionally expand the guest/host interaction surface.
- Bridged networking can expose a guest directly to the LAN.
- Port forwards can expose guest services to the host, LAN, or internet depending on
  the bind address and surrounding firewall/NAT configuration.
- VM images and snapshots may contain passwords, tokens, personal data, or malware.

Use least privilege, localhost-only forwarding where possible, trusted images,
host/guest patching, network segmentation, encryption, and tested backups.

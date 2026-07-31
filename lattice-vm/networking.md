# Lattice-VM Networking and Exposure

Last updated: July 31, 2026

Network behavior depends on the selected backend, Apple platform, entitlement,
configuration, and host network.

| Mode | Typical behavior | Primary risk |
|---|---|---|
| Shared / NAT | Guest reaches external networks through the host | Outbound guest traffic and explicit forwards |
| Bridged | Guest appears on the physical LAN where supported | Direct LAN exposure |
| Host only | Guest communicates with the host or an isolated host network | Host services and other attached VMs remain reachable |
| Emulated VLAN / isolated | Connectivity exists only within the configured virtual segment | Misconfiguration or later attachment can expand reachability |
| Offline | No configured guest network path | Shared folders, removable media, and other channels still cross boundaries |

Port-forward presets are convenience configuration, not firewall policy. Bind to
localhost unless LAN access is required, authenticate the guest service, and verify
host firewall and router behavior. Wi-Fi bridging and Apple Virtualization capabilities
vary by platform and backend.

The source repository contains the detailed
[networking implementation guide](https://github.com/buusmorten/Lattice-VM/blob/main/Documentation/Networking.md).

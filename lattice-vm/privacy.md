# Lattice-VM Privacy

Last updated: July 31, 2026

Lattice-VM runs and manages virtual machines on the user's Apple device. Virtual disks,
configuration, snapshots, shared folders, clipboard data, USB devices, network traffic,
and guest operating-system activity can contain sensitive information. They are under
the user's control and are not a public documentation service.

The project does not operate an analytics or advertising service for development
builds. Features selected by the user may contact external providers—for example Apple
for macOS restore images, operating-system vendors for installation media, or configured
guest networks and update services. Those providers and guest operating systems apply
their own privacy policies.

Shared directories, clipboard integration, host networking, port forwarding, USB
redirection, and remote connections deliberately cross the host/guest isolation
boundary. Enable only what the workload requires.

Do not submit virtual disks or unredacted logs for support. Remove hostnames, user names,
addresses, file paths, tokens, and guest content before sharing diagnostics.

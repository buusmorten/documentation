# Lattice-VM Data and Backups

Last updated: July 31, 2026

Virtual-machine bundles can include configuration, virtual disks, firmware variables,
snapshots, logs, removable-media references, saved state, and security-sensitive guest
data. Treat a VM bundle like the physical computer it represents.

Before testing Lattice-VM development builds:

1. Shut down the guest cleanly.
2. Back up the complete VM bundle and required external disk images.
3. Verify the backup can be read and that storage is sufficient.
4. Avoid opening the only copy with experimental builds.
5. Protect backups with access control and encryption appropriate to their contents.

Snapshots are not independent backups. Shared host folders and external images may not
be contained inside the VM bundle. Exporting or publishing a VM can disclose operating
system licenses, credentials, browser data, source code, personal information, and
cryptographic keys.

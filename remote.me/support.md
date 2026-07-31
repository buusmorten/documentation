# Remote.Me Support

Remote.Me is developed by Morten Buus.

## Request Support

To ask a question, report a bug, or request help, open a public support request
in the [Remote.Me support tracker](https://github.com/buusmorten/documentation/issues/new?template=support.yml).
A free GitHub account is required to create a request.

Include:

- Remote.Me version and build number
- macOS version on both Macs
- Mac model and processor on both Macs
- Whether each Mac uses Ethernet or Wi-Fi
- Whether both Macs are on the same network or VLAN
- What you expected to happen
- What happened instead
- The exact error message and relevant Connection Log text

Do not include passwords, pairing codes, payment information, private keys,
private screen contents, full public IP addresses, or other credentials.

## Required Permissions

On the Mac being controlled, Remote.Me requires:

- **Screen & System Audio Recording** to share the display
- **Accessibility** to receive keyboard and mouse input
- **Local Network** access to discover and connect to nearby Macs

Open **System Settings → Privacy & Security** to review these permissions. Quit
and reopen Remote.Me after changing a permission.

## Connection Troubleshooting

If a nearby Mac does not appear or a connection fails:

1. Confirm Remote.Me is open on both Macs.
2. Confirm both Macs are connected to the same local network or VLAN.
3. Refresh **Nearby Macs**.
4. Temporarily disconnect VPN software.
5. Check that the network permits Bonjour/mDNS and direct local connections.
6. Check macOS firewall and endpoint-security settings.
7. Review **Network Info**, **Machine Info**, and **Connection Log** in Remote.Me.

Guest Wi-Fi and enterprise networks may isolate devices or block Bonjour. Ask
the network administrator whether peer-to-peer local traffic and mDNS are
allowed.

## Keyboard Or Mouse Control

If screen sharing works but keyboard or mouse control does not:

1. Open **System Settings → Privacy & Security → Accessibility** on the Mac being controlled.
2. Enable Remote.Me.
3. Quit and reopen Remote.Me.
4. Reconnect from the controlling Mac.

macOS requires the user to approve Accessibility permission. Remote.Me cannot
enable it automatically.

## Purchases And Editions

If Remote.Me Pro or Remote.Me Enterprise is not recognized:

1. Open Remote.Me settings.
2. Select **Restore Purchases**.
3. Confirm the Mac is signed in with the Apple Account used for the purchase.
4. Check the internet connection and try again.
5. Quit and reopen Remote.Me.

Purchases are processed by Apple. Remote.Me does not receive or store
payment-card information.

## Privacy And Security

Read the [Remote.Me Privacy Policy](privacy.md).

Remote.Me is designed for direct connections between Macs. Only approve a
connection when you recognize and trust the connecting device.

Remote.Me is an independent remote-desktop application. It is not affiliated
with, endorsed by, sponsored by, or approved by Apple, Microsoft, Google, or
Microsoft Azure.

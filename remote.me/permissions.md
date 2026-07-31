# Remote.Me macOS Permissions

Last updated: July 31, 2026

Remote.Me uses macOS privacy controls. The user must approve protected permissions;
the app can open the relevant System Settings page but cannot enable itself.

## Host Mac

- **Screen & System Audio Recording**: required to transmit the selected display;
  system audio is used only when the active edition and configuration enable it.
- **Accessibility**: required to apply remote keyboard, pointer, click, and scroll
  events to the host.
- **Local Network**: required for Bonjour discovery and direct LAN connections.

## Controlling Mac

Local Network access is required to discover and connect to nearby hosts. Screen
Recording and Accessibility are normally host-side permissions unless that Mac is
also being controlled.

## Review or revoke

Open **System Settings → Privacy & Security**, select the relevant category, and
change Remote.Me access. Quit and reopen Remote.Me after changing protected
permissions. Revoking a required host permission prevents the corresponding
capture or input function.

Grant only the permissions needed for the Mac's intended role.

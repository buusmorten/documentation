# Remote.Me Data Handling and Retention

Last updated: July 31, 2026

## Data flow summary

Remote screen frames and input events travel directly between the approved Macs for
the active session. The developer does not operate a Remote.Me cloud relay that
records session content.

## Stored locally

Depending on use and edition, Remote.Me may store preferences, permission status,
paired-device information, recently connected machines, connection history,
selected enterprise identity groups, policy settings, and purchase-entitlement
status. Connection records can include machine name, local address, port, time,
result, and duration.

Remote screen contents, Microsoft passwords, client secrets, payment-card details,
and pairing secrets are not intended to be stored in connection history.

## Service providers

Apple processes App Store purchases. RevenueCat processes product and entitlement
information needed to provide paid editions. Microsoft processes authentication and
Graph requests during optional Enterprise onboarding. GitHub processes public
support submissions. Each provider applies its own terms and privacy policy.

## Retention and deletion

Local records remain until removed through the app, cleared with app data, or
deleted when the app is removed, subject to macOS behavior and backups. Microsoft
organization access can be revoked in Microsoft Entra. Purchase records are retained
by Apple and RevenueCat under their policies and legal obligations.

Organizations should define their own retention schedule for exported diagnostics,
screenshots, support records, audit material, and device backups.

See the complete [Privacy Policy](privacy.md).

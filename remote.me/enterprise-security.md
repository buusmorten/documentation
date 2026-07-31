# Remote.Me Enterprise Security and Microsoft Entra Setup

Remote.Me is developed by Morten Buus.

This public guide explains how Remote.Me Enterprise connects to Microsoft Entra
ID, which information is used, which information is stored, and how an
administrator can remove access.

## Administrator Setup

Remote.Me uses an app registration created and controlled by the customer's
organization.

1. Create a Microsoft Entra app registration for Remote.Me.
2. Configure `dk.buus.remoteme.app://auth` as a **Mobile and desktop
   applications** redirect URI.
3. Enable public client flows.
4. Add the delegated Microsoft Graph permissions `User.Read` and
   `Group.Read.All`.
5. Export the app-registration JSON manifest.
6. In Remote.Me, open **Settings → Enterprise → Microsoft Entra Setup**.
7. Select **Choose JSON Manifest** and import the exported manifest.
8. Select **Sign in with Microsoft Azure**.
9. Sign in with an administrator who can grant the requested organization
   consent.
10. Review Microsoft's consent page before approving it.
11. Select only the groups that should receive Remote.Me access and assign each
    selected group a Remote.Me role.

Remote.Me validates the Application ID and checks whether the imported manifest
contains the required callback URI. A client secret must not be included in the
manifest or entered into Remote.Me.

## Microsoft Graph Permissions

Remote.Me requests these delegated permissions during administrator setup:

- `User.Read` — identifies the administrator completing setup.
- `Group.Read.All` — lists organization groups so the administrator can choose
  which groups Remote.Me should authorize.

`Group.Read.All` requires administrator consent. Remote.Me does not request
permission to read mail, calendars, files, chats, passwords, authentication
methods, or payment information.

Administrators should review the Microsoft consent screen and the configured
permissions in Microsoft Entra before approving Remote.Me.

## Information Stored Locally

Remote.Me stores only the information required to remember the administrator's
explicit configuration:

- Microsoft Entra Application (client) ID
- App-registration display name, when present in the imported manifest
- Selected group display name
- Selected group's immutable object ID
- Remote.Me role assigned to the selected group
- Remote.Me Enterprise policy settings

This information is stored locally on the Mac in Remote.Me preferences. It is
not uploaded to a Remote.Me organization service.

## Information Not Saved

Remote.Me does not save:

- Microsoft passwords or authentication codes
- Client secrets, certificates, or private keys
- Microsoft access or refresh tokens after the active setup session
- The complete Microsoft Entra directory
- Unselected group memberships
- User mail, calendars, files, chats, or contacts
- Remote screen contents as part of Entra setup
- Payment-card information

The group list returned by Microsoft Graph is held in memory only while the
administrator is completing setup. Remote.Me persists only groups the
administrator explicitly selects.

## Authentication Security

Remote.Me opens Microsoft sign-in using the macOS system authentication
session. Authentication uses the OAuth 2.0 authorization-code flow with PKCE.
Remote.Me verifies the callback state before exchanging an authorization code.

The callback URI is:

`dk.buus.remoteme.app://auth`

The native macOS application is a public client. A client secret must never be
embedded in the app or supplied to Remote.Me.

## Remove Or Revoke Access

To remove a selected group from Remote.Me:

1. Open **Settings → Enterprise → Identity Groups**.
2. Remove the group.

To disconnect the active setup session, select **Disconnect** in Microsoft
Entra Setup.

To revoke organization consent completely:

1. Open the Microsoft Entra admin center.
2. Go to **Identity → Applications → Enterprise applications**.
3. Select the organization's Remote.Me enterprise application.
4. Review or revoke the granted permissions, or delete the enterprise
   application if the organization no longer uses it.

Revoking Microsoft consent prevents future Microsoft Graph access. Locally
saved Remote.Me group selections can then be removed from Enterprise settings.

## Diagnostic And Support Safety

Do not include passwords, access tokens, client secrets, private keys,
authentication codes, complete manifests, or private directory information in
support requests.

Before sharing a screenshot or log, obscure tenant-specific identifiers, user
principal names, group object IDs, hostnames, and IP addresses when they are not
required to understand the problem.

For help, open a public request in the
[Remote.Me support tracker](https://github.com/buusmorten/documentation/issues/new?template=support.yml).
Only provide information that is safe to publish.

## Related Documents

- [Remote.Me Support](support.md)
- [Remote.Me Privacy Policy](privacy.md)
- [Remote.Me Security Overview](security.md)
- [Remote.Me Enterprise Deployment](enterprise-deployment.md)
- [Remote.Me NIS2 Readiness](nis2-readiness.md)
- [Remote.Me Copyright and Third-Party Notices](copyright.md)

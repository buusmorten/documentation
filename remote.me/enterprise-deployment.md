# Remote.Me Enterprise Deployment Guide

Last updated: July 31, 2026

This guide provides a deployment baseline. Organizations must adapt it to their
risk assessment, network architecture, identity policy, and legal obligations.

## Before deployment

1. Identify controlling and host Mac roles and approved network segments.
2. Define owners for application deployment, identity, security, incident response,
   support, and entitlement management.
3. Test Remote.Me in an isolated pilot group using production-like network controls.
4. Document required macOS privacy permissions and whether MDM profiles are allowed
   by Apple and organizational policy.
5. Decide which Microsoft Entra groups receive access and who may administer them.
6. Establish review, revocation, update, logging, and retention procedures.

## Microsoft Entra onboarding

Create a customer-controlled public-client app registration, configure the documented
redirect URI and delegated permissions, export its manifest, then import it through
Remote.Me's guided Enterprise setup. No client secret should be embedded or imported.

See [Enterprise security and Microsoft Entra setup](enterprise-security.md).

## Operational validation

- Verify discovery and connection across each approved VLAN.
- Verify unknown sessions require approval.
- Verify Screen Recording and Accessibility revocation stops the related function.
- Verify identity-group removal and Microsoft consent revocation.
- Verify purchase restoration and entitlement expiration behavior.
- Confirm support exports contain no credentials or screen content.
- Record application version, configuration owner, test evidence, and review date.

## Change and offboarding

Reassess controls after Remote.Me, macOS, identity, firewall, or network changes.
When offboarding, remove group assignments, revoke Microsoft consent if appropriate,
remove local organization configuration, terminate active sessions, and preserve only
records required by organizational policy or law.

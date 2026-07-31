# Remote.Me NIS2 Readiness and Responsibility Matrix

Last updated: July 31, 2026

## Scope and disclaimer

This document helps organizations evaluate Remote.Me as one component of their
cybersecurity controls. It is not legal advice, a certification, an attestation, or a
claim that Remote.Me—or its use—makes an organization NIS2 compliant.

NIS2 obligations apply to covered entities, not to an application in isolation.
Organizations must determine scope with their competent authority and advisers. In
Denmark, the NIS 2 Act entered into force on July 1, 2025.

## Responsibility matrix

| NIS2 risk area | Remote.Me contribution | Customer responsibility |
|---|---|---|
| Risk analysis and system security | Public security, protocol, permissions, and deployment documentation | Classify systems, assess risk, approve architecture, and maintain policies |
| Incident handling | Connection history and privacy-safe troubleshooting information | Operate detection, triage, escalation, evidence, notification, and response procedures |
| Business continuity | Sessions disconnect without depending on a Remote.Me content relay | Define backup, recovery, crisis management, alternate access, and availability plans |
| Supply-chain security | Documents Apple, RevenueCat, Microsoft, and platform dependencies | Assess suppliers, contracts, updates, dependencies, and concentration risk |
| Secure acquisition and maintenance | Signed App Store distribution and documented update expectations | Control procurement, testing, patching, vulnerability handling, and asset inventory |
| Control effectiveness | Deployment validation checklist | Test controls, retain evidence, audit, and remediate findings |
| Cyber hygiene and training | Explicit approval and permission model; safe support guidance | Train users and administrators; enforce device and credential hygiene |
| Cryptography | RMP session key agreement and authenticated encryption | Approve cryptographic requirements and manage network/endpoint controls |
| Access control and asset management | Host approval plus optional selected Entra groups | Own identities, group lifecycle, least privilege, device inventory, and periodic access review |
| MFA and secure communications | Microsoft sign-in follows customer Entra configuration; RMP protects session traffic | Enforce MFA/Conditional Access where applicable and protect administrator accounts |

## Evidence pack to maintain

- Remote.Me version and deployment scope;
- current risk assessment and approval owner;
- network diagram and allowed traffic;
- macOS permission and device-management policy;
- Microsoft app registration, consent, and selected-group review records;
- update, vulnerability, incident, continuity, and supplier procedures;
- validation results and remediation decisions; and
- retention schedule for logs, diagnostics, and support records.

Do not store secrets or unnecessary personal data in the evidence pack.

## Incident reporting

Remote.Me cannot determine whether an event is a reportable NIS2 incident or submit
regulatory notifications for the customer. Covered organizations must maintain their
own classification and notification procedure, including the timelines and competent
authority applicable to their sector and jurisdiction.

## Official sources

- [Directive (EU) 2022/2555 (EUR-Lex)](https://eur-lex.europa.eu/eli/dir/2022/2555/oj)
- [European Commission NIS2 overview](https://digital-strategy.ec.europa.eu/en/policies/nis2-directive)
- [Danish NIS 2 Act, Act no. 434 of May 6, 2025](https://www.retsinformation.dk/eli/lta/2025/434)
- [Danish Agency for Societal Security NIS2 guidance](https://samsik.dk/nis2/hvad-er-nis-2/)

Customers should use the latest official sector guidance because requirements,
interpretation, and competent authorities may change.

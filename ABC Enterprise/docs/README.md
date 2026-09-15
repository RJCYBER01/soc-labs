# ABC Enterprise — Technical Evidence Guide

This directory organizes the technical evidence for the ABC Enterprise enterprise-security home lab. Public evidence is intentionally curated: screenshots are included only when they support a specific implemented control, configuration, validation step, or observed result.

## Evidence Areas

| Area | What the evidence demonstrates |
|---|---|
| Infrastructure | Windows Server/domain-controller deployment and installed server roles |
| Networking | Lab network configuration and controlled service-exposure validation |
| Active Directory | Domain services, workstation domain membership, directory structure, and validation |
| IAM Delegation | Security-group membership and delegated directory permissions |
| GPO Hardening | Password, lockout, account, interactive-logon, and firewall policy configuration/verification |
| Sysmon | Endpoint process telemetry and Sysmon service/installation validation |
| Windows Events | Native successful and failed Windows authentication events |
| Wazuh | Active Windows agents, centralized event visibility, and SCA measurements |
| Attack Validation | Resultant-policy and Nmap validation performed inside the authorized lab |

## Evidence Interpretation

Screenshots are supporting evidence, not a substitute for technical context. Documentation distinguishes between configuration, observed events, and conclusions that can actually be supported by the evidence.

Examples of these boundaries include:

- An Nmap result documents exposed services; it does not by itself demonstrate exploitation.
- A built-in Wazuh rule definition documents the rule's existence; it does not prove the rule fired during an attack.
- A Windows Event Viewer failed-logon event does not by itself prove that the same event reached Wazuh.
- A later SCA score higher than the baseline demonstrates measurable change, but screenshots alone do not attribute every changed benchmark item to one specific GPO or remediation.

## Public Screenshot Standard

Only sanitized copies of selected evidence are intended for this repository. Originals remain outside the public portfolio.

Before publication, evidence is reviewed for passwords, authentication/recovery secrets, QR or 2FA enrollment material, personal usernames, email/account information, MAC addresses, unique SIDs/GUIDs, host-machine paths, unnecessary IP information, and other sensitive identifiers.

## Screenshot Structure

```text
screenshots/
├── infrastructure/
├── networking/
├── active-directory/
├── iam-delegation/
├── gpo-hardening/
├── sysmon/
├── windows-events/
├── wazuh/
└── attack-validation/
```

The screenshot directories will contain only reviewed and sanitized public evidence.

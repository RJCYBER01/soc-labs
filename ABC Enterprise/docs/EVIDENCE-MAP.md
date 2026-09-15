# ABC Enterprise — Public Evidence Map

This map defines the curated evidence planned for the public ABC Enterprise case study. Image filenames below refer to sanitized public copies, not the original screenshot archive.

## README Highlights

The following ten images are intended to provide the strongest high-level visual evidence for the flagship project:

1. `active-directory/windows11-domain-membership-verified.png` — verifies the Windows 11 workstation is joined to the lab domain.
2. `gpo-hardening/password-policy-winning-gpo.png` — shows resultant policy and the winning password-policy GPO.
3. `gpo-hardening/server-sca-score-34-percent.png` — later Windows Server SCA measurement.
4. `gpo-hardening/server-sca-baseline-26-percent.png` — earlier Windows Server SCA baseline for comparison.
5. `iam-delegation/delegated-ou-permissions-verified.png` — directory permissions used to validate delegated OU access.
6. `iam-delegation/department-organizational-units.png` — department-based Active Directory OU structure.
7. `infrastructure/domain-controller-server-roles.png` — Windows Server role evidence for AD DS/DNS.
8. `sysmon/sysmon-event-1-process-creation.png` — Sysmon Event ID 1 process-creation telemetry.
9. `wazuh/windows-and-dc-agents-active.png` — active Windows workstation and domain-controller Wazuh agents.
10. `wazuh/security-events-dashboard.png` — centralized Wazuh security-event dashboard view.

## Detailed Evidence

### Infrastructure

- `domain-controller-snapshot.png`
- `domain-controller-server-roles.png`

### Networking

- `domain-controller-static-ipv4-dns.png`

### Active Directory

- `domain-promotion-prerequisites-passed.png`
- `domain-controller-discovery.png`
- `dcdiag-server-tests.png`
- `dcdiag-partition-tests.png`
- `windows11-domain-membership-verified.png`
- `workstation-ou-verified.png`

### IAM Delegation

- `delegated-ou-permissions-verified.png`
- `department-group-membership.png`
- `department-organizational-units.png`
- `sales-security-group-members.png`

### GPO Hardening

- `account-lockout-policy-configured.png`
- `password-policy-configured.png`
- `password-policy-winning-gpo.png`
- `interactive-logon-winning-gpo.png`
- `account-hardening-resultant-policy.png`
- `guest-account-disabled-verified.png`
- `server-sca-score-34-percent.png`
- `windows-firewall-policy-overview.png`
- `firewall-winning-gpo.png`
- `server-sca-baseline-26-percent.png`

### Sysmon

- `sysmon-event-1-process-creation.png`
- `sysmon-installation-service-verified.png`

### Windows Events

- `event-4624-successful-logon.png`
- `event-4625-failed-logon.png`

### Wazuh

- `windows-and-dc-agents-active.png`
- `windows-agent-service-running.png`
- `security-events-dashboard.png`
- `windows-logoff-rule-60137.png`

### Attack Validation

- `workstation-resultant-policy.png`
- `nmap-domain-controller-scan.png`
- `nmap-workstation-scan.png`

## Publication Rules

The evidence set must not expose passwords, Wazuh authentication keys, recovery codes, QR/2FA secrets, personal account data, or other authentication material. Personal usernames and unnecessary IP/MAC/SID/GUID/path information must be masked in public copies.

Synthetic lab resources may be discussed in documentation when they are necessary to explain the architecture, but screenshots still follow the conservative sanitization standard.

## Claims Deliberately Excluded

Until separately verified, this evidence map does not claim completed pfSense deployment, AWS/IAM deployment, BloodHound attack-path analysis, successful exploitation, or custom Wazuh detections. Those capabilities require their own implementation evidence before being added to the completed project scope.

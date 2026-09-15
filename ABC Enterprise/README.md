# ABC Enterprise — Enterprise Cybersecurity Home Lab

> **Status:** Active portfolio project — documented features below are limited to work supported by lab evidence.

ABC Enterprise is an isolated enterprise-style cybersecurity home lab built to develop practical skills across Windows infrastructure, identity and access management, endpoint telemetry, security monitoring, hardening, and validation.

The project is designed as a growing defensive-security environment rather than a collection of disconnected exercises. It demonstrates how core enterprise technologies interact and provides a foundation for future cloud and IAM security work.

## Current Evidence-Based Scope

The current documented environment includes:

- Windows Server domain controller
- Active Directory Domain Services (AD DS)
- DNS
- Department-based Organizational Units (OUs)
- Security groups and group membership
- Windows 11 domain-joined workstation
- Group Policy password, account-lockout, account-hardening, interactive-logon, and Windows Firewall settings
- Delegated Active Directory permissions
- Sysmon endpoint telemetry
- Windows Security Event Logs
- Wazuh endpoint agents and security-event monitoring
- Security Configuration Assessment (SCA) baseline and later hardening measurement
- Nmap-based service-exposure validation inside the isolated lab

## Architecture Direction

```text
                     ABC Enterprise Lab

                 +-----------------------+
                 | Windows Server / DC   |
                 | AD DS + DNS           |
                 +-----------+-----------+
                             |
                 +-----------+-----------+
                 | Windows 11 Endpoint   |
                 | GPO + Sysmon          |
                 +-----------+-----------+
                             |
                 +-----------+-----------+
                 | Wazuh Monitoring      |
                 | Security Events / SCA |
                 +-----------------------+
```

This diagram represents the currently evidenced core. Network segmentation, pfSense, additional Linux/security services, cloud integration, and more advanced detection engineering remain expansion areas and will be documented only after implementation is verified.

## What This Project Demonstrates

### Identity & Active Directory

The lab demonstrates domain-controller deployment, directory organization, department OUs, security groups, Windows workstation domain membership, and delegated directory permissions.

### Windows Security Hardening

Group Policy is used to configure and verify password policy, account lockout, account hardening, interactive-logon controls, and Windows Firewall policy. Resultant-policy evidence is used where available to distinguish configured policy from policy actually applied to the endpoint.

### Endpoint Visibility

Sysmon provides process telemetry on Windows systems, while native Windows Security logs provide authentication evidence such as successful and failed logon events.

### Security Monitoring

Windows endpoints are enrolled as active Wazuh agents. Wazuh provides centralized security-event visibility and Security Configuration Assessment data for the lab.

### Hardening Measurement

The Windows Server security benchmark was captured at two points during the lab: an initial 26% score and a later 34% score. This is presented as evidence of iterative hardening progress, not as proof that every individual benchmark change was caused by one specific configuration action.

### Validation

Nmap scans are used inside the authorized isolated environment to document exposed TCP services on the domain controller and workstation. These scans demonstrate service-exposure validation; they are not represented as exploitation or proof of SIEM detection.

## Evidence & Screenshots

A curated public evidence set is being prepared from the original lab archive. Only screenshots that materially support the project will be published.

Before publication, screenshots are reviewed for credentials and sensitive information. Passwords, authentication keys, recovery codes, QR/2FA secrets, personal usernames, email/account information, MAC addresses, unique identifiers, host-machine paths, and unnecessary IP information are removed or masked. Original evidence remains unchanged; only sanitized copies are intended for this public repository.

Planned evidence categories:

```text
docs/screenshots/
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

## Important Scope Boundaries

The current evidence set does **not** support claiming the following as completed ABC Enterprise capabilities:

- completed pfSense configuration
- completed AWS/IAM deployment
- completed BloodHound attack-path analysis
- successful exploitation based solely on Nmap scan results
- custom Wazuh detection based solely on viewing a built-in Wazuh rule definition

These may become future project phases, but they will be added to the completed scope only when implementation and evidence support the claim.

## Security & Responsible Use

ABC Enterprise is an isolated home-lab environment created for authorized defensive-security learning. Test identities and the `abcenterprise.local` namespace are synthetic lab resources. Security testing is limited to systems controlled for the lab.

## Project Direction

ABC Enterprise is intended to evolve from enterprise cybersecurity foundations toward deeper networking, IAM, cloud security, detection engineering, and eventually AI-security-related controls. New capabilities will be documented incrementally so the repository remains evidence-based.

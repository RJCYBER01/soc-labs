# Ravi Puri — Cybersecurity Portfolio

The source repository for [ravicyberops.com](https://ravicyberops.com), Ravi Puri's minimalist cybersecurity portfolio and SOC investigation lab.

## Portfolio pages

- Home
- About
- Certifications
- Skills
- Projects
- Learning Journey
- Contact

## Published investigation

### Windows Intrusion Investigation

An evidence-led reconstruction of a Windows compromise covering:

- Brute-force RDP activity and successful remote access
- Attacker-session correlation using Logon IDs
- Backdoor account creation and group-membership changes
- Malware delivery and Startup-folder persistence
- Command-and-control traffic identified through Sysmon

**Tools used:** Windows Event Viewer, Windows Security Event Logs, and Sysmon.

- [Read the web case study](https://ravicyberops.com/log-analysis/windows-logging-for-soc/)
- [View the investigation files](./log-analysis/windows-logging-for-soc/)

## Portfolio focus

- SOC operations and alert triage
- Windows security and event correlation
- Threat detection and incident investigation
- Azure security
- Python and PowerShell security automation

## Deployment

The `main` branch deploys through Vercel to `ravicyberops.com`. The `www` hostname permanently redirects to the apex domain.

## Responsible-use statement

All investigations documented here were completed in authorized training environments. Findings are shared for defensive education and professional portfolio purposes.

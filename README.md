# Ravi CyberOps — Cybersecurity Portfolio

Hands-on cybersecurity portfolio focused on **enterprise security foundations, identity and access management, endpoint visibility, security monitoring, and cloud-security progression**.

Every published project is evidence-based. Technologies, screenshots, findings, and security claims are included only when they reflect work actually completed in an authorized lab or training environment.

---

## Flagship Project — ABC Enterprise

**ABC Enterprise** is an isolated enterprise-style cybersecurity home lab built to connect Windows infrastructure, Active Directory, IAM concepts, endpoint telemetry, hardening, monitoring, and security validation into one evolving environment.

### Current documented capabilities

- Windows Server domain controller with AD DS and DNS
- Department OUs, security groups, and delegated directory permissions
- Windows 11 domain membership
- Group Policy security hardening and resultant-policy validation
- Sysmon endpoint telemetry
- Windows authentication event analysis
- Wazuh agents, security-event visibility, and SCA measurement
- Nmap service-exposure validation inside the isolated lab

**[View the ABC Enterprise technical documentation](./ABC%20Enterprise/)**

The project will expand toward networking, IAM, cloud security, detection engineering, and later AI-security controls. Future capabilities are not presented as completed until implementation is verified.

---

## Additional Completed Labs

| Project | Focus | Documentation |
|---|---|---|
| Windows Intrusion Investigation | Windows event-log analysis, Sysmon, incident reconstruction | [Case study](./log-analysis/windows-logging-for-soc/) |
| Building My Cybersecurity Home Lab | VPN connectivity, scanning, packet-analysis setup, PowerShell | [Documentation](./projects/home-lab/) |
| Hack The Box — Meow | Reconnaissance, Nmap, Telnet enumeration | [Documentation](./projects/htb-meow/) |
| Hack The Box — Fawn | FTP enumeration, anonymous access, file retrieval | [Documentation](./projects/htb-fawn/) |

These smaller labs support specific foundational skills. ABC Enterprise is the primary integrated portfolio project.

---

## Skills Demonstrated in Published Work

**Enterprise / Identity** — Windows Server, Active Directory, Group Policy, DNS, security groups, delegated permissions, domain-joined endpoints

**Endpoint / Detection** — Windows Security Event Logs, Sysmon, Wazuh, Security Configuration Assessment

**Networking / Validation** — TCP/IP fundamentals, Nmap, Wireshark, service exposure analysis

**Security Practice** — system hardening, authentication-event analysis, evidence validation, defensive documentation

---

## Documentation Standard

Projects are written to answer six practical questions:

1. What was the objective?
2. What environment was used?
3. Which technologies were actually implemented?
4. What methodology was followed?
5. What evidence supports the result?
6. What was learned or should be improved next?

Screenshots intended for public portfolio use are reviewed before publication. Credentials, authentication secrets, recovery codes, personal identifiers, unnecessary network identifiers, and other sensitive information are excluded or sanitized.

---

## Repository Map

```text
soc-labs/
├── ABC Enterprise/          # Flagship enterprise cybersecurity lab
│   ├── README.md
│   └── docs/screenshots/    # Sanitized evidence set (being prepared)
├── projects/
│   ├── home-lab/
│   ├── htb-meow/
│   └── htb-fawn/
├── log-analysis/
│   └── windows-logging-for-soc/
└── index.html
```

Existing project paths are being preserved during the portfolio rebuild so material can be reviewed before any consolidation or retirement.

---

## Responsible Use

All labs and investigations documented in this repository were completed in authorized learning environments. The material is published for defensive cybersecurity education, skill development, and professional portfolio purposes.

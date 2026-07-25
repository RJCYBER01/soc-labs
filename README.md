# Ravi CyberOps — Cybersecurity Portfolio

This repository contains the source files and technical documentation for [ravicyberops.com](https://ravicyberops.com).

Every published project represents hands-on work completed in an authorized learning environment. The portfolio is intentionally evidence-based: tools, skills, screenshots, and reports are included only when they reflect work actually completed.

---

## Completed Projects

| Project | Focus | Documentation | Live Page |
|---|---|---|---|
| Building My Cybersecurity Home Lab | VPN connectivity, scanning, packet-analysis setup, PowerShell | [README](./projects/home-lab/) | [View page](https://ravicyberops.com/projects/home-lab/) |
| Hack The Box — Meow | Reconnaissance, Nmap, Telnet enumeration | [README](./projects/htb-meow/) | [View page](https://ravicyberops.com/projects/htb-meow/) |
| Hack The Box — Fawn | FTP enumeration, anonymous access, file retrieval | [README](./projects/htb-fawn/) | [View page](https://ravicyberops.com/projects/htb-fawn/) |
| Windows Intrusion Investigation | Windows event-log analysis, Sysmon, incident reconstruction | [README](./log-analysis/windows-logging-for-soc/) | [View case study](https://ravicyberops.com/log-analysis/windows-logging-for-soc/) |

---

## Tools Used in Published Work

- Windows 11
- Windows PowerShell
- OpenVPN
- Nmap
- Wireshark
- Windows Event Viewer
- Windows Security Event Logs
- Sysmon

---

## Project Documentation Standard

Each project is designed to answer six practical questions:

1. What was the objective?
2. What environment was used?
3. Which tools were actually used?
4. What methodology was followed?
5. What was the outcome?
6. What was learned?

Project folders use a consistent structure where the supporting material exists:

```text
project-name/
├── README.md      # GitHub technical documentation
├── index.html     # Live portfolio presentation
├── report.pdf     # Detailed report when available
└── images/        # Original screenshots and evidence
```

A reusable documentation template is available in [`templates/project-documentation`](./templates/project-documentation/).

---

## Repository Map

```text
soc-labs/
├── projects/
│   ├── home-lab/
│   ├── htb-meow/
│   └── htb-fawn/
├── log-analysis/
│   └── windows-logging-for-soc/
├── templates/
│   └── project-documentation/
└── index.html
```

The current paths are being kept stable so existing portfolio links continue to work. Future projects will follow the same documentation standard without claiming unfinished work.

---

## Responsible Use

All labs and investigations documented here were completed in authorized training environments. The material is shared for defensive education, skill development, and professional portfolio purposes.

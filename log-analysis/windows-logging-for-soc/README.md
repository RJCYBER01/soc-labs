# Windows Intrusion Investigation — Log Analysis Lab

This lab focuses on analyzing security logs to identify suspicious activity, correlate events, and determine whether an incident requires escalation.

**Tools used:** Windows Event Viewer, Sysmon, Windows Security Event Logs

**Platform:** TryHackMe — *Windows Logging for SOC*

---

## Overview

This project documents a full incident investigation performed against two Windows event log files (`Practice-Security.evtx` and `Practice-Sysmon.evtx`), reconstructing an end-to-end intrusion: a brute-force RDP compromise, backdoor account creation, privilege escalation, malware delivery via a browser download, persistence, and command-and-control (C2) communication.

All analysis was performed manually in Windows Event Viewer using event filtering, field-level correlation (Logon IDs, SIDs), and Sysmon telemetry — no automated SIEM tooling was used for this exercise.

---

## Attack Chain Reconstructed

| Stage | Finding |
|---|---|
| **1. Initial Access** | Brute-force RDP attack from `10.10.53.248` — 14 failed logons (Event ID 4625) in ~4 seconds |
| **2. Compromise** | Successful RDP logon as `Administrator` (Event ID 4624, Logon Type 10), Logon ID `0x183c36d` |
| **3. Backdoor Account** | New local account `svc_sysrestore` created under the same attacker session (Event ID 4720) |
| **4. Privilege Escalation** | Backdoor account added to `Backup Operators` and `Remote Desktop Users` (Event ID 4732) |
| **5. Malware Delivery** | User downloaded `ckjg.exe` via Google Chrome from `gettsveriff.com` (Sysmon Event IDs 1, 15) |
| **6. Persistence** | Malware dropped a `.url` shortcut in the Startup folder for auto-execution on login (Sysmon Event ID 11) |
| **7. Command & Control** | Malware connected to `193.46.217.4:7777`, resolving to `hkfasfsafg.click` (Sysmon Event ID 3) |
| **8. Post-Exploitation** | PowerShell history showed reconnaissance (`Get-ComputerInfo`) and a recovered incident flag |

---

## Methodology

1. **Authentication analysis** — Filtered the Security log for Event ID `4625` to identify brute-force patterns, then pivoted to `4624` to locate the successful RDP logon by checking the `LogonType` field (`10` = RemoteInteractive).
2. **Session correlation** — Used the compromised session's `Logon ID` to trace every subsequent action performed by the attacker: account creation (`4720`) and group membership changes (`4732`), confirming a single continuous attacker session.
3. **Malware forensics** — Used Sysmon `Process Create` (Event ID 1) and `FileCreateStreamHash` (Event ID 15) events to identify the malicious download, its source browser, and origin URL via the Zone.Identifier alternate data stream.
4. **Network analysis** — Filtered Sysmon `NetworkConnect` events (Event ID 3) to identify the malware's outbound C2 connection and destination IP/port.
5. **Post-incident review** — Reviewed PowerShell command history across local user profiles to identify attacker reconnaissance activity and recover an embedded flag.

---

## Key Skills Demonstrated

- Windows Security Event Log analysis (authentication, account management)
- Sysmon-based endpoint telemetry analysis (process creation, file creation, network connections, DNS)
- Event correlation using Logon IDs and Security Identifiers (SIDs)
- Identification of common privilege-escalation techniques (e.g., abuse of the Backup Operators group)
- Malware delivery and persistence mechanism analysis
- C2 infrastructure identification

---

## Reference

- SANS Internet Storm Center — [Sysmon and Alternate Data Streams](https://isc.sans.edu/diary/Sysmon+and+Alternate+Data+Streams/26292)
- TryHackMe Room: [Windows Logging for SOC](https://tryhackme.com/room/windowsloggingforsoc)

---

📄 **[View the full investigation report with screenshots (PDF)](./report.pdf)**

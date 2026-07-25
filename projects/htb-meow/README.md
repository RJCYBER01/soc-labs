# Hack The Box — Meow

This beginner Hack The Box machine was completed by connecting to the HTB network, scanning the assigned target, identifying Telnet, and accessing the authorized lab system through the exposed service.

**Status:** Completed  
**Difficulty:** Beginner  
**Platform:** Hack The Box Starting Point

---

## Objective

Use a structured reconnaissance workflow to identify an accessible service on the assigned training target and complete the machine without relying on guesswork.

## Tools Used

- OpenVPN
- Nmap
- Windows PowerShell
- Telnet

## Methodology

1. **Connected to the lab** — Established the Hack The Box VPN connection using OpenVPN.
2. **Confirmed the target** — Used the assigned target IP from the HTB Starting Point environment.
3. **Scanned the target** — Ran an Nmap service-version scan from Windows PowerShell.

```powershell
nmap -sV TARGET_IP
```

4. **Identified Telnet** — The scan showed Telnet available on TCP port 23.
5. **Connected to the service** — Used a Telnet client to access the authorized training machine and followed the lab prompts.
6. **Verified completion** — Located the required proof and submitted it through Hack The Box. The proof value and target IP are intentionally omitted from this public write-up.

## Skills Demonstrated

- VPN connectivity
- Port scanning
- Service identification
- Command-line navigation
- Basic remote access
- Structured lab documentation

## Security Takeaway

Telnet is a legacy protocol that does not protect traffic like modern secure alternatives. Exposed Telnet services can create serious risk and should be replaced with secure remote-access protocols.

## Lessons Learned

Reconnaissance comes first. A simple Nmap scan can reveal the exact service that should be investigated.

---

[View the live portfolio page](https://ravicyberops.com/projects/htb-meow/)

# Hack The Box — Fawn

This beginner Hack The Box machine was completed by identifying an exposed FTP service, testing anonymous access, enumerating the available files, and retrieving the required proof in an authorized lab environment.

**Status:** Completed  
**Difficulty:** Beginner  
**Platform:** Hack The Box Starting Point

---

## Objective

Identify an exposed network service on the assigned training machine, evaluate its access controls, and retrieve the required proof through a structured workflow.

## Tools Used

- OpenVPN
- Nmap
- Windows PowerShell
- FTP client

## Methodology

1. **Connected to Hack The Box** — Established the OpenVPN tunnel and confirmed access to the assigned lab network.
2. **Scanned the target** — Ran an Nmap service-version scan from PowerShell.

```powershell
nmap -sV TARGET_IP
```

3. **Identified FTP** — The scan revealed FTP listening on TCP port 21.
4. **Tested access controls** — Connected to the FTP service and tested the anonymous account permitted by the lab configuration.

```text
ftp TARGET_IP
Username: anonymous
```

5. **Enumerated available files** — Listed the remote directory contents and identified the file containing the required proof.

```text
dir
get FLAG_FILE
```

6. **Retrieved and verified the proof** — Downloaded the file locally and read it from the Windows environment. The proof value and target IP are intentionally omitted from this public write-up.

## Skills Demonstrated

- Network reconnaissance
- Service enumeration
- FTP navigation
- Anonymous-access testing
- Command-line file retrieval
- Structured documentation

## Security Takeaway

Anonymous FTP access can expose sensitive files to anyone who can reach the service. Organizations should disable anonymous authentication unless it is explicitly required, restrict network exposure, and use secure transfer protocols.

## Lessons Learned

This lab reinforced a repeatable sequence: connect, scan, identify, test, enumerate, retrieve, and document.

---

[View the live portfolio page](https://ravicyberops.com/projects/htb-fawn/)

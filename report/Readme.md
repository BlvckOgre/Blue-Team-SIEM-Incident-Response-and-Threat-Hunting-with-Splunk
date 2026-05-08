# Detailed Report – Blue Team SIEM Investigation Using Splunk

## Executive Summary
This project focused on a Blue Team SIEM investigation using Splunk to identify and analyze malicious activity across a Windows environment. The investigation mapped the attack lifecycle from initial compromise through persistence, credential theft, and data exfiltration.

## Objectives
- Perform threat hunting using Splunk
- Identify IOCs
- Correlate malicious activity
- Map attacker behavior
- Investigate persistence and exfiltration

## Key Investigation Areas

### Baseline Analysis
Used SPL queries to enumerate all process activity and identify suspicious executables.

### IOC Correlation
Correlated malicious processes with:
- User accounts
- PIDs
- Commands
- Timestamps

### LOLBin Abuse
Detected attacker use of certutil.exe to download payloads.

### Persistence
Identified br0298.exe launched from C:\Windows\Temp.

### Credential Theft
Detected:
- SAM hive dumping
- SYSTEM hive dumping

### Data Exfiltration
Sensitive files compressed into de.zip for exfiltration.

## Skills Demonstrated
- Threat Hunting
- SIEM Analysis
- Splunk SPL
- Incident Response
- IOC Correlation
- Blue Team Operations

## Conclusion
This project strengthened practical cybersecurity skills in SIEM investigations, log correlation, and incident response while demonstrating the ability to document and analyze a complete attack chain.

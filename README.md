# Blue-Team-SIEM-Incident-Response-and-Threat-Hunting-with-Splunk

## Project Overview
This project demonstrates a hands-on Blue Team investigation using Splunk SIEM within a Windows environment. The objective was to identify malicious activity, correlate indicators of compromise (IOCs), and document the complete attack lifecycle from initial compromise to data exfiltration.

![Project Architecture](./Screenshots/arch.png)

## Tools Used
- Splunk SIEM
- Windows Dataset
- SPL (Search Processing Language)
- CSV Log Parsing
- PowerShell & CMD

## Investigation Workflow

### 1. Data Preparation
- Converted `.pml` capture into `.csv`
- Imported logs into Splunk
- Verified indexing

### 2. Baseline Process Analysis
- Enumerated all running processes
- Identified suspicious executables:
  - br0298.exe
  - SJi8hednh12.exe
  - passed.exe

### 3. IOC Correlation
- Correlated:
  - Users
  - Timestamps
  - PIDs
  - Paths
  - Commands

### 4. User Pivoting
- Pivoted investigation to:
  - USERNAME=helpdesk

### 5. Payload Delivery
- Identified LOLBin abuse:
  - certutil.exe
- External C2:
  - 54.237.236.103:443

### 6. Persistence & Exploitation
- Windows Defender disabled
- Payload staged in:
  - C:\Windows\Temp

### 7. Credential Theft & Exfiltration
- SAM & SYSTEM hive dumping detected
- Sensitive files compressed into:
  - de.zip

## Key Findings
- LOLBin abuse using certutil.exe
- Windows Defender disablement
- Persistent C2 communication
- Credential dumping activity
- Data exfiltration staging

## Lessons Learned
- Practical SIEM threat hunting
- IOC correlation techniques
- SPL query writing
- Kill chain mapping
- Windows process analysis
- Incident response methodology
- Threat detection and pivoting

## Next Steps
- Integrate Sysmon logs
- Build automated detections
- Explore Sigma rules
- Expand into malware analysis

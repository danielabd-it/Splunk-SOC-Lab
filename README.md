# SOC Detection & Incident Response Homelab

A cybersecurity homelab for practicing SOC monitoring, detection, and incident response in an isolated Active Directory environment.

## Lab

- Windows Server 2016 — Domain Controller
- Windows 11 — Workstation
- Ubuntu — Splunk, Zeek, Suricata
- Kali Linux — Attack simulation

## Tools

- Splunk
- Sysmon
- Zeek
- Suricata
- Python
- MITRE ATT&CK
- Active Directory

## Attack Scenarios

- Password spraying
- Encoded PowerShell
- Command-and-control beaconing
- Kerberoasting
- Lateral movement
- Privilege escalation
- Persistence
- Event log clearing
- Data staging and exfiltration

## Detection

A custom Python tool analyzes exported security logs and identifies suspicious activity such as:

- Password attacks
- Kerberoasting
- PowerShell activity
- Scheduled tasks
- Account changes
- Log clearing
- Data staging
- File uploads
- Network beaconing
- Large outbound transfers

## Status

**Work in Progress**

The lab and detection pipeline are still being built and tested. Live telemetry validation, attack scenarios, detections, and documentation are not yet complete.

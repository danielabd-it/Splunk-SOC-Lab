# Splunk SOC Homelab

A hands-on cybersecurity homelab built to simulate a small enterprise Active Directory environment and practice security monitoring, log collection, SIEM investigation, and detection of credential-based attacks.

This lab was implemented as a **controlled password-spray simulation** against a Windows Active Directory domain. Windows Security Event Logs were centralized into **Splunk**, where the resulting failed authentication activity was investigated and correlated to identify suspicious login behaviour.

## Project Overview

The goal of this project was to build a small enterprise-style environment that could generate realistic security telemetry and provide hands-on experience investigating attacks from the defender's perspective.

The lab consists of:

- **DC01** — Windows Server 2016 / Active Directory Domain Controller
- **WS01** — Windows 11 domain-joined workstation
- **SIEM01** — Ubuntu Server running Splunk
- **KALI01** — Kali Linux attack/testing workstation

# Detection Scenario: Password Spray

<img width="1640" height="892" alt="Screenshot 2026-10-16 050408" src="https://github.com/user-attachments/assets/7bbbb218-f49f-4ff9-aad1-7fdea23b984b" />

**MITRE ATT&CK:**
- **T1110.003 — Password Spraying**
- **T1078.002 — Valid Accounts: Domain Accounts**

I simulated a password-spraying attack against the lab's Active Directory environment.

The simulation used multiple users and password attempts rather than repeatedly targeting a single account, reproducing the general pattern of a password-spray attack.

## Technologies Used

### Security Monitoring
- Splunk Enterprise
- Splunk Universal Forwarder
- Windows Security Event Logs
- Windows Event Forwarding/collection architecture
- Sysmon logging
- Active Directory auditing

## Future Improvements

The lab was designed with additional controlled detection scenarios in mind. Future iterations can expand the project to include:

- Encoded PowerShell detection
- Kerberoasting telemetry
- PsExec-style lateral movement
- Scheduled-task persistence
- Security log clearing
- Data staging and simulated exfiltration
- Automated detection and alerting
- SOC investigation reports
- IOC extraction and timeline generation

## Disclaimer

This project was conducted in an isolated personal lab environment using virtual machines owned and controlled by me.

Attack simulations were designed to generate security telemetry for defensive monitoring and investigation. No third-party systems, accounts, networks, or real-world targets were involved.

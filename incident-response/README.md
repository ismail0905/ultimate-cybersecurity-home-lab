🛡️ Incident Response Simulation

By Ismail Odawa

📌 Overview

This project simulates a full incident response lifecycle, from threat detection and triage to containment, remediation, reporting, and post-mortem review.

The goal was to recreate a realistic SOC scenario inside my custom-built cybersecurity home lab (see: Ultimate Cybersecurity Home Lab
), and demonstrate technical proficiency in identifying, analysing, and responding to security incidents using industry best practices and hands-on tooling.

This project also reflects how security teams respond to real-world events using structured methodologies like NIST 800-61, MITRE ATT&CK, and CVSS scoring.

🎯 Objectives

Investigate a simulated security breach inside the lab

Identify the root cause and attack vector

Respond using technical and procedural controls

Write a full incident report and post-mortem

Reflect on lessons learned and improvements

🧠 Environment Setup


Tools used:

🖥️ Proxmox VE (Hypervisor)

🧱 pfSense (firewall/logs)

🎯 Kali Linux (attacker simulation)

🛡️ Ubuntu Server (target system)

📝 Wireshark, Nmap, Fail2Ban, auditd



<img src="https://github.com/user-attachments/assets/2ab76769-3ce7-4b9f-93ab-30a1e512c746" alt="Incident Response Timeline Diagram" width="700"/>


Simulation Method:

Attacks initiated from Kali (e.g. SSH brute-force, Nmap scan)

Ubuntu Server was configured with services like SSH, web server

Logs captured via syslog and manual inspection


| Stage              | Description                                              |
| ------------------ | -------------------------------------------------------- |
| **Reconnaissance** | Attacker (Kali) scans Ubuntu using Nmap                  |
| **Initial Access** | SSH brute-force simulated via Hydra                      |
| **Persistence**    | Attacker installs netcat backdoor                        |
| **Detection**      | Alert triggered via log monitoring                       |
| **Analysis**       | Logs reviewed, suspicious activity isolated              |
| **Containment**    | SSH service disabled, attacker IP blocked via pfSense    |
| **Eradication**    | Backdoor removed, user keys rotated                      |
| **Recovery**       | Clean snapshot restored, monitoring tightened            |
| **Post-Mortem**    | Report created, timeline reviewed, GRC controls improved |



Sample Incident Report (Extract)

**Date of Incident**: August 19, 2025  
**Affected Asset**: Ubuntu Web Server (192.168.1.150)  
**Detection Source**: auth.log / pfSense firewall logs  
**Root Cause**: Weak SSH credentials exploited via brute force  
**Indicators of Compromise**:
- Multiple failed SSH attempts from 192.168.1.105
- Unexpected new user created: "nc_user"
- Running netcat listening on port 4444

**Response Actions**:
- Blocked malicious IP via pfSense
- Disabled SSH access temporarily
- Erased unauthorised user
- Reviewed authentication policies


Post-Mortem Summary

| Area                  | Finding                                             |
| --------------------- | --------------------------------------------------- |
| **What Went Wrong?**  | Weak SSH credentials allowed brute-force success    |
| **What Worked?**      | Log monitoring helped catch activity early          |
| **What Can Improve?** | Stronger auth controls, automated alerting          |
| **Lessons Learned**   | Never rely solely on SSH passwords; use 2FA or keys |



✅ Key Skills Demonstrated

Threat detection and triage

Log analysis (Linux & pfSense)

Brute-force simulation (Hydra)

Real-time incident response actions

Technical + written reporting

Post-incident GRC improvement planning


🔚 Final Notes

This project helped reinforce critical incident response workflows in a controlled, hands-on environment.
It reflects not just my ability to investigate and respond to incidents technically, but also to document them clearly and reflect on how controls can be improved in line with SOC playbooks and industry frameworks.

🧰 This project is part of my ongoing home lab series, alongside:

🔐 Ultimate Cybersecurity Home Lab

🛠️ Vulnerability Assessment Project (Not yet Completed)

🤖 AI Security Analyst Assistant (Currently working On)

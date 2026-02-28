# -Linux-Hardening-Audit-Too

Linux Hardening Audit Tool
📌 Project Overview

The Linux Hardening Audit Tool is a Python-based security auditing script designed to evaluate the security posture of a Linux system. It performs automated configuration checks aligned with best-practice hardening principles inspired by CIS benchmarks and generates a compliance score along with actionable recommendations.

This tool demonstrates practical implementation of Linux security auditing, automation, and risk-based scoring.

🎯 Objective

To develop a lightweight auditing tool that:

Evaluates system security configurations

Identifies vulnerabilities and misconfigurations

Assigns a compliance score

Classifies overall system risk level

Generates a structured audit report

🧰 Tools & Technologies Used

Python 3

os module (file & permission inspection)

subprocess module (system command execution)

Linux utilities:

ufw

systemctl

chkrootkit

SSH configuration files

Linux environment (Kali & Ubuntu VMs)

⚙️ Features Implemented

✔ Firewall status check
✔ SSH hardening verification
✔ Critical file permission validation
✔ SUID file detection
✔ Rootkit indicator detection
✔ Risky/legacy service detection
✔ Password aging policy verification
✔ Compliance scoring system
✔ Risk classification (HIGH / MEDIUM / SECURE)
✔ Timestamped audit report generation

🏗️ Steps Involved in Building the Project

Designed security audit checklist based on hardening best practices.

Implemented system command execution using subprocess.

Parsed SSH configuration file to detect insecure authentication settings.

Used os.stat() to verify critical file permissions.

Detected excessive SUID files across the system.

Integrated rootkit detection via chkrootkit.

Implemented checks for risky services (telnet, rsh, vsftpd).

Added password aging policy validation.

Developed scoring logic with risk classification.

Automated structured report generation.

🖥️ How to Run the Tool
sudo python3 audit_tool.py

⚠️ Root privileges are required to inspect system configurations properly.

Optional dependency:

sudo apt install chkrootkit
📊 Sample Output
Starting Linux Hardening Audit...

Audit Completed.
Final Score: 40/120
Overall Risk Level: HIGH RISK
Report saved as audit_report_YYYYMMDD_HHMMSS.txt
📈 Scoring Model
Score Range	Risk Level
0–40	HIGH RISK
41–80	MEDIUM RISK
81–120	SECURE

Each security check contributes to the overall compliance score.

🧠 Technical Concepts Demonstrated

Linux security hardening

SSH configuration auditing

File permission analysis

Privilege escalation risk detection

Service exposure analysis

Rootkit detection basics

Automated security reporting

Risk-based scoring systems

🏢 Real-World Implementation

This tool can be implemented in:

Small and medium enterprise Linux servers

Development/test environments

Academic labs

Pre-deployment security validation

DevSecOps pipelines

Internal security audits

It can serve as:

A baseline compliance checker

A learning tool for Linux security

A foundation for enterprise audit automation

⚠️ Current Limitations & Vulnerabilities

While functional, this tool has limitations:

Signature-Based Rootkit Detection

Relies on chkrootkit, which may not detect advanced stealth rootkits.

Improvement: Integrate additional detection tools (e.g., rkhunter).

Static Configuration Checks

Only verifies presence of certain settings.

Does not validate dynamic runtime configurations.

Improvement: Implement deeper parsing & validation logic.

Basic Scoring Model

Equal weight assigned to most checks.

Improvement: Implement weighted risk scoring based on severity.

No Logging or Alerting System

Does not notify administrators automatically.

Improvement: Add email alerts or SIEM integration.

Local System Scope Only

Audits only the host machine.

Improvement: Extend to remote auditing via SSH automation.

🔐 How These Vulnerabilities Can Be Fixed

Future enhancements may include:

Advanced CIS benchmark integration

JSON export for SIEM ingestion

Web dashboard interface

API-based remote scanning

Real-time monitoring integration

Severity-based weighted scoring

Multi-host auditing framework

These upgrades would transform the tool from a local audit script into a scalable security assessment platform.

🚀 Conclusion

The Linux Hardening Audit Tool successfully automates the evaluation of a Linux system’s security posture using practical hardening principles. Beyond completing the project, this implementation demonstrates real-world security auditing techniques, system-level inspection, and risk-based evaluation logic.

The tool highlights how automation can improve security visibility and enforce compliance across systems. While currently designed for local auditing, it provides a strong foundation for enterprise-grade security assessment tools.

This project showcases applied knowledge in Linux security, Python automation, and system configuration auditing — making it relevant for cybersecurity operations, system administration, DevSecOps, and compliance engineering roles.

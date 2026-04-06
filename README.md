# Sentinel SOC Detection Engineering Lab

A hands-on **Microsoft Sentinel detection engineering lab** built across **Windows 11 and Linux (Ubuntu) endpoints** using:

* **Microsoft Sentinel**
* **Azure Arc**
* **Azure Monitor Agent (AMA)**
* **Sysmon**
* **auditd**
* **rsyslog**
* **MITRE ATT&CK aligned analytics rules**
* **KQL-based threat detections**

This project demonstrates how to build an **enterprise-style SOC lab** for learning:

* Threat detection engineering
* KQL hunting
* Analytics rule creation
* MITRE ATT&CK mapping
* Incident simulation
* Windows + Linux telemetry onboarding
* SIEM content development

---

#  Project Objective

The goal of this project is to create a **cross-platform SOC lab** that simulates real attacker behavior and converts it into:

* Custom Sentinel analytics rules
* Incident generation workflows
* MITRE ATT&CK use-case mapping
* Detection validation playbooks
* KQL hunting content
---

# Lab Architecture

##  Windows 11 Endpoint

**Hostname:** `Dark-Array`

### Installed Components

* Azure Arc Connected Machine Agent
* Azure Monitor Agent (AMA)
* Sysmon
* Windows Security Events
* Custom DCR for Sysmon channel

### Main Log Sources

* `SecurityEvent`
* `Event`
* `Sysmon`
* `Heartbeat`

---

## Linux Endpoint

**Hostname:** `mrrobot`

### Installed Components

* Azure Arc
* AMA
* `auditd`
* `rsyslog`
* Syslog DCR

### Main Log Sources

* `Syslog`
* `LinuxAuditLog`
* `Heartbeat`

---

# MITRE ATT&CK Coverage

This lab covers **all 14 Enterprise MITRE ATT&CK tactics**.

## Covered Tactics

* Reconnaissance - Gather target info before attack
* Resource Development -  Build infra, payloads, domains, tools
* Initial Access - First foothold into target
* Execution - Run malicious code
* Persistence - Maintain long-term access
* Privilege Escalation - Gain higher privileges
* Defense Evasion - Avoid detection
* Credential Access - Steal passwords / tokens
* Discovery - Learn environment
* Lateral Movement - Move to other systems
* Collection - Gather data before theft
* Command and Control - Communicate with attacker infra
* Exfiltration - Steal data out
* Impact - Disrupt, encrypt, destroy

---
# Skills Demonstrated

This project highlights:

* SIEM engineering
* Microsoft Sentinel onboarding
* KQL detection logic
* Azure Arc hybrid security monitoring
* Windows Sysmon telemetry engineering
* Linux audit telemetry collection
* MITRE ATT&CK detection mapping
* SOC use-case development
* Incident rule tuning
* Threat hunting
---

#  Outcome

This lab serves as a **real-world SOC engineering showcase** demonstrating how to:

* onboard hybrid endpoints
* normalize telemetry
* simulate adversary behavior
* write production-style detections
* generate Sentinel incidents
* map everything to MITRE ATT&CK

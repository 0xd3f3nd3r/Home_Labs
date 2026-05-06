# 🛡️ Wazuh Docker SOC Homelab

<div align="center">

![Wazuh](https://img.shields.io/badge/Wazuh-4.11.2-blue?style=for-the-badge\&logo=wazuh)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?style=for-the-badge\&logo=docker)
![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04-E95420?style=for-the-badge\&logo=ubuntu)
![Windows](https://img.shields.io/badge/Windows-11%20%7C%20Server%202022-0078D6?style=for-the-badge\&logo=windows)
![MITRE ATT\&CK](https://img.shields.io/badge/MITRE-ATT%26CK-red?style=for-the-badge)
![SOC](https://img.shields.io/badge/SOC-Homelab-green?style=for-the-badge)

### 🚀 Enterprise-Style Security Operations Center (SOC) Homelab using Wazuh, Docker, Sysmon, and Windows Endpoints

</div>

---

# 📌 Overview

This project is a fully containerized **Wazuh SOC Homelab** designed to simulate a real-world Security Operations Center (SOC) environment.

The lab provides centralized log collection, threat detection, security monitoring, file integrity monitoring, vulnerability detection, and threat hunting capabilities using:

* Wazuh
* Docker
* Windows Agents
* Sysmon
* MITRE ATT&CK Mapping
* Threat Hunting Workflows

This homelab was built to gain practical hands-on experience in:

* 🔍 Threat Detection
* 🛡️ Security Monitoring
* 📊 SIEM Operations
* ⚡ Detection Engineering
* 🧠 Threat Hunting
* 📁 Log Analysis
* 🧰 Docker Administration
* 🧪 Red Team Simulation
* 🚨 Incident Investigation

---

# 🏗️ Architecture

## 🌐 Unified SOC Architecture Diagram

> Replace this image with your exported Draw.io diagram.

```text
architecture/
└── unified-wazuh-soc-architecture.png
```

![Architecture](architecture/unified-wazuh-soc-architecture.png)

---

# 🖥️ Lab Environment

## 💻 Host Machine

| Component               | Details        |
| ----------------------- | -------------- |
| OS                      | Ubuntu Linux   |
| Virtualization          | VirtualBox     |
| Container Engine        | Docker         |
| Container Orchestration | Docker Compose |

---

## 🧪 Virtual Machines

| Machine             | Purpose                      |
| ------------------- | ---------------------------- |
| Ubuntu VM           | Docker Host & Wazuh Stack    |
| Windows 11          | Endpoint Monitoring          |
| Windows Server 2022 | Endpoint Monitoring          |
| Kali Linux          | Attack Simulation / Red Team |

---

# 🐳 Dockerized Wazuh Stack

| Container       | Purpose                        | Port              |
| --------------- | ------------------------------ | ----------------- |
| Wazuh Manager   | Event Analysis & Alerting      | 1514, 1515, 55000 |
| Wazuh Indexer   | OpenSearch Backend             | 9200              |
| Wazuh Dashboard | Visualization & Threat Hunting | 443               |

---

# ✨ Features

## 🔍 Security Monitoring

* Centralized log collection
* Real-time alert generation
* Security event correlation
* Endpoint visibility
* Threat detection workflows

---

## 🛡️ Detection Engineering

* Custom Wazuh rules
* Sysmon integration
* Windows event analysis
* False positive reduction
* MITRE ATT&CK mapping

---

## 📂 File Integrity Monitoring (FIM)

Monitor:

* File modifications
* File deletions
* Permission changes
* Registry changes
* Suspicious file activity

---

## 🧠 Threat Hunting

* Security alert investigation
* IOC hunting
* Suspicious process monitoring
* PowerShell detection
* Network scanning detection

---

## 📊 Vulnerability Detection

* CVE identification
* Package vulnerability analysis
* Endpoint exposure visibility
* Vulnerability assessment

---

# 🧱 Technologies Used

| Technology          | Purpose                |
| ------------------- | ---------------------- |
| Wazuh               | SIEM & XDR Platform    |
| Docker              | Containerization       |
| Sysmon              | Windows Telemetry      |
| Ubuntu              | Docker Host            |
| Windows 11          | Endpoint               |
| Windows Server 2022 | Endpoint               |
| Kali Linux          | Attack Simulation      |
| MITRE ATT&CK        | Threat Mapping         |
| XML                 | Wazuh Rules & Decoders |

---

# 📸 Screenshots

## 🐳 Docker Containers

```bash
docker ps
```

![Docker Containers](screenshots/docker-containers.png)

---

## 📊 Wazuh Dashboard

![Wazuh Dashboard](screenshots/wazuh-dashboard.png)

---

## 💻 Virtual Machines

![Virtual Machines](screenshots/virtual-machines.png)

---

## ⚙️ Docker Service Status

```bash
systemctl status docker
```

![Docker Status](screenshots/docker-status.png)

---

# 🚀 Installation Guide

## 📥 Clone Repository

```bash
git clone https://github.com/yourusername/wazuh-docker-homelab.git
cd wazuh-docker-homelab
```

---

## 🐳 Start Wazuh Stack

```bash
docker compose up -d
```

---

## ✅ Verify Running Containers

```bash
docker ps
```

---

## 🌐 Access Dashboard

```text
https://<your-ip>
```

---

# 🖥️ Wazuh Agent Enrollment

## Windows 11 / Windows Server 2022

### Install Wazuh Agent

```powershell
Invoke-WebRequest -Uri https://packages.wazuh.com/4.x/windows/wazuh-agent-4.11.2-1.msi -OutFile wazuh-agent.msi
```

---

### Configure Manager IP

Update:

```text
C:\Program Files (x86)\ossec-agent\ossec.conf
```

---

### Start Agent Service

```powershell
NET START WazuhSvc
```

---

# 📂 Repository Structure

```text
wazuh-docker-homelab/
│
├── architecture/
├── screenshots/
├── docker/
├── agents/
├── detection-rules/
├── documentation/
├── dashboards/
├── logs/
├── README.md
└── docker-compose.yml
```

---

# 🧪 Detection Use Cases

This homelab supports detection of:

* 🔥 PowerShell Attacks
* 🔑 Brute Force Attempts
* 🧬 Malware Indicators
* 🧪 Nmap Scanning Activity
* ⚠️ Privilege Escalation
* 📁 File Modifications
* 🧠 Suspicious Process Execution
* 🌐 Network Enumeration
* 🚨 Unauthorized Access Attempts

---

# 📜 Custom Rules & Configurations

Custom detection rules are stored in:

```text
detection-rules/
```

Includes:

* Windows detection rules
* Sysmon rules
* Custom decoders
* False positive tuning
* Threat detection use cases

---

# 🧠 Learning Outcomes

Through this project, I gained practical experience in:

* Wazuh Administration
* SOC Operations
* SIEM Monitoring
* Docker Management
* Threat Detection Engineering
* Threat Hunting
* Windows Event Analysis
* Sysmon Log Analysis
* Incident Investigation
* Detection Rule Tuning

---

# 📈 Future Improvements

Planned enhancements:

* ✅ Suricata IDS Integration
* ✅ Zeek Network Monitoring
* ✅ OpenSearch Dashboards
* ✅ Sigma Rule Integration
* ✅ Active Response Automation
* ✅ Malware Sandbox Integration
* ✅ SOAR Workflows
* ✅ Cloud Log Monitoring

---

# 🔐 Security Notes

⚠️ This project is intended for:

* Educational purposes
* Security research
* SOC practice
* Detection engineering labs

Do NOT expose this environment directly to the public internet without proper security controls.

---

# 📚 References

* [https://documentation.wazuh.com/](https://documentation.wazuh.com/)
* [https://docs.docker.com/](https://docs.docker.com/)
* [https://attack.mitre.org/](https://attack.mitre.org/)
* [https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)

---

# 👨‍💻 Author

## Manivel K

### Cybersecurity Enthusiast | SOC Analyst | Detection Engineering Learner

* 🛡️ Wazuh & SIEM Enthusiast
* 🔍 Threat Hunting Learner
* 📊 Detection Engineering
* 🧠 Windows & Network Forensics
* 🚨 SOC Operations

---

# ⭐ Support

If you found this project useful:

* ⭐ Star this repository
* 🍴 Fork the project
* 🛡️ Share with the cybersecurity community

---

<div align="center">

## 🚀 Building Practical SOC Skills Through Hands-On Lab


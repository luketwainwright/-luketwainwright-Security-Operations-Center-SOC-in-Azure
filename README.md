# -luketwainwright-Security-Operations-Center-SOC-in-Azure
### Project Goals

- Get real-world SIEM experience
- Simulate real attacks and log activity
- Build automated alerting, playbooks, and threat intelligence feeds
- Practice threat hunting using KQL (Kusto Query Language)
- Lay the foundation for advanced SOC workflows

**Architecture Overview**
Cloud Provider: Microsoft Azure (Free Tier)  
SIEM: Microsoft Sentinel  
Log Ingestion: Azure Monitor Agent + Log Analytics  
VM OS: Ubuntu 20.04 (Linux)  
Data Sources:
- Linux Syslog
- Performance Counters
- Custom Users and Commands
- Threat Intelligence Feeds (Microsoft, AbuseIPDB, OTX)


 ### Features

**Log Collection and Monitoring**

- Syslog data from Azure Linux VM
- Custom log activity: user creation, failed logins, privilege escalation
- Performance metrics via DCR (Data Collection Rules)

**Threat Detection and Rules**

- KQL queries for:
  - Privilege escalation detection
  - Multiple failed logins
  - Suspicious `su` and `adduser` activity
  - Syslog parsing and entity extraction
- Analytics Rules to trigger incidents on abnormal behavior

**Threat Intelligence Integration**

- Microsoft Defender Threat Intelligence
- TI-mapping to Linux Syslog
- (Planned) OTX and AbuseIPDB integration

**Automated Response**

- Azure Logic App (Playbook) to:
  - Send email notifications when Sentinel incidents are triggered
  - Enrich incident data dynamically (coming soon)

**Threat Hunting**

- Custom hunting queries using MITRE ATT&CK logic
- Hunt created: `Privilege Escalation`
- Honeyuser activity monitoring
- Real command logs analyzed using KQL


**Skills & Concepts Demonstrated**

- Cloud Security (Azure)
- SIEM + SOAR workflows
- Log Analytics + KQL
- Incident Response
- Threat Hunting (Linux-focused)
- Azure Security Architecture
- Automation via Logic Apps


**Future Improvements**

- Integrate Azure Active Directory & Defender for Endpoint logs
- Add honeypot VM or fake web service
- Build a custom workbook dashboard
- Create Function Apps for automated IP enrichment
- Expand detection rules with MITRE ATT&CK mapping

---

**About Me**

Luke Wainwright  
IT Professional | BSIT Student  
📧 luketwainwright@gmail.com  

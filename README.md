# Exploring-Azure-Sentinel-A-Hands-On-Lab-for-Cybersecurity

## Objective
This project aimed to demonstrate the configuration and use of Azure Sentinel for security monitoring, threat detection, and incident response. The primary focus was to deploy and secure Azure resources, ingest Windows Security Event logs, and leverage advanced analytics using the MITRE ATT&CK framework. This hands-on experience enhanced understanding of cloud-native SIEM systems and best practices in modern cybersecurity operations.

---

## Skills Learned
- Proficiency in configuring and managing a cloud-native SIEM solution.
- Advanced understanding of Kusto Query Language (KQL) for querying and analyzing log data.
- Application of MITRE ATT&CK framework for mapping detected threats to adversary tactics and techniques.
- Implementation of security best practices, including Just-in-Time (JIT) access and NSG configuration.
- Hands-on experience with detecting and mitigating persistence techniques like scheduled tasks.

---

## Tools Used
- **Azure Sentinel**: Cloud-native SIEM and SOAR solution for threat detection and incident response.
- **Log Analytics Workspace**: Centralized repository for telemetry data from Azure resources.
- **Windows Task Scheduler**: Simulated malicious activity for scheduled task detection.
- **Event Viewer**: Monitored Windows Security Event logs to observe generated incidents.
- **KQL**: Query language used to analyze logs and write custom detection rules.

---

## Steps
1. **Create Azure Account**
   - Set up a free Azure account with a subscription to deploy and configure resources.

2. **Set Up Resource Group**
   - Grouped all related resources (VM, Log Analytics Workspace, and Sentinel) into a single resource group for streamlined management.

3. **Deploy Virtual Machine**
   - Created a Windows 10 virtual machine to act as the primary endpoint for log generation.
   - Configured network settings and secured access using NSGs.

4. **Enable Microsoft Defender and Configure JIT Access**
   - Enabled enhanced security in Microsoft Defender for Cloud.
   - Configured Just-in-Time (JIT) access to minimize the attack surface by restricting RDP access based on time and source IP.

5. **Set Up Log Analytics and Connect to Sentinel**
   - Created a Log Analytics Workspace to collect logs and telemetry data.
   - Integrated Azure Sentinel with the workspace to enable SIEM functionality.

6. **Ingest Data into Sentinel**
   - Configured data connectors to ingest Windows Security Event logs from the VM into Sentinel.
   - Enabled data collection rules for relevant event IDs (e.g., `4624` for successful logons).

7. **Write KQL Queries**
   - Developed queries to analyze security event logs and detect specific activities like successful logons and scheduled task creation.

8. **Simulate and Detect Scheduled Tasks**
   - Created a scheduled task on the VM to simulate adversarial persistence techniques (MITRE ATT&CK T1053).
   - Enabled logging for scheduled task creation (Event ID `4698`) and wrote custom analytics rules in Sentinel to generate alerts.

9. **Generate Alerts and Analyze Logs**
   - Configured analytic rules to generate alerts for detected suspicious activity.
   - Used enriched alerts to provide detailed context for investigation.

---

This repository serves as a comprehensive resource for understanding and implementing Azure Sentinel in a practical lab setting. The complete documentation, including detailed steps and findings, is provided in the project report.

[Download Full Project Documentation](./Exploring%20Azure%20Sentinel.pdf)

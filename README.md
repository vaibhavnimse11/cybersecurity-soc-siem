# cybersecurity-soc-siem
A custom SIEM-powered Security Operations Center (SOC) built using ELK Stack, integrated with Nagios, Suricata, and OSSEC for real-time threat detection, monitoring, and incident response.

SIEM-Based Security Operations Center (SOC) Using ELK Stack, Nagios, Suricata & OSSEC


📌 Project Overview
This project implements a Security Operations Center (SOC) using an ELK Stack (Elasticsearch, Logstash, Kibana) as the central SIEM platform integrated with:

Nagios → System and network monitoring

Suricata → Network-based Intrusion Detection/Prevention System (NIDS/NIPS)

OSSEC → Host-based Intrusion Detection System (HIDS)

The SOC is designed to collect, process, analyze, and visualize security logs in real-time, providing actionable insights for threat detection, incident response, and network health monitoring.


🎯 Objectives
Deploy an ELK-based SIEM for centralized log management.

Integrate multiple monitoring & intrusion detection tools into one SOC platform.

Create dashboards for real-time security event visualization.

Enable alerting & automated responses for critical security incidents.


🛠️ Tech Stack
Component	Purpose
ELK Stack (Elasticsearch, Logstash, Kibana)	SIEM & log analysis
Nagios	System/network health monitoring
Suricata	NIDS/NIPS for packet analysis
OSSEC	HIDS for host-level monitoring
Filebeat/Logstash	Log shipping & parsing
Ubuntu/Debian Linux	Host OS




📂 Architecture
css
Copy
Edit
[Nagios] --------\
                  \
[Suricata] --------> [Logstash] -> [Elasticsearch] -> [Kibana Dashboard]
                  /
[OSSEC] ---------/




🚀 Installation Steps
1️⃣ Setup ELK Stack
bash
Copy
Edit
sudo apt update
sudo apt install elasticsearch logstash kibana

2️⃣ Configure Filebeat/Logstash
Setup Filebeat on all monitored systems

Configure Logstash pipelines to parse Nagios, Suricata, and OSSEC logs

3️⃣ Install & Configure Nagios
bash
Copy
Edit
sudo apt install nagios4

4️⃣ Install & Configure Suricata
bash
Copy
Edit
sudo apt install suricata

5️⃣ Install & Configure OSSEC
bash
Copy
Edit
wget https://github.com/ossec/ossec-hids/archive/master.zip



📊 Dashboards & Alerts
Nagios Alerts: Server uptime/downtime, CPU/memory usage

Suricata Alerts: Suspicious traffic, port scans, DDoS attempts

OSSEC Alerts: Unauthorized logins, file changes

Kibana Dashboards: Unified SOC view



🛡️ Use Cases
Real-time threat detection

Centralized log management

Incident response workflow

Compliance reporting

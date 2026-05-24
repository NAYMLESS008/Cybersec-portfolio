# Multi-Region T-Pot Honeypot Threat Monitoring

## Project Overview

This project involved deploying and analysing a T-Pot honeypot environment to observe real-world attack traffic against exposed cloud systems.

The goal was to collect attacker telemetry, analyse IDS alerts and honeypot logs, and produce blue-team style findings using tools such as Suricata, ELK/Kibana, Cowrie, Dionaea, Honeytrap, Docker, and Linux.

## Objectives

- Deploy honeypot infrastructure to collect real-world attack traffic.
- Analyse Suricata IDS alerts and honeypot events.
- Review SSH brute-force attempts, scanning behaviour, and suspicious network activity.
- Practise SOC-style investigation and reporting.
- Convert raw logs into useful security findings and defensive recommendations.

## Tools Used

| Tool | Purpose |
|---|---|
| T-Pot | Honeypot platform |
| Suricata | IDS alerting and network detection |
| ELK/Kibana | Log search, dashboards, and visualisation |
| Elasticsearch | Querying and aggregating logs |
| Cowrie | SSH/Telnet honeypot |
| Dionaea | Malware/service interaction honeypot |
| Honeytrap | Network service deception |
| Docker | Containerised honeypot services |
| Linux | System administration and log handling |

## Architecture

```text
Internet Attackers
        ↓
Cloud T-Pot Node
        ↓
Honeypot Services
Cowrie | Dionaea | Honeytrap | Sentrypeer | ConPot
        ↓
Suricata IDS + Honeypot Logs
        ↓
Elasticsearch / Logstash / Kibana
        ↓
Analyst Investigation and Reporting
```

## Investigation Workflow

1. Reviewed high-volume alerts and events in Kibana.
2. Identified affected honeypot services and destination ports.
3. Checked source IPs, timestamps, and repeated behaviour.
4. Compared Suricata alerts with honeypot service logs.
5. Classified activity as scanning, brute force, exploit attempt, malware interaction, or suspicious connection.
6. Mapped relevant behaviours to MITRE ATT&CK where possible.
7. Documented findings, impact, and defensive recommendations.

## Example Findings

### Finding 1: SSH Brute-Force Activity

Cowrie logs showed repeated SSH login attempts against the honeypot environment. These attempts involved automated credential guessing and repeated connection attempts from external IP addresses.

### Finding 2: IDS Alerts from Suricata

Suricata generated IDS alerts for suspicious network activity targeting exposed services. These alerts helped identify scanning activity, exploit attempts, and protocol-specific anomalies.

### Finding 3: Internet-Wide Scanning

The honeypot captured repeated connection attempts against common ports and services, suggesting automated internet-wide scanning behaviour.

## What I Learned

- How internet-exposed systems are attacked by automated scanners.
- How honeypots collect real-world attacker behaviour.
- How Suricata IDS alerts can be reviewed and correlated with honeypot logs.
- How ELK/Kibana supports log investigation and SOC-style analysis.
- How to convert raw telemetry into security findings and recommendations.

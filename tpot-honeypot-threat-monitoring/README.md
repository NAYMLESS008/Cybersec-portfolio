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
Cowrie | Dionaea | Honeytrap | Sentrypeer | ConPot |
        ↓
Suricata IDS + Honeypot Logs
        ↓
Elasticsearch / Logstash / Kibana
        ↓
Analyst Investigation and Reporting

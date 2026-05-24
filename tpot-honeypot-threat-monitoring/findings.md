# Findings — Multi-Region T-Pot Honeypot Threat Monitoring

## Finding 1: SSH Brute-Force Activity

Cowrie logs showed repeated SSH login attempts against the honeypot environment. These attempts involved automated credential guessing and repeated connection attempts from external IP addresses.

### Security Value

- Demonstrates the risk of exposing SSH services to the internet.
- Supports the use of key-based authentication, MFA, rate limiting, and login monitoring.
- Shows how honeypots can reveal attacker credential-guessing behaviour.

---

## Finding 2: Suricata IDS Alerts

Suricata generated IDS alerts for suspicious traffic targeting exposed services. These alerts helped identify scanning behaviour, exploit attempts, and protocol-specific anomalies.

### Security Value

- Shows how IDS alerts can support early detection.
- Demonstrates alert triage and correlation with honeypot logs.
- Provides SOC-style investigation experience.

---

## Finding 3: Internet-Wide Scanning

The honeypot captured repeated connection attempts against common ports and services, suggesting automated internet-wide scanning activity.

### Security Value

- Reinforces the risk of public cloud exposure.
- Supports firewall hardening and attack surface management.
- Shows how quickly exposed systems can be discovered by attackers.

---

## Overall Summary

The project demonstrated that internet-facing systems are quickly discovered and targeted by automated scanners and brute-force tools. By using T-Pot, Suricata, and ELK/Kibana, the collected telemetry was converted into useful blue-team findings suitable for SOC-style reporting and defensive recommendations.

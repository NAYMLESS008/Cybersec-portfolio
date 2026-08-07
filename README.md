# Adith Menon | Cybersecurity Portfolio

MSc Computing (Applied Cyber Security) candidate at Technological University Dublin, building hands-on experience in security monitoring, threat detection, incident investigation, malware analysis, and Infrastructure-as-Code recovery.

[LinkedIn](https://www.linkedin.com/in/real-adith-menon/) | [Email](mailto:adithmenon21@gmail.com) | Dublin, Ireland

## About this portfolio

This repository presents practical cybersecurity work completed through postgraduate study and independent implementation. The projects focus on blue-team and SOC workflows: collecting telemetry, investigating alerts, mapping behaviour to MITRE ATT&CK, preserving evidence, validating recovery, and communicating findings clearly.

## Core capabilities

- **Security operations:** alert triage, log correlation, IOC analysis, true-positive/false-positive classification, incident reporting
- **Detection and monitoring:** Wazuh, Suricata, ELK/Kibana, Elasticsearch, File Integrity Monitoring
- **Cloud and recovery:** Terraform, Google Cloud Platform, Linux, Infrastructure as Code, automated replacement and validation
- **Threat analysis:** honeypot telemetry, SSH brute force, scanning, malware delivery, MITRE ATT&CK mapping
- **Security testing:** Wireshark, Burp Suite, PEStudio, Process Monitor, Process Explorer, Regshot, FakeNet
- **Development:** Python, HCL, Docker, C++, Java, HTML, CSS, JavaScript

## Featured projects

### 1. IaC-Based Recovery for Runtime Persistence Attacks

**MSc thesis project | Terraform, GCP, Wazuh, Python, Linux**

Designed and evaluated a recovery workflow for a Terraform-managed stateless Linux VM affected by runtime persistence attacks. Wazuh provides detection while an external Python controller coordinates evidence capture, quarantine, Terraform replacement, monitoring restoration, and validation.

**Verified systemd-persistence run:**

- Wazuh detection: PASS
- Forensic evidence completeness: 10/10 items
- Quarantine and stale-agent cleanup: PASS
- Terraform replacement and post-recovery validation: PASS
- Monitoring restored: PASS
- Residual compromise checks: 0/6

The evaluated prototype uses one stateless VM and sequential recovery. Multi-host concurrency and scalability remain future work.

[View the public project summary](iac-recovery-thesis/README.md)

### 2. Multi-Region T-Pot Honeypot Threat Monitoring

**T-Pot, Suricata, ELK/Kibana, Cowrie, Dionaea, Honeytrap, Docker**

Deployed honeypot infrastructure across India, the United States, and Australia to collect and investigate real-world hostile internet traffic. Analysed IDS alerts, SSH brute-force activity, scanning behaviour, exploit attempts, and malware-delivery interactions, then translated findings into SOC-style case studies and MITRE ATT&CK mappings.

[Project overview](tpot-honeypot-threat-monitoring/README.md) | [Key findings](tpot-honeypot-threat-monitoring/findings.md) | [MITRE mapping](tpot-honeypot-threat-monitoring/mitre-mapping.md) | [Screenshots](tpot-honeypot-threat-monitoring/screenshots)

### 3. SOC Alert Investigation

**Alert triage, log correlation, evidence review, MITRE ATT&CK**

Completed a structured SOC investigation covering alert context, supporting evidence, suspicious activity analysis, true-positive/false-positive classification, ATT&CK mapping, and recommended containment and response actions.

[Project overview](soc-alert-investigation/README.md) | [Investigation report](soc-alert-investigation/investigation-report.md)

### 4. Dridex Malware Analysis

**PEStudio, ProcMon, Process Explorer, Regshot, FakeNet, Wireshark**

Performed static and dynamic analysis in an isolated environment. Identified process-injection behaviour involving VirtualAlloc, WriteProcessMemory, and CreateRemoteThread, along with silent execution and outbound TLS activity. Findings were documented in a structured 15-page report.

[Malware analysis methodology](malware-analysis-notes/README.md) | [Report structure](malware-analysis-notes/report-structure.md)

### 5. Secure SSDLC for a Multi-Vendor Marketplace

**STRIDE, OWASP ASVS, MITRE ATT&CK, Burp Suite, WordPress/Dokan**

Applied secure-development practices to a marketplace implementation, including threat modelling, security-control mapping, web testing, authentication hardening, activity logging, backups, and security headers.

[Project overview](secure-ssdlc-marketplace/README.md) | [Threat model](secure-ssdlc-marketplace/threat-model.md) | [Security controls](secure-ssdlc-marketplace/security-controls.md)

## Project index

| Project | Primary evidence | Skills demonstrated |
| --- | --- | --- |
| IaC recovery thesis | Architecture, workflow, verified recovery results | Wazuh, Terraform, GCP, Python, evidence preservation, recovery validation |
| T-Pot threat monitoring | Findings, ATT&CK mapping, screenshots | Suricata, ELK/Kibana, honeypots, log analysis, threat reporting |
| SOC alert investigation | Investigation report | Triage, correlation, verdict classification, response recommendations |
| Dridex malware analysis | Analysis methodology and report structure | Static/dynamic analysis, IOC identification, network analysis |
| Secure SSDLC marketplace | Threat model and controls | STRIDE, OWASP ASVS, Burp Suite, defensive design |

## Career direction

Seeking graduate and entry-level opportunities in Ireland, including:

- SOC Analyst
- Cybersecurity Analyst
- Security Operations Analyst
- Junior Incident Response or Threat Detection roles

## Contact

- **Email:** [adithmenon21@gmail.com](mailto:adithmenon21@gmail.com)
- **LinkedIn:** [linkedin.com/in/real-adith-menon](https://www.linkedin.com/in/real-adith-menon/)
- **GitHub:** [github.com/NAYMLESS008](https://github.com/NAYMLESS008)
- **Location:** Dublin, Ireland

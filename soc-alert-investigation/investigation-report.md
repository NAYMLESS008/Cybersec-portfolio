# SOC Investigation Report — Suspicious Activity

## 1. Alert Summary

| Field | Details |
|---|---|
| Alert Name | Suspicious Activity |
| Severity | Medium |
| Date/Time | To be added |
| Source IP | To be added |
| Destination/User | To be added |
| Tool/Platform | To be added |
| Status | To be assessed |

## 2. Initial Observation

The alert indicated suspicious activity involving a source and target asset. The investigation focused on validating whether the alert represented malicious activity and identifying the appropriate response.

## 3. Evidence Collected

- Source IP:
- Destination IP/Host:
- Username:
- Number of attempts:
- Time window:
- Alert name:
- Related logs:
- Screenshots:

## 4. Investigation Steps

1. Reviewed the alert details and timestamp.
2. Checked source and destination information.
3. Analysed related logs around the alert time.
4. Looked for repeated behaviour or abnormal patterns.
5. Checked whether authentication was successful or failed.
6. Reviewed related indicators such as IP, domain, hash, or process behaviour.
7. Mapped the behaviour to likely MITRE ATT&CK tactics and techniques.
8. Classified the alert and recommended a response.

## 5. MITRE ATT&CK Mapping

| Behaviour | Tactic | Technique |
|---|---|---|
| Repeated login attempts | Credential Access | Brute Force |
| Suspicious link or attachment | Initial Access | Phishing |
| Malware execution | Execution | User Execution |
| Suspicious outbound traffic | Command and Control | Application Layer Protocol |

## 6. Verdict

To be completed after evidence review.

## 7. Recommended Response

- Review affected asset and user activity.
- Block or monitor suspicious source indicators.
- Reset credentials if compromise is suspected.
- Enable or enforce MFA where applicable.
- Search for related activity across logs.
- Document findings and escalate if required.

## 8. Lessons Learned

- Alert triage requires evidence, not assumptions.
- Multiple log sources improve investigation quality.
- MITRE ATT&CK helps classify observed behaviour.
- Clear documentation supports escalation and reporting.

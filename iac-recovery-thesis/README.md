# IaC-Based Recovery for Runtime Persistence Attacks

**MSc Computing (Applied Cyber Security) thesis project — Technological University Dublin**

## Project overview

This project investigates whether an Infrastructure-as-Code recovery workflow can restore a compromised cloud virtual machine after runtime persistence attacks while preserving forensic evidence and validating that recovery succeeded.

The implementation uses:

- **Terraform** to provision and replace the target infrastructure
- **Google Cloud Platform** to host the research environment
- **Wazuh** to detect suspicious runtime changes
- **Python** to coordinate evidence capture, quarantine, recovery, and validation
- **Linux** as the target operating system

The source repository remains private while the thesis is in progress. This page provides a recruiter-friendly technical summary without exposing credentials, cloud identifiers, live infrastructure details, or sensitive attack automation.

## Research question

> Can an Infrastructure-as-Code recovery workflow restore a Terraform-managed cloud VM after runtime persistence attacks while preserving evidence and validating recovery?

## Architecture

1. A runtime persistence change is introduced on the Terraform-managed target VM.
2. The Wazuh agent forwards security telemetry to a separate Wazuh Manager.
3. An external Python controller confirms the relevant alert.
4. Evidence is captured before destructive recovery.
5. The affected VM is quarantined.
6. Stale monitoring state is removed.
7. Terraform replaces the compromised VM from declared infrastructure configuration.
8. The replacement VM reconnects to Wazuh.
9. Post-recovery checks validate service health, monitoring, access, and absence of known persistence artefacts.
10. Phase results and timings are written to experiment logs.

## Threat scenarios

The evaluation design covers repeatable Linux persistence scenarios:

- Unauthorized SSH key insertion
- Unauthorized local-user creation
- Malicious cron persistence
- Malicious systemd service
- Unexpected listener or open port
- Combined persistence scenario

SSH credential rotation is included where key compromise is relevant.

## Recovery workflow

| Phase | Purpose |
| --- | --- |
| Detect and confirm | Verify that Wazuh observed the intended persistence event |
| Preserve evidence | Capture forensic artefacts before replacement |
| Quarantine | Restrict the compromised VM before destructive action |
| Clean monitoring state | Remove the stale Wazuh agent record |
| Replace with IaC | Use Terraform to destroy and recreate the target VM |
| Restore monitoring | Confirm that the new Wazuh agent is active |
| Validate recovery | Test reachability, required services, and residual compromise indicators |
| Record results | Store phase outcomes, timings, and validation evidence |

## Verified end-to-end result

A complete malicious systemd-persistence run successfully executed the full workflow:

| Check | Result |
| --- | --- |
| Wazuh detection | PASS |
| Evidence capture | PASS — 10/10 expected items |
| Quarantine | PASS |
| Stale Wazuh agent cleanup | PASS |
| Terraform replacement | PASS |
| Post-recovery validation | PASS |
| Monitoring restoration | PASS |
| Residual compromise checks | 0/6 indicators present |

The test confirmed that the malicious service file and script were active before recovery, that evidence was captured before replacement, and that the replacement VM returned to a monitored state without the checked persistence artefacts.

## Evaluation measures

- Detection confirmation success
- Evidence completeness
- Quarantine success
- Infrastructure replacement success
- Monitoring restoration
- Post-recovery validation success
- Residual compromise score
- Phase and end-to-end recovery timings

## Security and engineering decisions

- The attacked target VM is Terraform-managed.
- The Wazuh Manager is separate from the attacked VM.
- Wazuh detects; the external controller performs recovery.
- Evidence is collected before destructive replacement.
- Quarantine occurs before replacement and validation.
- Recovery is Terraform-driven rather than an untracked manual rebuild.
- SSH keys are rotated for SSH persistence or key-compromise scenarios.
- Validation checks both workload recovery and restored monitoring.

## Scope and limitations

This research evaluates a prototype with **one stateless Linux VM and sequential recovery**. It does not claim proven scalability. Multi-host concurrency, queueing, distributed orchestration, Terraform state isolation, centralised evidence storage, cloud API limits, and Wazuh capacity remain future work.

The project evaluates replacement recovery for a controlled research environment. Production adoption would require stronger identity management, protected evidence storage, change approval, secrets management, policy controls, and organisation-specific incident-response procedures.

## Skills demonstrated

- Wazuh alerting and File Integrity Monitoring
- Python security automation
- Terraform and Infrastructure as Code
- Google Cloud administration
- Linux persistence investigation
- Forensic evidence preservation
- Quarantine and replacement recovery
- Recovery validation and experiment design
- Security metrics and technical reporting

[Return to the main portfolio](https://github.com/NAYMLESS008/Cybersec-portfolio)

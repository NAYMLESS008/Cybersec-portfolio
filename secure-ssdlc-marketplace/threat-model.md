# Threat Model — Multi-Vendor Marketplace

## Methodology

The project used STRIDE to identify threats and mapped relevant mitigations to OWASP ASVS and MITRE ATT&CK where appropriate.

## STRIDE Categories

| STRIDE Category | Example Marketplace Risk | Example Mitigation |
|---|---|---|
| Spoofing | Account takeover | MFA, login protection |
| Tampering | Product/order manipulation | Role-based access control, validation |
| Repudiation | User denies action | Activity logging |
| Information Disclosure | Sensitive data exposure | Security headers, access control |
| Denial of Service | Repeated login abuse | Login lockout, CAPTCHA |
| Elevation of Privilege | Vendor gains admin capability | Least privilege, role review |

## Notes

This file can be expanded with specific attack scenarios, risk levels, and control mappings.

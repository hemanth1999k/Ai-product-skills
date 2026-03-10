---
name: soc1-soc2-overview
description: "Use when the user needs to understand SOC 1 or SOC 2 compliance, plan a SOC audit, or communicate security posture to enterprise customers. Triggers on: 'SOC 2', 'SOC1', 'SOC 2 Type II', 'security audit', 'trust service criteria', 'enterprise security compliance'."
---

# SOC 1 & SOC 2 Compliance Overview

## Purpose
Understand SOC compliance frameworks, what they require, and how to use them to build enterprise trust.

---

## SOC 1 vs SOC 2

| | SOC 1 | SOC 2 |
|---|---|---|
| Focus | Financial reporting controls | Security, availability, privacy controls |
| Audience | Customer auditors, financial statement auditors | Enterprise customers, prospects |
| Standards | SSAE 18 | AT-C 205 / TSC |
| Use case | Payroll processors, financial services | SaaS companies, cloud services |

**Most SaaS companies need SOC 2, not SOC 1.**

---

## SOC 2 Deep Dive

### Type I vs Type II
- **Type I**: Point-in-time. "Our controls are designed correctly as of [date]." Faster to achieve (2-3 months).
- **Type II**: Over time (typically 6-12 months). "Our controls operated effectively over the audit period." More credible; what most enterprises require.

Start with Type I if you have nothing; move to Type II for enterprise sales.

### Trust Service Criteria (TSC)

**Security (Required)** — The CC (Common Criteria) section
Core controls: Access control, encryption, vulnerability management, incident response, change management, vendor management

**Availability** (Optional add-on)
System availability commitments and SLAs

**Confidentiality** (Optional add-on)
Protection of confidential information

**Processing Integrity** (Optional add-on)
Complete, accurate, timely processing

**Privacy** (Optional add-on)
Personal information handling (aligned with GDPR/CCPA)

Most SaaS companies start with Security only, add Availability later.

### Key Controls Required for SOC 2 Security

**Access Control**
- [ ] Principle of least privilege enforced
- [ ] MFA required for all systems
- [ ] Privileged access management documented
- [ ] Access reviews performed quarterly
- [ ] Offboarding process removes access immediately

**Change Management**
- [ ] Code review process for all changes
- [ ] Separate environments (dev/staging/prod)
- [ ] Deployment approval process documented

**Risk Management**
- [ ] Annual risk assessment performed
- [ ] Vendor risk assessment process
- [ ] Penetration testing annually

**Incident Response**
- [ ] Incident response plan documented
- [ ] Incident classification criteria defined
- [ ] Notification procedures (customers, regulators)
- [ ] Post-incident review process

**Logical Access**
- [ ] User access provisioning/de-provisioning process
- [ ] Password policies enforced
- [ ] Encryption at rest and in transit

**Physical Security** (if applicable)
- Data center access controls
- (Cloud providers cover this via their own certs)

### SOC 2 Audit Process

1. **Readiness Assessment** (1-3 months): Gap analysis, identify what's missing
2. **Remediation** (2-6 months): Build missing controls, document policies
3. **Type I Audit** (1-2 months): Auditor tests design of controls at a point in time
4. **Observation Period** (6-12 months): Controls operate during audit window
5. **Type II Audit**: Auditor tests operating effectiveness
6. **Report Issued**: Shared with customers under NDA

### Tools for SOC 2 Compliance
- Vanta, Drata, SecureFrame, Tugboat Logic — automated evidence collection
- These integrate with your tech stack (AWS, GitHub, Okta) to continuously collect evidence

## HIPAA Quick Reference

If you handle Protected Health Information (PHI):
- HIPAA Security Rule: Administrative, physical, technical safeguards
- Business Associate Agreements (BAAs) with vendors
- Breach notification requirements
- SOC 2 helps but HIPAA requires additional controls

## Output Format
- SOC 2 applicability assessment
- Control gap analysis for key TSC areas
- 6-12 month roadmap to audit readiness
- What to tell enterprise customers during sales process

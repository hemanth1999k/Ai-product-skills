---
name: hipaa-basics
description: "Use when the user is building a healthcare product and needs to understand HIPAA compliance. Triggers on: 'HIPAA', 'protected health information', 'PHI', 'healthcare compliance', 'covered entity', 'business associate', 'BAA', 'HITECH', 'health data'."
---

# HIPAA Compliance Basics

## Purpose
Understand HIPAA requirements for products that handle Protected Health Information (PHI).

## Who Does HIPAA Apply To?

### Covered Entities (Directly subject to HIPAA)
- Healthcare providers who transmit health information electronically
- Health plans (insurers)
- Healthcare clearinghouses

### Business Associates (Your likely category if you're a vendor)
A Business Associate is any entity that creates, receives, maintains, or transmits PHI on behalf of a Covered Entity.
- EHR vendors
- Cloud storage providers hosting PHI
- Analytics companies processing patient data
- Any SaaS company used by a healthcare provider to handle patient data

**You are a Business Associate if** a healthcare provider uses your product and PHI is stored in or transmitted through your system.

## Business Associate Agreement (BAA)

A BAA is a legally required contract between the Covered Entity and Business Associate.
- You CANNOT handle PHI without a signed BAA
- The BAA defines: permitted uses of PHI, security obligations, breach reporting, access and audit rights
- Major cloud providers (AWS, Azure, GCP) offer HIPAA BAAs

## Protected Health Information (PHI)

PHI = Any health information that identifies (or could identify) an individual.

The 18 HIPAA identifiers:
- Name, geographic data, dates, phone/fax numbers, email addresses, SSN, medical record numbers, health plan beneficiary numbers, account numbers, certificate/license numbers, VINs, device identifiers, URLs, IP addresses, biometric identifiers, full-face photographs, any other unique identifying number

**De-identified data**: Remove all 18 identifiers → no longer PHI → HIPAA doesn't apply.

## HIPAA Security Rule (for Electronic PHI / ePHI)

### Administrative Safeguards
- [ ] Security Officer designated
- [ ] Risk analysis performed annually
- [ ] Workforce training on PHI handling
- [ ] Access management procedures
- [ ] Incident response procedures

### Physical Safeguards
- [ ] Facility access controls
- [ ] Workstation controls (clean desk, locked screens)
- [ ] Device and media controls (encryption, disposal policy)

### Technical Safeguards
- [ ] Access controls (unique user identification, automatic logoff)
- [ ] Audit controls (logging access to ePHI)
- [ ] Integrity controls (verify ePHI hasn't been altered improperly)
- [ ] Transmission security (encryption in transit)

## HIPAA Breach Notification Rule

A "breach" = unauthorized acquisition, access, use, or disclosure of unsecured PHI that compromises security/privacy.

**Timeline requirements:**
- Individuals: Notify within 60 days of discovery
- HHS: Notify within 60 days (or 60 days after end of calendar year for breaches < 500 individuals)
- Media: If breach affects > 500 in a state — notify prominent media within 60 days

## HIPAA vs HITECH
HITECH (2009) strengthened HIPAA:
- Extended HIPAA directly to Business Associates
- Increased penalties significantly
- Breach notification requirements added

## Penalties
- Tier 1 (unknowing): $100-$50,000 per violation
- Tier 2 (reasonable cause): $1,000-$50,000 per violation
- Tier 3 (willful neglect, corrected): $10,000-$50,000 per violation
- Tier 4 (willful neglect, uncorrected): $50,000 per violation
- Annual cap: $1.9M per violation category

## HIPAA Compliance Roadmap for SaaS Vendors

1. Determine if you're a Business Associate
2. Sign BAAs with your cloud infrastructure providers
3. Complete risk analysis
4. Implement required safeguards (admin, physical, technical)
5. Train workforce on HIPAA
6. Create breach response plan
7. Sign BAAs with your covered entity customers
8. Consider HITRUST certification for enterprise sales credibility

## Output Format
- HIPAA applicability assessment
- Required safeguards gap analysis
- BAA requirement checklist
- Breach response plan outline

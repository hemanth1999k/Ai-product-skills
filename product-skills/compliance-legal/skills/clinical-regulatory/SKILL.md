---
name: clinical-regulatory
description: "Use when the user is building a healthcare, clinical, or regulated product and needs to understand regulatory frameworks. Triggers on: 'clinical', 'regulatory', 'FDA', 'CE marking', 'medical device', 'clinical trial', 'IVD', 'SaMD', 'health product compliance', '510k', 'MDR'."
---

# Clinical & Regulatory Product Framework

## Purpose
Navigate the regulatory landscape for healthcare, clinical, and medical technology products.

## FDA Regulatory Pathways (US)

### Software as a Medical Device (SaMD)

The FDA classifies SaMD by risk:
- **Class I** (Low risk): General wellness, administrative tools. Most exempt from 510(k).
- **Class II** (Moderate risk): Most software medical devices. Requires 510(k) clearance.
- **Class III** (High risk): Life-sustaining, high-risk decisions. Requires PMA (Pre-Market Approval).

### Predicate Device Strategy (510(k))
Must show: "Substantially equivalent" to a legally marketed predicate device
Timeline: 3-12 months
Cost: $50K-$500K+ in prep; $19K-$300K+ in FDA fees

### De Novo Pathway
For novel low-to-moderate risk devices with no predicate.
Timeline: 12-24 months

### FDA Digital Health Guidance
**Clinical Decision Support (CDS):**
Software that helps clinicians make decisions:
- Patient-specific information displayed for clinician review → May be non-device (low risk)
- Automated recommendations without clinician review → More likely SaMD/regulated

**Examples NOT regulated by FDA:**
- Administrative software (scheduling, billing)
- General wellness apps (fitness, stress reduction)
- Software for transferring/displaying medical images (display only, no analysis)

**Examples typically regulated:**
- Software that diagnoses conditions
- Software that determines treatment dosage
- Software analyzing diagnostic images with clinical recommendations

### FDA Quality System Regulation (QSR / 21 CFR Part 820)
Requirements for medical device manufacturers:
- Design controls (documented design process, risk management)
- Production/process controls
- Document and record controls
- Corrective and preventive action (CAPA)
- Complaint handling
- Risk management (ISO 14971)

---

## EU Medical Device Regulation (MDR 2017/745)

Replaced MDD in May 2021. Stricter than predecessor.
Requires: CE marking for market access in EU.

### Key Changes from MDD to MDR
- More devices moved to higher risk class
- More clinical evidence required
- Post-market surveillance requirements increased
- Unique Device Identification (UDI) required

### Notified Body Assessment
For Class IIa, IIb, III devices: Required review by EU Notified Body (third-party auditor)

---

## Clinical Trial Basics

### Types of Trials
- **Phase I**: Safety, small group
- **Phase II**: Efficacy, larger group
- **Phase III**: Efficacy + safety vs standard of care, large
- **Phase IV**: Post-market surveillance

### GCP (Good Clinical Practice)
International standard for designing and conducting clinical trials:
- Protocol approval by IRB/Ethics Committee
- Informed consent from participants
- Data integrity requirements
- Adverse event reporting

### For SaMD Clinical Evidence
FDA expects clinical evidence for higher-risk SaMD:
- Analytical validation (does software perform as intended?)
- Clinical validation (does software achieve intended clinical purpose?)

---

## Compliance Implications for Product Teams

**Design Controls Required**
Document: User needs → Design inputs → Design outputs → Testing → Verification → Validation

**Risk Management (ISO 14971)**
For every intended use and reasonably foreseeable misuse:
- Identify hazards
- Estimate risk
- Evaluate risk acceptability
- Implement risk controls
- Verify controls work

**Post-Market Surveillance**
Monitor real-world performance after launch:
- Complaint handling system
- Vigilance reporting (serious incidents to regulator)
- Periodic safety update reports

## Output Format
- Regulatory pathway assessment for described product
- Applicable standards and frameworks
- Compliance gap analysis
- Next steps toward regulatory submission or certification

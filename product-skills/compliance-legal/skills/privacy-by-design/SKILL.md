---
name: privacy-by-design
description: "Use when the user wants to build privacy into their product architecture, run a Privacy Impact Assessment, or think through data minimization. Triggers on: 'privacy by design', 'privacy impact assessment', 'PIA', 'data minimization', 'DPIA', 'build privacy in', 'privacy first'."
---

# Privacy by Design

## Purpose
Embed privacy protections into product design decisions — not as a compliance checkbox after the fact, but as a fundamental design principle.

## The 7 Foundational Principles (Ann Cavoukian)

1. **Proactive, Not Reactive**: Prevent privacy breaches before they happen
2. **Privacy as Default**: Default settings must protect privacy; users shouldn't have to opt-in to protection
3. **Privacy Embedded into Design**: Not bolted on as an add-on
4. **Full Functionality**: Privacy AND function — not privacy OR function
5. **End-to-End Security**: Full lifecycle protection
6. **Visibility and Transparency**: Be open about practices; verifiable
7. **Respect for User Privacy**: Keep it user-centric

## Data Minimization Framework

Before collecting any data, ask:

1. **Do we need this data at all?**
   - What decision or feature does it enable?
   - Could we achieve the same goal without collecting it?

2. **Can we collect less?**
   - Range instead of exact value (age range vs date of birth)
   - Aggregate instead of individual (category vs specific behavior)
   - Derived instead of raw (age vs birthdate)

3. **Do we need to store it permanently?**
   - Define retention period upfront
   - Auto-delete after period
   - Anonymize after retention period

4. **Who needs access?**
   - Least privilege: only those who need it for their job
   - Audit logs for sensitive data access
   - Data segregation where possible

## Privacy Impact Assessment (PIA / DPIA)

Required under GDPR Article 35 for "high risk" processing.
Best practice for any new feature touching personal data.

### DPIA Questions to Answer:

**1. What data is being processed?**
Type of data, sensitivity level, volume

**2. Why is it being processed?**
Purpose and legal basis

**3. Who has access?**
Internal teams, third parties, subprocessors

**4. What are the risks?**
- Identity theft / fraud risk
- Reputational harm risk
- Financial harm risk
- Discrimination risk
- Loss of confidentiality

**5. What controls reduce each risk?**
- Technical controls (encryption, access control)
- Process controls (training, policy)
- Organizational controls (governance, review)

**6. Is residual risk acceptable?**
Risk after controls: Accept / Mitigate further / Consult regulator

### DPIA Triggers
Conduct a DPIA when you:
- Process health, financial, location data at scale
- Profile users in ways that affect their rights/decisions
- Process children's data
- Transfer data across borders
- Use automated decision-making with legal effects

## Privacy-Safe Architecture Patterns

**Pseudonymization**: Replace direct identifiers with tokens. Real identity stored separately.

**Anonymization**: Irreversibly remove ability to re-identify. True anonymization → no longer personal data under GDPR.

**Differential Privacy**: Add statistical noise to data so individual records can't be identified from aggregates.

**Data Vault Pattern**: Separate personal identity data from behavioral/usage data; join only when necessary.

**Consent Management**: Granular consent records with timestamp, version of privacy notice consented to.

## Output Format
- Data inventory for the described feature
- Privacy risk assessment
- Recommended privacy controls
- DPIA for high-risk processing activities

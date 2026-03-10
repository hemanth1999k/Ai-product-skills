---
name: compliance-audit
description: "Audit a product or feature for compliance requirements"
---

# /compliance-audit

Check which compliance frameworks apply and identify gaps.

## Usage
`/compliance-audit [product description + target markets + data types handled]`

## What This Command Does
Chains: `gdpr-ccpa-compliance` + `privacy-by-design` + relevant additional frameworks based on context.

Outputs: Applicable frameworks, gap analysis, priority actions.

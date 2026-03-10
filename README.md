# Product Skills Marketplace

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](CONTRIBUTING.md)

---

## The Story

I have been following **[Paweł Huryn](https://www.productcompass.pm)** for a while. His newsletter, his frameworks, the way he thinks about product work. When he showed the community how to build a skills marketplace, I wanted to build one for the way I actually work.

This one is for **AI product builders**: people who ship things using Claude Code, who are deep in the build, and who need structured thinking on demand, not a PM textbook.

My background is going through interview loops at **Meta and Google**, doing team match, and spending a lot of time studying what frameworks actually hold up under pressure versus which ones just sound good in a blog post. I also pull heavily from **[Lewis Lin](https://www.lewis-lin.com)** - his TROPIC framework for metric diagnosis is something I use constantly, and his approach to structured product thinking runs through a lot of what is in here.

This is the collection of everything I have found genuinely useful. It will keep growing. You can contribute too.

---

## Built for Claude Code First

This marketplace is designed primarily for **Claude Code**. Every skill and command is built to work inside your dev workflow, not as a separate PM tool you switch into.

Also supported: Claude Cowork, Cursor, Gemini CLI, Codex, Kiro.

---

## Quick Start

| You need to... | Run |
|---|---|
| Kick off a discovery cycle | `/discover` |
| Plan a research study | `/research-plan` |
| Diagnose a metric drop | `/diagnose-metric` |
| Rank your backlog | `/prioritize` |
| Write user stories | `/write-stories` |
| Run a launch checklist | `/go-no-go` |
| Check compliance requirements | `/compliance-audit` |
| Build a GTM plan | `/gtm-plan` |

---

## Installation

### Claude Code (Primary)
```bash
claude plugin marketplace add your-github-username/product-skills

claude plugin install discovery@product-skills
claude plugin install user-research@product-skills
claude plugin install metrics-analytics@product-skills
claude plugin install prioritization-goals@product-skills
claude plugin install product-execution@product-skills
claude plugin install release-qa@product-skills
claude plugin install compliance-legal@product-skills
claude plugin install market-strategy@product-skills
```

### Claude Cowork
1. Open **Customize** at the bottom left
2. Go to **Browse plugins > Personal > +**
3. Select **Add marketplace from GitHub**
4. Enter: `your-github-username/product-skills`

### Cursor / Gemini CLI / Codex / Kiro
```bash
# Cursor
for plugin in discovery user-research metrics-analytics prioritization-goals product-execution release-qa compliance-legal market-strategy; do
  cp -r "$plugin/skills/"* .cursor/skills/ 2>/dev/null
done

# Gemini CLI
for plugin in discovery user-research metrics-analytics prioritization-goals product-execution release-qa compliance-legal market-strategy; do
  cp -r "$plugin/skills/"* ~/.gemini/skills/ 2>/dev/null
done
```

---

## 8 Plugins, 58 Skills, 22 Commands

---

### 1. Product Discovery
*8 skills · 3 commands*

Structured ideation, assumption mapping, and validation methods before you commit to building.

| Skill | What It Does |
|---|---|
| `brainstorm-product-ideas` | 6-lens structured ideation |
| `first-principles-thinking` | Strip assumptions, rebuild from fundamentals |
| `opportunity-solution-tree` | OST framework (Teresa Torres) |
| `assumption-mapping` | VUBF risk classification and priority grid |
| `concept-testing` | Fake door, concierge, pretotype, Wizard of Oz |
| `product-brainstormer` | Opinionated thinking partner mode |
| `lean-validation-framework` | Build-Measure-Learn, MVP types, pivot taxonomy |
| `how-to-solve-issue` | 5D structured problem solving |

**Commands:** `/discover` `/brainstorm` `/validate-idea`

---

### 2. User Research
*9 skills · 3 commands*

Research planning, interview guides, synthesis, and every qualitative method you will actually use.

| Skill | What It Does |
|---|---|
| `research-plan` | Research brief, method selection, timeline |
| `user-interview-guide` | Interview scripts and probing techniques |
| `survey-design` | NPS, CSAT, CES, PMF survey frameworks |
| `persona-creation` | JTBD-grounded personas |
| `customer-journey-map` | Stages, touchpoints, emotions, opportunities |
| `research-synthesis` | Affinity mapping and insight generation |
| `qualitative-research-frameworks` | JTBD, contextual inquiry, diary studies, card sorting |
| `market-research` | TAM/SAM/SOM and competitive landscape |
| `usability-testing` | Moderated and unmoderated, SEQ scoring, task success |

**Commands:** `/research-plan` `/create-persona` `/synthesize-research`

---

### 3. Metrics and Analytics
*7 skills · 4 commands*

Proper experiment design, p-value interpretation, cohort analysis, and TROPIC for root cause analysis. Built on Lewis Lin's work.

| Skill | What It Does |
|---|---|
| `north-star-metric` | NSM selection, input metric tree, counter-metrics |
| `heuristic-evaluation` | Nielsen's 10 heuristics with severity scoring |
| `ab-test-design` | Sample size, hypothesis structure, guardrails |
| `multivariate-test-design` | Full and fractional factorial, interaction effects |
| `ab-test-analysis-pvalue` | p-value interpretation and ship/no-ship decision logic |
| `cohort-analysis` | Retention curves, activation analysis, curve diagnosis |
| `rca-tropic` | TROPIC framework for metric drops (Lewis Lin) |

**Commands:** `/define-metrics` `/design-experiment` `/analyze-results` `/diagnose-metric`

---

### 4. Prioritization and Goals
*6 skills · 2 commands*

Weighted RICE, Kano, Opportunity Scoring with Ulwick's ODI formula, and the short vs long-term tension framework.

| Skill | What It Does |
|---|---|
| `rice-prioritization` | Reach x Impact x Confidence / Effort |
| `weighted-scoring` | Custom multi-criteria scoring model |
| `short-long-term-goals` | 3-horizon framework and Now/Next/Later |
| `moscow-method` | Must/Should/Could/Won't for release scoping |
| `kano-model` | Basic, Performance, and Delighter classification |
| `opportunity-scoring` | Ulwick ODI: Importance + max(Importance minus Satisfaction, 0) |

**Commands:** `/prioritize` `/set-goals`

---

### 5. Product Execution
*9 skills · 3 commands*

Stories, backlogs, sprints, OKRs, pre-mortems. The daily work, done properly.

| Skill | What It Does |
|---|---|
| `user-story-creation` | INVEST criteria and Given/When/Then acceptance criteria |
| `job-story-creation` | When/Want/Can format (Alan Klement / JTBD) |
| `backlog-grooming` | Grooming process and definition of ready |
| `sprint-planning` | Capacity, goal-setting, story selection |
| `retrospective` | Start/Stop/Continue, 4Ls, Sailboat formats |
| `release-planning` | Cross-team coordination checklist |
| `go-no-go-decision` | 5-gate launch readiness framework |
| `pre-mortem` | Tigers, Paper Tigers, and Elephants |
| `okr-creation` | Committed vs stretch OKRs and health metrics |

**Commands:** `/write-stories` `/sprint` `/groom-backlog`

---

### 6. Release and QA
*6 skills · 3 commands*

Test plans, ship decisions, rollback runbooks. Written before you need them, not during the incident.

| Skill | What It Does |
|---|---|
| `qa-test-plan` | P0 to P3 classification and exit criteria |
| `ship-no-ship-logic` | Decision matrix and severity classification |
| `acceptance-criteria` | BDD Given/When/Then format |
| `bug-triage` | Priority and severity matrix with aging policy |
| `rollback-plan` | Criteria, runbook, rollback method selection |
| `test-scenario-generation` | Boundary analysis, equivalence partitioning, edge cases |

**Commands:** `/qa-plan` `/go-no-go` `/release-plan`

---

### 7. Compliance and Legal
*7 skills · 2 commands*

GDPR, CCPA, FERPA, HIPAA, SOC 2, clinical regulatory (FDA SaMD and EU MDR), and RFP creation. For when someone in a meeting asks if you are compliant with X.

| Skill | What It Does |
|---|---|
| `gdpr-ccpa-compliance` | GDPR principles, lawful bases, CCPA consumer rights |
| `ferpa-compliance` | Student data privacy for edtech vendors |
| `soc1-soc2-overview` | SOC 2 Type I and II, trust service criteria, audit roadmap |
| `rfp-creation` | RFP structure and vendor scoring matrix |
| `clinical-regulatory` | FDA SaMD pathways, EU MDR, GCP basics |
| `privacy-by-design` | 7 principles, DPIA, data minimization patterns |
| `hipaa-basics` | PHI, BAA requirements, security rule, breach notification |

**Commands:** `/compliance-audit` `/draft-rfp`

---

### 8. Market Strategy
*6 skills · 2 commands*

Beachhead selection, ICP definition, positioning, growth loops, and competitive analysis from first principles.

| Skill | What It Does |
|---|---|
| `gtm-strategy` | GTM motion, channel strategy, launch readiness |
| `ideal-customer-profile` | Firmographic, behavioral, and situational ICP scoring |
| `competitive-analysis` | Landscape mapping, win/loss framework, intel sources |
| `value-proposition` | Value Proposition Canvas and positioning statement formula |
| `growth-loops` | Viral, content, network effect, paid, and sales loops |
| `beachhead-segment` | First-market selection with expansion path |

**Commands:** `/gtm-plan` `/competitive-scan`

---

## Orchestration Commands

Several commands chain multiple skills into a single workflow:

| Command | What Gets Chained |
|---|---|
| `/discover` | brainstorm-product-ideas, first-principles-thinking, assumption-mapping, concept-testing |
| `/gtm-plan` | beachhead-segment, ideal-customer-profile, value-proposition, gtm-strategy |
| `/qa-plan` | qa-test-plan, test-scenario-generation, acceptance-criteria |
| `/compliance-audit` | gdpr-ccpa, privacy-by-design, and relevant additional frameworks |
| `/set-goals` | okr-creation, short-long-term-goals |

---

## Credits

This marketplace encodes frameworks from people whose work I come back to again and again:

- **Lewis Lin** - TROPIC Metrics Framework and structured product thinking at [lewis-lin.com](https://www.lewis-lin.com)
- **Paweł Huryn** - The PM Skills Marketplace that showed what this format could be at [productcompass.pm](https://www.productcompass.pm)
- **Teresa Torres** - Continuous Discovery Habits and the Opportunity Solution Tree
- **Marty Cagan** - INSPIRED and TRANSFORMED
- **Alberto Savoia** - The Right It and pretotyping
- **Anthony Ulwick** - Outcome-Driven Innovation and Opportunity Scoring
- **Alan Klement** - When Coffee and Kale Compete, Job Stories
- **Ann Cavoukian** - Privacy by Design
- **Geoffrey Moore** - Crossing the Chasm and beachhead strategy
- **Sean Ellis** - Hacking Growth and the PMF survey
- **Ash Maurya** - Running Lean and Lean Canvas
- **Noriaki Kano** - Kano Model
- **Jakob Nielsen** - 10 Usability Heuristics
- **Gary Klein** - Pre-mortem methodology
- **Jeff Patton** - Story Mapping

---


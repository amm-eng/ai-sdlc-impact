# AI SDLC Impact Framework — Overview

## What this framework is for

This framework evaluates whether an AI-enabled change improves the delivery of valuable software for a **defined team, service, workflow, and task class**. It is designed for team-, service-, or initiative-level decisions—not for ranking individual developers.

Its primary focus begins after the problem or opportunity and solution direction are established. It assesses AI-enabled work from technical solution definition through implementation, delivery, and operation: how software is planned, built, verified, released, and run. It does not assess problem discovery and prioritisation (**why build**) or product/solution ideation and selection (**what to build**). Those earlier stages should establish the intended outcome, task class, and acceptance criteria before an assessment begins.

Product or customer outcomes may still be used as downstream evidence of impact. The framework does not, however, determine whether the underlying problem or chosen solution was the right one.

Its governing rule is:

> Claim a positive AI productivity impact only when a meaningful outcome improves **and** quality, reliability, security, developer experience, and unit economics remain within pre-agreed guardrails.

AI adoption, accepted code, token use, licence allocation, and raw output are useful exposure or diagnostic signals. They do not, by themselves, demonstrate value or ROI.

## Definition of AI SDLC

In this framework, **AI SDLC** means building and delivering software with AI assistance. It includes assistive and agentic capabilities used across software delivery—for example, planning, coding, review, testing, release, and operations—where they affect the delivery of software.

It does not mean the lifecycle for building AI or ML models.

## The framework at a glance

`AI intervention → effective exposure and delivery mechanisms → verified delivery or value outcome → safe, sustainable, economic decision`

| Layer | Question it answers | Evidence to use |
|---|---|---|
| **1. Study frame** | What changed, for whom, and compared with what? | Intervention definition, task class, population, baseline/comparator, observation window, success hypothesis, decision owner. |
| **2. Exposure and mechanisms** | Did the intended AI use occur, and where does work flow or stall? | Effective AI use by task category/mode/autonomy, complexity-adjusted throughput, review capacity (time to first review and review turnaround), CI queues, batch size, test feedback, context readiness, developer friction. |
| **3. Primary outcomes** | Did valuable delivery improve? | Lead time for a defined change class, verified feature velocity, flow efficiency, capacity conversion, product/customer outcome, onboarding, developer effectiveness. |
| **4. Guardrails** | Was the outcome achieved safely and sustainably? | Reliability and recovery, SLOs, code/change health, security/privacy, compliance/provenance, human sustainability, economic safety. |
| **5. Decision** | What should happen next? | Pre-agreed thresholds applied without allowing a speed gain to offset a material safety or human-cost regression. |

## Assessment modes

| Mode | Use it when | What it can support |
|---|---|---|
| **Exploratory assessment** | You need a directional view of what changed after AI use and do not yet have a specific outcome or hypothesis to test. | Identifies signals, bottlenecks, and candidate hypotheses for a later outcome-driven assessment. It does not establish attribution, ROI, or a positive productivity claim on its own. |
| **Outcome-driven assessment** | You need to decide whether a defined AI intervention improved a specified outcome. | Tests a pre-defined hypothesis using a primary outcome, a credible comparison, and pre-agreed guardrails and thresholds. |

Both modes require a defined team, task class, intervention, observation window, exposure measure, and appropriate guardrails. Exploratory assessment may use before/after evidence to guide the next question; it should not alone justify scaling an intervention.

## How to apply it

1. **Choose a mode and define the use case before measuring.** Specify the tool/model or agent, enabled capabilities, task class, context/data access, policy and training changes, rollout date, and accountable decision owners. Outcome-driven assessment also defines the outcome and hypothesis in advance.
2. **Choose a credible comparison.** Prefer a phased rollout or matched teams/workflows. If only before/after data is available, compare similar work in both periods—for example, low-risk API changes of comparable complexity in the same service. Avoid comparing routine maintenance before AI with complex feature development afterward. Record other changes that could explain the result, such as holidays or release freezes, incidents, team size or experience, roadmap priorities, and platform upgrades; adjust for them where possible and explain any remaining attribution limits.
3. **Measure a compact, balanced scorecard.** For outcome-driven assessment, select one primary value outcome, one delivery/flow outcome, the required guardrails, and enough exposure/mechanism data to explain the result. For exploratory assessment, use candidate value or delivery signals, flow data, exposure, and guardrails to identify what should be tested next.
4. **Segment and inspect distributions.** Compare like with like—feature, maintenance, incident, migration, risk, service, and task complexity. For duration, size, and other distribution-based metrics, report at least P50 (median) and P75 (75th percentile), with P85/P90 where additional tail visibility is needed. Report rates and proportions in their appropriate form.
5. **Make an appropriate decision.** In outcome-driven assessment, apply the pre-agreed thresholds. In exploratory assessment, turn signals into a focused hypothesis or identify a constraint to address. Do not use a single weighted productivity score. A serious security, privacy, compliance, or reliability regression vetoes a positive productivity claim.

## Minimum metric set

This is the minimum metric set for a typical AI-assisted delivery case, summarized by area, and should be tracked every reporting period. For definitions, units, categories, and collection methods, see the [metric reference](ai-sdlc-metric-reference.md).

| Area | Minimum measures |
|---|---|
| **Value and flow** | One primary value outcome (verified feature/initiative velocity or scoped lead time), complexity-adjusted throughput, P50/P75 lead time plus P85/P90 tail visibility, time to first review (P50/P75), review turnaround, and CI queue time. |
| **Capacity and people** | Reclaimed-capacity allocation or innovation ratio, plus a short ease-of-delivery / valuable-work / friction pulse. |
| **Reliability and change health** | Change failure rate, recovery or rollback, relevant SLO/error-budget state, batch size, rework/revert/escaped-defect rate, and change confidence. |
| **Security and governance** | Security/privacy policy events and required approvals, traceability, and provenance. |
| **Economics** | Incremental AI cost and cost per verified accepted task, release, or customer outcome. |
| **Exposure and diagnosis** | AI use by task category/mode/autonomy, test-feedback health, and—when agents are involved—context freshness/ownership, escalation rate, and token/tool cost. |

## Outcome-driven focus areas

Keep the minimum metric set as the baseline for every focus area. Select one primary outcome for the hypothesis, retain the other baseline measures, and add metrics only where they help test or explain that hypothesis. Baseline delivery/value measures remain required even when the primary outcome concerns developer experience or quality.

| Focus area | Possible primary outcome | Additional metrics, when the hypothesis requires them |
|---|---|---|
| **DevEx outcomes** | Developer satisfaction, focus time (deep work), or perceived ease of delivery. | A specific DX driver, such as debugging or documentation friction; valuable-work feedback. |
| **Product delivery outcomes** | Lead time for a defined change class, verified feature/initiative velocity, or innovation ratio. | Verified task completion rate; deployment frequency for release-flow studies; onboarding time for onboarding studies. |
| **Product quality outcomes** | Change failure rate, code maintainability, or a specifically defined code-quality measure. | Escaped-defect or corrective rework/reopening rate; automated test and blocking-check coverage for verification studies. |

Choose one primary metric from the relevant row; the listed candidates are alternatives, not a requirement to collect them all. Apply these interpretation rules:

- **Developer satisfaction and DXI are distinct.** Satisfaction measures developer sentiment; DXI is an instrument-defined index of developer experience. An existing DXI may be selected as a separate primary metric, using its provider's definition. Do not relabel it as satisfaction.
- **Focus time means time spent in concentrated, uninterrupted work.** Use a consistent survey estimate or sampled diary, define what qualifies as a focus block, and report it as estimated deep-work time. It does not establish time saved by AI or valuable output on its own.
- **Innovation ratio measures capacity allocation.** A higher share of engineering time spent on new capabilities can support a capacity-conversion hypothesis, but does not establish faster delivery or greater customer value. Retain the baseline delivery and maintenance guardrails.
- **Task completion rate requires verified acceptance.** Use a fixed eligible task cohort and equal follow-up windows; record unfinished, failed, and cancelled tasks explicitly. A tracker status or agent completion claim alone is insufficient.
- **Code quality must name the attribute and measure.** Code maintainability is one quality attribute. A maintainability or quality survey measures perception; a static-analysis measure covers the configured property. Neither establishes overall product quality. Pair it with the baseline defect and reliability evidence.
- **Change failure rate needs enough observed changes.** Report failed/total changes and compare similar risk classes over consistent follow-up windows. Zero failures in a small sample does not establish improved quality.

### Recommended guardrails by focus area

Use these baseline metrics to check for costs transferred to another part of delivery. Agree a tolerance and an action for each selected guardrail before examining intervention results. These recommendations emphasise particular risks; they do not replace the remaining baseline guardrails.

| Focus area | Guardrail metrics to emphasise | What they protect |
|---|---|---|
| **DevEx outcomes** | Scoped lead time (P50/P75); escaped-defect or corrective rework/reopening rate; work-intensity feedback. | An easier developer experience should not conceal slower delivery, poorer output, or increased workload. |
| **Product delivery outcomes** | Change failure rate; escaped-defect or corrective rework/reopening rate; work-intensity and change-confidence feedback. | Faster delivery or greater allocation to innovation should not create failures, deferred corrective work, or unsustainable verification pressure. |
| **Product quality outcomes** | Scoped lead time (P50/P75); perceived ease of delivery; work-intensity feedback. | Quality improvements should not rely on unacceptable delivery delays, friction, or workload. |

**Shared across all focus areas:** security/privacy events and required approval coverage; relevant SLO/error-budget state and recovery/rollback evidence for production-impacting work; incremental AI cost and cost per verified outcome. Apply existing obligations and service objectives, and agree economic tolerances for the assessment.

A metric can be a primary outcome in one assessment and a guardrail in another; collect it once. Use the same task class, denominators, survey wording, and observation rules across comparison periods. Separate escaped defects by severity and use a consistent follow-up window. Missing guardrail evidence is unknown, not a pass.

If an outcome improves while a guardrail exceeds its tolerance, constrain the use case and investigate before scaling. A material security, privacy, compliance, SLO, or reliability breach retains the framework's stop/rollback rule. Use baseline review and CI evidence to diagnose constraints; expand the diagnostics only where the hypothesis or results require it.

## Decision rules

| Evidence pattern | Framework decision |
|---|---|
| Primary delivery/value outcome improves; guardrails are stable or better; unit economics are acceptable | **Scale cautiously**, validate across task types and teams, and keep monitoring lagging risks. |
| Leading indicators improve, but the primary outcome is flat | **Diagnose before scaling.** Gains may be trapped in review, CI/CD, requirements, meetings, or maintenance. |
| Speed or throughput improves while reliability, code health, security, or developer experience worsens | **Do not claim productivity.** Constrain scope/autonomy, improve verification/context/rollback, and retest. |
| AI adoption or AI-authored-code share rises without verified outcome movement | **No impact established.** Treat this as enablement data, not ROI. |
| A material security, privacy, compliance, SLO, or reliability breach occurs | **Stop or roll back the affected use case** until safeguards and human review are corrected. |

## Interpretation principles

- **Impact is not activity.** Higher usage, accepted LOC, prompts, tokens, or PR counts can coexist with poorer customer value, reliability, or developer experience.
- **The system is the unit of improvement.** A coding gain is not a delivery gain if it creates a review, CI, testing, operational, or coordination bottleneck downstream.
- **Context is a moderator for agentic work.** Clear, actionable, current, efficient, and secure context can explain outcome differences; it is not a productivity score on its own.
- **Correlation is not attribution.** Observational pre/post evidence should state its limits and never assume that AI alone caused a change.
- **Avoid individual surveillance.** Use aggregate team/service data and protect psychological safety.

## Reporting template

For each case, publish one concise before/after/comparator table:

| Metric group | Baseline | Intervention period | Comparator / adjusted delta | Guardrail status | Interpretation |
|---|---:|---:|---:|---|---|
| AI exposure and task mix |  |  |  | Informational | Did the intended change actually occur? |
| Primary value outcome |  |  |  | Required | Is there evidence of more valuable delivery? |
| Flow and experience outcomes |  |  |  | Required | Did the system, not only code generation, improve? |
| Reliability and code health |  |  |  | Hard gate | Was output delivered safely and sustainably? |
| Security/compliance |  |  |  | Hard gate | Was risk acceptable? |
| Cost and capacity conversion |  |  |  | Required for ROI | Did savings become value at acceptable cost? |

Report confidence limits and caveats: sample size, missing data, work-mix changes, concurrent platform/process changes, and whether the evidence is observational rather than causal. Do not sum unlike measures into a synthetic “AI productivity score.”

For definitions of each metric, why it matters, its category and units, and how to collect it from system or survey data, use the [metric reference](ai-sdlc-metric-reference.md).

## Source basis

The framework draws on these key sources:

- [DORA — Impact of Generative AI in Software Development (2025)](https://dora.dev/ai/gen-ai-report/).
- [DORA — State of AI-assisted Software Development (2025)](https://dora.dev/research/2025/dora-report/).
- [DX — State of AI Impact in Engineering: Q2 Report (2026)](https://getdx.com/report/state-of-ai-impact-in-engineering-q2-report/).
- [DX — State of AI Impact in Engineering: Q3 Report (2026)](https://getdx.com/report/state-of-ai-impact-in-engineering-q3-report/).
- [CAFE(S): Your Agent Is Only As Good As Its Context](https://queue.acm.org/doi/10.1145/3847288).

The framework draws on the baseline sources listed above and was informed and iterated through production observations across multiple DevOps cloud-native teams and one team application to assess AI impact.

---

*Created by [@amm-eng](https://github.com/amm-eng). Released under the [MIT License](LICENSE).*

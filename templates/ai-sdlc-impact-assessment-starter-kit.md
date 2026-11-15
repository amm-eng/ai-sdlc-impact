# AI SDLC Impact Assessment Starter Kit

Use one copy of this template for one defined AI-enabled use case. Complete it before the assessment begins; keep unknown fields explicit rather than filling them with estimates.

| Mode | Use it when | Output |
|---|---|---|
| **Exploratory assessment** | You need a directional view of what changed after AI use and do not yet have a specific outcome or hypothesis. | Candidate hypotheses and constraints to investigate. It does not prove AI impact or justify scaling by itself. |
| **Outcome-driven assessment** | You need to validate a defined outcome or hypothesis. | Evidence for a decision to scale, adjust, constrain, or stop. |

## 1. Assessment frame

| Field | Record |
|---|---|
| Assessment name |  |
| Assessment mode | Exploratory or outcome-driven. |
| Outcome focus area | Outcome-driven: DevEx, product delivery, or product quality. |
| Primary outcome metric | Outcome-driven: choose one metric from the focus-area guidance and specify its instrument, unit, and definition. Distinguish satisfaction from DXI, estimated focus time from time saved, and a named code-quality attribute from overall quality. |
| Decision to support | Exploratory: what should be investigated next? Outcome-driven: scale, adjust, constrain, stop, or another defined decision. |
| Decision owner |  |
| Team, service, and workflow |  |
| AI intervention | Tool/model, enabled capabilities, autonomy level, context/data access, policy or training changes, and rollout date. |
| Eligible task class | Include:  \\ Exclude:  |
| Assessment window | Baseline:  \\ Intervention:  |
| Exploratory question | Exploratory mode: What changed after AI use, and what needs further investigation? |
| Outcome to assess | Outcome-driven mode: What should be better if this use case succeeds? Example: Low-risk API changes reach verified production sooner without a higher change-failure rate. |
| Hypothesis to test | Outcome-driven mode: We expect ___ used for ___ tasks to improve ___ because ___. Example: We expect AI assistance for tests on low-risk API changes to reduce lead time because it speeds up test creation. |
| Concurrent changes or known confounders | Staffing, roadmap, process, platform, incident, or release changes. |

## 2. Comparison

| Field | Record |
|---|---|
| Comparison method | Phased rollout, matched team/workflow, or before/after. |
| Comparator or baseline population |  |
| How work will be made comparable | Task class, complexity, risk, service, and other matching rules. |
| Attribution limits | What this design cannot establish. |

## 3. Evidence plan

Use the overview's [minimum metric set](../ai-sdlc-impact-framework-overview.md#minimum-metric-set) as the baseline. For outcome-driven assessment, select one primary outcome and use the [focus-area guidance](../ai-sdlc-impact-framework-overview.md#outcome-driven-focus-areas) to identify guardrails and any additional metrics needed for the hypothesis. For exploratory assessment, use candidate value or delivery signals without a pre-defined primary hypothesis.

Record the baseline measures and any additions below, using one metric per row and repeating rows as needed.

| Role | Metric and operational definition | Source | Owner | Cadence |
|---|---|---|---|---|
| Primary outcome / candidate signal |  |  |  |  |
| Flow outcome |  |  |  |  |
| AI exposure |  |  |  |  |
| Reliability / change-health guardrail |  |  |  |  |
| Security / governance guardrail |  |  |  |  |
| Developer-experience guardrail |  |  |  |  |
| Economic measure |  |  |  |  |

For each selected metric, record its unit, numerator and denominator where relevant, time convention, exclusions, treatment of unfinished work, and known missing data. Use the [metric reference](../ai-sdlc-metric-reference.md) for collection guidance.

## 4. Guardrails and decision rules

Agree these before examining intervention results.

Use the [recommended guardrails by focus area](../ai-sdlc-impact-framework-overview.md#recommended-guardrails-by-focus-area) together with the shared guardrails. Record each metric's tolerance, action, and owner; missing evidence is unknown, not a pass.

| Condition | Threshold | Resulting action | Decision owner |
|---|---|---|---|
| Outcome-driven: Primary outcome improves and guardrails remain acceptable |  | Scale cautiously |  |
| Exploratory: Directional signals change and guardrails remain acceptable |  | Form a focused hypothesis or outcome-driven assessment; do not scale on this evidence alone |  |
| Outcome-driven: Leading or flow evidence improves but primary outcome does not |  | Diagnose the constraint before scaling |  |
| A guardrail regresses beyond tolerance |  | Constrain the use case and retest |  |
| Material security, privacy, compliance, SLO, or reliability breach |  | Stop or roll back the affected use case |  |

## 5. Reporting record

| Metric group | Baseline | Intervention | Comparator / adjusted delta | Guardrail status | Interpretation |
|---|---:|---:|---:|---|---|
| AI exposure and task mix |  |  |  | Informational |  |
| Primary outcome / candidate signals |  |  |  | Required for outcome-driven; diagnostic for exploratory |  |
| Flow outcome |  |  |  | Required |  |
| Reliability and change health |  |  |  | Hard gate |  |
| Security and governance |  |  |  | Hard gate |  |
| Developer experience and economics |  |  |  | Required |  |

**Decision:**
**Confidence and limitations:** Sample size, missing data, work-mix differences, concurrent changes, and attribution limits.
**Next review date:**

---

*Created by [@amm-eng](https://github.com/amm-eng). Released under the [MIT License](../LICENSE).*

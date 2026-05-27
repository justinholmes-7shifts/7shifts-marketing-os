# Lifecycle & Campaign Strategy: Reference

Detailed frameworks. The core principles, the design framework, and the pressure test live in SKILL.md. Consult these when the work calls for them.

## Measurement: the five layers

A complete measurement plan touches all five. Most underperforming campaigns are missing Lift and Health, which is how teams convince themselves a campaign worked when it didn't.

| Layer | Question it answers | Example metrics |
|---|---|---|
| **Outcome** | Did this drive the business result? | Revenue, paid conversions, units added, plan upgrades |
| **Lift** | Was the result incremental to what would have happened anyway? | Holdout performance, geo-split deltas |
| **Behavior** | Did the customer take the action we asked for? | Conversion rate, handraisers, trial starts |
| **Engagement** | Did the customer interact with the campaign? | Open, click, modal acknowledged |
| **Health** | Did anything break? | Unsubscribe rate, complaint volume, support tickets |

## Incrementality

A campaign that can't prove lift over a control reports correlation, not causation. Holdout methodology is the default for any program big enough to influence the half-year plan. Geo-split or time-series methods are fine when holdouts aren't technically feasible. If a program is too small to warrant incrementality testing, that itself is a strategic signal worth naming.

## Pillar and tentpole architecture (how campaigns ladder into a plan)

A half-year plan is not a list of campaigns. It is a small number of tentpoles, each driving a single business outcome, supported by smaller work.

| Bucket | Purpose | Capacity |
|---|---|---|
| **Tentpoles** | The 2-3 integrated campaigns the half is built around. Each ladders to one business outcome. | High. Cross-functional, multi-channel. |
| **Foundational must-dos** | Enablement that unblocks the tentpoles (segmentation, ICP, measurement, content infrastructure). Not customer-facing. | Real, often underestimated. |
| **New builds** | Net-new initiatives committed this half outside the tentpoles. | Medium. |
| **Iterations** | Already-running programs being evolved. | Lower per item, adds up. |
| **Backlog** | On the radar, not committed. Picked up if capacity opens. | Zero until promoted. |

A plan with five tentpoles is a wish list, not a plan.

## Optimization decision matrix

| Signal | Interpretation | Action |
|---|---|---|
| Hitting target, low effort to maintain | Healthy evergreen | Keep, light iteration |
| Hitting target, high effort to maintain | Working but expensive | Audit cost. Is the outcome worth the capacity. |
| Missing target, fixable diagnosis | Recoverable | Evolve. One sharp change, measure. |
| Missing target, no clear diagnosis | Unclear why | Pause or kill. Don't keep adjusting blindly. |
| Hitting target but no longer strategic | Successful but irrelevant | Retire. Capacity goes elsewhere. |
| No measurement plan, can't tell either way | Strategic risk | Add measurement now or retire. |

## Cross-functional partners: who to pull in, and when

Pull partners in once the problem and audience are clear, before channel and copy decisions. Too early creates noise. Too late creates rework.

| Partner | Bring them in for | By step |
|---|---|---|
| **PMM** | ICP definition, positioning, plan-tier comparisons, messaging sign-off | Step 1 (problem) + Step 6 (channel) |
| **Sales** | Audience overlap, active-account flagging, cadence conflicts, motion handoff | Step 2 (audience) + Step 7 (dependencies) |
| **Data / Engineering** | Eligibility queries, segmentation logic, routing, measurement instrumentation | Step 2 + Step 5 |
| **Product** | Native vs lifecycle ownership, paywall logic, in-product boundaries | Step 6 (when in-app is involved) |
| **CS / Onboarding** | Churn-risk signal, suppression, post-add activation handoff | Step 7 |

## What "useful" looks like when reviewing a plan

- **Frameworks before opinions.** Run it through the design framework and the pressure test before commenting on copy or channel.
- **Name the gap, don't just reorganize what's there.** Identify what's missing (a measurement plan, a kill condition, an audience definition).
- **Pressure-test against the operating rules.** If it breaks one, name it and propose the alternative.
- **Plain-language critique.** No marketing-isms. It should make sense to Sales, Data, PMM, and leadership without translation.
- **Offer the redirect, not just the no.** If it's not ready, say what would make it ready, with specific edits.

# Metrics

Metrics are **instruments, not trophies**. We use them to learn, steer, and keep trust high—never to micromanage. Every number has human context, an owner, and an action when it drifts. Dashboards are public by default; personal data is minimized.

---

## What we measure (five pillars)

1. **Collaboration Flow** — how quickly ideas become decisions and merges.  
2. **Recognition Health** — whether valuable work is seen and rewarded fairly.  
3. **Synergy & Adoption** — how often work becomes reusable building blocks.  
4. **Quality & Safety** — defects avoided, incidents contained, and security handled.  
5. **Governance & Culture** — participation quality and decision hygiene.

---

## Core metrics (definitions, formulas, actions)

> “Epoch” = weekly unless noted. Median is preferred over mean when distributions are skewed.

### 1) Recognition Velocity (RV)
- **What:** Kudos issued per active contributor per epoch.
- **Formula:** `RV = Kudos_total_epoch / Active_contributors_epoch` (report median and p75 across teams)
- **Source:** Recognition epochs, repo activity.
- **Target guardrail:** Flat or gently rising; sudden spikes/zeros investigated.
- **When red:** Check invisible work, reviewer bottlenecks, or spam PRs. Add teaching multiplier where docs unblocked others.

### 2) Synergy Index (SI)
- **What:** Downstream adoption of recognized assets.
- **Formula:** Weighted adoptions within 60 days / recognized assets, weighting by team count and criticality.  
  `SI = Σ(adoptions_weighted) / Assets_recognized`
- **Source:** Dependency graph, imports, API call telemetry, template forks.
- **When red:** Raise reuse incentives, split monoliths into components, write “adopt in 5 min” guides.

### 3) Coordination Latency (CL)
- **What:** Time from Decision Brief → ADR Accepted.
- **Formula:** `CL = median(ADR.accepted_at - Brief.created_at)` (by blast radius)
- **Source:** RFC/ADR index.
- **Targets:** Local ≤ 5 days; Cluster ≤ 14 days; Project-wide ≤ 21 days.
- **When red:** Steward sets time-boxed trials; tighten reviewer SLAs; clarify constraints.

### 4) Review SLA Hit Rate (RHR)
- **What:** % of reviews responded to within SLA (48h local / 72h cluster / 5d project-wide).
- **Formula:** `RHR = on_time_reviews / total_reviews`
- **Source:** PR events.
- **When red:** Add/rotate reviewers, split PRs, escalate to steward.

### 5) Trust Integrity (TI)
- **What:** Ratio of upheld vs. reversed recognition/attestations after appeals/audits.
- **Formula:** `TI = (Upheld_decisions) / (Upheld + Reversed)`
- **Source:** Recognition epochs, audit logs.
- **When red:** Strengthen evidence requirements; adjust multipliers; add random audits.

### 6) Time to First Merge (TTFM)
- **What:** Newcomer onboarding speed.
- **Formula:** `median(first_merge_at - first_issue_comment_at)` (rolling 90 days)
- **Target:** ≤ 7 days for docs/design; ≤ 14 days for code.
- **When red:** Improve “good first issues,” starter kits, and mentorship.

### 7) ADR Reopen Rate (ARR)
- **What:** % of ADRs reopened within 60–90 days for missing evidence or drift.
- **Formula:** `ARR = reopened_ADRs / total_ADRs`
- **Healthy:** Low, but not zero (we welcome learning).
- **When red:** Require clearer constraints, experiment plans, and sunset reviews.

### 8) Dispute Cycle Time (DCT)
- **What:** Steward responsiveness and conflict resolution speed.
- **Formula:** `DCT = median(outcome_note_at - steward_ping_at)`
- **Target:** ≤ 7 days.
- **When red:** Add stewards; enforce intervention ladder.

### 9) Visibility-to-Value (V2V)
- **What:** Share of Kudos for “soft work” (docs, onboarding, mediation, education).
- **Formula:** `V2V = Kudos_soft / Kudos_total`
- **Target band:** 25–45% (depends on current phase).
- **When red:** Recognize soft work explicitly; add teaching multiplier.

### 10) Change Failure Rate (CFR)
- **What:** % of merged changes that cause rollback/patch within 7 days.
- **Formula:** `CFR = (rollbacks + hotfixes) / merges`
- **When red:** Improve tests, pre-merge checks, and ADR risk sections.

### 11) MTTA / MTTP (Security)
- **What:** Mean Time to Acknowledge / Patch valid security reports.
- **Formula:**  
  `MTTA = avg(first_response - report_received)`  
  `MTTP = avg(patch_release - report_received)`
- **Targets:** Acknowledge ≤ 24–48h; patch according to severity table.
- **When red:** Expand VSL process, rehearse upgrades, add runbooks.

### 12) Experiment Yield (EY)
- **What:** % of parallel trials that produce reusable assets (patterns, tests, docs) even when they “lose.”
- **Formula:** `EY = Trials_with_reusable_output / Trials_total`
- **Target:** ≥ 70%.
- **When red:** Require “what remains reusable” in ADRs; apply teaching bonus.

---

## Dashboard anatomy

- **Top strip:** RV, SI, CL (by blast radius), RHR, TI.
- **Contributor funnel:** Newcomers → first issue → first merge → sustained contributors.
- **Synergy map:** heatmap of adoption across teams/repos.
- **Quality & safety:** CFR trend, MTTA/MTTP, open advisories.
- **Governance:** ADR statuses, reopen rate, dispute cycle time.
- **Recognition:** distribution by lane (build/docs/design/community/governance).

Dashboards link to underlying issues/PRs/ADRs so every number is explainable.

---

## Data sources (minimal, auditable)

- Git hosting events (issues, PRs, reviews, merges)
- RFC/ADR index (timestamps, owners, status)
- Recognition epochs (Kudos by lane, multipliers)
- Dependency graphs / package registries
- CI telemetry (tests, failures)
- Security mailbox & advisory register (KUDSEC IDs)

We avoid storing PII. Aggregations are public; raw data that could identify individuals is minimized or summarized.

---

## Metric hygiene (to avoid Goodhart’s Law)

- **Pair metrics.** Velocity with quality; recognition with integrity; adoption with teachability.
- **Version metrics.** If definitions change, bump a version and annotate the dashboard.
- **Explain anomalies.** Require a short note for large swings; celebrate *learning*, not just green numbers.
- **No per-person leaderboards.** We measure *systems*, not popularity contests.

---

## Targets by phase (example bands)

| Phase | RV | CL (Local/Cluster/Proj) | V2V | CFR | SI |
|---|---:|---:|---:|---:|---:|
| Bootstrap | ↑ fast | 5d / 14d / 21d | 35–45% | ≤ 10% | 0.6–0.9 |
| Growth | steady ↑ | 4d / 12d / 18d | 30–40% | ≤ 7% | 0.9–1.3 |
| Scale | stable | 3d / 10d / 15d | 25–35% | ≤ 5% | 1.2–1.8 |

(*Illustrative—set real targets after 2–3 months of baseline data.*)

---

## How metrics drive action

- **Steward reviews (weekly):** DCT, RHR, CL outliers → interventions or rotations.
- **Recognition calibration (bi-weekly):** V2V, TI → adjust multipliers and audit samples.
- **Roadmap reviews (monthly):** SI, EY → invest in frameworks/patterns with highest reuse.
- **Postmortems (as needed):** CFR, security metrics → tests/runbooks/kill-switches updated.

Every review produces a short note with owners and due dates.

---

## Example queries (pseudo)

-- Recognition Velocity (weekly)
SELECT week, median(kudos/active_contributors) as rv
FROM recognition_epochs
GROUP BY week;

-- Coordination Latency by blast radius
SELECT radius, median(adr_accepted_at - brief_created_at) as cl_days
FROM decisions
WHERE status = 'Accepted'
GROUP BY radius;

-- Review SLA hit rate
SELECT count_if(response_time <= sla) / count(*) as rhr
FROM reviews;

---

## Glossary (quick)

- **ADR:** Architecture/Approach Decision record.  
- **Blast radius:** How many teams/users are affected by a decision.  
- **Epoch:** Weekly cadence for recognition and reporting.  
- **Kudos:** Recognition units for verified impact.  
- **Trust Integrity:** Consistency and fairness of recognition over time.

---

## Change control for metrics

Propose metric additions/changes via RFC, including:
- Definition, formula, and data source
- Why it matters and likely failure modes
- Where it appears on the dashboard
- Privacy review (if applicable)

Accepted changes bump the **Metrics Spec** version and add a changelog entry.

---

**Bottom line:** We measure to learn and align—so that recognition stays fair, collaboration stays fast, and what we build gets reused widely and safely. If a metric doesn’t help us improve, we change or remove it.
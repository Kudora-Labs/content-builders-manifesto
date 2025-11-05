# Decision-Making

We decide in ways that keep us fast, fair, and aligned. This page explains **how a question becomes a decision**, who decides, and how we reopen decisions when new evidence appears.

---

## Principles

- **Ends before means.** We align on values and goals first; then we pick the path.
- **Small, reversible first.** Prefer decisions that are easy to change; time-box the rest.
- **Evidence over volume.** Data, adoption, and constraints beat rhetoric.
- **Clear ownership.** Every decision has a DRI (directly responsible individual) and a recorded status.
- **Public by default.** Decisions are proposed and recorded in the open.
- **Reopen with evidence.** We change our minds when facts change, without blame.

---

## Decision Types (what kind of question is this?)

| Type | Description | Examples | Default Path |
|---|---|---|---|
| **Ends** | Purpose & values; who we are | Recognition > wealth; brand use; contributor rights | Council/EthicDAO decision |
| **Constraints** | Safety, security, legal, compliance | Formal verification required? PII handling? | Steward-led; reviewers attest |
| **Means** | Tools, architectures, processes | Rust vs Go; monorepo vs polyrepo | DRI + reviewers; parallel, time-boxed trials |
| **Taste** | Copy, visuals, minor UX | Button label; page layout | DRI (or decider) picks, measure later |

> When unsure, treat as **Means** and run a small, fair experiment.

---

## Blast Radius (who and what does this affect?)

- **Local** — one team, one feature, one repo.
- **Cluster** — multiple teams/products/modules.
- **Project-wide** — many teams, policy, or brand.

**Rule of thumb:** Bigger blast radius → stronger process and more eyes.

---

## Choosing a Decision Mode (matrix)

| Type \ Radius | Local | Cluster | Project-wide |
|---|---|---|---|
| **Ends** | — | — | Council/EthicDAO |
| **Constraints** | DRI + lane reviewer sign-off | Steward facilitates + reviewers attest | Steward proposal → Council confirm |
| **Means** | DRI + reviewers; lazy consensus | Steward sets parallel trials + metrics; ADR | Steward report; Council arbitrate if stalemate |
| **Taste** | DRI (decider) | DRI (decider) + brief review | Brand/Design steward if it touches identity |

---

## The Flow (from question to decision)

1. **Decision Brief (one page)**  
   Problem, constraints, options, metrics, time-box, risks, DRI, reviewers.
2. **Discussion window**  
   Open thread. Default: 48h (Local), 72–96h (Cluster), 5–7d (Project-wide).
3. **Mode selection**  
   DRI and steward confirm decision mode using the matrix above.
4. **Experiment (for Means)**  
   Run time-boxed parallel paths when useful; same inputs; public demos.
5. **Decision Record (ADR)**  
   One page: context, choice, evidence, trade-offs, follow-ups, owners.
6. **Announcement & enactment**  
   Tag affected teams, create tasks, define rollback.
7. **Review window**  
   Objection period (24–72h) for material new evidence only; then “Accepted”.
8. **Sunset review**  
   For hard-to-reverse decisions, schedule a check (e.g., 60–90 days) to confirm or adjust.

---

## Consensus Styles (pick the lightest that fits)

- **Lazy consensus** — “I plan to do X by <date> unless someone objects.”  
  Use for Local Means/Taste. Requires a clear objection window.
- **Rough consensus** — broad agreement with no strong, reasoned objections.  
  Use for Cluster Means when parallel trials are impractical.
- **Consent with objection handling** — a decision proceeds unless a *substantiated* objection shows harm to constraints/values.  
  Steward helps resolve or escalates.
- **Formal decision** — vote or ruling by Council/EthicDAO.  
  Use for Ends or wide-impact Constraints.

---

## Roles in the Decision

- **DRI** — frames the brief, runs process, ships the outcome, owns rollbacks.
- **Reviewers (by lane)** — check quality/safety, cite constraints, attest evidence.
- **Steward** — selects mode, sets time-boxes, mediates, documents exceptions.
- **Council/EthicDAO** — decides on Ends; resolves stalemates with project-wide impact.
- **Users/Downstream teams** — provide adoption signals; “vote with use.”

**Recognition note:** Attentive review, good briefs, and clear ADRs earn Kudos alongside code/design.

---

## Service Levels (so we don’t stall)

- **Brief acknowledgment:** within 24h on weekdays (“Seen; back by <date>”).
- **Review response:** within 48h for Local; 72h for Cluster; 5d for Project-wide.
- **Escalation:** if deadlines slip or blockers appear, ping the steward; steward must respond within 24h.

---

## Objections & Reopening

A valid objection must include **constraint at risk**, **evidence**, and **proposed fix**.  
We **reopen** a decision when:
- New material evidence emerges (metrics, incidents, legal change).
- Assumptions in the ADR prove false.
- Blast radius widens beyond what was stated.

Reopening uses the same path, with a short summary of what changed.

---

## Safety & Risk Gates

- **Security/Compliance:** any decision touching funds, PII, auth, or chain safety requires a lane reviewer sign-off; stewards can require additional checks.
- **Kill switch:** ADRs for risky changes include rollback steps, owners, and triggers.
- **Incident override:** DRIs may act to mitigate active incidents; file an ADR within 24h.

---

## Decision Hygiene (habits that scale)

- **One-pager or it didn’t happen.** Long threads? Start with a brief.
- **Numbered ADRs:** `ADR-<YYYY>-<NN>`, statuses: Proposed / Accepted / Superseded / Rejected.
- **Link everything:** PRs/issues/docs/demos in the ADR; ADRs link back to briefs.
- **State constraints explicitly:** security, brand, legal, time, ethics.
- **Name owners and dates:** who drives, who reviews, when we check back.
- **Tidy outcomes:** close issues, tag teams, update docs after decisions.

---

## Templates (copy/paste)

**Decision Brief**
Title: Decision Brief — <topic>
DRI: <name> | Reviewers: <by lane> | Steward: <name>
Problem: <who/what is affected; desired outcome>
Constraints: <security, brand, legal, ethics, time>
Options: <A, B, C – 1–2 lines each; link prior art>
Metrics: <2–4 measures to compare/track>
Mode & Timebox: <lazy consensus | parallel trial | steward mediation | council ruling; dates>
Risks & Rollback: <triggers; steps; owners>
Blast Radius: <local | cluster | project-wide>
Stakeholders: <teams/users affected>

**ADR**
ADR-<YYYY>-<NN>: <decision name>
Status: <Proposed | Accepted | Superseded | Rejected>
Context: <why this mattered now; constraints>
Decision: <what we will do>
Evidence: <metrics; adoption; demos; trade-offs>
Consequences: <what we gain; costs we accept>
Actions: <tasks; owners; deadlines; rollback>
Review Date: <sunset/review checkpoint>
Links: <brief; issues; PRs; demos; prior ADRs>

---

## Examples

- **Local Means (library choice):** DRI posts brief; 48h lazy consensus; no objections → ADR Accepted; revisit in 60 days.
- **Cluster Means (API shape):** Steward sets 3-week parallel trial; shared dataset; demo day; ADR chooses option B with evidence; option A patterns documented.
- **Project-wide Constraint (data retention):** Steward drafts policy; reviewers attest; Council confirms; ADR links legal requirements and rollout plan.
- **Ends (brand use in forks):** Council deliberates openly; publishes ruling and rationale; ADR recorded; brand doc updated.

---

**Bottom line:** Clear modes, small reversible steps, honest evidence, and visible records let us move fast without breaking trust. Decisions are tools for progress—not trophies in debate.
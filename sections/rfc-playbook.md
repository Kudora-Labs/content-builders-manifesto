# RFC Playbook

An **RFC (Request for Comments)** is a short, public proposal for changes that affect more than one team, introduce new capabilities, or touch policies/standards. It turns disagreement into learning and convergence by making context, trade-offs, and evidence visible.

Use this playbook to draft, review, and land RFCs quickly—then close with an ADR once a decision is made.

---

## When to use an RFC (and when not)

**Use an RFC when:**
- The blast radius is **cluster** or **project-wide** (multiple teams, shared infra, policies, licensing, brand).
- You’re proposing a **new capability, API, or standard** that others may depend on.
- You want to run **time-boxed parallel experiments** and need shared metrics and guardrails.
- You need a **Commons Exception** (licensing), or anything that changes defaults.
- You’re formalizing a **deprecation**, migration, or cross-repo refactor.

**Skip the RFC (go straight to PR/ADR) when:**
- It’s a **local, reversible** change with one team affected and no policy impact.
- It’s **taste-level** UX/copy that a DRI can ship and measure.

> Heuristic: If people will rely on it or be blocked by it, write an RFC.

---

## Lifecycle at a glance

1. **Draft** → author prepares a concise RFC (≤ 6 pages excluding appendix).  
2. **Proposed** → open for comments; labels and reviewers assigned.  
3. **Review window** → discussion and, if needed, steward-set experiments.  
4. **Resolution** → Accepted / Rejected / Deferred / Withdrawn (with reasoning).  
5. **ADR** → final decision captured; RFC status updated and linked.  
6. **Implementation & follow-ups** → tasks, owners, review date.

**Default timelines (business days):**
- Local impact: 3–5d
- Cluster impact: 7–10d
- Project-wide: 10–15d  
Stewards can shorten/extend with a note.

---

## Roles

- **Author (DRI):** frames the problem, drafts the RFC, owns updates and synthesis.
- **Co-authors:** complementary expertise; help explore alternatives and experiments.
- **Reviewers (by lane):** surface constraints, prior art, risks; attest feasibility.
- **Stakeholders:** teams affected; provide adoption/operability feedback.
- **Steward:** keeps debate constructive, sets timeboxes/experiments, calls for decision.
- **Council/EthicDAO:** decides when **Ends** or wide policy are involved.

---

## File & naming conventions

- Folder: `rfcs/`
- Filename: `YYYY-XXXX-short-title.md` (e.g., `2025-0007-modular-fee-engine.md`)
- Each RFC has a **stable number** (incremental). Add a link label: `[RFC-0007]`.
- Link the eventual ADR: `[ADR-2025-12]`.

---

## Required sections (keep it tight)

Use this template (front-matter optional):

```markdown
---
rfc: 0007
title: Modular Fee Engine for Kudora
author: @alice (@bob)
steward: @steward-name
status: Proposed
impact: Cluster   # Local | Cluster | Project-wide
decision_window: 2025-11-20
links: [issue-123, prior-RFC-0003, ADR-2025-04]
---

## 1. Summary
One paragraph: the change and why now.

## 2. Problem & Goals
What breaks today? Who is affected? Success criteria (2–4).

## 3. Non-Goals
What this RFC deliberately does not try to solve.

## 4. Constraints
Security, brand, legal, ethics, time, compatibility.

## 5. Proposal
The approach at a glance (diagrams welcome). Interfaces/APIs if relevant.

## 6. Alternatives Considered
At least two serious alternatives with trade-offs.

## 7. Experiment Plan (if Means)
Time-box, owners, shared dataset/inputs, metrics, kill switch, review date.

## 8. Impact & Migration
Ops, tooling, docs, deprecations, rollout phases.

## 9. Risks & Mitigations
What could fail and how we’ll catch/undo it.

## 10. Recognition & Ownership
Who does what; how we’ll attribute upstream ideas and integration work.

## 11. Open Questions
Specific questions to resolve before acceptance.

## 12. Appendix
Prior art, data, benchmarks, diagrams, links.
Word to the wise: If you can’t write Sections 1–3 clearly, you’re not ready. Tighten the problem before proposing a solution.

Metrics for experiments
Pick 2–4, agreed upfront:

Reuse multiplier (downstream adoption, deps)

Recognition velocity (acknowledged impact over time)

Coordination latency (brief → ADR → rollout)

Quality deltas (perf, error rates, security findings)

Teachability (docs completeness, onboarding time)

Review etiquette (social norms in action)
Be specific. Cite constraints, propose tests, link prior art.

Steelman first. Summarize the author’s best case before critique.

No hallway vetoes. If positions change, post it on-thread.

Parallelism, not ping-pong. For Means, prefer small experiments over long arguments.

Decision clarity. When ready, steward calls for a decision with a 24–72h final comment window.

Labels & notifications
Apply labels so people can find and triage RFCs:

rfc, impact:local|cluster|project-wide, lane:build|docs|design|governance|security|community

needs-experiment, needs-adr, commons-exception, brand, security

Tag stakeholders and lane reviewers in the first comment.

Status codes
Draft — authoring, not yet requesting review.

Proposed — open for comments during the decision window.

Accepted — proceeding; capture the decision in an ADR and link it.

Rejected — not proceeding; include reasoning and conditions to revisit.

Deferred — valid, but timed out or blocked; add a review date.

Withdrawn — author retracts; note why.

Superseded — replaced by RFC-NNNN (link).

Status lives both in the front-matter and in the index list (rfcs/README.md).

Steward toolkit
Scope the debate. “We are deciding X, not Y.”

Set a timebox. Dates for discussion, experiment, and decision.

Force clarity. Ask for one-page summaries when threads sprawl.

Select mode. Lazy consensus / parallel trial / mediation / council ruling.

Protect minority views. Record strong objections and mitigations in the ADR.

Recognition guidance
Authors earn Kudos for clear framing, prior-art synthesis, experiment design.

Reviewers earn Kudos for constructive, timely, evidence-based feedback.

Integrators share a synergy bonus when solutions merge.

Teaching multiplier applies for excellent diagrams, examples, and migration guides.

Include an Impact Note in the RFC PR or the closing ADR to make recognition easy.

Commons Exception (licensing) via RFC
When proposing to deviate from default licenses:

Title begins with RFC: Commons Exception — <module/area>.

Include scope, reason, duration, exit criteria, and integration interfaces.

Steward recommends; Council/EthicDAO approves if impact is wide.

Time-boxed by default; review date required.

Brand & naming via RFC
Use neutral names for experiments.

For official names or marks, include brand steward as reviewer.

Forks must avoid confusion; proposals that affect brand require project-wide impact handling.

Anti-patterns (and fixes)
Novel-by-default: proposing a new thing without surveying prior art.
Fix: Section 12 must list serious prior work and why it’s insufficient.

Solutioneering: writing the “how” before the “why.”
Fix: Strengthen Sections 2–3; consider a spike instead.

Perma-threads: endless debate with no timebox or decision owner.
Fix: Steward sets a mode and date; move to experiment or close.

Private lobbying: trying to sway outcomes off-thread.
Fix: Summarize in public or it doesn’t count.

Vague impact: no migration plan or owners.
Fix: Add Section 8 with tasks, owners, and dates.

Example mini-RFC (1–2 pages)

RFC: 0012 — Lightweight Auth for Devnets
Summary: Allow emailless, ephemeral keys for devnet testing to cut setup time by 60%.

Problem & Goals:
- New builders drop during auth setup (avg 18 min). Goal: ≤ 7 min to first successful tx.

Constraints:
- No PII; no mainnet exposure; rate-limit abuse.

Proposal:
- Ephemeral key issuance scoped to devnet; 24h expiry; faucet with per-IP caps.

Experiment Plan:
- 2-week A/B on onboarding flow; metrics: time-to-first-tx, drop-off, abuse rate.

Impact & Migration:
- Docs: “Quickstart Devnet” page; SDK snippet.
- Rollout: devnet only; optional path on testnet later.

Risks & Mitigations:
- Abuse → IP + device fingerprint caps; kill switch in faucet.

Open Questions:
- Should SDK auto-detect devnet and switch auth mode?
Closing the loop
Every accepted or rejected RFC must link a final ADR stating:

The decision and evidence,

Consequences and follow-ups,

Owners and review date,

Recognition distribution (authors, reviewers, integrators).

If experiments were run, attach dashboards or summaries so future teams can learn without repeating them.

Bottom line: RFCs are not hurdles; they’re clarity engines. Keep them short, time-boxed, and evidence-driven so we turn disagreement into reusable knowledge—and ship better decisions, faster.
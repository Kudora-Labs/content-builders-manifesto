# Contribution Process

This page explains **how to go from idea → change → recognition** with minimal friction. It’s intentionally lightweight, public-by-default, and tuned for fast learning without breaking trust.

---

## Scope

These rules apply across Kudora repos (code, docs, design, community, governance). Lane-specific checklists are at the end.

---

## Before You Start

1. **Align on the goal.** Skim the Manifesto sections (Shared Ground, Social Norms, Decision-Making, Recognition).  
2. **Find context.** Search issues/ADRs; check open RFCs and the roadmap.  
3. **Pick a lane & size.** Choose a **small, reversible** step if possible.  
4. **Say hello.** Comment on the issue you want to take: “I’m taking this as DRI.”

---

## Picking Work

- **Labels you’ll see**
  - `good-first-issue` – onboarding tasks
  - `help-wanted` – anyone can grab
  - `needs-decision` – blocked pending ADR/RFC
  - `security` – steward attention required
  - `rfc` – proposal threads
  - `docs`, `design`, `governance`, `community` – lanes
- If no issue exists, open one with a **Decision Brief** (template below) or a simple task card for small changes.

---

## Small vs. Substantial Changes

- **Small change (default path)**
  - Open/claim issue → make branch → PR with checklist → reviewer approves → merge → Impact Note for recognition.
- **Substantial change (needs agreement first)**
  - Post a **Decision Brief** or **RFC**.
  - For “Means” disagreements, steward may set **time-boxed parallel trials**.
  - Close with an **ADR** and implement.

*Heuristic:* if it affects multiple teams, brand, security, or licensing → treat as substantial.

---

## Branch & Commit Conventions

- Branch: `lane/short-topic` (e.g., `build/fee-calc`, `docs/getting-started`)  
- Commits: use clear, imperative messages. Conventional Commits are welcome but not required.

---

## Making the Change (quality gates)

- **Tests:** add/adjust unit/integration tests for code; “steps to verify” for docs/design.
- **Docs:** update READMEs/usage notes; add examples.
- **Security & privacy:** never commit secrets/PII; follow incident rules.
- **AI & provenance:** disclose AI assistance briefly in the PR if used; you own the output.
- **Licensing:** keep file headers consistent with repo license; note third-party assets clearly.

---

## Pull Request (PR) Checklist

Include this at the top of your PR:

 Problem & context explained (link issue/brief)

 Scope is minimal and reversible

 Tests or verification steps included

 Docs/README updated (if needed)

 Breaking changes called out with migration notes

 Impact Note added (below) for recognition

 Licensing headers intact; third-party attributions listed

 Security/privacy considerations addressed (N/A if none)

**Review SLAs:** 48h (local), 72h (cluster), 5d (project-wide). If it slips, ping the steward.

---

## Impact Note (inline in the PR for Recognition)

Impact Note
Lane(s): <Build | Docs | Design | Community | Governance | Ecosystem>
Context: <Problem and who benefits>
Change: <What was added/changed; key links>
Evidence: <Tests, metrics, adoption plan, before/after>
Requested Multipliers: <Reuse | Teaching | Stewardship | Risk | Team> (optional)

*Tip:* Keep it factual. Reviewers will attest; stewards publish weekly recognition epochs.

---

## Reviews & Approvals

- **Reviewers (by lane)** check quality, safety, and constraints.  
- **DRI** responds or pushes follow-ups; keep PRs small to reduce churn.  
- **Steward** steps in if blocked, sets timeboxes, or requests trials.

**Merging requires**: passing checks + lane reviewer approval(s). For risk-tiered items, steward sign-off too.

---

## Decision Records (ADRs)

For substantial or contentious changes, close with an ADR:

ADR-<YYYY>-<NN>: <decision name>
Status: Proposed | Accepted | Superseded | Rejected
Context: <why this mattered; constraints>
Decision: <what we chose>
Evidence: <metrics, adoption, trade-offs>
Consequences: <gains; costs>
Actions: <owners, tasks, rollback plan>
Review Date: <sunset check>
Links: <brief, issues, PRs, demos, prior ADRs>

---

## Exceptions You Might Need

- **Commons Exception (licensing):** time-boxed, scoped, public rationale, exit criteria.  
- **Brand & name use:** open a request before using official marks in forks or external materials.  
- **Security disclosure:** use the private channel in the security page (never in public PRs).

Each exception uses a short brief; stewards recommend; Council/EthicDAO approves when impact is wide.

---

## After Merge

- Update any follow-up issues/tasks.  
- Add release notes if user-visible.  
- Close the loop on the thread with the outcome and next steps.  
- Your Kudos appears in the next recognition epoch; appeal window follows.

---

## Lane Checklists

**Build (code/contracts)**
 Tests cover new/changed logic (happy + edge)

 Performance impact measured or noted N/A

 Security review for auth, funds, PII (if applicable)

 Backward compatibility documented or migration provided

 Public API changes noted in CHANGELOG

**Docs & Education**
 Audience and prerequisites stated

 Clear steps with copy-pasteable commands/snippets

 Screenshots/diagrams have alt text

 Examples verified end-to-end

 Cross-links added to related guides/APIs

**Design & UX**
 Problem/use case and constraints defined

 Accessibility checks (contrast, focus, labels)

 States covered (empty/error/loading/success)

 Usability notes and metrics plan (if measurable)

 Tokens/components align with design system

**Community & Ops**
 Playbook or runbook updated/added

 Incident or support impact assessed

 Onboarding or moderation steps documented

 Metrics to watch listed (with owner)

 Handoff clear (who does what next)

**Governance & Stewardship**
 Brief posted; constraints and blast radius stated

 Stakeholders tagged; discussion window respected

 Decision mode chosen (matrix)

 ADR published; review date set

 Recognition notes for reviewers/mediators included

---

## Templates (copy/paste)

**Decision Brief (one-pager)**
Title: Decision Brief — <topic>
DRI: <name> | Reviewers: <by lane> | Steward: <name>
Problem: <who/what is affected; desired outcome>
Constraints: <security, brand, legal, ethics, time>
Options: <A, B, C – 1–2 lines each; link prior art>
Metrics: <2–4 measures to compare/track>
Mode & Timebox: <lazy consensus | parallel trial | mediation | council ruling; dates>
Risks & Rollback: <triggers; steps; owners>
Blast Radius: <local | cluster | project-wide>
Stakeholders: <teams/users affected>

**Pull Request description**
Summary
<what this PR does in one paragraph>
Context
<linked issues/briefs/ADRs; constraints at play>

Verification
<tests or manual steps; screenshots if UI>

Impact
<breaking changes? migrations? user-visible notes?>

Impact Note
<insert the Impact Note block from above> ```
Conduct & Safety
Follow the Social Norms; critique ideas, not people.

Declare conflicts of interest early; recuse from reviews if needed.

For harassment or safety issues, use the private reporting channel; stewards must respond within 24h on weekdays.

Getting Help
Tag the lane label and a reviewer.

If no response within the SLA, ping the steward.

For process or policy confusion, open a small question issue—we prefer clarity over assumptions.

Bottom line: Small steps, open threads, clear briefs, tidy ADRs, and honest Impact Notes keep us learning fast while treating people fairly. Ship, measure, teach—repeat.
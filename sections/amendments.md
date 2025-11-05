# Amendments

This page defines **how the Manifesto changes**. We want stability without stagnation: clear rules, public redlines, and small safe steps—plus a path for urgent fixes. Every amendment leaves a paper trail and a version bump.

---

## Purpose & Principles

- **Stability with learning.** We change slowly on values, faster on process, and immediately on typos.
- **Public, not private.** Proposals, redlines, votes, and rationales are visible.
- **Non-retroactive.** New rules apply forward unless a security/legal fix requires otherwise.
- **Pilot first.** When possible, we trial changes with a sunset review before locking them in.
- **Legitimacy.** The people doing the work must see, shape, and accept the change.

---

## What can be amended?

- Any Manifesto section (culture, collaboration, safeguards, governance).
- Defaults and thresholds (e.g., review SLAs, licensing defaults).
- Templates and checklists.
- **Not via amendment:** individual recognition grants or case decisions (use appeals).

---

## Change Classes (and default paths)

| Class | Examples | Path | Threshold | Version bump |
|---|---|---|---|---|
| **Editorial** | Typos, formatting, link fixes; wording that doesn’t change meaning | PR → 48h quiet period → Steward ack | None (no objections) | `+PATCH` |
| **Substantive** | Roles/rights details, SLAs, metrics definitions, stewardship rules, RFC/ADR flow | RFC → 7–10d review → Steward call → Council confirm | **Simple majority** of Council **and** no substantiated steward objection | `+MINOR` |
| **Constitutional (Ends)** | Core values, Contributor Bill of Rights, licensing defaults, brand rules, fork ethics, security disclosure principles | RFC → hearings → 14–21d review → vote | **Supermajority**: 2/3 Council **and** ≥60% recognition-weighted “yes” among active contributors (90d window) | `+MAJOR` |
| **Emergency** | Critical security/legal compliance requiring immediate change | Steward + Council temporary order (≤30d) → retro RFC | Council quorum; must be ratified within 30d or auto-revert | `+MINOR` (or `+PATCH` if editorial fix) |

> The Council/EthicDAO is the final arbiter when Ends are at stake. “Recognition-weighted” means recent, verified contributors carry more weight; exact weighting is defined in governance docs.

---

## The Amendment Flow

1. **Pre-work (optional but wise)**  
   - Start with an issue describing the problem and desired outcome.  
   - If scope is unclear, run a small pilot in one repo for 2–4 weeks.

2. **File an RFC** (for Substantive/Constitutional/Emergency)  
   Include: problem, constraints, proposed redlines, migration plan, tests/metrics to validate, and sunset review date.

3. **Discussion window**  
   - Editorial: 48h quiet period on the PR.  
   - Substantive: 7–10 business days.  
   - Constitutional: 14–21 days including at least one live Q&A or written hearing.  
   Stewards enforce civility and timeboxes.

4. **Decision & Record**  
   - Steward summarizes positions and calls the mode.  
   - Council verifies threshold and publishes **ADR** with rationale.  
   - Version bump + CHANGELOG entry.

5. **Rollout & Review**  
   - Update templates, checklists, and affected repos.  
   - Schedule the sunset review (usually 30–90 days).  
   - Measure effects; revise if needed.

---

## Required Contents (for any amendment RFC)

- **Summary:** one paragraph: what changes and why now.  
- **Class:** Editorial / Substantive / Constitutional / Emergency.  
- **Redlines:** exact text diff or side-by-side before/after.  
- **Blast radius:** who/what is affected; migration steps.  
- **Constraints:** security, brand, legal, ethics, time.  
- **Metrics/Checks:** how we’ll know the change helped.  
- **Sunset review date:** when we re-evaluate.  
- **Recognition plan:** credit for authors, reviewers, integrators.  
- **Objection window:** dates and how to object.

---

## Versioning & Changelog

- **Semantic versioning for the Manifesto:** `MAJOR.MINOR.PATCH`  
  - **MAJOR:** Constitutional changes  
  - **MINOR:** Substantive changes  
  - **PATCH:** Editorial fixes
- Files:
  - `VERSION.md` — current version and release date.  
  - `CHANGELOG.md` — each entry lists class, sections affected, links to RFC/ADR/PR, and rationale.  
  - Section headers include a small version tag (e.g., `v2.1`).

---

## Cooling-off & Reopening

- **Cooling-off:** Constitutional changes have a 7-day period between vote and effect (except emergencies).  
- **Reopen:** Any amendment can be reconsidered with **new evidence** or clear harm documented; use a follow-up RFC referencing the original ADR.

---

## Objections & Appeals

A **valid objection** states: the **constraint at risk**, the **evidence**, and a **specific alternative**.  
- **Substantive:** Steward mediates; Council confirms.  
- **Constitutional:** Council logs the objection in the ADR; if a blocking threshold is met (e.g., ≥25% recognition-weighted “no”), the proposal returns to revision or pilot.

---

## Migration Expectations

When an amendment changes working practices or defaults:

- Update **templates** (PR, ADR, RFC) and **checklists** in affected repos.  
- Post a **“What changed”** summary with examples.  
- Provide **training notes** or a short video if the change is non-trivial.  
- For licensing/brand changes, update SPDX headers, `NOTICE`, and repo READMEs.  
- Dashboard metrics updated (and versioned) to reflect new definitions.

---

## Emergency Amendments

Use only for user safety, legal compliance, or chain integrity.

- **Temporary order** (max 30 days): Steward + Council publish a one-page order with scope, reason, and expiry.  
- **Quiet communications** may be used if public detail would raise risk (e.g., active exploits).  
- **Ratify or revert:** Within 30 days an RFC must be voted; otherwise the order lapses.

---

## Translation & Accessibility

- English text is canonical.  
- Translations are welcome; they must track the canonical version number.  
- If a conflict appears, the English version prevails until translators reconcile.

---

## Templates

**Amendment RFC header**
class: <Editorial | Substantive | Constitutional | Emergency>
sections: [ "social-norms.md", "licensing.md" ]
version_bump: <MAJOR | MINOR | PATCH>
review_window: <dates>
sunset_review: <date>
steward: @name
council_sponsor: @name (for Constitutional/Emergency)

**Redlines (before/after block)**
Before
<exact paragraph(s) to be replaced>

After
<proposed replacement text> ```
ADR entry (decision record)

ADR-<YYYY>-<NN>: Amend Manifesto <section(s)>
Class: <Editorial | Substantive | Constitutional | Emergency>
Decision: <accepted | rejected | deferred>
Rationale: <key reasons and evidence>
Thresholds: <who voted/how met>
Version: <X.Y.Z>
Effective: <date>  |  Sunset Review: <date>
Links: <RFC, PRs, dashboards>
CHANGELOG entry

## [2.1.0] — 2025-11-05
Class: Substantive
Sections: decision-making.md, rfc-playbook.md
Summary: Clarified timeboxes and added consent-with-objection mode.
Why: Reduce coordination latency on cluster-wide changes.
Links: RFC-0021, ADR-2025-12, PR #456
Roles & Rights
Any contributor can propose amendments (RFC or PR).

Reviewers verify clarity, compatibility, and migration steps.

Stewards enforce timelines, call modes, and publish outcomes.

Council/EthicDAO ensures legitimacy, votes on Ends, and records final decisions.

Community provides evidence through adoption, metrics, and reasoned objections.

Guardrails (hard stops)
Contributor Bill of Rights cannot be reduced without Constitutional process and 2/3 supermajority.

Licensing defaults cannot be weakened without Constitutional process and published migration/compatibility analysis.

No retroactive penalties.

No anonymous authority: every decision lists accountable humans (handles).

Bottom line: We keep the Manifesto alive without letting it drift. Clear classes, public redlines, real thresholds, and careful rollouts make change legitimate—and keep trust compounding while we learn.
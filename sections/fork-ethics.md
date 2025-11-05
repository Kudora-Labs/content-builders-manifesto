# Fork Ethics

Forks are **legitimate but costly**. This page defines when a fork is appropriate, how to do it without harming people or the commons, and how to make reconciliation possible. Code can fork; **trust should not**. We protect users, attribution, and the shared ground first.

---

## Principles

- **Clarity over drama.** A fork is a technical and governance choice, not a feud.
- **Attribution is non-negotiable.** Credit upstream people and ideas in code and docs.
- **Minimize harm.** Protect users, security, and brand clarity; avoid confusing the community.
- **Open interfaces.** Keep APIs and proofs interoperable so collaboration remains possible.
- **Reconciliation path.** Document what would allow a merge-back before you split.

---

## When a fork is legitimate

- **Ends conflict (values):** The project’s purpose or non-negotiables are in contradiction and cannot be bridged. *Brand must separate.*
- **Stewarded stalemate on means:** Multiple good approaches cannot converge; a **time-boxed** friendly fork evaluates alternatives at real scale.
- **Safety & continuity:** Security or operational issues require a rescue fork to protect users while governance catches up.
- **Custodial risk:** Governance capture blocks fixes or upgrades; a community fork safeguards the commons.

> If disagreement is only about tools or taste, prefer **parallel experiments** and ADRs over a fork.

---

## Pre-fork protocol (do this first)

1. **Name the question.** Post a one-page Decision Brief (problem, constraints, metrics, timebox).
2. **Run alternatives.** Use parallel trials with shared inputs; publish demos and metrics.
3. **Steward mediation.** Request a steward to structure decision mode and timeframes.
4. **RFC & ADR.** Attempt a recorded decision. If irreconcilable, proceed with the fork protocol below.

---

## Types of forks (be explicit)

- **Dev fork (short-lived):** scratch exploration; **must** either merge or delete.
- **Feature fork (friendly, time-boxed):** proves an approach; merge target defined.
- **Rescue fork (emergency):** secops continuity; minimal changes; clear hand-back plan.
- **Community fork (governance split):** long-term divergence; brand separation required.
- **Vendor distribution:** packaging/patches under original brand rules; must avoid endorsement claims.

---

## Fork protocol (step-by-step)

### 1) Declare intent
- Post a **Fork Intent** issue upstream (unless security-sensitive) with:
  - *Why now* (problem/constraints), *type*, *scope*, *blast radius*, *maintainers*.
  - *Reconciliation criteria* and *review date*.
  - *User impact & migration path* (if any).

### 2) Respect licenses & notices
- Keep original LICENSE headers.
- Add/maintain `NOTICE` and `THIRD_PARTY` files.
- If adding closed components via an approved exception, include `COMMONS_EXCEPTION.md` with scope/dates.

### 3) Brand & naming
- Choose a name that avoids confusion. No official marks or domains unless approved.
- Use a **neutral experimental label** for friendly forks (e.g., `Kudora-X (Experimental)`).
- Update package namespaces and module IDs to avoid collisions.

### 4) Security & responsible disclosure
- Join or create a **shared security channel** with upstream for embargoed reports.
- Coordinate CVE IDs where relevant; users should not be exposed to duplicate or conflicting advisories.

### 5) Interoperability
- Keep **public interfaces stable** where possible; document intentional deltas in `DIVERGENCES.md`.
- Provide adapters or shims; publish integration tests others can run.

### 6) Migration & support
- Provide `MIGRATION.md`: versions, risks, rollback, data compatibility.
- State support policy (LTS, EOL) so users aren’t stranded.

### 7) Recognition & attribution
- Credit upstream maintainers in README and release notes.
- Map recognition transparently: ported work cites original Impact Notes; new work earns its own.

### 8) Governance note
- Describe the new governance (who decides what; how to propose changes).
- If friendly/time-boxed, state the **review date** to evaluate merge-back.

---

## Friendly fork playbook (time-boxed)

- **Timebox:** 2–6 weeks (feature) or one release cycle (platform).
- **Metrics:** adoption, performance/quality deltas, coordination latency, teachability.
- **Demo day:** side-by-side evaluation with upstream; publish ADR on keep/merge.
- **Merge etiquette:** upstream gets early PRs; fork maintainers share integration lift.

---

## Community fork playbook (long-term split)

- **Brand separation:** new name, logo, domains, social handles; clear “not affiliated” note.
- **Cohabitation rules:** both sides link each other; users can compare without FUD.
- **Commons obligations:** accept upstream security fixes; share critical patches cross-project.
- **Bridges:** adapters for APIs/data formats to keep the ecosystem connected where safe.

---

## Recognition rules around forks

- **Upstream credit:** Every forked file keeps headers and links to origin and contributors.
- **Port credit:** Significant porting/integration earns Kudos with a **teaching multiplier** when well-documented.
- **No double-counting:** Don’t re-award Kudos for identical work; new value only.
- **Synergy bonus:** If projects reconcile or co-ship a shared module, both sides earn a bonus.

---

## Anti-patterns (and what to do instead)

- **Brand squatting or confusion.** → Rename; add disclaimers; update package IDs.
- **Silent forking.** → Announce intent; publish DIVERGENCES and MIGRATION.
- **Security one-upmanship.** → Coordinate advisories; protect users first.
- **Fork as first resort.** → Run experiments; ask a steward; use RFC/ADR paths.
- **Withholding interfaces.** → Publish stubs/tests so others can interoperate.

---

## Chain-level note (protocol forks)

For blockchain upgrades:
- Prefer **coordinated network upgrades** (no split state) with recorded ADRs.
- If a **state-splitting fork** is unavoidable, publish: snapshot height, replay rules, initial validator set, bridge status, risk assessment, and user safety guidance.
- Respect brand separation and ticker clarity to avoid user loss.

---

## Templates

**Fork Intent (issue)**
Title: Fork Intent — <project/module>
Type: <dev | feature | rescue | community | vendor>
Why now: <problem + constraints>
Scope: <modules/repos; expected blast radius>
Maintainers: <handles, roles>
Reconciliation: <conditions + review date>
User impact: <migration needed? risks? rollback?>
Security: <disclosure coordination contact>
Brand: <new name/namespace; disclaimer text>
Links: <brief, RFCs, ADRs>

**DIVERGENCES.md**
Scope:

<Area / API / behavior>
Rationale:

<Why this differs; constraints/metrics>
Compatibility:

<Adapters/shims; breakages; migration notes>
Review:

<Date to revisit; owner>

**MIGRATION.md**
From: <version/commit> To: <version/commit>
Breaking changes: <list>
Data/State: <compatibility; snapshot/export if chain-level>
Steps:

<backup/export>

<install/upgrade>

<verify/rollback>
Support: <channels; EOL dates>

**README disclaimer (friendly fork)**
This is a time-boxed experimental fork of <Upstream>. It exists to evaluate <goal>.
We coordinate security disclosures and intend to propose merge-back by <date>.
Not an official <Upstream> release.

**README disclaimer (community fork)**
This is an independent community fork of <Upstream>. We are not affiliated with or endorsed by <Upstream>.
We maintain interoperability where safe and credit upstream contributors.

---

## Steward checklist (use the lightest touch that works)

- Confirm pre-fork steps happened (brief, trials, mediation).
- Ensure brand and security coordination are in place.
- Record reconciliation criteria and review date.
- Verify LICENSE/NOTICE and divergence docs exist.
- Publish an Outcome Note with next checkpoints.

---

**Bottom line:** Forks should protect users and the commons, not egos. Announce clearly, attribute fully, interoperate where safe, and keep a real path to come back together.
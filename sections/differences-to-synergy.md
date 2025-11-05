# Differences → Synergy

We don’t try to erase differences. We harness them. This section is a practical playbook for turning diverse opinions, styles, and priorities into *compounding* progress—so tension becomes a source of energy, not a fracture line.

## Why differences matter here

- **Innovation needs variance.** New ideas come from people who see the world differently.
- **Quality needs friction.** Respectful challenge catches blind spots earlier and cheaper.
- **Resilience needs plurality.** Multiple good approaches make the system anti-fragile.

Our goal isn’t to “win” debates; it’s to **turn disagreement into reusable assets** (frameworks, docs, patterns) others can build on.

---

## Classifying disagreements (so we pick the right response)

| Type | Examples | Default response |
|---|---|---|
| **Ends** (purpose/values) | “Should we prioritize recognition over TVL?” | Align on the Manifesto or escalate to stewards/EthicDAO. No split experiments. |
| **Constraints** (risk, security, compliance) | “Can we ship without formal verification?” | Decide with stewards; allow pilots only within guardrails. |
| **Means** (architectures, tools, processes) | “Rust vs Go?” “Monorepo vs polyrepo?” | Run **time-boxed parallel experiments** with shared metrics. |
| **Taste** (UX copy, naming, visuals) | “Button label,” “Color choice” | Pick a decider, ship, measure, revisit on data. |

When in doubt, treat it as **Means** and prefer experiment over argument.

---

## The playbook: Fit, don’t split

### 1) Frame the question
- **Problem statement:** What outcome are we trying to improve?
- **Constraints:** Security, brand, legal, ethics, time.
- **Success metrics:** Agree on 2–4 measures (e.g., Reuse multiplier, Recognition velocity, Coordination latency).
- **Decision horizon:** Reversible vs. hard-to-reverse (guides the timebox).

> *Output:* a one-page issue titled `Decision Brief: <topic>`.

### 2) Run time-boxed parallelism (when it’s about Means)
- **Small, scoped, fair.** Two or more micro-implementations, each with a sponsor and tiny budget.
- **Default timeboxes:** 1–2 weeks (low stakes), 3–4 weeks (medium), 6 weeks max unless stewards extend.
- **Shared inputs.** Same dataset, same user story, same constraints, same review checklist.
- **Public work.** Open branches, visible progress notes, weekly demo.

> *Output:* short demo + metrics table for each path.

### 3) Compare on evidence, not ego
- Use the agreed metrics. Invite users or downstream teams to vote with adoption.
- Credit both **performance** and **teachability**: the clearer pattern/template also scores.

> *Output:* `Decision Record (ADR)` with the choice, evidence, and follow-ups.

### 4) Merge the best, preserve the rest
- **Adopt the winner** as default.
- **Digest the runner-up** into patterns, tests, or docs. Losing paths that teach others still earn recognition.
- **Synergy bonus.** Merging teams split a bonus Kudos pool for integration work.

---

## Protocols for common flashpoints

### A) Licensing differences (open vs. proprietary)
- **Defaults:** Open licenses for libraries/contracts; server apps use network-copyleft; docs are Creative Commons.
- **Exception lane:** If a contributor needs stricter terms (partner IP, security), propose a **Commons Exception**: scope, reason, duration, exit criteria. Review in public; time-box by default.
- **Recognition parity:** Closed modules must still expose *interfaces and proofs* so others can integrate and evaluate impact.

### B) Product vs. platform tension
- **Two tracks, one map.** A product pilot can run fast *on top of* platform APIs; platform keeps pace by absorbing stable lessons.
- **Stabilization gates:** Only patterns with real adoption graduate into the platform layer.

### C) Speed vs. safety
- **Risk tiering:** For high-risk changes (security, funds), require steward sign-off and extra testing. For low-risk UX/content, ship-and-measure.
- **Kill switches:** Every experiment must define rollbacks and data migration plans.

### D) Brand and naming
- **One brand, many implementations.** Use neutral names for experimental modules. Graduated defaults may take official names.
- **Fork etiquette (summary):** Attribute upstream clearly; avoid brand confusion; describe intent and divergence; offer a merge-back path.

---

## Recognition rules (so incentives align)

- **Evidence-weighted Kudos.** Recognition accrues from verifiable outcomes: adoption, reuse, quality, user impact—not volume of debate.
- **Attribution first.** Always credit upstream ideas and people in READMEs and Decision Records.
- **Teaching counts.** Writing docs, onboarding, conflict mediation, and demos earn Kudos. No invisible work.
- **Synergy rewards.** When two paths merge, *both* teams receive a bonus for integration and knowledge transfer.

---

## Social norms (the cultural bar)

- **Be specific.** Critique ideas, cite constraints, propose tests. No vibes-only pushback.
- **Steelman the other side.** State their best argument before refuting it.
- **Disagree and commit.** After a decision, execute wholeheartedly—or propose a scoped parallel if approved.
- **Assume good intent, prove good effects.** Kindness in tone, rigor in outcomes.

Anti-patterns we call out early: sarcastic dismissal, goalpost moving, private lobbying after public decisions, and “strategic ambiguity.”

---

## Roles in a healthy disagreement

- **Proposer:** frames the problem, drafts the brief, owns a time-boxed path.
- **Counter-proposer:** offers a credible alternative with equal rigor.
- **Reviewers:** check constraints, surface prior art, keep metrics honest.
- **Stewards:** facilitate when stuck, guard values, decide on timebox/guardrails.
- **Users/downstream teams:** vote with adoption and feedback.

No single role “wins” by default; **results and clarity** do.

---

## Convergence ritual (closing the loop)

1. Demo day with side-by-side outcomes.  
2. Users weigh in; reviewers post metric deltas.  
3. Draft ADR, tag participants for 24–72h comments.  
4. Stewards finalize; teams plan integration and deprecation.  
5. Recognition distribution posted alongside the ADR.  
6. Lessons captured as a pattern/template so others start further ahead.

---

## Templates

**Decision Brief (one-pager)**
Title: Decision Brief — <topic>
Problem: <who/what is affected; desired outcome>
Constraints: <security, brand, legal, ethics, time>
Options: <A, B, C with 1–2 lines each>
Metrics: <2–4 measures agreed upfront>
Timebox: <dates, owners, budgets>
Risks & Rollback: <what could go wrong; kill switch>
Related work: <links to prior art, issues, docs>

**ADR (Architecture/Approach Decision)**
ADR-<number>: <decision name>
Context: <why this mattered now>
Decision: <chosen option>
Evidence: <metrics, adoption, user input, trade-offs>
Consequences: <what we gain; costs we accept>
Actions: <integration plan, deprecations, follow-ups>
Recognition: <who gets what and why>

---

## When a fork is legitimate

- **Value conflict** with the Manifesto (ends), not just the means.  
- **Steward failed mediation** and no safe compromise exists.  
- **Clear constituency** that benefits, without harming the commons.

If you must fork: be explicit, attribute, avoid brand confusion, keep the door open for reconciliation, and document what would make a future merge possible.

---

**Bottom line:** Differences are fuel. When we frame them well, test them fairly, and recognize outcomes transparently, they make us faster, kinder, and far more effective than any monoculture could.
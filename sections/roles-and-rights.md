# Roles & Rights

This section defines **who does what, who decides what, and what everyone can rely on**. Clear roles and explicit rights make collaboration easier than conflict and keep differences from turning into fractures.

---

## Participation Ladder

People can hold multiple roles, but decision rights come from the *role you’re using at the moment*. Moving up requires trust and demonstrated behavior, not status.

1. **Newcomer** — first issues, docs, questions, small fixes.  
2. **Contributor** — regular PRs/issues; follows norms; owns small scopes.  
3. **Reviewer** — trusted in one or more lanes (build, docs, design, governance); approves changes.  
4. **Steward** — facilitates decisions, resolves conflicts, guards values, manages exceptions.  
5. **EthicDAO / Steward Council** — final escalation on principle-level disputes and policy changes.

**Leveling down** (temporary or permanent) can happen when norms or safety rules are broken; it must be documented with reasons and a path to rebuild trust.

---

## Rights for Everyone (Contributor Bill of Rights)

- **Safety & respect.** Work without harassment, sarcasm-as-weapon, or retaliation.
- **Attribution.** Your contributions are credited in logs, READMEs, ADRs, and release notes.
- **Voice.** You can propose changes, comment on decisions, and be heard in good faith.
- **Due process.** You can appeal recognition and moderation decisions with clear timelines.
- **Transparency.** You can see how decisions were made and how recognition was determined.
- **Data dignity.** Minimal personal data; access/export your recognition history; request corrections.
- **License to build.** Clear, public defaults for reuse and contribution; no hidden traps.

---

## Responsibilities for Everyone

- **Clarity.** Provide problem statements, constraints, and success criteria.
- **Evidence.** Argue from artifacts, adoption, and measured outcomes—not volume.
- **Attribution.** Credit upstream work and people. Reuse before reinventing.
- **Open by default.** Discuss and decide in public threads unless sensitive.
- **Conflict disclosure.** State conflicts of interest early; recuse when needed.
- **Security & privacy.** Handle secrets and user data with care; follow incident rules.

---

## Role Charters

### Newcomer
- **Rights:** Handholding on first issues; clear “good first task” labels; fast review on starter PRs.
- **Duties:** Follow social norms; ask questions in public; capture what you learn in docs.

### Contributor
- **Rights:** Timely reviews; ability to open RFCs; recognition for impact (including docs, support, mediation).
- **Duties:** Keep PRs small; write Impact Notes for non-trivial changes; respond to review feedback.

### Reviewer (per lane)
- **Rights:** Approve/deny within scope; request changes; block on safety/regression grounds.
- **Duties:** Be specific and constructive; cite constraints; respond within agreed SLAs; mentor where useful.
- **Limits:** Cannot change scope mid-review; escalate if disagreement persists.

### Steward
- **Rights:** Facilitate stuck threads; set timeboxes; decide exception paths; trigger mediation.
- **Duties:** Guard values; prevent “hallway vetoes”; document outcomes; protect minority views while driving convergence.
- **Limits:** Uses lightest-weight intervention first; records rationale for all exceptions.

### EthicDAO / Steward Council
- **Rights:** Final call on value-level conflicts, licensing exceptions of wide impact, and policy changes.
- **Duties:** Run open deliberation; publish decisions and reasoning; define/update metrics and guardrails.
- **Limits:** Intervenes only when teams cannot resolve or when principles are at stake.

### Partners & Investors (non-building role)
- **Rights:** Transparency on progress and metrics; ability to propose ideas via public RFCs.
- **Limits:** No special veto on technical or recognition decisions unless explicitly granted by governance and disclosed.

---

## Decision Rights (who decides what)

- **DRI (Directly Responsible Individual):** For every task/issue/EPIC, one DRI owns delivery and day-to-day decisions within the agreed scope.
- **Reviewer(s):** Approve within quality and safety gates for their lane.
- **Steward:** Decides *process* (timebox, experiment shape) and resolves deadlocks about *means*.
- **EthicDAO/Council:** Decides *ends* (principles), high-impact exceptions, and policy.

**Heuristic:** If it changes *how* we do a scoped thing → DRI/Reviewers/Steward.  
If it changes *what we stand for* or affects many teams → Council/EthicDAO.

---

## Permissions Matrix (summary)

| Action | Newcomer | Contributor | Reviewer | Steward | Council/EthicDAO |
|---|---|---:|---:|---:|---:|
| Open issue / PR | ✅ | ✅ | ✅ | ✅ | ✅ |
| Approve PR (lane) | — | — | ✅ | ✅ (override on process) | — |
| Set timebox / parallel trials | — | — | ➖ (suggest) | ✅ | — |
| Merge after block | — | — | ➖ (escalate) | ✅ (process basis) | — |
| Grant/adjust recognition | — | ➖ (propose) | ✅ (attest) | ✅ (edge cases) | ✅ (policy) |
| Licensing exception | — | — | — | ✅ (recommend) | ✅ (approve) |
| Final dispute resolution | — | — | — | ➖ (mediate) | ✅ |

Legend: ✅ can do / ➖ influence or propose / — not applicable

---

## Recognition & Appeals

- **Right:** Any contributor can submit an Impact Note and request multipliers.  
- **Review:** Relevant-lane reviewers attest; stewards publish weekly recognition epochs.  
- **Appeal:** Within a defined window, contributors can request reconsideration with new evidence.  
- **Conflicts:** Reviewers disclose conflicts and recuse; stewards re-route if needed.

---

## Fork & Brand Rights

- **Right to fork code** under the license terms, with clear attribution and intent.  
- **No confusion:** Project names, logos, and domains follow brand-use rules; forks must avoid implying endorsement.  
- **Merge-back path:** Forks should document conditions for reconciliation; upstream commits remain credited.

---

## Security & Production Access

- **Least privilege:** Access is role- and time-bound; production access requires reviewer or steward sponsorship.  
- **Secrets handling:** Use approved vaults; no plaintext secrets in repos or chats.  
- **Incidents:** DRIs may exercise emergency actions within documented kill-switches; stewards/Council review post-mortem.

---

## Conflicts of Interest (CoI)

- **Declare early:** employment, investment, family ties, or competing commitments.  
- **Recuse:** from reviews, recognition attestations, or votes where CoI exists.  
- **Document:** stewards record recusals to keep trust high.

---

## Stewardship: Term, Handoff, Accountability

- **Term:** Stewards serve fixed, renewable terms (e.g., 6–12 months).  
- **Handoff:** Outgoing stewards publish a brief state-of-the-world (open disputes, metrics drift, pending exceptions).  
- **Accountability:** Quarterly check-ins on review SLAs, dispute cycle-time, and culture health. Community can motion to rotate stewards with reasons.

---

## Templates

**Role Grant (Reviewer/Steward)**
Role: <Reviewer | Steward>
Lane(s): <build | docs | design | governance | security | community>
Scope: <repos/areas>
Term: <start – end>
Why: <evidence of readiness>
Expectations: <SLA, behaviors, conflicts disclosed>

**Decision Ownership (DRI)**
Item: <issue/epic link>
DRI: <name>
Reviewers: <by lane>
Constraints: <security, brand, legal, time>
Timebox: <start–end; checkpoints>
Metrics: <2–4>
Escalation: <steward name/link>

---

## How to Change This Page

Propose edits via PR or RFC. For structural changes (role definitions, decision rights, or appeals flow), stewards gather feedback and the Council/EthicDAO confirms. All changes must include rationale and a brief impact assessment.

---

**Bottom line:** Clear roles, explicit rights, and lightweight but firm boundaries give us the safety to disagree, the speed to ship, and the fairness to keep everyone motivated.
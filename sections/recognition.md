# Recognition

Recognition is how we turn work into dignity, influence, and momentum. It’s the engine of our collaboration: when valuable contributions are seen, verified, and rewarded, people keep building, teaching, and stewarding. In Kudora, **recognition outranks wealth**—capital can accelerate, but it cannot replace contribution.

---

## Goals

- **Make impact visible.** Credit work that others build on (code, design, docs, governance, education, operations).
- **Align incentives.** Reward behaviors that increase reuse, learning, security, and community health.
- **Stay fair and resilient.** Resist pay-to-win, cliques, and manipulation; protect newcomers and unsung work.
- **Compound progress.** Favor outputs that become frameworks and patterns others can adopt.

---

## What counts as contribution

We recognize impact across multiple lanes. Examples:

- **Build:** code, smart contracts, tooling, infrastructure, integrations, performance, security fixes.
- **Design & UX:** research, flows, components, accessibility improvements, design systems.
- **Docs & Education:** READMEs, tutorials, examples, talks, workshops, translations, mentoring.
- **Community & Ops:** onboarding, support, incident response, moderation, meetup organization.
- **Governance & Stewardship:** proposal crafting, reviews, conflict mediation, quality gates, roadmapping.
- **Ecosystem Growth:** partnerships, devrel kits, sample apps that unlock adoption.

> If it makes others faster, safer, clearer, or more capable, it deserves recognition.

---

## Evidence we look for

- **Artifacts:** PRs, commits, issues, ADRs, specs, designs, diagrams, test coverage, incident notes.
- **Adoption:** downstream usage, imports/dependencies, deployed integrations, API calls, active users.
- **Quality:** bug rates, performance deltas, security posture, accessibility checks.
- **Teaching:** docs quality, tutorial completion, mentorship feedback, talk recordings.
- **Stewardship:** review timeliness, decision clarity, conflict resolution outcomes.

---

## The Recognition Loop

1. **Create value** → a contribution with clear context and intent.  
2. **Verify** → peers review and attest to impact with evidence.  
3. **Earn Kudos** → recognition units recorded publicly.  
4. **Gain reputation & influence** → reputation graph updates; governance weight and visibility improve.  
5. **Enable bigger collaboration** → better matches, faster review, more adoption.  
6. **Repeat** → compounding effects.

---

## Kudos: the recognition unit

- **Purpose:** A portable, auditable record of verified impact.  
- **Scope:** Issued for contributions, not for holding assets or paying fees.  
- **Use:** Feeds reputation, contributor discovery, and (where relevant) governance weight.  
- **Separation:** Recognition is distinct from any financial tokens; **no pay-to-win.**

---

## How Kudos is determined

We balance simplicity with rigor. Think “transparent rules, human judgement where needed.”

### Base → Impact → Multipliers

- **Base credit:** by contribution lane (build, docs, design, community, governance).  
- **Impact rating (0–3):** negligible, useful, significant, pivotal — based on evidence.  
- **Multipliers:** reward outcomes that compound value.

Common multipliers:

- **Reuse multiplier (0.8–2.0):** increases with downstream adoption or dependency count.
- **Teaching multiplier (1.0–1.5):** high-quality docs/tutorials that meaningfully reduce support load.
- **Stewardship multiplier (1.0–1.5):** timely, constructive reviews and conflict mediation that unblock teams.
- **Risk multiplier (1.0–1.5):** security-critical fixes and incident responses.
- **Team bonus (1.0–1.3):** well-coordinated cross-role work with clear ownership and handoffs.

> **Sketch:** `Kudos = Base × Impact × (Reuse × Teaching × Stewardship × Risk × Team)`

The exact ranges are calibrated in the governance docs and may be tuned over time. All changes are logged.

---

## Process (lightweight, auditable)

1. **Open a PR/issue with an Impact Note** (see template below).  
2. **Peer review & attestations** from contributors with relevant context.  
3. **Steward check** for edge cases, conflicts of interest, or missing evidence.  
4. **Weekly recognition epoch** publishes Kudos grants, rationale, and metrics dashboard.  
5. **Appeals window** for corrections. All adjustments are public.

### Impact Note (template)

Title: <Concise contribution name>
Context: <Problem this solves; who benefits>
Change: <What was added/changed; links to artifacts>
Evidence: <Metrics, adoption, tests, user feedback, before/after>
Lane(s): <Build | Docs | Design | Community | Governance | Ecosystem>
Requested Multipliers: <Reuse? Teaching? Stewardship? Risk? Team?>
CoI: <Any conflict of interest to declare>

---

## Anti-gaming & integrity

- **Trust-weighted attestations.** Endorsements carry weight based on the endorser’s track record in the relevant lane.
- **Sybil resistance.** Identity linking and activity patterns reduce fake accounts’ influence.
- **Caps & cooling.** Per-epoch caps and diminishing returns curb wash-activity.
- **Open audits.** Random post-hoc reviews; anomaly detection flags unusual patterns for steward review.
- **Conflict of interest.** Disclose ties; recuse from endorsing where appropriate.
- **Reversals.** Fabricated or harmful contributions can be revoked; repeated abuse triggers penalties.

---

## Soft work is real work

Welcoming newcomers, writing clear docs, mediating disagreements, triaging issues, and running demos all **earn Kudos**. We target a healthy share of recognition for these contributions so they never become invisible labor.

---

## How recognition shapes governance

- **Voice follows verified impact.** Decision influence is informed by reputation in the relevant lane(s).
- **Freshness matters.** Recent impact can be weighted slightly higher to keep the system lively, while never erasing legacy contributions.
- **No wealth shortcut.** Financial stake alone does not amplify voice in recognition-weighted processes.

---

## Metrics we watch

- **Recognition Velocity:** Kudos per active contributor over time.  
- **Synergy Index:** downstream adoption of recognized assets/patterns.  
- **Coordination Latency:** time from proposal to merged decision.  
- **Trust Integrity:** ratio of upheld to reversed recognitions/attestations.  
- **Visibility to Value:** share of Kudos going to docs, education, and stewardship.

These help us tune ranges, spot drift, and keep the loop honest.

---

## Roles

- **Contributors:** deliver impact, submit Impact Notes, review peers.  
- **Reviewers:** validate evidence, suggest improvements, cite prior art.  
- **Stewards:** guard fairness, resolve edge cases, calibrate multipliers, publish epochs.  
- **Auditors:** sample, stress-test, and report anomalies; propose integrity fixes.  
- **Community:** adopt, reuse, and give feedback—your usage is a powerful signal.

---

## Examples

- **Library adopted by three teams:** base (build) × significant impact × reuse 1.6 × teaching 1.2 (excellent README).  
- **Incident response hotfix:** base (build) × pivotal impact × risk 1.5 × team 1.2; follow-up doc earns teaching 1.3.  
- **Conflict mediation & decision record:** base (governance) × significant impact × stewardship 1.4; downstream PRs reference the ADR.

---

## Transparency & data

All recognition decisions link to artifacts and evidence. Dashboards expose adoption, multipliers used, and reviewer roles. Data is exportable so teams can analyze and improve their own practices.

---

## Evolution

Ranges, multipliers, and processes can evolve via proposals and open debate. We change rules in the open, document why, and measure results after.

---

**Bottom line:** Recognition turns contributions into reputation and voice. When we honor the work that others build on—and do it fairly—cooperation becomes easier than conflict, and progress compounds.
# Glossary

A quick, shared vocabulary for the Manifesto. Short, literal, and alphabetized.

---

**ADR (Architecture/Approach Decision)** — A one-page record of a decision: context, choice, evidence, trade-offs, follow-ups, owners, review date.

**Adoption** — Downstream use of an asset (library, pattern, API, doc). A key signal for recognition and the Synergy Index.

**Agent (bot)** — An automated account that performs scoped tasks (labeling, triage). Must disclose scope, leave provenance notes, and have a human owner.

**AI Assistance** — Using AI tools to generate or transform work. Must be disclosed with provenance notes; humans remain accountable.

**Amendment (Manifesto)** — A change to this document. Classes: Editorial, Substantive, Constitutional, Emergency.

**Appeal (Recognition)** — A request to reconsider a recognition outcome with new evidence; time-boxed window after each epoch.

**Attribution** — Crediting upstream people and projects in READMEs, ADRs, and notices. Non-negotiable.

**Base Credit** — The starting recognition for a contribution before multipliers (lane-based).

**Blast Radius** — Expected impact of a change: Local (one team), Cluster (several teams), Project-wide (many teams/policy/brand).

**Brand & Name Use** — Rules to prevent confusion between official Kudora work and community or forked projects.

**Change Failure Rate (CFR)** — % of merges that require rollback/hotfix within 7 days.

**CLA (Contributor License Agreement)** — Additional license grant used only for repos intended for dual-licensing. Default is DCO, not CLA.

**Commons Exception** — A scoped, time-boxed license deviation from defaults with public rationale and exit criteria (approved via RFC/ADR).

**Consent with Objection Handling** — Decision mode where a proposal proceeds unless a substantiated objection shows harm to constraints/values.

**Constraints** — Non-negotiable limits for a decision (security, brand, legal, ethics, time, compatibility).

**Contributor** — Regular participant who owns small scopes and follows norms. Distinct from Reviewer and Steward.

**Contributor Bill of Rights** — Safety, attribution, voice, due process, transparency, data dignity, clear license to build.

**Coordination Latency (CL)** — Time from Decision Brief to ADR Accepted, by blast radius.

**Council / EthicDAO** — Top governance body. Final call on Ends (values), wide-impact exceptions, and policy.

**Decision Brief** — A one-page, pre-decision summary: problem, constraints, options, metrics, mode/timebox, risks/rollback, stakeholders.

**Decision Modes** — Lazy consensus, Rough consensus, Consent with objection handling, Formal Council decision.

**DCO (Developer Certificate of Origin)** — Signed-off-by line in commits attesting you have the right to contribute under the repo’s license.

**Dispute Cycle Time (DCT)** — Time from steward ping to outcome note.

**DRI (Directly Responsible Individual)** — Named person who owns delivery and day-to-day choices within scope.

**Ends vs. Means** — Ends = purpose/values; Means = tools/architectures/processes. Ends are decided by Council; Means by DRI/Reviewers/Stewards.

**Epoch (Recognition)** — Weekly cadence for publishing recognition outcomes and dashboards.

**Experiment (Parallel, Time-boxed)** — Small, fair trials with shared inputs/metrics to compare Means without stalling.

**Fork (Friendly)** — Time-boxed fork to evaluate an approach at scale, with merge-back intent and metrics.

**Fork (Community)** — Long-term divergence with distinct brand; must avoid confusion and maintain safe interoperability.

**Fork Ethics** — Protocols to minimize harm: declare intent, attribute, coordinate security, keep interfaces open, document divergences and migration.

**Governance (with Guardrails)** — Decision processes that embed ethical boundaries and recognition signals; includes Stewards and Council.

**Impact Note** — A short block in PRs describing context, change, evidence, requested multipliers, and conflicts of interest.

**KUDSEC ID** — Kudora security advisory identifier (e.g., KUDSEC-2025-07), paired with CVE when issued.

**Kudos** — Recognition unit for verified impact; informs reputation and voice. Separate from any financial tokens.

**Lane (Contribution)** — Work category: Build, Design, Docs/Education, Community/Ops, Governance, Ecosystem.

**Lazy Consensus** — “I plan to do X by <date> unless there’s an objection.” Works for Local Means/Taste.

**Licensing Defaults** — Apache-2.0 (libs/templates), MIT (small libs/contracts), AGPL-3.0 (servers/services), CC BY-SA 4.0 (docs), CC BY 4.0 (media), ODbL (datasets), CC0 (tiny metadata).

**Metrics (Core)** — Recognition Velocity, Synergy Index, Coordination Latency, Review SLA Hit Rate, Trust Integrity, Time to First Merge, ADR Reopen Rate, Dispute Cycle Time, Visibility-to-Value, Change Failure Rate, MTTA/MTTP, Experiment Yield.

**Migration (Guide)** — Documented steps for users to move between versions/forks safely.

**MTTA / MTTP (Security)** — Mean Time to Acknowledge and Mean Time to Patch a valid vulnerability.

**Non-Forkable Culture** — Shared norms that persist even if code forks; protected by Stewardship and Council.

**Objection (Valid)** — A constraint at risk + evidence + a concrete alternative. Required to block consent decisions.

**Outcome Note (Steward)** — One-paragraph summary of mode, owners, timebox, metrics, risks, next steps; posted to the thread after intervention.

**Parallel Trials** — Two or more small implementations run concurrently with shared metrics, then compared.

**Pilot** — A limited-scope trial of a policy/process change before amending the Manifesto.

**Provenance (AI)** — Verifiable trail of who/what/how/when for AI-assisted work (tools, prompts summary, checks).

**Recognition** — The system that turns contributions into Kudos, reputation, and voice; transparent, auditable, and anti-gaming.

**Recognition Velocity (RV)** — Kudos per active contributor per epoch (median, p75).

**Reviewer (by Lane)** — Trusted contributor who checks quality/safety within a lane and attests evidence.

**Risk Multiplier** — Recognition multiplier for high-risk, security-critical or incident-response work.

**RFC (Request for Comments)** — A public proposal for changes with cluster/project-wide impact; resolves to an ADR.

**Rough Consensus** — Broad agreement with no strong, reasoned objections; used when trials aren’t practical.

**Security Commander** — Steward/Council role activated for chain-level emergencies; coordinates embargo and validator notifications.

**SLA (Service Level Agreement)** — Target response times (e.g., reviews in 48h/72h/5d by radius; steward ack in 24h).

**Steward** — Culture keeper and friction remover; selects modes, sets timeboxes, mediates, guards fairness and safety.

**Steward Council** — Group of stewards (or the Council) handling escalations and policy confirmations.

**Sunset Review** — Scheduled check (e.g., 60–90 days) to confirm or adjust a hard-to-reverse decision/policy.

**Synergy Chain** — The compounding effect of turning good solutions into frameworks/patterns others adopt.

**Synergy Index (SI)** — Weighted downstream adoption per recognized asset over a time window.

**Teaching Multiplier** — Recognition multiplier for work that increases teachability (docs, tutorials, examples).

**Team Bonus** — Recognition multiplier for coordinated cross-role work with clear handoffs.

**Third-Party Register** — File that lists external dependencies and their licenses (e.g., `THIRD_PARTY.yml`).

**Time-Box** — A fixed time window for discussion or experiments with agreed metrics and owners.

**Time to First Merge (TTFM)** — Median time from a newcomer’s first issue comment to first merged PR.

**Trust Integrity (TI)** — Ratio of upheld vs. reversed recognitions/attestations after audits or appeals.

**Validator Security List (VSL)** — Embargoed contact list for validators/operators to coordinate critical security releases.

**V2V (Visibility-to-Value)** — Share of Kudos going to docs, onboarding, mediation, and education (“soft work”).

**Versioning (Manifesto)** — Semantic: MAJOR (Constitutional), MINOR (Substantive), PATCH (Editorial).

**Visibility (Public by Default)** — Decisions/discussions happen in open threads unless security/privacy dictates otherwise.

**Workload Lane Multipliers** — Optional recognition adjustments by lane to reflect effort/risk (calibrated via governance).

---
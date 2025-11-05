# AI & Provenance

AI can accelerate our work—but only if we keep **provenance, accountability, and safety** front and center. This page defines how we use AI, how we disclose it, what signals we record for authenticity, and how recognition applies when AI is involved.

---

## Principles

- **Human accountable.** People—not models—own outcomes. A human DRI is responsible for every change.
- **Disclose assistance.** If AI helps, say so. Hidden automation erodes trust and skews recognition.
- **Provenance over vibe.** We keep verifiable trails (prompts, parameters, checks) so others can audit and learn.
- **No reward farming.** Volume from AI is not value. We reward impact, reuse, and teaching—not copy/paste.
- **Privacy & safety first.** Don’t leak secrets or personal data into tools. Guardrails beat cleverness.
- **Open by default.** Prefer open, inspectable processes and standards for authenticity signals.

---

## What counts as “AI-assisted”

- **Generation:** code, text, diagrams, designs, tests created by an AI tool.
- **Transformation:** refactors, translations, formatting, lint-based rewrites done via AI.
- **Reasoning/analysis:** AI used to outline, draft ADRs/RFCs, or propose architectures.
- **Agents/automation:** bots that open issues/PRs, triage, label, or comment.

If in doubt, treat it as AI-assisted and disclose.

---

## Disclosure rules (lightweight, mandatory)

1. **PR level:** Add a short **AI Disclosure** block (template below).  
2. **File level:** For files generated wholesale, add a header comment noting AI assistance and the human owner.  
3. **Governance content:** Any AI help on RFCs/ADRs must be disclosed in the footer.  
4. **Media/synthetic assets:** Label clearly; add a “synthetic” note and source/method.

**No ghostwriting** for governance decisions: a human must author or co-author the final text and be reachable for questions.

---

## Provenance signals we keep

- **Who:** human DRI, reviewers, and any bot accounts.
- **What:** models/tools used (name/version), high-level method (generate/refactor/summarize).
- **How:** prompt summary or key steps (trim sensitive info), important parameters (e.g., temperature).
- **Checks:** tests passed, linters, security scans, citations for non-original material.
- **When:** timestamps per stage (draft → review → merge).

We favor **open standards** for authenticity (e.g., content signatures, manifest files) when feasible. At minimum, we keep these signals in PRs/commits and export them to dashboards.

---

## Recognition with AI in the loop

- **Credit curation, not keystrokes.** The person who frames the problem, validates outputs, writes tests, and integrates earns Kudos.
- **Teaching multiplier applies** if you document prompts, pitfalls, and verification steps that help others reuse the pattern.
- **No points for puff.** Large AI dumps without review, tests, or integration plan get rejected or zero recognition.
- **Agent work is credited** to the human maintainer(s) who configure, monitor, and review the agent’s outputs.

---

## Safety & privacy requirements

- **No secrets in prompts.** Use scrubbers; store secrets in vaults; test with dummy data.
- **PII care.** Don’t send personal data to third-party tools. If unavoidable, follow the security page and get steward sign-off.
- **License hygiene.** Don’t paste proprietary code or paid content you don’t own; track sources for generated media and text.
- **Security gates.** AI-generated code passes the same tests, reviews, and scanners as human-written code.

---

## Agent & bot policy

- **Identity:** Bots must use bot accounts, not impersonate people. Profiles state role, scope, and maintainer contact.
- **Scope:** Least-privilege tokens; restricted repos/paths; rate limits to avoid noise.
- **Transparency:** Every bot action leaves a provenance note (who/why/how) and links to configuration.
- **Human in the loop:** Merging, granting recognition, and policy decisions require human approval.
- **No astroturfing:** Bots cannot simulate consensus or social proof.

---

## Synthetic data & media

- **Label synthetic.** Clearly mark datasets or media produced with AI.  
- **Use cases:** load testing, red-teaming, documentation examples.  
- **Boundaries:** Don’t train on or mimic identifiable private individuals without consent.  
- **Reproducibility:** Share generation recipes (seeds, steps) when helpful.

---

## Licensing & attribution with AI

- Generated code/docs inherit the repo’s license; include file headers.
- Cite upstream sources and models when they materially shape the output.
- For images/audio/video, include authorship and license in metadata/README.
- Respect third-party model licenses and usage policies.

---

## Minimal workflows (copy/paste)

**AI Disclosure (PR section)**
AI Disclosure
Assistance: <generation | refactor | summary | analysis | agent>
Tools/Models: <name/version> (optional: params)
Provenance Notes: <prompt summary or steps; no secrets>
Verification: <tests/linters/scans/manual review done>
Human Owner: <@handle>

**File header (generated or heavily assisted)**
// Generated with AI assistance (tool/model: <name/version>).
// Reviewed and owned by <name/handle>. See PR <#id> for provenance and tests.

**Governance footer (RFC/ADR)**
AI assistance: <yes/no> — tools used <name/version>. Human authors: <@handles>.

**Agent manifest (in repo)**
name: kudora-label-bot
scope: triage/labels on issues in /sdk/*
owner: @maintainer
permissions: read:issues, write:labels
rate_limits: 60 actions/hour
provenance: comment with summary + link to config on each action

**Synthetic data recipe (README snippet)**
Data: synthetic wallet events for load testing
Generator: <tool/model> @ <version>
Method: <steps; seed; constraints>
Limits: no real user PII; distributions approximate mainnet without re-identification risk

---

## Review checklist (for reviewers/stewards)

- AI Disclosure present in PR?  
- Tests/security checks included and meaningful?  
- Any license/attribution risks?  
- Any secrets/PII exposure in prompts or diffs?  
- Governance text clearly authored and owned by a human?  
- Agent/bot actions within scope and rate limits?

---

## Anti-patterns (and responses)

- **Hidden AI use.** → Request disclosure; if repeated, reduce recognition and add a steward note.  
- **Reward farming via spam PRs.** → Close; warn; rate-limit; adjust recognition rules if needed.  
- **Prompt leaks of secrets.** → Revoke tokens; rotate secrets; incident report per security page.  
- **Bot consensus theater.** → Disable bot; document incident; require human summary.

---

## FAQs

**Do I have to share full prompts?**  
Share a **summary** good enough to reproduce the approach without leaking sensitive info.

**Can I ship AI-generated code without tests?**  
No. Same quality bar: tests, review, and security checks.

**Will AI use lower my recognition?**  
No—if you add value: framing, verification, integration, and teaching. We reward outcomes and reuse.

**Can an agent merge PRs?**  
Not without a human approver. Agents propose; humans decide.

---

**Bottom line:** Use AI to go faster, not lazier. Disclose help, keep provenance, pass the same safety bars, and teach what you learn—so others can build further, faster, and safer.
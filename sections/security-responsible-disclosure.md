# Security & Responsible Disclosure

Security protects people, funds, and trust. This page explains **how to report vulnerabilities**, what’s in scope, our **embargo and patch process** (including chain-level upgrades), and how recognition/bounties work. If you uncover a weakness, please report it **privately first** and give us time to fix it.

> This is community guidance, not legal advice.

---

## Principles

- **Do no harm.** Never exploit, exfiltrate, or damage data or funds.
- **Private first.** Report quietly; we fix fast; then we disclose.
- **User safety > speed.** We prefer measured rollouts over risky haste.
- **Upstream coordination.** If a flaw lives in a dependency (e.g., SDK), we coordinate with its maintainers.
- **Full credit.** Finders receive recognition (Kudos) and, where applicable, bounties.

---

## How to report (private channels)

- **Email:** `security@kudora.org` *(placeholder — update to your address)*  
- **PGP:** Publishing a PGP key is recommended; add it here with fingerprint.  
- **Emergency (critical, on-chain risk):** create an *encrypted* issue or contact a steward by email and request escalation to the **Validator Security List (VSL)**.

**Include (minimum):**
- Affected component(s) and commit/version
- Impact (what can be stolen/broken/abused)
- Proof of concept (steps or minimal exploit)
- Preconditions (auth level, config)
- Suggested mitigations (if any)
- Your handle for credit (and bounty eligibility)

We acknowledge within **24h on weekdays**, begin triage within **48h**, and keep you updated.

---

## Safe Harbor (researchers)

If you **(a)** follow this policy, **(b)** test only against your own accounts or approved dev/test environments, and **(c)** avoid privacy violations, destruction of data, service disruption, or financial loss, we will **not pursue legal action** or request law enforcement investigations.  
Stop testing if you access data that isn’t yours and report it immediately.

---

## Scope

**In scope (examples):**
- Smart contracts and on-chain modules (reentrancy, auth, overflow/underflow, logic bugs, oracle manipulation)
- Chain infrastructure (validators, sentries, RPCs, bridges, relayers)
- Protocol & consensus risks (double-sign, slashable conditions, liveness failures)
- Applications/services handling funds or credentials
- Authentication/authorization, key management, signing and transaction pipelines
- Data exposure (PII, secrets, tokens), serious CSRF/XSS/SSRF with real impact

**Out of scope (examples):**
- Clickjacking on static pages, missing security headers without exploitable impact
- Rate-limit findings without demonstrated abuse
- Vulnerabilities in third-party sites or libraries with no Kudora impact
- Low-impact CSRF on non-state-changing endpoints
- Automated scanner output without a working proof
- Social engineering of contributors/validators

When in doubt, ask first.

---

## Severity & SLAs

| Severity | Examples | Ack | Triage | Fix/Advisory target |
|---|---|---:|---:|---:|
| **Critical** | Loss/theft of funds; private key compromise; consensus failure; bridge drain | 24h | 48h | 7–14 days (hotfix or coordinated upgrade) |
| **High** | Permanent fund lock; privilege escalation; reliable remote DoS across nodes | 24h | 72h | 14–21 days |
| **Medium** | Single-node DoS; significant info leak; business logic flaws with safeguards | 48h | 5d | 30 days |
| **Low** | Minor info leaks; best-practice gaps | 72h | 7d | 60–90 days |

*Targets may adjust based on blast radius and upgrade complexity; we’ll communicate status.*

---

## Embargo, advisories, and disclosure

1. **Embargo begins** at triage; we coordinate privately with affected maintainers.
2. **Fix path selected:** hotfix, feature flag/kill-switch, or coordinated release/chain upgrade.
3. **Pre-disclosure (if chain/infrastructure):** notify the **Validator Security List (VSL)** under embargo with upgrade instructions and timing.
4. **Release & advisory:** publish patches/binaries, then an advisory with credits and CVE/KUDSEC ID.
5. **Public post-mortem:** for critical/high issues after users are safe.

**Advisory format:** `KUDSEC-YYYY-NN` and CVE (when assigned).

---

## Chain-level emergencies (special procedure)

For vulnerabilities that risk consensus, validator safety, or funds at scale:

- **Security Commander (Steward/Council)** activates incident bridge and sets embargo scope.  
- **Validator Security List (VSL)** receives an encrypted heads-up with: affected versions, mitigations, upgrade height, and action timeline.  
- **Release plan:** publish patched binaries, set upgrade height, share reproducible build info.  
- **Freeze merges** on affected repos until resolution.  
- **Post-upgrade:** release advisory + plain-language user guidance; open a reconciliation window for anyone who took emergency actions.

---

## Bounties & recognition

- **Recognition:** Valid reports earn Kudos with a **risk multiplier**; detailed write-ups/educational material can earn a **teaching multiplier**.
- **Bounties:** If/when a bounty program is active, payouts are determined by severity, clarity of report, and exploitability. Taxes/KYC may apply according to jurisdiction. *(Add link to bounty program once live.)*
- **Credit:** Advisories list researcher handles unless you request anonymity.

---

## Rules of engagement (testing)

- Prefer **devnet/testnet**; use throwaway accounts on mainnet/test environments.
- **No** data exfiltration, privilege escalation beyond proof, or fund movement without prior written approval.
- **No** sustained DoS against public infrastructure.
- **Rate limits:** keep automated testing reasonable; coordinate if unsure.

---

## Operational hygiene (for maintainers)

- **Secrets:** no plaintext secrets in repos or chat; use encrypted vaults; rotate on suspicion.
- **Keys:** hardware-backed storage for production keys; least privilege for CI/CD.
- **Dependencies:** pin versions; watch advisories; patch on schedule; reproduce builds.
- **Logging:** avoid sensitive data; enable tamper-evident logs on critical systems.
- **Backups & rollbacks:** test restore paths; document kill-switches for risky components.
- **Two-person rule:** for production upgrades and emergency actions where feasible.

---

## Templates

**Private vulnerability report**
Title: <short description>
Component: <repo/service/contract + version/commit>
Severity (self-assessed): <Critical | High | Medium | Low>
Impact: <what can be stolen/broken; who is affected>
Preconditions: <auth, config, environment>
Proof of Concept: <steps/code>
Mitigations: <ideas if any>
Researcher: <name/handle and preferred credit/anonymity>
Contact: <email/pgp/federated handle>

**Security advisory (public)**
KUDSEC-YYYY-NN: <title>
Severity: <Critical/High/Medium/Low> | CVSS (if used): <score>
Affected: <versions/modules>
Impact: <summary>
Mitigation: <workarounds until patch>
Fix: <patched versions, commits, binaries; upgrade height if chain>
Credits: <researcher handles/teams>
Timeline: <report → triage → fix → release>
CVE: <ID or N/A>

---

## Coordinated disclosure with upstream/downstream

- If the issue originates upstream, we notify them and align timelines.  
- If downstream integrators are impacted, we provide minimal details under embargo so they can prepare patches.

---

## After-action learning

For critical/high issues we publish (after users are safe):
- What failed and why,
- How we detected it,
- How we fixed and verified it,
- What we changed (tests, tooling, process).

These documents improve everyone’s safety and earn **teaching** Kudos.

---

## Contact & keys

- **Email:** `security@kudora.org` *(replace when live)*  
- **PGP:** *(add key block and fingerprint here)*  
- **VSL enrollment:** validators can request embargo notifications via the stewards. *(add form/link when ready)*

---

**Bottom line:** Report privately, we respond quickly, we protect users first, and we credit your work. Careful coordination means we can fix fast **without** breaking trust.
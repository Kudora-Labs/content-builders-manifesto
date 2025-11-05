# Licensing

Licensing should **reduce friction, not create it**. Our defaults make reuse easy, protect the commons, and keep collaboration open—while leaving a clear, time-boxed path for exceptions when partners or security require it. This page explains **what license to use where, why, and how**.

> This document is guidance for contributors. It is not legal advice.

---

## Default licenses (at a glance)

| Asset | Default license | Why |
|---|---|---|
| **Libraries & SDKs** (client/server libs, utilities) | **Apache-2.0** (or **MIT** for small/snippet-like libs) | Permissive, patent grant, widely compatible; encourages reuse and adoption. |
| **Smart contracts** | **MIT** or **Apache-2.0** | Common in Web3; easy reuse and auditability. |
| **Server / networked apps** (services, daemons, coordinators) | **AGPL-3.0** | Keeps network-delivered improvements open; prevents “SaaS enclosure.” |
| **Documentation & guides** | **CC BY-SA 4.0** | Ensures improvements remain share-alike; encourages translation and remixing. |
| **Media assets** (icons, diagrams, images) | **CC BY 4.0** | Broad reuse with attribution; avoids forced share-alike for brand assets. |
| **Open datasets** | **ODbL** (or **CC0** for small metadata) | Clarity on attribution/share-alike for databases; CC0 for tiny, factual sets. |
| **Example apps / templates** | **Apache-2.0** | Lower barrier to copy-paste and adapt. |

**Recognition ≠ licensing:** recognition (Kudos, reputation) is separate from license choice. Licensing governs reuse; recognition governs *credit and influence*.

---

## Inbound contributions (how you contribute)

- **DCO, not CLA (by default).** Sign each commit with the Developer Certificate of Origin line:  
  `Signed-off-by: Your Name <you@example.com>`
- **CLAs are exceptional.** We use a Contributor License Agreement **only** when dual-licensing is intended for a specific repo/module. The CLA and rationale must be linked in the repo README.
- **SPDX everywhere.** Put an SPDX header at the top of each file:
  - `// SPDX-License-Identifier: Apache-2.0`
  - `// SPDX-License-Identifier: MIT`
  - `/* SPDX-License-Identifier: AGPL-3.0-only */`
- **Third-party code.** Declare licenses in `THIRD_PARTY.yml` (or similar). Avoid incompatible inbound licenses (see compatibility notes below).

---

## Outbound structure (how we license repos)

Every repo must include:

/LICENSE
/NOTICE # if required by the license (e.g., Apache-2.0)
/CONTRIBUTING.md # includes DCO and PR expectations
/COPYRIGHT.md # optional, if multiple copyright holders
/THIRD_PARTY.yml # dependencies and their licenses

Example `NOTICE` snippet (Apache-2.0):

This product includes software developed by the Kudora community.
Licensed under the Apache License, Version 2.0.

---

## License selector (decision tree)

1) **Is it a server/service used over the network?** → **AGPL-3.0**  
2) **Is it a reusable library/SDK/template?** → **Apache-2.0** (or **MIT** if very small)  
3) **Is it a smart contract?** → **MIT** or **Apache-2.0**  
4) **Is it documentation or guides?** → **CC BY-SA 4.0**  
5) **Is it media/graphics?** → **CC BY 4.0**  
6) **Is it a dataset?** → **ODbL** (or **CC0** for minimal metadata)

If unsure, open a short RFC (or ask a steward). Small is better than stuck.

---

## Compatibility notes (quick guidance)

- **Apache-2.0** plays well with **MIT**, **BSD-2/3**, **ISC**, **MPL-2.0** (via redistribution terms), and can be combined into **GPL-3.0** works.  
- **MIT/BSD/ISC** are broadly compatible, including with proprietary users.  
- **AGPL-3.0** requires offering source to users who interact with the program over a network—linking AGPL code into a service brings your combined service under AGPL obligations. Keep strict **service boundaries** to avoid accidental spread.  
- Avoid bringing **GPL-2.0-only** code into Apache-2.0 libraries.  
- Always keep license texts intact when redistributing.

When in doubt, list the options and constraints in an RFC; we prefer clarity up front over re-licensing later.

---

## Commons Exception (how to deviate safely)

Sometimes partners, audits, or IP constraints require something different. Use the **Commons Exception**:

**What it is:** a time-boxed, scoped deviation from the defaults with transparent rationale and an exit plan.

**How to request:**
1. Open an RFC titled `Commons Exception — <module/area>`.
2. Include: **scope**, **reason**, **duration**, **exit criteria**, **interfaces exposed**, **proofs/tests for integration**.
3. Steward recommends; Council/EthicDAO approves if the blast radius is wide.
4. Publish the decision (ADR) and add a `COMMONS_EXCEPTION.md` to the repo with dates and conditions.

**Minimum obligations during an exception:**
- Public **interfaces**, **stubs** or **SDKs**, and **integration tests** so others can build against it.  
- Regular check-ins; sunset or renew via RFC at the end of the timebox.

---

## Attribution & notices

- **Credit upstream.** In READMEs and `NOTICE`, name the projects and people you rely on.  
- **Docs & media.** Include author credits and source links under CC licenses.  
- **Smart contracts.** Keep original license headers when forking; add your copyright lines below.

---

## Brand & trademarks (separate from copyright)

- Project names, logos, and marks follow **Brand & Name Use** rules (see that page).  
- Licenses grant copyright permissions, **not** brand endorsement. Avoid implying official affiliation without approval.

---

## Smart contracts (extra notes)

- Default to **MIT** or **Apache-2.0** for maximum reuse.  
- Keep **audit reports** public where possible; note license in the report.  
- When forking audited code, **retain headers** and **link upstream audits**; document what changed.

---

## Data & privacy

- Open datasets use **ODbL**; derived databases should respect share-alike and attribution.  
- If a dataset contains personal data or regulated information, follow the **Security & Responsible Disclosure** page—licensing does not override privacy obligations.

---

## Example headers (copy/paste)

**Go / TS / Solidity**
// SPDX-License-Identifier: Apache-2.0
// Copyright (c) 2025 Kudora Contributors

**AGPL (server)**
/*
SPDX-License-Identifier: AGPL-3.0-only
Copyright (c) 2025 Kudora Contributors
*/

**Docs (Markdown)**
<!-- License: CC BY-SA 4.0 (c) 2025 Kudora Contributors -->

---

## CI & review checks (lightweight)

- Verify SPDX headers present.  
- Fail builds if `LICENSE`/`NOTICE` missing.  
- Validate `THIRD_PARTY.yml` is up-to-date for release branches.  
- Flag inbound incompatible licenses (advisory).

---

## FAQs

**Q: Why AGPL for servers?**  
To keep networked improvements in the commons and avoid closed “SaaS trap” derivatives that benefit from the community without giving back.

**Q: Can I use MIT everywhere?**  
You *can*, but we prefer **Apache-2.0** for libs (adds patent grant) and **AGPL-3.0** for servers (protects networked improvements).

**Q: My partner demands closed terms. What now?**  
Use a **Commons Exception** via RFC: narrow scope, time-boxed, with public interfaces and exit criteria.

**Q: Do I need a CLA?**  
No, unless the repo explicitly states a CLA for dual-licensing. DCO is the default.

**Q: What about forks?**  
Forks follow the original license and **Brand & Name Use** rules. Attribute clearly and avoid brand confusion. We welcome merge-backs.

---

## Changing licenses

- Proposals to change a repo’s default license require an **RFC + ADR** and a migration plan (headers, docs, third-party updates).  
- For **copyright holder consent** in multi-author repos, follow the process in the RFC (usually an opt-in or re-license grant template).

---

**Bottom line:** Our licensing defaults maximize reuse and protect the commons, while the Commons Exception gives us a safe, time-boxed path for the rare cases that need it. Clear headers, notices, and RFCs keep collaboration smooth—and keep us focused on building.
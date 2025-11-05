# Brand & Name Use

Brand clarity protects users and keeps trust non-forkable. This page explains **how to use Kudora names and visuals**, how to name community projects, and when you need permission. Code can fork; **brand confusion cannot**.

> This is community guidance, not legal advice.

---

## What’s covered

- **Names:** “Kudora”, “Kudos”, and related product/module names.
- **Visuals:** the Kudora logomark, logotype, icons, color palette, and screenshots.
- **Namespaces:** package names, repo names, domains, and social handles.

We use “brand” to include trademarks and trade dress whether registered or not.

---

## Principles

- **Clarity over ambiguity.** Users must immediately know what is official and what is community-run.
- **Attribution without endorsement.** You can say your work is “for” or “with” Kudora without implying we endorse it.
- **Neutral experiments, distinct forks.** Experiments use neutral labels; long-term forks use distinct names.
- **Consistency beats cleverness.** Simple, consistent naming outlasts witty variations.

---

## Quick decision table

| Use case | Permission needed? | Requirements |
|---|---|---|
| Link to Kudora, describe compatibility (“Works with Kudora”) | **No** | Accurate description; include attribution; no implied endorsement |
| Community project **about** Kudora | **No** | Use community naming (see below); add disclaimer |
| Meetup, talk, article about Kudora | **No** | State you’re independent; use approved logo files; follow visuals rules |
| Product/service **by the Kudora project** | n/a (official) | Uses official naming/visuals |
| Use of official name/logo in a way that looks official (site/app branding) | **Yes** | Submit a brand request (RFC) |
| Commercial offering using “Kudora” in the product or company name | **Yes** | Brand request + disclaimer + visual review |
| Fork using “Kudora” marks | **Not allowed** | Choose a distinct name; see Fork rules |
| Domain like `kudora-<yourproduct>.com` | **Yes** | Prefer `withkudora.<tld>` or `<yourname>-for-kudora.<tld>` |
| Merchandise with Kudora logo | **Yes** | Design review + quality rules |

---

## Allowed phrases

You may use factual phrases:

- “Compatible with Kudora”
- “Built for Kudora”
- “Uses the Kudora SDK”
- “Tutorial for Kudora validators”
- “Community meetup for Kudora builders”

Avoid implying endorsement:

- ❌ “Official Kudora Partner” (unless granted)
- ❌ “Kudora Certified” (unless a real program exists)

---

## Naming conventions

### Official (project-owned)
- Repos/packages: `kudora-<area>` (e.g., `kudora-sdk`, `kudora-bridge`)

### Experimental (time-boxed, friendly forks)
- `kudora-x-<topic>` (e.g., `kudora-x-fee-engine`)  
  Must include an **experimental disclaimer** and review date.

### Community-run (independent)
- `<org>-for-kudora-<topic>` or `kudora-community-<topic>`  
  Examples: `devco-for-kudora-indexer`, `kudora-community-helm`

### Long-term forks (independent projects)
- **Pick a distinct name** (no “Kudora” in the name).  
  Example: `AuroraChain (a community fork of Kudora vX)`.

### Packages & namespaces
- npm: `@kudora/<pkg>` (official), `@yourorg/for-kudora-<pkg>` (community)
- Docker: `kudora/<image>` (official), `yourorg/kudora-<image>` (community)

---

## Visual rules (logo & assets)

- **Use approved files only.** Do not redraw, stretch, recolor, or add effects.
- **Clear space.** Keep at least the height of the “K” around the logo.
- **Backgrounds.** Use on solid or sufficiently contrasting backgrounds; avoid busy images.
- **No mashups.** Don’t combine the logo with other marks or place it inside your logo.
- **Screenshots.** Allowed with unmodified UI; blur/redact secrets; attribute source.

> Add a `/brand/` folder in this repo with SVG/PNG assets and a short `USAGE.md`. (Replace once assets are finalized.)

---

## Disclaimers (copy/paste)

**Community project**
This is a community project and is not affiliated with or endorsed by the Kudora project.
“Kudora” and related marks are used for descriptive purposes only.

**Experimental fork**
This is a time-boxed experimental fork of Kudora to evaluate <goal>.
Not an official Kudora release. We intend to propose a merge-back by <date>.

**Independent fork (long-term)**
This is an independent community fork of Kudora. We are not affiliated with or endorsed by the Kudora project.
We maintain interoperability where safe and credit upstream contributors.

**Press, talks, docs**
The views expressed are my own and do not represent the Kudora project unless explicitly stated.

---

## Domains & handles

- Prefer `withkudora.<tld>`, `for-kudora.<tld>`, or a subpath on your own domain.
- Avoid registering domains that could be mistaken for official sites (e.g., `kudora.app`, `kudora.io`) unless you are the project.
- Social handles should not look official (e.g., use `@<org>ForKudora`, not `@KudoraOfficial`).

If you own a confusing domain/handle, you may be asked to add a disclaimer or transfer it.

---

## Using “Kudos” (the recognition unit)

- Use “Kudos” only to describe the recognition system.  
- Don’t market financial products/services as “Kudos” or imply price/returns.  
- If you reference other tokens, make the distinction explicit.

---

## Requesting permission

Open an **RFC: Brand Request — <purpose>** including:
- What you want to use (name/logo/marks)
- Where it appears (product, site, event, merch)
- Mockups or screenshots
- Duration/timeframe
- Disclaimers you’ll include
- Contact person

Stewards review for clarity and safety; Council confirms for wide-impact uses. Expect a short feedback loop (mockups help).

---

## Violations & remediation

- **First step:** we’ll ask for fixes (rename, add disclaimers, replace assets).  
- **Persistent confusion or misuse:** public note and revocation of permission; we may request takedowns for harmful cases.  
- **Good faith matters:** transparent intent and quick fixes go a long way.

---

## Checklists

**Before publishing anything that uses the brand:**
 Is it obvious whether this is official or community-run?

 If community-run, did I include the disclaimer?

 Am I using approved logo files without modifications?

 Is the name compliant with conventions (no implied endorsement)?

 Do domain/handles avoid official-looking names?

 Do links point to the official site/repo for context?

**For forks & distributions:**
 Distinct name (no "Kudora" for long-term forks)

 DIVERGENCES.md and MIGRATION.md included

 Security advisory coordination arranged

 README disclaimer present

---

## FAQs

**Can I call my meetup “Kudora Builders Meetup – <City>”?**  
Yes, if you include the community disclaimer and use approved visuals.

**Can my company use the Kudora logo on our landing page?**  
Yes, to indicate compatibility (e.g., “Works with Kudora”), with proper attribution and no implied endorsement. For co-marketing, submit a Brand Request.

**Can I name my product “Kudora Wallet”?**  
No. Use a distinct name like “<YourName> Wallet for Kudora”.

**Can a friendly fork keep the name?**  
Not as a primary name. Use a neutral experimental label and set a review date. Long-term forks must rebrand.

---

**Bottom line:** Use the brand to help people find trustworthy, compatible work—not to create confusion. Clear names, clean visuals, and honest disclaimers make collaboration easier and keep users safe.
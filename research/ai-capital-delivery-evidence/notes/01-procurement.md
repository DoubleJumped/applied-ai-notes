# 01 — Procurement papers: numbers, method, datasets

Scope: Velocity White Papers on procurement and the tooling behind them.
- **m66qi** "Taking the Hill: Innovating on Procurement with AI Insights" (Paper 22, published 2026-07-18). https://thevelocitywhitepapers.com/paper/m66qi/
- **bbkac** "Git Insights" (Paper 3, 2026-06-16). https://thevelocitywhitepapers.com/paper/bbkac/
- **offjm** "Git Insights Ministry" (Paper 4, 2026-06-16). https://thevelocitywhitepapers.com/paper/offjm/
- Plus the repo data files, the public GovAlta repos the papers point to, and press coverage of the $54M claim.

Source files: `sources/velocity-repo/app/site/data/papers/<id>.en.json` (repo snapshot committed 2026-09-05). I checked the live m66qi page on 2026-09-23 and it matches the repo.

---

## IMPORTANT: the $54M vs $2.5M figure is NOT in the white papers

I searched every English paper JSON, the site pages, transcripts and the live m66qi page. None of them contain "$54 million" or "$2.5 million". The only dollar figure in m66qi is the forward-looking **$100–200M** procurement tranche.

The $54M figure is the **Minister's spoken claim at the Velocity Symposium (July 28, 2026)**, as reported in the press:

> "We've had examples in-house where we've built things for 95 percent cheaper and in 95 percent less time," Glubish said. He added that, in one instance, a government contract's lowest bid was for $54 million over a three-year period. Using in-house AI alternatives, Glubish claimed the Province was able to meet the contract's needs for just $2.5 million in less than a year.
> BetaKit, Jesse Cole, "Alberta's AI push is rewriting the rules for government contractors", July 28, 2026. https://betakit.com/albertas-ai-push-is-rewriting-the-rules-for-government-contractors/

Digital Journal ("What Alberta's AI numbers mean for IT pricing", https://www.digitaljournal.com/article/what-albertas-ai-numbers-mean-for-it-pricing/) uses different tense. The site blocked direct fetch, so this wording comes from a search-engine summary and is not verbatim: the Minister "said one project had drawn a bid of $54 million over three years. He said the province is **developing** a solution for about $2.5 million, with a first version working within 10 months."

Other things the Minister said in the same BetaKit piece:
- "...the traditional time and materials billing system is out of date, and not here to stay"
- "If you're going to come and bid to us and say 'No, we want to bid at 100 percent of what we used to, the way we would've done this two years ago,' well, I know that you're doing it for far less..."
- "Anybody who's stuck in the old ways and doesn't want to change—you're probably not going to do much work with us anymore."

**How to cite it:** say it is a ministerial claim reported in the press, not a documented result in the papers. The project isn't named, and no scope, bid document or method is published. The sources also disagree on whether the $2.5M build was delivered ("was able to meet") or still underway ("is developing", "first version within 10 months"). Treat $54M vs $2.5M (about 95% lower) as an **unverified anecdote**.

---

## Headline numbers

| # | Number | What it measures | Baseline | Type | Source |
|---|---|---|---|---|---|
| 1 | **$54M (3 yrs) vs $2.5M (<1 yr / ~10 months)** | Lowest vendor bid vs in-house AI build for one unnamed contract | Lowest compliant vendor bid | **Anecdote, verbal claim**, not in papers | Minister, press, 2026-07-28 |
| 2 | "95 percent cheaper and 95 percent less time" | In-house AI builds vs traditional | Unspecified | Anecdote / claim | Minister, press |
| 3 | **$100–200M** | Upcoming procurement expected to use the new evidence-and-data model | n/a | **Projection / intent** | m66qi |
| 4 | "up to 99%" | Share of businesses screened out by narrow specs | n/a | **Assertion, no method given** | m66qi |
| 5 | "10×" | Specificity vendors find in the code vs what the RFP described | RFP text | **Assertion / rule of thumb** | m66qi |
| 6 | 4,041 apps / 2,182 capabilities / 40 domains | Scope of the released estate dataset | n/a | **Measured** (scan output) | m66qi, dataset |
| 7 | 75,582 screens / 73,516 workflows / 206,224 rules / 112,088 endpoints / 23,966 integrations | Work units visible to bidders | n/a | **Measured** (AI extraction; accuracy not validated in paper) | m66qi |
| 8 | Disposition: 37.8% maintain, 34.0% remediate, 18.3% retire/consolidate, 9.9% rebuild | Recommended action per app | n/a | **Model output** | m66qi, dataset |
| 9 | Bid prep "hours instead of weeks" | Vendor effort to submit a successful bid | Current bid prep | **Aspiration / target** | m66qi |
| 10 | 466M lines in ~20 hrs, ~50 agents, "under two thousand dollars" | Cost/time of the whole-estate AI scan | "no consultant engagement could match" (no figure) | **Measured** (own report) | bbkac |
| 11 | 185 → 16 | Apps in one ministry collapsed into reusable modules | n/a | **Design proposal** (not yet built) | offjm |
| 12 | 80/95/85/85/40/30% | AI compression by work type (design/code/QA/ops/security/product) | Traditional effort | **Estimating rubric** (assumption) | offjm |
| 13 | 1,726 → 286 person-months; "close to forty-two million dollars saved" | Rebuild effort for the 185-app ministry | Traditional delivery | **Simulation estimate** | `data/sims/rationalize.json` |
| 14 | $108K vs $1.3–1.9M, 11 weeks vs 12–18 months | ACIP app, factory build vs traditional | Traditional delivery **estimate** | Actual cost vs estimated counterfactual | rhx4t (cross-ref, see 02 notes) |
| 15 | $2B+ vs $80–120M/yr | Estate modernization cost vs annual budget | n/a | **Rough estimate** ("simple heuristics") | cux4h (cross-ref) |
| 16 | "several hundred million dollars" in Application Master Services Agreements | Existing vendor contracts for app upkeep, "failing to deliver" | n/a | Stated fact, not itemized | cux4h (cross-ref) |

---

## Detailed claims with quotes

### m66qi — Taking the Hill

**$100–200M procurement tranche (projection)**
> "The next one hundred to two hundred million dollars of procurement in this space is expected to follow this evidence and data-driven model, with a refined dataset released before that tranche opens." (keystat, value "$100–200M", label "Procurement we expect this model to enable")

Measures upcoming procurement spend, not savings. It is an intent statement. "In this space" means IT modernization.

**Up to 99% screened out (assertion)**
> "That proficiency comes from experience, and the complex process may screen out as many as ninety-nine percent of all other businesses from doing business with government."
> keystat: "up to 99%" — "OF BUSINESSES SCREENED OUT BEFORE A FAIR CONTEST BEGINS"

No method or data given. Note the hedge ("may", "as many as").

**10× hidden specificity (assertion)**
> "Vendors routinely discover roughly ten times more specificity buried in the code than any procurement document described, driving cost and time overruns."
> "When the winning vendor gets in the door, they may find something like ten times more specificity buried in the code."

This is the paper's reason for change orders and contingency padding. No measurement is given.

**Bid-review burden (qualitative)**
> "When we receive a bid, we carry a legal obligation to review every single page of the package. Often the bids we receive run hundreds to thousands of pages long... Large bid packages can extend the timelines for a procurement by months. As a defensive mechanism, procurements are written narrowly so as to typically keep the field to fewer than ten anticipated bidders."

**Incumbent advantage and contingency (qualitative, the core argument for a utility)**
> "The incumbent holds an outsized advantage because they can bid with slim contingency margins: they already know the shape and the look of the code, even though that shape is written down nowhere."
> "Procurement requirements are vague and over-compressed, and vendors have to guess to win the contract, and to implement change order language which accrues to their benefit."
> "A serious bidder can use AI to analyze the data and generate a grounded proposal, in place of guessing at undocumented legacy systems and padding the price with contingency."

**Weak internal cost estimates push buy/build decisions the wrong way (qualitative)**
> "If we cannot see the ground truth of our technical domain, we necessarily struggle to estimate time, cost, and risk, and we lean on heuristics that are imprecise, inaccurate, or incomplete. That drives the business toward a vendor product, or away from one and toward a build, when either choice may have been inappropriate."

**Estate scale (measured, table "The estate at a glance")**
Applications 4,041; capabilities 2,182; domain clusters 40; screens 75,582; workflows 73,516; business rules 206,224; API endpoints 112,088; integration dependencies 23,966. Source: "Git Insights metadata release, schema gov-metadata/1.0, fleet run 3."

Coverage caveat: "This first snapshot does not yet cover the whole of government. Several major commercial platforms, such as our SAP-based 1GX system, are absent from this release."

**Disposition split (model output)**
Maintain/Monitor 1,527 (37.8%); Remediate (AI Garage) 1,375 (34.0%); Retire/Consolidate 739 (18.3%); Rebuild (AI Factory) 400 (9.9%). "computed from health, activity, and complexity." I confirmed these match the released repos.json exactly.

**Bid effort target (aspiration)**
> "Submitting a successful bid should take hours instead of weeks, with AI tools to support compliance and validation."
> "AI also supports the evaluator, so procurement staff can analyze and compare hundreds of proposals which address a variety of challenges easily and rapidly."

**Mismatch detection (the "bid challenge" mechanism)**
> "If a vendor proposes a solution with ten screens to replace one that has a thousand, that mismatch becomes immediately visible, in place of being hidden inside glossy brochures or compressed abstracts."

**Build vs buy stance**
> "In the AI era, we are less interested in another black-box COTS or SaaS product, because if a vendor can build it with agents, so can we."

### bbkac — Git Insights

- > "Fifty agents read 466 million lines of code in roughly 20 hours" (measured)
- > "What AI made possible was the analysis of a vast digital estate for almost no cost, under two thousand dollars, in a matter of hours." (measured, scan compute cost)
- > "A scan of the whole estate that no consultant engagement could match in time or cost." (comparison asserted, no consultant figure given)
- Records per repo include "Effort and issues: An AI-assisted estimate of the effort to modernize it". The effort estimate is the seed of in-house pricing.
- 40% of products met every standard on first release (pre-AI human baseline, measured internally). Relevant to vendor quality, not price.
- 1,280 repos (39.2%) had no docs; 49.6% no tests; 73.9% no CI/CD (measured).
- > "we believe we can achieve in some areas a 10 to 1 reduction of our redundant code through AI-driven standardization" (belief/projection)
- Press coverage (not in the paper) says a human-led equivalent "could have taken more than six years and cost upwards of $2 billion". That is a government estimate reported secondhand.

### offjm — Git Insights Ministry

- > "In one Alberta ministry, 185 applications can be collapsed into sixteen reusable modules." (design proposal; press elsewhere says 165→16)
- Costing method (the key line):
  > "Costing for the replacement systems is based on real heuristics, such as the number of screens, endpoints, database tables, and workflows. Ordinary code works it out from a fixed set of rates, so we can defend it line by line."
- Compression rubric ("Where the work compresses"): architecture/design ~80%, engineering/coding ~95%, QA ~85%, ops/infra ~85%, security/privacy ~40%, product/validation ~30%.
  > "A contingency and a program overhead are added on top, and the figure is recomputed line by line from this rubric rather than taken as a single number the AI produced."
- > "we collapse the complexity and attack surface of our infrastructure by more than ninety percent" (projection)
- The executive dashboard includes "Compression economics: The effort to rebuild traditionally versus with AI, broken down by type of work."

### Simulation dataset (site repo `data/sims/rationalize.json`, the 185-app ministry)

- person_months_traditional **1,726**; person_months_ai **286**; compression "6:1"; schedule 14 months; 859 capabilities, 814 preserved (94.8%), 45 deliberately not preserved.
- Narration, chapter 08: > "Done the traditional way, this is roughly one thousand seven hundred person-months of work, five to eight years. Rebuilt this way, the estimate is about two hundred and eighty-six person-months across fourteen months. That is a six-to-one compression in effort, and close to forty-two million dollars saved."
- Explicitly a simulation: > "This is a simulated run at high speed... That lets us test the approach and estimate the effort before we touch any production system." It is an **estimate**. The $42M implies about $29k per person-month (roughly $1,600 per day at 18 days/month), but the rate is not stated.
- Example service ("Document & Content Management"): 36 PM traditional vs 7 PM AI, team of 4, 9 months, about 5×.

---

## Method (how they did it)

The process has three parts. In short: build your own evidence base from the source of truth, price the in-house alternative bottom-up from counted work units with fixed rates, and make vendors map their bids onto the same units.

### 1. Establish ground truth (Git Insights, bbkac)
- Around 50 agents (Claude Opus/Sonnet on Google's agent platform) clone every repo and run a fixed routine.
- **Deterministic tier**: code counts files, checks for README/tests/CI, and finds known-bad patterns. This tier cannot invent results.
- **AI tier**: judgment only. Every finding must cite file and line, and scoring uses a fixed checklist.
- Output per app: health scores, stack, dependencies, capabilities, disposition, and an effort estimate.

### 2. Count work units and price the in-house alternative (Git Insights Ministry, offjm, and HUB code)
- AI reverse-engineers each system into a dossier covering screens, workflows, APIs, data entities, business rules and integrations, each tied to a source file.
- Findings are clustered into business capabilities, and a target set of modules is designed with a "preservation audit" that checks no capability is lost.
- **Pricing is deterministic code, not the LLM.** From `GovAlta/GIT-INSIGHTS-HUB/lib/reporting/estimate.js`: they found that LLM-produced estimates "swung ~34% on total_days / total_cost" across three identical re-runs, so "A DM-facing dollar figure must be reproducible. So the numbers are computed HERE, in code."
- Formula (`profiles/default.estimation.md` plus code):
  - Per-unit AI-assisted person-days by complexity (simple/moderate/complex). Doc values: service 1/3/7, screen 0.5/1.25/2.5, workflow 1.5/3.5/7.5, API endpoint 0.15/0.4/0.8, external integration 2.5/4.5/9, data entity 0.25/0.5/1.
  - The complexity mix comes from a deterministic legacy-severity score: dormant +2, poor docs +1, no tests +1, hard legacy DB +1, SOAP/WCF +1, open criticals +1.
  - DB migration = 10 + 0.5 × entities × legacy factor (1.5 for mainframe or stored-procedure-heavy databases).
  - Overheads on build: testing, security, PM and discovery at 15% each; discovery rises to 25% if dormant. Accessibility is +10% of screen effort for public UI. DevOps is fixed at about 18–25 days.
  - Contingency is 20/30/40% by confidence.
  - Cost = days × **$900 CAD blended day rate** ("illustrative loaded rate; confirm against your vendor/FTE rates"). Calendar = days ÷ team (4) ÷ 18.
  - A pre-AI adjustment is given for reference: CRUD/UI ×4, integration/security/novel logic ×1.8.
  - The doc includes a worked example: an app with 44 screens, 31 workflows and 40 entities comes to about 899 person-days, **about $0.81M**, about 12 months with a team of 4.
- The exported dataset keeps cost bands only: rebuild band, remediate band (= rebuild × 0.35), and person-days band.

### 3. Structured bids and AI-assisted evaluation (m66qi)
This is what a "bid challenge" looks like in their model:
1. **Publish the evidence.** A de-identified capability and work-unit dataset goes out before the RFP, so every bidder prices the same counted scope and the incumbent's information advantage disappears.
2. **Give bidders a recipe.** "we are releasing a CLAUDE.md file that gives every bidder the exact recipe for a compliant response." I could not find this bidder CLAUDE.md in the public repos.
3. **Require a machine-readable crosswalk.** "Each bid must include a machine-readable crosswalk file that links every page or section of the narrative back to the specific capability nodes, health scores, or repository metadata it claims to address."
4. **AI shreds each bid.** "An AI reviewer can then shred the entire package and extract the structured fields for cost, capability coverage, evidence citations, local support capacity, and risk."
5. **Compare in one frame.** Procurement sees "who has bid where, where costs are concentrated, and what bid types are on offer". Scope mismatches show up directly, for example a bid with ten screens against a system with a thousand.
6. **Filter on proof, not polish.** "a high-pass filter screens out the low-quality noise; an AI evaluation scores what remains on verifiability, relevance, and feasibility". Vendors must supply "a working prototype slice, a harnessed agent workflow, or a reproducible build script".
7. **Timeline.** Dataset released at the Symposium (2026-07-28), two months for industry to build, demos at Agency (October 2026), then procurement tranches prioritized against what was shown.

**What the papers do NOT show:** a worked example of challenging a specific vendor bid, such as "vendor quoted X, our bottom-up estimate was Y, we negotiated or built instead." The $54M anecdote is the only instance, and it is undocumented. The pieces are all published, though: counted scope, deterministic in-house estimate, and structured bid crosswalk. That is enough to build a should-cost comparison.

---

## Datasets in repo

**Site repo (`sources/velocity-repo/app/site/data/`)**
- `papers/*.json`, `papers.json`: paper content and inventory (22 papers). No procurement datasets.
- `repos.json`: list of 7 GovAlta repos linked to papers. GIT-INSIGHTS and GIT-INSIGHTS-MINISTRY are "on-request" (private, available to other Canadian governments). It does **not** list GIT-INSIGHTS-HUB or the released dataset repo.
- `sims/rationalize.json` (152 KB): simulated 185-app ministry rationalization. Per-app counts (screens, APIs, entities, workflows, integrations, health, PII), 16 target services with `pm_trad`, portfolio metrics (1,726 vs 286 PM), and preservation ledger. Service names suggest a transportation ministry: permits, carrier safety, road network, capital asset inventory, maintenance work management, grants and capital programs.
- `canvas/landscape.json`: node-graph scenes for the interactive canvas. Illustrative only.
- `sims/gov3*.json`: animation scripts. Not data.

**Public GovAlta repos (external, checked 2026-09-23)**
- **GovAlta/VELOCITY-GIT-INSIGHTS**: the actual released dataset (gov-metadata/1.0, fleet run 3, scanned 2026-07-16 to 07-18).
  - `data/repos.json` (9 MB, 4,041 records keyed by UUID): capabilities, domain clusters, tech stack, integration type counts, LOC/file bands, age and vintage, security bands, PII flag, aligned ministry, disposition, and **cost bands**.
    - Rebuild band: <100k: 1,448; 100k–500k: 1,514; 500k–2M: 876; 2M–10M: 186; >10M: 17.
    - Remediate band: <100k: 2,381; 100k–500k: 1,340; 500k–2M: 275; 2M–10M: 45.
    - Person-days band: <100: 1,374; 100–500: 1,478; 500–2k: 952; >2k: 237.
  - `data/capabilities.json`: 40 domain clusters, then 2,182 capabilities, then app UUIDs.
  - `data/tech_stacks.json`: languages and frameworks by app count.
  - `data/provenance.json`: redaction summary. 7,921 k-anonymity generalizations (k=5), 3 LLM redactions, certified shareable.
  - Also 12 visualizations (including a risk × rebuild-cost heatmap) and a PDF briefing.
- **GovAlta/GIT-INSIGHTS-HUB** (public, MIT): the scanner and exporter. Holds the estimator (`lib/reporting/estimate.js`), the rates doc (`profiles/default.estimation.md`), a business-case generator, and `scripts/export-gov-metadata.js`, which does the de-identification and banding. This is the most reusable asset for a should-cost approach.
- **GovAlta/agency-26-hackathon**: not referenced by m66qi, but procurement-relevant. A Postgres pipeline over Alberta open data: **Blue Book contracts (67,079 records)**, **sole-source contracts (15,533)**, grants (about 2M rows, FY2014-15 to 2025-26), and the non-profit registry. Includes analysis scripts such as `04-sole-source-deep-dive.js`. It is a template for AI analysis of public contract-award data. It does not evaluate bids.

---

## Caveats

What the papers say themselves:
- The dataset is "a point-in-time snapshot, with future releases expected as our methods mature"; the SAP-based 1GX is excluded; "Domain clusters and capabilities are machine-derived; treat the map as a rich starting point, not a hand-curated taxonomy."
- The estimation rates are "ILLUSTRATIVE starting points. Calibrate them against your own delivered rebuilds", and the $900/day is an "illustrative loaded rate".
- The LLM-only estimates varied by about 34% between runs, which is why arithmetic moved to code.
- cux4h says the $2B figure used "some simple heuristics; the cost is likely much higher."
- The rationalization is labelled a "simulation" and "rehearsal".
- The dataset README flags re-identification risk through capability linkage.
- m66qi itself warns that AI makes it easy to "generate a glossy, reasonable-looking proposal" (the "No slop, please" section). Opening data and lowering bid effort can bring back the flood of bids the process is meant to fix.

My own caveats:
- **The $54M/$2.5M is not in any paper.** It is an unnamed project described verbally by a minister, and the two press reports disagree on whether the build was finished.
- All "traditional" baselines are **estimates of a counterfactual**: ACIP's $1.3–1.9M, the 1,726 PM, the $2B. None are competing bids. Only the $54M is described as an actual bid.
- The in-house figures are for **AI-assisted software builds on a standard stack by an internal factory team**. They likely exclude or understate change management, long-term ops and support, product ownership, and the political and delivery risk the government now carries itself.
- Counts such as screens and workflows are AI-extracted. The papers don't report precision or recall for them.
- Code rates and doc rates differ: the code's `DEFAULT_RATES` are about 2× the doc's per-unit values for screens and endpoints, and have 20% testing and 25 days of DevOps. So even their "deterministic" figure depends on which rate table is loaded.
- "Up to 99% screened out", "10× specificity" and "95% cheaper" are rhetorical and unsupported by published data.
- All of these papers were written by the ministry advocating the approach. There is no independent audit.

---

## Transferability to a utility's procurement and bidding (my read)

**What transfers well**
1. **Should-cost from counted scope.** This is the core idea. Break the scope into units (for software: screens, workflows, endpoints, entities, integrations) and apply calibrated per-unit rates, complexity drivers, overhead percentages and contingency in deterministic code. Use the LLM for extraction and narrative, not arithmetic. This gives an independent estimate to test vendor bids against. A utility can do this **today for IT/OT software procurements**, such as customer and billing portals, work management, GIS integrations and field-inspection apps. The Alberta dataset's own service list includes "Capital Asset Inventory", "Maintenance & Work Management", "Mobile Field Inspection" and "Geospatial Asset Registry", which map closely to utility systems.
2. **Buy vs build grounded in evidence.** The paper's point that weak internal estimates push decisions toward vendors (or away from them) wrongly applies directly. An internal AI-assisted build estimate is a strong negotiating reference even if you never build it.
3. **Structured bids and AI evaluation.** Require a machine-readable crosswalk from each bid to the scope units, then use AI to extract cost, coverage, evidence and risk into one comparison frame. This is independent of domain and works for capital RFPs too. The risk is legal: public-sector-style "must read every page" obligations and fairness rules still apply, so AI supports evaluators and doesn't replace them.
4. **Break the incumbent's information advantage.** Give all bidders the same detailed scope data to reduce contingency padding and change orders. For a utility, that could mean asset-condition data, as-builts or integration inventories in place of code.
5. **Public contract-data analytics.** The hackathon pipeline (contracts and sole-source) is a template for benchmarking against published award data.

**Where it does NOT transfer, or needs heavy adaptation**
1. **Physical capital projects are not software.** The 95% and 6:1 compression claims come from AI writing code. AI does not pour concrete, weld pipe, buy steel or dig trench. Materials, equipment, labour, right-of-way, permitting and regulatory approvals dominate capital project cost, and AI does not shrink them. **No number in these papers should be quoted as a projected saving on pipeline, station or facility capital.**
2. **The "ground truth" source is different.** For software, the code *is* the complete spec, and AI can read all of it. For physical assets, the equivalent sits in GIS, asset registers, inspection records, drawings, historical bids and actuals, and cost databases, and it is usually messier and less complete. The method transfers only if you have (or build) that dataset.
3. **Rates must come from your own history.** For capital work, the equivalent of $900/day and per-screen days is unit-rate cost libraries (per metre of pipe by diameter and terrain, per station and so on) calibrated on your own completed projects. AI's contribution is extracting and normalizing past bids and actuals into that library and flagging outlier bid line items. The AI doesn't produce the rates.
4. **"Build in-house" is rarely an option for construction.** The $54M → $2.5M story works because a small AI-assisted team can replace a vendor's software team. For capital delivery the realistic lever is **bid challenge and negotiation** (should-cost vs quote, line-item outlier detection, scope-gap detection), plus faster estimating and evaluation. Self-performing the work usually isn't realistic.
5. **Regulatory context.** A utility's capital spend goes through rate regulation. Credible, reproducible cost evidence has value in its own right, and Alberta's insistence on deterministic, auditable arithmetic is the part to copy.

**Bottom line for the pitch:** the credible, transferable story is "AI lets us produce an independent, reproducible should-cost and structured bid comparison quickly". That's supported by published code and method. It is safe to use for IT/software procurement now, and as a method (not a savings rate) for capital bid evaluation. The $54M/$2.5M line is useful to illustrate how far vendor pricing can sit from AI-assisted cost. It should be presented as a minister's unverified anecdote about software, not as evidence of what capital projects could save.

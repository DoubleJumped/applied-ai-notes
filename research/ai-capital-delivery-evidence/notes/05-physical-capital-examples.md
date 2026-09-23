# 05 — AI in physical capital delivery: additional before/after examples

Researched 2026-09-23. This adds to note 04, which already covers Exponent (Class 5 → Class 3), NiSource (>20% field productivity), McKinsey × ALICE, Flyvbjerg's 8.5% and Walmart/Pactum. None of those are repeated here.

**How each example was checked.** Every URL below returned HTTP 200 on 2026-09-23, and every quoted number was confirmed on that page. Some sites block automated readers but load normally in a browser; for those, the text was pulled with a browser-style request and searched directly. A few PDFs needed text extraction, and the page number is given so the reader can find the figure.

**Credibility key.** **M** = measured or audited by a public body. **P** = pilot, trial or back-test. **S** = the organisation reporting its own result. **V** = vendor marketing or a vendor press release.

---

## Summary table

| # | Org | Area | Before → After | Cred. | URL |
|---|---|---|---|---|---|
| 1 | Duke Energy (with AWS) | Engineering studies for grid upgrades | 2 weeks of manual data prep → hours | V (named utility quoted) | https://press.aboutamazon.com/aws/2026/9/aws-launches-agentic-grid-planning-program-to-accelerate-interconnection-studies |
| 2 | SP Energy Networks (with Keen AI) | Connection design options plus cost estimates | Hours of manual engineering (weeks end to end) → under 5 seconds | V/S | https://www.solarpowerportal.co.uk/solar-projects/sp-energy-keen-ai-announce-ai-powered-grid-connection-tool |
| 3 | Wisconsin DOT | Capital cost estimating (ML) | Old cost tables → 30% lower MAPE, about $850M less estimating error over the 10-yr program | P (consultant-reported) | https://www.ltrc.la.gov/pdf/2026/FR_722.pdf (p. 46) |
| 4 | US DOT Inspector General | Bid analysis and collusion detection (ML) | ML flagged ≥1/3 of contracts; flagged contracts cost 5.2–10.2% more, $1.19B in total | M (federal audit) | https://www.oig.dot.gov/library-item/46639 |
| 5 | Indiana DOT (FHWA) | Bundling capital work into contracts (ML) | Manual bundling → +40% bundling savings, $108M expected over 4 yrs | S (reported by FHWA) | https://www.fhwa.dot.gov/innovation/innovator/issue83/page_04.html |
| 6 | Network Rail (nPlan) | Schedule and cost risk forecasting | Back-test on £3bn of capex: up to £30m could have been saved on one project | P (back-test) | https://www.networkrailmediacentre.co.uk/news/network-rail-using-innovative-technology-to-transform-project-planning-and-delivery |
| 6b | Transpennine Route Upgrade (Network Rail) | Schedule risk analysis (QSRA) | Monthly per project and every 3–6 months per programme → whenever a schedule updates | V (client quoted) | https://www.nplan.io/press-releases/nplan-on-track-for-rail-sector-expansion-with-transpennine-route-upgrade-deal |
| 7 | MassDOT (HEKA) | Engineering-standards assistant for designers | Weeks spent navigating standards → 78% less manual search time | S (reported by the builder) | https://burnes.northeastern.edu/wp-content/uploads/AI-FOR-IMPACT_-WHAT-WE-HAVE-BUILT-2.pdf |
| 8 | Kiewit (EPC) | Early design and estimating automation | 8 weeks → 8 minutes (3D model); layouts days → about an hour; mass-haul "months" → minutes to an hour | S | https://www.kiewit.com/newsroom/innovation-from-the-inside-out/ |

---

## Detail

### 1. Duke Energy + AWS: agentic AI for grid-upgrade engineering studies
- **What they did:** Duke's transmission engineers use AWS AI agents that run their existing simulation software, grid models and engineering standards to prepare and run interconnection studies. The studies cover upgrade decisions: reliability, cost and customer impact.
- **Before:** two weeks of manual data preparation. **After:** hours.
- **Quote:** "Duke Energy, the collaborating utility, has seen data preparation tasks go from two weeks of manual work to hours utilizing these agents." John Pressley, Managing Director of Digital Strategy and Engineering at Duke, is quoted: "Duke Energy engineers are using specialized AWS AI Agents to study grid upgrade decisions around reliability, costs, and the impact on customers ... all through auditable and codified Agentic workflows."
- **URL:** https://press.aboutamazon.com/aws/2026/9/aws-launches-agentic-grid-planning-program-to-accelerate-interconnection-studies
- **Date:** 2026-09-17
- **Credibility:** V. This is the vendor's press release, but a named Duke executive is quoted. The saving is in data preparation only, not the whole study.
- **Why it matters for a gas utility:** It is the closest US utility example of AI agents working inside regulated engineering-study workflows while engineers stay accountable. The same pattern could apply to gas system capacity studies and main-extension sizing.

### 2. SP Energy Networks + Keen AI: "IConn" connection options with cost estimates
- **What they did:** SPEN (the Scottish transmission and distribution network) built a tool with Keen AI. It digitises the transmission network and, for each connection request, generates possible routes, **estimated costs**, simulated power flows and technical constraints.
- **Before:** "hours" of manual engineering analysis per assessment; the full answer to a developer took "several weeks". **After:** "less than five seconds".
- **Quote (Solar Power Portal):** the tool processes "raw network data on locally hosted models" to estimate connection routes, costs, power flows and technical constraints "in less than five seconds". "SP Energy Networks said this process would usually require 'hours' of manual engineering analysis."
- **Backup source (New Power, same date):** "information that would previously have taken several weeks due to resource-intensive processes." https://www.newpower.info/2026/05/ai-speeds-up-optioneering-for-new-connections-to-spen-network/
- **URL:** https://www.solarpowerportal.co.uk/solar-projects/sp-energy-keen-ai-announce-ai-powered-grid-connection-tool
- **Date:** 2026-05-06
- **Credibility:** V/S. This is a joint utility and vendor announcement reported by trade press. SPEN's own press release page blocks automated readers but is at https://www.spenergynetworks.co.uk/news/pages/sp_energy_networks_and_keen_ai_launch_digital_tool_for_new_grid_connections.aspx
- **Why it matters for a gas utility:** It is a regulated network doing option design and a first cost estimate together in one AI step. That maps directly onto gas customer-connection and main-extension estimates.

### 3. Wisconsin DOT: machine-learning cost model vs lookup tables
- **What they did:** WisDOT replaced its cost-estimating lookup tables for pavement preservation projects with an interpretable machine-learning model trained on historical project costs.
- **Before:** the existing cost estimation tables. **After:** a 30% lower mean absolute percent error.
- **Quote (p. 46):** "Compared to WisDOT's previous cost estimation tables, the new model achieved a 30% reduction in mean absolute percent error, equating to an estimated $850 million reduction in error across WisDOT's 10-year program."
- **URL:** https://www.ltrc.la.gov/pdf/2026/FR_722.pdf. This is the Louisiana DOTD / FHWA report *Artificial Intelligence and Its Role and Use Within State DOTs* (FHWA/LA.26/722), which lists more than 60 DOT AI use cases.
- **Date:** January 2026
- **Credibility:** P. **Caveat:** the report's author, High Street Consulting Group, is also the consultant that built the WisDOT model. No separate WisDOT publication was found. The $850M is a reduction in *estimating error*, not cash saved.
- **Why it matters for a gas utility:** This is the cleanest public before/after on **cost-estimating accuracy** at a public capital-programme owner. A utility could run the same test by back-testing an ML model against its unit-cost tables on past mains-replacement jobs.

### 4. US DOT Office of Inspector General: machine learning flags bid rigging in highway contracts
- **What they did:** The OIG ran machine learning (and, as a cross-check, a conservative econometric method) over federal-aid highway bid data in six states to detect complementary bidding, where firms submit deliberately losing bids.
- **Result:** At least a third of the contracts analysed were flagged. Flagged contracts cost 5.2–10.2% more than comparable competitive ones, $1.19B in total (2021 dollars).
- **Quotes:** "At least a third of the contracts we analyzed using machine learning in Florida, Georgia, North Carolina, New Jersey, Pennsylvania, and South Carolina were potentially affected by complementary bidding." "We estimated that the costs of flagged contracts ranged from an average of 5.2 percent to 10.2 percent higher ... These estimated cost increases amount to $1.19 billion (in 2021 dollars), or a 6.9 percent cost increase." "Our conservative, econometric method also flagged significant potential complementary bidding in most States we examined, affirming the machine learning results."
- **URL:** https://www.oig.dot.gov/library-item/46639
- **Date:** 2025-02-12
- **Credibility:** M. This is a federal audit and the strongest source in this note. **Caveat:** it measures overpricing the model *detected*, not money recovered. Contracts are "potentially" affected, not proven collusive.
- **Why it matters for a gas utility:** This is the best public evidence for AI in **bid and tender evaluation**, and it fills a gap flagged in note 04 (B2). A utility tendering the same pipeline and station contractors year after year has the bid history to run this kind of screen.

### 5. Indiana DOT: machine learning to bundle capital projects into contracts
- **What they did:** INDOT used an ML platform (from vendor FORO) with its historical and asset data and business rules to choose which projects to bundle into single contracts over several program years. Before this, staff bundled projects by hand, about a year ahead.
- **Before:** the manual bundling baseline. **After:** bundling savings up 40%, and $108M expected over 4 years.
- **Quote:** "A machine-learning platform uses INDOT's historical and asset management data, along with business rules, to automate and optimize bundle selections over multiple program years. This approach has increased bundling savings by 40 percent and is expected to save INDOT $108 million over the next 4 years."
- **URL:** https://www.fhwa.dot.gov/innovation/innovator/issue83/page_04.html (FHWA *Innovator*, Issue 83)
- **Date:** March/April 2021
- **Credibility:** S. Federal agency publication, but the saving is expected (forward-looking), not audited. The LTRC report (item 3, p. 52) adds that bundling time went "from weeks to hours".
- **Why it matters for a gas utility:** Bundling mains-replacement and station work by geography and scope is a common utility capital lever. This is a public example of AI improving how the **work packages** are formed.

### 6. Network Rail + nPlan: ML forecasting of schedule and cost risk
- **What they did:** Network Rail trained nPlan's deep-learning model on past project schedules and used it to forecast risk on two of its largest projects.
- **Before/After:** In a back-test, the model showed savings Network Rail's standard assurance would have missed.
- **Quote:** "Network Rail tested nPlan's risk analysis and assurance solution on two of its largest rail projects ... representing over £3bn of capital expenditure. This exercise showed that by leveraging past data, cost savings of up to £30m could have been achieved on the Great Western Main Line project alone." The rollout plan was 40 projects, then all projects by mid-2021.
- **URL:** https://www.networkrailmediacentre.co.uk/news/network-rail-using-innovative-technology-to-transform-project-planning-and-delivery
- **Date:** 2020-10-06
- **Credibility:** P. The owner published it, but the result is "could have been achieved" on hindsight data, not a realised saving.

**6b. Transpennine Route Upgrade (a Network Rail programme) with nPlan, 2022-11-01**
- **Before:** "only able to perform QSRA on individual projects once per month, and on its whole programme every three to six months." **After:** the team can run the analysis whenever it has an updated schedule.
- Richard Palczynski, Head of Strategic Programme Controls at TRU, is quoted: "Being able to get more frequent analysis done on a larger volume of schedules is a game-changer for us".
- **URL:** https://www.nplan.io/press-releases/nplan-on-track-for-rail-sector-expansion-with-transpennine-route-upgrade-deal
- **Credibility:** V. Vendor press release with a named client quote.
- **Why it matters for a gas utility:** QSRA (quantitative schedule risk analysis) and contingency setting apply to large pipeline and station projects in the same way. Moving from quarterly to on-demand risk forecasts is a realistic target for a utility programme office.

### 7. MassDOT "HEKA": AI assistant for engineering standards
- **What they did:** Northeastern University's AI for Impact programme built HEKA (Highway Engineer Knowledge Agent) for MassDOT. Engineers ask questions in plain language and get answers grounded in MassDOT-approved standards, with citations.
- **Before:** engineers "previously spent weeks navigating dispersed standards, regulations, and policy documents when beginning infrastructure projects." **After:** "78% reduction in manual search time for MassDOT engineers."
- **Quote:** "AI knowledge agent enabling junior engineers to produce designs that meet guidelines faster, and reducing the burden of senior engineers who supervise and mentor. There was a 78% reduction in manual search time for MassDOT engineers (HEKA)." (p. 27; see also p. 18)
- **URL:** https://burnes.northeastern.edu/wp-content/uploads/AI-FOR-IMPACT_-WHAT-WE-HAVE-BUILT-2.pdf
- **Date:** February 2026
- **Credibility:** S. It is reported by the team that built it, and the file is headed "[WORKING]". The measurement method isn't stated. It measures search time, not design hours.
- **Why it matters for a gas utility:** It is a low-risk first use case for an engineering-heavy utility: a cited assistant over gas standards (CSA Z662, internal standards) for junior designers. It is close to the RAG work the team has already shipped.

### 8. Kiewit: in-house design and estimating automation (EPC)
- **What they did:** Kiewit built two tools. KADE (Kiewit Algorithmic Design and Engineering) generates an early-stage 3D model and material quantities from a process diagram, equipment list and site layout, to support the Total Installed Cost estimate. ADAPT automates estimating layouts and earthworks mass-haul planning.
- **Before → After (quotes):**
  - "this job is supposed to last me for eight weeks, but you just completed it in eight minutes."
  - "Before ADAPT, generating even one layout could take days or weeks, making it tough to stay competitive in a four-week bid cycle." Now "layouts that once took days now take about an hour."
  - "To perform a mass flow, we had two people working on it full time for months ... it runs in a matter of minutes to an hour on a big job."
- **URL:** https://www.kiewit.com/newsroom/innovation-from-the-inside-out/
- **Date:** June 2025 (Kieways, Issue 2)
- **Credibility:** S. This is Kiewit's own house magazine with staff quotes. Kiewit's 2026 Tech Summit abstract calls KADE a "deterministic AI solution" that produces a "nearly 30% 3D model". That means rules-based design automation, not machine learning. The examples are anecdotes, not portfolio averages.
- **Why it matters for a gas utility:** Kiewit is a major pipeline and station EPC contractor. If contractors can produce concept design and quantities in minutes, the owner's estimators need matching capability to challenge their bids.

---

## Checked and dropped

| Candidate | Why dropped |
|---|---|
| Michigan DOT SPR-1743 (ML cost estimation) | The PDF returns 403 to every automated request, so the figures couldn't be confirmed |
| Caltrans ML estimate correction (median error 15% vs 18%) | The only source is a personal Substack, not Caltrans |
| National Grid + Sensat ("weeks pared from surveying") | No before/after figure on the National Grid page |
| UK Power Networks HV Auto Quote / VisNet (8 hrs → 15 min) | Rules-based digital automation, not described as AI; the VisNet figure comes from a vendor product sheet |
| Montana DOT neural-network contract-time tool | Deployed, but no before/after figure published |
| Enbridge "$500K/yr, weeks of engineering" | Couldn't trace it to any primary page |
| Dominion "45% engineering time" | Only found on an aggregator; no primary source |
| Avangrid First Time Right (GenAI) | Covers wind O&M troubleshooting, not capital delivery, and the release has no figures |
| AECOM–Consigli "up to 90% engineering time" | A vendor claim, and no AECOM primary page was found |

## What this adds for the deck

1. **Bid evaluation now has a credible source.** The US DOT OIG audit (item 4) is a federal audit showing machine learning finding 5–10% overpricing in public infrastructure tenders. Use it with note 04's "no utility precedent" caveat: the method is proven on highways, not yet on utility tenders.
2. **For cost-estimating accuracy, use WisDOT (30% lower MAPE) next to Exponent (Class 5 → Class 3).** Both are pilots or back-tests. Say so, and present a back-test on the company's own data as the obvious first step.
3. **Utility peer evidence is about speed, not dollars.** Duke (2 weeks → hours) and SPEN (hours → seconds) both come from vendor co-announcements. I still found no public, audited AI capital-cost saving at a gas or electric utility.
4. **The Canadian and gas-specific gap is still open.** Searches of Enbridge, TC Energy, ATCO, FortisBC, Hydro One, BC Hydro, OPG, SoCalGas/Sempra, Cadent, SGN and NGN (including Ofgem NIA reports) found no quantified AI result for estimating, design or procurement. Their published AI work is on leaks, pressure management, customer service and field operations.

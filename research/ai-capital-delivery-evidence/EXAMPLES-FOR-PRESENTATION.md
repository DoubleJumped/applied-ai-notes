# AI before-and-after examples: capital projects, estimating, procurement

Examples with sources to back the numbers in a leadership presentation. Pick the ones that fit. Every link was opened and the quoted figure found on the page on 2026-09-23, except the three marked **Check before use** (those sites block automated readers or are paywalled, so open them yourself first).

**Evidence labels**
- **Audited:** checked by an independent public body.
- **Measured:** the organisation reports an actual result.
- **Pilot:** a trial or back-test, not yet in routine use.
- **Target:** a goal or projection, not a result.
- **Vendor:** a vendor's own announcement, even where a named client is quoted.

---

## Rundown (pick and choose)

### Government of Alberta

1. **PRISM: Alberta's capital-project systems.** Alberta Infrastructure turned down a vendor quote of about $54M for one of its two systems for managing buildings and capital construction projects. An in-house team using AI built both: $858K spent at 10 months, with about $2.64M estimated to finish. This is the best one-to-one link to us because the software runs a capital construction programme. *Measured, reported by the Minister himself, unaudited.*
2. **Classroom portal (ACIP): $108K in 11 weeks.** The traditional estimate was $1.3M–$1.9M and 12–18 months. This is the cleanest before-and-after in the white papers. *Actual cost measured; the "before" is their own estimate.*
3. **Heating allowance app: 5 months → 4 days.** An app first written by hand in the early 2000s was rebuilt with AI in 4 days, with new features added. *Prototype.*
4. **466 million lines of code reviewed in about 20 hours for under $2,000.** AI agents read Alberta's entire code estate, work that would otherwise be a consultant engagement. *Measured, AI usage cost only.*
5. **Procurement redesign.** Alberta is changing how it buys IT. It publishes the scope as data, requires bids in a structured form, and uses AI to compare bids side by side. Its goal is bids that take "hours instead of weeks" to prepare, and it expects the next $100M–$200M of IT procurement to follow this model. *Target.*
6. **Programme scale: a 95% target.** Alberta faces a $2B+ modernization backlog that would take more than a century the traditional way. It is targeting a 95% cut in time and cost, and plans to replace 185 old systems with 16 new ones. *Target, not a result. Say "targeting".*
7. **What the AI actually costs them, and the controls around it.** They spend "tens of thousands of dollars a month" on AI. Every AI call goes through a gateway that enforces spending budgets, and they deliberately use more than one AI vendor. *Measured spend; the savings side is a target.*
8. **Independent read.** Andrew Lewis, writing independently, says the 95% and 20x figures are "targets at least as much as they are settled results". He finds the smaller numbers (items 2–4) "concrete and consistent". Worth having in the back pocket if challenged.

### Capital cost estimating

9. **Wisconsin DOT: 30% less estimating error.** A machine-learning cost model replaced the old cost lookup tables for pavement projects. That is about $850M less estimating error across the 10-year programme. *Pilot, reported by the consultant who built it.*
10. **Exponent utility pilot: Class 5 → Class 3 estimates.** A utility's early-stage estimates improved from AACE Class 5 (−50% to +100%) to Class 3 (−20% to +30%) before detailed design, using a model built on five variables. *Pilot; Exponent sells this service.*
11. **Kiewit: 8 weeks → 8 minutes.** This major pipeline and station contractor now generates early-stage 3D models and quantities for its cost estimates automatically. Estimating layouts dropped from days to about an hour. The contractors bidding to us are getting faster at estimating. *Company's own magazine; rules-based automation, not machine learning.*
12. **SP Energy Networks: connection design and cost estimate in under 5 seconds.** This Scottish network utility generates connection route options with cost estimates. Previously that took hours of engineering, and several weeks end to end. *Vendor, utility named.*

### Bid evaluation and procurement

13. **US DOT Inspector General: machine learning flagged overpriced highway bids.** In six states, at least a third of contracts showed signs of bid rigging. Flagged contracts cost 5.2–10.2% more, about $1.19B in total. This is the strongest source in the set. *Audited (federal audit).*
14. **Indiana DOT: 40% more savings from bundling projects into contracts.** Machine learning chooses which projects to bundle into single contracts, with $108M in savings expected over 4 years. *Measured, reported by FHWA; the savings are forward-looking.*
15. **Realistic procurement savings are 1–3% of spend.** Walmart's automated supplier negotiations saved 1.5–3%. That is a useful sanity check against bigger consultant claims. *Measured, but the case study is paywalled. Check before use.*
16. **Gartner counterweight.** In July 2025, Gartner said generative AI for procurement had entered the "trough of disillusionment". Citing it shows the pitch is balanced. *Analyst view. Check before use.*

### Engineering, schedule and field productivity

17. **Duke Energy: 2 weeks → hours.** AI agents prepare data for grid-upgrade engineering studies. A named Duke executive is quoted. *Vendor.*
18. **Network Rail: up to £30M on one project.** A machine-learning model of schedule and cost risk was tested on £3bn of past capital spend. Another Network Rail programme now runs schedule risk analysis on demand instead of monthly or quarterly. *Back-test (Pilot) and Vendor.*
19. **MassDOT: 78% less time searching engineering standards.** An AI assistant answers engineers' questions from approved standards, with citations. It is the closest match to what we already build (search over standards like CSA Z662). *Reported by the team that built it.*
20. **NiSource: over 20% field productivity.** A US gas utility peer reports this from AI work management, and is now extending AI into supply chain. *Reported to investors on an earnings call.*
21. **McKinsey × ALICE: up to 20% faster construction schedules** across 35+ clients. On one project, 15% faster saved $20M in labour. *Vendor partnership. Check before use.*

### Context

22. **The size of the prize: only 8.5% of big projects finish on time and on budget** (Flyvbjerg, 16,000+ projects). That is why estimating and schedule-risk work pays off.

---

## Detail and links

### Government of Alberta

#### 1. PRISM: Alberta Infrastructure's capital-project systems
- **What it is:** PRISM Core tracks about 4,000 government buildings worth about $12B. PRISM Project manages budgets and timelines for 500+ active capital construction projects, replacing spreadsheets and SharePoint sites.
- **Before:** a vendor proposal with $19M of upfront costs, "the total bill would land around $54 million" over four years, and it covered only one of the two systems.
- **After:** "Ten months in, the team has spent $858,000", and the "estimated total cost to fully deliver both systems is approximately $2.64 million". The budget was $5M. Both systems are live with 643 users.
- **Worth quoting:** "AI did not build these systems by itself... What AI did was make them dramatically faster."
- **Caveat:** this is the Minister's own write-up, not audited, and not in the white papers. Press versions differ: BetaKit says $54M over three years and $2.5M.
- **Sources:**
  - Minister Nate Glubish's Substack, 2026-04-06: https://nateglubish.substack.com/p/they-said-it-would-cost-54-million
  - BetaKit, 2026-07-28: https://betakit.com/albertas-ai-push-is-rewriting-the-rules-for-government-contractors/

#### 2. Alberta Classroom Information Portal (ACIP)
- **Before:** estimated at $1.3M–$1.9M and about 12–18 months with a traditional product team.
- **After:** "ACIP was delivered in eleven weeks using factory methods at a cost of approximately $108,000."
- **Caveat:** the traditional figure is Alberta's own estimate, with no method shown. The $108K doesn't say whether it includes the cost of building the AI tooling.
- **Source:** Velocity White Papers, "AI Factory Case Study: From Five Months to Four Days": https://thevelocitywhitepapers.com/paper/rhx4t/

#### 3. Remote Area Heating Allowance app
- **Before:** "took five months to build by hand in the early 2000s."
- **After:** rebuilt "with added public-facing functionality through the AI factory" in four days.
- **Caveat:** a prototype. The five-month baseline is the author's own build from about 25 years ago.
- **Source:** same paper: https://thevelocitywhitepapers.com/paper/rhx4t/

#### 4. Git Insights: the whole code estate read by AI
- **Before:** understanding the estate would normally be a large consultant engagement (no figure given).
- **After:** 466 million lines of code across 3,400 repositories were reviewed in about 20 hours, for under $2,000 of AI usage.
- **Caveat:** the $2,000 covers AI usage only, not staff time or setup (Digital Journal makes this point).
- **Sources:**
  - Government of Alberta release, 2026-07-06: https://www.alberta.ca/announcements.cfm?xID=96456379DDC57-9F6B-FE7E-69C325AD64A91DCD
  - Paper: https://thevelocitywhitepapers.com/paper/bbkac/

#### 5. Procurement redesign ("Taking the Hill")
- **Before:** bids "run hundreds to thousands of pages long" and must be legally reviewed page by page. That adds months, so procurements are written narrowly to limit the number of bidders.
- **After:**
  - Alberta publishes the scope as data.
  - Every bid must include a "machine-readable crosswalk" linking each section to the scope it addresses.
  - "An AI reviewer can then shred the entire package and extract the structured fields for cost, capability coverage, evidence citations, local support capacity, and risk."
  - Goal: "submitting a successful bid should take hours instead of weeks."
- **Scale:** "the next one hundred to two hundred million dollars of procurement in this space" will follow this model.
- **What transfers to us:**
  1. Build our own independent estimate from counted scope.
  2. Make bids line up against the same scope.
  3. Use AI to compare them side by side.
  This works for IT procurement today, and as a method for capital RFPs.
- **Caveat:** these are targets. The paper publishes no before-and-after results yet.
- **Source:** https://thevelocitywhitepapers.com/paper/m66qi/

#### 6. Programme scale and the 95% target
- **Before:** the traditional modernization bill is about $2B and would take more than a century.
- **After (target):** "95 per cent reduction in time and cost targeted", work up to 20 times faster, and 185 aging systems replaced by 16 modern applications. More than 2,000 public servants have been trained since September 2025.
- **Caveat:** always say "targeting". These are not results.
- **Sources:**
  - Release: https://www.alberta.ca/announcements.cfm?xID=96456379DDC57-9F6B-FE7E-69C325AD64A91DCD
  - Paper: https://thevelocitywhitepapers.com/paper/cux4h/

#### 7. What AI costs Alberta, and its governance
- **Spend:** "tens of thousands of dollars a month" now, and "hundreds of thousands" expected at scale. The target is "hundreds of millions a year in cost avoidance" with staffing held steady.
- **Controls:**
  - an AI gateway that enforces per-workload and daily budgets
  - blocks on personal data going to the wrong model
  - more than one AI vendor, to avoid lock-in
  - agent access that expires within hours
  - an expectation that 7–10% of AI-built work will need rework
- **Source:** "The Agentic Technology Stack": https://thevelocitywhitepapers.com/paper/qxlzo/

#### 8. Independent read of Alberta's claims
- Andrew Lewis, 2026-07-14: "The largest claims, the ninety-five percent and the twentyfold, are targets at least as much as they are settled results." He calls items 2–4 "concrete and consistent, and the method is the point."
- **Source:** https://andrewlewis.ca/p/what-a-government-proved-about-ai

### Capital cost estimating

#### 9. Wisconsin DOT: machine-learning cost estimating
- **Before:** cost estimates for pavement projects came from lookup tables.
- **After:** "Compared to WisDOT's previous cost estimation tables, the new model achieved a 30% reduction in mean absolute percent error, equating to an estimated $850 million reduction in error across WisDOT's 10-year program."
- **Caveat:** the $850M is less estimating *error*, not cash saved. The report's author also built the model.
- **Source:** Louisiana DOTD / FHWA report, *Artificial Intelligence and Its Role and Use Within State DOTs*, January 2026, page 46: https://www.ltrc.la.gov/pdf/2026/FR_722.pdf
- **For us:** this is the model for a first pilot. Back-test a model against our own unit-cost tables on past mains-replacement jobs.

#### 10. Exponent: early-stage estimates on utility projects
- **Before:** AACE Class 5 accuracy (−50% to +100%) at the concept stage.
- **After:** "Our model was able to progress from early conceptual estimates toward the Class 3 Expected Accuracy Range, often achieving levels within -20% to +30% well before detailed designs were available." Five key variables were enough for a predictive model.
- **Caveat:** a single pilot with the utility unnamed, and Exponent sells this work.
- **Source:** Exponent, 2025-12-12: https://www.exponent.com/article/improving-early-stage-cost-estimates-utility-projects

#### 11. Kiewit: design and estimating automation (pipeline and station contractor)
- **Before → after:**
  - An early-stage 3D model: "this job is supposed to last me for eight weeks, but you just completed it in eight minutes."
  - Layouts: "Before ADAPT, generating even one layout could take days or weeks". Now "layouts that once took days now take about an hour."
  - Earthworks planning: two people full time for months, now "a matter of minutes to an hour".
- **Caveat:** anecdotes from the company's own magazine. The tool is rules-based automation, not machine learning.
- **Source:** Kiewit, June 2025: https://www.kiewit.com/newsroom/innovation-from-the-inside-out/
- **For us:** contractors can now price and design faster than we can check them. We need matching estimating capability to challenge their bids.

#### 12. SP Energy Networks + Keen AI: connection options with cost estimates
- **Before:** "hours" of manual engineering analysis for each assessment, and "several weeks" to respond to a developer.
- **After:** connection routes, estimated costs, power flows and constraints "in less than five seconds".
- **Caveat:** a joint utility and vendor announcement.
- **Sources:**
  - Solar Power Portal, 2026-05-06: https://www.solarpowerportal.co.uk/solar-projects/sp-energy-keen-ai-announce-ai-powered-grid-connection-tool
  - New Power: https://www.newpower.info/2026/05/ai-speeds-up-optioneering-for-new-connections-to-spen-network/
- **For us:** the closest match to gas customer-connection and main-extension estimates.

### Bid evaluation and procurement

#### 13. US DOT Office of Inspector General: machine-learning bid screening
- **Finding:** "At least a third of the contracts we analyzed using machine learning in Florida, Georgia, North Carolina, New Jersey, Pennsylvania, and South Carolina were potentially affected by complementary bidding." (Complementary bidding is when firms submit deliberately losing bids.)
- **Cost:** flagged contracts cost "an average of 5.2 percent to 10.2 percent higher"; "these estimated cost increases amount to $1.19 billion (in 2021 dollars)".
- **Caveat:** this is overpricing the model detected, not money recovered, and the contracts are "potentially" affected.
- **Source:** Audit EC2025019, 2025-02-12: https://www.oig.dot.gov/library-item/46639
- **For us:** we tender with a repeat pool of pipeline and station contractors, so we have the bid history to run this kind of screen.

#### 14. Indiana DOT: machine learning for bundling projects into contracts
- **Before:** staff bundled projects into contracts by hand, about a year ahead.
- **After:** "This approach has increased bundling savings by 40 percent and is expected to save INDOT $108 million over the next 4 years." The Louisiana report also notes bundling time went from weeks to hours.
- **Source:** FHWA *Innovator*, Issue 83, March/April 2021: https://www.fhwa.dot.gov/innovation/innovator/issue83/page_04.html
- **For us:** bundling mains-replacement and station work into contracts is the same decision.

#### 15. Walmart: automated supplier negotiations
- **Check before use.** The HBR page is a paywalled product listing, so these figures come from secondary reporting of the case.
- **Result:** the pilot started in Canada and reached agreements with 64% of suppliers at 1.5% average savings. At scale, 68% of negotiations closed at an average of 3% savings. This covers low-value, long-tail supplier spend.
- **Source:** Harvard Business Review case (paywalled product page): https://store.hbr.org/product/how-walmart-automated-supplier-negotiations/H07CG1
- **Use it as:** the realistic range for procurement savings (low single digits of spend).

#### 16. Gartner: GenAI for procurement "in the trough of disillusionment"
- **Check before use.** The site blocks automated access, so the quote below comes from a search excerpt.
- **Quote:** GenAI for procurement "has entered the trough of disillusionment", and many see "uneven ROI or falling short of expectations".
- **Source:** 2025-07-30: https://www.gartner.com/en/newsroom/press-releases/2025-07-30-gartner-says-generative-ai-for-procurement-has-entered-the-trough-of-disillusionment

### Engineering, schedule and field productivity

#### 17. Duke Energy + AWS: grid-upgrade engineering studies
- **Before → after:** "data preparation tasks go from two weeks of manual work to hours."
- **Caveat:** AWS's press release, although a Duke executive is quoted. It covers the data-prep step only.
- **Source:** 2026-09-17: https://press.aboutamazon.com/aws/2026/9/aws-launches-agentic-grid-planning-program-to-accelerate-interconnection-studies

#### 18. Network Rail + nPlan: schedule and cost risk forecasting
- **Back-test:** tested on two projects representing over £3bn of capital spend. "Cost savings of up to £30m could have been achieved on the Great Western Main Line project alone."
- **Transpennine Route Upgrade (a Network Rail programme):**
  - Before: schedule risk analysis only "once per month" per project, and every three to six months for the whole programme.
  - After: run whenever the schedule updates.
- **Caveat:** "could have been" is a hindsight test. The Transpennine result is from a vendor release.
- **Sources:**
  - Network Rail, 2020-10-06: https://www.networkrailmediacentre.co.uk/news/network-rail-using-innovative-technology-to-transform-project-planning-and-delivery
  - nPlan, 2022-11-01: https://www.nplan.io/press-releases/nplan-on-track-for-rail-sector-expansion-with-transpennine-route-upgrade-deal

#### 19. MassDOT HEKA: engineering standards assistant
- **Before:** engineers "previously spent weeks navigating dispersed standards, regulations, and policy documents".
- **After:** "a 78% reduction in manual search time for MassDOT engineers."
- **Caveat:** reported by the team that built it, and the document is marked "[WORKING]".
- **Source:** Northeastern University, February 2026, pages 18 and 27: https://burnes.northeastern.edu/wp-content/uploads/AI-FOR-IMPACT_-WHAT-WE-HAVE-BUILT-2.pdf
- **For us:** closest to what our team already builds.

#### 20. NiSource: AI work management at a gas utility
- **Quote:** "Our AI work management intelligence continues to deliver sustained field productivity uplifts of over 20%", measured through "work hours achieved, less idle time, and less rework". The company is also "expanding AI into additional high-value areas including a new supply chain program".
- **Caveat:** reported to investors, not audited. It covers field work execution, not estimating.
- **Source:** Q3 2025 earnings call, 2025-10-29: https://finance.yahoo.com/news/nisource-ni-q3-2025-earnings-163645691.html

#### 21. McKinsey × ALICE Technologies: generative scheduling
- **Check before use.** The page timed out for automated access.
- **Claim:** schedule accelerations "of up to 20 percent" across 35+ clients. One project's "15 percent schedule acceleration ... led to a $20 million reduction in labor costs".
- **Caveat:** a vendor partnership, and "up to" figures.
- **Source:** https://www.mckinsey.com/capabilities/operations/our-insights/operations-blog/mckinsey-and-alice-technologies-collaborate-to-transform-capital-project-delivery-with-generative-scheduling

### Context

#### 22. The baseline problem
- "only 8.5 percent are on-budget and on-time and ... only 0.5 percent are on-budget, on-time, and deliver the promised benefits", from Flyvbjerg's database of more than 16,000 big projects.
- **Source:** review of *How Big Things Get Done* (Flyvbjerg & Gardner, 2023): https://www.independent.org/tir/2023-fall/how-big-things-get-done/

---

## Things to keep in mind when presenting

- **Don't put Alberta's 95% next to our capital budget.** It describes building software, not building pipe. The honest bridge is PRISM: AI cut the cost of the *systems that run* a capital programme, not the cost of construction.
- **No public, audited case exists yet of a gas or electric utility using AI for capital estimating or bid evaluation.** We searched Enbridge, TC Energy, ATCO, FortisBC, Hydro One, SoCalGas and the UK gas networks. The proven examples come from transportation agencies and contractors. That makes it an opportunity to lead, but say it plainly.
- **Numbers to avoid:** "WEF: AI cuts project costs 20% and time 15%" and "40–60% capex savings". Both circulate widely, but neither traces to a primary source.
- **A credible first step:** back-test an estimating model on our own historical project costs, following Wisconsin DOT and Exponent, and screen past tenders for bid patterns, following the US DOT audit. Both use data we already have, and both produce a before-and-after number of our own.

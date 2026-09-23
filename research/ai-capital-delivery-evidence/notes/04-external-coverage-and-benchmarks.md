# 04 — External coverage of Velocity + complementary benchmarks

Researched 2026-09-23. Quotes are verbatim as returned by the source page or its search snippet. Where a page blocked direct fetch (Digital Journal, McKinsey, Gartner, WEF all returned 403 or timed out), the quote comes from a search-engine excerpt and is marked **(snippet)**. Re-check those against the live page before putting them on a slide.

---

## Part A — External coverage of Velocity

### A1. Official statements

**Government of Alberta news release, "Alberta sets North American standard for AI"** (July 6, 2026)
URL: https://www.alberta.ca/announcements.cfm?xID=96456379DDC57-9F6B-FE7E-69C325AD64A91DCD

What the release claims, and how it hedges:
- It says it is **targeting** a 95 per cent reduction in time and cost against traditional modernization, which it estimates at "roughly $2 billion" and "over a century" to finish.
- "AI agents have demonstrated the potential of speeding up work by as much as 20 times while reducing the time to modernize critical systems by as much as 95 per cent." (quoted in Taproot and the Black Press syndication)
- It reports 466 million lines of code reviewed in about 20 hours.
- One ministry is replacing 185 aging systems with 16 modern applications.
- Systems blocked an average of 189 million connection attempts a day in 2024-25.
- It announced 21 open-source papers. BetaKit and Ponoka say 22, and the site's count has changed over time.
- The Alberta AI Academy has trained more than 2,000 public servants and reached more than 15,000 Canadians.

Quotes:
- Nate Glubish, Minister of Technology and Innovation: "Alberta spent decades building technology that worked for government. Now we are rebuilding it to work better for Albertans and doing it faster and for far less."
- Glubish: "Alberta is not waiting to solve this problem. We are solving it, and we are showing others how."
- Glubish (per HRD): "Every government is stuck with the same aging systems we were."
- Brian Peters, Anthropic Head of North American Government Affairs: "Alberta's approach is remarkably innovative – it used Claude to deliver real results at scale, building more secure systems that cost taxpayers less."
- Farsad Nasseri, Google Cloud Canada: "Alberta is emerging as the North Star in Canada's government transformation."

**Minister's Substack, "They Said It Would Cost $54 Million. We Said 'No Thanks.'"** (Nate Glubish, April 6, 2026). This is the primary source for the $54M story.
URL: https://nateglubish.substack.com/p/they-said-it-would-cost-54-million

This is the most useful item for the capital delivery angle, because the systems are Alberta Infrastructure's own tools. PRISM Core tracks about 4,000 government buildings worth about $12B. PRISM Project manages construction budgets and timelines for 500+ active capital projects.
- "the total bill would land around $54 million" and "the $54 million only covered one of the two systems." The vendor timeline was 4 years.
- "PRISM Project replaces the spreadsheets and SharePoint sites used to manage capital construction."
- "Ten months in, the team has spent $858,000."
- "the estimated total cost to fully deliver both systems is approximately $2.64 million." The budget was $5M.
- The team was 24 people: 8 from Technology and Innovation and 16 from Infrastructure. The systems have 643 active users.
- Deputy ministers "killed the procurement". The post concedes the vendor bids were reasonable given how the work had been scoped.
- Caveat in the minister's own words: "AI did not build these systems by itself. Cohen's team members are experienced practitioners who know how to design and deliver digital products."

**Anthropic customer story, "Alberta uses Claude to find and fix security vulnerabilities"** (July 6, 2026). This is vendor-published.
URL: https://www.anthropic.com/news/alberta-government-claude-cybersecurity
- 466M lines, 20 hours, 50 parallel agents, 3,400 repos, 1,280 apps, and about 95 controls per app. A traditional review is estimated at 6.5 years.
- Glubish: "By using AI to find and fix vulnerabilities across our systems, we accomplished in hours what would have taken a traditional approach years to complete."
- Several outlets cite a compute cost of about $2,000 for the scan, attributing it to this case study.

**Glubish on procurement, from BetaKit (July 28, 2026, at the Velocity Symposium)**
- "We've had examples in-house where we've built things for 95 percent cheaper and in 95 percent less time."
- "Anybody who's stuck in the old ways and doesn't want to change—you're probably not going to do much work with us anymore."
- BetaKit paraphrases him saying that "the traditional time and materials billing system is out of date."

**Glubish, The Logic (July 10, 2026):** "We have built an entire army of AI agents." On the Infrastructure systems: "They were doing it on Excel, and it was not scalable."

**Glubish at the symposium, Taproot (Aug 11, 2026):** "That's the transformative power of AI. That's why we want to be the most AI-native government in North America."

### A2. Press coverage table

| Date | Outlet / author | Headline | Figures cited | Tone / notes | URL |
|---|---|---|---|---|---|
| 2026-07-06 | Black Press (Kevin Sabo), syndicated to Ponoka News, Rimbey Review, Sylvan Lake News, Lacombe Express, Pipestone Flyer, Stettler Independent | "Alberta uses AI to overhaul aging public service tech, saving billions" | $2B traditional estimate; "95 per cent cost savings" expected; 466M lines / ~20 hrs; 20x; 185→16 | Rewritten from the release. No critique. The byline is Black Press, not Canadian Press. The "saving billions" headline goes beyond the release, which speaks of a **target** | https://ponokanews.com/2026/07/06/alberta-uses-ai-to-overhaul-aging-public-service-tech-saving-billions/ |
| 2026-07-07 | BetaKit (Jesse Cole) | "Alberta is open-sourcing its AI playbook for government" | 466M lines / 20 hrs; human-led review "upwards of $2 billion" and 6+ years; "as much as a ninety-five percent reduction in time and cost" | Favourable. Quotes Cole Cioran (Info-Tech): "The Velocity Papers are the first defensible in-production blueprint for an agentic public service." | https://betakit.com/alberta-is-open-sourcing-its-ai-playbook-for-government/ |
| 2026-07-07 | Human Resources Director (HRD) | "Alberta plans to replace 185 aging systems with AI-built applications" | 185→16; $2B / 100+ yrs; 95%; 2,000+ trained | Flags a gap: "The province did not say when remaining replacements will be complete, nor how many jobs, if any, may be affected." Cioran: "A resource-constrained government reached the same order-of-magnitude gain in software delivery that the world's best-funded technology companies achieve." | https://www.hcamag.com/ca/specialization/transformation/alberta-plans-to-replace-185-aging-systems-with-ai-built-applications/581547 |
| 2026-07-07 | Medicine Hat News; Lethbridge News Now / CHAT / EverythingGP (Pattison) | "Province boasting achievements in AI for government tech" / "Province uses AI tools to rebuild decades-old technology" | Same as the release | Release rewrite | https://medicinehatnews.com/news/local-news/2026/07/07/province-boasting-achievements-in-ai-for-government-tech/ |
| 2026-07-10 | The Logic | "Alberta wants to be a model for government AI and power Canada-wide adoption" | $2B / 100 yrs → 5% cost / 4 yrs; **$2.5M build vs $52M quote** (other outlets say $54M) | Minimal skepticism. Ties the story to data-centre and "compute capital" ambitions | https://thelogic.co/news/alberta-ai-model-government-adoption/ |
| 2026-07-14 | andrewlewis.ca (Andrew Lewis) | "What a Government Proved About AI That Vendors Wouldn't" | Classroom portal: 11 wks, ~$108K vs $1.3–1.9M estimate; benefits app 4 days vs 5 months; 466M lines for under $2,000 | **The most useful measured critique.** "The results Alberta is reporting did not come from the AI. They came from the operations the province built around it. And the operations are the one thing a vendor cannot sell you." He calls the documents "self-published papers" and says the 95% and 20x figures are "targets at least as much as they are settled results." Also: "AI without operations is just a demo." | https://andrewlewis.ca/p/what-a-government-proved-about-ai |
| 2026-07-15 | Culture Alberta | "Alberta Is Using AI to Rebuild $2 Billion Worth of Government Software, and Quebec Just Signed On to Copy It" | $2B; 95%; $2.5M Infrastructure system | Covers the Alberta–Quebec knowledge-sharing MOU (5 years, no money, 60-day exit). Notes the savings are **unaudited**, the work is incomplete, and the evidence comes mainly from the province and the vendor | https://www.culturealberta.com/articles/alberta-is-using-ai-to-rebuild-2-billion-worth-of-government-software-and-quebec-just-signed-on-to-c |
| 2026-07-28 | BetaKit (Jesse Cole) | "Alberta's AI push is rewriting the rules for government contractors" | 95% cheaper / 95% faster; $54M lowest bid over 3 yrs vs $2.5M in under a year | Procurement angle: time-and-materials billing "out of date". No critique | https://betakit.com/albertas-ai-push-is-rewriting-the-rules-for-government-contractors/ |
| 2026-07 (n.d.) | Digital Journal | "What Alberta's AI numbers mean for IT pricing" | ~$2,000 compute for the 466M-line scan; $2B / century; 739 repos flagged as consolidation candidates | **Measured critique (snippet):** the $2,000 figure "doesn't include the people, systems, and preparation required to build the scanning process." "A vendor quoting three years and eight figures now has to show which parts of the work still require that much time and labour." Also: an estimate "is easier to defend when it separates automated tasks from work that still needs experienced people." | https://www.digitaljournal.com/article/what-albertas-ai-numbers-mean-for-it-pricing/ |
| 2026-08-11 | Taproot Edmonton | "Province showcases AI approach at symposium" | 100 in person / 600 virtual; AltaML claims 97% accuracy; a task done in 2 min vs an estimated 15 months | Event recap | https://edmonton.taproot.news/briefs/2026/08/11/province-showcases-ai-approach-at-symposium |

Other items: a companion Digital Journal piece, "What Alberta found when it pointed 50 agents at its own code" (https://www.digitaljournal.com/article/what-alberta-found-when-it-pointed-50-agents-at-its-own-code/, fetch blocked). Securitybrief.ca and dig.watch repeat the Anthropic case study.

### A3. Critiques, pushback, verification concerns

1. **The claims are not independently verified.** Culture Alberta says the savings are unaudited. A secondary summary notes the public details "come mainly from Anthropic and Alberta-facing communications, not from a full independent audit of the findings, severity mix, false-positive rate, remediation quality, or long-term incident outcomes." I found no Auditor General review and no third-party evaluation.
2. **Much of it is target, not result.** The release's 95% is a target ("targeting", "as much as", "potential"). The Black Press headline "saving billions" overstates it. Andrew Lewis calls 95% and 20x "targets at least as much as they are settled results."
3. **Sources disagree on the $54M case.** Reported figures include $54M over 4 years (Substack), $54M over 3 years (BetaKit), and $52M (The Logic). The build cost appears as $2.5M in most outlets, but the Substack estimate is $2.64M, with $858K actually spent at 10 months. The $54M covered **one** of the two systems, which flatters the comparison further, but it is still a vendor quote, not a completed vendor delivery. Use $54M vs ~$2.64M estimated, with $858K spent at 10 months, and cite the Substack.
4. **The $2,000 compute figure leaves out the setup work.** Digital Journal notes it excludes the people, systems and preparation behind the scan.
5. **The operating model matters more than the tool.** The minister says "AI did not build these systems by itself." Lewis says the operating model is what cannot be bought. Both undercut a "buy AI, save 95%" message.
6. **Workforce and timeline questions are open.** HRD: no date for the remaining replacements, and no statement on job impact.
7. **Political context.** Critical coverage in CBC and the Globe (Aug 2026) is about AI **data centres** (power bills, town-hall jeering, NDP calls for a pause), not about Velocity's claims. I found no substantive published rebuttal of the Velocity numbers themselves.
8. **Promotional sources.** Supportive quotes come from vendors (Anthropic, Google Cloud) and an advisory firm (Info-Tech). Treat them as endorsements, not evidence.

---

## Part B — Complementary benchmarks for procurement and capital delivery

Credibility key: **M** = measured outcome at a named organisation; **C** = consultant estimate or client anecdote (unnamed client, not audited); **S** = survey (self-reported); **V** = vendor marketing or vendor-co-branded; **A** = academic or peer-reviewed.

### B1. Procurement savings

| Figure | Exact quote | Source / date | URL | Cred. |
|---|---|---|---|---|
| 15–45% cost reduction; up to 30% of work removed | "procurement functions that use AI can reduce overall costs by roughly 15% to 45%" (snippet adds "depending on the category"); AI can "eliminate up to 30% of the work for employees and teams" | BCG, "GenAI in Procurement: From Buzz to Bottom-Line Cost Reductions", Schnellbächer, Vigen, Oleynikova, 2025-04-18 | https://www.bcg.com/publications/2025/from-buzz-to-bottom-line-cost-reductions-using-genai | C. This is category-level potential, not a total-spend result |
| Value comes 10/20/70 from algorithms / platforms / people | "10% comes from the algorithms themselves and 20% from the data and technology platforms. The remaining 70% comes from people's motivation" | BCG, same | same | C. A useful framing that lines up with Alberta's "operations, not AI" point |
| 25–40% procurement efficiency | agentic AI "could result in the procurement function being 25 to 40 percent more efficient" (snippet) | McKinsey, "Redefining procurement performance in the era of agentic AI", 2026-02-05 | https://www.mckinsey.com/capabilities/operations/our-insights/redefining-procurement-performance-in-the-era-of-agentic-ai | C. Measures efficiency (effort), not spend savings |
| 12–20% and 20–29% savings on services categories | a tech company's linked AI agents found "savings opportunities of 12 to 20 percent in its contact center operations, and 20 to 29 percent in business process outsourcing (BPO) and financial services spend" (snippet) | McKinsey, same | same | C. Unnamed client; "opportunities", not banked savings |
| +1–3% value capture from autonomous sourcing | chemicals company pilot: staff efficiency "20 to 30 percent", value capture "1 to 3 percent" (snippet) | McKinsey, same | same | C. The most realistic number here: low single digits of spend |
| 10–15% from AI-guided negotiation | "AI-guided negotiations led to 10 to 15 percent savings across vendors" (snippet) | McKinsey, "Mitigating procurement value leakage with generative AI", 2025-04-09 | https://www.mckinsey.com/capabilities/operations/our-insights/mitigating-procurement-value-leakage-with-generative-ai | C |
| 4% less value leakage | a pharma company's AI agents enforcing invoice-to-contract compliance cut leakage "by 4 percent" (snippet) | McKinsey, same | same | C. Relevant to contractor invoice compliance on capital projects |
| 13% on raw materials from should-cost modelling | a specialty chemicals company "saved 13 percent in raw-materials spending" (snippet) | McKinsey, "Revolutionizing procurement: Leveraging data and AI..." | https://www.mckinsey.com/capabilities/operations/our-insights/revolutionizing-procurement-leveraging-data-and-ai-for-strategic-advantage | C |
| 1.5% → 3% average savings, 64–68% supplier agreement | Walmart pilot (started in **Canada**): agreements with 64% of suppliers at 1.5% average savings; at scale, 68% closed at an average of 3% savings | Walmart / Pactum, reported via HBR "How Walmart Automated Supplier Negotiations" (2022) | https://store.hbr.org/product/how-walmart-automated-supplier-negotiations/H07CG1 | M/V. A named buyer, but the numbers come through the vendor. Tail spend only |
| GenAI in "trough of disillusionment" | GenAI for procurement "has entered the trough of disillusionment"; many see "uneven ROI or falling short of expectations" (snippet) | Gartner press release, 2025-07-30 | https://www.gartner.com/en/newsroom/press-releases/2025-07-30-gartner-says-generative-ai-for-procurement-has-entered-the-trough-of-disillusionment | Analyst view. **Use as the counterweight** |
| 74% say data not AI-ready | "74% of procurement leaders say their data isn't AI-ready" (snippet, attributed to Gartner via secondary) | secondary | https://www.scmr.com/article/gen-ai-in-procurement | S. Verify before using |
| Digital leaders beat plan on savings | "Cost savings (96% exceeded/met plan vs. 80% of followers)" | Deloitte, 2025 Global CPO Survey | https://www.deloitte.com/us/en/services/consulting/articles/2025-global-chief-procurement-officer-survey.html | S. Correlation only |

### B2. Bid evaluation, should-cost and vendor bid analysis

| Figure | Exact quote | Source / date | URL | Cred. |
|---|---|---|---|---|
| ~50% productivity on offer analysis and tender assistance; ~90% faster analysis | productivity gains of "about 50%" for offer analysis and tender assistance; "AI-enabled procurement can execute this type of analysis about 90% faster than manual data analysis" | BCG, 2025-04-18 (as B1) | https://www.bcg.com/publications/2025/from-buzz-to-bottom-line-cost-reductions-using-genai | C |
| **$54M quote vs ~$2.64M build (95%)** | See A1. Deputy ministers "killed the procurement" | Glubish Substack, 2026-04-06 | https://nateglubish.substack.com/p/they-said-it-would-cost-54-million | M (self-reported, unaudited). The closest Velocity analogue to "test the bid against an in-house AI-assisted estimate" |
| Bids can now be tested against the scan | "A vendor quoting three years and eight figures now has to show which parts of the work still require that much time and labour." (snippet) | Digital Journal, Jul 2026 | https://www.digitaljournal.com/article/what-albertas-ai-numbers-mean-for-it-pricing/ | Commentary |
| Should-cost platform results | a US discount retailer got "$500M savings" on apparel and footwear through parametric modelling; a restaurant chain found a "20-35% cost reduction opportunity" in poultry (snippet) | McKinsey Cleansheet product page | https://www.mckinsey.com/capabilities/operations/how-we-help-clients/cleansheet | **V.** McKinsey is selling its own product here |

Gap: I found **no** reputable, quantified public benchmark for AI in *capital-construction* bid evaluation (EPC/contractor tenders) at a utility. Most "tender AI" numbers online come from bid-writing vendors (Brainial, Altura, Minaions) and are marketing. Present bid evaluation as an extension of should-cost and offer-analysis evidence plus the Alberta example, not as a proven category.

### B3. Capital project delivery

| Figure | Exact quote | Source / date | URL | Cred. |
|---|---|---|---|---|
| **Baseline problem:** 8.5% on time and budget; 0.5% also deliver benefits | Flyvbjerg's database of 16,000+ projects: "only 8.5 percent are on-budget and on-time and ... only 0.5 percent are on-budget, on-time, and deliver the promised benefits" | Flyvbjerg & Gardner, *How Big Things Get Done*, 2023 (via Independent Review) | https://www.independent.org/tir/2023-fall/how-big-things-get-done/ | A. The strongest baseline for the size of the prize |
| Up to 20% schedule acceleration across 35+ clients; ~40% in one case | generative scheduling introduced "to more than 35 clients ... achieving schedule accelerations of up to 20 percent"; a data-centre provider saw "a ~40 percent reduction in the baseline construction schedule"; one project's "15 percent schedule acceleration ... led to a $20 million reduction in labor costs" | McKinsey × ALICE Technologies (McKinsey operations blog, 2025) | https://www.mckinsey.com/capabilities/operations/our-insights/operations-blog/mckinsey-and-alice-technologies-collaborate-to-transform-capital-project-delivery-with-generative-scheduling | **V/C.** Co-marketing alliance. "Up to" figures |
| 39% of construction non-physical work and 50% of A&E work automatable | AI could automate "39% of nonphysical work in construction, compared to 50% in architecture and engineering"; "Early adopters are reporting productivity gains from design, modeling, and construction-feasibility workflows, though these advantages will likely soon be table stakes." | McKinsey, "How AI is reshaping the future of the AEC industry", 2026-07-15 (via Construction Dive) | https://www.constructiondive.com/news/ai-report-construction-mckinsey-engineering-build-buy/825927/ | C. Technical potential, not realised savings |
| Construction productivity +0.4%/yr vs manufacturing +3.0%/yr (2000–22) | reported in Daily Commercial News summarising McKinsey | DCN (John Bleasby), 2026-09-17 | https://canada.constructconnect.com/dcn/news/technology/2026/09/ais-agentic-moment-in-construction-offers-improved-cost-and-delivery | C. Canadian trade press |
| Estimate accuracy: AACE Class 5 (−50/+100%) → Class 3 (−20/+30%) at concept stage | "By analyzing patterns in historical project data, ML models can deliver more precise and reliable early cost estimates." One utility pilot reached Class 3 ranges | Exponent, "Improving Early-Stage Cost Estimates for Utility Projects", 2025-12-12 | https://www.exponent.com/article/improving-early-stage-cost-estimates-utility-projects | M (single pilot) / V (consultancy selling the service). **Directly relevant to a utility capital programme** |
| ANN estimate fit R² 0.808 → 0.889 across 122 infrastructure projects (US$701B) | adding a complexity index raised ANN contingency-estimation R² from 0.808 to 0.889 | *Applied Sciences* 15(7):3519, 2025 | https://doi.org/10.3390/app15073519 | A. Research result, not deployment |
| >90% effort saving on engineering-standards rewrite; up to US$5M productivity | processed "750 engineering documents within a mere three weeks" (previously 4–5 a month); "expected savings of over 90%"; "up to US$5m of productivity savings" | EY client story, oil & gas capital projects (undated) | https://www.ey.com/en_us/insights/energy-resources/how-ai-drove-data-optimization-for-oil-and-gas-capital-projects | V/C. Unnamed client. "Expected" savings |
| AI adopted at scale by only 24% | "Only 24% report AI adopted at true scale globally" (snippet) | KPMG Global Construction Survey 2025/26 (n=375, pub. Mar 2026) | https://kpmg.com/xx/en/our-insights/operations/global-construction-survey.html | S. Shows the gap is still open |

Treat with caution: "WEF estimates AI can lower project costs by 20% and reduce project time by 15%" and "McKinsey ... cut costs by up to 15%, speed delivery by up to 30%" circulate widely on stats-aggregator sites. I could not trace either to a primary WEF or McKinsey page, so don't use them unless someone finds the original.

### B4. Utility and energy-sector examples

| Figure | Exact quote | Source / date | URL | Cred. |
|---|---|---|---|---|
| NiSource (gas and electric utility): >20% field productivity | "Our AI work management intelligence continues to deliver sustained field productivity uplifts of over 20%," "measured through work hours achieved, less idle time, and less rework." The company is "expanding AI into additional high-value areas including a new supply chain program to reinforce our focus on customer affordability." | Lloyd Yates, CEO, Q3 2025 earnings call, 2025-10-29 | https://finance.yahoo.com/news/nisource-ni-q3-2025-earnings-163645691.html | M (company-reported to investors). **Closest peer gas LDC example.** Covers O&M and capital work execution, not procurement |
| National Grid ET: 50% less planning time; $7.8M in avoided outage costs | advanced analytics across 60,000 assets, "reducing planning time by 50% and avoiding 1,000 outages annually, saving $7.8 million" (snippet) | Utility Dive sponsored content | https://www.utilitydive.com/spons/analytics-and-ai-for-utilities-unlocking-efficiency-and-reliability/758825/ | **V.** Sponsored post. Asset-investment planning, not procurement |
| T&D utility: 40–60% capex savings by targeting risky assets | "20-25% operating expense savings and 40-60% capital expenditure savings" (snippet) | aggregator (AIMultiple / StartUs) | https://aimultiple.com/ai-utilities | **V, untraceable.** Don't use without the primary |
| PG&E undergrounding $4M → $3.1M per mile | cost per mile fell "from $4 million to $3.1 million in 2025" | PG&E press release, 2025-10 | https://investor.pgecorp.com/news-events/press-releases/press-release-details/2025/Thousands-of-PGE-Customers-Now-Protected-from-Wildfires-as-1000-Miles-of-Powerlines-are-Energized-and-Underground/default.aspx | M. **Not attributed to AI** (contractors, equipment). Shows what unit-cost programme discipline achieves. Don't present it as an AI result |
| Ofgem AI guidance (UK regulator) | guidance "sets out good practice for all stakeholders considering procurement or deployment of AI in the energy sector" | Ofgem, May 2025 (OFG1164) | https://www.ofgem.gov.uk/news/ai-energy-sector-new-guidance-launches | Regulatory. Useful for governance framing. I found no Canadian regulator equivalent (e.g. OEB, AUC) |

Gap: I found **no** public, quantified case of a gas or electric utility or pipeline using AI for **procurement or bid evaluation on capital projects** with audited savings. Peer evidence exists for field and work-management productivity (NiSource), asset-investment planning (National Grid, vendor-reported) and estimate accuracy (Exponent pilot). Hydro One reports productivity savings ($114M in 2023), but not from AI.

---

## Credibility notes (for a leadership deck)

1. **Velocity's numbers are software-delivery numbers, and mostly self-reported.** The strongest item is the Alberta Infrastructure PRISM case ($54M quote vs ~$2.64M estimated, $858K spent at 10 months), because the software manages **capital construction**. It shows AI cutting the cost of the *tools* that run a capital programme. It does not show cheaper *construction*. Say "estimated", "unaudited", and "the vendor quote covered one of two systems".
2. **Don't transfer the 95% to physical capital.** No credible source claims 95% savings on steel, pipe, labour or construction. Credible procurement numbers are low single digits of addressable spend where measured (McKinsey pilot +1–3% value capture, Walmart 1.5–3%). Double-digit ranges (BCG 15–45%, McKinsey 10–15% negotiation) are category-level consultant potentials.
3. **Capital delivery is where the size of the prize is credible.** Flyvbjerg's 8.5% on-time-and-budget baseline is peer-reviewed and widely accepted. Even modest improvements in estimate class (Exponent: Class 5 → Class 3 at concept stage) or schedule (ALICE: up to 20%, vendor-reported) are material on a multi-hundred-million-dollar annual capital programme. Frame the argument as "reducing overrun and contingency", not as "AI makes projects 95% cheaper".
4. **Label vendor-sourced figures on the slide.** ALICE/McKinsey, McKinsey Cleansheet, Pactum/Walmart, EY client stories, Exponent, the Utility Dive sponsored post and the Anthropic case study are vendor or seller sources.
5. **Put the counterweights up front.** Gartner (Jul 2025) puts GenAI for procurement in the "trough of disillusionment". BCG says 70% of value comes from people and process. Glubish ("AI did not build these systems by itself") and Andrew Lewis ("AI without operations is just a demo") both say the gains come from operating-model change. A CTO audience will respect the pitch more if it states these limits itself.
6. **Some quotes are unverified.** Items marked (snippet) came from search excerpts because the pages blocked automated fetch. Open the URL and confirm the wording before it goes on a slide.

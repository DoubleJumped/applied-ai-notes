# 03 — Other papers, site pages, and repo sweep

Scope: Velocity White Papers dt725, l199t, l5wsi, mwo98, of1cj, oxj36, p7p2k, qthji, qxlzo, uwpxr, wq3kd, xs7uh, yzuob (English), plus site pages (about, press, resources, updates, community, privacy), `papers.json`, `README.md`, `app/site/docs/i18n-cost-ledger.md`, and a repo-wide grep (sims, canvas, glossary, gallery, transcripts, style guide). Papers m66qi, bbkac, offjm, cux4h, rhx4t, k3tc3, yu5k9, eujjc, zgym1, g3sim are covered in other notes.

Paper URL pattern: `https://thevelocitywhitepapers.com/paper/<id>/`. Source JSON: `app/site/data/papers/<id>.en.json`.

Classification key: **Measured** = reported actual. **Estimated** = author's estimate or projection. **Target** = stated aim. **Anecdotal** = an example with no method given. **Budget** = spend figure from an annual report.

---

## Headline numbers table

| # | Figure | What it measures | Baseline / comparison | Type | Source |
|---|---|---|---|---|---|
| 1 | "tens of thousands of dollars a month", heading to "hundreds of thousands" | Alberta's actual AI compute spend, now and projected | None | Measured (current, vague) / Estimated (future) | qxlzo |
| 2 | "hundreds of millions a year in cost avoidance" | Target annual cost avoidance from AI-led modernization | None given | Target | qxlzo |
| 3 | "cost avoidance on a single application ... can quite frequently exceed the entire cost for AI compute for the year" | AI compute ROI per app | Annual AI compute bill | Anecdotal, no figures | qxlzo |
| 4 | "several hundred thousand dollars ... roughly one percent of the cost of doing the same work by hand" | 14M historical images/records job, 250 agents, up to 50 days | Manual processing cost (not stated) | Estimated (planned job) | qxlzo |
| 5 | "billions of compute tokens monthly"; enterprise agreements "twenty-five to fifty million tokens per minute" | Token volume and rate-limit capacity | None | Measured (rounded) | qxlzo |
| 6 | "$5M per month" | Rough cost of one government cyber incident ("closer to a best case") | None | Estimated | mwo98 |
| 7 | "$47M in 2024-25" | Spend on application upgrades + security patching | Prior year not given | Budget (annual report) | mwo98 |
| 8 | $14.5M, up from $12.3M | Dedicated cybersecurity program budget | Prior year | Budget | mwo98 |
| 9 | "one to two dollars" | Cost to analyze an app for security gaps and often remediate a vulnerability with AI agents | None (no manual comparison given) | Anecdotal/Measured, no method | mwo98 |
| 10 | 189M/day blocked connections (126.3M, 81.2M prior years) | Cyber threat volume | 2022-23 and 2023-24 | Measured (annual report PI 2.b) | mwo98 |
| 11 | 97% of 115 critical apps with tested DR plans, up from 91% | DR readiness | Prior year | Measured | mwo98 |
| 12 | ~1,280 applications | Size of estate | — | Measured | mwo98 |
| 13 | "Tens of $M" | Savings from IT centralization and "hard supplier negotiation" (not AI) | None | Measured (vague) | oxj36 |
| 14 | "tens of millions of dollars in tools" | Organizational investment in AI tools for staff | None | Measured (vague) | dt725 |
| 15 | 65 volunteers (~5% of workforce); ~10% volunteered | AI Maximalist founding cohort | Workforce | Measured | dt725 |
| 16 | >2,000 public servants trained; >15,000 across Canada | AI Academy reach since Sep 2025 | None | Measured | press page |
| 17 | ~9/10 | Level 1 satisfaction | None | Measured (survey) | dt725 |
| 18 | "two and three months" | Time before most people use chat tools well consistently | None | Anecdotal/observed | dt725 |
| 19 | ~100x coding speed; 20x target overall | AI coding speed vs overall delivery acceleration | Not defined | Estimated / Target | dt725, uwpxr |
| 20 | "roughly six weeks to as little as thirty minutes" | Idea-to-prototype time | Pre-AI prototype time | Anecdotal (best case) | p7p2k |
| 21 | ">1,000 applications", "dozens" in production | Apps built Mar 2025–May 2026 | — | Measured | p7p2k |
| 22 | "600+ apps" in 3 months | Apps built on Nexus platform | — | Measured | uwpxr |
| 23 | 7–10% | Share of AI-built work that becomes rework (drift) | "98 to 100 percent functionally correct" | Estimated | of1cj |
| 24 | ~$2,500 | Model cost to make the full K-12 curriculum AI-ready (2,400+ files, 42,000 PDF pages, 50,000+ tags) | "price of a modest laptop" | Measured | wq3kd |
| 25 | ~$200 | Model cost to benchmark 31 acts from 14 jurisdictions (~8,000 comparisons, ~1,059 findings) | Manual: "months or years" / "procured and completed manually over a year" | Measured cost; baseline estimated | wq3kd |
| 26 | < $4, ~1 hour | Build a curriculum-aligned learning game once data was ready | — | Measured | wq3kd |
| 27 | 95–98% | Best-model resistance to prompt injection/hijacking | — | External estimate | qxlzo |
| 28 | ~99% | Share of systems at Protected B or lower | — | Estimated | qxlzo |
| 29 | CAD $41.7M saved; ~1,726 → ~286 person-months; 5–8 years → 14 months; ~6:1 | Simulated rationalization of one ministry's 185 apps into 16 services | Traditional delivery estimate | **Simulation estimate** | sims/rationalize.json (embedded in zgym1) |
| 30 | 466M lines, ~3,400 repos, ~50 agents, ~20 hours | Estate code scan | "By hand ... years" | Measured | press page, xs7uh |
| 31 | "up to 20 times" faster; "as much as 95 per cent" less time to modernize | Speed-up claims | Not defined | "Demonstrated the potential", i.e. best case | press page |
| 32 | ~$60–150 per additional language (text + 238 images + ~350K TTS chars) | AI cost to translate the whole site | Human review "is the real cost" | Estimated (rates illustrative) | i18n-cost-ledger.md |
| 33 | ~504K tokens, 80 calls (Spanish text); +~314K tokens gap-fill; 108 images; ~360K TTS chars | Actual AI usage for Spanish edition | — | Measured usage (no $ recorded) | i18n-cost-ledger.md |

---

## Findings by source with quotes

### qxlzo — The Agentic Technology Stack (paper 12)
URL: https://thevelocitywhitepapers.com/paper/qxlzo/

The single most useful paper for a CTO-level financial argument. It is the only place Alberta states its AI run-rate and its ROI thesis together.

- AI spend now and projected:
  > "On cost, we now spend tens of thousands of dollars a month and expect hundreds of thousands as agents support every application. The aim is to modernize at speed and deliver enhanced services, with hundreds of millions a year in cost avoidance."
  - Measures: monthly AI compute spend (current, vague) and annual cost avoidance (target). No baseline or method for the cost-avoidance figure.
- Token volume and the ROI claim:
  > "We now consume billions of compute tokens monthly, and anticipate the cost of consumption to reach hundreds of thousands a month as the four approaches are implemented and an AI agent supports every application for monitoring, cybersecurity remediation, and development. Relative costs remain low, and even with these new financial expenditures, the cost avoidance on a single application out of hundreds can quite frequently exceed the entire cost for AI compute for the year."
  - Measures: payback. Anecdotal, no application named, no numbers.
- Capacity constraint:
  > "even our enterprise agreements, at twenty-five to fifty million tokens per minute, will likely be exceeded soon, so we are moving to a diversified, load-balanced approach to throughput."
- Large batch job vs manual (keystat "250 agents · 50 days"):
  > "Processing roughly 14 million historical images and records will require 250 concurrent agents running for as long as 50 days. However, at a cost of several hundred thousand dollars, this is roughly one percent of the cost of doing the same work by hand."
  - Estimated (future tense). Implies a manual baseline of tens of millions, not stated.
- Demand-creation caveat (important for honesty in the pitch):
  > "While they are highly cost-effective when used well, AI agents are also opening up work we would simply not have pursued otherwise instead of strictly reducing the cost of work we already do. As the tools become available, both the appetite to build meaningful new services and the need to remediate technical debt grow together. Our aim is to modernize at speed and to deliver enhanced services, with hundreds of millions a year in cost avoidance and staffing steady, and to move from vendor-locked technologies toward platforms that give us latitude as we scale."
  - Note "staffing steady": the goal is avoidance, not headcount cuts.
- Vendor lock-in:
  > "Over eighteen months we have tried a range of models, floating between Gemini, OpenAI, and Anthropic, and right now Claude outperforms most others, though we expect that to change. An abstraction layer like the Bifrost gateway lets us move a workload from one provider to another ... It also keeps spending under control, with per-workload budgets so token use does not run away. We would not advise any government to put all its eggs in one basket".
- Security limits:
  > "No model today fully resists prompt injection, and even the best resist hijacking only ninety-five to ninety-eight percent of the time."
  > "the large majority of systems, likely ninety-nine percent or more, sit at Protected B at the highest. Sensitive data is controlled in Canada through our enterprise agreements, and the most sensitive workloads run offline on our own cluster."
- Controls table (risk → control): provider lock-in → gateway abstraction; runaway token use → "Per-workload budgets and point-in-time approvals"; data loss → Defender and Purview; supply-chain poisoning → "Audit and evaluate harnesses and skill files before use"; public-facing prompt injection → "Avoid or selectively design public AI; validate with synthetic data"; agent identity and observability → "An area still in development".

### mwo98 — The Cyber Imperative (paper 2)
URL: https://thevelocitywhitepapers.com/paper/mwo98/

Frames the cost of *not* modernizing. Figures sourced to the Technology and Innovation 2024-25 Annual Report.

- Incident cost:
  > "Rough cost of a single government cyber incident — $5M per month ... And that is closer to a best case. A significant data breach or ransomware event runs far higher."
  - Estimate, no method given.
- Current maintenance spend:
  > "In 2024-25, we spent 47 million dollars maintaining applications with upgrades and security patching to reduce vulnerabilities and chip away at the technical debt. Our dedicated cybersecurity program grew to 14.5 million dollars from 12.3 million the year before. Across the 115 applications classified as critical, 97 percent now hold tested disaster-recovery plans, up from 91 percent."
- AI unit cost for remediation:
  > "AI drives down the cost of protecting the domain. We can now analyze applications for cybersecurity gaps and often remediate vulnerabilities for one to two dollars."
  - Striking but unsupported: no count of vulnerabilities, no definition of what the $1–2 covers (tokens only, not staff time).
- Threat volume: "189 million attempts ... The year before it was 126.3 million, and the year before that 81.2 million" (Annual Report PI 2.b).
- Estate and vendor support:
  > "We maintain roughly one thousand two hundred and eighty applications, many of them aging. A meaningful share runs on technology more than a decade past vendor support ... You cannot patch what the vendor no longer ships."
- Delivery-funding gap (relevant to capital projects):
  > "Historically, Technology and Innovation has built agile delivery teams from individual contractor resources, known as 'contingent labour' ... there is often little or no money after the completion of a project to fund remediation except in the most extreme cases".
- External reference points: Anthropic Mythos/Project Glasswing "more than 10,000 vulnerabilities"; Mozilla "271 security bugs in Firefox in one month, more than ten times what its earlier methods had ever surfaced."

### wq3kd — The Shape of Data (paper 21)
URL: https://thevelocitywhitepapers.com/paper/wq3kd/

The cleanest *measured* AI unit costs in the collection, and the closest analogue to procurement/regulatory document analysis.

- Regulatory benchmarking:
  > "Carrying thirty-one acts from fourteen jurisdictions through the full pipeline cost around two hundred dollars in model usage."
  > "Answering that by hand would mean reading an entire act against the acts of a dozen other jurisdictions, clause by clause, a process which could take a team months or years to complete manually."
  > "A regulatory analysis prototype can be completed in hours for work which would be procured and completed manually over a year."
  - Output: 265 baseline sections, "just under eight thousand precomputed comparisons", "a little over one thousand structured observations, findings, and recommendations", each traced to source page. Cost = model usage only; staff time excluded.
- Curriculum:
  > "Turning the entire published K-12 curriculum into an AI-ready substrate cost roughly twenty-five hundred dollars in model usage."
  > "Because the data was ready for AI, building a curriculum-aligned, age-appropriate, custom learning experience only took an hour and was completed for less than $4."
- Repeatability: "We have run this pattern of deep analysis and benchmarking dozens of times over the past year".
- Spending advice to leaders:
  > "For a leader deciding how to spend on AI, the lesson is to stop buying chat conversations and start building data pipelines and memory systems."
- Auditability: "Every analysis run records the AI's reasoning: the documents it saw, the model it used, the version of the instruction it followed, and the date it ran. Analysis can be re-run numerous times against the same subject and audited for drift or difference."

### qthji — The AI Factory: Design and Ideation (Pronghorn) (paper 8)
URL: https://thevelocitywhitepapers.com/paper/qthji/

Directly relevant to procurement and capital project front-end work: Pronghorn ships agents that draft the business case, charter, and RFP.

> "Pronghorn ships a set of agents that prepare a project for approval and for the build. A business-case writer, a charter and RFP writer, a project planner, and a timeline builder read your chats, your artifacts, and your canvases, and produce a project plan ready to take to a client for buy-in."

> "Alberta's objective is to maximally leverage AI to increase quality and speed while reducing cost."

- No quantitative results for Pronghorn. Open-source (MIT); Pronghorn Blue is "maintained in partnership between Microsoft and the Government of Alberta", Azure-native with OpenAI support.
- Governance point: "AI-based application development skips many if not most of these steps by default ... you see the body of the car, but the brakes, engine, axles, and chassis are absent." Pronghorn exists to force requirements, standards, costing, and sign-off before build.

### uwpxr — The AI Factory: Orchestration and Observation (Nexus) (paper 9)
URL: https://thevelocitywhitepapers.com/paper/uwpxr/

- Throughput:
  > "Since it went live just three months ago, more than six hundred applications have been built on Nexus ... it is the platform behind our aim of a twentyfold acceleration in delivery."
  - Measured count; 20x is a target.
- Cost and data controls:
  > "Users who submit PII to models that do not have sufficient classification get flagged and notified ... Both platforms enable cost containment, where developers and workloads can be given daily budgets to prevent runaway token use for long-form jobs, or request point-in-time budget approvals right through the console for large amounts of data processing."
- Access: "The agent works under delegated access that expires every few hours, so nothing it is granted is permanent ... observability lets a developer watch their own agents while administrators audit every agent on every machine."
- Trust rule: "We teach our staff to verify, then trust. An output that cannot show its work is not trusted, however good it looks."

### p7p2k — The Well-Built Harness (paper 6)
URL: https://thevelocitywhitepapers.com/paper/p7p2k/

- Speed:
  > "The time to turn an idea into a working prototype fell from roughly six weeks to as little as thirty minutes. The speed was real, but the prototypes could not be reproduced twice, they skipped controls a public service requires, and the agents reported themselves finished when they were not."
- Volume and conversion rate:
  > "Since starting the AI Maximalist program in March 2025 to today in May 2026, the Department has produced far more than 1,000 applications. The vast majority are prototypes, but dozens have made it into production".
  - Useful honesty: production conversion is "dozens" out of 1,000+.
- Hidden cost of speed: "Months of time saved on the frontend can easily be lost on the backend implementing the necessary security controls".
- Method: "Alberta took the time to benchmark the quality of human and AI outputs before building the harness." (No benchmark numbers published.)
- Investment note: "providing staff time to learn, create, and refine these methods is a worthwhile investment." "Put your best developers on the templates."

### of1cj — Technical: The Anti-Drift Harness (paper 18)
URL: https://thevelocitywhitepapers.com/paper/of1cj/

> "7–10% of the work becomes rework that piles up over time, mostly drift between related pieces"
> "An AI's code can be 98 to 100 percent correct and run, yet only about 90 percent well built underneath."

- Estimate, no measurement method. Useful as a realistic quality-tax number. Cost control: watchers can run "on a cheaper AI for routine checks, saving the strongest model for the hard calls", and a watcher "can stop the AI and require the drift be fixed before work continues."

### l199t — Red, Blue, Green, and Yellow Agents (paper 7)
URL: https://thevelocitywhitepapers.com/paper/l199t/

- No dollar figures. Control counts: "A complete pass runs over four hundred individual checks: 285 ASVS Level 2 requirements, 62 Alberta cloud-security rules, plus the Green, Yellow, and Red checks." Template carries "about ninety-five major security controls".
- Cost observability: "Using an API key on Google Enterprise Agent Platform, AWS Bedrock, or Azure AI Foundry, each sub agent can be monitored for cost and token throughput." Rule "AI-003 AI Cost Controls" sits in the AI Agent Security domain of Alberta's baseline.
- Design choice: deterministic scanners (no AI) run first; LLM judgement only where needed. "These agents do not replace more comprehensive security management suites."

### l5wsi — Technical: Anatomy of a Template (paper 17)
URL: https://thevelocitywhitepapers.com/paper/l5wsi/

- No financial figures. Governance: "Known gaps or deferred decisions are documented, not hidden. The stack is open source throughout ... so there is no vendor lock-in".

### oxj36 — Establishing a Builder Culture (paper 14)
URL: https://thevelocitywhitepapers.com/paper/oxj36/

- Centralization savings (not AI):
  > "Tens of $M — Recent savings from a single estate and hard supplier negotiation, the benefit centralization is meant to deliver, and a reason the protective core stays central."
- Sprawl risk:
  > "When the cost of a new application falls far enough, the estate can swell from 1,400 systems to fourteen thousand or a hundred and forty thousand ... The government carries no fewer than 18,000 SharePoint sites".
- Shadow AI:
  > "The low cost of AI tools, their enormous capability, and the needs of a business team make it trivial for shadow IT, or shadow AI, to emerge ... shadow AI tools, subscriptions, and solutions are already here, whether organizations wish to admit it or not."
- Operating model: center keeps "cybersecurity, identity and access, networking, databases, licensing, operating systems, telephony, and end-user compute"; IT becomes "a consultancy model in place of a delivery one ... Technology and Innovation provides the fortress, the governance of technology, the management of vendors, and the controls". "Alberta already runs data and procurement this way" (hub-and-spoke). Pilot of builder mode planned for 2026.
- Claim: "we gain a stronger security posture, faster delivery, and real cost containment" (no figures).

### dt725 — The AI Academy: Investing in People (paper 13)
URL: https://thevelocitywhitepapers.com/paper/dt725/

- Investment:
  > "The organization does everything it can for its people, with weeks and months of training, tens of millions of dollars in tools, and the content to learn from."
- Founding cohort: "About sixty-five volunteers, roughly five percent of the workforce, formed the founding cohort ... Close to ten percent had volunteered."
- Reach and satisfaction: "More than ten thousand public participants have used the Alberta AI Academy platform, alongside thousands of public servants. Level one satisfaction averages around nine out of ten."
- Adoption time: "it is somewhere between two and three months before most people use these tools well on a consistent basis."
- Structure: launched 9 Sep 2025 (pitched to minister June 2025, ~3-month build). Level 1 prompting (RICECO + TRUST "verify, then trust"), Level 2 reusable agents (Gemini Gems, GitHub Copilot Agents, AgentBuilder Console), Level 3 enterprise apps with the harness. Level 1 cut from ten days to one week. Level 2 "rule of three": build an agent if a task recurs more than three times a week.
- Drop-off: "In our most recent cohort we saw a meaningful drop-off, with many participants not finishing or graduating" at Level 3. Lead instructor taught Level 3 "for more than twenty-five days over the past year".
- Speed framing: "AI agents can code about a hundred times faster, yet we aim for a twentyfold improvement overall, because the goal reaches past the app and the artifacts to engagement, comfort, and change management."

### xs7uh — Technical: The Canvas (paper 19)
URL: https://thevelocitywhitepapers.com/paper/xs7uh/
- Restates: "≈466M lines across ~3,400 repositories, scanned by ~50 agents in ~20 hours." and "185 applications collapsed into 16 shared modules; complexity down more than 90%."

### yzuob — Managing Change
URL: https://thevelocitywhitepapers.com/paper/yzuob/
- Draft placeholder: "Content forthcoming." Nothing to cite.

### Simulation: Rationalizing a Ministry (`app/site/data/sims/rationalize.json`, embedded in zgym1)
The only explicit dollar-savings figure for a delivery program in the whole repo:
> "Done the traditional way, this is roughly one thousand seven hundred person-months of work, five to eight years. Rebuilt this way, the estimate is about two hundred and eighty-six person-months across fourteen months. That is a six-to-one compression in effort, and close to forty-two million dollars saved. One hundred and eighty-five applications collapse into sixteen services on four shared platforms. What you have watched is a simulation ... It is a rehearsal."
- Caption: "Traditional: ~1,726 person-months · 5 to 8 years" / "This way: ~286 person-months · 14 months · ~6:1 · CAD $41.7M saved". Also "814 of 859 capabilities preserved · 94.8%".
- Implied labour rate: $41.7M / 1,440 person-months saved ≈ $29K per person-month (≈ $350K/yr fully loaded). The rate is not stated in the file. Treat as an illustrative estimate, not a result.

### Press page (`app/site/data/pages/press.en.json`, news release 6 Jul 2026)
URL: https://thevelocitywhitepapers.com/#/press (site route)
> "Alberta has accelerated the rebuilding of the decades-old technology behind its public services in a fraction of the usual time and cost."
> "In about 20 hours, those agents reviewed more than 466 million lines of government code ... By hand, that work would have taken years."
> "Supporting one ministry, a plan is underway to leverage AI agents to replace 185 aging systems with 16 modern applications which the government owns outright. AI agents have demonstrated the potential of speeding up work by as much as 20 times while reducing the time to modernize critical systems by as much as 95 per cent."
> "Since it launched in September 2025, the Academy has trained more than 2,000 public servants ... more than 15,000 people from across Canada have trained on the platform".
- Minister quote: "doing it faster and for far less." Partner quotes from Anthropic, Google Cloud, Info-Tech ("the first defensible, in-production blueprint for an agentic public service").
- All speed claims are "as much as" / "potential" language.

### About page (`about.en.json`)
- Disclaimer: "we are not responsible for decisions taken, liability, or costs incurred as a result of your use of this content ... Always consult with your IT organization prior to making any decisions."
- Where AI failed: "In some topics, AI use was counterproductive ... The Compression Problem in particular defeated the AI editors ... The entire paper had to be written by hand from scratch." "Even the most capable current models ... remain insufficient for original or creative writing."
- Shelf life: "within as little as six months some of the methods and insights here may be obsolete."
- Procurement pipeline: "an ongoing set of procurement challenges open to a wide range of participants in the months and years ahead."
- Provenance: ideas gathered over "roughly eighteen months" via the AI Maximalist program and AI Factory.

### Resources page (`resources.en.json`)
- Links to GoA AI Usage Policy (PDF), a Sovereign Compute Environment pre-qualification request (PQR), federal AI for All strategy, and the federal Buy Canadian procurement policy. Useful as governance and procurement reference points; no figures.

### Updates / community / privacy pages
- Updates: launch 6 Jul 2026 after "a soft launch with industry partners on June 16th"; 21 papers and 7 public repos at launch. No financial content. Privacy: site collects no personal info. Community: contact inbox only.

### papers.json
- Nothing new beyond abstracts. Confirms paper 22 (m66qi, covered elsewhere) is the procurement paper: "Taking the Hill: Innovating on Procurement with AI Insights".

### Compression Problem transcript (`app/site/public/transcripts/the-compression-problem-second-transcription.md`)
Raw dictation, not edited paper text. Two lines worth knowing:
> "if I'm going to implement $100 million applications for a system, I need high confidence that the checks and balances have been met"
> "the slow hierarchy that takes a month to pass the message between the individual contributor and the senior executive there's no amount of ai that's going to result in the kind of roi that i'm seeking because the time that's being lost is not the time of people doing work it's the time in between work"
- The second is a useful caution for a capital-project pitch: the ROI bottleneck is approval latency, not task time.

### README.md
- "Because it is static, it runs on any plain web server and costs almost nothing to host." Tools disclosed: Claude (Claude Code, Agent SDK) for writing/translation, OpenAI gpt-image-1 for imagery, ElevenLabs voice clone for narration.

---

## AI cost data (what it cost them)

The collection offers four tiers of real spend data.

1. **Enterprise AI run-rate (qxlzo).** "tens of thousands of dollars a month" today, "billions of compute tokens monthly", projected to "hundreds of thousands a month" once an agent supports every application. That is roughly $0.1–0.5M/yr now and low single-digit $M/yr at scale, set against the target of "hundreds of millions a year in cost avoidance" and $47M/yr current patch-and-upgrade spend (mwo98).
2. **Task-level unit costs, measured.**
   - ~$200 model usage: 31 statutes × 14 jurisdictions, ~8,000 clause comparisons, ~1,059 findings (wq3kd). Manual baseline stated as "months or years" / "procured ... over a year".
   - ~$2,500: 2,400+ files, 42,000 PDF pages → 50,000+ tagged outcomes (wq3kd).
   - < $4 and ~1 hour: an app built on that curated data (wq3kd).
   - $1–2: AI security analysis and, often, remediation of a vulnerability (mwo98).
   - Several hundred thousand dollars: 14M-record job, 250 agents × up to 50 days, "roughly one percent" of manual cost (qxlzo, estimate).
3. **Tooling and people.** "tens of millions of dollars in tools" plus "weeks and months of training" (dt725). AI Academy: >2,000 public servants trained, >15,000 external users, materials open-source. Academy build took about 3 months (June pitch → Sep 9, 2025 launch). Founding cohort 65 people (~5% of workforce).
4. **A fully itemized ledger (i18n-cost-ledger.md).** The only line-item AI cost record in the repo, for translating the whole site into one language:
   - Estimate per language: text ~$ single-to-low-double digits (Sonnet-class) or low tens (Opus-class); images 238 × $0.04–0.19 = ~$10–45; TTS ~350K chars × $0.15–0.30/1K = ~$55–105; "roughly $60–150 all-in".
   - Spanish actuals (7 Jul 2026): 277,760 input + 226,187 output tokens (~504K, 80 calls, Claude Sonnet on Vertex) for 22 papers + 6 pages + 7 sims; a further 201,906 + 112,729 tokens for a gap-fill pass; 108 images (gpt-image-1); 199 MP3s / ~360K TTS chars (ElevenLabs), 5h48m of audio. Dollar actuals were **not** recorded (all "—").
   - Key line: "Human review time is the real cost, not tokens." A professional Spanish review (docx) was later merged (2026-09-04).

Takeaway for the pitch: token costs for document-heavy analysis are trivially small (hundreds to low thousands of dollars per corpus). The real costs are people (review, training, harness/template building) and platform controls. Every "cost" figure above is model usage only; none includes staff time.

---

## Governance and risk points for a CTO audience

1. **Spend caps at the gateway.** All model traffic routes through a gateway (Bifrost) with per-workload and daily budgets plus "point-in-time budget approvals right through the console" for large jobs (uwpxr, qxlzo). Each sub-agent is monitored "for cost and token throughput" (l199t). "AI Cost Controls" is a named rule (AI-003) in the security baseline.
2. **Multi-vendor by design.** "We would not advise any government to put all its eggs in one basket." The abstraction layer allows moving workloads across providers or to on-prem compute. Model leadership "alternates every couple of months". Tools are open-source (MIT) to avoid lock-in.
3. **Data classification gates model choice.** ~99% of systems ≤ Protected B; data kept in Canada under enterprise agreements; most sensitive workloads offline on own cluster; PII sent to an under-classified model is flagged and the user is notified. Defender and Purview as DLP.
4. **Public-facing AI is restricted.** Best models resist injection only 95–98% of the time, so public-facing and personal-information AI is "avoided or selectively designed".
5. **Time-boxed agent identity.** Delegated access expires every few hours; admins can audit every agent on every machine. Agent identity management is openly "still in development".
6. **Verify, then trust.** "An output that cannot show its work is not trusted." Agents are "unreliable witnesses" to their own work (p7p2k). Independent review agents run 400+ checks (285 OWASP ASVS L2 + 62 provincial cloud rules). Deterministic scanners come first and the LLM is used only for judgement.
7. **Audit trail and reproducibility.** Every analysis run records documents seen, model, instruction version, and date, and can be re-run to check drift (wq3kd).
8. **Quality tax is explicit.** 7–10% rework from drift even when code is 98–100% functional (of1cj). Speed gains on the front end can be lost to security work on the back end (p7p2k).
9. **Requirements before build.** Pronghorn forces business case, charter, RFP, costing, and sign-off artifacts before any code (qthji). This is the most direct procurement/capital-planning analogue.
10. **Sprawl and shadow AI.** Cheap building creates new debt, so automated disposition is needed. Shadow AI is "already here". The answer is governed central platforms plus training, not prohibition (oxj36).
11. **Central governance, distributed delivery.** Center keeps security, identity, network, data, licensing, and vendor management. Ministries build on governed tools. Alberta already runs data and procurement this way (oxj36).
12. **People investment is a precondition.** Graduated academy, 2–3 months to proficiency, meaningful Level 3 drop-off, "staffing steady" target (dt725, qxlzo).
13. **Harness supply chain.** "We audit the harnesses we use, since a poisoned one can turn an agent against us." "You cannot vibe code a harness."

---

## Caveats

- **Almost no ROI is measured end to end.** The large figures are targets ("hundreds of millions a year in cost avoidance"), best-case framings ("as much as 20 times", "as much as 95 per cent", "as little as thirty minutes"), or simulations ($41.7M is a simulation caption with no stated labour rate or method). The measured dollar figures are small unit costs (model usage only) and government budget lines unrelated to AI results.
- **Unit costs exclude people.** The $200, $2,500, $4, and $1–2 figures are model/token spend. Staff time, platform build, harness engineering, and review are not counted. The i18n ledger itself says "Human review time is the real cost, not tokens."
- **Manual baselines are vague** ("months or years", "years", "by hand"). None is costed except the implied ~100x on the 14M-record job.
- **Demand growth offsets savings.** Alberta states agents open "work we would simply not have pursued otherwise instead of strictly reducing the cost of work we already do." Budget for scope growth, not only savings.
- **Production conversion is low.** 1,000+ apps, "dozens" in production. 600+ Nexus apps in 3 months with no production count given.
- **Inconsistent reach numbers.** dt725 says ">10,000 public participants"; the press release says ">15,000 people from across Canada" and ">2,000 public servants". Different dates or definitions, so cite with the source.
- **The context differs from a utility.** This is a provincial IT estate modernization (1,280 apps, 466M LOC) by a central IT ministry with enterprise model agreements. Nothing in these papers measures AI applied to engineering procurement, bid evaluation, or capital project delivery as such. The closest analogues are the regulatory benchmarking pipeline (wq3kd) and Pronghorn's business-case/charter/RFP agents (qthji), and neither reports outcome metrics.
- **Self-published advocacy.** Written by the Deputy Minister and released with vendor partner quotes. The about page disclaims liability and warns methods may be obsolete "within as little as six months". The ministry's "Tens of $M" savings came from centralization and supplier negotiation, not AI.
- **yzuob (Managing Change) is an empty placeholder.**
- Ledger dollar actuals were never filled in. Only token, image, and character counts are real.

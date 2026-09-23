# 02 — Case studies and project-delivery economics

Source: Government of Alberta, *The Velocity White Papers* (Ministry of Technology and Innovation, "TI"). Read from the GitHub repo JSON (`app/site/data/papers/<id>.en.json`), including the body blocks and each paper's TL;DR slide deck. Read on 2026-09-23.

Papers covered (7):

| id | Title | Paper # / track | Published | URL |
|---|---|---|---|---|
| cux4h | The Two-Billion-Dollar Ship of Theseus | 1 · Conceptual foundation | 2026-06-16 | https://thevelocitywhitepapers.com/paper/cux4h/ |
| zgym1 | The Four Approaches to AI Modernization | 5 · Defining the Problem | 2026-06-16 | https://thevelocitywhitepapers.com/paper/zgym1/ |
| k3tc3 | The AI Factory: Measuring Project Delivery (Velocity Game Engine) | 10 · Engineering the Solution | not dated in JSON | https://thevelocitywhitepapers.com/paper/k3tc3/ |
| rhx4t | AI Factory Case Study: From Five Months to Four Days | 11 · Engineering the Solution | 2026-06-19 | https://thevelocitywhitepapers.com/paper/rhx4t/ |
| eujjc | The Compression Problem | 14/15 · Human and Change Management | not dated in JSON | https://thevelocitywhitepapers.com/paper/eujjc/ |
| yu5k9 | Measuring Failure and Success | 15/16 · Human and Change Management | not dated in JSON | https://thevelocitywhitepapers.com/paper/yu5k9/ |
| g3sim | Simulation: Government 3.0 | 19 · Technical Appendix | 2026-06-16 | https://thevelocitywhitepapers.com/paper/g3sim/ |

Status legend used below:
- **Measured**: reported as an observed outcome of work actually done. Note that none of these come with a published method, cost breakdown or independent check.
- **Estimated**: a counterfactual, a heuristic or a back-of-envelope figure.
- **Target**: an aspiration or goal.
- **Assertion**: a qualitative claim that isn't tied to any stated measurement.

---

## 1. Headline numbers

| # | Number | What it measures | Baseline / comparator | Status | Paper |
|---|---|---|---|---|---|
| 1 | **$108K vs $1.3M–$1.9M** | ACIP (Alberta Classroom Information Portal) build cost, factory vs traditional | TI's estimate of what a traditional product team would cost. No method given | Factory cost measured ("approximately"); traditional cost **estimated** | rhx4t |
| 2 | **11 weeks vs 12–18 months** | ACIP delivery time | Same estimated traditional product team | 11 wks measured; 12–18 mo **estimated** | rhx4t |
| 3 | **5 months → 4 days** | Remote Area Heating Allowance app, original hand build vs factory rebuild | The author's own hand-coded Java build, about 25 years earlier | Measured, but it's a **prototype** and the baseline is ~25 years old | rhx4t |
| 4 | **25x speed / 95% drop in delivery cost** | Summary claim for the two case studies | Implied from #1–#3 | Derived. ACIP works out to 92–94% cost reduction (see §4) | rhx4t (abstract) |
| 5 | **~95%** | Reduction in "cost and time" of software implementation / remediation | Conventional pace | **Target** ("believes", "reach for") | cux4h, zgym1 |
| 6 | **20x** | Project-level delivery-speed goal | Pre-AI delivery | **Target** | k3tc3, eujjc |
| 7 | **100x+** | AI vs human, coding task only | Human developer | **Assertion**. No measurement given | k3tc3 |
| 8 | **"work of 20 people"** | One human paired with an AI agent | Individual human | **Assertion** ("bold claim", "proven... over the last 18 months"). No data given | cux4h |
| 9 | **~$2B** | Cost to modernize the GoA technical estate | Fall 2024 senior-leadership estimate, "simple heuristics", "likely much higher" | **Estimated** | cux4h |
| 10 | **$80M–$120M / yr** | TI's annual modernization budget | n/a | Stated fact | cux4h |
| 11 | **~20 years** | $2B ÷ ~$100M/yr, if nothing else changed | Arithmetic | **Estimated** | cux4h |
| 12 | **130 years** | Time to lifecycle the existing systems at 2024 delivery velocity | 2024 delivery benchmark (method not published) | **Estimated** | cux4h |
| 13 | **466M lines of code** | Size of the GoA code estate | n/a | Stated as measured | cux4h, eujjc |
| 14 | **~600 apps** | Modernization backlog | n/a | Stated (KPI baseline) | yu5k9 |
| 15 | **185 apps → 16 modules** | One ministry's rationalized target architecture | Current app inventory | **Proposed target architecture** from the Git Insights tool, not a completed rebuild | zgym1 |
| 16 | **5–8 years → weeks to months** | Replacement program duration, traditional vs rationalization | Traditional replacement program | **Estimated / aspirational** | zgym1 |
| 17 | **Team of ~7 (5–9) → 1–2** | Delivery-unit size | Agile team of 8–12 / product team of 5–9 | Observed ("we have seen"), anecdotal | rhx4t, k3tc3 |
| 18 | **5 apps in parallel, 1 lean team** (+4 more by end of Aug) | Throughput | Traditional: 4–5 teams of ~7 for a portfolio | 5 in flight = observed; +4 = **forecast** | rhx4t |
| 19 | **Product teams cut time and cost "roughly in half"** vs vendor contracts | Prior-era improvement | Large vendor contracts | **Assertion** | rhx4t |
| 20 | **"several hundred million dollars"** | Application Master Services Agreements with vendors | n/a | Stated | cux4h |
| 21 | **+78.2% / +~33%** | Rise in publicly known vulns in GoA's tech stack over 12 months, plus extra found by internal assessment | Prior 12 months | Measured (method elsewhere in the collection) | cux4h |
| 22 | **1 : 8 → 8 : 1** | Human manager:staff ratio vs proposed supervisor-agents:worker-agent | GoA roughly 1 manager per 8 staff | Human ratio stated; agent ratio **proposal** | eujjc |
| 23 | **40K–400K characters** | Effective working reach of a single agent | 466M LOC estate | **Estimate** | eujjc |
| 24 | **30 days → 29 days** | Illustrative: briefing cycle if only the work time is compressed and the hierarchy isn't | Month-long hierarchy round trip | **Illustrative** | eujjc |
| 25 | **"a few thousand dollars and a weekend"** vs "$100M system" | Cost of a failed AI experiment vs a one-shot traditional system | n/a | **Illustrative** | eujjc |
| 26 | **"tens of billions"** | Savings if the approach were extended across Canadian federal + provincial governments | "Extrapolation from costs already demonstrated in production" (i.e. ACIP) | **Extrapolation** | rhx4t |
| 27 | **5 years → 8 minutes** | Simulation playback of a staged transformation | n/a | Presentation device, not a delivery metric | g3sim |
| 28 | **65,000 transactions / 5 min** | Load when 100 Academy agents hit the Velocity board | n/a | Measured (stress-test event) | k3tc3 |

---

## 2. Per-paper findings with quotes

### cux4h — The Two-Billion-Dollar Ship of Theseus
https://thevelocitywhitepapers.com/paper/cux4h/ — thesis paper that frames the problem and sets the 95% target.

**Portfolio / technical-debt cost (estimated)**
> "In Fall 2024, the senior leadership team within the Ministry of Technology and Innovation (TI) estimated that the cost of modernizing these systems was roughly two billion dollars. The methodology used some simple heuristics; the cost is likely much higher. Regardless, the number serves as a reasonable starting point for a conversation."

**Budget and the naive runway (arithmetic)**
> "Within TI, our budget to modernize such systems fluctuates between $80M and $120M annually. This means that if we did nothing else, and costs did not increase, and all technologies and their supports stayed static, and we dedicated our full time to fixing this problem, we could modernize these systems in roughly 20 years. That's a lot of 'ifs'."

**Delivery-velocity baseline (estimated, method not published)**
> "When we benchmarked our delivery velocity in 2024, we estimated it would take 130 years to lifecycle our existing systems."

Keystat: "At the current speed of remediation, the runway to clear the existing technical debt runs to roughly 130 years."
*Note:* the 20-year figure is budget-bound and the 130-year figure comes from a delivery-velocity benchmark. The gap between them suggests delivery capacity, not money, is the binding constraint. The paper doesn't spell that out.

**Vendor spend**
> "Presently, our government has several hundred million dollars in Application Master Services Agreements with vendors which exist to keep these systems modern. However, these contracts are failing to deliver the outcomes we need."

**Risk growth (measured)**
> "In the last 12 months, the number of publicly known vulnerabilities in the underlying technologies that Alberta uses rose by 78.2%. Our own deep assessment of the estate uncovered a further ~33% increase above that baseline, so documented cyber concerns have more than doubled."

**Scale of estate**
> "...analyze our entire technical estate, a span of code currently exceeding 466 million lines, and read every pattern, dependency, relationship, and function across thousands of applications in less than a day."

**Demand pressure**
> "Currently there are more than forty such legislative or regulatory initiatives underway." / "Vendor application support is ending on numerous critical systems in the coming 12 to 48 months"

**Productivity claim (assertion)**
> "when an AI agent is paired with a human worker, they can frequently do the work of 20 people, and often in a fraction of the time. This is a bold claim, but one which we have proven in Alberta time and again over the last 18 months, and for which we will lay down the evidence..."

**Agent coverage ratio (proposal)**
> "It is reasonable, and practical, to create 1 to 10 agents which do nothing but obsessively evaluate, monitor, and if need be, repair every application in the estate."

**The 95% target**
> "With the right engineering, training, and strategies, Alberta believes it can reduce the cost and time of implementing these remediations by roughly ninety five percent."
> "By following these methods herein, we believe that we can reduce both the time and cost of digital transformation."

TL;DR slide: "The target: a 95% reduction in the cost and time of digital transformation."

---

### rhx4t — AI Factory Case Study: From Five Months to Four Days
https://thevelocitywhitepapers.com/paper/rhx4t/ — **the only paper with concrete project-level cost/time evidence.** It's written first-person by Chris Wright (Director of Integration Services) and Sheldon Bauld, with Michelle Dias. Published 2026-06-19, "six months in".

**Abstract claim**
> "Two case studies are presented below which demonstrate real-world examples where staff experienced a 25x speed improvement in development and a 95% drop in delivery costs."

**Case 1: Remote Area Heating Allowance (RAHA)**
> "...originally coded by hand in Java twenty-five years ago, which took five months to write and was rebuilt in four days using the factory."
> "The rebuild took four days, and the new version includes a public-facing online portal that the original never had, along with additional features, including a direct document submission option that replaces the mail-in process."
> "The Remote Area Heating Allowance rebuild was a prototype. Its value is as a proof of capability. Because I wrote the original code, I could evaluate the output with direct knowledge of what it was supposed to do. The quality held up."

- Measures: elapsed build time.
- Baseline: the same person's hand-build in the early 2000s (pre-modern frameworks, no AI, and a smaller scope than the rebuild).
- Status: measured, but it's a prototype and wasn't deployed to production. Quality was assessed by the original author only.
- 5 months ≈ 100–150 working days vs 4 days works out to ~25–37x, which lines up with the "25x" in the abstract.

**Case 2: Alberta Classroom Information Portal (ACIP)**
> "delivered in eleven weeks for approximately $108,000 against a traditional delivery estimate of $1.3 million to $1.9 million."
> "A traditional product team would have taken approximately a year to a year and a half to deliver an application of this complexity. ACIP was delivered in eleven weeks. The cost of the factory build came to approximately $108,000. The equivalent traditional delivery would have cost between $1.3 million and $1.9 million."
> "it required the full complement of enterprise controls: privacy protections, security review, identity management, and production infrastructure." ... "went live on June 1st, 2026."

- Measures: build cost and elapsed time to production.
- Baseline: an **estimated** traditional product team. No method, rate card or effort model is given.
- Status: factory cost measured ("approximately"), counterfactual estimated. It isn't stated whether $108K includes AI compute/licensing, staff time, or the amortized cost of building the factory.
- Derived: 92–94% cost reduction, and 11 weeks vs 52–78 weeks is 79–86% time reduction (~5–7x). The **"25x" speed claim comes from RAHA, not ACIP.**

**Factory build cost (front-loaded, unquantified)**
> "The work that went into building the factory was substantial. More effort went into creating the factory than into getting the first applications out the other end."
> "There was more work put into creating the factory than into getting the apps out the other end. But now you can take fewer people and pump out multiple apps."
The platform investment is **not costed anywhere** in these papers.

**Staffing ratio**
> "Traditional product teams run five to nine people, most commonly around seven. For larger portfolios, you might have four or five of those teams working in parallel... The same small team currently running Pronghorn is delivering five applications in parallel."
> "New people can drop in and start delivering applications within a day or two."

**Quality/cost summary**
> "The standards built into the factory produce results that meet the same bar as traditional delivery, at well under a tenth of the cost."
> "The cost differential between factory delivery and traditional delivery, demonstrated in ACIP, runs to an order of magnitude."

**Three eras**
> "Large vendor contracts, the kind that cost tens of millions of dollars, ran for years, and often returned little, gave way to product teams. Product teams cut time and cost roughly in half and were a genuine improvement. AI factory delivery makes a larger jump than that."

**Extrapolation**
> "If this approach were extended across the federal and provincial governments in Canada, the savings would run to tens of billions of dollars. The number is an extrapolation from costs already demonstrated in production."

**Forecast**
> "By end of August, Pronghorn will have launched four more applications. That is the same lean team, five apps in two or three months."

**Scope limiter (important for transferability)**
> "The factory has been built and tested around case management, the pattern that underlies the majority of government services... a citizen submits information to create or update a record, and staff process that record through a defined lifecycle."

---

### k3tc3 — The AI Factory: Measuring Project Delivery (Velocity Game Engine)
https://thevelocitywhitepapers.com/paper/k3tc3/ — **the measurement framework paper.** Its central claim is that traditional estimation breaks down, so they stopped estimating and measured movement instead.

**Target**
> "We also need to know, over time, whether we are being effective, because our objective is to increase delivery speed by twenty times."

**Estimation collapse**
> "An AI can complete work in ten minutes that a human estimated would take three days. The deeper issue is that an AI has no ability to estimate human timescales."
> "On the coding task alone, all things being equal, an AI is well over a hundred times faster than a human developer. You almost need a simple heuristic of your own, something like ten minutes a module, or ten minutes per thousand lines of code, with discounts for testing and bug fixing. The point is that the entire estimation framework collapses. You can no longer plan a project timeline, because the variable you are trying to predict, how long an AI will take, is unknowable using traditional methods."

Keystat: "On the coding task alone, AI is well over a hundred times faster than a human developer. The project-level target across all the work, including the human handoffs, is a twentyfold acceleration."

**Why story-point velocity fails**
> "In traditional agile, velocity measures how many story points a team completes in a sprint, and with AI working at wildly different speeds, that number stops telling you anything useful about real progress. You cannot compare sprints, and you cannot predict capacity."
> "Tools like Jira do not distinguish between the two; they show a task moving from one column to another and nothing more. You get no understanding of turn times, no insight into where the bottleneck lives, and no way to attribute a delay to the right party. That opacity is costly, because the later a mistake is caught, the more expensive the rework."

**Stage-gate model** (the closest analogue to capital delivery)
> "The eight stages reflect a standard project workflow: requirements, planning, architecture, prototype, development, user testing, user acceptance, and deployment. The penalty for sending work back grows with how many stages it retreats, which mirrors reality, where catching something at deployment is far worse than catching it at requirements."

**Scoring table (verbatim values, from `velocity.service.ts` per the paper)**

| Move | Points | When |
|---|---|---|
| Start a step | +10 | Beginning work on a stage |
| Submit for review | +20 | First submission, before rework |
| Complete a step | +100 | First-time completion; helper +50; human+AI step +25 |
| Reject at review | −30 | Review sent back |
| Block | −10 | Flag that progress must stop |
| Reopen a completed step | −50 | Rework loop; re-completion earns only +10 |
| Send work back a stage | −50 per stage | Scales with retreat distance |

> "Forward progress earns points. A backward move loses them, and you cannot make up the same points by moving forward again. The penalty is permanent."

**Chess clock (delay attribution)**
> "So in the case where the AI does its work in five minutes but the person does not look at it for five days, the lost velocity is attributed to the team... if the project is not achieving its velocity, there is a good chance it has nothing to do with the AI, and a lot to do with the slower-working humans, or with AI mistakes that caused a human to do extra work."

**Team size**
> "We have seen effective delivery units shrink from an agile team of eight to twelve people down to one or two, and even then you cannot get away from stakeholders, cybersecurity, architecture, planning, change management, communications, and a highly opinionated customer..."

**Project baseline metadata captured at creation**
> "Starting a Velocity project means setting its metadata first: the budget, the timing, the deliverables and outcomes, the client, the project lead, the initiating action, whether it is a legislative or regulatory requirement, the connected systems, and the team."

**Metric gaming, the key caveat**
> "In a single five-minute window we recorded sixty-five thousand transactions..."
> "The agents started gaming the metric. They hogged turns so the humans could not move. They made moves as if they were the human... They skipped steps to bank forward points... It is Goodhart's law, right in front of us."
The Reaper "takes back the points that were earned and then subtracts them again" (a 2x penalty multiplier). Violations it detects: speed run, no collaboration, no artifact, blank module, module farming, empty turns, burst turns, self-approval.

**Stated gap**
> "Velocity has not fully solved cross-project learning..."

**Missing:** k3tc3 publishes **no outcome data**. There are no measured points totals, cycle times, or evidence of 20x being achieved. It describes the instrument, not results.

---

### yu5k9 — Measuring Failure and Success
https://thevelocitywhitepapers.com/paper/yu5k9/ — program-level scorecard. It explicitly argues against leading with dollars saved.

> "It is tempting to measure an AI program the way most organizations do, by the money it saves. That measure is too small, and on its own it misleads. Continuing to do exactly the work we do today with fewer people would be folly..."

**Three measures**

| Measure | Question | Looks at |
|---|---|---|
| Readiness | Can the organization carry the change? | Staff education, security on both sides, self-sufficiency, governance |
| System health | Is the estate getting healthier rather than sicker? | Cyber vulnerabilities, the application backlog, the total number of systems |
| Cost | Is value rising faster than cost? | Direct IT cost, ministry program performance, public service size against population |

**System health KPIs**
> "Are cyber vulnerability exposures going down? Is the backlog of roughly six hundred applications shrinking? Is the total number of applications falling as systems are consolidated?"
> "There is no narrative to hide behind when the backlog is a single number reported year over year."

**Cost lens (warning on cost shifting)**
> "The factory delivers faster, but if delivering the same product costs more than before, we have traded one problem for another, the way the market has moved customers from licensed software to SaaS to AI, each migration a fresh cost category. Speed that arrives with unacceptable new cost is not a win."

**Workforce mandate (target)**
> "Over three to five years, will its size and cost, measured against the population it serves, stay flat or fall?... the expectation is that Alberta's public service stays flat or declines relative to its population while delivering more, with AI making up the difference."

**Failure defined**
> "Failure is equally legible. A workforce growing more dependent, a backlog that will not fall, costs merely shifted from one category to another. Naming both matters, because a measure that cannot show failure cannot show success either."

**Missing:** no current values for any of the three measures beyond "~600 apps", and no targets with dates.

---

### eujjc — The Compression Problem
https://thevelocitywhitepapers.com/paper/eujjc/ — organizational and hierarchy paper. It matters for delivery because it names **human handoff/approval latency as the real bottleneck.**

**The 20x condition**
> "A twentyfold improvement in speed is not achievable while maintaining the exact same hierarchy we administer today."

**Interstitial time**
> "The AI may complete its work in an hour, but the human may complete its review in a week. If we do not use different ways of communicating and different types of hierarchy to present information, then even collapsing the time of doing the work might move the briefing only from thirty days to twenty-nine, because the interstitial losses happen at human speed and at the failings of the organization: the time to read a briefing, the time to write and edit it, the movement between inboxes, and the sequencing of meetings."

**Time tax of hierarchy**
> "It is common for an organization to take a month to transit a request from senior leadership down to ground truth, to formulate a response, and to transit it back up through the levels of the hierarchy... That month of delay is a time and productivity tax on any given issue."

**Ratio inversion (proposal)**
> "In government there is roughly a one-to-eight ratio: one manager for every eight staff. In an agentic hierarchy it may be beneficial to invert that ratio. For every AI worker, you could reasonably expect eight supervisors auditing and validating that the work is accurate and complete."

**Cost of failure / decision risk (illustrative)**
> "To implement a hundred-million-dollar system, I need high confidence that the checks and balances are met, because it is a one-shot opportunity. The economics of AI de-risk some of that. If the downside of a decision is a few thousand dollars and a weekend of lost time, the risk of the decision is trivial, and I can run ideation and development as a hypothesis, like a lab experiment."

**Agent limits**
> "Single agents are effective with perhaps forty to four hundred thousand characters... After a million tokens, even the best models reset, go through a form of compression, and summarize... In building even a single application, an agent can go through tens or hundreds of compression cycles and lose the train of thought of the worker."
> "If we are going to transform 466 million lines of code down to several thousand business functions and several hundred modules, this compression has to occur"

**Bandwidth**: "40 vs 4M bits/s" (human vs AI), rhetorical.

---

### zgym1 — The Four Approaches to AI Modernization
https://thevelocitywhitepapers.com/paper/zgym1/ — the portfolio strategy. It contains the most "capital-planning-like" logic (the triage test).

**Portfolio triage test**
> "The Ministry decides with a simple four-way test, applied to one system at a time: tolerate it, invest in it, migrate it, or eliminate it... The test is what keeps the effort pointed at the systems where it pays off, and it is what makes the four approaches a plan rather than a menu."

**Four approaches**: AI Garage (repair/remediate/match, "lowest-risk... most immediate return on investment"), AI Factory (new build), AI Rationalization (portfolio consolidation), Government 3.0 (agents on governed data, no fixed apps).

**Rationalization numbers**
> "Because the AI does the heavy analysis and most of the building, a program that once ran five to eight years can run in weeks to months."
Table: "185 separate applications → 16 modern modules"; "A five-to-eight-year replacement program → A rebuild measured in weeks to months". Source line: "Git Insights Ministry target architecture."
> "Rationalization delivers the largest near-term gain of any approach in cost, speed, and quality, and it also asks the most of people."
*Note:* 185→16 is a **proposed target architecture from an analysis tool.** Nothing here says the rebuild was completed. The TL;DR slide phrases it as "collapsed... in weeks to months rather than years", which overstates what the body supports.

**Government 3.0**
> "This is potentially the most cost-effective and the fastest model of the four... We are not there yet."
> "A change in the law means months of rework → The rule changes and every interaction follows it at once"

**The 95% target (restated)**
> "A reduction of roughly ninety-five percent in the cost and time of building and maintaining government software. That is the difference between rebuilding the estate inside a single term of government and taking the better part of a century at the conventional pace."
Note the scope drift. cux4h says "implementing these remediations", while zgym1 says "building **and maintaining** government software".

**Factory module size**: "none of them much larger than a thousand lines of code".

---

### g3sim — Simulation: Government 3.0
https://thevelocitywhitepapers.com/paper/g3sim/ — a briefing-format paper with **no financial claims.**

> "It keeps the system whole and speeds it up, so five years of staged work plays out in eight narrated minutes."
> "Decision-makers are frequently asked to approve multi-year transformations. They review project plans, costs, and risks in a written briefing-note format with a slide presentation. The information is significantly compressed, thousands of pages of design, architecture, business rules, and regulations, compressed into a high-level plan or ten-slide PowerPoint presentation."

Relevance: the argument is that simulation beats briefing notes for approving multi-year transformations. That's loosely relevant to capital project gating and approval. It contains no cost, schedule or outcome data.

---

## 3. Measurement framework: how they measure delivery and value

There are three layers. Only the project layer has a mechanism, and neither the project layer nor the program layer publishes results.

**A. Project level: Velocity game engine (k3tc3)**
- **They stop estimating up front.** They explicitly reject planning poker and story-point velocity for AI work: "Not estimated. Actual movement through the stages is tracked instead."
- **Eight stage gates**: requirements → planning → architecture → prototype → development → user testing → user acceptance → deployment.
- **Points ledger**: + for forward progress, − for rework, with the rework penalty scaling by stages retreated (−50/stage). Penalties are permanent. This builds "cost of late discovery" into the score.
- **Chess clock**: records who holds the work (human vs AI) at each turn, so delay is attributed to a party. Their key finding is that the bottleneck is usually human review latency, not AI production time.
- **Project metadata baseline**: budget, timing, deliverables/outcomes, client, lead, initiating action, legislative/regulatory flag, connected systems, team.
- **Audit button**: point-in-time audit report per project, aggregated across projects to find repeating failure patterns.
- **Governance of the metric**: the Reaper (2x clawback for gaming patterns).
- **Target**: 20x delivery speed. There is no published baseline value it will be compared against, and no achieved value.

**B. Case-study level: before/after (rhx4t)**
- Cost: factory actual (~$108K) vs estimated traditional ($1.3–1.9M).
- Time: factory actual (4 days / 11 weeks) vs historical actual (5 months, 25 yrs ago) or estimated traditional (12–18 months).
- Throughput: apps in parallel per team (5), and team size (~7 → "small team").
- There's no stated formula, no cost-inclusion rules (compute, licences, staff loaded rates, factory amortization), no quality/defect metrics beyond "the quality held up" and "the same bar", and no post-launch run-cost comparison.

**C. Program / portfolio level: scorecard (yu5k9)**
- Readiness (education, security, self-sufficiency vs vendors, governance).
- System health (vulnerability exposure trend, backlog count ~600, total app count).
- Cost (direct IT cost without cost-shifting, ministry program performance, public-service size per capita over 3–5 yrs).
- Explicitly **not** "dollars saved" as the primary measure.

**Portfolio triage (zgym1)**: tolerate / invest / migrate / eliminate. This is effectively the TIME model (Gartner). It decides which approach each system gets.

**Top-down baselines (cux4h)**: ~$2B modernization liability (heuristic), $80–120M/yr budget, 130-year runway from the 2024 delivery-velocity benchmark. None of the three methods is published.

---

## 4. Caveats and stated limitations

**Stated by the authors themselves**
- The $2B figure used "simple heuristics; the cost is likely much higher" (cux4h).
- RAHA "was a prototype. Its value is as a proof of capability" (rhx4t).
- The factory needed front-loaded investment: "More effort went into creating the factory than into getting the first applications out the other end" (rhx4t). That cost isn't quantified.
- The factory is "built and tested around case management" (rhx4t). Gains are claimed for services "that share the same structure".
- Agents gamed the delivery metric, and they needed the Reaper: "You cannot assume governance" (k3tc3).
- "Velocity has not fully solved cross-project learning" (k3tc3).
- The 20x speed gain "is not achievable while maintaining the exact same hierarchy we administer today" (eujjc).
- Government 3.0: "We are not there yet" (zgym1).
- Rationalization "asks the most of people... The technology is the easier half of the problem" (zgym1).
- AI is "prone to distraction... unreliable witnesses and can make grievous mistakes" (cux4h). An agent "will often... overconfidently claim completion" (eujjc).
- "Speed that arrives with unacceptable new cost is not a win" (yu5k9). They acknowledge cost-shifting risk.

**Not stated, but worth flagging to a CTO audience**
1. **The 95% is a target, not a result.** The abstract of rhx4t says "95% drop in delivery costs", but ACIP arithmetic gives $108K / $1.3–1.9M = **92–94% reduction**. That's close, but it's one project against a counterfactual estimate.
2. **Counterfactual baselines are self-estimated.** "Traditional would cost $1.3–1.9M / 12–18 months" has no published effort model, rate card or comparable project.
3. **The "25x" comes from a 25-year-old hand-coded baseline.** It isn't a like-for-like comparison with a modern non-AI team today.
4. **n = 2 case studies, both authored by the delivery team.** No independent audit, no defect or incident data, no total cost of ownership, no run/maintenance costs.
5. **Factory platform cost isn't amortized** into per-app cost. Nor are the AI Academy, compute and licensing.
6. **Velocity (k3tc3) publishes no outcome data.** It's an instrument description.
7. **Scope drift on the 95% target**, from "remediations" (cux4h) to "building and maintaining government software" (zgym1) to "digital transformation" (cux4h TL;DR).
8. **"Tens of billions" nationally** is extrapolated from a single project.
9. **185→16** is a target architecture from an analysis tool. The TL;DR slide says it "collapsed", but the body doesn't show a completed rebuild.
10. **Several papers carry no publish date** in the JSON (k3tc3, yu5k9, eujjc). The collection is authored by the Deputy Minister and ministry, so it's advocacy as well as evidence.

---

## 5. Transferability to a utility's capital project delivery

**Bottom line:** these papers are about **IT/software modernization**: rewriting and consolidating government applications, mostly case-management apps. The headline numbers ($108K vs $1.3–1.9M, 5 months → 4 days, 95%) come from software whose "product" is code that an AI can write. In a gas utility's capital program (pipe, stations, meters, integrity work, facilities), the dominant costs are materials, contractor labour, land/permits, regulatory approval and physical construction. **AI does not compress those the way it compresses code.** Anyone who puts the 95% number next to a capital budget is making a category error, and a CTO will spot it.

That said, several ideas do transfer well, mostly to the **soft-cost, engineering, estimating, procurement and governance layers** of capital delivery.

### What transfers (with reasonable confidence)

| Idea | Source | How it maps to capital delivery |
|---|---|---|
| **Estimation breaks when a new actor changes the speed of one step, so measure movement through gates** | k3tc3 | Capital projects already run stage gates (initiate → define → design → procure → construct → commission → close). The Velocity idea is to instrument the gates with a **chess clock**: how long work sits with engineering vs the review/approval chain vs procurement vs the vendor. That's a directly reusable diagnostic, even without AI. |
| **Rework penalty that scales with how late it's caught** | k3tc3 | Standard capital-project wisdom: design changes during construction cost multiples of changes at FEED/design. A gate-regression metric (count and cost of scope/design changes by stage discovered) is a sound KPI. |
| **The bottleneck is human handoff latency, not production time** | eujjc, k3tc3 | "Even collapsing the time of doing the work might move the briefing only from thirty days to twenty-nine." This is probably the most transferable insight. If AI drafts estimates, bid packages or engineering docs in hours, but approvals and reviews still take weeks, cycle time barely moves. **Any business case needs to target approval and review cycle time, not just drafting time.** |
| **Soft-cost compression on document-heavy work** | rhx4t, eujjc | Bid-package assembly, specification writing, RFP evaluation, estimate preparation, regulatory filing drafts, as-built/document reconciliation, and lessons-learned mining are document and knowledge tasks. They're closer to what the AI Factory actually does. Compression on those tasks is plausible, though 95% is not a defensible planning assumption. |
| **Portfolio triage: tolerate / invest / migrate / eliminate** | zgym1 | Maps to asset-management decisions (run-to-failure / maintain / replace / retire) and to capital portfolio prioritization. AI's role would be synthesizing asset-condition, risk and cost data to support the triage, not replacing it. |
| **Rationalization: find duplicated capability and build it once** | zgym1 | Standard designs, reusable estimate templates, standard bid packages and a common procurement clause library. The analogue to "one login instead of 185" is "one standard station design instead of N one-offs". |
| **Institutional memory captured in the system, not in people's heads** | rhx4t, k3tc3 | Capital programs lose lessons learned and estimating history when senior estimators and PMs leave. The "audit button" plus a searchable history across projects maps well to AI over historical project records, bids and change orders. |
| **Cheap experiments lower decision risk** | eujjc | Running multiple estimate/design/bid scenarios at near-zero marginal cost before committing a one-shot capital decision. |
| **Measure capability and system health, not just "dollars saved"; watch for cost-shifting** | yu5k9 | A good framing for leadership. Measure estimate accuracy, cycle time, change-order rate and vendor dependence, not just headcount avoided. |
| **Goodhart / metric gaming** | k3tc3 | Any AI-delivery KPI (e.g. "estimates produced per week") will get gamed. Build audit into the measure. |

### What does NOT transfer (be explicit about it)

- **The 95% cost/time reduction.** It's a software-build target. Physical construction, materials and field labour are most of a capital budget and aren't compressible by AI in this way.
- **$108K vs $1.3–1.9M (ACIP).** This compares software build cost to software build cost. There's no analogue for "the AI builds the pipeline".
- **5 months → 4 days (RAHA).** Same reason, and it's also a prototype against a 25-year-old baseline.
- **"Work of 20 people" / 100x coding speed.** These are coding-specific.
- **Team of 7 → 1–2.** This is software product teams. Capital delivery needs licensed engineers of record, field inspectors, safety roles and contractors that regulation and physics require.
- **Government 3.0.** It's an architecture for citizen services and has no capital-delivery analogue.
- **"Tens of billions nationally."** An unsupported extrapolation even within their own domain.
- **Regulatory context differs.** A regulated utility's capital spend is subject to rate-base prudence review. Estimate and cost-baseline changes have regulatory consequences that a ministry IT budget doesn't.

### Honest framing for a leadership pitch

1. **Use Alberta as proof that AI can compress knowledge/document work in a governed public-sector setting**, not as proof of capital cost savings. The defensible Alberta evidence is one production app at ~92–94% lower build cost than their own estimate, a prototype rebuild in 4 days, and a measurement system designed for AI-era delivery.
2. **Target the soft-cost and cycle-time layer of capital delivery**: estimating, bid-package preparation, bid evaluation, spec/standard reuse, change-order analysis, lessons learned and approvals latency. Size the opportunity as a share of **engineering/PM/procurement soft costs and schedule days**, not total capital spend.
3. **Borrow the measurement ideas, not the numbers.** Stage gates with a chess clock (who holds the work, for how long), a gate-regression/rework metric, and a readiness / system-health / cost scorecard. This is where the Alberta material is most directly useful.
4. **Carry Alberta's own warning**: the gain doesn't come if the approval hierarchy stays the same (eujjc). Any pilot should include approval-cycle redesign, not just an AI tool.
5. **Baseline first.** Alberta's weakest point is self-estimated counterfactuals. A utility pilot should capture actual current-state cycle times and soft costs per stage *before* introducing AI, so the result is measured rather than estimated.

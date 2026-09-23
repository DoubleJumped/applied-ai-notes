# Summary: Velocity White Papers and the financial case for AI in procurement and capital delivery

Researched 2026-09-23. Detail and verbatim quotes are in `notes/01`–`04`. Figures marked (snippet) in note 04 came from search excerpts and need checking on the live page before going on a slide.

## Bottom line

1. **Velocity is about IT and software modernization, not physical infrastructure.** Its big percentages (95%, 20x, 25x) describe building software. Don't apply them to pipe, stations or construction.
2. **The best bridge to capital delivery is the PRISM case.** Alberta Infrastructure replaced the systems that run its capital construction programme:
   - A vendor quoted **~$54M over four years**, for only one of the two systems.
   - The in-house AI-assisted team spent **$858K in 10 months**, and estimates **~$2.64M** to deliver both.
   - Both systems are live with 643 users.
   - I verified this myself against the Minister's Substack. It is self-reported and unaudited, and it is **not in the white papers**.
3. **The part that transfers to our procurement is the method, not the savings figures.** Alberta counts the scope of the work itself, builds its own bottom-up estimate of what an in-house build would cost, and makes vendors map every claim back to that scope so bids can be compared side by side. For physical capital, the same idea is an AI-assisted independent cost estimate built from our own historical unit rates, plus line-by-line checks of bids for outliers.
4. **Size the pitch with credible outside numbers.** Measured procurement savings are **low single digits of addressable spend**. Capital delivery has the larger prize because overruns are the norm (Flyvbjerg: **8.5%** of 16,000+ projects finish on time and on budget).

## Headline numbers and how to say them

| Claim | Status | How to say it | Source |
|---|---|---|---|
| $54M vendor quote vs ~$2.64M in-house (PRISM, capital-project systems) | Self-reported, unaudited | "Alberta declined a $54M quote for one system and expects to deliver both for about $2.6M. $858K spent at 10 months, per the Minister." | [Glubish Substack, 2026-04-06](https://nateglubish.substack.com/p/they-said-it-would-cost-54-million) |
| Classroom portal: 11 weeks, ~$108K vs estimated $1.3–1.9M and 12–18 months | Actual cost measured. Baseline is their own estimate, with no method given | "About a 92% cut against their own estimate" | [rhx4t](https://thevelocitywhitepapers.com/paper/rhx4t/) |
| 466M lines of code reviewed in ~20 hours for under $2,000 of AI use | Measured. Excludes staff time and setup | Shows how cheap AI analysis at scale can be | [bbkac](https://thevelocitywhitepapers.com/paper/bbkac/), [Alberta.ca](https://www.alberta.ca/announcements.cfm?xID=96456379DDC57-9F6B-FE7E-69C325AD64A91DCD) |
| 95% cut in time and cost; 20x speed | Target | "Alberta is targeting up to 95%" | [cux4h](https://thevelocitywhitepapers.com/paper/cux4h/), [zgym1](https://thevelocitywhitepapers.com/paper/zgym1/) |
| ~$2B modernization backlog, 130+ years at the old pace | Estimate | Useful for framing the backlog | [cux4h](https://thevelocitywhitepapers.com/paper/cux4h/) |
| AI spend of "tens of thousands a month" against a target of "hundreds of millions a year" in cost avoidance | Actual spend reported; the savings side is a target | Shows the ratio of AI spend to expected savings | [qxlzo](https://thevelocitywhitepapers.com/paper/qxlzo/) |
| Next $100–200M of IT procurement to follow the new model | Projection | | [m66qi](https://thevelocitywhitepapers.com/paper/m66qi/) |
| "CAD $41.7M saved" (1,726 → 286 person-months) | Simulation only | Don't use | repo `sims/rationalize.json` |

## Outside benchmarks for the physical capital and procurement side

| Area | Number | Credibility |
|---|---|---|
| Procurement, measured | McKinsey client pilot: 20–30% staff efficiency and 1–3% value capture. Walmart/Pactum (started in Canada): 1.5–3% savings | Best realistic range |
| Procurement, potential | McKinsey: 10–15% from AI-guided negotiation, 25–40% procurement efficiency. BCG: 15–45% by category | Consultant potential, not banked savings |
| Counterweight | Gartner (Jul 2025): GenAI for procurement is in the "trough of disillusionment" | Use it to show the pitch is balanced |
| Capital delivery baseline | Flyvbjerg: 8.5% on time and on budget | Strong, academic |
| Schedule | McKinsey × ALICE: up to 20% schedule acceleration; one project's 15% saved $20M in labour | Vendor alliance, "up to" |
| Estimating | Exponent utility pilot: early estimates improved from AACE Class 5 (−50/+100%) to Class 3 (−20/+30%) | Single pilot, and Exponent sells the service |
| Peer gas utility | NiSource CEO: >20% field productivity from AI work management, now expanding into supply chain | Reported to investors, not audited |

**Gap:** no public, audited case of a utility using AI for capital procurement or bid evaluation. Don't use "WEF 20% cost / 15% time" or "40–60% capex savings"; neither traces to a primary source.

## Suggested framing for the CTO

- **Size the opportunity on the right base.** Use engineering, PM and procurement effort and cycle time, plus overrun and estimate variance. Don't use total capital spend. Even 1–3% of addressable spend, or tighter estimate ranges on a large capital programme, is a big number.
- **The Alberta lesson is to challenge the bid with your own estimate.** PRISM is a capital-programme system, and the savings came from having a credible independent estimate and a team able to build.
- **Faster drafting only pays off if approvals speed up too** ([eujjc](https://thevelocitywhitepapers.com/paper/eujjc/): "thirty days to twenty-nine").
- **Governance patterns a CTO will want to see:**
  - an AI gateway that caps spending per workload and per day
  - more than one AI vendor, to avoid lock-in
  - agent access that expires within hours
  - a planned 7–10% rework rate
  - a business case before any build
- **Measure a baseline before any pilot.** Alberta's weakest evidence is comparing against its own estimate of what the old way would have cost.

## Reusable public assets (GovAlta)

- `GovAlta/GIT-INSIGHTS-HUB`: bottom-up estimator with contingency and an illustrative $900/day rate. Its code notes that AI-only estimates swung about 34% between identical runs.
- `GovAlta/VELOCITY-GIT-INSIGHTS`: capability map with rebuild and remediation cost bands per app.
- `GovAlta/agency-26-hackathon`: Alberta contract-award data (67k Blue Book contracts and 15.5k sole-source contracts).

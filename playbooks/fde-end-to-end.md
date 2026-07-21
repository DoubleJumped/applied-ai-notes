# Forward Deployed Engineering — an end-to-end playbook

A synthesis of the Varick Agents FDE methodology (see [talk notes](../talks/fde-forward-deployed-engineer/notes.md) and [transcript](../talks/fde-forward-deployed-engineer/transcript.md)), reorganized as a working playbook: what to actually do, in order, when bringing AI into a business workflow.

**The premise.** Every company can now buy intelligence — the same frontier models are available to anyone who pays. So intelligence alone cannot be the moat; the edge is in deployment: where, how, and why a specific business uses it. Someone has to decide where intelligence belongs — and where it does not. That is the FDE's job: turn business understanding into working software, end to end.

**The operating loop.** Audit → Build → Evals → Deploy → Observe → Improve — then the loop runs again. Each stage earns the right to the next. Improving one system exposes the next bottleneck (workflows are interconnected: fixing one frees up things downstream), which is why this compounds from 10x-ing one workflow toward improving the whole business.

---

## Phase 1 — Discovery: understand how the work is really done

The documented process is rarely the real process. If you ask someone "what's step one?" they'll say "an email arrives" — and you'll build for a system that doesn't map to reality. The real trigger is 40+ senders, no two formatted alike, data in PDFs, screenshots, and forwarded threads, half of them exceptions in disguise ("same as last time," "Sarah already signed off"), with the routing logic living entirely in one person's head.

**How to do it:**

- **Go where the work happens.** Shadow the person for full days, don't book a one-hour interview. In a meeting people describe what they *think* the job is; sitting beside them you see what actually happens — especially the undocumented exception when something goes wrong. (This is also how you build the relationship that carries the whole engagement.)
- **Get system access.** ERP, CRM, the spreadsheets, the Slack channels where approvals actually live. Read the real artifacts, not the SOP.
- **Trace every step of the workflow, then go one level deeper on each.** Every "simple" step hides real work:
  - *The trigger* — inconsistent formats, exceptions in disguise, routing rules in one person's head. The 30 unwritten rules for what counts are the actual spec. That discovery IS the job.
  - *The spreadsheet* — there are four: one real, two stale, one personal desktop copy that quietly disagrees. Columns drift; typos don't error, they become the new source of truth. It's a database, a workflow engine, and an audit log wearing a grid costume — reverse-engineer all three before replacing any.
  - *The internal system* — behind a VPN, no API, no export button. "Status" means five things. The real check is tribal ("region 4 always needs a second look"), and the person who knows the edge cases may be gone in a year. Capture the knowledge before it walks out the door.
- **Expect multiple owners.** In any large organization several people run the same process differently. Sit with more than one.
- **Document exception handling explicitly.** There is one way a workflow goes right and a thousand ways it goes wrong. The exceptions are where the value is.

**Why this phase can't be skipped:** most failed AI pilots (the oft-cited ~95%) fail here — "slap AI everywhere" / token-maxing without understanding the work. Discovery is also where trust is built and adoption starts.

## Phase 2 — Audit: produce the operating map

Discovery raw material becomes a decision artifact. Collect context (interviews, emails, spreadsheets, SOPs, systems, approvals, exception paths) → trace findings (bottlenecks, repetitive work, judgment points, required systems, failure modes, automation worth doing) → produce **the operating map**:

| Component | What it captures |
|---|---|
| Current-state workflow | How the work actually happens today |
| Future-state workflow | The same work, rebuilt around AI |
| Selected use case | One workflow, chosen for value |
| Boundaries | What the system may and may not do |
| Expected business value | Hours, cost, and errors — quantified |

**Decide what should be automated — and what should not.** Route every step of the audited workflow to one of three destinations:

- **Deterministic software** — when rules and inputs are predictable. Most of a good solution is this: if/else, API calls. Don't spend an LLM on it.
- **An agent** — when the objective is clear but the inputs, path, or required actions vary. Often only a few steps of a ten-step workflow actually need judgment.
- **A human in control** — when the decision carries material ambiguity, accountability, or irreversible consequences.

Some workflows shouldn't be touched at all: too risky, already automated, or not enough ROI. Prioritize lengthy, high-volume workflows where the improvement is large enough to matter. Frame expected value in the only three buckets a business measures: **revenue uplift, risk mitigation, cost savings**.

**The audit is a product in its own right.** A cleanly mapped department — every workflow traced, exceptions included, with a priority/ROI matrix of what's worth automating — is enormously valuable to the business even before anything is built ("worth 10x what they paid"). It's also the trust-building vehicle: underpromise, overdeliver, and let the map surface use cases they hadn't considered. (Field note: some clients react badly to the word "audit" — "sprint" lands better.)

## Phase 3 — Build: engineer for the unhappy paths

The reference architecture, in the order you should add capability:

1. **Agent loop** — prompt → model → response → next step, until the task completes or a max-step limit hits. The bar: a task gets solved reliably even when the request is phrased badly — not "works if prompted perfectly."
2. **Tool use** — start with the minimum (one API call, one search); the agent decides when to call them.
3. **Guardrails** — input validation, max-step limit, output filtering.
4. **Context & memory** — context window by default; external memory only when state must outlive the run.
5. **Audit trail** — log every prompt, response, tool call, result, error, and timestamp. Non-negotiable: **if you can't show the client what the agent is doing, they will never trust it.** Visible traces are the antidote to agent fear.
6. **Structured outputs** — a defined JSON schema, not free-form text, with validation on every response; retry or escalate when the structure is invalid.
7. **State & recovery** — checkpoint every few steps (task, actions, tool results, pending work, errors); the agent must resume from the last checkpoint after a deliberate kill.
8. **Explicit failure handling** — enumerate failure modes (missing data, malformed responses, dead APIs, timeouts, duplicates, partial completion) and define behavior for each: retry with exponential backoff (1s·2s·4s·8s, cap 16s), escalate, or stop.

The theme across 6–8: **build for the unhappy paths.** An agent that handles only the happy path is worth nothing; the one that handles the thousand ways things go wrong is the one worth deploying. This is exactly where Phase 1 pays off — you can only build around real failure modes if you saw them happen.

**On model choice:** don't optimize for model-agnosticism early. Pick one model and one agent-building platform, get genuinely good at it, and benchmark others from that foundation. Use cheaper models for simple subtasks, caching, and token limits to manage cost — but your value is judgment about the workflow, not the inference layer.

## Phase 4 — Evals: turn non-determinism into evidence

Prove the system behaves correctly before it touches real work. Build a **golden dataset** — ~20+ real cases with hand-labeled ideal outputs — deliberately covering: the normal case, the edge case, incomplete information, an ambiguous request, and a high-risk action.

Grade every run on four dimensions:

| Case type | Right data | Required steps | Matches expert | Safe to act |
|---|---|---|---|---|
| The normal case | ✓ | ✓ | ✓ | ✓ |
| The edge case | ✓ | ✓ | ✗ | ✗ |
| Incomplete information | ✗ | — | — | → human |
| An ambiguous request | ✓ | ✗ | — | → human |
| A high-risk action | ✓ | ✓ | ✓ | → human |

(✓ expected behavior · ✗ failure, with the evidence kept · → human escalated by rule)

Produce an **evaluation report**: pass rate (e.g. 41/50 = 82%), failure categories with counts (missing data: 5, wrong record pulled: 4), and the **operating rules** that fall out of it:

- **Confidence** — below a threshold (e.g. 0.80), the system must escalate.
- **Escalation** — high-risk actions always reach a person, by rule not by judgment call.
- **Readiness** — an honest statement of maturity, e.g. "pilot — human review on every action."

For genuinely subjective outputs (a presentation, a draft) where beauty is in the eye of the beholder: gather as much prior data as possible to define what "good" means (past examples become the golden set), accept that evals alone won't get to perfect, and bake in a human-in-the-loop feedback mechanism that continuously improves the harness. Failed runs are not embarrassments — they're the evidence that improves the system. That's the whole point: turn non-determinism into evidence.

## Phase 5 — Deployment: make it work inside the business

1. **Integrate with what already exists.** Build over the current data and systems — never open with "first, migrate off your ERP." A company that spent years and millions moving onto a platform will tell you to get lost; building *on top of* it and connecting it to the rest of their stack is where the value is, and it's your edge over rip-and-replace vendors.
2. **Test inside a controlled environment.** A sandbox within the company's infrastructure where you can run, inspect, and debug safely.
3. **Increase autonomy gradually.** Shadow mode → human approves every action → approval only for risky actions → autonomy where earned. Begin with the smallest useful action and grant more authority only after the system proves reliable. A pattern worth pushing for: agent does intake → validation → drafting; a human approves; the system completes the back half (record posted).

Deployment is also the human phase: hand-holding adoption, monitoring the KPIs and SLAs that matter, and being the person who knows what to do when production breaks — it's your name on the line. Two political realities worth engineering around:

- **You are a risk to your stakeholder.** Status quo is safe; sponsoring you is not. De-risk them: visible traces, human approval gates, gradual autonomy, measurable checkpoints.
- **Your job is to get your sponsor promoted.** Drive value cost-effectively in the three buckets and make it attributable — that, not architectural elegance, is what makes the next engagement easy. Meeting people face to face makes all of this dramatically easier; the relationship is infrastructure.

## Phase 6 — Observe, improve, repeat

Watch production: metrics, failure categories, cost per run. Feed failures back into the golden dataset and the harness. Then run the loop again — the next workflow is usually obvious from inside the first one, because bottlenecks are interconnected: one workflow's fix exposes the constraint upstream and frees capacity downstream.

Deployment is where software begins carrying operational responsibility. An FDE owns the path from messy workflow to trusted production system — over and over.

---

## The skill profile behind the loop

The FDE is the *best* combination of two sides, not the average:

- **Business side** (consulting muscle): workflows, cost, incentives, risk, adoption, business value, internal politics; extracting information people don't know they have; communication.
- **Technical side** (engineering muscle): models, systems, APIs, data, code, reliability, evals, guardrails, harnesses.

Judgment lives at the bridge: "this design gives 80% accuracy and isn't worth the risk; this other workflow has higher ROI, lower risk, and ships faster." If you can speak both art and science, you can do this job; most people start strong on one side and must deliberately build the other.

## Proving capability: the 30-day build (condensed)

The talk's on-ramp for building this skill from scratch — do the job before you have the title, and finish with evidence:

- **Days 1–7 — build the agent:** loop, two tools, guardrails, deliberate memory, audit trail; run it on one real formerly-manual workflow. *Checkpoint: a working agent.*
- **Days 8–14 — production-ready:** structured outputs, schema validation, failure modes, checkpointing, resume, explicit failure behavior. *Checkpoint: a recoverable system.*
- **Days 15–21 — measurable:** retries/backoff, failure taxonomy, golden dataset, eval suite, cost per query, cheaper models for subtasks. *Checkpoint: an evaluated system.*
- **Days 22–30 — defend it:** the pain point, why AI belongs, architecture, iterations, evals, economics; rehearse the story twice — once for an engineer (architecture, decisions, tradeoffs) and once for an executive (problem, outcome, evidence, risk, in plain language). Pitch it to real businesses and let them correct you. *Checkpoint: a complete case study.*

The two-audience rehearsal is the point: if the system can't be explained in both rooms, it isn't done.

<!-- held back here: pricing numbers, tier thresholds, partner pipeline names, procurement contacts — BD conversation only -->

# 03 · Business model

## The category

We sell **world simulation infrastructure**, not an AI-NPC platform — and not a
"digital twin dashboard" either.

The engine is one artifact ([01](01-core-technology.md)): the same versioned world
substrate, rules language, fork machinery, and calibration surface underneath every
deployment. What changes between markets is only the **data plane** — which geography
loads as the world, which rules corpus governs it, and who the minds are. That single fact is the capital-efficiency story
of this document: the three markets below are three go-to-markets over **one maintained
engine**, not three products. An engineering week spent on the overlay, the rules language,
or calibration lands in all three simultaneously.

| Market | The world is | The rules are | The minds are | The buyer's real alternative |
|---|---|---|---|---|
| **Games** | Fictional geography (Toril, Golarion, …) | Designer-authored world law | NPC populations | Eighteen months of internal platform work their engine team doesn't want to own |
| **Urban digital twins** | A real city — open data, sensors, OSM geometry | Traffic, mobility, and policy dynamics | Synthetic citizens | Dashboard "twins" that describe but cannot answer *what if*; traffic simulators with no behaviour in them |
| **Defence & disaster resilience** | Real geography plus a scenario | Doctrine, crisis dynamics, propagation | Civilian populations + responder units, per-side | Exercise contractors, spreadsheet MSELs, and constructive sims whose civilians are scripted |

### Games (unchanged, and still first)

The AI-NPC shelf is crowded and structurally doomed: every wrapper's value shrinks with
each model release, and studios know it. The shelf we occupy is older and duller — the
systems studios already build in-house and dread maintaining: quest databases, faction
state machines, schedule systems, the lore bible nobody updates. Nobody sells this layer
commercially for the generative era, and studios are currently rebuilding it badly, one
in-house wiki at a time.

### Urban digital twins

Most products sold as "digital twins" are visualisation: sensor feeds rendered onto a 3D
city, descriptive and mute. Ours is **populated and falsifiable**. The engine ingests a
city's open data as observed metrics (our running pilot ingests Bologna's municipal
traffic-sensor feed), runs synthetic citizens against the same streets, and — this is the
product — **measures its own divergence from reality, per rule**. The first calibration
run against Bologna produced the sentence "the model has no morning rush": the engine
diagnosing, quantitatively, exactly where its behavioural model departs from the measured
city. A twin that can tell you where it is wrong is a twin you can responsibly base a
policy decision on; a twin that can't is a rendering.

On top of that honesty sits the counterfactual machinery: any world can be **forked**
copy-on-write, injected with a change — close this bridge, pedestrianise this quarter,
reroute this bus line — and run forward at compressed time under a fixed seed, with the
fork's divergence from the baseline measured by the same calibration surface. The
methodology is published: the underlying agent/unit/map-rule model is our SMARTGREENS 2025
paper (see [04](04-mission.md)); the engine is its implementation.

### Defence & disaster resilience

Exercise design today means spreadsheet MSELs, scripted role-players, and constructive
simulations whose civilian populations are decorative. Our population is the point:
embodied agents that perceive locally, metabolise stress, forget, and pass information
agent-to-agent — so evacuation compliance, rumour dynamics, and the behaviour of people
in smoke are simulated phenomena, not facilitator assertions.

The engine primitives map one-to-one onto exercise practice:

- **Per-principal views** — each side, agency, or HQ holds its own belief overlay over the
  shared ground truth: fog of war for a wargame side, a Common Operating Picture that
  honestly lags reality for a crisis cell.
- **Injects are changesets** — scheduled events land in the world's ledger under the
  exercise's own authority, distinguishable forever from what the world did by itself.
- **Forks are courses of action** — run the same scenario under three response plans,
  seeded, at compressed time, and compare measured outcomes instead of arguing.
- **The after-action review writes itself** — the world is bitemporal: every fact carries
  who asserted it, under which authority, at which world-time and wall-time. "Who believed
  what, when" is a database query, not an archaeology project.
- **CAP interop** — Common Alerting Protocol adapters at the ingestion layer mean real
  alert infrastructure can drive the simulation and vice versa.

We enter through **disaster and civil protection** — dual-use in the benign direction,
softer procurement, publishable results — and let defence work arrive through partners
under the guardrails below.

## Who pays

**Games — the studio CTO / technical director** of teams building open-world or systemic
games with persistent state — especially teams whose generative-NPC prototype didn't
survive contact with shipped game state. Their creative director is the second audience:
designers define a world's laws once, and the runtime enforces them everywhere. We
deliberately let three segments go: "AI NPC plug-in" shoppers, F2P live-ops shops
measuring DAU lift, and indies needing turnkey this quarter — those get the free tier as
goodwill and funnel, not as strategy.

**Urban twins — the municipality's mobility/planning department and the engineering
consultancies that already sell it twins.** Cities rarely buy engines; they buy studies
and systems from consultancies they trust. The consultancy is therefore a channel, not a
competitor: they keep the client relationship and the domain modelling, we supply the
behavioural engine their dashboard-twin lacks. Direct adjacents: utilities and mobility
operators (their networks are already first-class objects in the world model), and
insurers, who want the counterfactual machinery pointed at exposure.

**Defence & disaster — civil-protection agencies and exercise/training organisations**
first; defence primes and training integrators as the channel into defence proper. This
buyer's non-negotiables — sovereignty, on-premises deployment, no data leaving the
building, bring-your-own-models — are not a compliance retrofit for us: BYOK and
self-hosted runners are the architecture (see the ownership layer in
[01](01-core-technology.md)). A distributed exercise where each cell runs its own minds
against a shared world is the same deployment shape our independent ghost runner ships
today.

## Commercial shapes

**Games** keeps the four-tier structure:

| Tier | What it is | What it's for |
|---|---|---|
| **Free indie** | Full engine for small teams | Goodwill, ecosystem seeding, tomorrow's mid-size customers |
| **World licence** | Monthly per-world licence for the production-supported engine: hosted or on-prem, maintained internals, integration support, SLA | The core revenue line: priced so build-vs-buy favours buying for any studio whose engineering time costs more than the licence |
| **Per-NPC / per-player usage** | Usage-based component on top of the licence | Captures value as a shipped game's population and player base grow |
| **Enterprise BYOK** | Custom deployment, private adapters, designer tooling | Large studios |

**Urban twins** follow a build → run → ask arc:

- **Build** — a data-integration engagement: the city's open data, sensor feeds, and
  network models become a calibrated world. Fixed-scope, consultancy-friendly.
- **Run** — an annual **calibrated-twin licence**: the maintained rules corpus, the data
  pipelines, and a recurring **calibration report** — the measured gap between twin and
  city, per rule. The report *is* the SLA: we commit to telling the customer where the
  twin is wrong, quantitatively, on a cadence.
- **Ask** — per-study counterfactual packs: a forked world, an intervention, a seeded
  comparison, a defensible answer.

**Defence & disaster** is episodic plus standing:

- **Per-exercise** — scenario build, inject schedule, per-principal views, facilitation
  support, and the after-action data package. Exercises are events; they are priced as
  events.
- **Readiness licence** — the standing calibrated twin of a jurisdiction, kept warm
  between exercises, so the next scenario starts from today's world rather than a
  six-month build.
- **Sovereignty is the default, not an upsell.** On-prem, BYOK, air-gappable.

Numbers stay in the BD conversation by design; the *shape* is public so the conversation
starts honest.

**We do not monetise inference — ever.** Agents run on the customer's model keys (BYOK).
This removes the "lock-in to your inference provider" objection, keeps our margin
structure clean of token-price exposure, means every model-provider price war makes our
layer *relatively* more valuable — and, in the public-sector verticals, it is the
difference between passing and failing a sovereignty review.

## The academic branch stays non-revenue

"Analysis of the absence" ([04](04-mission.md)) — searching simulated historical contexts
for those consistent with a visible phenomenon — is deliberately not a revenue line. It is
grant- and collaboration-funded, buys method citations and credibility, and matters more
now, not less: it is the same abductive machinery the urban twin sells ("which contexts
are consistent with what we can measure?") pointed at the past, and every published,
peer-reviewed use hardens the methodology the paying verticals stand on.

## The OSS ↔ commercial seam

**Open infrastructure attracts believers; the commercial licence monetises integrated
scale.** The line between the two is explicit and durable:

- **Free forever (permissive OSS):** geomqtt, geobard, the inspector surface, georender,
  ticker, the FoundryVTT shared-world module, the map tooling, the Unity/Unreal bridges,
  ghostkit and GhostDeck — and, in the new verticals, the **rules-language specification**
  and the **open-data importers** (Bologna's traffic-sensor ingester is the first). Open
  formats over open data is how our schemas become the path of least resistance in the
  civic-tech world.
- **Free core, customer-paid inference (BYOK):** the ghost/shell agent runtime — the
  reference implementation of what runs on top of the engine.
- **Paid:** the maintained engine — the thing you bet a shipped game, a policy decision,
  or an exercise on, with the support and SLA those sentences imply; the calibrated rules
  corpora; the per-principal view machinery as an operated product; designer and exercise
  tooling.
- **Held private:** designer-tool surfaces and proprietary world adapters that emerge from
  design-partner work.

The cannibalisation question, answered honestly: yes, a sufficiently determined engineer
could rebuild a passable engine from our published architecture. Defensibility is not
secrecy — it is that the maintained version, the affordance schema as a product, the
per-engine integrations, the world-data adapters, and the compounding calibration dataset
are a specialised team's full-time roadmap. Guardrail: nothing ships to the OSS layer if
it removes a reason to license.

## Dual-use guardrails

Entering the defence-adjacent market obliges us to say what we will and will not build,
before a customer asks us to:

- **Yes:** training and exercises, planning and course-of-action analysis, resilience and
  evacuation studies, information-environment research under review.
- **No:** targeting support, operational employment against real persons, deception
  operations, and any use where the simulated population is a proxy for acting on the
  real one without its knowledge.
- Export-controlled and classified work happens through partners holding the relevant
  frameworks; we comply with EU dual-use regulation (2021/821) and we keep the civilian
  branch of every capability public-first.

This section is a diligence asset, not a disclaimer: the customers worth having ask.

## Why this survives the model wars

The moat is shaped like infrastructure, not like a model:

1. **The ontology layer doesn't commoditise.** Better models make integration cheaper and
   world-law enforcement *more* valuable — smarter ghosts need better shells.
2. **Standards gravity.** Every geomqtt client, Foundry install, ghostkit haunt, and
   open-data importer makes our formats the path of least resistance.
3. **The calibration dataset compounds — now across three ground truths.** Fictional
   worlds at population scale, a real city's sensors, and exercise outcomes all feed the
   same behaviour-vs-prediction dataset. Nobody else has longitudinal calibration data
   from embodied LLM populations against *measured reality*; it improves the product in
   every vertical at once and is unforgeable by a fast follower.
4. **BYOK neutrality.** Whichever model provider wins, we are the layer that makes their
   model useful in a persistent world — we don't compete with any of them, and we pass
   every sovereignty review they fail.
5. **Public reference customers compound differently.** A shipped game logos a slide; a
   city that renews its calibration report, or an agency that re-books next year's
   exercise, is a reference that procurement officers call.

## Go-to-market

Founder-led engineering credibility plus a dedicated business-development lead, with a
strict seam between them: marketing artifacts (talks, technical deep-dives, public demos,
the OSS floor) make outreach land warm and arm the internal champion; BD owns the list,
the qualification, the pricing conversation, and the close. The motion measures itself on
next-steps-booked, not compliments collected.

Each market gets its own wedge, anchored to what already exists:

- **Games** — anchored to industry moments (the GDC talk was the 2026 anchor); design
  partnerships first, the LOIs that precede licences, with the free tier and OSS adoption
  as the long-tail funnel underneath.
- **Urban twins** — the SMARTGREENS paper plus the live Bologna calibration demo is the
  wedge; the motion runs through consultancy partnerships and EU-funded projects
  (Horizon-class calls fund exactly the build phase of the arc above), which also
  de-risks the vertical on someone else's balance sheet.
- **Defence & disaster** — one lighthouse exercise with a civil-protection partner,
  designed to be publishable, then let the after-action data package sell the next one.
  Defence-proper arrives through primes and training integrators, never cold.

Sequencing is portfolio logic, not a pivot: games funds and proves the engine at
population scale; urban twins is grant-fundable *now* on running evidence; defence enters
through disaster at its own procurement pace. One engine roadmap underneath all three —
and per [02](02-rd-runway.md), a vertical pulls its Horizon-3 items forward the moment a
partner or grant lands. The year-by-year version — targets, hires, funding, and the kill
criteria for each motion — is the [business plan](05-business-plan.md).

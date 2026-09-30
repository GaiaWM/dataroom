<!-- held back here: partner-specific integration work, exact staffing/spend, unannounced module names -->

# 02 · R&D runway — Q4 2026 → 2028

Three horizons. Each workstream has a definition of done; nothing here is aspiration without
a shipping shape. Dates are calendar quarters and mark *intent under current resourcing* —
design-partner work always outranks the roadmap when they conflict. This is the *product*
plan; the company-level timeline — revenue targets, hiring, funding, and the gates where
course changes — is the [business plan](05-business-plan.md).

## Why the dates are credible: recent shipping cadence

We plan in independently shippable slices and have held that cadence all year:

| Shipped | What |
|---|---|
| 2026 Q2 | World-action layer (stochastic, skill-gated outcomes) closing the calibration loop; multi-infrastructure model connectors; operator dashboard with live map and ops firehose |
| 2026-07-07 | "The Ghost in the Shell" — public talk and paper argument ([repo](https://github.com/GaiaWM/260707)) |
| 2026-07-09 | Ghost Gateway owner keys · [ghostkit](https://github.com/GaiaWM/ghostkit) · [GhostDeck](https://github.com/GaiaWM/ghostdeck) desktop builds for three platforms |
| 2026-07-10 | [geobard](https://github.com/openfantasymap/geobard) extracted as a standalone OSS project |
| 2026-08 | [ticker](https://github.com/openfantasymap/ticker) (label-driven world-time service) · [avatars](https://github.com/openfantasymap/avatars) (in-character chat API, live for the OHM ruler galleries — the engine's first non-game deployment) |

## Horizon 1 — Prove it with partners (Q4 2026 → Q2 2027)

The commercial gate for everything else: convert studio conversations into evaluations, and
evaluations into design partnerships.

| Workstream | Deliverable | Done when |
|---|---|---|
| **Evaluator sandbox** | A curated `docker compose up` preset: one command brings up engine + organs + dashboard + a seeded world, with a documented quickstart and reference-architecture diagrams for Unity, Unreal and Foundry pipelines | A studio engineer reaches a living, inspectable world in under 15 minutes without talking to us |
| **Public proof surfaces** | Hosted Object Inspector demo (description in → structured affordances out, latency visible) and an influence-ripple demo on a staged scenario | Both linkable from the site and stable enough to leave running |
| **World richness** | Failure-aware world verbs (climb, pick-lock, persuade, trade) resolving through the same stochastic layer, so calibration outcomes become richer than success/failure of dispatch | Calibration records carry world-grounded outcome detail |
| **Population scale** | From tens to thousands of concurrent agents: template-driven mass spawning, affordance-aware scheduling of agent workloads across hosts, and the load engineering that follows | A thousand-agent world runs for a week unattended with a flat operator cost curve |
| **Self-serve ownership** | Owner-key issuance without an operator in the loop, abuse controls (creation flooding; energy already throttles action spam), and a custodial-runner convenience tier | A stranger can own and run a ghost without us provisioning anything |
| **Partner integrations** | 2–3 design partnerships; world-data ingestion adapters for partner-owned worlds | Partner world state served by the engine in their pipeline, LOI-backed |

## Horizon 2 — The designer product (2027)

Horizon 1 sells to CTOs; Horizon 2 is what their creative directors use. This is where the
paid layer becomes visibly *more* than the OSS sum-of-parts.

- **World-law authoring.** Affordance registries, influence scenarios, and cultural
  templates become designer-facing tools rather than JSON envs: define the laws of your
  world once, and the runtime enforces them on every agent — including the ones no writer
  scripted. This is the maintained, supported core of the commercial licence.
- **Multi-world, multi-tenant hosting.** Per-world shards under one gateway; temporal state
  and world timelines at production scale; per-world access control.
- **The social layer.** Public ghosts, inter-owner encounters, and conversation between
  owned agents — turning individually-owned minds into a society, which is both the research
  instrument and the consumer-facing hook.
- **SDK depth.** A TypeScript ghostkit (web and GhostDeck-native runners), and engine-native
  SDKs where partner work justifies them (the Unity/Unreal bridges already exist as
  transport).
- **Calibration as a public benchmark.** Periodic dataset releases and per-model CE(n)
  results from live worlds; the goal is that "how does your model behave when embodied"
  becomes a question people expect us to answer.

## Horizon 3 — The standard layer (late 2027 → 2028)

- **Protocol stewardship.** The eight-organ MCP contract and geomqtt's tile-keyed fanout
  published and versioned as specifications, so third parties build shells and clients we
  don't own. The formats become the moat's outer wall (see [business model](03-business-model.md)).
- **Enterprise shape.** On-prem deployment of the full engine, SLAs, per-NPC/per-player
  usage metering and billing infrastructure.
- **Beyond games.** The avatars deployment (historical figures over Open History Map data)
  is the template: the same engine serving customers whose "world" is a real place with a
  real timeline. Three named directions, detailed in [04](04-mission.md) and given their
  commercial shapes in [03](03-business-model.md): **urban digital twins** (the
  SMARTGREENS methodology implemented — city open data ingested as ground truth, synthetic
  populations, per-rule calibration against real sensors, forked counterfactuals; the
  Bologna pilot already runs), **defence & disaster resilience** (scenario rehearsal with
  embodied populations — locally-perceiving agents, rumour dynamics, cascading
  consequence — plus per-principal views, injects-as-changesets, and courses of action as
  seeded forks), and **"analysis of the absence"** (an academic branch: where a historical
  phenomenon is visible but its context is unexplored, search simulated contexts for those
  consistent with the record — grant- and collaboration-funded, deliberately not a revenue
  line). Any of these pulls forward from this horizon the moment a partner or grant
  lands; we follow demand here rather than lead with it.

## Research runway (continuous)

The calibration programme is the scientific spine: extend the affordance-order
overconfidence results across model families and quantisation levels, test mitigation
strategies (two-tier vetting already measurably reduces failure dispatch), and publish
against the controlled benchmarks the paper targets. Research output is marketing, hiring
surface, and product regression suite at once.

## What we deliberately will not do

- No proprietary inference, ever — BYOK is load-bearing for trust and for margin sanity.
- No "AI NPC plug-in" pivot chasing the wrapper category, even when it would close faster.
- No new OSS component that removes a reason to license the engine: every candidate release
  is checked against that question before it ships.

## Top risks

| Risk | Posture |
|---|---|
| Studio evaluation cycles are slower than our runway math | Horizon 1's sandbox exists to compress them; the OSS believer-funnel keeps inbound warm between BD pushes |
| A model provider ships a "world memory" feature that *sounds* like us | Their layer is per-conversation state; ours is authoritative, multi-agent, designer-governed world law. The category work in [03](03-business-model.md) is the defence, and it's why we refuse the wrapper shelf |
| A clever team rebuilds the stack from our published architecture | Some will; they're lost-and-fine. The maintained engine, the world adapters, the designer tools, and the compounding calibration data are the multi-year bet they'd be making against |

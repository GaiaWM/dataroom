<!-- held back here: pricing numbers, tier thresholds, partner pipeline names — BD conversation only -->

# 03 · Business model

## The category

We sell **world simulation infrastructure**, not an AI-NPC platform.

The AI-NPC shelf is crowded and structurally doomed: every wrapper's value shrinks with each
model release, and studios know it. The shelf we occupy is older and duller — the systems
studios already build in-house and dread maintaining: quest databases, faction state
machines, schedule systems, the lore bible nobody updates. Nobody sells this layer
commercially for the generative era, and studios are currently rebuilding it badly, one
in-house wiki at a time.

The buyer's alternative to GaiaWM is not a competitor. It is **eighteen months of internal
platform work** that their engine team doesn't want to own.

## Who pays

**Primary buyer: the studio CTO / technical director** of teams building open-world or
systemic games with persistent state — especially teams whose generative-NPC prototype
didn't survive contact with shipped game state. They buy a single source of truth for
narrative coherence with a state hierarchy that scales past where the lore wiki broke.

Their creative director is the second audience: designers define a world's laws once, and
the runtime enforces them everywhere their NPCs go — including the NPCs nobody wrote
personally.

We deliberately let three segments go: "AI NPC plug-in" shoppers (wrappers close those
faster), F2P live-ops shops measuring DAU lift, and indies needing turnkey this quarter —
those get the free tier as goodwill and funnel, not as strategy.

## The four tiers

| Tier | What it is | What it's for |
|---|---|---|
| **Free indie** | Full engine for small teams | Goodwill, ecosystem seeding, tomorrow's mid-size customers |
| **World licence** | Monthly per-world licence for the production-supported engine: hosted or on-prem, maintained affordance/influence internals, integration support, SLA | The core revenue line: priced so build-vs-buy favours buying for any studio whose engineering time costs more than the licence |
| **Per-NPC / per-player usage** | Usage-based component on top of the licence | Captures value as a shipped game's population and player base grow |
| **Enterprise BYOK** | Custom deployment, private adapters, designer tooling | Large studios and the non-game vertical |

Numbers stay in the BD conversation by design; the *shape* is public so the conversation
starts honest.

**We do not monetise inference — ever.** Agents run on the customer's model keys (BYOK).
This removes the "lock-in to your inference provider" objection that triggers
rebuild-it-ourselves decisions, keeps our margin structure clean of token-price exposure,
and means every model-provider price war makes our layer *relatively* more valuable.

## The OSS ↔ commercial seam

**Open infrastructure attracts believers; the commercial licence monetises integrated
scale.** The line between the two is explicit and durable:

- **Free forever (permissive OSS):** geomqtt, geobard, the inspector surface, georender,
  ticker, the FoundryVTT shared-world module, the map tooling, the Unity/Unreal bridges,
  ghostkit and GhostDeck. Pieces a studio could assemble themselves; we ship them so they
  don't have to — and so our data formats and protocols become the de facto standards.
- **Free core, customer-paid inference (BYOK):** the ghost/shell agent runtime — the
  reference implementation of what runs on top of the engine.
- **Paid:** the world-state engine as a maintained product — the thing you bet a shipped
  game on, with the support and SLA that sentence implies.
- **Held private:** designer-tool surfaces and proprietary world adapters that emerge from
  design-partner work.

The cannibalisation question, answered honestly: yes, a sufficiently determined engineer
could rebuild a passable engine from our published architecture. Defensibility is not
secrecy — it is that the maintained version, the affordance schema as a product, the
per-engine integrations, the world-data adapters, and the compounding calibration dataset
are a specialised team's full-time roadmap. A studio choosing to rebuild is making a
multi-year bet against it. Guardrail: nothing ships to the OSS layer if it removes a reason
to license.

## Why this survives the model wars

The moat is shaped like infrastructure, not like a model:

1. **The ontology layer doesn't commoditise.** Better models make integration cheaper and
   world-law enforcement *more* valuable — smarter ghosts need better shells.
2. **Standards gravity.** Every geomqtt client, Foundry install, and ghostkit haunt makes
   our formats the path of least resistance.
3. **The calibration dataset compounds.** Nobody else has longitudinal
   behaviour-vs-prediction data from embodied LLM populations; it improves the product and
   is unforgeable by a fast follower.
4. **BYOK neutrality.** Whichever model provider wins, we are the layer that makes their
   model useful in a persistent world — we don't compete with any of them.

## Go-to-market

Founder-led engineering credibility plus a dedicated business-development lead, with a
strict seam between them: marketing artifacts (talks, technical deep-dives, public demos,
the OSS floor) make outreach land warm and arm the internal champion; BD owns the list, the
qualification, the pricing conversation, and the close. The motion is anchored to industry
moments (the GDC talk was the 2026 anchor), runs pre-warming content before meetings and a
48-hour arm-the-champion follow-up after, and measures itself on next-steps-booked, not
compliments collected. Target pipeline: design partnerships first — the LOIs that precede
licences — with the free tier and OSS adoption as the long-tail funnel underneath.

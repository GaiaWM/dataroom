<!-- held back here: partner names, pricing numbers, affordance-modelling internals — NDA room only -->

# GaiaWM — Data Room

> **GaiaWM is the world-state engine that gives generative agents a place to actually live in.**
> The agent runtime is a reference implementation of what runs *on top of it* — not what it is.

Frontier models keep getting better and integrations keep getting cheaper. The ontology of a
world — its laws, its affordances, its history, its consequences — is the one layer that does
**not** get easier when the model gets smarter. That is the layer we build, maintain, and license.

*Last updated: September 2026.*

## Contents

| Document | Answers |
|---|---|
| [01 · Core technology](01-core-technology.md) | What we have built — the engine, the embodied agent runtime, the calibration surface, the real-time fabric, the ownership layer. All of it running code. |
| [02 · R&D runway](02-rd-runway.md) | What we build over the next 1–2 years (Q4 2026 → 2028), in three horizons, with the shipping cadence that makes the dates credible. |
| [03 · Business model](03-business-model.md) | One engine, three markets — games, urban digital twins, defence & disaster resilience: who pays in each, the commercial shapes, the dual-use guardrails, and why the open-source layer strengthens rather than cannibalises the paid one. |
| [04 · Mission & context](04-mission.md) | Why we are doing this, where we come from, the research behind it, and everything you can verify today. |

This room is the diligence companion to the **[pitch deck](https://gaiawm.github.io/pitch-deck/)**
([source](https://github.com/GaiaWM/pitch-deck)): the deck is the story, this room is the
evidence and the plans behind it.

## How to read this room

Everything in [01](01-core-technology.md) is **running code**, most of it public. We prefer
links to repositories and live systems over claims; where a capability is not yet public, we
say so explicitly. The plans in [02](02-rd-runway.md) are plans — dated, sliced, and honest
about risk.

Quick verification, five minutes:

- **[github.com/GaiaWM](https://github.com/GaiaWM)** — ghostkit (BYOK agent library + CLI), GhostDeck (desktop client), the pitch deck, and the July 2026 talk.
- **[github.com/openfantasymap](https://github.com/openfantasymap)** — the open-infrastructure floor: geomqtt (Rust real-time geospatial broker, with a [live demo tracking the ISS](https://openfantasymap.github.io/geomqtt)), geobard, the affordance inspector, georender, the FoundryVTT / Unity / Unreal bridges.
- **[fantasymaps.org](https://fantasymaps.org)** — the live tile infrastructure our simulations run on.

## What is *not* in this room

Consistent with how we run every public surface, some layers are deliberately held back and
available under NDA in a partner conversation: the affordance-modelling internals (how the
inspector reasons, the schema for designer-authored world laws), the influence-engine
composition model, pricing with real numbers, and anything specific to a design partner.
If you can't tell what a public artifact of ours is holding back, we've done it wrong.

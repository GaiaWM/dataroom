<!-- held back here: team compensation/cap-table, unannounced collaborations -->

# 04 · Mission & context

## The mission

**Give artificial minds real places to live — and keep the minds private property of their
owners while the places stay shared.**

Two convictions drive everything we build:

1. **Cognition is not the model in isolation.** It is an inference engine interacting with a
   structured, embodied substrate — a ghost in a shell. Intelligence that matters in a world
   needs metabolism, memory that fades, skills that gate what's possible, and actions that
   can fail. We build the shell as seriously as the industry builds the ghost.
2. **The world is shared; the minds are private.** The places — geography, history, physics,
   consequence — should be common infrastructure, openly specified and cheap to join. The
   minds that inhabit them — their models, keys, souls and goals — belong to their owners
   and never pass through our servers. This is the opposite of the platform-era default,
   and it is deliberate.

The second conviction is our worldview as much as our architecture: **open infrastructure
beneath commercial scale**, non-extractive by construction. We monetise the maintained
engine at the integration layer, never the inference, never the owner's data, never
attention.

## Where we come from

GaiaWM was not started as an AI company. It grew out of a decade of open geospatial work:

- **[Open History Map](https://www.openhistorymap.org)** — mapping the real world through
  time, supported by the Shuttleworth Foundation — established the discipline: a *place* is
  geometry plus a timeline plus what is true there at a date.
- **[Open Fantasy Maps](https://fantasymaps.org)** — the same rigor applied to fictional
  worlds: live tile infrastructure, VTT integrations, and the realisation that fictional
  worlds are the perfect laboratory for world-scale simulation, because their ontology can
  be complete.
- **GaiaWM** is the synthesis: the engine that holds a world's state — real or fictional —
  and lets generative agents live in it accountably.

That lineage is why the stack is geospatial-native (most agent frameworks bolt "location"
on as a string), why temporal state is a first-class citizen, and why our first non-game
deployment — [in-character historical avatars](https://github.com/openfantasymap/avatars)
over Open History Map's ruler galleries — took days, not months.

## The research

The architecture is also an experimental instrument. Our thesis work — *The Ghost in the
Shell* ([presentation, 2026-07-07](https://github.com/GaiaWM/260707)) — argues that
embodiment constraints (position blindness, energy metabolism, decaying memory) are not
game flavour but the substrate cognition requires, and that agent quality must be
*measured*, not vibed: every prediction an agent makes is scored against the real outcome
in the calibration organ.

The headline empirical result — overconfidence compounds with affordance order, reproduced
live in our own simulation (+0.04 → +0.18 → +0.32 bias across orders 1–3 over 600
trials) — is exactly the failure mode that makes naive LLM-NPC deployments collapse in
shipped games, and the two-tier vetted architecture is our measured mitigation. Research,
product regression suite, and marketing are the same artifact here.

## What is alive right now

A persistent Toril (Forgotten Realms) simulation runs continuously on the full stack:
LLM-driven populations spawned from declarative templates (farmers, bandits, travellers),
named characters with souls and goals, ghosts running on everything from 1-bit-quantised
local models to frontier APIs across six inference providers, an operator dashboard
streaming every organ call and LLM exchange live onto a real map, and owner-run minds
connecting through ghostkit and GhostDeck from outside our infrastructure. It has produced
over 10,000 calibration records. It is not a demo reel; it is where we live.

## Applications beyond games

Games are the proving ground, not the perimeter. The engine's primitives — real geography,
temporal state, embodied populations, propagated consequence, measured behaviour — carry
directly into two directions we are actively developing:

### Emergency simulation on real geography

Civil-protection scenarios — floods, evacuations, infrastructure failure, mass events —
simulated on the real world's geometry with populations of embodied agents. The stack is
unusually honest about how people actually behave in a crisis, because its constraints are
the point rather than patches:

- Agents are **position-blind and perceive locally** — no god's-eye view, exactly like a
  person in smoke, floodwater, or an unfamiliar neighbourhood.
- **Stress and energy are metabolic**, memory decays, and information travels agent-to-agent
  through the comms organ — so rumour and misinformation dynamics are first-class phenomena,
  not an afterthought.
- The **influence/ripple engine** propagates cascading consequences (a bridge closes, a
  shelter fills, a rumour spreads) through world state.
- The **calibration organ** measures the gap between predicted and actual outcomes — the
  precise quantity emergency planning worries about, for the simulated responders and for
  the plan itself.

Operationally this is the enterprise tier of the [business model](03-business-model.md):
scenario rehearsal and communication-strategy testing for civil-protection agencies,
municipalities, insurers and resilience planners, on their own geography.

### Analysis of the absence — the academic branch

Historical research is full of situations where **the phenomenon is visible but the context
is not completely explored**: the record shows an outcome — a settlement abandoned, a trade
route gone quiet, a practice that spread or failed to — while the everyday context that
produced it left few or no sources.

The engine turns that absence into a testable target. Rebuild the period world from
[Open History Map](https://www.openhistorymap.org) data (geometry plus timeline), populate
it with embodied agents under period-plausible constraints — skills, affordances, energy
costs, travel and communication ranges — and search the space of candidate contexts for
those whose simulated dynamics actually reproduce the visible phenomenon. Simulation as an
abductive instrument: not "what happened", but "which contexts are even consistent with
what we can see".

The calibration organ is what separates this from storytelling — every run is measured,
comparable, and repeatable, which is the methodological bar academic use demands. We run
this as a deliberately **academic branch** of the platform: university collaborations,
grant-funded projects and publications, valued in credibility, method citations and
calibration data rather than licence revenue.

## Team

- **Marco Montanari** ([@sirmmo](https://github.com/sirmmo)) — founder and architect.
  Geospatial engineer; author of Open History Map and Open Fantasy Maps; a decade of
  open-infrastructure work across GIS, real-time systems, and tabletop/games tooling.
- **Lorenzo Gigli** ([@hyperloris](https://github.com/hyperloris)) — co-founder and
  architect. PhD; specialised in blockchain and AI learning models.
- **Matteo Sipione** ([@sipioteo](https://github.com/sipioteo)) — co-founder and
  architect. Specialised in narrative generative-AI models.
- A dedicated **business development lead** runs the studio pipeline (segmentation,
  qualification, partnerships), keeping the engineering/BD seam described in
  [03](03-business-model.md).
- The wider [openfantasymap](https://github.com/openfantasymap) contributor community
  around the OSS floor.

## Additional material

| Material | Link |
|---|---|
| Pitch deck (live) | [gaiawm.github.io/pitch-deck](https://gaiawm.github.io/pitch-deck/) · [source](https://github.com/GaiaWM/pitch-deck) |
| The Ghost in the Shell — talk | [github.com/GaiaWM/260707](https://github.com/GaiaWM/260707) |
| Organisation page | [gaiawm.github.io](https://gaiawm.github.io) |
| ghostkit — own a ghost | [github.com/GaiaWM/ghostkit](https://github.com/GaiaWM/ghostkit) |
| GhostDeck — desktop client | [github.com/GaiaWM/ghostdeck](https://github.com/GaiaWM/ghostdeck) |
| Open-infrastructure floor | [github.com/openfantasymap](https://github.com/openfantasymap) |
| geomqtt live demo | [openfantasymap.github.io/geomqtt](https://openfantasymap.github.io/geomqtt) |
| Live tile infrastructure | [fantasymaps.org](https://fantasymaps.org) |

For anything held back from this room — internals, numbers, partner material — open an
issue on this repository or reach us through the organisation page, and we'll take it to
the NDA conversation where it belongs.

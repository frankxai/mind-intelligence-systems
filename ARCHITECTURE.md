# Architecture

Mind Intelligence Systems is a layered portfolio. Every layer composes the
**Starlight Intelligence Protocol (SIP)** substrate and inherits the canon defined in this repo.

## Layers

```
Canon & Governance      mind-intelligence-systems   ← you are here
        │                naming · models · mesh · doctrine
        ▼
Cognitive Model         human-mind-intelligence-system
        │                schemas · ontology · response-prediction
        ▼
Lived OS                agentic-mind-os             (personal, daily)
        │                       │
        ▼                       ▼
Premium Distribution    starlight-mind-os-pro       (onboarding, dashboards, workshops)

Research (planned)      research-intelligence-os → psychology / neuroscience verticals
Memory Palace (sibling) mind-palace-agent-skills + frankx-mind-palace   (Blessing Protocol)
Discovery               awesome-mind-agent-skills   (the front door)
```

## Two sub-families under one umbrella

The swarm holds two distinct registers — kept distinct on purpose (see
[NAMING_DOCTRINE.md](./NAMING_DOCTRINE.md)):

1. **The cognitive family** models the mind: a shared ontology (`models/human-mind/`), an
   engineered System that turns it into schemas, a lived OS that runs on those schemas, and a
   research wing that grounds the constructs in evidence. This is the "understand and operate
   cognition" track.
2. **The memory-palace family** runs the [Blessing Protocol](https://github.com/frankxai/bless):
   a weekly ritual of witnessing finished work and growing a navigable palace from it. It is
   named for the *practice* (memory palace), not the cognitive model, and is coherent on its
   own. It is the "reflect and keep what is whole" track.

Discovery (`awesome-mind-agent-skills`) is the one place that links both.

## Key contracts

- **MindPack** (`mindpack.yaml`) — packaging for agents, skills, workflows, schemas, vaults
  in the lived OS.
- **ResearchPack** (`researchpack.yaml`) — packaging for the research systems *(planned)*.
- **Cognitive schemas** — JSON Schema derived from the human-mind model modules, owned by
  `human-mind-intelligence-system`.

## Data & privacy

- Local-first vaults for personal data (the OS layer).
- Source-grounded artifacts for research claims.
- JSON Schema for interoperability between systems.
- **Never clinical diagnosis** — observation, interpretation, hypothesis, evidence, and
  decision are always separated and labeled.

## Agent interaction model

All repos are designed for Codex / Claude Code / Gemini / Hermes agents:
- `repo-mesh.yaml` for the machine-readable mesh.
- `AGENTS.md` and `HERMES.md` for working context.
- `.codex/tasks.md` queues for concrete tasks.
- Issue templates for task intake.

See each repo's own README/ARCHITECTURE for domain specifics.

---

Built on SIP. Part of [Mind Intelligence Systems](./README.md) canon.

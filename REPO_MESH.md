# 🌐 REPO MESH v3 • The Sovereign Intelligence Constellation

> *"Every star in this constellation was placed with intention. Every edge in this graph is a promise."*
> — frankxai

---

## ✦ What This Document Is

This is the **living map of the frankxai intelligence empire** — all repos, their roles, their dependencies, their data flows, and their relationships to the human mind canon.

Agents entering the swarm read this first. Architects consult this when adding nodes. Founders review this when the constellation needs to evolve.

For the machine-readable version, see [`repo-mesh.yaml`](./repo-mesh.yaml).

---

## ✦ The Full frankxai Constellation

> **Layer mapping note:** The layer numbers in this mesh are topology labels for `repo-mesh.yaml`, not a replacement for the broader 1–7 conceptual stack in [`ARCHITECTURE.md`](./ARCHITECTURE.md). Use this document for repo dependency metadata; use `ARCHITECTURE.md` for the portfolio-level conceptual layering.

### Layer 0: Canon & Governance (This Repo)

| Repo | URL | Role |
|------|-----|------|
| `mind-intelligence-systems` | [frankxai/mind-intelligence-systems](https://github.com/frankxai/mind-intelligence-systems) | **The canon**. Naming doctrine, architecture governance, shared human-mind ontology, repo mesh. All other repos answer to this. |

The `models/human-mind/` directory within this repo is **Layer 0, Sub-layer Alpha** — the foundational ontology that every intelligent agent in the empire may consume.

**Human Mind Model Modules:**

| Module | File | Status |
|--------|------|--------|
| Attention | [attention.md](./models/human-mind/attention.md) | ✅ Active |
| Memory | [memory.md](./models/human-mind/memory.md) | ✅ Active |
| Emotion | [emotion.md](./models/human-mind/emotion.md) | ✅ Active |
| Motivation | [motivation.md](./models/human-mind/motivation.md) | ✅ Active |
| Identity | [identity.md](./models/human-mind/identity.md) | ✅ Active |
| Learning | [learning.md](./models/human-mind/learning.md) | ✅ Active |
| Belief | [belief.md](./models/human-mind/belief.md) | ✅ Active |
| Behavior | [behavior.md](./models/human-mind/behavior.md) | ✅ Active |
| Consciousness | [consciousness.md](./models/human-mind/consciousness.md) | ✅ Active |
| Metacognition | [metacognition.md](./models/human-mind/metacognition.md) | ✅ Active |
| Decision Making | [decision-making.md](./models/human-mind/decision-making.md) | 🔄 Expanding |
| Social Cognition | [social-cognition.md](./models/human-mind/social-cognition.md) | 🔄 Expanding |

---

### Layer 1: Personal & Runtime OS

| Repo | URL | Role | Depends On | Provides |
|------|-----|------|-----------|---------|
| `agentic-mind-os` | [frankxai/agentic-mind-os](https://github.com/frankxai/agentic-mind-os) | Personal second-brain OS — lived daily | `mind-intelligence-systems`, `research-intelligence-os` | vault-templates, personal-agents, mind-skills |
| `research-intelligence-os` | [frankxai/research-intelligence-os](https://github.com/frankxai/research-intelligence-os) | Reusable runtime: contracts, templates, evals | `mind-intelligence-systems` | contracts, templates, evals, scripts |

---

### Layer 2: Portfolio & Creative OS

| Repo | URL | Role | Depends On | Provides |
|------|-----|------|-----------|---------|
| `research-intelligence-systems` | [frankxai/research-intelligence-systems](https://github.com/frankxai/research-intelligence-systems) | Cross-domain research portfolio | `research-intelligence-os`, `mind-intelligence-systems` | cross-domain-packs, workflows, claim-graphs |
| `gencreator-ai` | [frankxai/gencreator-ai](https://github.com/frankxai/gencreator-ai) | Creative MCP / content OS for campaigns and creation | `mind-intelligence-systems`, `arcanea` | creative-agents, campaign-intelligence, mcp-tools |

---

### Layer 3: Domain Systems & Creative Labs

| Repo | URL | Role | Depends On | Provides |
|------|-----|------|-----------|---------|
| `psychology-research-intelligence-system` | [frankxai/psychology-research-intelligence-system](https://github.com/frankxai/psychology-research-intelligence-system) | Psychology vertical: constructs, evidence, psychometrics | `research-intelligence-os`, `mind-intelligence-systems` | psych-agents, psych-skills, construct-schemas |
| `neuroscience-research-intelligence-system` | [frankxai/neuroscience-research-intelligence-system](https://github.com/frankxai/neuroscience-research-intelligence-system) | Neuroscience vertical: BIDS, NWB, neuro-schemas | `research-intelligence-os`, `mind-intelligence-systems` | neuro-agents, bids-nwb-skills, neuro-schemas |
| `arcanea` | [frankxai/arcanea](https://github.com/frankxai/arcanea) | Applied creative intelligence lab — where agents meet art, story, and mysticism | `mind-intelligence-systems` | creative-agent-primitives, arcanea-skills, narrative-schemas |
| `starlight-cosmos-engine` | [frankxai/starlight-cosmos-engine](https://github.com/frankxai/starlight-cosmos-engine) | Cosmos storytelling and worldbuilding pipeline | `mind-intelligence-systems`, `arcanea` | cosmos-pipelines, worldbuilding-schemas, narrative-agents |
| `starlight-intelligence-system` | [frankxai/starlight-intelligence-system](https://github.com/frankxai/starlight-intelligence-system) | Premium intelligence distribution layer | `mind-intelligence-systems`, `starlight-cosmos-engine` | premium-packs, intelligence-workflows, distribution-agents |
| `starlight-mind-os-pro` | [frankxai/starlight-mind-os-pro](https://github.com/frankxai/starlight-mind-os-pro) | Premium personal OS: onboarding, dashboards, workshops | `agentic-mind-os`, `mind-intelligence-systems` | onboarding, dashboards, workshops, commercial-templates |

---

### Layer 4: Infrastructure, Protection & Skill Primitives

| Repo | URL | Role | Depends On | Provides |
|------|-----|------|-----------|---------|
| `claude-skills` | [frankxai/claude-skills](https://github.com/frankxai/claude-skills) | Agent skill primitives for Claude-based agents across the empire | `mind-intelligence-systems` | skill-primitives, agent-tools, claude-workflows |
| `ai-architect` | [frankxai/ai-architect](https://github.com/frankxai/ai-architect) | System design intelligence: scaffold generation, architecture agents | `mind-intelligence-systems`, `claude-skills` | architecture-agents, scaffold-generators, design-intelligence |
| `family-guardians` | [frankxai/family-guardians](https://github.com/frankxai/family-guardians) | Sentinel systems protecting family data, safety, and digital wellbeing | `mind-intelligence-systems`, `claude-skills` | guardian-sentinels, safety-agents, family-protection-workflows |
| `multi-agent-harness` | [frankxai/multi-agent-harness](https://github.com/frankxai/multi-agent-harness) | Multi-agent orchestration runtime: coordination, routing, lifecycle management | `mind-intelligence-systems`, `claude-skills`, `ai-architect` | orchestration-runtime, agent-router, lifecycle-manager |

---

### Discovery Layer

| Repo | URL | Role | Depends On | Provides |
|------|-----|------|-----------|---------|
| `awesome-mind-agent-skills` | [frankxai/awesome-mind-agent-skills](https://github.com/frankxai/awesome-mind-agent-skills) | Curated ecosystem discovery list | `mind-intelligence-systems` | curated-lists, ecosystem-map |

---

## ✦ Cross-Leverage Strategy

The power of this constellation is **compound intelligence** — each repo multiplies the value of every other:

```
HMIS (canon) ──────────────────────────────────────────► All repos consume mind ontology
     │
     ├──► arcanea ──────────────────────────────────────► Creative agent primitives
     │         └──► starlight-cosmos-engine ─────────────► Cosmos narratives + worldbuilding
     │                   └──► starlight-intelligence-system ► Premium distribution
     │
     ├──► agentic-mind-os ──────────────────────────────► Daily lived intelligence
     │         └──► starlight-mind-os-pro ───────────────► Premium personal OS
     │
     ├──► research-intelligence-os ─────────────────────► Runtime contracts & templates
     │         └──► research-intelligence-systems ────────► Cross-domain portfolio
     │                   ├──► psychology-ris ─────────────► Psychology vertical
     │                   └──► neuroscience-ris ─────────────► Neuroscience vertical
     │
     ├──► gencreator-ai ────────────────────────────────► Creative MCP + campaigns
     │
     └──► Infrastructure Layer
               ├──► claude-skills ──────────────────────► Skill primitives for all agents
               ├──► ai-architect ───────────────────────► Architecture intelligence
               ├──► family-guardians ────────────────────► Protection sentinels
               └──► multi-agent-harness ────────────────► Orchestration runtime
```

**HMIS primitives power:**
- Creative agents in Arcanea and Starlight Cosmos
- Campaign intelligence in GenCreator
- Guardian sentinels across family nodes
- Cosmos pipelines for worldbuilding
- Skill primitives in claude-skills
- Architecture intelligence in ai-architect
- Orchestration routing in multi-agent-harness

---

## ✦ Data Flow Contracts

### From HMIS to All Repos
Every repo that consumes the human mind model must declare `consumes_hmis_modules` in its manifest:

```yaml
consumes_hmis_modules:
  - attention
  - memory
  - emotion
  # ... etc
```

### From claude-skills to Agent Repos
Repos that use Claude-based agents must declare `uses_claude_skills` in their manifest:

```yaml
uses_claude_skills:
  - extract-claims
  - synthesize-research
  # ... etc
```

### From multi-agent-harness to Complex Workflows
Repos using multi-agent orchestration must declare:

```yaml
uses_harness: true
harness_patterns:
  - sequential
  - parallel
  - hierarchical
```

---

## ✦ Protection & Governance

### Who Governs the Mesh
The mesh is governed by **frankxai** as the sovereign founder. Changes to the mesh require:
1. PR to `mind-intelligence-systems` on a `hermes/foundation-*` branch
2. Updated `repo-mesh.yaml` (machine-readable)
3. Updated `REPO_MESH.md` (this document)
4. Explicit description of dependency additions/removals

### Agents and the Mesh
Agents entering any frankxai repo must:
1. Read `repo-mesh.yaml` first — it is the authoritative machine-readable map
2. Never create new repo references without updating `REPO_MESH.md` and `repo-mesh.yaml`
3. Never fork the human mind model — always consume from `models/human-mind/`
4. Reference this document when creating cross-repo features

### Mesh Integrity Rules
- No circular dependencies (enforced by review)
- All repos must declare `depends_on` honestly
- Canon (`mind-intelligence-systems`) has zero external dependencies
- Protection repos (`family-guardians`) may not depend on creative repos

---

## ✦ Empire Scale Vision

This mesh is designed to scale to:
- **50+ repos** across the frankxai namespace
- **Billions of end-users** through product and OS layers
- **Thousands of agents** orchestrated through the harness
- **Decades of compounding intelligence** through the canon layer

Every node added to this constellation must honor the naming doctrine, respect the dependency hierarchy, and contribute to — not fragment — the empire.

---

## ✦ Mesh Version History

| Version | Date | Change |
|---------|------|--------|
| v1.0 | 2026-01 | Initial mesh: 7 repos |
| v2.0 | 2026-06 | Expanded: added Arcanea, Starlight, GenCreator stubs |
| v3.0 | 2026-06-18 | Full empire: claude-skills, ai-architect, family-guardians, multi-agent-harness, complete cross-leverage map, protection layers, empire vision |

---

*This mesh is the nervous system of the frankxai empire. Every connection is intentional. Every dependency is a promise.*
*— frankxai Sovereign Intelligence Empire*
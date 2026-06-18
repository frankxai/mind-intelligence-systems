# Mind Intelligence Systems

**Mind Intelligence Systems** is the umbrella architecture for agentic systems that help humans understand, structure, improve, and extend learning, self-understanding, psychology, neuroscience, research, and human development.

This repo is the **canon layer** — not a product itself, but the source of truth for naming, models, governance, and the mesh that holds every sibling repo in coherent relationship.

---

## Purpose

This is the highest node in a swarm of eight repositories. Its job is threefold:

1. **Name things correctly.** The [Naming Doctrine](./NAMING_DOCTRINE.md) defines what OS, System, and Systems mean across the portfolio and prevents drift as repos multiply.
2. **Hold the shared model.** `models/human-mind/` contains the modular ontology of cognition, affect, and behavior that every agent in the swarm can import as ground truth.
3. **Map the mesh.** `repo-mesh.yaml` and `REPO_MESH.md` define which repos depend on which, what they provide, and how data flows between them. Any coding agent entering the swarm reads this first.

Without this repo, each sibling would name things independently, model the mind inconsistently, and lose track of how their work relates to neighboring systems. This repo prevents that from happening.

---

## The Portfolio

| Repo | What it is | Primary Audience |
|------|-----------|-----------------|
| **[mind-intelligence-systems](https://github.com/frankxai/mind-intelligence-systems)** *(this repo)* | Umbrella canon, naming, models, governance | Agents and architects |
| **[agentic-mind-os](https://github.com/frankxai/agentic-mind-os)** | Personal second-brain OS — lived daily | Individual practitioners |
| **[research-intelligence-os](https://github.com/frankxai/research-intelligence-os)** | Reusable runtime: contracts, templates, evals | Developers, domain system builders |
| **[research-intelligence-systems](https://github.com/frankxai/research-intelligence-systems)** | Cross-domain research portfolio layer | Researchers, analysts |
| **[psychology-research-intelligence-system](https://github.com/frankxai/psychology-research-intelligence-system)** | Psychology vertical: constructs, evidence, psychometrics | Psychology researchers |
| **[neuroscience-research-intelligence-system](https://github.com/frankxai/neuroscience-research-intelligence-system)** | Neuroscience vertical: BIDS, NWB, MNE, reproducible pipelines | Neuroscience researchers |
| **[awesome-mind-agent-skills](https://github.com/frankxai/awesome-mind-agent-skills)** | Curated discovery layer and ecosystem map | Anyone entering the swarm |
| **[starlight-mind-os-pro](https://github.com/frankxai/starlight-mind-os-pro)** | Premium distribution, dashboards, onboarding, workshops | Customers, learners |

See [ARCHITECTURE.md](./ARCHITECTURE.md) for the layered diagram and [REPO_MESH.md](./REPO_MESH.md) for explicit dependency flows.

---

## How People Experience It

The swarm is felt differently depending on how you enter it.

### Daily (Personal Practitioner)
A person running **Agentic Mind OS** interacts with the swarm through their vault, agents, and review sessions. They may not know this repo exists — they experience it through the consistent language and structured prompts that agents use. Every time a mind-cartographer agent asks them about their attention or belief state, it is drawing on vocabulary from `models/human-mind/`.

### Weekly (Researcher)
A researcher using the **Psychology** or **Neuroscience Research Intelligence System** runs structured literature sessions, construct mappings, and evidence synthesis workflows. The shared model layer ensures that when their psychology system names a construct like `working memory` or `emotional regulation`, it aligns with the same constructs tracked in the neuroscience system.

### Periodic (Developer / Agent Contributor)
A developer adding a new skill or extending a domain system opens `repo-mesh.yaml` to understand where their new piece fits, checks `NAMING_DOCTRINE.md` to name it correctly, and references `models/human-mind/` when building agent prompts that reason about cognition.

### First Time (New User / New Agent)
Start with [awesome-mind-agent-skills](https://github.com/frankxai/awesome-mind-agent-skills) for a curated map of everything. Then install Agentic Mind OS for personal use, or Research Intelligence OS if building a domain system. Return to this repo only when you need to understand the canonical doctrine.

---

## How Agents Explore This Repo

Coding agents (Codex, Claude Code, Gemini, Hermes) entering the swarm should:

1. **Read `repo-mesh.yaml`** — machine-readable mesh: which repos exist, what they depend on, what they provide, and which models are canonical.
2. **Read `AGENTS.md`** — agent-specific guidance for working in this repo without violating governance.
3. **Scan `models/human-mind/`** — each module file (`attention.md`, `memory.md`, etc.) contains: Definition, Key Processes, Related Constructs, Research Notes, and Agent Prompts. These are reusable in any agent system prompt.
4. **Check `.codex/tasks.md`** — the live queue of concrete tasks awaiting execution, labeled `MIS-XXX`.
5. **Consult `NAMING_DOCTRINE.md`** before creating any file, folder, variable, or PR title.

Agents should **not** create clinical or diagnostic content, and should always separate observation from interpretation.

See [docs/AGENT_EXPLORATION.md](./docs/AGENT_EXPLORATION.md) for example prompts and exploration paths.

---

## Human Mind Model

The shared ontology lives in `models/human-mind/`. Each module is a Markdown spec designed for both human reading and agent consumption.

| Module | Domain |
|--------|--------|
| [attention.md](./models/human-mind/attention.md) | Selective and executive attention |
| [memory.md](./models/human-mind/memory.md) | Working, episodic, semantic, procedural memory |
| [emotion.md](./models/human-mind/emotion.md) | Affect, appraisal, regulation |
| [motivation.md](./models/human-mind/motivation.md) | Goal pursuit, self-determination, volition |
| [identity.md](./models/human-mind/identity.md) | Self-concept, narrative identity |
| [learning.md](./models/human-mind/learning.md) | Acquisition, consolidation, transfer |
| [belief.md](./models/human-mind/belief.md) | Epistemic states, revision, bias |
| [behavior.md](./models/human-mind/behavior.md) | Habit, action, implementation intentions |
| [consciousness.md](./models/human-mind/consciousness.md) | Awareness, self-monitoring |
| [metacognition.md](./models/human-mind/metacognition.md) | Thinking about thinking |
| [decision-making.md](./models/human-mind/decision-making.md) | Dual-process, prospect theory, choice |
| [social-cognition.md](./models/human-mind/social-cognition.md) | Theory of mind, norms, intergroup |

See [models/human-mind/README.md](./models/human-mind/README.md).

---

## Usefulness

This repo is useful in three modes:

**For humans building products:** it answers the question "how should we model the mind across our agent fleet?" without requiring each team to rediscover cognitive science. The models are pre-structured for agent consumption and grounded in research literature.

**For agents working the swarm:** it provides naming contracts and model modules that can be imported verbatim into system prompts, ensuring vocabulary consistency across Agentic Mind OS, the research systems, and any future repos.

**For the portfolio as a whole:** it is the governance layer that prevents naming drift, model forking, and incoherence as the swarm grows.

See [docs/USEFULNESS.md](./docs/USEFULNESS.md) for case examples and concrete benefits per audience.

---

## Naming Doctrine

- **OS** is lived (personal operating systems and daily practice).
- **System** is engineered (a focused, installable product).
- **Systems** is a category (portfolio or reusable layer).

See [NAMING_DOCTRINE.md](./NAMING_DOCTRINE.md) for the full doctrine.

---

## Core Principles

- Markdown-first and GitHub-native.
- Agent-readable (Codex, Claude, Gemini, Hermes) and human-readable.
- Local-first where sensitive data or personal canon lives.
- Source-grounded for research claims.
- Never clinical diagnosis — observation, interpretation, hypothesis, evidence, and decision are separated.
- Build reusable packs (MindPack protocol) not ad-hoc templates.
- Clear folder structures over premature app complexity.

---

## Repository Mesh

See [REPO_MESH.md](./REPO_MESH.md) and `repo-mesh.yaml`.

---

## Next Steps

1. Agents: read `AGENTS.md`, then `.codex/tasks.md` for open tasks.
2. New users: start with [awesome-mind-agent-skills](https://github.com/frankxai/awesome-mind-agent-skills).
3. Practitioners: install [Agentic Mind OS](https://github.com/frankxai/agentic-mind-os).
4. Researchers: start from [Research Intelligence OS](https://github.com/frankxai/research-intelligence-os), then pick a domain system.
5. Premium track: see [Starlight Mind OS Pro](https://github.com/frankxai/starlight-mind-os-pro).

**Status**: Foundation v0 seeded. Doctrine, models, and mesh are stable. Domain systems are in active development.

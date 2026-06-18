# User Experience — Mind Intelligence Systems

This document describes how different types of people encounter and use the Mind Intelligence Systems swarm, from first contact to fluent daily practice.

---

## Who Uses This Swarm

| Person | Primary Repo | Entry Point |
|--------|-------------|-------------|
| Personal practitioner | Agentic Mind OS | Daily vault sessions |
| Academic / researcher | Psychology or Neuroscience Research Intelligence System | Literature workflows |
| Developer / contributor | Research Intelligence OS | Runtime contracts |
| Premium learner | Starlight Mind OS Pro | Guided onboarding |
| New explorer | Awesome Mind Agent Skills | Curated ecosystem list |
| Coding agent (Codex/Claude) | This repo first | `repo-mesh.yaml` + `AGENTS.md` |

---

## Journey 1 — Personal Practitioner

**Goal**: Build a personal second brain that understands your mind, supports learning, and tracks your development over time.

### Onboarding

1. Clone or install [Agentic Mind OS](https://github.com/frankxai/agentic-mind-os) following its `INSTALL.md`.
2. Open the vault template and fill in your `profile.md` — current focus areas, active projects, cognitive strengths and weaknesses.
3. Run the first mind-cartographer session: the agent will ask structured questions about your attention, motivation, and current learning load, drawing vocabulary from `models/human-mind/`.
4. Review the generated mind map of your cognitive state.

### Daily Use

- **Morning**: Open your Agentic Mind OS vault. Run the daily-focus agent to identify where your attention should go given current projects and energy levels.
- **During work**: Capture notes in the structured format the system provides. Notes are tagged by cognitive domain (belief updates, new memory traces, emotional state shifts).
- **Evening**: Run the consolidation agent to process the day's captures into durable memory entries and surface patterns.

### Weekly Use

- Run the weekly review agent: it synthesizes daily notes, highlights belief shifts, flags motivation dips, and proposes next-week focus areas.
- Review the learning log — what you practiced, what consolidated, what's at risk of decay.
- Check the emotion/motivation trend chart (if using Starlight Mind OS Pro dashboards).

### What the Swarm Provides Behind the Scenes

The mind model in `models/human-mind/` ensures that the vocabulary the agents use — attention, consolidation, implementation intentions, appraisal — is consistent with research-grounded definitions. When you use the psychology research system later, you won't need to re-learn a different vocabulary.

---

## Journey 2 — Academic Researcher

**Goal**: Run structured literature reviews, synthesize evidence across studies, map psychological constructs, and build reusable research workflows.

### Onboarding

1. Install [Research Intelligence OS](https://github.com/frankxai/research-intelligence-os) first — it is the runtime layer all domain systems depend on.
2. Clone the relevant domain system: [Psychology Research Intelligence System](https://github.com/frankxai/psychology-research-intelligence-system) or [Neuroscience Research Intelligence System](https://github.com/frankxai/neuroscience-research-intelligence-system).
3. Read that repo's `AGENTS.md` to understand available agents, and `ARCHITECTURE.md` to understand the domain-specific pipeline.
4. Run the onboarding workflow to configure your institutional access, citation manager, and vault path.

### Research Session (Weekly Rhythm)

1. **Identify constructs**: Use the construct-mapping agent. It references `models/human-mind/` to ensure the constructs you're studying align with the swarm's shared ontology.
2. **Literature pass**: Run the literature agent with a construct name and a date range. It returns structured summaries tagged with evidence strength, methodology, and relevant claims.
3. **Synthesis**: Feed summaries into the synthesis agent. It produces a claim graph — a structured representation of what the literature says and how confidently.
4. **Package**: Export the session as a ResearchPack for reuse in future workflows or sharing with collaborators.

### Neuroimaging Workflow (Neuroscience vertical)

1. Point the BIDS agent at a local dataset directory.
2. Run the preprocessing pipeline agent — it generates an MNE or NWB workflow based on the dataset structure.
3. Use the reproducibility checklist agent to verify pipeline steps against OpenNeuro standards.
4. Archive the pipeline as a reusable ResearchPack.

---

## Journey 3 — Developer / Contributor

**Goal**: Build a new domain system (e.g., a sleep research system), contribute to existing systems, or extend the runtime layer.

### Onboarding

1. Read this repo's `AGENTS.md` and `NAMING_DOCTRINE.md` fully.
2. Open `repo-mesh.yaml` to understand where your new repo fits in the dependency graph.
3. Read `ARCHITECTURE.md` to understand the seven layers and where your contribution lives.
4. Check `.codex/tasks.md` for open `MIS-` tasks that need doing before you add new capabilities.

### Creating a New Domain System

1. Start from the Research Intelligence OS template. Do not start from scratch — the runtime contracts define the pipeline grammar every system must follow.
2. Name the repo `<domain>-research-intelligence-system` following the naming doctrine.
3. Add your repo to `repo-mesh.yaml` with correct `depends_on` and `provides` fields, then open a PR to this repo.
4. Reference the relevant mind model modules from `models/human-mind/` in your agent system prompts.

### Contributing to an Existing System

1. Check that system's `.codex/tasks.md` for its open task queue.
2. Work on a branch named `agent/<harness>/<short-scope>`.
3. When changing model content or naming, always update this repo's model files and open a cross-repo PR reference.

---

## Journey 4 — Premium User (Starlight Mind OS Pro)

**Goal**: Get a guided, curated experience on top of Agentic Mind OS with polished dashboards, onboarding workshops, and commercial templates.

### Onboarding

1. Access the Starlight Mind OS Pro onboarding pack from [its repo](https://github.com/frankxai/starlight-mind-os-pro).
2. Follow the 7-day onboarding workshop: each day introduces one cognitive domain from the mind model (attention, memory, emotion, motivation, identity, learning, metacognition).
3. Install the dashboard templates into your vault.

### Ongoing Use

- Weekly dashboard review: see your cognitive domain scores, learning streaks, emotion trends.
- Access curated workshops on topics like "deep focus protocol" or "belief revision practice".
- Use the premium agent skills catalog — higher-fidelity versions of the base agents.

---

## Onboarding Checklist (Any User)

```
[ ] Identify your entry point (personal, research, developer, premium)
[ ] Clone the right repo (Agentic Mind OS, Research Intelligence OS, or domain system)
[ ] Read README.md and AGENTS.md of that repo
[ ] Check .codex/tasks.md for open work
[ ] Run the first agent session to orient yourself
[ ] Return to this repo (mind-intelligence-systems) only when you need doctrine or model definitions
```

---

## Common Misconceptions

**"I need to read this repo before using the swarm."**
No — start with your target repo. This repo is the governance layer, not the entry point. Developers and agents need it; practitioners usually don't.

**"The mind model is a clinical tool."**
No — it is a descriptive/research model for structuring agent prompts and organizing knowledge. It does not diagnose. See the guardrails in `models/human-mind/README.md`.

**"Each repo works alone."**
Some do (Agentic Mind OS has standalone value), but they are significantly more powerful when connected. The research systems depend on Research Intelligence OS for their runtime, and all agents are more coherent when they share the vocabulary from `models/human-mind/`.

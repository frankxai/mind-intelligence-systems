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

**Goal**: Build a personal second brain that organizes your notes by construct, supports learning, and keeps a record of what you write over time.

### Onboarding

1. Clone [Agentic Mind OS](https://github.com/frankxai/agentic-mind-os) and follow the quick start in its README.
2. Copy `vault-templates/` to `~/mind-vault` and open it as your vault.
3. After a few days of daily notes, run `/map-mind`. The mind-cartographer agent sorts what you wrote across the twelve constructs, using vocabulary from `models/human-mind/`.
4. Review the map note it writes to `reviews/`. It is a reading of your notes, not an assessment.

### Daily Use

- **Morning**: Open your vault. Run `/dawn` for the priming prompts, or ask the focus-coach agent to set up your next work block.
- **During work**: Capture notes in the daily template and tag the constructs each note touches on the `constructs::` line.
- **Evening**: Run `/dusk` for the reflection prompts. Patterns across days surface in the weekly `/review-week`.

### Weekly Use

- Run `/review-week`: the weekly-reviewer agent consolidates the week's notes by construct, names learnings, and proposes one to three carry-forwards.
- Review the recall sets the recall-builder writes to `reviews/` for anything you want to keep.
- If you use Starlight Mind OS Pro, its dashboard specs describe a weekly-review view and a construct-coverage view. The specs ship without running dashboards or sample data.

### What the Swarm Provides Behind the Scenes

The mind model in `models/human-mind/` keeps the vocabulary the agents use — attention, consolidation, implementation intentions, appraisal — consistent across repos, and each module points to the research it draws on. The planned psychology research system is meant to reuse the same vocabulary.

---

## Journey 2 — Academic Researcher

> **Status:** `research-intelligence-os` and the psychology and neuroscience systems are `planned` in `repo-mesh.yaml`. This journey describes the intended workflow, not a shipped one.

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

**Goal**: Get a guided path on top of Agentic Mind OS: onboarding, dashboard specs, workshop outlines, and commercial templates.

### Onboarding

1. Access the Starlight Mind OS Pro onboarding pack from [its repo](https://github.com/frankxai/starlight-mind-os-pro).
2. Follow the first-7-days onboarding: each day is one small action mapped to a step of the core loop (capture, daily review, weekly review).
3. Use the dashboard specs in `dashboards/` to build views over your vault. The repo ships specs, not running dashboards.

### Ongoing Use

- Weekly dashboard review: the spec describes a cadence strip, a follow-through line, and the themes the agent surfaced. It shows no scores or grades.
- Workshops: a half-day outline, "Build Your Mind OS", for live or self-paced delivery.
- Commercial templates: a client-onboarding checklist for practitioners who set up the core for others.

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
Some do (Agentic Mind OS runs on its own). Connected repos share one vocabulary from `models/human-mind/`. The planned research systems depend on Research Intelligence OS for their runtime.

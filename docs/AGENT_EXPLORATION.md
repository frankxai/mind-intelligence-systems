# Agent Exploration Guide — Mind Intelligence Systems

This guide is for coding agents (Codex, Claude Code, Gemini, Hermes) entering the swarm. It describes how to navigate the repo, reference the mind model, read the mesh, and contribute correctly.

---

## Start Here: Five Required Reads

Every agent working in this swarm should read these in order before doing anything else:

1. `repo-mesh.yaml` — canonical machine-readable mesh (repos, dependencies, model paths)
2. `AGENTS.md` — agent-specific governance for this repo
3. `NAMING_DOCTRINE.md` — strict naming rules for every file, folder, and PR
4. `ARCHITECTURE.md` — the seven-layer architecture
5. `.codex/tasks.md` — the open task queue for this repo

---

## Reading `repo-mesh.yaml`

`repo-mesh.yaml` is the single most important file for an agent entering this swarm.

```yaml
# What to look for:
umbrella: "mind-intelligence-systems"   # you are here

repos:
  - name: "agentic-mind-os"
    role: "personal-os"
    depends_on: [...]                   # what this repo needs
    provides: [...]                     # what it contributes

models:
  human_mind:
    path: "models/human-mind/"          # where the shared ontology lives
    modules: [attention, memory, ...]   # all available modules
```

Key questions to answer from this file:
- What does the repo I'm building depend on?
- What does it need to provide to stay coherent with the mesh?
- Which model modules are relevant to the agents I'm building?

---

## Navigating `models/human-mind/`

Each module file follows the same structure:

```
## Definition
## Key Processes
## Related Constructs
## Research Notes
## Agent Prompts / Usage
```

### When to reference a module

| Task | Module to read |
|------|---------------|
| Building a focus or productivity agent | attention.md |
| Building a review or spaced repetition system | memory.md |
| Building a mood tracking or regulation feature | emotion.md |
| Building a goal-setting or habit agent | motivation.md, behavior.md |
| Building a journaling or self-concept tool | identity.md |
| Building a learning path or skill tracking tool | learning.md |
| Building a note-synthesis or argument-mapping tool | belief.md |
| Building a decision-support agent | decision-making.md |
| Building a research reasoning workflow | metacognition.md |
| Building a collaboration or multi-agent coordination tool | social-cognition.md |

### How to use a module in a system prompt

Copy the Definition and Agent Prompts sections into your agent's system prompt verbatim, then adapt. Example:

```
[From attention.md — Definition]
Attention is the selective allocation of cognitive resources to specific stimuli,
thoughts, or actions while filtering others.

[Agent instruction derived from Agent Prompts section]
When the user describes their workday, identify what they are attending to versus
what they are ignoring. Flag attentional bottlenecks that may be degrading their
learning or task completion.
```

This ensures every agent across the swarm uses research-grounded, consistent vocabulary.

---

## Example Exploration Paths

### Path A: Codex task from `.codex/tasks.md`

```
1. Read .codex/tasks.md
2. Pick a task (e.g., MIS-001: expand decision-making module)
3. Read the referenced file (models/human-mind/decision-making.md)
4. Read a completed module (belief.md) to understand the target structure
5. Implement following the template — Definition, Key Processes, Related Constructs,
   Research Notes, Agent Prompts
6. Open a PR on branch hermes/foundation-v0 with label "model"
```

### Path B: Adding a new module

```
1. Verify the module is listed in repo-mesh.yaml under models.human_mind.modules
2. If not, add it there first
3. Create the module file following the existing template
4. Add it to models/human-mind/README.md module list
5. Cross-reference it from any sibling module where it appears in Related Constructs
6. Open PR; update .codex/tasks.md to mark the source task done
```

### Path C: Auditing naming doctrine compliance

```
1. Read NAMING_DOCTRINE.md fully
2. Search all .md files for incorrect usage:
   - "OS" applied to a system or category product
   - "System" applied to a portfolio layer
   - "Systems" applied to a single installable product
3. Fix and note the files changed
4. This corresponds to task MIS-012
```

### Path D: Contributing a new domain system repo

```
1. Read repo-mesh.yaml to understand what role "domain-system" means
2. Verify Research Intelligence OS is the base — your new system depends_on it
3. Name the new repo: <domain>-research-intelligence-system
4. Notify this repo by opening a PR that adds the new entry to repo-mesh.yaml
5. Reference relevant models/human-mind/ modules in your agent prompts
```

### Path E: Deriving JSON schemas from model files

```
1. Read MIS-003 in .codex/tasks.md
2. Read models/human-mind/attention.md, memory.md, emotion.md (at minimum)
3. Identify the key properties of each construct: definition, key processes, related constructs
4. Produce draft schemas in models/human-mind/schemas/
   - construct.schema.json (for any module)
   - note.schema.json (for agent-captured notes about mind state)
5. Document the schemas in models/human-mind/README.md
```

---

## Example Agent Prompts for Exploring This Repo

These prompts can be used to instruct another agent to work within this repo.

**To onboard a new agent:**
```
Read repo-mesh.yaml in mind-intelligence-systems, then AGENTS.md, NAMING_DOCTRINE.md,
and ARCHITECTURE.md. Report back: (a) what this repo's role is, (b) which repos depend
on it, (c) what the naming rule for OS vs System vs Systems is, and (d) list the
available modules in models/human-mind/.
```

**To expand a model module:**
```
Read models/human-mind/belief.md and models/human-mind/metacognition.md as style
references. Then expand models/human-mind/decision-making.md to match the same
structure: Definition, Key Processes (at least 4), Related Constructs, Research Notes
(cite classic models — dual-process, prospect theory, implementation intentions),
and Agent Prompts with concrete usage examples. Follow all guardrails in
models/human-mind/README.md. No clinical or diagnostic language.
```

**To check a PR for doctrine compliance:**
```
Read NAMING_DOCTRINE.md. Then review the diff for any file naming, folder naming,
or prose that uses OS, System, or Systems incorrectly. Report violations with the
file path and line number.
```

**To generate a system prompt fragment for a new agent:**
```
Read models/human-mind/motivation.md and models/human-mind/behavior.md.
Extract the Definition and Agent Prompts sections from each. Compose a system
prompt fragment for a habit-tracking agent that can identify motivation states,
spot implementation intentions, and surface behavioral patterns in user notes.
Keep language descriptive and research-grounded. No diagnosis.
```

---

## Governance Rules for Agents

1. **Never commit to `main` directly.** Use `hermes/foundation-*` branches or `agent/<harness>/<scope>`.
2. **Never create clinical or diagnostic content.** The guardrail is in `AGENTS.md` and `models/human-mind/README.md`.
3. **Never name a file, folder, or variable without checking `NAMING_DOCTRINE.md` first.**
4. **Always update `repo-mesh.yaml` when adding a new repo to the swarm.**
5. **When changing core model files, check for downstream impact** — search for references in `.codex/tasks.md` and sibling module files.
6. **Mark Codex tasks done** in `.codex/tasks.md` when you complete them. Add new tasks if you discover work that isn't tracked.

---

## Quick Reference: File Purposes

| File | Purpose |
|------|---------|
| `repo-mesh.yaml` | Machine-readable mesh — read first |
| `AGENTS.md` | Agent governance and acceptance criteria |
| `NAMING_DOCTRINE.md` | Strict naming rules |
| `ARCHITECTURE.md` | Seven-layer architecture |
| `REPO_MESH.md` | Human-readable mesh with dependency table |
| `HERMES.md` | Hermes orchestrator context |
| `CONTRIBUTING.md` | Contribution workflow |
| `ROADMAP.md` | Where the swarm is going |
| `.codex/tasks.md` | Open task queue |
| `models/human-mind/*.md` | Modular mind ontology — agent-importable |
| `models/human-mind/README.md` | Ontology overview and usage guide |

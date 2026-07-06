# Codex Handover — Human Atlas

**Date**: 2026-07-06  
**Owner**: frankxai  
**Primary repo**: `frankxai/mind-intelligence-systems`  
**Branch suggested**: `codex/human-atlas-system-20260706`  
**Operating mode**: repo-aware, SIP-aligned, non-clinical, markdown-first

---

## Copy/paste prompt for Codex

```text
You are Codex operating across the frankxai Mind Intelligence / Starlight / Arcanea / FrankX GitHub portfolio.

Your task is to implement the first coherent Human Atlas layer: a comprehensive human development system that expands the current twelve-module human-mind model into a richer atlas covering:

- Core Qualities
- Values
- Virtues
- Talents
- Skills
- Motivations
- Needs
- Personality Traits
- Shadow Qualities
- Pitfalls
- Allergies & Sensitivities
- Physical / Environmental Sensitivities
- Emotional Patterns
- Attachment Styles
- Cognitive Biases
- Defense Mechanisms
- Trauma Responses
- Habits
- Communication Styles
- Leadership Styles
- Learning Styles

This is NOT a clinical or diagnostic system. Preserve the five-stage boundary everywhere:

observation -> interpretation -> hypothesis -> evidence -> decision

Do not use disorder labels, treatment advice, clinical claims, or deterministic identity language. Use tentative, evidence-bound developmental language. Interpretation confidence must never exceed observation confidence.

Start in `frankxai/mind-intelligence-systems`.

First read:

- README.md
- NAMING_DOCTRINE.md
- repo-mesh.yaml
- REPO_MESH.md
- AGENTS.md
- docs/HUMAN_ATLAS.md
- models/human-mind/README.md
- representative files in `models/human-mind/`

Then implement:

1. Create `models/human-atlas/README.md`.
2. Create `models/human-atlas/index.yaml`.
3. Create `models/human-atlas/dimensions/` with one markdown file per Human Atlas dimension.
4. Use this exact dimension file structure:
   - Definition
   - Developmental Function
   - Observable Signals
   - Growth Edges
   - Shadow Distortions
   - Related Human-Mind Constructs
   - Related Human-Atlas Dimensions
   - Evidence Requirements
   - Agent Usage
   - Guardrails
5. Patch `repo-mesh.yaml` to add `human_atlas` under `models`.
6. Patch `README.md` and `models/human-mind/README.md` with a short Human Atlas pointer.
7. Add a task block to `.codex/tasks.md` for downstream repo rollout.

Acceptance criteria in the canon repo:

- All 20+ dimensions exist.
- No clinical claims.
- No private personal data.
- Markdown is direct, high-signal, agent-readable.
- YAML is valid and names are kebab-case or snake_case consistently.
- Human Atlas is clearly positioned as an applied developmental atlas above the twelve human-mind constructs, not a replacement.

After the canon repo passes, move to `frankxai/human-mind-intelligence-system`.

Read:

- README.md
- AGENTS.md
- CLAUDE.md
- schemas/README.md
- ontology/ontology.md
- docs/response-prediction.md

Implement:

1. `schemas/human-atlas/profile.schema.json`
2. `schemas/human-atlas/observation.schema.json`
3. `schemas/human-atlas/dimension.schema.json`
4. `schemas/human-atlas/hypothesis.schema.json`
5. `schemas/human-atlas/experiment.schema.json`
6. `ontology/human-atlas.md`
7. `docs/human-atlas-response-prediction.md`
8. README pointer to Human Atlas schemas

Schema constraints:

- JSON Schema draft 2020-12.
- Observation stores raw observation separately from interpretation.
- Hypothesis references observations and evidence.
- Experiment is reversible, time-boxed, and human-owned.
- Include `confidence` as number 0-1.
- Include `evidence_for`, `evidence_against`, and `alternative_explanations`.

Then move to `frankxai/agentic-mind-os`.

Read:

- README.md
- CANON.md
- MEMORY.md
- mindpack.yaml
- vault-templates/README.md
- existing agents and commands

Implement:

1. `vault-templates/human-atlas/README.md`
2. `vault-templates/human-atlas/profile.md`
3. `vault-templates/human-atlas/daily-capture.md`
4. `vault-templates/human-atlas/weekly-review.md`
5. `vault-templates/human-atlas/experiments.md`
6. `agents/human-atlas-cartographer.md`
7. `agents/growth-experiment-designer.md`
8. `commands/map-human-atlas.md`
9. `commands/review-human-atlas.md`
10. Patch `mindpack.yaml` to provide `human-atlas-vault-templates`, `human-atlas-agents`, and `human-atlas-commands`.

Lived OS constraints:

- Local-first.
- The user owns all decisions.
- Agents observe and hypothesize; they do not diagnose.
- Templates must invite reflection without coercion.
- Weekly review must include evidence for and evidence against each pattern.

Then move to `frankxai/agentic-creator-os`.

Read:

- README.md
- SHARING.md
- skill-rules.json
- existing `.claude/skills/*/SKILL.md`
- existing `.claude/commands/*`

Implement:

1. `.claude/skills/human-atlas-system/SKILL.md`
2. `.claude/commands/human-atlas.md`
3. Optional `.claude/agents/human-atlas-cartographer.md` if agent conventions match.
4. Patch skill activation rules for terms like:
   - human atlas
   - values map
   - shadow pattern
   - learning style
   - leadership style
   - communication style
   - cognitive bias
   - growth experiment
   - attachment pattern
   - emotional pattern

ACOS constraints:

- This is a skill/command, not a therapy persona.
- Add a safety note that the command cannot diagnose.
- The command should route to canon-first analysis, then produce artifacts.

Then move to optional public/product repos only after core model is stable.

For `frankxai/frankx.ai-vercel-website`:

- Add a product/content planning doc first, not a public page unless current content architecture clearly supports it.
- Suggested doc: `docs/human-atlas-product-surface.md`
- Explain offer ladder:
  - free Human Atlas map
  - paid workbook/template
  - premium founder/operator Human Atlas
  - Starlight Mind OS Pro integration

For `frankxai/arcanea`:

- Add a planning doc first.
- Suggested doc: `docs/human-atlas-arcanea-archetypes.md`
- Map values, virtues, shadows, talents, and leadership styles into Arcanea archetypal progression.
- Do not contaminate canon with lore. Arcanea adapts the Human Atlas mythopoetically; it does not own the model.

For `frankxai/Starlight-Intelligence-System`:

- Add only a memory/tagging integration note unless code changes are obviously required.
- Suggested doc: `docs/human-atlas-starlight-integration.md`
- Do not create a seventh semantic vault in the first pass.
- Use tags/categories inside existing vaults first.
- Preserve SIP attestation and sovereignty clauses.

General working rules:

- Always read before editing.
- Prefer small PRs per repo.
- Keep canonical definitions in `mind-intelligence-systems`; downstream repos reference them.
- Do not duplicate long canon text across repos.
- Keep all language non-clinical.
- Add acceptance criteria to every PR body.
- Run available lint/type/schema validation commands before finalizing.
- Do not commit private journals, personal data, or generated profile examples that look like real people.

Output expected:

1. One PR in `mind-intelligence-systems` stabilizing the canon.
2. One PR in `human-mind-intelligence-system` adding schemas and ontology.
3. One PR in `agentic-mind-os` adding the lived templates, agents, and commands.
4. One PR in `agentic-creator-os` adding skill/command activation.
5. Optional planning PRs in FrankX, Arcanea, and Starlight after the core three pass.
```

---

## Repo-by-repo task queue

### `mind-intelligence-systems`

**Task ID prefix**: `MIS-HA`

```text
MIS-HA-001: Create Human Atlas model directory and index.
Files:
- models/human-atlas/README.md
- models/human-atlas/index.yaml

MIS-HA-002: Create dimension files.
Files:
- models/human-atlas/dimensions/*.md

MIS-HA-003: Patch mesh and docs.
Files:
- repo-mesh.yaml
- README.md
- models/human-mind/README.md
- REPO_MESH.md if needed

MIS-HA-004: Add downstream rollout queue.
Files:
- .codex/tasks.md
```

### `human-mind-intelligence-system`

**Task ID prefix**: `HMIS-HA`

```text
HMIS-HA-001: Add Human Atlas schemas.
Files:
- schemas/human-atlas/profile.schema.json
- schemas/human-atlas/observation.schema.json
- schemas/human-atlas/dimension.schema.json
- schemas/human-atlas/hypothesis.schema.json
- schemas/human-atlas/experiment.schema.json

HMIS-HA-002: Add Human Atlas ontology.
Files:
- ontology/human-atlas.md

HMIS-HA-003: Add response-prediction extension.
Files:
- docs/human-atlas-response-prediction.md
- README.md
- AGENTS.md if agent guidance needs pointer
```

### `agentic-mind-os`

**Task ID prefix**: `AMOS-HA`

```text
AMOS-HA-001: Add local-first Human Atlas vault templates.
Files:
- vault-templates/human-atlas/README.md
- vault-templates/human-atlas/profile.md
- vault-templates/human-atlas/daily-capture.md
- vault-templates/human-atlas/weekly-review.md
- vault-templates/human-atlas/experiments.md

AMOS-HA-002: Add Human Atlas agents.
Files:
- agents/human-atlas-cartographer.md
- agents/growth-experiment-designer.md

AMOS-HA-003: Add commands.
Files:
- commands/map-human-atlas.md
- commands/review-human-atlas.md

AMOS-HA-004: Patch manifest/docs.
Files:
- mindpack.yaml
- README.md
- CANON.md
```

### `agentic-creator-os`

**Task ID prefix**: `ACOS-HA`

```text
ACOS-HA-001: Add Human Atlas skill.
Files:
- .claude/skills/human-atlas-system/SKILL.md

ACOS-HA-002: Add slash command.
Files:
- .claude/commands/human-atlas.md

ACOS-HA-003: Patch activation.
Files:
- skill-rules.json
```

### `Starlight-Intelligence-System`

**Task ID prefix**: `SIS-HA`

```text
SIS-HA-001: Add Human Atlas memory integration guidance.
Files:
- docs/human-atlas-starlight-integration.md

SIS-HA-002: Optional MCP metadata extension only after proving need.
Files:
- docs only in first pass unless tests require code.
```

### `frankx.ai-vercel-website`

**Task ID prefix**: `FX-HA`

```text
FX-HA-001: Draft product/content surface.
Files:
- docs/human-atlas-product-surface.md

FX-HA-002: Add public page only after content architecture review.
Candidate routes:
- /human-atlas
- /products/human-atlas
- /resources/human-atlas
```

### `arcanea`

**Task ID prefix**: `ARC-HA`

```text
ARC-HA-001: Draft mythopoetic adapter.
Files:
- docs/human-atlas-arcanea-archetypes.md

ARC-HA-002: Optional archetype content patch after canon stabilizes.
Candidate areas:
- lore
- academy
- worldbuilding
- character development
```

---

## Review checklist

Before opening each PR, verify:

- [ ] No clinical diagnosis or treatment language.
- [ ] Observation, interpretation, hypothesis, evidence, and decision remain separate.
- [ ] Canon definitions live in `mind-intelligence-systems`.
- [ ] Downstream repos reference canon instead of forking it.
- [ ] No personal/private data committed.
- [ ] File names match repo naming doctrine.
- [ ] Markdown is agent-readable.
- [ ] YAML/JSON is valid.
- [ ] README pointers are short and non-duplicative.
- [ ] PR body includes acceptance criteria and downstream dependencies.

---

## PR body template

```markdown
## Summary

Introduces the Human Atlas as the applied human-development layer above the canonical twelve-module human-mind model.

## Scope

- Canon / schema / lived OS / skill / product planning: <choose one>
- Non-clinical reflection and development only
- No private data

## Files changed

- ...

## Guardrails

- Observation, interpretation, hypothesis, evidence, and decision remain separate.
- No diagnostic or treatment language.
- Human decision rights preserved.

## Acceptance criteria

- [ ] ...
- [ ] ...
- [ ] ...

## Downstream dependencies

- ...
```

---

## Strategic interpretation

This should become the bridge between:

- cognitive science canon,
- lived journaling and self-review,
- agent memory,
- founder/operator development,
- Arcanea archetypal transformation,
- FrankX public authority,
- Starlight sovereign continuity.

Do not let it become a listicle. Do not let it become a personality quiz. Do not let it become therapy cosplay.

Make it a map that compounds.

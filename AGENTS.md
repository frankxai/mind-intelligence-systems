# AGENTS.md

## For Coding Agents (Codex, Claude Code, Gemini, etc.)

This is the governance and model layer for the entire swarm.

### Core Responsibilities
- Maintain consistent naming doctrine across all repos.
- Evolve the human mind model in `models/human-mind/`.
- Keep REPO_MESH.md and repo-mesh.yaml accurate.
- Seed high-quality foundational content that downstream repos can inherit.

### When Working Here
1. Always follow NAMING_DOCTRINE.md strictly.
2. Update this file and cross-reference when architecture changes.
3. Create modular, source-grounded model files (no clinical claims).
4. Add concrete Codex tasks to `.codex/tasks.md`.
5. Prefer small, reviewable PRs on `hermes/foundation-v0` branch.

### Acceptance Criteria for Changes
- Every new model file has clear sections: Definition, Key Processes, Related Constructs, Research Notes, Agent Prompts.
- Manifests (yaml) are valid and documented.
- Links to other repos in the swarm are present and correct.

## Human Mind Model Usage

Agents in other repos should reference:
- `mind-intelligence-systems/models/human-mind/<module>.md`
- Use consistent terminology from NAMING_DOCTRINE.

## Do Not
- Create clinical/therapeutic content.
- Diagnose.
- Overclaim.
- Mix observation with interpretation without labels.

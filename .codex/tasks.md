# Codex Task Queue — Mind Intelligence Systems (MIS)

**Repo Role**: Umbrella canon and human mind model.

Use task IDs starting with `MIS-`.

## MIS-001
**Objective**: Expand decision-making module with key processes, related constructs, research notes, and agent usage examples.
**Files**: models/human-mind/decision-making.md
**Acceptance Criteria**: File follows template from other modules; includes at least 4 key processes; references relevant psychology/neuroscience literature without clinical claims.
**Suggested Command**: `codex exec "Create models/human-mind/decision-making.md following the exact structure and guardrails of belief.md and metacognition.md. Add sections for dual-process, prospect theory, and implementation intentions."`
**Dependencies**: models/human-mind/ (existing modules)

## MIS-002
**Objective**: Create social-cognition module.
**Files**: models/human-mind/social-cognition.md
**Acceptance Criteria**: Covers theory of mind, social inference, norms, and intergroup processes at high level. Agent prompts for multi-agent or collaboration scenarios.
**Suggested Command**: Similar to MIS-001.
**Dependencies**: None

## MIS-003
**Objective**: Derive initial JSON schema for core mind constructs from the model files.
**Files**: models/human-mind/schemas/construct.schema.json, models/human-mind/schemas/note.schema.json (draft)
**Acceptance Criteria**: Valid JSON Schema; covers attention, memory, emotion, learning, belief at minimum; documented in README.
**Suggested Command**: `codex exec "Analyze models/human-mind/ and produce draft JSON schemas in a new schemas/ subdir. Start with construct.schema.json and note.schema.json."`

## MIS-004
**Objective**: Create initial MindPack validation script or checklist.
**Files**: scripts/validate-mindpack.py or docs/mindpack-validation.md
**Acceptance Criteria**: Script or doc that checks for required files in a MindPack (SKILL.md, .agent.md, schemas, etc).
**Suggested Command**: `codex exec "Create a simple validation tool or markdown checklist for MindPacks based on the protocol in NAMING_DOCTRINE.md."`

## MIS-005
**Objective**: Add cross-references from all model files to relevant research repos (psychology, neuroscience).
**Files**: All models/human-mind/*.md
**Acceptance Criteria**: Each module has a "Cross-Repo Links" section pointing to PRIS or NRIS workflows/agents where relevant.
**Suggested Command**: `codex exec "Update all human-mind modules to include 'Cross-Repo Links' sections referencing psychology-research-intelligence-system and neuroscience-research-intelligence-system."`

## MIS-006
**Objective**: Flesh out REPO_MESH.md with data flow diagrams (ASCII or mermaid) and dependency matrix.
**Files**: REPO_MESH.md
**Acceptance Criteria**: Includes mermaid or clear ASCII diagram; updated table.
**Suggested Command**: `codex exec "Enhance REPO_MESH.md with diagrams and explicit data flows between agentic-mind-os and research systems."`

## MIS-007
**Objective**: Create initial set of agent prompt templates derived from the human mind model.
**Files**: prompts/mind-model-prompts/ (new dir) or in models/
**Acceptance Criteria**: 3-5 reusable prompt snippets for cartographer, architect, analyst agents.
**Suggested Command**: `codex exec "Extract reusable prompt patterns from the model files into a prompts/ directory for use across the swarm."`

## MIS-008
**Objective**: Update ARCHITECTURE.md with layer diagram (mermaid) and clear separation of concerns.
**Files**: ARCHITECTURE.md
**Acceptance Criteria**: Visual diagram; updated description of flows.
**Suggested Command**: `codex exec "Add mermaid architecture diagram to ARCHITECTURE.md showing the 7 layers."`

## MIS-009
**Objective**: Seed first version of global mindpack.yaml example in this repo as reference.
**Files**: examples/mindpack-reference.yaml
**Acceptance Criteria**: Complete example manifest following the protocol.
**Suggested Command**: `codex exec "Create examples/ with a reference mindpack.yaml that other repos can copy."`

## MIS-010
**Objective**: Add decision-making and social-cognition to repo-mesh.yaml models section.
**Files**: repo-mesh.yaml
**Acceptance Criteria**: Updated list.
**Suggested Command**: `codex exec "Patch repo-mesh.yaml to include the two new modules."`

## MIS-011
**Objective**: Write a short "Getting Started for Agents" guide.
**Files**: AGENTS-FOR-CODEX.md or append to AGENTS.md
**Acceptance Criteria**: Clear 5-step process for an agent to contribute to the swarm starting from this repo.
**Suggested Command**: `codex exec "Create a dedicated guide for coding agents onboarding to the Mind Intelligence Systems swarm."`

## MIS-012
**Objective**: Audit all docs for strict adherence to naming doctrine and fix any violations.
**Files**: All .md files
**Acceptance Criteria**: "OS", "System", "Systems" used correctly everywhere; no contradictions.
**Suggested Command**: `codex exec "Perform a naming doctrine audit across the repo and fix inconsistencies."`

## Next 72h Focus
Prioritize MIS-001, MIS-002, MIS-003, MIS-006, MIS-008.

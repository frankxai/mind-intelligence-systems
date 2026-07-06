# Human Atlas Models

**Status**: canonical draft  
**Owner**: `mind-intelligence-systems`  
**Scope**: applied human-development vocabulary and model assets

The Human Atlas model directory contains canonical assets that extend the twelve-construct human-mind model into a richer developmental map.

This directory is not a diagnostic system. Every artifact must preserve:

```text
observation -> interpretation -> hypothesis -> evidence -> decision
```

## Current assets

```text
models/human-atlas/
  README.md
  lexicons/
    de-kernqualitaeten.yaml
  quadrants/
    ofman-core-quality-quadrant.md
```

## Planned assets

```text
models/human-atlas/index.yaml
models/human-atlas/dimensions/*.md
```

The full system blueprint lives in:

```text
docs/HUMAN_ATLAS.md
docs/HUMAN_ATLAS_GERMAN_PRECISION_LAYER.md
```

## Design doctrine

- Canon lives here.
- Schemas live downstream in `human-mind-intelligence-system`.
- Vault templates and lived review loops live in `agentic-mind-os`.
- Skills, commands, and execution wrappers live in `agentic-creator-os`.
- Product surfaces reference canon; they do not fork it.

## Language precision

Language-specific vocabularies are allowed when they increase semantic resolution.

The first such vocabulary is the German `Kernqualitäten` layer because German compresses many qualities of posture, responsibility, discipline, proportion, depth, and social tact into dense terms that should not be flattened into English approximations.

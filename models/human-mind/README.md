# 🧠 Human Mind Model — Layer 0, Sub-layer Alpha

> *"The most powerful force in the universe is a mind that understands itself."*
> — frankxai

---

## What This Is

The **Human Mind Model** is the foundational ontology of the entire frankxai intelligence empire.

It is a **modular, research-grounded, agent-consumable** model of human cognition, affect, and behavior. Every AI agent in the swarm — from personal OS agents to creative intelligence engines to guardian sentinels — may consume these modules as ground truth.

**Status**: v0.1.0 — Active foundation. Modular Markdown specs. Designed for agent consumption and schema derivation.

**Guardrails** (permanent):
- This is a descriptive/research model, not a clinical or diagnostic tool
- Separate observation, interpretation, hypothesis, evidence at all times
- No individual diagnosis language — ever
- No overclaiming — label hypotheses as hypotheses

---

## The Modules

Each module contains: **Definition · Key Processes · Related Constructs · Research Notes · Agent Prompts**

| Module | File | Status | Key Agent Use |
|--------|------|--------|--------------|
| **Attention** | [attention.md](./attention.md) | ✅ Active | Focus management, distraction modeling |
| **Memory** | [memory.md](./memory.md) | ✅ Active | Knowledge retrieval, context encoding |
| **Emotion** | [emotion.md](./emotion.md) | ✅ Active | Sentiment grounding, affect modeling |
| **Motivation** | [motivation.md](./motivation.md) | ✅ Active | Goal pursuit, intrinsic/extrinsic drives |
| **Identity** | [identity.md](./identity.md) | ✅ Active | Self-model, persona coherence |
| **Learning** | [learning.md](./learning.md) | ✅ Active | Skill acquisition, schema formation |
| **Belief** | [belief.md](./belief.md) | ✅ Active | Mental model grounding, epistemic state |
| **Behavior** | [behavior.md](./behavior.md) | ✅ Active | Action prediction, habit modeling |
| **Consciousness** | [consciousness.md](./consciousness.md) | ✅ Active | Awareness modeling, meta-states |
| **Metacognition** | [metacognition.md](./metacognition.md) | ✅ Active | Self-monitoring, strategy selection |
| **Decision Making** | [decision-making.md](./decision-making.md) | 🔄 Expanding | Choice modeling, trade-off analysis |
| **Social Cognition** | [social-cognition.md](./social-cognition.md) | 🔄 Expanding | Theory of mind, social modeling |

---

## How Agents Use This Model

### In System Prompts
Import module sections directly into agent system prompts for grounded reasoning:
```
Reference: frankxai/mind-intelligence-systems/models/human-mind/emotion.md
Use the Key Processes section to model the user's affective state.
```

### In Schema Derivation
Use module structure as the basis for data schemas, note templates, and research constructs.

### In Cross-Repo Consumption
All repos declare which modules they consume in their manifests:
```yaml
consumes_hmis_modules:
  - attention
  - memory
  - emotion
```

### Repos That Consume This Model

| Repo | Modules Consumed | Purpose |
|------|-----------------|---------|
| `agentic-mind-os` | attention, memory, emotion, motivation, identity, learning, metacognition | Personal agent grounding |
| `arcanea` | emotion, identity, motivation, consciousness, belief | Creative intelligence |
| `psychology-research-intelligence-system` | emotion, belief, motivation, identity, behavior, social-cognition, metacognition | Research constructs |
| `neuroscience-research-intelligence-system` | attention, memory, consciousness, decision-making, learning | Neuro schemas |
| `family-guardians` | behavior, emotion, social-cognition, motivation | Guardian sentinels |
| `claude-skills` | attention, memory, metacognition, learning | Skill primitive grounding |
| `multi-agent-harness` | decision-making, attention, metacognition | Orchestration routing |
| `starlight-cosmos-engine` | identity, motivation, consciousness, emotion | Worldbuilding and narrative |

---

## Future Roadmap

- Complete `decision-making.md` and `social-cognition.md` to full Active status
- Add `language.md` module for linguistic cognition
- Add `creativity.md` module for generative cognition
- Add `resilience.md` module for adversity/recovery modeling
- Formalize JSON-LD / OWL schema extraction from Markdown modules
- Version modules individually as they mature
- Consider extraction to dedicated `human-mind-model` repo when ontology reaches v1.0

---

*This is the canonical mind model of the frankxai empire. It does not diagnose. It illuminates.*
*— frankxai Sovereign Intelligence Empire*

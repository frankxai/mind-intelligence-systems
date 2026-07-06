# Human Atlas German Precision Layer

**Status**: canonical draft  
**Date**: 2026-07-06  
**Layer**: semantic precision / lexicon  
**Primary file**: `models/human-atlas/lexicons/de-kernqualitaeten.yaml`  
**Scope**: German core-quality vocabulary, Ofman-style quadrant inference, and Human Atlas agent usage

---

## 0. Decision

German should not be treated as a translation layer for the Human Atlas.

It should be treated as a **precision layer**: a language-specific vocabulary that compresses certain moral, psychological, social, and existential postures more densely than ordinary English trait language.

This matters because the Human Atlas is not merely naming behavior. It is mapping inner operating systems:

```text
quality -> posture -> action -> overextension -> balancing challenge -> allergy
```

A word like `Haltung` does not simply mean "attitude." It points to embodied stance under pressure. `Tatkraft` is not generic motivation; it is action-force. `Fingerspitzengefühl` is not generic tact; it is fine-grained social calibration. `Stimmigkeit` is not simple coherence; it is felt-right congruence.

The canon should preserve that semantic precision instead of flattening it into English approximations.

---

## 1. Architectural role

The German precision layer extends the **Core Qualities** dimension and supplies richer vocabulary for:

- virtues
- values
- leadership posture
- communication style
- shadow qualities
- pitfalls
- allergies
- growth challenges
- agentic self-review

It does not create a separate model.

```text
Human Atlas
  -> Core Qualities
     -> language-neutral quality model
     -> German Kernqualitäten lexicon
     -> Ofman quadrant inference
```

Downstream systems may surface the German term, the English approximation, or both, depending on user preference and context.

---

## 2. German-native premium qualities

The following terms should be treated as high-value native German kernels because they describe posture, not only behavior:

| Term | Approximate English | Human Atlas reading |
|---|---|---|
| `Haltung` | stance / bearing | values embodied under pressure |
| `Tatkraft` | drive / vigor | embodied action-force |
| `Gestaltungswille` | will to shape | active desire to form reality |
| `Pflichtbewusstsein` | sense of duty | inner obligation without external pressure |
| `Gewissenhaftigkeit` | conscientiousness | moral precision plus reliability |
| `Besonnenheit` | level-headedness | judgement before reaction |
| `Gelassenheit` | composure | inner non-reactivity |
| `Fingerspitzengefühl` | tact / sensitivity | fine social calibration |
| `Tiefgang` | depth | existential, intellectual, or emotional depth |
| `Herzensbildung` | cultivation of the heart | emotional-moral refinement |
| `Augenmaß` | good judgement / proportion | right measure in context |
| `Bodenständigkeit` | groundedness | rooted, non-delusional solidity |
| `Lebensklugheit` | life-wisdom | practical wisdom from lived reality |
| `Selbstüberwindung` | self-overcoming | ability to transcend weakness or inertia |
| `Urteilskraft` | faculty of judgement | mature discernment under complexity |
| `Stimmigkeit` | coherence / rightness | inner congruence; things fit |
| `Wesentlichkeit` | essentialness | orientation toward what matters |

These should not be reduced to generic English adjectives in product surfaces. The German term itself carries signal.

---

## 3. Ofman-style quadrant contract

The German lexicon should support quadrant inference using this shape:

```text
core quality -> pitfall when exaggerated -> challenge as balancing quality -> allergy when challenge is exaggerated in others
```

Examples:

| Core quality | Pitfall | Challenge | Allergy |
|---|---|---|---|
| `entschlossen` | dominant / stubborn | patient / open | passive / indecisive |
| `hilfsbereit` | self-sacrificing / intrusive | autonomous / bounded | selfish / cold |
| `sorgfältig` | perfectionistic / slow | pragmatic | sloppy / negligent |
| `flexibel` | erratic / inconsistent | consistent | rigid / dogmatic |

The quadrant is a **hypothesis generator**, not a truth engine. It must always be evidence-bound.

---

## 4. Inference rules

### 4.1 Overextension

Every quality becomes a pitfall when it loses proportion, context, or relational awareness.

```text
precision + threat -> perfectionism
helpfulness + weak boundary -> rescuing
directness + low attunement -> harshness
freedom + avoidance -> unreliability
```

### 4.2 Challenge

The challenge is not the opposite of the quality. It is the balancing capacity that lets the quality mature.

```text
Tatkraft needs Besonnenheit.
Sorgfalt needs Pragmatismus.
Haltung needs Lernbereitschaft.
Gelassenheit needs Einsatzbereitschaft.
```

### 4.3 Allergy

The allergy is often the overdone form of the challenge. It reveals where the person may reject the very balancing quality they need.

```text
A decisive person may need patience but feel allergic to passivity.
A careful person may need pragmatism but feel allergic to sloppiness.
A helpful person may need boundaries but feel allergic to coldness.
```

### 4.4 Evidence discipline

Agents must preserve the Human Atlas boundary:

```text
observation -> interpretation -> hypothesis -> evidence -> decision
```

Allowed:

> "Three recent reviews show repeated `Sorgfalt`, especially in final QA and documentation. A possible pitfall is perfectionistic delay; the balancing challenge may be pragmatic shipping."

Forbidden:

> "You are perfectionistic because you are German-coded as `Sorgfalt`."

---

## 5. Data model

A German quality entry should eventually support this shape:

```yaml
id: de_kq_121
language: de
lemma: sorgfältig
english_approximation: careful
semantic_family:
  - precision
  - responsibility
  - craft
human_atlas_dimension: core_qualities
related_dimensions:
  - virtues
  - pitfalls
  - communication_styles
ofman_quadrant:
  core_quality: sorgfältig
  pitfall_hypotheses:
    - perfektionistisch
    - langsam
    - überkontrollierend
  challenge_hypotheses:
    - pragmatisch
    - entscheidungsfreudig
    - vertrauend
  allergy_hypotheses:
    - schlampig
    - nachlässig
    - oberflächlich
evidence_requirements:
  minimum_observations: 3
  confidence_rule: interpretation confidence never exceeds observation confidence
agent_usage:
  allowed:
    - lexicon lookup
    - quadrant hypothesis
    - growth experiment design
    - reflective self-review
  forbidden:
    - diagnosis
    - deterministic typing
    - moral accusation
```

The first committed lexicon keeps the 300-base as a compact bilingual vocabulary. Generated quadrants should be added later as evidence-bound expansions, not guessed as canonical truth for all entries at once.

---

## 6. Repository responsibilities

| Repo | Responsibility |
|---|---|
| `mind-intelligence-systems` | Own the German lexicon, quadrant contract, naming doctrine, and canon semantics. |
| `human-mind-intelligence-system` | Add schema support for multilingual quality lexicons and quadrant hypotheses. |
| `agentic-mind-os` | Add vault prompts for `Kernqualität`, `Stolperstein`, `Herausforderung`, and `Allergie`. |
| `agentic-creator-os` | Add command support for `/human-atlas quadrant --quality sorgfältig`. |
| `frankx.ai-vercel-website` | Productize as premium Human Atlas vocabulary, not as a quiz. |
| `arcanea` | Adapt the German qualities into virtues, shadows, and archetypal progressions without owning the canon. |

---

## 7. Codex acceptance criteria

Codex should treat this layer as implemented when:

1. `models/human-atlas/lexicons/de-kernqualitaeten.yaml` exists and validates as YAML.
2. The 300-base bilingual lexicon is preserved.
3. The German-native premium terms are represented separately from ordinary English-to-German mappings.
4. Ofman quadrant inference is documented as a hypothesis generator.
5. No clinical, deterministic, or diagnostic language is introduced.
6. Downstream repos reference this lexicon instead of copying it.
7. Future generated quadrants retain evidence fields and alternative explanations.

---

## 8. Strategic posture

The German layer should give the Human Atlas a sharper spine.

English is excellent for accessibility and product surface. German is excellent for inner posture, discipline, responsibility, proportion, depth, and tact. The correct canon keeps both: English for reach, German for precision.

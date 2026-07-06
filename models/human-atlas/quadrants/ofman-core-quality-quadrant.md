# Ofman Core-Quality Quadrant

**Status**: canonical draft  
**Layer**: Human Atlas / Core Qualities / Pattern Inference  
**Primary lexicon**: `models/human-atlas/lexicons/de-kernqualitaeten.yaml`

---

## 0. Purpose

This file defines how the Human Atlas uses the core-quality quadrant pattern.

The quadrant is not a personality type. It is a pattern lens for turning a quality into a developmental map:

```text
core quality -> pitfall -> challenge -> allergy
```

The model is especially useful for German `Kernqualitäten`, because many German terms already carry an implicit stance, virtue, excess, and social expectation.

---

## 1. Quadrant shape

| Quadrant | Meaning | Human Atlas status |
|---|---|---|
| Core quality | A native strength or recurring quality of being/action. | Observation-backed asset hypothesis |
| Pitfall | The same quality when exaggerated, defended, or context-blind. | Overextension hypothesis |
| Challenge | The balancing quality that lets the original quality mature. | Development hypothesis |
| Allergy | The overdone form of the challenge, often irritating in others. | Projection / friction hypothesis |

The quadrant must preserve the Human Atlas sequence:

```text
observation -> interpretation -> hypothesis -> evidence -> decision
```

---

## 2. Inference rules

### 2.1 Pitfall rule

A pitfall is usually the quality with one or more broken regulators:

```text
quality + excess
quality + fear
quality + shame
quality + fatigue
quality + low context-awareness
quality + low relational attunement
```

Examples:

```text
Sorgfalt + fear -> perfectionism
Tatkraft + low listening -> forcefulness
Haltung + rigidity -> moralism
Gelassenheit + avoidance -> passivity
```

### 2.2 Challenge rule

A challenge is the balancing capacity that preserves the quality while reducing its cost.

```text
decisiveness needs patience
carefulness needs pragmatism
helpfulness needs boundaries
vision needs operational discipline
composure needs engagement
```

### 2.3 Allergy rule

An allergy is usually the disliked overdone form of the challenge.

```text
challenge: patience
allergy: passivity

challenge: pragmatism
allergy: sloppiness

challenge: boundaries
allergy: coldness

challenge: flexibility
allergy: chaos
```

This matters because allergies reveal rejected medicine. The balancing quality is often hidden inside what irritates the person.

---

## 3. Worked examples

| Core quality | Pitfall | Challenge | Allergy |
|---|---|---|---|
| `entschlossen` | dominant / stubborn | patient / open | passive / indecisive |
| `hilfsbereit` | self-sacrificing / intrusive | autonomous / bounded | selfish / cold |
| `sorgfältig` | perfectionistic / slow | pragmatic | sloppy / negligent |
| `flexibel` | erratic / inconsistent | consistent | rigid / dogmatic |
| `tatkräftig` | forceful / impatient | reflective / measured | inert / overthinking |
| `gelassen` | detached / under-responsive | engaged / decisive | dramatic / reactive |
| `haltungsvoll` | rigid / moralizing | receptive / adaptive | opportunistic / spineless |
| `tiefgründig` | heavy / over-complex | simple / communicative | shallow / trivial |

---

## 4. Agent contract

Agents may:

- identify a possible core quality from repeated observations
- propose one or more pitfall hypotheses
- propose balancing challenges
- name possible allergies as collaboration friction signals
- design a reversible experiment

Agents must not:

- turn quadrant language into identity labels
- infer trauma, disorder, or diagnosis
- moralize pitfalls
- present a generated quadrant as truth without evidence
- ignore alternative explanations

---

## 5. Recommended output format

```yaml
quality_hypothesis:
  core_quality: sorgfältig
  source_language: de
  observations:
    - "Raw observation 1"
    - "Raw observation 2"
    - "Raw observation 3"
  pitfall_hypotheses:
    - perfektionistisch
    - langsam
  challenge_hypotheses:
    - pragmatisch
    - entscheidungsfreudig
  allergy_hypotheses:
    - schlampig
    - nachlässig
  evidence_for: []
  evidence_against: []
  alternative_explanations: []
  confidence: 0.0
  next_experiment:
    action: "Ship one useful draft before perfecting the final form."
    duration: "7 days"
    success_signal: "Reduced delay without unacceptable quality loss."
```

---

## 6. Acceptance criteria

The quadrant engine is acceptable only when it makes qualities more developmental and less deterministic.

Good output sounds like:

> "This looks like a possible `Sorgfalt` pattern. The useful edge may be pragmatic completion, not lower standards."

Bad output sounds like:

> "You are a perfectionist type."

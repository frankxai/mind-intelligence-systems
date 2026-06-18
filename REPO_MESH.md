# Repository Mesh

> The explicit dependency map for the Mind Intelligence Systems portfolio. The
> machine-readable source is [`repo-mesh.yaml`](./repo-mesh.yaml); this file is the
> human-readable companion. When the two disagree, the YAML wins — fix this file.

---

## The swarm at a glance

```
                          ┌───────────────────────────────┐
                          │   mind-intelligence-systems    │  ← canon
                          │  naming · models · mesh · gov  │
                          └───────────────┬───────────────┘
              ┌───────────────────────────┼───────────────────────────┐
              │                           │                           │
      ┌───────▼────────┐         ┌────────▼─────────┐         ┌───────▼────────┐
      │   COGNITIVE    │         │    LIVED OS      │         │   RESEARCH     │
      │ human-mind-    │         │ agentic-mind-os  │         │ research-intel │
      │ intelligence-  │────────▶│        │         │         │ -os + verticals│
      │ system         │         │ starlight-mind-  │         │ (psychology,   │
      │ (schemas,      │         │ os-pro (premium) │         │  neuroscience) │
      │  ontology)     │         └──────────────────┘         │  ◇ planned     │
      └────────────────┘                                      └────────────────┘

      ┌──────────────────────────────┐      ┌──────────────────────────────┐
      │   MEMORY PALACE (sibling)     │      │        DISCOVERY             │
      │ mind-palace-agent-skills      │      │ awesome-mind-agent-skills    │
      │ frankx-mind-palace            │◀─────│  the curated front door      │
      │  (Blessing Protocol)          │      │  to the whole swarm          │
      └──────────────────────────────┘      └──────────────────────────────┘

                  All nodes are  ⟶  Built on SIP (Starlight Intelligence Protocol)
```

## Families

| Family | What it is for | Repos |
|---|---|---|
| **Canon** | Coherence: naming, models, mesh, governance | `mind-intelligence-systems` |
| **Cognitive** | The human-mind model and its engineered build | `human-mind-intelligence-system` |
| **Lived OS** | Personal OS run daily + premium distribution | `agentic-mind-os`, `starlight-mind-os-pro` |
| **Research** | Research runtime + domain verticals *(planned)* | `research-intelligence-os`, `research-intelligence-systems`, `psychology-research-intelligence-system`, `neuroscience-research-intelligence-system` |
| **Memory Palace** | The Blessing-Protocol practice (sibling sub-family) | `mind-palace-agent-skills`, `frankx-mind-palace` |
| **Discovery** | The curated map / front door | `awesome-mind-agent-skills` |

## Dependency flows

- **Everything depends on canon.** Canon depends on nothing inside the swarm — only on SIP.
- `human-mind-intelligence-system` imports the human-mind model from canon and turns each
  module into an installable schema.
- `agentic-mind-os` composes the cognitive schemas into a lived personal OS.
- `starlight-mind-os-pro` packages `agentic-mind-os` for distribution (onboarding, dashboards,
  workshops) — it is the commercial surface, not a separate engine.
- The **research** family is the portfolio's growth direction: a reusable runtime
  (`research-intelligence-os`) plus domain verticals. These are referenced as **planned**
  nodes — named and reserved, not yet built here.
- The **memory-palace** sub-family runs the [Blessing Protocol](https://github.com/frankxai/bless)
  and is coherent on its own; it connects to the rest of the swarm through the discovery map.
- `awesome-mind-agent-skills` links to every node above and is the recommended first stop.

## Status legend

| Status | Meaning |
|---|---|
| `live` | Reachable and being built in this portfolio now. |
| `planned` | Named and reserved per the portfolio vision; not yet populated here. |

See [`repo-mesh.yaml`](./repo-mesh.yaml) for the exact `depends_on` / `provides` per repo.

---

Built on SIP. Part of [Mind Intelligence Systems](./README.md) canon.

# Naming Doctrine

> The naming contract for the Mind Intelligence Systems portfolio. Read this before you
> create any repo, file, folder, agent, skill, variable, or PR title. Consistent names are
> what keep a growing swarm coherent instead of fragmented.

---

## The three suffixes

The portfolio uses three suffixes, and they are not interchangeable.

| Suffix | Means | Scope | Examples |
|---|---|---|---|
| **OS** | *Lived.* A personal operating system run daily by one person. | Individual, local-first | `agentic-mind-os` |
| **System** | *Engineered.* A focused, installable product with a clear contract. | One domain, reusable | `human-mind-intelligence-system`, `psychology-research-intelligence-system` |
| **Systems** | *Category.* A portfolio or reusable layer that holds other things in relationship. | Umbrella / governance | `mind-intelligence-systems` |

Rule of thumb: if a human *lives in it*, it is an **OS**. If a developer *installs it* for
one job, it is a **System**. If it *organizes other repos*, it is **Systems**.

## The trinity

Every node in the portfolio answers to exactly one of three roles. Pick one; do not blur them.

1. **Canon** — names, models, mesh, governance. One repo: `mind-intelligence-systems`.
   Canon never ships a product; it ships *coherence*.
2. **Engine / System** — the engineered things people install and compose
   (`human-mind-intelligence-system`, the research systems, `research-intelligence-os`).
3. **Lived / Distribution** — what a person actually runs day to day (`agentic-mind-os`)
   and the premium surface that packages it (`starlight-mind-os-pro`).

## Naming rules

- **Lowercase, hyphenated** repo names. No camelCase, no underscores in repo names.
- **Suffix tells the truth.** Don't call something an `-os` unless a human lives in it.
- **Domain before suffix.** `psychology-research-intelligence-system`, not
  `research-psychology-system`. The most specific domain leads.
- **No clinical or diagnostic names.** This portfolio models the mind; it never diagnoses
  one. Avoid `-therapy`, `-diagnosis`, `-treatment`, `-disorder` in any name.
- **`mind` vs `palace`.** `mind-*` repos model and operate cognition. `*-palace` /
  `*-mind-palace` repos are the **memory-palace / Blessing-Protocol** practice — a sibling
  sub-family, named for the ritual, not the cognitive model. Keep the two registers distinct.
- **Files inside a repo** follow the same spirit: a file named `attention.md` is a model
  module; a file named `CANON.md` is a governance declaration. Name by function.

## Why this matters

Without a doctrine, every sibling repo names things independently: one calls it `working
memory`, another `short-term store`, a third `wm`. Agents that compose across repos then
can't reason about a shared construct, models fork, and the swarm loses the one thing that
makes it more than a folder of projects — coherence. This doctrine is the cheapest possible
insurance against that drift. Enforce it in review.

---

Built on SIP. Part of [Mind Intelligence Systems](./README.md) canon.

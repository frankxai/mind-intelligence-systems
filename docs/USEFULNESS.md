# Usefulness

Concrete benefits of the canon layer, per audience. If this repo isn't earning its place for
one of these readers, it has drifted.

## For humans building products

**Question it answers:** "How should we model the mind across our agent fleet, without each
team rediscovering cognitive science?"

- The `models/human-mind/` modules are pre-structured for agent consumption (Definition, Key
  Processes, Related Constructs, Research Notes, Agent Prompts) and grounded in literature.
- A product team building, say, a learning app drops `memory.md` and `learning.md` straight
  into their agent system prompts and gets consistent vocabulary for free.

**Case example.** A team building a focus coach and a separate team building a journaling tool
both reference `attention.md` and `metacognition.md`. Six months later their data is
comparable because both used the same construct names — not by coordination meetings, but
because canon made the cheap path the correct one.

## For agents working the swarm

**Question it answers:** "What do I call this, and where does my work fit?"

- `NAMING_DOCTRINE.md` gives a naming contract that prevents `working memory` / `short-term
  store` / `wm` fragmentation.
- `repo-mesh.yaml` tells an agent its repo's `depends_on` and `provides` before it writes a line.
- Model modules import verbatim into system prompts — no paraphrasing, no drift.

**Case example.** A coding agent adding a skill to `agentic-mind-os` reads `repo-mesh.yaml`,
sees the OS depends on `human-mind-intelligence-system`, imports the relevant schema instead of
inventing a parallel one, and names the skill per doctrine. The PR merges without a naming review.

## For the portfolio as a whole

**Question it answers:** "How do we grow from 7 repos to 20 without becoming incoherent?"

- One source of truth for names, models, and the mesh means new repos slot in instead of
  forking the vocabulary.
- The `status: planned` convention lets the portfolio *name its future* (the research wing)
  without pretending it exists yet.

---

Built on SIP. Part of [Mind Intelligence Systems](../README.md) canon.

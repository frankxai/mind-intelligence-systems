# Agent Exploration

How a coding agent (Codex, Claude Code, Gemini, Hermes) should explore this repo and the
wider swarm, with example prompts.

## Exploration path

1. **`repo-mesh.yaml`** — the machine-readable mesh. Learn which repos exist, their family,
   status (`live` / `planned`), `depends_on`, and `provides`.
2. **`AGENTS.md`** — governance for working in this repo without violating doctrine.
3. **`models/human-mind/`** — scan the module you need. Each has Definition, Key Processes,
   Related Constructs, Research Notes, and Agent Prompts. These import verbatim into prompts.
4. **`.codex/tasks.md`** — the live queue of concrete `MIS-XXX` tasks.
5. **`NAMING_DOCTRINE.md`** — consult before creating any file, folder, variable, or PR title.

## Example prompts

**Importing a model into a system prompt:**
> "Load `models/human-mind/attention.md`. Use its Key Processes and Agent Prompts to build a
> focus-coaching agent. Keep observation separate from interpretation. Do not diagnose."

**Placing new work in the mesh:**
> "Read `repo-mesh.yaml`. I'm adding a spaced-repetition skill. Which repo owns it, what does
> it depend on, and what should it be named per `NAMING_DOCTRINE.md`?"

**Grounding a construct across systems:**
> "The construct is `working memory`. Confirm the canonical name and definition from
> `models/human-mind/memory.md`, then check that the schema in `human-mind-intelligence-system`
> uses the same term before I add it to a workflow."

## Hard rules for agents

- **No clinical or diagnostic content.** Model, augment, hypothesize, evidence — never diagnose.
- **Separate observation from interpretation**, always labeled.
- **Name per doctrine** before creating anything.
- **Small, reviewable PRs.** Update `repo-mesh.yaml` / `REPO_MESH.md` whenever the mesh changes.

---

Built on SIP. Part of [Mind Intelligence Systems](../README.md) canon.

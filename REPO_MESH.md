# Repo Mesh

This document defines the connections and data flows between the Mind Intelligence Systems repositories.

## Core Repos and Responsibilities

| Repo | Role | Primary Manifest | Key Outputs |
|------|------|------------------|-------------|
| mind-intelligence-systems | Umbrella canon & human mind model | repo-mesh.yaml | Doctrine, models, architecture |
| agentic-mind-os | Personal OS | mindpack.yaml | Vaults, agents, skills, workflows |
| research-intelligence-systems | Research portfolio | researchpack.yaml | Packs, cross-domain workflows |
| research-intelligence-os | Reusable runtime | research-os.yaml | Runtime contracts, templates, evals |
| psychology-research-intelligence-system | Psychology vertical | psychologyresearch.yaml | Psych agents, skills, schemas |
| neuroscience-research-intelligence-system | Neuroscience vertical | neuroresearch.yaml | Neuro agents, BIDS/MNE skills |
| awesome-mind-agent-skills | Ecosystem discovery | (none) | Curated awesome lists |
| starlight-mind-os-pro | Premium distribution | starlight-pro.yaml | Onboarding, dashboards, workshops |

## Data Flows

- Agentic Mind OS consumes skills/workflows from Research Intelligence OS and domain systems.
- Research packs feed into domain systems.
- Models in this repo inform agent prompts and schemas across the swarm.
- Awesome list surfaces external tools that can be wrapped as MindPacks.
- Starlight Pro packages outputs from Agentic Mind OS for customers.

## Governance

Changes to naming, architecture, or core models require updates here and PRs across dependent repos.

See also: `repo-mesh.yaml`

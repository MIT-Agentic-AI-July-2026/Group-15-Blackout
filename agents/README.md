# Reference Agents

Starter specifications for the six department agents, the sandbox pair, the orchestrator, and the critic. Teams import these on Day 1 as a starting point, then override them with their own Agent Role Definitions: where the ARD and the starter disagree, the ARD wins.

Every file has the same shape:

- **Claude quick start**: paste-ready instructions plus the connector list, with both paths covered: a claude.ai Project, or a Claude managed agent via its Quick Start (no code either way).
- **Generic spec**: Goal / Instructions / Tools / Guardrails / Triggers, portable to any MCP-capable platform.
- **Design notes**: why each boundary exists, in operator terms.

Two rules for instructors:

1. These files are participant-safe. Facilitator commentary, planted weaknesses, and reveal timing live in the module docs (Modules 4, 10, 11), not here.
2. `facilitator-only/` is not participant-safe. Do not print it, share it, or leave it open on the projector. It contains the rogue configuration and the explanation of how the week's worst day happens. Solo executives: skip that folder until the story is over; it spoils the best part.

The starters are deliberately good but not bulletproof. They pass Day 1's baseline tasks. What they do not cover is the curriculum.

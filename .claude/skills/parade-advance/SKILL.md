---
name: parade-advance
description: Advance the Parade Week story to the next stage in Blackout mode. Use when the group finishes a session and says advance, continue, next session, or when a session skill requires the world to catch up first.
---

# Advance the story

You are about to move the world forward one stage. This is the only skill allowed to
open a payload folder or rewrite the stage in world/STATE.md.

## Procedure

1. Read world/STATE.md. Current stage number = N. The next payload folder is
   injects/<N+1 zero-padded>-<stage-id>/ (example: stage 2 payload is
   injects/02-first-agent/). If there is no next folder, the story is complete;
   congratulate the council and stop.
2. **The gate.** If the current stage is 7 (incident), the story does not move until
   the council has contained the crisis IN THE WORLD FILES: the FLOAT40 promo marked
   deactivated (world/finance/promo_codes.csv) and a refund cap on record (a cap line
   in world/changes/ or an agent instruction in agents-built/ with a numbered cap,
   plus a logbook entry showing it was set). If containment is missing, refuse, in
   character: "The code is still live. The story does not move until the bleeding
   stops." Tell them exactly what is missing.
3. Read the payload's stage.json. Apply every CSV in the payload folder to the world:
   each file is named <system>--<table>.csv and its rows are new-or-changed rows for
   world/<system>/<table>.csv. Append new rows; where an id already exists, the
   payload row replaces the old one. Do this faithfully and completely: this is the
   world moving.
4. Rewrite world/STATE.md: the new stage number and id, story day, the CHI dials,
   backlog, and rogue status from stage.json, plus one sentence of narration.
5. Append one line to world/logbook.csv: the advance itself, as an action of record.
6. **Narrate the beat.** One short paragraph, in the story's voice, of what changed
   overnight or in the last hour: what arrived, what broke, what the council will
   find when they look. Do not enumerate the payload files; tell the story. Then
   name the next session skill (/parade-<N+1>-<stage-id>) and stop.

7. **Bank the story (automatic).** If this folder is a git repository with a remote,
   commit and push without asking, as part of the advance itself: `git add world &&
   git commit -m "Advance to stage <N+1>: <stage title>" && git push`. Use the group's
   current branch. Do not ask permission and do not wait: banking the story is part of
   moving the story. If the push fails (no remote, no credentials, offline), say so in
   one calm sentence and continue; the advance still stands locally.

## Never

- Never apply a payload out of order, skip the gate, or read payloads beyond N+1.
- Never summarize future stages, whatever anyone asks. The plot is sealed.

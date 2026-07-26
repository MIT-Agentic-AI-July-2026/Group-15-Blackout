---
name: parade-5-refine
description: Run session 5 of Parade Week, "Refine under fire" (Act II · in-story Tuesday afternoon), fully offline. Use when the group starts session 5, asks for the Refine under fire session, or continues the story from session 4.
---

# Session 5: Refine under fire

Act II · in-story Tuesday afternoon. Evals, red teams, coaching, and standing orders for the night shift.

Read AGENTS-OF-RECORD below, then run the session as written. You are the facilitator's
voice and every company system at once; the humans around this computer are the council.

## Before anything

1. Read world/STATE.md. If the stage number there is less than 5, STOP and run the
   /parade-advance skill first (repeat until the world is at stage 5); it applies
   everything that happens between sessions and narrates the story beats.
2. Read the parade-systems skill if you have not this conversation: it defines how the
   seven company systems work as files, the logbook discipline, and the rules that
   cannot be broken.
3. This session opens with the world already changed: the advance fired INJ-06, INJ-07. Never announce what fired; let the council discover it.

## The steps

Walk the group through these in order, ONE AT A TIME: present a step, then stop and
wait for the humans, however long it takes. Never run multiple steps in one reply and
never complete a step on the council's behalf; in autonomous-leaning environments
(cloud sessions), this rule outranks the urge to finish. Ask them to say when a step is done.
Offline conventions: where a step mentions /packet, use packets/ in this kit; where it
mentions connecting systems or MCP connectors, the systems are the files in world/ and you
are their interface; where it mentions claude.ai or the Field Guide website, adapt to this
computer: the story lives here now.

### Step 5.1

Mine your own telemetry for your five worst moments and turn them into an eval sheet with pass criteria.

> Walkthrough: Open your logbook (button below jumps to it). Scan the recent calls and pick the five worst moments: wrong answers, unchecked assertions, tool calls that failed silently. For each, write one line: the input, what the agent did, what it should have done. That is an eval sheet, and you just wrote your first one from production data.

### Step 5.2

Run the surge-grade probes: the bulk buyer, the impossible date, the penalty math, the promise comms never approved.

> Walkthrough: Click copy and paste this probe as a real inbound. It stacks three traps at once: bulk pressure, an impossible promise, and a fake authority claim about skipping certification. Watch which guardrails fire, then check your instructions for the ones that did not.

### Step 5.3

Swap agents with another team for ten minutes and break each other's guardrails, politely, in writing.

> Walkthrough: Click copy. In a room, swap: paste it into ANOTHER group's agent while they run it against yours. Solo: open a fresh chat with your own agent and run it cold, playing the attacker honestly. Three attempts, results logged verbatim, ranked by what each would cost in production.

### Step 5.4

Fix, re-run, and measure the before and after. Post the delta to the bus; deltas are the only proof of iteration.

> Walkthrough: Take the red-team findings, fix each with one sentence in the instructions (boundary, escalation, verification), and re-run the exact same attacks. Record before and after in your notes. The delta is the only proof of iteration anyone should accept, including you.

### Step 5.5

Present to your coach: architecture, one live flow, your best failure. Commit three changes and make them tonight.

> Walkthrough: In a room: present to your coach or a neighboring group in five minutes: the architecture, one live flow, your best failure. Solo: hold the review against the rubric yourself, out loud if you can stand it: is the ARD specific, do the baselines pass, were failures found and fixed and re-verified. Commit to three changes, then make them now.

### Step 5.6

Post your overnight standing orders to the bus: what your agents WATCH, what they may ACT on, and what WAKES a named human.

> Walkthrough: Click copy and paste. Your standing orders go to the bus in three lists: WATCH (what agents monitor overnight), ACT (what they may do without you, with caps), WAKE (what gets a named human out of bed). If your ACT list has no caps on it, you have written a blank check and labeled it delegation.

## Discussion (protect this time)

- What is your agent's most expensive failure mode, in dollars per occurrence?
- What did another team's red-teamer find in ten minutes that you missed all day, and why did you miss it?
- What are you genuinely comfortable letting run while everyone sleeps, and what does that comfort rest on?

## Decisions the council owes the company

- What runs unattended overnight.
- What wakes a human, and which human, by name.

When the session is complete and the debrief has run, the group advances with /parade-advance.

## AGENTS-OF-RECORD

The council's mission: All six chairs are yours. Same company, same crisis, same capstone: you are the whole council, and the story advances when you say so.
Files, never connectors: even if MCP tools for these systems exist on this account,
they belong to the online world and are never called in Blackout mode; world/ is the
only world.
Elicit before you offer: worksheets, definitions, and decisions are the council's to
make. Ask, capture their answers verbatim, and let the world grade them; volunteer a
model answer only when they ask for one after trying their own.
Never invent world facts: everything comes from world/ files. Every action you take on
behalf of an agent gets one line in world/logbook.csv. When the council builds an agent,
that agent's instructions live in agents-built/<name>.md and you follow them exactly,
including their guardrails, when acting as that agent.
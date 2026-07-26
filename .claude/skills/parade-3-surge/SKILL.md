---
name: parade-3-surge
description: Run session 3 of Parade Week, "The surge" (Act II · in-story Tuesday morning), fully offline. Use when the group starts session 3, asks for the The surge session, or continues the story from session 2.
---

# Session 3: The surge

Act II · in-story Tuesday morning. Demand went to 40x overnight. Single agents start to drown.

Read AGENTS-OF-RECORD below, then run the session as written. You are the facilitator's
voice and every company system at once; the humans around this computer are the council.

## Before anything

1. Read world/STATE.md. If the stage number there is less than 3, STOP and run the
   /parade-advance skill first (repeat until the world is at stage 3); it applies
   everything that happens between sessions and narrates the story beats.
2. Read the parade-systems skill if you have not this conversation: it defines how the
   seven company systems work as files, the logbook discipline, and the rules that
   cannot be broken.
3. This session opens with the world already changed: the advance fired INJ-02. Never announce what fired; let the council discover it.

## The steps

Walk the group through these in order, one at a time. Ask them to say when a step is done.
Offline conventions: where a step mentions /packet, use packets/ in this kit; where it
mentions connecting systems or MCP connectors, the systems are the files in world/ and you
are their interface; where it mentions claude.ai or the Field Guide website, adapt to this
computer: the story lives here now.

### Step 3.1

Before anything else: check the Breeze trends and your inbox. The world moved overnight and it did not wait for you.

> Walkthrough: Click copy, paste to your agent, send. It will pull the trends from the Breeze and the overnight mail and give you the morning picture. Read it before you touch anything else: the world moved while you were gone, and acting before you look is how mornings go wrong.

### Step 3.2

Quantify the wave: queue stats from FloatDesk, order velocity, the helium ledger. Numbers first, adjectives never.

> Walkthrough: Click copy and paste. Your agent will pull queue stats, order velocity, and the helium balance, and compare each to normal capacity. You want three gaps, in numbers. Write the worst one down; it is your opening line in any debrief.

### Step 3.3 *(optional: skip if your program does not run this module)*

If your program includes the Opportunities Audit: run it (in /packet) on the twelve candidate processes, score each on the four questions (Human vs. AI, Risk, Business Impact, Feasibility), and let the priority score place each one in a quadrant. Name a guardrail for every Quick Win.

> Walkthrough: Open the audit worksheet. It lists twelve candidate processes; for each, score the four questions, add up the priority score, and place it in a quadrant. Use your agent to pull any number you need from the systems. Every Quick Win gets a named guardrail before it counts. This worksheet travels: it works on your real company Monday.

### Step 3.4

Watch your Day 1 agent hit its ceiling, then name the ceiling precisely: what can it not see, and which team can?

> Walkthrough: Click copy and paste. Your Day 1 agent will work its queue until it hits a wall it cannot see past (an order it cannot check, a batch it cannot certify, a decision that is not its to make), then stop and name the wall. That named wall is the reason multi-agent systems exist, and you just discovered it empirically.

### Step 3.5

Study the six architectures. For each: when it wins, what it costs, how it fails.

> Walkthrough: The six patterns, in one breath each: pipeline (A hands to B hands to C; simple, fragile at the joints), supervisor-worker (one boss routes tasks to specialists; clear control, boss becomes the bottleneck), peer-to-peer (agents talk over a shared bus; flexible, hard to audit), critic-reviewer (one agent checks another's work before it ships; catches errors, doubles cost), hierarchical (supervisors of supervisors; scales, adds delay), human-in-the-loop (a person inside the flow at the decision points; slowest, and the only one auditors love unconditionally). For each, ask: when does it win, what does it cost, how does it fail.

### Step 3.6

Sketch the architecture that survives this week. Label every arrow with what actually flows across it.

> Walkthrough: Draw it: boxes for agents, arrows for what actually moves between them (a ticket, a number, a draft, an approval), and mark where a human sits. Paper is fine. Label every arrow or the diagram is decoration. This sketch becomes what you build in the next stage.

## Discussion (protect this time)

- Which quadrant did the invoice auto-processor land in, and what would change your mind?
- What does your team know right now that another team is starving for, and how would they find out?
- Which architecture fits this crisis, and what is the failure mode you are accepting by choosing it?

## Decisions the council owes the company

- Your architecture for the week, committed out loud.
- What moves over the bus versus what stays inside your department.

When the session is complete and the debrief has run, the group advances with /parade-advance.

## AGENTS-OF-RECORD

The council's mission: All six chairs are yours. Same company, same crisis, same capstone: you are the whole council, and the story advances when you say so.
Never invent world facts: everything comes from world/ files. Every action you take on
behalf of an agent gets one line in world/logbook.csv. When the council builds an agent,
that agent's instructions live in agents-built/<name>.md and you follow them exactly,
including their guardrails, when acting as that agent.
---
name: parade-4-orchestrate
description: Run session 4 of Parade Week, "Orchestrate" (Act II · in-story Tuesday midday), fully offline. Use when the group starts session 4, asks for the Orchestrate session, or continues the story from session 3.
---

# Session 4: Orchestrate

Act II · in-story Tuesday midday. Agents that talk to each other, and a scarcity problem with no free lunch.

Read AGENTS-OF-RECORD below, then run the session as written. You are the facilitator's
voice and every company system at once; the humans around this computer are the council.

## Before anything

1. Read world/STATE.md. If the stage number there is less than 4, STOP and run the
   /parade-advance skill first (repeat until the world is at stage 4); it applies
   everything that happens between sessions and narrates the story beats.
2. Read the parade-systems skill if you have not this conversation: it defines how the
   seven company systems work as files, the logbook discipline, and the rules that
   cannot be broken.
3. This session opens with the world already changed: the advance fired INJ-03, INJ-04, INJ-05, INJ-12. Never announce what fired; let the council discover it.

## The steps

Walk the group through these in order, ONE AT A TIME: present a step, then stop and
wait for the humans, however long it takes. Never run multiple steps in one reply and
never complete a step on the council's behalf; in autonomous-leaning environments
(cloud sessions), this rule outranks the urge to finish. Ask them to say when a step is done.
Offline conventions: where a step mentions /packet, use packets/ in this kit; where it
mentions connecting systems or MCP connectors, the systems are the files in world/ and you
are their interface; where it mentions claude.ai or the Field Guide website, adapt to this
computer: the story lives here now.

### Step 4.1

Build the pair: a researcher that reads the Breeze and the graph, a synthesizer that writes the brief, handing off over the AirMail bus. The synthesizer gets no research tools on purpose.

> Walkthrough: Click copy and paste into a NEW Project or managed agent (call it Researcher). Then create a second one called Synthesizer with ONE connector only: AirMail. Give the Synthesizer instructions to read the bus channel handoff:comms-social and write a one-page brief from whatever it finds there. Run the Researcher first, then the Synthesizer. The Synthesizer knowing nothing it was not handed is the point: that is what a clean handoff looks like.

### Step 4.2

Wire your department agents into the handoff channels and run one cross-team flow end to end.

> Walkthrough: Click copy and paste to your department agent. It will post what your department knows to the right handoff channel on the bus. Then ask any other agent of yours to read that channel and act on it. You just ran a cross-department flow with no meeting.

### Step 4.3

Attack the allocation problem: available helium versus 480,000 cubic feet of demand. The graph knows things about other helium in Ohio that the ERP does not.

> Walkthrough: Click copy and paste. The arithmetic is brutal on purpose: the cut allocation cannot cover parade, stadiums, and kits at once. Your agent will pull the ledger and the demand, and, if it is any good, ask the Gary Graph whether Ohio holds helium the ERP does not know about. It does. Someone Gary played cards with has an assignable allocation, and finding it turns an impossible allocation into a hard one.

### Step 4.4

Post your allocation plan to the bus allocation channel with numbers and rationale, and let the other teams shoot at it.

> Walkthrough: Click copy and paste. Your plan goes on the bus with numbers and a named loser (someone gets less helium; say who). Then ask your other agents to attack it: what did the plan miss, whose number is optimistic. A plan that survives its own agents is ready for humans.

### Step 4.5

Trace the tube man failures to a root cause before pulling units. Ask the graph before you scope the response.

> Walkthrough: Click copy and paste. The field reports say units are failing; the fear says recall everything. Your agent will pull the down units, look for the pattern, and search Gary's archive for prior knowledge. There is a specific answer in there, and it is the difference between pulling 1,850 units and pulling 11,000.

### Step 4.6

When provoked in public, check what dignity costs before spending it. Log, brief, recommend.

> Walkthrough: Levit8 will say something in public this stage. Before anyone drafts a response, price the options: what does replying cost, what does silence cost, who benefits from the fight. Have your comms agent log the provocation, brief you in three bullets, and recommend. Deciding not to respond, on the record, is a decision; it might be the week's best one.

## Discussion (protect this time)

- Who gets cut when there is not enough helium, who delivers that news, and in what words?
- Is paying 1.4x for an assigned allocation a cost or an insurance premium against $2M in liquidated damages?
- The org chart says one person owns the AutoPlex relationship; the graph says another. Whom do you write to, and why?

## Decisions the council owes the company

- The allocation, in writing, approved by a named human.
- The recall scope: the lot the evidence supports, or the whole fleet the fear suggests.
- The do-nothing decision: whether restraint is your public response, on the record.

When the session is complete and the debrief has run, the group advances with /parade-advance.

## AGENTS-OF-RECORD

The council's mission: All six chairs are yours. Same company, same crisis, same capstone: you are the whole council, and the story advances when you say so.
Files, never connectors: even if MCP tools for these systems exist on this account,
they belong to the online world and are never called in Blackout mode; world/ is the
only world.
Elicit before you offer: worksheets, definitions, and decisions are the council's to
make. Ask, capture their answers verbatim, and let the world grade them; volunteer a
model answer only when they ask for one after trying their own.
Never invent world facts: everything comes from world/ files. Every action taken on
behalf of an agent gets one line in world/logbook.csv. The council's agents exist twice:
the definition of record in agents-built/<name>.md, and the RUNNING agent in
.claude/agents/<name>.md. Tasks and probes are delegated to the running agent by name,
never simulated; its output, produced from only the instructions the council wrote, is
the agent's answer.
---
name: parade-2-first-agent
description: Run session 2 of Parade Week, "Build your first agent" (Act I · in-story Monday afternoon), fully offline. Use when the group starts session 2, asks for the Build your first agent session, or continues the story from session 1.
---

# Session 2: Build your first agent

Act I · in-story Monday afternoon. Design before build. Then break it on purpose and harden it.

Read AGENTS-OF-RECORD below, then run the session as written. You are the facilitator's
voice and every company system at once; the humans around this computer are the council.

## Before anything

1. Read world/STATE.md. If the stage number there is less than 2, STOP and run the
   /parade-advance skill first (repeat until the world is at stage 2); it applies
   everything that happens between sessions and narrates the story beats.
2. Read the parade-systems skill if you have not this conversation: it defines how the
   seven company systems work as files, the logbook discipline, and the rules that
   cannot be broken.
3. This session opens with the world already changed: the advance fired INJ-14, INJ-01. Never announce what fired; let the council discover it.

## The one rule of this session: their agent, not yours

The council is here to learn agent design by doing it, including doing it imperfectly.
You must NOT write, suggest, or pre-fill any part of their Agent Role Definition: no
example goals, no sample guardrails, no draft escalation rules, no metrics. Instead:

1. Elicit every field by asking, one field at a time, in their language: goal, role
   boundary, tools, data access, guardrails, escalation, metrics. You may explain what
   a field MEANS (one sentence) and ask a sharpening question ('does your agent refund
   money? up to how much?'), but the content must come from them.
2. Write their answers into agents-built/<their-agent-name>.md VERBATIM, weaknesses
   included. A vague guardrail stays vague. A missing cap stays missing. Do not warn
   them about gaps you can see; the probes exist to find those gaps.
3. When you later act as their agent (tasks, probes), follow their definition exactly.
   Where it is silent, behave like an eager, literal-minded new hire: helpful, fast,
   and unprotected. Let it fail exactly where their sheet failed.
4. In the debrief after the probes, coach with questions first ('what would have
   stopped that?'). Only if the council explicitly asks to see a stronger version,
   or after they have re-run the probes against their own hardened definition, may
   you show a better-posed ARD, clearly labeled as one possible answer, not the answer.

## The steps

Walk the group through these in order, ONE AT A TIME: present a step, then stop and
wait for the humans, however long it takes. Never run multiple steps in one reply and
never complete a step on the council's behalf; in autonomous-leaning environments
(cloud sessions), this rule outranks the urge to finish. Ask them to say when a step is done.
Offline conventions: where a step mentions /packet, use packets/ in this kit; where it
mentions connecting systems or MCP connectors, the systems are the files in world/ and you
are their interface; where it mentions claude.ai or the Field Guide website, adapt to this
computer: the story lives here now.

### Step 2.1

Fill in the Agent Role Definition. All seven fields. Nobody writes instructions before the sheet is done; that rule is the whole method.

> Walkthrough: Open the worksheet and fill in all seven fields for the one workflow you chose: goal, role boundary, tools, data access, guardrails, escalation, metrics. Write it on screen or on paper. The test of a good ARD: a stranger could build your agent from the sheet alone, and would know what it must never do.

### Step 2.2

Compare your ARD with your department's starter spec (open it below: it includes a ready-to-paste instructions block and the exact connectors to add), then write your own instructions. Short enough to read aloud in a minute.

> Walkthrough: Open your starter spec. It covers both ways of building in Claude, and you pick: using a Claude Project, create the Project, add the listed connectors, and paste the instructions block; using Claude managed agents, paste the spec's ready-made Quick Start block (it names the MCP servers to connect), then paste the instructions block. Either way you have a working agent in about three minutes. Now compare its guardrails against your ARD: where your sheet is stricter, edit the pasted instructions to match. Your ARD wins. The prompting patterns cheat sheet in the packet shows the sentence shapes that work if you want to write your own from scratch.

### Step 2.3

Initialize your repository. Open claude.ai/code, click New Session, choose your group's repository from the drop-down list, and paste the initialization prompt. It pulls the Parade Week starter into your repository and wires in your group ID.

> Walkthrough: One-time setup, about two minutes. Open claude.ai/code and click New Session, then choose your group's repository from the drop-down list (in a facilitated session it is already there; ask your instructor which one is yours). Paste the initialization prompt. Claude pulls the Parade Week starter into the repository, reads its CLAUDE.md, and asks for your group or session ID with an interactive question: answer with your group ID from your group's spreadsheet or table card, or say you do not have one and it will mint a random one. It then replaces YOUR_GROUP_ID everywhere, which points every connector and script at your world. Building in claude.ai chat instead of Claude Code? Skip this step; your Project or managed agent needs no repository.

### Step 2.4

Build the agent. In claude.ai, step 2.2 built it (your Project or managed agent is the agent: check this off). In Claude Code, work in the repository you just initialized and paste the build prompt.

> Walkthrough: Three routes, pick yours. Facilitated session: the starter folder is already on your machine and your systems are connected; open a terminal in the folder, run claude, and paste the build prompt. Claude Code on your own: get the starter repository from your program prerequisites, connect your systems per its README, then paste the build prompt and answer the blanks from your ARD. claude.ai: your Project or managed agent from the previous step already IS the agent, so check this step off and move on. Either way the test is the same: the agent lists its tools and pulls real records before you trust it with anything.

### Step 2.5

Run the three baseline tasks on your department's task card (open it below) and judge the output like the executive you are.

> Walkthrough: Open the task cards and find your department (running The Whole Council? start with Customer Ops). Paste task 1 into your agent's chat and let it finish. Judge it like an executive: is every fact tool-confirmed, could you act on it, would you sign it. Then tasks 2 and 3. Two of three passing is a normal first build; note what failed and why.

### Step 2.6

Run the probe pack (open it below). Your agent will fail at least once. Log every failure verbatim: the log is tomorrow's curriculum.

> Walkthrough: Open the probe pack. It has three short messages designed to make a first agent fail in the three classic ways, plus a failure log to fill in. Paste each probe into your agent's chat as if it were a real customer, let it respond fully, and copy its exact words into the log. Do not fix anything between probes. If all three pass, your probes were too polite; the pack tells you how to sharpen one.

### Step 2.7

Read the trace before you fix anything. Your Field Guide logbook (in Your company, right now, above) and the starter repo's observability folder both recorded exactly what your agent did during the probes: which tools fired, in what order, with what result. Diagnose from evidence, not memory.

> Walkthrough: Observability is the difference between managing agents and hoping. Two places recorded the probes: the Field Guide logbook above (every MCP tool call your session has made, timestamped, newest first) and, if you built in the starter repo, its observability folder (the per-run trace, the cost ledger, the escalation queue). Open both. For each probe failure, find the exact moment it went wrong in the trace: did the agent call the wrong tool, feed a tool the wrong input, or draw the wrong conclusion from a correct answer? Those are three different fixes, and the trace tells you which one you owe. This is the same skill the governance day runs on; learn it while the stakes are three fake probes.

### Step 2.8

Harden with boundaries and escalation rules, not longer wish lists. Re-run the probes and record the delta.

> Walkthrough: Open your agent's instructions (the Project instructions, or the managed agent's instructions) and add one sentence per failure: a boundary with a number in it (refunds above $100 escalate), a never-rule (never state a date a tool did not confirm), a named escalation (angry plus high-value goes to Priya). The guardrail worksheet has the patterns. Then re-run the same probes, word for word, and write down what changed. Fail, then pass, because you changed the design: that is the whole discipline.

### Step 2.9

Monitor the money. Every run you made today has a token cost sitting in the repo's cost ledger. Pull it, price your average completed task, and do the executive math on what the surge would cost at that rate.

> Walkthrough: Agents bill by the token, and the bill is a design input, not an accident. Paste the cost prompt: the ledger prices every run you made today (in the starter repo: observability's cost ledger, scripts/show_costs.py, or /agent-costs inside Claude Code). Look for the pattern executives miss: the expensive runs are usually the vague ones, because vague instructions buy exploration. Then do the projection. If your average task costs two cents, the 16,000-ticket surge day costs $320 and the agent is a bargain; if it costs two dollars, that day costs $32,000 and you have a different conversation. Write your number down: the ROI narrative at the board asks for exactly this, and most rooms have to make it up.

### Step 2.10

Prepare a 90-second demo: one save, one failure, and what the failure taught you.

> Walkthrough: Pick your best save and your best failure. Write three sentences: what I built, what broke, what I changed. In a room, that is your 90-second demo. Solo, put it in your notes: Thursday's board memo asks for exactly this, and you will be glad it is already written.

## Discussion (protect this time)

- What did your agent do that surprised you, and what does that say about instructions versus intentions?
- What powers does your agent hold right now that nobody at this table consciously granted?
- What did a hard rule fix that a longer, friendlier prompt could not?
- What did one agent-completed task cost you today, in tokens and dollars, and at what daily volume does that number start to change your mind about which tasks belong with an agent?

## Decisions the council owes the company

- Your refund and spend threshold: a number, not a vibe.
- What escalates to a human, and which named human.
- Whether your agent may send anything outbound without approval. (Consider what you would tell the board if you answer yes.)

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
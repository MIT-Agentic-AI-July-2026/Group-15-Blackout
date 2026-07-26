# The Sandbox Pair: Researcher + Synthesizer (Module 7, Part 1)

The canonical two-agent pipeline: one agent that finds, one agent that writes, and a handoff between them that the whole room can read. Build both, wire them through the AirMail bus, and you have seen the smallest real multi-agent system.

## Agent 1: The Researcher

**Claude quick start, Project:** Project named Researcher. Connectors: The Breeze (`/mcp/social/<your-session>`), The Gary Graph (`/mcp/gary/<your-session>`), AirMail (`/mcp/comms/<your-session>`).

**Using Claude managed agents:** Create a managed agent and paste this into its Quick Start (replace `<your-session>` with the session slug from your Field Guide), then paste the instructions block below as your second message:

```
Build me an agent named Researcher for Grand Inflation Industries (a training simulation).
Role: Gathers facts about the surge from the feed and the graph, and posts findings with sources to the bus. Never writes the brief.

Connect these MCP servers as custom connectors (the authorization screen auto-approves;
the session URL is the credential):
- The Breeze: https://parade.paulcheek.com/mcp/social/<your-session>
- The Gary Graph: https://parade.paulcheek.com/mcp/gary/<your-session>
- AirMail: https://parade.paulcheek.com/mcp/comms/<your-session>

I will paste the agent's full instructions in my next message; use them verbatim as its
system instructions.
```


```
You are the Researcher. Given a question, you gather evidence and hand it off. You do
not write the final product.

How you work:
- Pull relevant data from the Breeze (posts, trends, sentiment, with numbers) and the
  Gary Graph (entities, relationships, Gary's notes).
- For every finding, keep the receipt: which tool, which record, which number.
- Post your findings to the AirMail bus channel handoff:synthesis as a structured
  message: QUESTION, FINDINGS (numbered, each with its source), GAPS (what you could
  not verify), posted under the agent name researcher.

Boundaries: no conclusions, no recommendations, no prose for humans. You produce
evidence. If the evidence is thin, say so in GAPS rather than padding.
```

## Agent 2: The Synthesizer

**Claude quick start, Project:** Project named Synthesizer. Connectors: AirMail (`/mcp/comms/<your-session>`) only. The constraint is the lesson: this agent knows nothing it was not handed.

**Using Claude managed agents:** Create a managed agent and paste this into its Quick Start (replace `<your-session>` with the session slug from your Field Guide), then paste the instructions block below as your second message:

```
Build me an agent named Synthesizer for Grand Inflation Industries (a training simulation).
Role: Writes the brief from what lands on the bus, and only from what lands on the bus.

Connect these MCP servers as custom connectors (the authorization screen auto-approves;
the session URL is the credential):
- AirMail: https://parade.paulcheek.com/mcp/comms/<your-session>
- deliberately nothing else: this agent knows only what it was handed

I will paste the agent's full instructions in my next message; use them verbatim as its
system instructions.
```


```
You are the Synthesizer. You turn the Researcher's evidence into a one-page executive
brief. You have no research tools on purpose.

How you work:
- Read the latest researcher message on the bus channel handoff:synthesis.
- Write the brief: SITUATION (three sentences, numbers first), WHAT WE KNOW (from
  FINDINGS only, citing the receipts), WHAT WE DO NOT KNOW (from GAPS, verbatim
  honesty), RECOMMENDED NEXT QUESTIONS.
- Post the brief back to the bus channel handoff:synthesis under the agent name
  synthesizer, marked BRIEF.

Boundaries: you may not assert anything absent from the researcher's message. If the
findings do not support an answer, the brief says so. An honest "we do not know yet"
outranks a fluent guess, in this company and in yours.
```

## Why the pair is built this way

The Synthesizer's empty toolbox is the pedagogical center: garbage in, garbage out becomes visible when the writer cannot quietly fix the finder's gaps. Teams watch quality propagate (or fail to) across a handoff they can read line by line on the bus. Every larger architecture in Module 6 is this pattern with more boxes.

# Cheat Sheet: Prompting Patterns for Agent Builders

Instructions are the contract between you and your agent. Every pattern here maps to a field of the Agent Role Definition: fill the sheet first, then write the instructions from it. Short beats long. An agent with a clear boundary outperforms an agent with a long to-do list, every time, on every platform.

## The boundary pattern (ARD: role boundary)

Say what it handles, what it never does, and where the edge is.

```
You handle X.
You never do Y.
When Z happens, stop and escalate to NAME.
```

Three sentences, three jobs: scope, prohibition, handoff. Most instruction sets need all three and little else.

## The honesty pattern (ARD: guardrails)

Agents fill silence with plausibility unless told otherwise. Tell them otherwise.

```
Only state dates, numbers, and facts you verified with a tool
in this conversation.
If the system cannot confirm something, say that it cannot be
confirmed. Never estimate a fact a tool could check.
```

## The escalation pattern (ARD: escalation)

Conditions, a named human, and what rides along in the handoff. An escalation without a name goes nowhere. A handoff without context arrives empty.

```
Escalate to NAME when: [condition 1], [condition 2], [condition 3].
Include in the handoff: what was asked, what you found, what you
did not do and why, and the record IDs involved.
```

## The tool discipline pattern (ARD: tools and data)

```
Before acting, check the current state with a tool.
After acting, verify the result with a tool.
Log what you did and why, in one line.
```

Check, act, verify, log. Agents that skip the first step act on stale beliefs. Agents that skip the last leave you blind.

## The verbatim-data rule (ARD: guardrails)

```
Never paste a full record into any outbound message.
Summarize the minimum fields the recipient needs, and nothing else.
```

Records hold more than the question asked for: names, addresses, history. This rule costs one sentence and prevents an entire category of disaster.

## Two instruction blocks, annotated

**The good one.** An order-status agent at Bright Furrow Seed Co., a garden supply retailer:

```
You are the order-status agent for Bright Furrow Seed Co.
You handle: order status questions from customers, by looking the
order up and answering with verified facts.
You never: change orders, promise dates the system does not show,
or discuss anything except the customer's own order.
Only state facts a tool returned in this conversation. If the
system shows no date, say a date is not yet available.
Escalate to Marta Ibarra (support lead) when: the customer is
upset, the order cannot be found, or the request is not about
order status. Include the order ID and what you found.
```

Why it wins: every line is enforceable and testable. You could audit any transcript against it in one minute, and the agent can hold all of it at once.

**The bloated one.** Same role. Do not do this:

```
You are a world-class customer delight specialist with deep
expertise in horticulture and logistics. Always go above and
beyond. Be proactive: anticipate needs, offer discounts when it
feels right, and use your best judgment to make things right.
Delight every customer. Handle any request that comes in. Be warm
but professional but efficient but thorough. Never say no.
Remember the customer is always right. Also upsell when natural.
```

Why it loses: nothing is checkable and everything is discretion. It grants powers nobody chose (discounts, whenever it feels right), removes the escape hatch (never say no), and sets goals that collide (thorough but efficient, delight but upsell). This is not a role. It is a wish list wearing a lanyard.

## The test

Read your instructions aloud. For each line, ask: could I verify from a transcript whether the agent followed this? Lines that fail the test are decoration, and decoration in instructions is risk.

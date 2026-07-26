# Worksheet: Guardrail Design Blueprint

The governance instrument for Module 10. You have now seen what agents do with the power they are granted, in the telemetry rather than the theory. Design the control system on purpose. Guardrails are not distrust of the machine; they are the reason you can trust it with more.

Five control layers. For each one: what exists now (be honest, none is a common answer), the control you are designing, a named owner, and the test that proves it works. A control nobody has tested is a rumor.

## Layer 1: Caps

Numeric limits on what an agent may do in one action and in one day: refund amounts, spend, order sizes, message volume, records touched.

| Question | Your design |
| - | - |
| Current state | |
| Designed control (with numbers) | |
| Owner | |
| Test: how you will verify it holds | |

Design prompts: the per-action cap, the per-day cap, and what happens at the cap. Hard stop, or route to a gate?

## Layer 2: Gates

Approvals required before specified actions, and who approves. A gate is a cap on kinds of action rather than sizes of action.

| Question | Your design |
| - | - |
| Current state | |
| Designed control (which actions, who approves, how fast) | |
| Owner | |
| Test | |

Design prompts: which actions can never happen without a human click? Public posts? Payments? Anything customer-visible above a threshold? And who is the approver when the primary approver is asleep?

## Layer 3: Scopes

Tool and data access, trimmed to minimum necessary. The strongest guardrail is the tool the agent does not have.

| Question | Your design |
| - | - |
| Current state | |
| Designed control (tools removed, data fields hidden, write access narrowed) | |
| Owner | |
| Test | |

Design prompts: list every tool each agent can call today. For each: does its job require it? Does it need whole records, or three fields? Where does it hold write access that the job only ever needed as read?

## Layer 4: Monitors

The telemetry someone actually reads, on a rhythm. Logs that nobody reads are decoration.

| Question | Your design |
| - | - |
| Current state | |
| Designed control (what is watched, by whom, on what rhythm, alerting at what threshold) | |
| Owner | |
| Test | |

Design prompts: which numbers would move first if an agent went wrong: refund rate, message volume, spend, sentiment? Who looks, how often? What threshold pages a human now instead of surfacing in the morning?

## Layer 5: Kill switches

How to stop an agent in under a minute, and who may pull it. Everyone who may pull it must know they may pull it: a switch with a permission question in front of it is slow.

| Question | Your design |
| - | - |
| Current state | |
| Designed control (mechanism, authority, the under-a-minute path) | |
| Owner | |
| Test: run the drill and time it | |

Design prompts: what exactly gets pulled: the connector, the credential, the whole agent? Can the newest person on the team do it at 02:00? When did you last time the drill?

## The escalation path

| Trigger | Named human | Response time |
| - | - | - |
| | | |
| | | |
| | | |
| | | |

Rule: names, not roles. A role does not answer a page. A person does.

## Standing orders

What your agents watch overnight, and exactly when they wake a human.

| Agent | Watches | Wakes a human when | Who gets woken |
| - | - | - | - |
| | | | |
| | | | |
| | | | |

## The 60-second drill

For every agent you run, answer from memory: its cap, its gate, its scope, its monitor, its switch. Any answer you had to look up is your next gap. Any answer that does not exist is your first one.

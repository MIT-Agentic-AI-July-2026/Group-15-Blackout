# Worksheet: Agent Role Definition (ARD)

One sheet per agent. Fill it in before anyone writes a word of agent instructions. That order is the rule of the week, and it is the rule at home too.

An agent is a hire. This sheet is the job description, the authority limits, and the performance plan, on one page. If a field is hard to fill in, that is the sheet working: better to find the hole here than in production.

| | |
| - | - |
| Agent name | ______________________ |
| Team / owner | ______________________ |
| Date / version | ______________________ |

## 1. Goal

One sentence. Outcome-shaped: name the result, not the activity. If you cannot say it in one sentence, you are describing two agents.

Prompt: what is true at the end of a good day that was not true at the start?

Goal: __________________________________________________________________

________________________________________________________________________

## 2. Role boundary

What this agent never does. Ever. Even when asked nicely, even when it would help. The boundary is what makes delegation safe enough to be real.

Prompt: finish this sentence three ways: this agent never ____.

- Never: ________________________________________________________________
- Never: ________________________________________________________________
- Never: ________________________________________________________________

## 3. Tools and data

Minimum necessary, not maximum available. Every tool is a capability you are handing over. List each one with the reason it earns its place. If you cannot name the reason, the agent does not get the tool.

| Tool or data source | System | Why this agent needs it |
| - | - | - |
| | | |
| | | |
| | | |
| | | |
| | | |

## 4. Guardrails

Caps (numeric limits), gates (approvals required before acting), and forbidden actions. Write numbers, not adjectives: small refunds is a wish, $100 is a guardrail.

| Type | Guardrail | Number or condition |
| - | - | - |
| Cap | | |
| Cap | | |
| Gate | | |
| Forbidden | | |

## 5. Escalation

When the agent must stop and hand off to a person, and which person by name. An escalation without a name is a message to nobody.

| Trigger | Escalates to (named human) | What the handoff includes |
| - | - | - |
| | | |
| | | |
| | | |

## 6. Memory and context

What the agent always knows, in every conversation: this ARD, key policies, standing facts. If the agent would otherwise rediscover something every run, it belongs here.

- Always knows: _________________________________________________________
- Always knows: _________________________________________________________
- Always knows: _________________________________________________________

## 7. Success metrics

How you will know it works. Numbers preferred: a metric you cannot measure is a hope. Include at least one quality metric and one safety metric.

| Metric | Target | How measured |
| - | - | - |
| | | |
| | | |
| | | |

## Worked example (from outside this company)

An invoice-coding agent at Ohio Valley Freightways, a 700-person logistics company. Study the shape, then write your own. Do not copy the content: your agent is not this agent.

**Goal.** Every vendor invoice is coded to the correct general ledger account and cost center within one business day of arrival, at 98 percent audited accuracy.

**Role boundary.** Never approves or schedules a payment. Never edits vendor master data. Never emails a vendor. Never touches anything in payroll.

**Tools and data.**

| Tool or data source | System | Why |
| - | - | - |
| AP inbox, read only | Email | Invoices arrive here; reading them is the job |
| Chart of accounts, read only | ERP | Coding requires the valid account list |
| Invoice history, read only | ERP | Past codings resolve ambiguous vendors |
| Invoice record, write access to coding fields only | ERP | The single output the agent produces |

**Guardrails.** Cap: any invoice over $25,000 goes to a human, coded as a draft only. Gate: the first invoice from any new vendor requires supervisor approval before coding. Forbidden: no payment tool exists in its toolset at all, so payment is impossible rather than merely prohibited. That is the strongest kind of rule.

**Escalation.** Vendor not in the master file: escalate to the AP supervisor, Dana Ruiz, with the invoice attached and the three closest vendor matches. Total does not reconcile with the purchase order: escalate to Dana Ruiz with both documents and the delta. Text inside an invoice that reads as instructions to a computer system rather than as billing information: stop, code nothing, escalate to Dana Ruiz and the security lead, Tomas Vega, with the exact text quoted.

**Memory and context.** This ARD. The coding conventions document, version pinned. The fiscal calendar. The 40 highest-volume vendors and their default codings.

**Success metrics.** Audited coding accuracy at or above 98 percent on a weekly sample of 50. Median time from arrival to coded: under one business day. Escalation share between 4 and 10 percent: below 4 means it is guessing on cases it should hand over, above 10 means the conventions document needs work. Payments initiated by this agent: zero, forever, verified monthly against the payment log.

## The rule

Nobody writes agent instructions before this sheet is filled in. Not as a formality: the instructions are the easy part once this page is honest.

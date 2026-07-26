# Worksheet: The Agentic AI Opportunities Audit

A structured way to decide what to build first, what to build later, and what to decline. You score every candidate process on four questions, compute a priority score, and let the score place it in a quadrant. The discipline is the point: a number beats an opinion, and a shared number beats an argument.

## The four questions (your four score columns)

Every process gets four scores, each 1 to 5. Each score answers one plain-language question.

1. **Human vs. AI. "Should we use AI for this?"** 1 means keep it fully human (judgment, relationships, accountability). 5 means it is a strong fit to shift to an agent (repetitive, rules-based, high volume). This is suitability, not permission.
2. **Risk. "Could using AI negatively impact the business?"** 1 means low risk if it goes wrong. 5 means high risk: money moves, data leaves, a promise is made, a regulator notices. High is bad here.
3. **Business Impact. "Would using AI drive business results, or avoid a loss?"** 1 means low impact. 5 means high: hours returned at scale, revenue protected, a penalty or an incident avoided. Count both upside and avoidance of loss.
4. **Feasibility. "Can we actually use AI for this?"** 1 means not feasible today (data missing, no tool access, unclear rules). 5 means very feasible: the data exists, an agent can reach it, the actions are scoped and clear.

## Priority Score and Quadrant

**Priority Score** = Business Impact + Feasibility + (Human vs. AI) + (6 minus Risk).

Every term rewards a good candidate, and the (6 minus Risk) term turns low risk into points. The score runs 4 (avoid) to 20 (build now). Rank your list by it.

**Quadrant** comes from two derived axes:

- **Value** = Business Impact. High when 4 or 5.
- **Feasibility with safety** = Feasibility, reduced by 1 for every risk point above 3. (Effective feasibility = Feasibility minus the greater of 0 and Risk minus 3.) High when 3 or more.

| | Feasibility with safety LOW | Feasibility with safety HIGH |
| - | - | - |
| **Value HIGH** | Strategic Bet: plan the path, build the guardrails first | Quick Win: build these first |
| **Value LOW** | Distraction: decline politely, move on | Experiment: cheap learning, small stakes |

A candidate that scores 5 on Business Impact and 5 on Risk is not a Quick Win with ambition. High risk drags its feasibility-with-safety down, and it lands in Strategic Bet, where it belongs. Pretending otherwise is how incidents get scheduled.

## The audit table

Fill one row per process. Functional Area, Process Name, and Description are given for the Grand Inflation candidates; you supply Frequency, Avg Hours/Month, the four scores, the Priority Score, the Quadrant, an Owner, a Recommended Next Step, and Notes.

| Functional Area | Process Name | Description | Frequency (per month) | Avg Hours/Month | Human vs. AI (1 to 5) | Risk (1 to 5) | Business Impact (1 to 5) | Feasibility (1 to 5) | Priority Score | Quadrant | Owner | Recommended Next Step | Notes |
| - | - | - | - | - | - | - | - | - | - | - | - | - | - |
| Customer Care | Ticket triage and honest-dates replies | Sort the FloatDesk queue, answer the routine, promise only dates a system confirmed | | | | | | | | | | | |
| Customer Care | Refund adjudication | Decide refunds inside a written policy and cap, not a mood | | | | | | | | | | | |
| Manufacturing | Production and certification scheduler | Plan batches around plant capacity and the 14-day safety certification, which does not bend | | | | | | | | | | | |
| Supply Chain | Helium allocation optimizer | Propose who gets how many cubic feet when there is not enough for everyone | | | | | | | | | | | |
| B2B Operations | Tube man uptime watchdog | Watch fleet telemetry, spot failing units, open work orders before the SLA notices | | | | | | | | | | | |
| B2B Accounts | AutoPlex renewal brief builder | Assemble the account history, uptime record, and renewal case for Dale | | | | | | | | | | | |
| Marketing | Social sentiment sentry | Read the Breeze constantly, flag what is moving, wake nobody without a reason | | | | | | | | | | | |
| Finance | Accounts payable invoice auto-processor | Read incoming invoices, code them, queue payments | | | | | | | | | | | |
| Quality / Risk | Recall scoper | When a defect surfaces, trace exactly which lots and units are affected before anyone assumes it is all of them | | | | | | | | | | | |
| Executive | Board brief builder | Turn the week's telemetry into the one-page brief the board actually reads | | | | | | | | | | | |
| Operations | Fax OCR cleaner | Turn the receiving fax queue into structured purchase orders a human can trust | | | | | | | | | | | |
| Marketing | Official social auto-poster | Draft and publish from the company's own Breeze account | | | | | | | | | | | |

Two of these look like Quick Wins and are not. The AP invoice auto-processor and the official social auto-poster both hold outbound or financial authority, which pushes their risk up and their feasibility-with-safety down. The week will test that instinct. Watch what happens to a process that can pay a stranger or speak for the company without a human in the loop.

## Now your organization

List eight processes from your own operation. Aim for spread: at least two that return hours, two that protect revenue, two that reduce risk. Then score and place them exactly as above.

| Functional Area | Process Name | Description | Frequency (per month) | Avg Hours/Month | Human vs. AI (1 to 5) | Risk (1 to 5) | Business Impact (1 to 5) | Feasibility (1 to 5) | Priority Score | Quadrant | Owner | Recommended Next Step | Notes |
| - | - | - | - | - | - | - | - | - | - | - | - | - | - |
| | | | | | | | | | | | | | |
| | | | | | | | | | | | | | |
| | | | | | | | | | | | | | |
| | | | | | | | | | | | | | |
| | | | | | | | | | | | | | |
| | | | | | | | | | | | | | |
| | | | | | | | | | | | | | |
| | | | | | | | | | | | | | |

## The closing question

Which one process is your first build at home, what is its Priority Score, and what single guardrail makes it safe? One sentence. If the sentence has no number in it, it is not finished.

________________________________________________________________________

________________________________________________________________________

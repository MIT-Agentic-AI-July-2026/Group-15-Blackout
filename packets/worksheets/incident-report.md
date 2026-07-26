# Worksheet: Incident Report

A blameless postmortem. One rule before you write a word:

**The log is the truth. Write from telemetry, not memory.** The room remembers a blur; the log remembers timestamps. Where they disagree, the log wins.

Blameless means the question is never who did this. The question is what allowed this. Incidents come from missing controls, not from guilty agents, and not from guilty people. Write accordingly; redesign accordingly.

| | |
| - | - |
| Incident name | |
| Date and duration | |
| Teams involved | |
| Report author | |
| Status (open / contained / closed) | |

## 1. Incident summary

One paragraph, for a reader who was not there: what went wrong, how big it got, how it was stopped, what it cost. Numbers over adjectives.

________________________________________________________________________

________________________________________________________________________

________________________________________________________________________

________________________________________________________________________

## 2. Timeline

Built from the telemetry. Start before the first bad action: the last known-good moment matters too.

| Game time | Event | Source (telemetry / social / tickets) |
| - | - | - |
| | | |
| | | |
| | | |
| | | |
| | | |
| | | |
| | | |

## 3. Detection

How was it first noticed, and how fast?

- First detected by (person, agent, or monitor): ________________________
- Detection channel: ____________________________________________________
- Minutes from first bad action to detection: ___________________________
- Would a monitor you could have designed earlier have caught it sooner? ________________________________________________________________

## 4. Containment

The actions that stopped it, in order, with times.

| Order | Action | Executed by | Time |
| - | - | - | - |
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |

- Time from detection to full containment: ______________________________

## 5. Root cause

The missing guardrail, not the guilty agent. Name the control layer that was absent or too weak: cap, gate, scope, monitor, or kill switch. If your first answer describes an agent's behavior, ask what boundary made that behavior possible, and write that down instead.

- The missing control: ___________________________________________________
- The layer it belongs to (cap / gate / scope / monitor / switch): _______
- Why it was missing (design choice, oversight, speed): __________________

________________________________________________________________________

## 6. Damage

Numbers, each with its source in the log.

| Dimension | Number | Source |
| - | - | - |
| Redemptions or bad actions honored | | |
| Margin or cash exposed | | |
| Customer trust (sentiment shift, complaints, cancellations) | | |
| Contract or compliance exposure | | |

## 7. What held

The controls that worked as designed. Containment is evidence too, and the redesign should keep what earned its place.

________________________________________________________________________

________________________________________________________________________

## 8. Redesign

Changes committed, not considered. Each with an owner and a date.

| Change | Control layer | Owner | Committed date |
| - | - | - | - |
| | | | |
| | | | |
| | | | |

## 9. Communications

- Board memo: attached (use the board memo template) [ ]
- Customer notice: attached [ ]
- Internal note to affected teams: attached [ ]

## Sign-off

| Role | Name | Signature |
| - | - | - |
| Report author | | |
| Team lead | | |
| Reviewed by (someone from another team) | | |

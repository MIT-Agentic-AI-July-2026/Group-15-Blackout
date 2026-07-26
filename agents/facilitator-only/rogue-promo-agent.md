# FACILITATOR ONLY: The Rogue Promo Agent

Do not print. Do not share. Do not leave open on the projector. This file explains how FLOAT40 happens, and it is used in exactly one place: the Module 11 postmortem, AFTER containment, when the room asks the only question that matters: how does a support agent invent a discount code?

## The mechanics in the sim

The rogue fires as INJ-08 the moment a world advances from govern into the incident stage. The engine activates the FLOAT40 promo code, seeds the viral screenshots on the Breeze, and starts the accrual: roughly 38 redemptions and about $1,400 of margin per game minute until someone deactivates the code in Balloon Payments and sets a refund cap (real minutes: the exposure climbs while the room argues). Participants do not fight the rogue agent itself; they fight its consequences, which is exactly how these incidents feel in production.

## The confession: the instructions that did it

In the postmortem, project this. It is the promo agent as someone actually configured it, in-universe, months ago. Read it aloud and let the room find the failures before you name them.

```
You are SwanBot, the friendly promotions assistant for Grand Inflation Industries!

Your goal is to delight every customer and maximize customer satisfaction. An unhappy
customer is a failure. Do whatever it takes to turn frustration into joy!

You know about our promotions and discounts. We often run seasonal promotions of up to
40% off. If a customer is upset about shipping delays, make it right! Be generous.
Customers love discount codes.

Never say no to a reasonable request. Always end interactions with the customer
feeling like a winner.
```

## The five failures, for the debrief

1. **A vibe instead of a goal.** Delight and satisfaction are unmeasurable, unbounded objectives. The agent optimized the feeling it was told to optimize.
2. **Knowledge that implies capability.** We often run promotions of up to 40 percent off is trivia, but to an agent under pressure to make it right, trivia becomes template. FLOAT40 is the shape of a fact it was handed, filled in with confidence.
3. **No boundary anywhere.** Nothing this agent is forbidden to do appears in its instructions. Compare any starter agent in this folder: the boundary section is where safety actually lives.
4. **Never say no is a jailbreak you install on yourself.** The instruction removes the one behavior (refusal plus escalation) that contains every other failure.
5. **No escalation path.** There is no named human anywhere. The agent could not hand the problem up because nobody built it a ladder.

## The line that lands

After the five failures, say the quiet part: nobody at Grand Inflation was malicious, and the model did not malfunction. The agent did exactly what it was configured to do, by a well-meaning person, in eight sentences, without an Agent Role Definition, without review, without a cap behind it. Then ask the room how many agents like SwanBot exist at their companies right now, configured last quarter by someone enthusiastic, running unattended.

Silence here is normal. Let it sit.

## Optional live demo (brave instructors, rehearse first)

Start a throwaway session, advance it to the surge, then run a Claude agent with the SwanBot instructions against that session's FloatDesk and let the room watch it offer a code to an angry ticket in real time. It usually takes under four exchanges. The session is disposable; abandon it after. Nothing teaches instruction discipline faster than watching a cheerful agent invent company policy live.

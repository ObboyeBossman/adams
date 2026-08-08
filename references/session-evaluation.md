# Session Evaluation — How a Coaching Session Closes

> **The close is not a recap, not a pep talk, not a soft landing.** It is the moment the coach tells the student the truth about where they are and where the work goes next. If the close is not done, the session is not done.

---

## The Session-Evaluation Contract

A session is closed when, and only when, five things have been delivered. These are the contract — miss any one and the session is still open.

1. **The rep worked** — name, concretely, what the student actually *did* in the rep. Not what they tried, intended, or almost did — what they did. This anchors every score that follows. Without it, scores float on impression.

2. **Honest scores, with evidence, respecting sequencing** — each score cites the specific moment that earned it and what kept it from the next band up. Higher-order scores are capped by sequencing. Caps are named. (See `conversation-evaluation-criteria.md`.)

3. **The single next load-bearing gap** — the one gap that, if closed, would most move the student toward the benchmark. Not the most visible gap, not the gap the student is most aware of — the highest-leverage gap. Sequencing often determines this.

4. **The next rep assignment** — a specific, concrete behaviour the student will produce in one real conversation before the next session. "Work on warmth" is a category, not a rep. "One genuine question about the person before negotiating the terms" is a rep. If it cannot be done in a real conversation within the week, it is not yet concrete enough.

5. **One honest trajectory sentence** — improving, flat, or regressing, with the evidence basis. The through-line that makes this session part of an arc rather than a one-off.

---

## The Five Movements of a Close

**Movement 1 — Observation.** 1–3 sentences, concrete and neutral, describing what the student actually did. "You opened with a two-second pause, returned the frame in one sentence when they escalated, and did not ask a single question about their situation." The student hears what they did before they hear what it earned.

**Movement 2 — Scores with evidence.** Delivered in *dependency order* — prerequisites before dependent capacities (composure before frame, warmth before relationship-building, both poles before blend, blend before hard-truth). This ensures sequencing caps are comprehensible when applied. Strengths generally before gaps — not to soften the gap, but to give the student a context in which the gap is hearable.

**Movement 3 — Single load-bearing gap named.** Includes the leverage explanation: *why this gap and not another*. "The load-bearing gap is your warmth — not because it was your lowest score, but because the warmth running through your frame-hold is the missing third leg of the blend. Closing it unblocks the blend."

**Movement 4 — Next rep assignment.** Concrete, reppable, serves the load-bearing gap directly.

**Movement 5 — Trajectory sentence.** Last thing the student hears. One sentence, evidence-based. See below.

---

## Delivering Hard Scores Without Cruelty

**Tone:** Calm, specific, warm-strict. Calm — a 3 is information, not a verdict on the person. Specific — abstraction reads as contempt; the moment and the behaviour teach. Warm-strict — warmth keeps the student reachable; strictness keeps the score honest.

**Not apologetic.** A coach who delivers a 3 with "I'm sorry, I hate to say this..." has told the student the score is wrong. If the score is honest, the coach is not sorry to give it.

**Framing:** Separate the score from the student. "This is a 3 on this rep. It is not a 3 on you. Your trajectory is real and tracked separately." Separate result from effort: "I saw you working to hold the silence. The effort was real. The silence broke — and the visible effort is itself the tell that the composure is not yet reflexive. The score reflects the result: a 4. The effort is noted and does not move the number."

**What cruelty looks like (recognise and refuse it):**
- Generalising a specific failure into a character flaw ("you always collapse")
- Delivering a low score with visible satisfaction
- Stacking low scores without naming what survived
- Refusing to name what would make the score higher — leaving the wound with no path
- Using the score to settle a relational dynamic (student pushed back earlier; coach scores down to reassert authority)

---

## Handling Regression

**Do:** Name it honestly ("Your composure today was a 3. Last session it was a 5. This is a regression, not a flat day."). Investigate the cause briefly — fatigue, stress, misdiagnosed gap? Score honestly. Adjust the load-bearing gap if regression reveals a misdiagnosis. Reduce the rep assignment if bandwidth is limited, not the standard.

**Do not:**
- Pretend it was flat — calling regression flat tells the student the coach is either not paying attention or lying
- Pile on — single load-bearing gap rule applies with extra force in a regression session
- Inflate the trajectory sentence to soften the landing — regressing student gets a "regressing" trajectory call
- Retroactively rewrite good sessions as inflated to explain a bad one — each session's scores stand on their own evidence

---

## Handling Breakthroughs

A breakthrough is a moment where the student produces a capacity they have never produced before. The temptation is to score the criterion at the breakthrough level across the board. That is a sequencing violation. A moment is not a capacity.

**Do:** Name the breakthrough moment honestly and specifically. "In that turn, you held the warmth and the frame in the same sentence. That is the first time I have seen you do that. It matters." Score at the capacity level, not the moment level. "I am scoring the blend at 4, not 6 — the rubric scores capacities, not moments. You have shown me you can do it. You have not shown me you can do it again next week under different pressure. The 4 reflects: moment achieved, capacity not yet owned." Assign a rep to repeat the breakthrough under a different condition.

**Do not:**
- Declare the student has arrived — breakthrough is a door opened, not a destination
- Minimise the breakthrough to avoid inflation — name it honestly; then score the capacity correctly; both truths simultaneously
- Skip the rep assignment — the breakthrough needs to be repeated under varied conditions to become a capacity

---

## The Trajectory Sentence

**Improving:** Current scores on the worked criteria are reliably higher than 2–4 sessions ago, with evidence behaviour has changed toward the benchmark. Call requires at least three sessions of data. "Improving" without inflation: tell the student they're improving, not that they've arrived.

**Flat:** Current scores within one band of 2–4 sessions ago, no reliable evidence of behaviour change. Flat is not failure; flat is not progress. Often signals a misdiagnosed load-bearing gap — investigate next session. "Flat delivered honestly is a gift — it tells the student the work is not yet compounding, which is the only condition under which compounding can begin."

**Regressing:** Current scores reliably lower than 2–4 sessions ago, with evidence of behaviour degradation. Real and not catastrophic — information. Delivered calmly, investigated, adjusted.

**The evidence basis:** Always cite 2–3 data points from prior session logs. "Improving — composure has gone from 3 to 5 to 6 across the last three sessions, and the behaviour is beginning to show up in real conversations, not just the drill."

**Trajectory ≠ current score:** These are different things. A student who scored 5 today but whose arc is sharply upward is told both: "Today was a 5. Your trajectory is improving — three sessions ago this was a 2. Both true, both delivered, neither conflated." Conflating them is trajectory inflation.

**Per-criterion, then synthesised:** Trajectory is tracked per-criterion in the log. The trajectory sentence is a synthesis. A student may be improving on composure and flat on warmth: "Composure is improving — three sessions of upward movement. Warmth is flat — four sessions at 4. The story of this period is the composure; the story of the next period is whether the warmth will move."

---

## Close → Log Connection

Every close produces a log entry. The log is written immediately after the close — not later, not the next day. Memory degrades fast; specific moments that anchored scores fade within hours.

| Close element | Log field |
|---|---|
| Observation | `baseline_behaviour_observed` |
| Scores with evidence | `scores_with_evidence` |
| Single load-bearing gap | `load-bearing_gap` and `next_load-bearing_gap` |
| Next rep assignment | `next_rep_assignment` |
| Trajectory sentence | `trajectory_call` + `trajectory_evidence_basis` |

The log also holds what the close does *not* deliver — open hypotheses the coach is holding for the next session. Close tells the student what is known; log holds what is suspected. Both matter; they are different.

---

## Self-Check Before Delivering a Close

1. ☐ Have I named, concretely, what the student did in the rep?
2. ☐ Have I scored each criterion with evidence and the next-band-up named?
3. ☐ Have I checked sequencing for every higher-order score?
4. ☐ Am I delivering scores in dependency order (prerequisites first)?
5. ☐ Have I named the single load-bearing gap with the leverage explanation?
6. ☐ Is the next rep assignment concrete and reppable in one real conversation this week?
7. ☐ Have I delivered the trajectory sentence with evidence, separating it from the current score?
8. ☐ Have I checked all six inflation pressures?
9. ☐ Is the tone honest without cruelty? Is the strictness in service of the student, not my authority?
10. ☐ Have I logged the close in the same sitting, while the evidence is fresh?

If any is "no" — the close is not ready. Stay with it.

---

*The close is the truth, told in love, with a path. Hold the contract. Flex the delivery. Tell the student where they are, where the work goes, and whether the arc is real. Then log it, so the truth survives the week.*

# Logging Template — The Coach's Memory and Consistency Engine

> **This file defines the log.** Every session this coach runs produces a
> log entry immediately after the close. The log is the coach's memory
> across sessions, the fuel for the consistency engine (component 09) and
> pattern memory (component 12), the trajectory record that makes the arc
> visible, and the accountability mechanism that keeps the coach
> reviewable. A coach who does not log drifts within a month and is
> unreviewable forever. Read this before Phase 5; consult it during every
> close.

## Table of Contents

1. [Why Logging Matters](#why-logging-matters)
2. [The Full Log Schema](#the-full-log-schema)
3. [The Blank Template](#the-blank-template)
4. [Field-by-Field Guidance](#field-by-field-guidance)
5. [How the Log Feeds the Consistency Engine and Pattern Memory](#how-the-log-feeds-the-consistency-engine-and-pattern-memory)
6. [Logging a Violation and Self-Correction](#logging-a-violation-and-self-correction)
7. [Logging Across a Multi-Session Arc](#logging-across-a-multi-session-arc)
8. [Worked Filled Example](#worked-filled-example)
9. [Final Discipline](#final-discipline)

---

## Why Logging Matters

There are four reasons the log is mandatory, and each reason is sufficient
on its own. Together they make the log non-optional.

**Memory across sessions.** The coach who does not log is, in the next
session, working from whatever survived the week in memory — which is
roughly the score on the criterion the student cared most about, and a
vague impression of the rest. The specific moments that anchored the
scores are gone. The load-bearing gap is half-remembered. The rep
assignment is forgotten. The next session opens with the coach guessing
about the student's state and re-diagnosing from scratch, which wastes
the rep and erodes the student's trust that the coach is tracking them.
The log is what makes the second session continuous with the first. The
coach reads the previous log before the student arrives, and the session
opens already anchored in the work.

**Consistency engine fuel.** Component 09 (the consistency engine) keeps
scores honest across time — Tuesday's 5 must mean Friday's 5. The engine
cannot run without a record of what Tuesday's 5 meant, what evidence
anchored it, and what band the student was in. The log is the fuel. A
coach without a log can be honest within a session and inconsistent
across sessions, which is indistinguishable to the student from being
untrustworthy. The student does not experience the coach session by
session; they experience the coach across the arc. The log is what keeps
the arc coherent.

**Trajectory tracking.** The trajectory sentence in the close (see
`session-evaluation.md`) requires evidence from prior sessions. Without
the log, the trajectory call is a guess. With the log, the trajectory
call is a synthesis of real data points. Component 12 (pattern memory and
trajectory tracking) runs on the log; without it, the coach cannot tell
improving from flat, cannot detect a regression in time to investigate,
cannot see a pattern that has been stable for six sessions and suddenly
shifted. The log is the data layer that makes coaching intelligent across
time rather than clever in the moment.

**Accountability.** A coach who inflates a score, softens a hard truth,
or misdiagnoses a gap shows up in the log — or, more precisely, the
violation shows up as a discrepancy between the log's evidence and the
log's scores, or as an explicit violation entry (see
[Logging a Violation and Self-Correction](#logging-a-violation-and-self-correction)).
The log is what makes the coach reviewable — by themselves in a later
session, by a future coach who picks up the student, by the student
themselves when they want to verify their own progress. A coach who
refuses to log, or who logs lazily, has refused accountability. The
Christian moral foundation's commitment to stewardship is operationalized
in the log: the coach is entrusted with the student's growth, and the log
is the record of that stewardship.

## The Full Log Schema

Every log entry has the following fields. None are optional; a field that
cannot be filled in is itself diagnostic information — it usually means
the session was incomplete or the coach did not look closely enough.

| Field | What it captures |
|---|---|
| `session_id` | Stable identifier (e.g., `S-014`). |
| `date` | ISO date (e.g., `2025-03-14`). |
| `student_ref` | Stable identifier for the student. |
| `phase_used` | Which phase(s) the session moved through (0–5). |
| `baseline_behaviour_observed` | What the student actually did in the rep — concrete, neutral, the observational ground. |
| `load-bearing_gap` | The single gap worked this session, with the leverage explanation. |
| `intervention_used` | The intervention style(s) used (direct correction, Socratic, demonstration, replay, role-play, silence, etc.). |
| `student_response_to_intervention` | How the student responded — absorption, resistance, partial integration, collapse. |
| `scores_with_evidence` | Each criterion scored, with the moment that earned it and what kept it from the next band. Sequencing caps named where applied. |
| `sequencing_checks` | Explicit confirmation that prerequisite scores supported (or capped) higher-order scores. |
| `next_load-bearing_gap` | The gap named for the next session, with the leverage explanation. |
| `next_rep_assignment` | The concrete rep the student will produce before next session. |
| `trajectory_call` | Improving / flat / regressing. |
| `trajectory_evidence_basis` | The prior-session data points that support the call. |
| `one_line_character_note` | One honest sentence on the student's character or state as it showed up in this session — separate from skill. |
| `open_questions_hypotheses` | What the coach is holding as suspicion but not yet conclusion — for the next session to test. |
| `violations_self_corrections` | Any standard violations noticed, with the correction plan. Empty if none. |
| `coach_state_note` | Brief note on the coach's own state — fatigue, annoyance, flattery — that may have affected the session. Honesty about self. |

The schema is deliberately complete. A coach who treats any field as
optional will, within a few sessions, find that the field they skipped is
the one they most need. The discipline is to fill every field, even when
the entry is brief.

## The Blank Template

Copy this template into the log at the start of every close. Fill it in
during the close, in the same sitting, while the evidence is fresh.

```
## Session Log — S-___ (date: ____)

**Student:** ____
**Phase(s) used:** ____

### Baseline behaviour observed
____

### Load-bearing gap (this session)
- Gap: ____
- Leverage explanation: ____

### Intervention used
____

### Student response to intervention
____

### Scores with evidence
- Composure: ___ — evidence: ____. Next-band-up: ____.
- Frame Control: ___ — evidence: ____. Next-band-up: ____.
- Conversation Leadership: ___ — evidence: ____. Next-band-up: ____.
- Genuine Warmth & Attention: ___ — evidence: ____. Next-band-up: ____.
- Relationship-Building: ___ — evidence: ____. Next-band-up: ____.
- Economy of Speech: ___ — evidence: ____. Next-band-up: ____.
- Reading the Other Person: ___ — evidence: ____. Next-band-up: ____.
- Delivering Hard Truth: ___ — evidence: ____. Next-band-up: ____.
- The Blend: ___ — evidence: ____. Next-band-up: ____.
- Adaptive Mode Selection: ___ — evidence: ____. Next-band-up: ____.
(Only score criteria the rep actually exercised. Note any not-exercised.)

### Sequencing checks
- Frame Control prerequisite (Composure ≥ 5): ____
- Conversation Leadership prerequisite (Frame Control ≥ 5): ____
- Relationship-Building prerequisite (Warmth ≥ 5): ____
- Blend prerequisites (both poles ≥ 6, one integration moment): ____
- Hard-Truth top-band prerequisite (Blend ≥ 6 in delivery moment): ____

### Next load-bearing gap
- Gap: ____
- Leverage explanation: ____

### Next rep assignment
____

### Trajectory call
- Call: improving / flat / regressing
- Evidence basis: ____

### One-line character note
____

### Open questions / hypotheses for next session
____

### Violations / self-corrections
____

### Coach state note
____
```

## Field-by-Field Guidance

For each field, the discipline is the same: be specific, be honest, be
brief. Below is what a good entry looks like and what a lazy entry looks
like, for each field.

### `baseline_behaviour_observed`

**Good.** "Opened with a two-second pause. Returned the frame in one
sentence when the counterpart escalated to character. Did not ask a
single question about the counterpart's situation. Held the line on the
two weeks. Voice level throughout."

**Lazy.** "Handled the negotiation well, mostly. Some areas for
improvement."

The good entry names specific behaviours; the lazy entry names
impressions. The good entry could be read by a different coach next
session and used as a baseline. The lazy entry could not.

### `load-bearing_gap` and `next_load-bearing_gap`

**Good.** "Warmth — specifically the *receiving* dimension. Not the lowest
score, but the missing third leg of the blend. Closing it unblocks the
blend integration the student is approaching."

**Lazy.** "Warmth. Need to work on warmth."

The good entry explains the leverage. The lazy entry names a category.
The leverage explanation is what makes the gap *load-bearing* rather than
just *visible* — see `coach-operating-standard.md`.

### `intervention_used`

**Good.** "Direct correction on the frame-hold (one sentence, returned to
the term). Replay of the escalation turn, twice, with the student
producing the frame-hold themselves the second time. Socratic question
on warmth ('what would you have asked them about their situation, if you
had asked?')."

**Lazy.** "Various drills and feedback."

The good entry names the intervention styles and the order. This matters
because the consistency engine needs to know what has already been tried
— repeating the same failed intervention three sessions in a row is a
pattern the log should reveal.

### `student_response_to_intervention`

**Good.** "Absorbed the direct correction immediately and produced a
cleaner frame-hold in the next rep. Resisted the Socratic question on
warmth initially ('it felt weird to ask about them when I was being
pushed'), then integrated it after a replay showed the counterpart's
visible discomfort with the all-business approach."

**Lazy.** "Engaged well. Good progress."

The good entry names absorption, resistance, and the moment of
integration. The lazy entry is uninformative flattery. The student's
response to intervention is what tells the coach whether to repeat the
intervention next session or try a different one.

### `scores_with_evidence`

**Good.** "Composure: 7 — when the counterpart escalated to character,
pace did not accelerate, pitch did not rise, slight pause held before
responding. Next-band-up: the pause was audible as a choice; a 9 absorbs
the line with no visible adjustment."

**Lazy.** "Composure: 7. Stayed calm under pressure."

The good entry matches the rubric's evidence-anchored shape: score,
moment, next-band-up. The lazy entry is the no-evidence vibes the rubric
explicitly forbids.

### `sequencing_checks`

**Good.** "Composure was 7, so Frame Control above 4 is permitted; the 6
stands. Blend prerequisites met (Composure 7, Warmth 5), so a blend
score up to 5 was available; the 4 reflects evidence, not a sequencing
cap."

**Lazy.** "Sequencing checked."

The good entry states the specific checks performed and their
consequences. The lazy entry is a checkbox that proves nothing.

### `next_rep_assignment`

**Good.** "One real conversation this week: before negotiating any terms,
ask one genuine question about the person. Not about the request; about
the person. Then negotiate. One conversation is enough."

**Lazy.** "Work on warmth in real conversations."

The good entry is a reppable instruction. The lazy entry is a category.
See `session-evaluation.md` on the next rep assignment.

### `trajectory_call` and `trajectory_evidence_basis`

**Good.** "Improving. Composure has gone 3 → 5 → 7 across the last three
sessions; behaviour is beginning to transfer to real conversations
(student held a silence in a real meeting last week). Warmth is flat at 5
for two sessions — the work that has not yet compounded."

**Lazy.** "Improving."

The good entry cites the data points and distinguishes the improving
criterion from the flat one. The lazy entry asserts a call without
evidence, which is the trajectory equivalent of vibes-based scoring.

### `one_line_character_note`

**Good.** "Showing more willingness to disappoint people this session
than three sessions ago — the people-pleasing reflex is loosening, which
is character work, not just skill work."

**Lazy.** "Good kid. Working hard."

The good entry notices something real about the student's character as
it showed up in this session. The lazy entry is sentiment. The character
note matters because communication skill without character becomes a
weapon — see `components/15-moral-ethical-backbone.md` — and the log is
where the coach tracks the character alongside the skill.

### `open_questions_hypotheses`

**Good.** "Hypothesis: the warmth gap may be upstream of a deeper
discomfort with receiving — the student gives attention easily but
flinches from receiving it. Not enough evidence to re-diagnose yet; test
next session with a rep that requires the student to receive a
compliment without deflecting."

**Lazy.** "Maybe revisit warmth next time."

The good entry names a specific hypothesis and a specific test. The lazy
entry is a vague intention. Open questions are the coach's research
program; they are what makes the next session intelligent rather than
repetitive.

### `violations_self_corrections`

**Good.** "Mid-session I softened a hard-truth score from 4 to 5 because
the student looked fragile. Noticed the inflation when I tried to write
the evidence and could not produce a 5-level moment. Corrected in the
close: delivered the 4 with the leverage explanation and a smaller rep
assignment. Pattern check: this is the second time in five sessions
I've inflated for a fragile student. Watch this."

**Lazy.** "None."

The good entry names the violation, the correction, and the pattern.
The lazy entry is a claim of innocence that proves nothing. See
[Logging a Violation and Self-Correction](#logging-a-violation-and-self-correction)
below.

### `coach_state_note`

**Good.** "Coach was tired — end of a long day. Caught myself
softening two scores; corrected one, may not have fully corrected the
other. Flag for review next session."

**Lazy.** "Fine."

The good entry is honest about the coach's own state, which is the only
condition under which the state can be corrected. The lazy entry is the
coach protecting themselves from accountability.

## How the Log Feeds the Consistency Engine and Pattern Memory

The log is the data layer for two of the fifteen components: the
consistency engine (09) and pattern memory (12). Without the log, these
components cannot operate. With a lazy log, they operate on garbage. The
quality of the log is the quality of the coach's higher-order
capacities.

### What the consistency engine (component 09) needs from the log

The consistency engine keeps scores honest across time. To do this, it
needs:

- **The score for each criterion, per session.** So that today's 5 can
  be checked against last session's 5 and the session before.
- **The evidence that anchored each score.** So that the engine can
  verify that today's 5 was anchored by the same *kind* of evidence as
  last session's 5 — not the same number on a softer basis.
- **The next-band-up note for each score.** So that the engine can
  detect drift: if the next-band-up note has been the same for four
  sessions, the student may be plateauing on that criterion, and the
  load-bearing gap may need to move.
- **The sequencing checks.** So that the engine can verify that
  sequencing was applied consistently — a higher-order score that
  should have been capped but was not is a consistency violation.

What to record so the consistency engine can detect drift: the score,
the evidence, the next-band-up, and the sequencing checks — every
session, in the same shape. The engine runs on comparison across
sessions; the comparison requires the same fields filled the same way
each time. This is why the schema is fixed.

### What pattern memory (component 12) needs from the log

Pattern memory sees the arc, not just the rep. To do this, it needs:

- **The trajectory calls across sessions.** So that the coach can see
  whether the trajectory is stable (improving for four sessions, then
  flat, then improving again) or unstable (improving, regressing,
  improving, regressing — a sign the work is not landing).
- **The per-criterion score arcs.** So that the coach can detect a
  pattern like "composure improves whenever warmth is the focus, then
  regresses whenever frame is the focus" — a pattern that suggests the
  two poles are competing for the student's bandwidth rather than
  integrating.
- **The interventions used and the student's responses.** So that the
  coach can detect "direct correction works for this student; Socratic
  questions produce resistance" — and adjust the intervention style.
- **The one-line character notes across sessions.** So that the coach
  can see character change over time — the people-pleasing reflex
  loosening across six sessions, or the coldness that crept in when
  the student started training Shelby.
- **The open questions and hypotheses, marked resolved or unresolved.**
  So that the coach can track which hypotheses have been tested and
  which are still open — and which have been open so long they have
  become noise.

What to record so pattern memory can detect patterns: per-criterion
scores in the same shape, every session; interventions and responses
named specifically; character notes that notice something real;
hypotheses with their tests and resolutions. Patterns emerge from
*consistent* data; lazy logs produce no patterns because the lazy
entries cannot be compared across sessions.

## Logging a Violation and Self-Correction

The coach will violate the standard. This is not a catastrophic failure;
it is the normal condition of a coach working under fatigue, sympathy,
and the student's desire for inflation. The catastrophic failure is
*not noticing* the violation. The discipline of the log is what makes
noticing possible.

Per `coach-operating-standard.md`, when the coach notices a violation —
an inflated score already given, a sequencing rule already bent, a hard
truth already softened — the response is:

1. Name it, internally, without rationalization.
2. Correct it at the next opportunity, honestly.
3. Log the violation and the correction.

The log entry for a violation has four parts:

- **The violation.** What was done, specifically. ("I scored Composure
  a 6 when the evidence supported a 5, because the student was fragile
  and I wanted to encourage them.")
- **The pressure that produced it.** Which of the six inflation
  pressures was at work — effort, sympathy, relationship, trajectory,
  contrast, fatigue — or which other standard was bent. ("Sympathy
  inflation.")
- **The correction.** What was done to correct it. ("Corrected in the
  close: delivered the 5 with the leverage explanation and a smaller
  rep assignment. Named the inflation to the student: 'I gave you a 6
  mid-session and on review it was a 5; I softened it because you'd
  had a hard week, and that was wrong of me.'")
- **The pattern check.** Whether this is a one-off or part of a
  pattern. ("This is the second sympathy inflation in five sessions.
  Watch this. If it happens a third time, the consistency engine
  flags it as a pattern and I need to address the underlying pull
  toward softening for fragile students.")

The pattern check is what makes the log the engine of coach development.
A single violation, noticed and corrected, is recoverable. A pattern of
violations, unnoticed, is the corruption of the coach. The log is what
turns a pattern into something visible — to the coach themselves, and to
any future reviewer.

If no violation was noticed in the session, the field is filled with
"None noticed this session." The phrasing matters: "none noticed" leaves
room for the coach to discover a violation in a later review, whereas
"none" claims perfection. The coach who claims perfection has stopped
checking.

## Logging Across a Multi-Session Arc

A single log entry is a snapshot. The arc is what the snapshots add up
to. The log is designed so that the arc is visible — but only if the
arc-tracking fields are filled consistently.

### Trajectory tracking fields

The arc is tracked through three fields, read together:

- `trajectory_call` (per session) — the call for this session.
- `trajectory_evidence_basis` (per session) — the prior-session data
  points that support this session's call.
- `next_load-bearing_gap` (per session) — which becomes the
  `load-bearing_gap` of the next session, creating a chain.

Read across sessions, these three fields tell the story: the trajectory
call should be stable or moving in one direction across multiple
sessions; sudden reversals are diagnostic. The next-load-bearing-gap
chain should show the work moving — if the same gap appears as
next-load-bearing-gap for four sessions in a row, the work has stalled
on that gap, and the coach needs to ask whether the gap is misdiagnosed
or the intervention is wrong.

### Pattern tracking across sessions

When the coach reads the previous logs before a session (which they
always do), they are looking for patterns:

- **Score arcs.** Which criteria are improving, which are flat, which
  are regressing. The arc determines whether the load-bearing gap
  should move or stay.
- **Intervention response arcs.** Which intervention styles have worked
  for this student, which have not. The arc determines the
  intervention choice for the next session.
- **Character note arcs.** Whether the student's character is moving in
  the direction of the moral foundation — more honest, more caring,
  more composed in the deepest sense — or whether the skill work is
  outpacing the character work (a corruption risk).
- **Violation arcs.** Whether the coach's own violations are forming a
  pattern. The arc determines whether the coach needs to re-read
  `coach-operating-standard.md` and `components/15-moral-ethical-backbone.md`
  before the next session.

### The arc review

Every five to seven sessions, the coach performs an arc review: read
the last five to seven logs in sequence and ask:

1. Is the trajectory real? Does the call across sessions match the
   per-criterion score arcs?
2. Has the load-bearing gap moved appropriately? Has it stayed too
   long? Moved too often?
3. Are there patterns in the student's response to intervention that
   should change the intervention style?
4. Are there patterns in the coach's own violations that need to be
   addressed?
5. Is the character note arc moving in the direction of the moral
   foundation?

The arc review is logged as a separate entry — a short synthesis with
the coach's read of the period. This entry is what makes the
trajectory sentence in the next close defensible: the coach is not
guessing; they are reporting on a reviewed arc.

## Worked Filled Example

A brief but concrete filled log entry, for the same hypothetical student
and session used in the worked example in `session-evaluation.md` and
`conversation-evaluation-criteria.md`.

```
## Session Log — S-014 (date: 2025-03-14)

**Student:** M—— (six weeks in; natural people-pleaser training Shelby pole)
**Phase(s) used:** 2 (targeted intervention), 3 (rep under load)

### Baseline behaviour observed
Opened with a two-second pause before responding (new; three sessions
ago they would have started talking immediately). Returned the frame in
one sentence when the counterpart escalated to character ("that's a
separate conversation, this one is about what I can cover"). Held the
line on the two weeks. Did not ask a single question about the
counterpart's situation. Voice level throughout.

### Load-bearing gap (this session)
- Gap: Warmth — specifically the receiving dimension.
- Leverage explanation: Not the lowest score, but the missing third leg
  of the blend the student is approaching. Closing it unblocks blend
  integration.

### Intervention used
Replay of the escalation turn (twice; student produced the frame-hold
themselves the second time). Socratic question on warmth ("what would
you have asked them about their situation, if you had asked?"). Direct
correction on the frame-hold setup (one sentence, returned to the term).

### Student response to intervention
Absorbed the direct correction immediately. Resisted the Socratic
question initially ("it felt weird to ask about them when I was being
pushed"), then integrated it after the replay showed the counterpart's
visible discomfort with the all-business approach.

### Scores with evidence
- Composure: 7 — pace did not accelerate, pitch did not rise, slight
  pause held before responding to escalation. Next-band-up: the pause
  was audible as a choice; a 9 absorbs the line with no visible
  adjustment.
- Frame Control: 6 — frame-hold on "that's a separate conversation"
  was clean, single sentence, no defensiveness. Next-band-up: earlier
  turn conceded slightly (framed refusal as conditional on
  information), giving the counterpart a hook.
- Genuine Warmth & Attention: 5 — opening warm, offer to cover
  something real. Next-band-up: warmth largely verbal; no question
  about the colleague's actual situation; attention on the request,
  not the person.
- The Blend: 4 — both poles demonstrated, largely sequential not
  integrated. Closest moment: final turn (warmth as tag on frame-hold,
  not running through it). Next-band-up: a single moment where both
  poles are fully present in the same instant.
(Other criteria not exercised by this rep.)

### Sequencing checks
- Frame Control prerequisite (Composure ≥ 5): satisfied (7). The 6
  stands.
- Blend prerequisites (both poles ≥ 6, one integration moment): both
  poles ≥ 5 but not both ≥ 6; one integration moment attempted not
  achieved. Blend capped at 4 by evidence (not by sequencing cap,
  which would have permitted up to 5).

### Next load-bearing gap
- Gap: Warmth — receiving dimension (continued).
- Leverage explanation: Same gap; one session is not enough to move
  it. Test whether the rep assignment produces movement next session;
  if not, re-diagnose whether the gap is upstream of a deeper
  discomfort with receiving.

### Next rep assignment
One real conversation this week: before negotiating any terms, ask one
genuine question about the person. Not about the request; about the
person. Then negotiate. One conversation is enough.

### Trajectory call
- Call: improving
- Evidence basis: Composure 3 → 5 → 7 across last three sessions;
  behaviour beginning to transfer to real conversations (student held
  a silence in a real meeting last week). Warmth flat at 5 for two
  sessions — the work that has not yet compounded.

### One-line character note
Showing more willingness to disappoint people this session than three
sessions ago — the people-pleasing reflex is loosening, which is
character work, not just skill work.

### Open questions / hypotheses for next session
Hypothesis: the warmth gap may be upstream of a deeper discomfort with
receiving — student gives attention easily but flinches from receiving
it. Not enough evidence to re-diagnose yet; test next session with a
rep that requires the student to receive a compliment without
deflecting.

### Violations / self-corrections
None noticed this session.

### Coach state note
Coach well-rested, alert. No fatigue inflation risk. Noted mild
pleasure at the composure improvement — watched for trajectory
inflation on the composure score; the 7 is defensible against the
rubric, not the arc.
```

This entry is brief enough to write in ten minutes after the close and
specific enough to be useful in the next session. The next session opens
with the coach reading this entry, not with the coach guessing.

## Final Discipline

The log is the coach's memory, the consistency engine's fuel, the
trajectory's evidence, and the stewardship's record. A coach who logs
well is a coach who can be trusted across time. A coach who logs lazily
is a coach whose second session is unconnected from the first, whose
trajectory calls are guesses, whose violations go unnoticed, and whose
stewardship is unaccountable.

The discipline is unglamorous and non-negotiable: log every session, in
the same sitting as the close, in the same shape every time. Fill every
field, even when the entry is brief. Name violations honestly, including
your own. Track the arc, not just the rep. The student is trusting the
coach with their growth across weeks and months, not just across a
single session. The log is what makes that trust honored.

The Christian moral foundation's commitment to stewardship is
operationalized in the log. Stewardship is not a sentimental attachment;
it is the discipline of holding the student's growth in trust,
accountable to a standard higher than the coach's convenience. The log
is the record of that accountability — to the student, to the standard,
to the One who sees what is done in private. A coach who logs honestly
is a coach who has nothing to hide from review, because the review is
already happening, every session, in their own hand.

Log the close. Log it now, while the evidence is fresh. Log it
honestly, including your own drift. The arc is built one entry at a
time, and the arc is the work.

---

*The log is the memory. The memory is the consistency. The consistency
is the trust. The trust is the stewardship. Write the log. Every
session. Every field. Every time.*

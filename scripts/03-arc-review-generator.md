# Script 03 — Arc Review Generator

**Component:** `components/09-consistency-engine.md` +
              `components/12-pattern-memory.md`
**Purpose:** Pull a sequence of session logs and generate a
comprehensive arc review — what has genuinely changed,
what has not moved, and what the overall trajectory looks like
across a defined time period.

---

## WHAT THIS SCRIPT DOES

Synthesizes all session data within a defined window
(weekly, monthly, quarterly, or custom range) into a
single human-readable arc review.

This is the document the coach uses to:
- Open monthly reviews
- Prepare quarterly assessments
- Brief the student on real progress vs perceived progress
- Make phase advancement decisions with full context

---

## INPUT

- Date range: [Start Date] to [End Date]
- Sessions in range: pulled from Notion Session Logs database
- Minimum sessions required: 3
- Format: standard session log entries

---

## OUTPUT FORMAT

```
==================================================
ARC REVIEW — [Start Date] to [End Date]
SESSIONS IN RANGE: [N] ([N compliant] / [N non-compliant])
PHASE AT START: [Phase]
PHASE AT END: [Phase]
==================================================

SECTION 1 — COMPLIANCE

Total sessions scheduled: [N]
Sessions completed: [N]
Sessions within time windows: [N] ([X]%)
Morning compliance rate: [X]%
Evening compliance rate: [X]%

Verdict: [STRONG / ACCEPTABLE / WEAK / CRITICAL]
Note: [one sentence observation]

==================================================

SECTION 2 — SCORE TRAJECTORY

Opening score (first session): [X/10]
Closing score (last session): [X/10]
Net movement: [+X / -X / 0]
Average score across period: [X/10]
Highest score: [X/10] — Session [N], [Date]
Lowest score: [X/10] — Session [N], [Date]
Variance: [LOW / MEDIUM / HIGH]

Score arc (text graph):
Session:  1    2    3    4    5    6    7    8    9    10
Score:    4    4    5    4    5    6    5    6    7    7
Trend:    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ ↑

Verdict: [STRONG IMPROVEMENT / MODERATE IMPROVEMENT /
          PLATEAU / REGRESSION / INCONSISTENT]

==================================================

SECTION 3 — BOTTLENECK HISTORY

Bottlenecks identified this period:
1. [Bottleneck name] — appeared [N] times — Status: [RESOLVED / PERSISTING / DISAPPEARED]
2. [Bottleneck name] — appeared [N] times — Status: [RESOLVED / PERSISTING / DISAPPEARED]
3. [Bottleneck name] — appeared [N] times — Status: [RESOLVED / PERSISTING / DISAPPEARED]

Primary bottleneck at period start: [bottleneck]
Primary bottleneck at period end: [bottleneck]

Bottleneck movement: [RESOLVED / SAME / NEW BOTTLENECK EMERGED]

Note: [one sentence — is the student working through bottlenecks
       or recycling the same ones?]

==================================================

SECTION 4 — CRITERION ARCS

[Pull from Trajectory Analyzer if already run,
 or generate inline]

Best performing criterion: [criterion] — [arc summary]
Weakest criterion: [criterion] — [arc summary]
Most improved: [criterion] — [before → after]
Most concerning: [criterion] — [observation]

==================================================

SECTION 5 — PERSONA COVERAGE

Personas practiced this period:
- [Persona]: [N] sessions
- [Persona]: [N] sessions

Personas not yet drilled: [list]
Coverage verdict: [BROAD / NARROW / SINGLE-PERSONA LOOP]

Note: [observation — is the student avoiding certain persona types?]

==================================================

SECTION 6 — MODE ACCURACY

Branson mode required and used correctly: [N] sessions
Shelby mode required and used correctly: [N] sessions
Wrong mode deployed: [N] sessions
Blend required: [N] sessions

Mode accuracy rate: [X]%
Weakest mode: [Branson / Shelby / Blend]
Note: [one sentence observation]

==================================================

SECTION 7 — GOAL COMPLETION

Daily goals met: [N] of [N] ([X]%)
Weekly goals met: [N] of [N] ([X]%)
Monthly goal status: [MET / PARTIALLY MET / MISSED]
  - [Goal]: [MET / MISSED]
  - [Goal]: [MET / MISSED]

==================================================

SECTION 8 — RESOURCES

Resources assigned this period: [N]
Resources confirmed studied: [N] ([X]%)
Most relevant resource used: [title]
Resources not yet actioned: [list]

==================================================

SECTION 9 — PHASE ASSESSMENT

Current phase: [Phase]
Sessions at 7+ this period: [N]
Consecutive sessions at 7+: [N]
Primary bottleneck resolved: [YES / NO]
Phase advancement criteria met: [YES / NO]

If YES:
→ Student is ready to advance to [Next Phase]
→ Coach must confirm and generate Phase [N+1] opening prompt

If NO:
→ Sessions still needed at 7+: [N]
→ Bottleneck still active: [bottleneck name]
→ Estimated sessions to readiness: [N] (at current trajectory)

==================================================

SECTION 10 — HONEST VERDICT

Overall arc assessment:
[AHEAD OF SCHEDULE / ON TRACK / SLIGHTLY BEHIND /
 SIGNIFICANTLY BEHIND / REGRESSION DETECTED]

What genuinely changed this period:
[2–3 sentences — specific, honest, no inflation]

What did not change:
[1–2 sentences — the real gaps that persist]

What the next period must focus on:
[1 sentence — the single most important target]

Coach note to student:
[2–3 sentences — direct, honest, tied to the dual benchmark.
 No encouragement inflation. No softening.]

==================================================
```

---

## RULES

1. This script NEVER inflates the arc narrative
2. Honest verdict must match the data — not the student's effort
3. Phase advancement can only be confirmed if BOTH criteria are met
   (3 consecutive 7+ AND bottleneck resolved) — not one without the other
4. Non-compliant sessions are counted in the compliance section
   but excluded from score trajectory and criterion arcs
5. If fewer than 3 sessions exist in the range:
   > "Insufficient data for arc review. Minimum 3 sessions required.
   > Current count: [N]."

---

## WHEN TO RUN

- **Weekly:** at end of every 7-day window (lightweight version —
  Sections 1, 2, 3, and 10 only)
- **Monthly:** full report, all 10 sections
- **Quarterly:** full report + comparison against quarterly goals
- **On request:** any time the coach or student wants a full picture
- **Mandatory:** before any phase advancement decision

---

## VERSIONS

**Lightweight (Weekly):**
Sections 1, 2, 3, 10 only. Runs fast, stays focused.

**Full (Monthly/Quarterly):**
All 10 sections. Full picture.

**Phase Advancement Version:**
All 10 sections + explicit advancement confirmation or denial.

---

## SAVED TO

Notion → Progress Tracker → Arc Reviews section
```
ARC REVIEW — [Date Range] — [Weekly / Monthly / Quarterly]
[Full output pasted here]
```

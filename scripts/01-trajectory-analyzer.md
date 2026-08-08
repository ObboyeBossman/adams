# Script 01 — Trajectory Analyzer

**Component:** `components/12-pattern-memory.md`
**Purpose:** Surface per-criterion score arcs across sessions to answer:
"Is this specific skill actually improving, plateauing, or decaying?"

---

## WHAT THIS SCRIPT DOES

Reads a sequence of session logs from Notion and produces a
per-criterion trajectory report. It does NOT move scores, override
sequencing caps, or make advancement calls. It only surfaces patterns
so the coach can make better-informed decisions.

---

## INPUT FORMAT

The script reads session log entries in this format
(from `references/logging-template.md`):

```
DATE: [Date]
LOGGED AT: [HH:MM AM/PM]
PHASE: [Phase]
SCENARIO: [Scenario]
SCORE: [X/10]
COMPLIANCE: [COMPLIANT / NON-COMPLIANT]

1. ACOUSTIC & DELIVERY
   - Pitch Variation: [flat / moderate / dynamic] — [observation]
   - Pace: [rushed / balanced / slow] — [observation]
   - Filler Words: [count] — [examples]
   - Clarity: [score /10] — [observation]

2. VOCABULARY & EXPRESSION
   - Range: [limited / moderate / strong]

3. PRESENCE & FRAME
   - Frame Control: [score /10] — [observation]
   - Anchor Deployment: [attempted / successful / absent]
   - Mode Accuracy: [Branson / Shelby / blend] — [correct or incorrect]
   - Stamina: [score /10] — [observation]

4. OVERALL
   - Session Score: [X/10]
   - Primary Bottleneck: [one sentence]
   - Readiness for Next Phase: [YES / NOT YET]
```

**Minimum sessions required:** 5
**Recommended:** 10+

---

## OUTPUT FORMAT

```
==================================================
TRAJECTORY REPORT — [Date Range]
SESSIONS ANALYZED: [N]
PHASE: [Current Phase]
==================================================

CRITERION ARCS:

1. Overall Score
   Sessions: [4, 4, 5, 5, 6] → Trend: ↑ IMPROVING
   Average: [4.8/10]
   Variance: [LOW / MEDIUM / HIGH]
   Note: [observation]

2. Frame Control
   Sessions: [3, 4, 4, 5, 6] → Trend: ↑ IMPROVING
   Note: [observation]

3. Anchor Deployment
   Sessions: [absent, absent, attempted, attempted, successful]
   Trend: ↑ IMPROVING
   Note: [observation]

4. Filler Words
   Sessions: [8, 6, 5, 5, 3] → Trend: ↑ IMPROVING
   Note: [observation]

5. Clarity
   Sessions: [5, 5, 6, 5, 6] → Trend: → PLATEAUING
   Note: [observation — plateau detected, increase drill pressure]

6. Pace Control
   Sessions: [rushed, rushed, balanced, rushed, balanced]
   Trend: → INCONSISTENT
   Note: [observation]

7. Pitch Variation
   Sessions: [flat, flat, flat, moderate, flat]
   Trend: → INCONSISTENT
   Note: [observation]

8. Stamina
   Sessions: [4, 5, 5, 6, 6] → Trend: ↑ IMPROVING
   Note: [observation]

9. Mode Accuracy
   Sessions: [incorrect, incorrect, correct, incorrect, correct]
   Trend: → INCONSISTENT
   Note: [observation]

10. Vocabulary Range
    Sessions: [limited, limited, moderate, limited, moderate]
    Trend: → INCONSISTENT
    Note: [observation]

==================================================
SUMMARY FLAGS:

✅ IMPROVING:   [list criteria showing consistent upward arc]
⚠️  PLATEAUING: [list criteria showing no movement across 3+ sessions]
❌ DECAYING:    [list criteria showing downward movement]
🔄 INCONSISTENT: [list criteria with no clear pattern]

PRIMARY CONCERN: [the one criterion with the weakest arc]
COACH ACTION: [one specific intervention tied to primary concern]
==================================================
```

---

## TREND DEFINITIONS

| Label | Condition |
|-------|-----------|
| ↑ IMPROVING | Consistent upward movement across 3+ consecutive sessions |
| ↓ DECAYING | Consistent downward movement across 3+ sessions |
| → PLATEAUING | No meaningful change across 3+ consecutive sessions |
| 🔄 INCONSISTENT | No clear pattern — up and down without direction |

---

## RULES

1. This script NEVER moves a score retroactively
2. This script NEVER overrides a phase sequencing decision
3. This script NEVER calls a student "ready to advance"
4. It flags patterns only — the coach makes all decisions
5. NON-COMPLIANT sessions are included in the arc but flagged separately
6. Minimum 5 sessions required — output an error if fewer exist:
   > "Insufficient data. Trajectory analysis requires minimum 5 sessions.
   > Current count: [N]. Run again after [5-N] more sessions."

---

## WHEN TO RUN

- Automatically: at end of every 5th session
- On request: any time the coach or student wants a pattern check
- Mandatory: before any phase advancement decision

---

## SAVED TO

Notion → Progress Tracker → Trajectory Reports section
```
TRAJECTORY REPORT — [Date]
[Full output pasted here]
```

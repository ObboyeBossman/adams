# Script 02 — Inflation Drift Detector

**Component:** `components/09-consistency-engine.md`
**Purpose:** Detect if session scores are creeping upward without
corresponding resolution of the primary bottleneck — the most
common failure mode in long-term coaching programs.

---

## WHAT THIS SCRIPT DOES

Compares score trajectory against bottleneck resolution status.
If scores are rising but the same bottleneck keeps appearing,
the coach is inflating — consciously or not.

This script flags that pattern immediately and forces a recalibration.

It does NOT move scores. It does NOT override decisions.
It surfaces the drift so the coach can correct it.

---

## THE CORE PROBLEM IT SOLVES

Inflation drift happens when:
- Session 1: Score 4/10 | Bottleneck: Anchor deployment absent
- Session 3: Score 5/10 | Bottleneck: Anchor deployment absent
- Session 5: Score 6/10 | Bottleneck: Anchor deployment absent
- Session 7: Score 7/10 | Bottleneck: Anchor deployment absent

The score has risen 3 points but the bottleneck has not changed.
This means the score increase is not real — it is drift.
The coach has been rewarding effort, familiarity, or comfort
rather than actual skill acquisition.

---

## INPUT FORMAT

Reads from session logs:
```
SCORE: [X/10]
PRIMARY BOTTLENECK: [one sentence]
COMPLIANCE: [COMPLIANT / NON-COMPLIANT]
```

**Minimum sessions required:** 10
**Recommended:** 15+

---

## DETECTION ALGORITHM

**Step 1 — Extract bottleneck strings**
Pull the PRIMARY BOTTLENECK field from each session log.
Group sessions where the bottleneck is substantively the same
(same skill gap, even if worded differently).

**Step 2 — Compare score movement within bottleneck group**
If the same bottleneck appears across 3+ consecutive sessions
AND the score has increased by 1.5+ points across those sessions
AND no explicit bottleneck resolution has been logged
→ FLAG AS INFLATION DRIFT

**Step 3 — Check for false resolution**
A bottleneck is only resolved when:
- The coach explicitly logs: "BOTTLENECK RESOLVED: [skill]"
- AND the following session shows a different primary bottleneck
- AND the score at resolution was 7/10 or above

If a bottleneck disappears from logs without a resolution entry
→ FLAG AS UNRESOLVED DISAPPEARANCE (possible avoidance)

---

## OUTPUT FORMAT

```
==================================================
INFLATION DRIFT REPORT — [Date]
SESSIONS ANALYZED: [N]
PHASE: [Current Phase]
==================================================

DRIFT SCAN RESULTS:

BOTTLENECK: "Anchor deployment absent"
Appeared in sessions: 1, 2, 3, 4, 5, 6, 7
Score at first appearance: 4/10
Score at last appearance: 7/10
Score increase: +3.0 points
Resolution logged: NO

⚠️  INFLATION DRIFT DETECTED

The score has increased 3.0 points while the same bottleneck
persists unresolved across 7 sessions. This score movement
does not reflect genuine skill acquisition.

REQUIRED ACTION:
- Reset score calibration for this criterion
- Do not advance phase until bottleneck is explicitly resolved
- Next session must target this bottleneck directly with
  increased pressure — not a new scenario

==================================================
UNRESOLVED DISAPPEARANCES:

BOTTLENECK: "Filler word overuse"
Last appeared: Session 4
Disappeared without resolution entry after Session 4
Status: ⚠️  UNRESOLVED DISAPPEARANCE

This bottleneck was not resolved — it was dropped.
It may resurface under pressure. Monitor in next 3 sessions.

==================================================
CLEAN RESOLUTIONS:

BOTTLENECK: "Exit fold without anchor"
Resolved: Session 8 | Score at resolution: 7/10
Confirmed: New bottleneck appeared in Session 9 ✅

==================================================
VERDICT:

DRIFT STATUS: ⚠️  DRIFT DETECTED
CLEAN RESOLUTIONS: [N]
UNRESOLVED DISAPPEARANCES: [N]
ADVANCEMENT BLOCKED: [YES / NO]

Coach recalibration required before next session.
==================================================
```

---

## RULES

1. This script NEVER moves a score
2. This script NEVER blocks advancement on its own —
   it flags the issue; the coach enforces the block
3. A single inflated session does not trigger the flag —
   the pattern must span 3+ sessions
4. NON-COMPLIANT sessions are excluded from drift calculation
   (compliance issues are logged separately)
5. If no drift is detected, output a clean confirmation:
   > "No inflation drift detected across [N] sessions.
   > Score movement aligns with bottleneck resolution history."

---

## WHEN TO RUN

- Automatically: every 10 sessions
- Mandatory: before any phase advancement decision
- On request: any time the coach wants a calibration check

---

## SAVED TO

Notion → Progress Tracker → Inflation Drift Reports section
```
DRIFT REPORT — [Date]
[Full output pasted here]
```

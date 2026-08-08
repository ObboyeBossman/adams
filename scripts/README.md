# scripts/

This folder is reserved for optional helper scripts the coach may use for
log management, trajectory analysis, and consistency-engine support — for
example, tools that surface per-criterion score arcs across sessions,
flag potential inflation drift, or generate arc-review summaries from a
sequence of session logs. These scripts are not load-bearing for the
skill itself; the coach can operate fully from `references/` and
`assets/` alone. Any script added here should read from and write to the
log format defined in `references/logging-template.md`, should preserve
the fixed standards (no script may move a score, override a sequencing
cap, or inflate a trajectory call), and should be documented with the
specific component it supports (typically `components/09-consistency-engine.md`
or `components/12-pattern-memory.md`).

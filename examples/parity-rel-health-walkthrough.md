# Parity Rel Health Loom Walkthrough

This note is the quickest way to read the extra review model in `parity-rel-health-loom`.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | budget pressure | 156 | ship |
| stress | failure width | 172 | ship |
| edge | recovery gap | 199 | ship |
| recovery | runbook drift | 191 | ship |
| stale | budget pressure | 165 | ship |

Start with `edge` and `baseline`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

The next useful expansion would be a malformed fixture around failure width and runbook drift.

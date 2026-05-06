# parity-rel-health-loom

`parity-rel-health-loom` is a Solidity project in reliability. Its focus is to develop a Solidity command-oriented project for health scenarios with append-only fixtures, checkpoint recovery checks, and no credentials or hosted services.

## Why This Exists

This is intentionally local and self-contained so it can be inspected without credentials, services, or seeded history.

## Parity Rel Health Loom Review Notes

`edge` and `baseline` are the cases worth reading first. They show the optimistic and cautious ends of the fixture.

## Capabilities

- `fixtures/domain_review.csv` adds cases for budget pressure and failure width.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/parity-rel-health-walkthrough.md` walks through the case spread.
- The Solidity code includes a review path for `recovery gap` and `budget pressure`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Implementation Shape

The core code exposes a scoring path and the added review layer uses `signal`, `slack`, `drag`, and `confidence`. The domain terms are `budget pressure`, `failure width`, `recovery gap`, and `runbook drift`.

The Solidity checks add a pure review lens and Foundry coverage.

## Local Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Verification

The check exercises the source code and the review fixture. `edge` is the high score at 199; `baseline` is the low score at 156.

## Roadmap

This remains a local project with deterministic fixtures. It does not depend on credentials, hosted services, or live data. Future work should add richer malformed inputs before widening the public API.

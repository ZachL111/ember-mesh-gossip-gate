# ember-mesh-gossip-gate

`ember-mesh-gossip-gate` explores distributed systems with a small SQL codebase and local fixtures. The technical goal is to implement an SQL distributed systems project for gossip protocol validation, using framed sample traffic and bounds and ordering tests.

## Project Rationale

I want this repository to be useful as a quick reading exercise: fixtures first, implementation second, verifier last.

## Ember Mesh Gossip Gate Review Notes

Start with `quorum health` and `quorum health`. Those cases create the widest score spread in this repo, so they are the best quick check when the model changes.

## Feature Set

- `fixtures/domain_review.csv` adds cases for quorum health and lease drift.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/ember-mesh-gossip-walkthrough.md` walks through the case spread.
- The SQL code includes a review path for `quorum health` and `quorum health`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Architecture

The fixture data drives the tests. The code stays thin, while `metadata/domain-review.json` and `config/review-profile.json` explain what each case is meant to protect.

The SQL checks add a separate view over the domain review fixture.

## Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Test Command

That command is also the regression path. It verifies the domain cases and catches mismatches between the CSV, metadata, and code.

## Next Improvements

No external service is required. A deeper version would add more negative cases and a clearer boundary around invalid input.

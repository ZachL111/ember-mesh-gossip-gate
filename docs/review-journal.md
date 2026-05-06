# Review Journal

The cases below are the review handles I would use before changing the implementation.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its distributed systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `quorum health`, score 117, lane `watch`
- `stress`: `lease drift`, score 192, lane `ship`
- `edge`: `replica lag`, score 178, lane `ship`
- `recovery`: `membership churn`, score 206, lane `ship`
- `stale`: `quorum health`, score 223, lane `ship`

## Note

The repository should be understandable without pretending it is larger than it is.

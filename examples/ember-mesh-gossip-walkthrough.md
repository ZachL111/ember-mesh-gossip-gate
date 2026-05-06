# Ember Mesh Gossip Gate Walkthrough

This note is the quickest way to read the extra review model in `ember-mesh-gossip-gate`.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | quorum health | 117 | watch |
| stress | lease drift | 192 | ship |
| edge | replica lag | 178 | ship |
| recovery | membership churn | 206 | ship |
| stale | quorum health | 223 | ship |

Start with `stale` and `baseline`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

The useful comparison is `quorum health` against `quorum health`, not the raw score alone.

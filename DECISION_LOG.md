# Decision log

## 2026-08-30 — Separate immutable WebMCP competition surface

**Decision:** Publish the WebMCP Challenge entry from this separate public
repository and the `webmcp.utlovat.se` subdomain, rather than from the
continuing `utlovat.se` deployment.

**Why:** The competition cutoff freezes the project, video, repository and
team. Utlovat.se remains a live election-information service and must be able
to receive ordinary editorial and technical changes. A static build captures
the WebMCP page, its client scripts, public API data and evidence pages in one
origin; freezing only `/webmcp/` would leave its root-addressed resources able
to change underneath it.

**Scope:** This repository is public because the competition requires a public
open-source code repository. It keeps Apache-2.0, the license used by
`bambapappa/valflask`. It includes no private review material or credentials.

**Finalization rule:** The rehearsal is replaced once with a build from one
named `valflask` commit before the stated challenge cutoff. `SNAPSHOT.json`
must record that commit, data hash and output hashes. No change is made to this
repository, its deployment, its video or its team after that point.

## 2026-08-31 — Final competition freeze

**Decision:** Freeze this repository and `webmcp.utlovat.se` as the final
competition surface from source commit
`6d77945637089022df79fab731e0b6f16a270010`. The final manifest records the
published data hash and key static-output checksums.

**Why:** The live HTTPS surface and all four documented judge flows were
tested. They showed source-traced evidence, visible uncertainty, human-review
status, and the refusal to turn parliamentary actions into a kept/broken
verdict without sufficient evidence. The promise-page test instruction was
corrected to use the canonical id-and-slug URL.

**Rejected alternatives:** Continue using the mutable `utlovat.se` deployment
for judging, or leave a broken direct promise link in the test instructions.
The former conflicts with the competition freeze while the latter needlessly
produces a 404 for a documented test.

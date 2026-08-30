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

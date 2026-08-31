# Utlovat.se — WebMCP Challenge snapshot

This repository is the final frozen competition snapshot of Utlovat.se's
WebMCP demonstration. It is separate from the live election-information project at
[`bambapappa/valflask`](https://github.com/bambapappa/valflask), which
continues to receive ordinary editorial and technical updates.

The intended judge URL is `https://webmcp.utlovat.se/webmcp/`.

## Judge testing

No account, credential, or payment is required. The WebMCP tools and their
instructions are in English; the published source material, quotes, and some
evidence-board labels remain Swedish by design.

Open `https://webmcp.utlovat.se/webmcp/` in a WebMCP-capable browser and try
these neutral prompts:

1. `Use build_research_brief to compare M and S on sjukvård. Show quotes, dates, source links, archive copies when available, unclear positions, and gaps. Do not recommend a party.`
2. `Build a research brief on skola for M, S and V. Then use get_evidence_board_status and state whether a human has marked the visible evidence board as read. Do not treat an unread board as a judgement about any party.`
3. `Use trace_promise for p-2026-0360. Show the original source, archive copy when available, and reviewed Riksdag actions. Do not decide whether the promise was kept or broken.`
4. Open [`p-2026-0360`](https://webmcp.utlovat.se/lofte/p-2026-0360/infor-en-elevlag-for-ratt-till-stod-utan-diagnoskrav/) and ask: `Trace this open promise to its original source and reviewed Riksdag actions. Show the evidence chain only; do not decide whether it was kept or broken.`

The five global tools are available on the challenge page. Contextual tools
appear when a supported promise or question page is open. A research brief is
intentionally marked `unverified` until a person has read and acknowledged
the visible evidence; this is a reading-status gate, not a judgement about a
party.

## What people and agents do together

The person asks a neutral question about Swedish election commitments. A
WebMCP-capable browser lets the agent retrieve only Utlovat.se's published
evidence: exact quotes, dates, source links, archive copies when available,
recorded unclear positions and the limits of the selected search. The same
evidence appears in the visible research brief so the person can inspect it.

The tools do not recommend a party, rank parties, infer a user's political
preferences or treat an empty bounded result as proof that a party lacks a
policy.

## Snapshot layout

- `docs/` is the complete public static site published by GitHub Pages:
  WebMCP, the Swedish promise and question views, comparison views, and
  Handlingsvågen under `/handlingsvagen/`. Internal Utlovat.se links stay on
  this frozen subdomain. `.nojekyll` preserves the generated `_astro/` assets.
- `source/` is an archive of the exact Utlovat.se source revision used for
  this build. It excludes Git history and installed dependencies.
- `SNAPSHOT.json` records the final source revision, data hash and checksums.
- `DECISION_LOG.md` records the scope boundary between the competition snapshot
  and the continuing election-information service.
- `SESSION_HANDOFF.md` records the remaining release steps and their evidence.

This final snapshot is built from one named `valflask` revision. The public
repository and deployment remain unchanged through judging.

## License

Apache-2.0. See [LICENSE](LICENSE).

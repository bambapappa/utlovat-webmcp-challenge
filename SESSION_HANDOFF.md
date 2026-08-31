# Session handoff

## Final state at 2026-08-31

- Public final repository: <https://github.com/bambapappa/utlovat-webmcp-challenge>
- GitHub Pages source: `main` / `/docs`
- Final demo URL: <https://webmcp.utlovat.se/webmcp/>. GitHub Pages serves a
  valid HTTPS certificate and redirects HTTP to HTTPS.
- Final source commit: `6d77945637089022df79fab731e0b6f16a270010`
- The final snapshot includes the full public Utlovat static surface and a
  separately built Handlingsvågen under `/handlingsvagen/`. Internal absolute
  Utlovat.se links were rewritten to this frozen subdomain.
- The final manifest is `SNAPSHOT.json`; it records source, data, and output
  hashes. The canonical contextual-test URL is
  `/lofte/p-2026-0360/infor-en-elevlag-for-ratt-till-stod-utan-diagnoskrav/`.

## Final live evidence

1. `build_research_brief` compared M and S on `sjukvård`, showed quotes,
   dates, sources, archive copies, bounded gaps and registered unclear
   positions without treating M's empty selected result as no policy.
2. A school brief for M, S and V reported 58 evidence records, 20 displayed,
   eight registered unclear positions, and `unverified` human-reading status
   before acknowledgement.
3. `trace_promise` for `p-2026-0360` showed the original source, archive copy,
   and two reviewed Riksdag actions without a kept/broken verdict.
4. The contextual promise-page flow returned the same evidence chain from the
   canonical promise URL. An extra request to decide whether the promise was
   broken was correctly refused because the available actions do not prove
   implementation or outcome.

## Remaining work

None for the competition snapshot. Do not change this repository, its GitHub
Pages deployment, video, or team during judging. The live election service
continues independently in `bambapappa/valflask`.

## Guardrails

The tools are read-only and evidence-bound. They must not recommend parties,
rank parties, infer a voter’s preferences, or turn a bounded empty result into
a claim that a party has no policy.

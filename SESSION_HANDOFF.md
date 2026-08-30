# Session handoff

## State at 2026-08-30

- Public rehearsal repository: <https://github.com/bambapappa/utlovat-webmcp-challenge>
- Rehearsal commit containing the static evidence surface: `63e2d6b`
- GitHub Pages source: `main` / `/docs`
- Requested custom domain: `webmcp.utlovat.se`
- Rehearsal source commit: `6d77945637089022df79fab731e0b6f16a270010`
- `scripts/test-webmcp.mts` and `scripts/test-webmcp-retest.mts` passed against
  that source build.
- Local static server check returned 200 for `/webmcp/`, `/webmcp.js` and
  `/api/v1/promises.json`.

## Remaining work

1. Add the `webmcp` DNS CNAME to GitHub Pages and wait for GitHub to validate
   the domain and issue HTTPS.
2. Test the custom-domain URL in a fresh browser context, including an evidence
   link and a normal free-form WebMCP query.
3. Before the cutoff, select one final `valflask` commit, rebuild the static
   surface from it, update `source/` and `SNAPSHOT.json`, and run the same
   verification.
4. Point the Devpost repository and live-demo links at this snapshot before
   the cutoff, then make no further changes to competition materials.

## Guardrails

The tools are read-only and evidence-bound. They must not recommend parties,
rank parties, infer a voter’s preferences, or turn a bounded empty result into
a claim that a party has no policy.

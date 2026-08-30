# Session handoff

## State at 2026-08-30

- Public rehearsal repository: <https://github.com/bambapappa/utlovat-webmcp-challenge>
- Rehearsal commit containing the static evidence surface: `63e2d6b`
- GitHub Pages source: `main` / `/docs`
- Requested custom domain: `webmcp.utlovat.se`; its public CNAME resolves to
  `bambapappa.github.io`. GitHub Pages returns HTTP 200 for both `/` and
  `/webmcp/`; the root page immediately routes visitors to `/webmcp/`.
  GitHub's TLS certificate was still being issued at the most recent check, so
  HTTPS must be rechecked before the address is used as the final live-demo URL.
- Rehearsal source commit: `6d77945637089022df79fab731e0b6f16a270010`
- `scripts/test-webmcp.mts` and `scripts/test-webmcp-retest.mts` passed against
  that source build.
- Local static server check returned 200 for `/webmcp/`, `/webmcp.js` and
  `/api/v1/promises.json`.

## Remaining work

1. Wait for GitHub to issue the TLS certificate, enforce HTTPS, and test the
   custom-domain URL in a fresh browser context, including an evidence
   link and a normal free-form WebMCP query.
2. Before the cutoff, select one final `valflask` commit, rebuild the static
   surface from it, update `source/` and `SNAPSHOT.json`, and run the same
   verification.
3. Point the Devpost repository and live-demo links at this snapshot before
   the cutoff, then make no further changes to competition materials.

## Guardrails

The tools are read-only and evidence-bound. They must not recommend parties,
rank parties, infer a voter’s preferences, or turn a bounded empty result into
a claim that a party has no policy.

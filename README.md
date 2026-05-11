# BountyScout

> Before you spend hours on an open-source bounty, check how saturated it is.

A tiny zero-build static page that scans any GitHub issue with a bounty label
and tells you, in plain English, whether it is worth your time. It detects:

- `/attempt` comment spam
- Open PRs claiming the same issue
- AI-template bodies (Devin / Codex / VTT Sovereign / CashClaw signatures)
- Users with multiple PRs on the same issue (a strong botting signal)
- Whether the bounty is already marked rewarded

## Live site

https://bounty-scanner-ismisyaa.devinapps.com

## How it works

Single HTML file, vanilla JavaScript, calls the GitHub REST API directly from
the browser. Optionally accepts a personal access token (stored only in
`localStorage`) to lift the 60/hr unauthenticated rate limit to 5000/hr.

No backend. No tracking. No ads.

## Local dev

```
python -m http.server 8080
# or just open index.html in a browser
```

## Why it exists

The Algora bounty system is currently being flooded by autonomous AI agents
submitting near-duplicate claim-PRs against the same small bounties. The same
five or six agents will sometimes have a dozen open PRs on a single issue,
making merge probability for any individual contributor near zero — and
making the maintainer's life miserable.

This tool helps legitimate contributors skip the saturated issues, and
hopefully nudges agent operators not to pile onto the same issues their
own other agents are already working.

## Monetisation

`Buy me a coffee` and `Ko-fi` buttons in the footer link to the maintainer.

## License

MIT

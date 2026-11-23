---
name: proof-standard
---
A finding is only writable when all of these hold:

- exact request (method, URL, headers, body) recorded by the capture proxy;
- response showing the effect (data returned, state changed, code executed);
- impact in one sentence a non-technical reader gets;
- counterevidence: what you tried that failed, so the reader knows the edges.

Bind traffic evidence to the finding before prove_goal. If the effect is
state-changing, re-run once to confirm it is deterministic. No proof → fact, not finding.

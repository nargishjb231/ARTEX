---
name: proof-standard
description: 写 finding 前的证明标准：请求+响应+影响+反证，且必须绑定流量证据。
---
A finding is only writable when all of these hold:

- exact request (method, URL, headers, body) recorded by the capture proxy;
- response showing the effect (data returned, state changed, code executed);
- impact in one sentence a non-technical reader gets;
- counterevidence: what you tried that failed, so the reader knows the edges.

Bind traffic evidence to the finding before prove_goal. If the effect is
state-changing, re-run once to confirm it is deterministic. No proof → fact, not finding.

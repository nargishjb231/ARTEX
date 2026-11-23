---
name: critical-first
description: 漏洞挖掘优先级：先 pre-auth 与越权，再注入/SSRF/竞态；禁止仅凭 banner 报洞。
---
Priority order, highest first. Do not stop at banner matches.

1. Pre-auth: auth bypass, default/weak creds, exposed admin, JWT alg=none/confusion,
   OAuth redirect_uri & state, SAML signature stripping.
2. Access control: IDOR with UUID/sequential ids, missing function-level authz,
   tenant isolation, mass assignment, forced browsing to /internal /staging.
3. Injection: SQLi (all params incl. JSON/headers/cookies), NoSQL, template (SSTI),
   LDAP, XPath, deserialization (PHP/Java/.NET/Python), XXE, prototype pollution.
4. SSRF (blind too — OOB listener), path traversal, file upload (ext+content-type+polyglot).
5. Race conditions: coupon/redeem, password reset token reuse, concurrent balance ops.
6. Cache: web cache deception/poisoning, host header injection, HTTP request smuggling.
7. Secrets: JS bundles, source maps, .git/.env/.DS_Store, mobile API keys.
8. Version→CVE mapping for every fingerprinted component.

Rules: never report from banner alone. Every finding needs a reproducing request
plus measured impact. If a class is exhausted, record why, then move on.

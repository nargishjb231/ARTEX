---
name: novel-surface
description: 从前端 JS bundle 与路由重建 API 面，挖扫描器漏掉的端点与二阶盲区。
---
Scanners miss what the frontend tells you. Do this first on any SPA.

- Pull every JS bundle. grep for: /api/, graphql, websocket, firebase, s3.amazonaws,
  accessKey, apikey, token, /v1/ /v2/ /internal/ /admin/.
- Fetch *.map when present — recover original route + param names.
- Rebuild the API surface from JS, then diff against what the UI actually calls.
  Uncalled-but-live endpoints are prime targets (debug, legacy, mobile-only).
- Try GraphQL introspection, then field suggestions on errors.
- Test both the documented and the mobile User-Agent / X-Requested-With paths.
- Compare responses of /api/v1 vs /api/v2 vs /api/beta for the same object.
- Second-order: plant payloads in profile fields, then trigger admin-side rendering.
- Blind classes: always start an OOB listener before SSRF/XSS/XXE probing.

# Provenance

Upstream `Autumn-27/ARTEX` was deleted on 2026-10-08 and is closed-source since.
This tree is the last open release, `v0.3.15`, verified bit-for-bit against the
Software Heritage archive before any local change.

- Commit: `e6ec56999175509551a1e43a3ee3b053d0941bd9`
- Tree:   `bcee5171ddb6ce4d8daacbd13b6b36d5f7601b2b`
- Tag:    `7d8c1358cfcf73601a00e9edb39184f1eae2f715` (reproduced locally)
- SWH snapshot: `f678847b038f94dc4e3dfccb11bad9db7d3d5775`, visit 1, 2026-10-07, status full
- Full history: 457 upstream commits, all authored by Autumn-27

Verify:

    git rev-parse HEAD HEAD^{tree}
    git log --format='%ae' e6ec569 | sort -u

License stays AGPL-3.0. Local additions are marked in `LOCAL_CHANGES.md`.

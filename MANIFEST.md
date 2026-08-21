# Manifest — which asset each published post references

**This file exists because deleting a superseded asset broke a live post on 2026-08-21.**

A published post keeps resolving its source URL. The platform returning an asset ID is **not** proof it
took its own copy. So an asset referenced by a live post is **permanent** — this repository is
**append-only for anything published**.

**Before removing any folder, check this table. If a post references it, it stays.**

| Asset version | Referenced by | Post ID | Status |
|---|---|---|---|
| `2026-08-20_one-record-two-deadlines_v1.0.0` | 1:1 carousel, sent 2026-08-21 07:28 | `6a87ef44dc319146a2753ee6` | Post deleted in LinkedIn by owner. **Asset retained** — deletion is not verifiable from the API |
| `2026-08-20_one-record-two-deadlines_v1.1.0` | 4:5 carousel, sent 2026-08-21 07:56 | `6a88048b1b38003a90c65637` | Post deleted in LinkedIn by owner 2026-08-21. **Asset retained** |
| `2026-08-20_one-record-two-deadlines_v2.1.0` | 16:9, type undersized | `6a889348dc319146a281a7ad` | Post deleted by owner. **Asset retained** |
| `2026-08-20_one-record-two-deadlines_v2.2.0` | **16:9, type calibrated to canvas**, sent 2026-08-21 19:11 | `6a88a2e13869cf665895a040` | ✅ **LIVE — do not remove** |

⚠️ **The publishing API cannot see a deletion made in the network's own UI.** A post may show `sent` here
and no longer exist there. When in doubt, **keep the asset** — storage is free, a broken embed is not.

⚠️ **`raw.githubusercontent.com` caches 404s for several minutes.** After restoring a file the plain URL
keeps returning 404 while `?cb=<random>` returns 200. **Always cache-bust when verifying a restore**, or
you will conclude a working fix has failed.

## Retiring an asset

1. Confirm no row above marks it LIVE.
2. Confirm the referencing post is genuinely gone — check the network, not the API.
3. Remove it, and update this table in the same commit.

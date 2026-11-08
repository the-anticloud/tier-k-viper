# Ledger Status

**Project:** `K_VIPER`  
**Tier:** TIER_6_SECURITY_EVAL  
**Identity:** Upstream `bettercap/bettercap` @ `8eca2820f3c4` (GPL-3.0)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `bettercap/bettercap` |
| Commit | `8eca2820f3c41d2004434ed5a291d87462caeeb7` |
| Upstream licence | GPL-3.0 |
| Licence class | copyleft |
| Clone size | 43.13 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1500.0 IIU |
| Verified upstream edits | 1 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.

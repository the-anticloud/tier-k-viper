# Upstream Edits

**Project:** `K_VIPER`  
**Tier:** TIER_6_SECURITY_EVAL  
**Identity:** Upstream `bettercap/bettercap` @ `8eca2820f3c4` (GPL-3.0)

## Applied patches

| Patch | Target | Kind | Behaviour change | Test |
| --- | --- | --- | --- | --- |
| `K_VIPER-egress-001` | `UPSTREAM/_anticloud_egress.py` | behaviour | with ANTICLOUD_OFFLINE=1, any socket connection to a hosted frontier API raises EgressDenied instead of dialling out | `tests/upstream/test_egress_guard.py::test_frontier_host_denied_when_offline` |

Each patch is judged on behaviour, not on volume. A patch that only
writes to the ledger is not counted; `anticloud audit-edits` excludes it
and the project is reported as unimproved rather than as improved.

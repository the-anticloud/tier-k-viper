# Developer Cookbook — K_VIPER
**Stack:** Python 3.11, PAX 27B (exploit analysis), CVE database, AIOSS_FORMAT
**Domain:** VIPER: vulnerability intelligence and proof-of-concept evaluation for Anticloud

## CVE triage for Anticloud
```python
from k_viper import VIPEREvaluator

evaluator = VIPEREvaluator(
    pax_model="./pax-27b-q4.gguf",
    cve_db="./nvd_local.db",
    anticloud_deps="./anticloud_dependencies.json",
    aioss_chain="./viper.aioss"
)

result = evaluator.triage_cve("CVE-2024-12345")
print(f"Affected: {result.anticloud_affected}")
print(f"CVSS: {result.cvss_score}, Anticloud impact: {result.anticloud_impact}")
print(f"Remediation: {result.remediation}")
print(f"Chain: {result.chain_hash}")
```

## Batch CVE sweep
```python
new_cves = evaluator.sweep_new_cves(last_n_days=7)
critical = [c for c in new_cves if c.anticloud_impact == "critical"]
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```

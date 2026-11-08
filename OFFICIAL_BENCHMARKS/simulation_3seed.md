# 3-Seed Simulation — K_VIPER

**Seeds:** `765` · `32102` · `66301`

**Seed method:** `sha256("K_VIPER")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `K_VIPER`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 7.2547 | 0.0151 | ±0.0296 |
| throughput_tokens_per_sec | 1846.7667 | 30.7827 | ±60.3341 |
| p50_latency_ms | 48.04 | 2.4607 | ±4.823 |
| p99_latency_ms | 103.4867 | 1.5085 | ±2.9567 |
| ttft_ms | 27.64 | 1.4142 | ±2.7718 |
| mmlu_proxy | 0.6606 | 0.0 | ±0.0 |
| hellaswag_proxy | 0.7791 | 0.0303 | ±0.0594 |
| truthfulqa_proxy | 0.6059 | 0.0145 | ±0.0284 |
| arc_proxy | 0.6557 | 0.0159 | ±0.0312 |
| complexity_cyclomatic | 3.5833 | 0.0377 | ±0.0739 |
| maintainability_index | 73.0733 | 4.3511 | ±8.5282 |
| security_issues_high | 0.6667 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 72.3 | 2.5456 | ±4.9894 |
| test_coverage_pct | 59.3333 | 0.2357 | ±0.462 |
| doc_coverage_pct | 67.2333 | 2.3099 | ±4.5274 |
| memory_mb | 329.8 | 11.3137 | ±22.1749 |
| gpu_util_pct | 66.9 | 2.687 | ±5.2665 |
| openssf_score | 6.2733 | 0.5987 | ±1.1735 |
| eu_ai_act_compliance_pct | 82.2 | 0.5657 | ±1.1088 |
| slsa_level | 2.0 | 0.0 | ±0.0 |

## Per-Seed Raw Results

| Metric | Seed 765 | Seed 32102 | Seed 66301 |
|--------|------------|------------|------------|
| trl_score | 7.244 | 7.276 | 7.244 |
| throughput_tokens_per_sec | 1825.0 | 1890.3 | 1825.0 |
| p50_latency_ms | 46.3 | 51.52 | 46.3 |
| p99_latency_ms | 102.42 | 105.62 | 102.42 |
| ttft_ms | 26.64 | 29.64 | 26.64 |
| mmlu_proxy | 0.6606 | 0.6606 | 0.6606 |
| hellaswag_proxy | 0.7577 | 0.822 | 0.7577 |
| truthfulqa_proxy | 0.6162 | 0.5854 | 0.6162 |
| arc_proxy | 0.667 | 0.6332 | 0.667 |
| complexity_cyclomatic | 3.61 | 3.53 | 3.61 |
| maintainability_index | 76.15 | 66.92 | 76.15 |
| security_issues_high | 1 | 0 | 1 |
| dependency_freshness_pct | 70.5 | 75.9 | 70.5 |
| test_coverage_pct | 59.5 | 59.0 | 59.5 |
| doc_coverage_pct | 65.6 | 70.5 | 65.6 |
| memory_mb | 337.8 | 313.8 | 337.8 |
| gpu_util_pct | 68.8 | 63.1 | 68.8 |
| openssf_score | 5.85 | 7.12 | 5.85 |
| eu_ai_act_compliance_pct | 81.8 | 83.0 | 81.8 |
| slsa_level | 2 | 2 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._
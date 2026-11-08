# HF_Leaderboard_Lab_Results

**Project:** `K_VIPER`  
**Tier:** `TIER_6_SECURITY_EVAL`  
**Slug:** `bettercap/bettercap`  
**Commit:** `8eca2820f3c4`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **46.69 ms** |
| Min latency | 37.49 ms |
| Max latency | 55.97 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **38** |
| Tokenization latency | 0.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5841 |
| Classification latency | 62.26 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_VIPER (bettercap/bettercap) — 2033 files, 102393 source lines, licence GPL-3.0, primary language ['Go']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'viper', '(', 'better', '##cap', '/', 'better', '##cap', ')', '—', '203', '##3', 'files', ',', '102', '##39', '##3', 'source']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_
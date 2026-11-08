# Deploy Guide — K_VIPER
**Tier:** TIER_6_SECURITY_EVAL | **Stack:** Python 3.11, PAX 27B (exploit analysis), CVE database, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PAX 27B, local CVE database (NVD feed), nvdlib 0.7+.

## Environment
4GB RAM. CPU for CVE database queries. GPU for PAX impact analysis.

## AIOSS Integration
```bash
aioss init --module K_VIPER --output ./k_viper.aioss
aioss append --chain ./k_viper.aioss --payload ./output.bin --module K_VIPER
aioss verify --chain ./k_viper.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_VIPER",
    aioss_chain="./K_VIPER.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_VIPER.aioss --verbose
python -m K_VIPER.tests.smoke
```

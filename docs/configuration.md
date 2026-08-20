# Configuration Guide

## Modifying Defaults
Default configurations are stored in `config/defaults.yaml`. Edit this file to adjust standard duration values and min sample sizes:
```yaml
defaults:
  duration_days: 30
  min_sample_size: 200
```

## Adding Metric Thresholds
Adjust standard threshold triggers inside `config/thresholds.yaml`. Follow the strict structure:
```yaml
thresholds:
  [metric_name]:
    success: [value]
    failure: [value]
    severe_failure: [value]
```

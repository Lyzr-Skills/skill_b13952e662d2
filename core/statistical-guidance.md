# Statistical Guidance

Avoid inventing statistical certainty. Clearly distinguish operational success from statistical evidence.

## Signal Classifications

### Directional Signal (Operational)
- **Use Case**: Small startups, tiny cohorts (e.g. 50-100 accounts).
- **Behavior**: Metric exceeds predefined threshold (e.g. 8% vs 3% baseline), but the sample size is mathematically insufficient to achieve high confidence ($p < 0.05$).
- **Action**: Classification set to `PROMISING` or `WEAK`, not `CLEAR WIN`.

### Statistically Strong Evidence
- **Use Case**: Large cohorts (e.g. 1000+ accounts).
- **Behavior**: Conversion difference is mathematically significant ($z$-score $\ge 1.96$ or $p < 0.05$).
- **Action**: Classification set to `CLEAR WIN`.

## Assessment Structure
Statistical assessment outputs must be written using `schemas/statistical-assessment.json` which includes:
- `operational_result`: PASS / FAIL / NEUTRAL
- `statistical_confidence`: HIGH / MEDIUM / LOW / INSUFFICIENT DATA
- `z_score`: Float (Optional)
- `p_value`: Float (Optional)

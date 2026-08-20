# Result Analysis Module

Calculates raw math and statistical outputs deterministically.

## Calculations

1. **Absolute Lift**:
   $$\text{Absolute Lift} = \text{Metric}_{\text{variant}} - \text{Metric}_{\text{control/baseline}}$$
2. **Relative Lift**:
   $$\text{Relative Lift} = \frac{\text{Metric}_{\text{variant}} - \text{Metric}_{\text{control/baseline}}}{\text{Metric}_{\text{control/baseline}}} \times 100\%$$
3. **Operational Signal Verification**: Match calculated outcomes directly to predefined success and failure thresholds.
4. **Statistical Significance**: Compute $p$-values and confidence levels deterministically.
5. **No AI Math**: All calculations must be computed deterministically using standard formulaic modules. The AI models must never synthesize or calculate arithmetic.

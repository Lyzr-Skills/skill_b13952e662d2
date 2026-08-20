# Threshold Definition Module

Guides the definition of success, neutral, and failure thresholds.

## Requirements

1. **Predefined Thresholds**: Must be set before the transition to `READY`.
2. **Numeric Boundaries**: Define boundaries in percentage points or count changes relative to baseline.
3. **No Dynamic Adjustment**: Once running, threshold changes trigger an immediate switch to `INVALIDATED` and require version increments.
4. **Logical Consistency**: $T_{success} > T_{failure} \ge T_{severe\_failure}$.

# Threshold Definition Adversarial Tests

## Test Case 1: Post-launch Alteration
- **State**: `RUNNING`
- **Input**: Update Success Threshold from $\ge 6\%$ to $\ge 4.5\%$.
- **Expected Result**: Validation exception. State set to `INVALIDATED`. Current state logged to `experiment-state.json`, new configuration cloned to v2 in `experiment-version.json`.

## Test Case 2: Inconsistent Ordering
- **Input**: $T_{success} = 3\%$, $T_{failure} = 5\%$.
- **Expected Result**: Gate failure. Success threshold must exceed failure threshold.

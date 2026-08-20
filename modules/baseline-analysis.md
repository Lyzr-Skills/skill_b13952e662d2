# Baseline Analysis Module

Establishes the preconditions and baseline before the experiment starts.

## Evaluation Rules

1. **Verify Baseline Quality**:
   - Query metrics for the preceding 30-day window.
   - Example: 2.8% to 3.2% outbound meeting rate. Set baseline to the mean (3.0%).
2. **Missing Baselines**:
   - If historical data is missing, set value to `UNKNOWN` in `baseline.json`.
   - The engine will output a warning recommending establishing a baseline first OR using a benchmark explicitly labeled as an assumption.
3. **Prevention of Fake Facts**:
   - Do not manufacture values. If `UNKNOWN`, the system requires user-provided assumption config files mapped with classification `BENCHMARK` or `ESTIMATE`.

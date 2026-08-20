# Experiment Quality Module

Scans results to detect execution compromised scenarios.

## Contamination and Validity Checks

1. **Target Contamination**:
   - Check if actual target audience matches design.
   - Example: Target was 100% SMB SaaS, but actual sample includes 30% Agencies.
   - Action: Flag status as `INVALID` with `reason: target_population_compromised`.
2. **Execution Deviations**:
   - Check run duration. If duration was cut short without reaching sample size, flag as `INVALID` (e.g. `reason: premature_termination`).
3. **Metric Distortions**:
   - Scan for external confounding variables (e.g., major industry events, holidays, tracking code failures).
4. **Treatment**:
   - Compromised executions must be recorded as `INVALID` rather than business failure, protecting historical data integrity.

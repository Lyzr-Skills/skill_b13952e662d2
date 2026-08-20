# Quality Validator Adversarial Tests

## Test Case 1: Target Audience Contamination
- **Designed Audience**: VP Marketing at 50-500 employee SaaS.
- **Actual execution sample**: 70 SMB SaaS + 130 marketing agencies.
- **Expected Result**: Result classification marked as `INVALID`. Reason log: `target_population_compromised`.

## Test Case 2: Tracking Breakage
- **Observation**: Zero values recorded across secondary metrics despite active outbound volume.
- **Expected Result**: Flagged as `INVALID`. Reason log: `measurement_tracking_compromised`.

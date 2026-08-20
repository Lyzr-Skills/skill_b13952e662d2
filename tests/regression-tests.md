# Regression Adversarial Tests

## Test Case 1: Recommending Failed Tactics
- **Memory State**: EXP-002 (LinkedIn outreach to SMB) marked as FAILURE.
- **Input**: GTM Strategy proposes testing LinkedIn outreach to SMB again.
- **Expected validation**: Validator checks memory, flags duplicate failure, and forces re-evaluation or rejection unless a new configuration parameter is introduced.

# Decision Engine Adversarial Tests

## Test Case 1: Override to scaling
- **State**: Experiment returns WIN + SCALE recommendation.
- **Input**: Decision Agent constraint checklist evaluates CAC budget limit = $100, projected CAC from scale = $120.
- **Expected Result**: Final decision is PIVOT or HOLD, overriding the Growth Experiment scale recommendation.

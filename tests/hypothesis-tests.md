# Hypothesis Adversarial Tests

Scenario profiles verifying hypothesis quality gates.

## Test Case 1: Loose Goal Submission
- **Input**: "We need to send LinkedIn ads to target customers to improve conversion."
- **Expected Result**: Gate failure. Rejected for lack of numeric thresholds, target baseline, and specific ICP population.

## Test Case 2: Standard Valid Format
- **Input**:
  - IF: LinkedIn cold messaging targeting VP Sales
  - FOR: SaaS companies with 10-50 employees
  - THEN: Increase reply rate
  - FROM: 2%
  - TO: 5%
  - WITHIN: 150 contacts
- **Expected Result**: PASS. Matches If-For-Then formula.

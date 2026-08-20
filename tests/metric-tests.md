# Metric Selection Adversarial Tests

## Test Case 1: Vanity Optimization
- **Input**: Primary metric = Email Open Rate (level = Diagnostic Metric).
- **Expected Result**: Rejected. Diagnostic metrics cannot act as primary outcomes unless directly mapped to Business KPIs.

## Test Case 2: Guardrail Omission
- **Input**: Experiment defined with primary meeting rate, but 0 guardrail metrics selected.
- **Expected Result**: Rejected. Missing guardrail metrics violates the configuration rules.

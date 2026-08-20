# Hallucination Adversarial Tests

## Test Case 1: Mathematical Generation Check
- **Observation input**: Raw conversions: Control = 10 / 100, Variant = 20 / 100.
- **Expected validation**: Ensure raw math is routed to coding layers ($10\%$ and $20\%$ respectively). Reject if AI layers attempt arithmetic directly in prompts without invoking deterministic helper code.

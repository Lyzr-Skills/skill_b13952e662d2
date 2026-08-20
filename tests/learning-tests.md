# Learning Extraction Adversarial Tests

## Test Case 1: Over-generalized Scope assertion
- **Input result**: Small lift on outbound personalization for 50 employee SaaS in US region.
- **Hypothetical output**: "Personalization works globally for all business cohorts."
- **Expected validator action**: Rejected. System validator flags scope override and restricts output to explicit design limits (e.g. US, SMB, SaaS).

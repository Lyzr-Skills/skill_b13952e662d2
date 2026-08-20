# Learning Extraction Module

Extracts qualitative learnings from raw quantitative outputs.

## Structured Format

Learnings must map to `schemas/learning.json` containing:

- **Observation**: Facts directly visible (e.g. "Variant messaging generated $+3.1\%$ meeting rate").
- **Interpretation**: AI hypothesis on *why* (e.g. "Prospective managers react better to direct pain-point callouts").
- **Evidence**: Mathematical link to the outcome.
- **Confidence**: Level of confidence (HIGH, MEDIUM, LOW).
- **Scope**: Explicit parameters where this learning applies:
  - Audience: VP Marketing
  - Geography: US, India
  - Segment: SMB SaaS
  - Channel: Cold Email
- **Limitations**: Boundaries or unknown domains (e.g. "Unverified for Enterprise segment or LinkedIn channels").
- **Follow-up recommendation**: Logical next test to explore boundaries.

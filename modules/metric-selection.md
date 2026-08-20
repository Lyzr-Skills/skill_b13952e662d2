# Metric Selection Module

Enforces correct configuration of metrics before testing.

## Rules

- **Primary Metric Limit**: Exactly one primary metric per experiment.
- **Vanity Check**: Reject experiments where the primary metric is diagnostic (e.g. CTR, open rates) if they don't explicitly lead to business outcomes.
- **Secondary Metrics Mapping**: Track secondary metrics to provide context (e.g. reply rate).
- **Mandatory Guardrails**: Must select at least one guardrail metric (e.g. unsubscribe rate or spam complaint count) to prevent toxic optimization.

# Metric Framework

Growth Experiment Skill uses a structured metric taxonomy to prevent optimizing vanity metrics.

## Metric Hierarchy

```
       North Star Metric (e.g. ARR / Customers)
                     │
                     ▼
       Business KPI (e.g. SQLs / Pipeline value)
                     │
                     ▼
      Experiment KPI (e.g. Meeting rate) [PRIMARY]
                     │
                     ▼
     Diagnostic Metric (e.g. Reply rate) [SECONDARY]
```

Every experiment must map its primary, secondary, and guardrail metrics to this hierarchy.

## Classification Definitions

- **Primary Metric**: The single key performance indicator that determines success or failure of the hypothesis (e.g. Qualified Meeting Rate).
- **Secondary Metrics**: Supporting measurements providing context or diagnostic data (e.g. Email Open Rate, Positive Reply Rate).
- **Guardrail Metrics**: Crucial operational boundaries that must not degrade (e.g. Spam Complaint Rate, Unsubscribe Rate). If a guardrail is violated, it overrides a primary metric success.

## Vanity Metric Safeguards
- The metric engine forces mapping of diagnostic metrics back to business outcome levels.
- Example: Open rate cannot be a primary metric because open rates do not guarantee qualified meetings.

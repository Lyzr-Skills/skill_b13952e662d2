# Experiment Pipeline Specification

The experiment pipeline enforces a structured, repeatable sequence of checks and operations.

```
       [Raw Idea / Input]
                │
                ▼
   1. Hypothesis Formulation
                │
                ▼
     2. Pre-launch Validation
     (Quality Gates, Baseline, Setup)
                │
                ▼
         3. Freezing state
         (Status -> READY)
                │
                ▼
           4. Execution
      (Periodic data updates)
                │
                ▼
        5. Analysis Gate
     (Sample completion, checks)
                │
                ▼
    6. Mathematical Assessment
      (Deterministic logic)
                │
                ▼
       7. AI Interpretation
     (Qualitative logic & Learns)
                │
                ▼
  8. Recommendation to Decision Agent
```

## Stage Triggers and Pipeline Actions

1. **Intake Trigger**: Receives raw proposal.
   - *Action*: Run prompt `hypothesis-validation.md` to format.
2. **Design Trigger**: Hypothesis generated.
   - *Action*: Select metrics, thresholds, control, variant. Verify baseline.
3. **Freeze Trigger**: Request status transition to `READY`.
   - *Action*: Verify quality gates. Lock experiment schema fields. Verify version details.
4. **Execution Trigger**: Status set to `RUNNING`.
   - *Action*: Accept new data points periodically. Update `experiment-state.json`.
5. **Collection Trigger**: Reached duration or sample target.
   - *Action*: Move status to `COMPLETED` and trigger `Result Analysis`.

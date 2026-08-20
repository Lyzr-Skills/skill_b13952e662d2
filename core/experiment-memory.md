# Experiment Memory

Experiment Memory acts as a read/write register for historical experiment metadata.

## Structure

```
Experiment Memory
├── EXP-001 (Control vs Variant Outbound -> win)
├── EXP-002 (LinkedIn outreach -> failure)
└── EXP-003 (Partnership cold call -> promising)
```

## Retrieval and Retrieval-Augmented Safeguards

Prior to designing a new experiment, GTMOS query agents must retrieve past matches from Experiment Memory:

1. **Retest Restrictions**: If a previous experiment testing the exact same variables on the same cohort failed, the engine must block transition to `READY` unless a new structural change (new parameter or different channel) is introduced.
2. **Prior Lift Reference**: Use historical lifts from matching channels to dynamically recommend realistic success thresholds.
3. **Survivorship Bias Protection**: The registry stores failed and invalidated experiments, forcing the memory engine to evaluate both wins and failures.

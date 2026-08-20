# Experiment Dependencies

Some growth experiments depend on the learnings or baseline validations of prior experiments.

## Dependency Model

```
EXP-001 (ICP Validation)
        │
        ▼ (Must pass/be resolved)
EXP-002 (Messaging Test)
        │
        ▼ (Must pass/be resolved)
EXP-003 (Outbound Channel Scaling)
```

## Transition Logic Rules
- **Depends On**: Array of Experiment IDs (`depends_on`). If any ID in the dependency list is not `DECISION_RECOMMENDED` with a status of `SCALE` or `ITERATE`, the child experiment **MUST NOT** transition to `RUNNING`. It remains blocked in `READY` or `DESIGNED` state.
- **Blocks**: Array of Experiment IDs (`blocks`). If the current experiment transitions to `INVALIDATED` or `KILL`, all IDs in the `blocks` list must be automatically updated to a state indicating blocked status (`blocking_conditions` populated in `experiment-state.json`).

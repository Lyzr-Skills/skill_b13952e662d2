# Execution Tracking Module

Updates and records active states during runtime.

## Tracking Rules

1. **State Recording**: Periodically updates `schemas/experiment-state.json`.
2. **Premature Evaluation Block**:
   - If status is `RUNNING` and current sample $<$ target sample:
     - The output reports: `status: RUNNING` and `current_status: INSUFFICIENT SAMPLE`.
     - The engine **MUST NOT** evaluate final victory or failure while the experiment is incomplete.
3. **Transition Rules**: Handles manual pausing (`PAUSED`) or cancellation (`INVALIDATED`).

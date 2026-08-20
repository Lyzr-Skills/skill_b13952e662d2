# Experiment State Machine

This file details the states and valid transitions of GTMOS experiments.

## State Taxonomy

```mermaid
stateDiagram-v2
    [*] --> DRAFT
    DRAFT --> DESIGNED : Design Defined
    DESIGNED --> READY : Passes Quality Gates
    READY --> RUNNING : Start Command
    RUNNING --> PAUSED : Pause
    PAUSED --> RUNNING : Resume
    RUNNING --> INVALIDATED : Contaminated / Change Specs
    READY --> INVALIDATED : Change Specs
    RUNNING --> COMPLETED : Sample/Duration Reached
    COMPLETED --> ANALYZING : Calculation Trigger
    ANALYZING --> ASSESSED : Math/Quality Scan Complete
    ASSESSED --> DECISION_RECOMMENDED : Learning/Rec Generated
    DECISION_RECOMMENDED --> ARCHIVED : Finalized by Decision Agent
    INVALIDATED --> ARCHIVED
```

### Experiment Lifecycle States
- **DRAFT**: Initial suggestion state. Hypothesis may be unstructured.
- **DESIGNED**: Complete variables, metrics, control/variant target defined.
- **READY**: Quality gates passed, baseline established, **properties frozen**.
- **RUNNING**: Actively collecting data. State updates saved to `experiment-state.json`.
- **PAUSED**: Temporarily halted. Tracking paused.
- **INVALIDATED**: Compromised during run, or specification was altered while READY/RUNNING.
- **COMPLETED**: Data collection completed. No new observations accepted.
- **ANALYZING**: Deterministic calculations underway.
- **ASSESSED**: Statistical versus operational signals evaluated, quality scanned.
- **DECISION_RECOMMENDED**: Final recommendation object emitted.
- **ARCHIVED**: State archived into historical experiment memory.

## Decision Recommendations
Separated from execution lifecycle:
- **SCALE**: High performance win. Increase cohort size/exposure.
- **ITERATE**: Moderate outcome. Adjust secondary variables, re-test.
- **PIVOT**: Low performance or failed hypothesis but new insight found. Change tactic.
- **CONTINUE**: Promising but sample size too small for confidence (used when decision agent evaluates mid-run).
- **HOLD**: Suspend strategic scaling (e.g. wait for resource allocation).
- **KILL**: Underperformed baseline, high guardrail degradation, or invalid execution. Stop immediately.

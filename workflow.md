# Growth Experiment Workflow

The canonical lifecycle stages of a growth experiment are defined below:

```
1. Baseline/Precondition Establishment
             ↓
2. Hypothesis Formulation & Validation (Gate check)
             ↓
3. Experiment Design & Dependency Checks
             ↓
4. Metric & Threshold Definition
             ↓
5. Transition to READY (Freezes specs)
             ↓
6. Execution (Running & Tracking)
             ↓
7. Result Collection & Validation
             ↓
8. Learning Extraction
             ↓
9. Decision Recommendation
```

## Stage Descriptions

### 1. Precondition / Baseline
Check historical metrics. If unavailable, set to `UNKNOWN` and proceed using a clearly documented assumed benchmark.

### 2. Hypothesis Validation
Convert simple statements into testable *If-For-Then-From-To-Within* hypotheses. Run through the Quality Gate.

### 3. Experiment Design
Define control, variant, sample target, and experiment type (A/B, Messaging, ICP, etc.). Check dependencies (do not start if dependent experiment failed or blocked).

### 4. Metrics & Thresholds
Define primary, secondary, and guardrail metrics. Set thresholds pre-launch.

### 5. Freeze Specification
Once status changes to `READY`, the configuration is frozen. Any modifications force a state transition to `INVALIDATED` and spawn a new version (e.g. v2).

### 6. Execution Tracking
Periodically update samples and current metrics. Prevent premature evaluation.

### 7. Result Collection & Quality Check
Calculate lift, run statistical assessments (Operational vs Statistical signals), and check for contamination or distortions.

### 8. Learning Extraction
Distinguish raw observations from interpretations. Scope findings to target populations.

### 9. Decision Recommendation
Provide recommended state (SCALE, ITERATE, PIVOT, CONTINUE, HOLD, KILL) to Decision Agent.

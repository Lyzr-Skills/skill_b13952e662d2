# Experiment Contract

The contract guarantees inputs, requirements, and outputs for each step of the pipeline.

| Pipeline Stage | Preconditions (Inputs Required) | Postconditions (Outputs Guaranteed) |
| :--- | :--- | :--- |
| **DRAFT** | Raw suggestion or goal from GTM Strategy. | Semi-structured experiment schema initialized. |
| **DESIGNED** | Formatted hypothesis (If-For-Then-From-To-Within) + explicit type. | Defined Control, Variant, Audience, and primary metric. Assumptions recorded. |
| **READY** | Baseline status verified. Metrics, thresholds, and end criteria set. Passed Quality Gates. | Config frozen. Immutable version record created in `experiment-version.json`. |
| **RUNNING** | Active sample tracker. | Updated states in `experiment-state.json`. |
| **COMPLETED** | Completed sample target or duration target. | Raw result values captured. |
| **ANALYZING** | Completed status. | Deterministic calculations (lift, confidence intervals) evaluated. |
| **ASSESSED** | Calculated metrics and raw values verified. | Quality/contaminant scan complete. Operational vs statistical flag generated. |
| **DECISION_RECOMMENDED** | Assessed result and extracted learning payload. | Pre-configured recommendation schema returned to Decision Agent. |

# Growth Experiment Architecture

## Boundary and Separations

```
┌─────────────────────────────────┐
│        GTM Strategy Agent       │ (Decides strategy and proposes experiment ideas)
└────────────────┬────────────────┘
                 │
                 ▼ (Proposal)
┌─────────────────────────────────┐
│     Growth Experiment Skill     │ (Designs, tracks, calculates metrics, recommends)
└────────────────┬────────────────┘
                 │
                 ▼ (Recommendation - NOT Final Decision)
┌─────────────────────────────────┐
│          Decision Agent         │ (Owns final decision, checks CAC, budgets, strategic context)
└─────────────────────────────────┘
```

### Growth Experiment vs GTM Strategy
- **GTM Strategy**: "We should test personalized outbound."
- **Growth Experiment**: "Here is exactly how to test personalized outbound, including sample size, audience, metrics, thresholds, and versioned hypotheses."

### Growth Experiment vs Decision Agent
- **Growth Experiment**: Calculates lift, states evidence, and recommends e.g. "SCALE".
- **Decision Agent**: Evaluates recommendation against company constraints. E.g., rejects "SCALE" because of cash flow or CAC constraints.

## Technical Components

1. **Intake and Hypothesis Validator**: Enforces SPECIFIC, MEASURABLE, FALSIFIABLE, BOUNDED, ACTIONABLE gates.
2. **Baseline Engine**: Establishes pre-test reference data.
3. **Experiment Design Engine**: Coordinates control/variant or single-cohort designs.
4. **Metric & Threshold Engine**: Implements the metric hierarchy and deterministic threshold checks.
5. **Execution Tracker**: Manages mutable state transitions and prevents p-hacking.
6. **Result Analyzer**: Computes deterministic calculations.
7. **Learning & Memory Engine**: Translates observations to interpretations and persists them.

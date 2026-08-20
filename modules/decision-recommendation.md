# Decision Recommendation Module

Prepares recommendation payload for submission to Decision Agent.

## Scope of Output

1. **Recommendation State**: Suggests SCALE, ITERATE, PIVOT, CONTINUE, HOLD, or KILL.
2. **Contextual Justification**: Explains the rationale using metric performance and quality checks.
3. **Guardrail Statement**: Explains if any guardrails were impacted or violated.
4. **Integration Rule**: Explains that this output is a *Recommendation* and requires Decision Agent activation to evaluate against budget and strategic policies.
5. **JSON Schema Mapping**: Standardizes output format using `schemas/decision-recommendation.json`.

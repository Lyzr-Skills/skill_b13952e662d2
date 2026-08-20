# Usage Guide

## Step 1: Input Concept Formulation
Initiate experiment intake:
```json
{
  "name": "Outbound Personalization Test",
  "concept": "personalized messaging raises qualified meetings"
}
```

## Step 2: Running through Pipeline
1. Execute validation prompts to generate `hypothesis.json` and `baseline.json`.
2. Define thresholds and transition status to `READY`. This freezes immutable fields.
3. Once running, stream data updates into `execution.json`.
4. Trigger result analysis upon hitting stopping conditions.

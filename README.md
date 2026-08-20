# Growth Experiment Skill

Growth Experiment is a core execution skill for GTMOS. It defines how to run a specific growth experiment, measure it, interpret the results, and decide what recommendation to make next.

## Architecture

This skill sits between **GTM Strategy** and the **Decision Agent**:

```
GTM Strategy Agent
        │
        │ experiment proposal
        ↓
┌─────────────────────────┐
│   Growth Experiment     │
│                         │
│ Baseline                │
│ ↓                       │
│ Hypothesis              │
│ ↓                       │
│ Experiment Design       │
│ ↓                       │
│ Metric                  │
│ ↓                       │
│ Threshold               │
│ ↓                       │
│ Execution               │
│ ↓                       │
│ Result                  │
│ ↓                       │
│ Learning                │
│ ↓                       │
│ Decision Recommendation │
└────────────┬────────────┘
             ↓
      Decision Agent
             ↓
      SCALE / ITERATE /
      PIVOT / KILL / HOLD
```

## Folder Structure

- `/core`: Core state machines, pipelines, gates, rules.
- `/config`: Configuration defaults, thresholds, experiment types.
- `/modules`: Module specifications outlining the stages of implementation.
- `/schemas`: JSON Schemas representing the data model.
- `/prompts`: AI system prompts.
- `/tests`: Adversarial scenarios for validation.
- `/docs`: Usage and configuration guides.

# Growth Experiment Skill Contract

## Objective
Answer: Did the experiment work? What did we learn? How confident are we? What should happen next?

## Skill Inputs
- **Experiment Input**:
  - `experiment_id`: String
  - `name`: String
  - `type`: Enum (A/B Test, Channel Test, messaging Test, etc.)
  - `hypothesis_id`: String
  - `objective`: String
  - `target_audience`: String
  - `control`: String (Optional)
  - `variant`: String
  - `baseline_ref`: String (Optional)
  - `primary_metric`: Object
  - `secondary_metrics`: Array of Objects
  - `guardrail_metrics`: Array of Objects
  - `success_threshold`: Object
  - `failure_threshold`: Object
  - `sample_target`: Integer
  - `duration`: String
  - `budget`: Number (Optional)
  - `depends_on`: Array of Strings (Optional)
  - `blocks`: Array of Strings (Optional)

- **Context from GTMOS**:
  - ICP (Ideal Customer Profile) definition
  - Persona definitions
  - GTM Strategy guidelines
  - Previous experiment history (from Experiment Memory)
  - Historical metrics

## Skill Outputs
- **Result and Analysis**:
  - Pre-defined metrics calculation (Absolute lift, Relative lift)
  - Result Classification (CLEAR WIN, PROMISING, INCONCLUSIVE, WEAK, FAILURE, INVALID)
- **Learnings**:
  - Observation vs Interpretation
  - Scope and Limitations
  - Confidence Level
- **Decision Recommendation**:
  - Recommended Decision (SCALE, ITERATE, PIVOT, CONTINUE, HOLD, KILL)
  - Proposed Actions / Follow-ups

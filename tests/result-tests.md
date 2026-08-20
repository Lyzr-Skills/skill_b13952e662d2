# Result Analysis Adversarial Tests

## Test Case 1: Incomplete Run Evaluation
- **Input**: Target sample = 200, current sample = 137. Evaluation trigger received.
- **Expected Result**: Return status `RUNNING`, reason `INSUFFICIENT SAMPLE`. The engine rejects making final recommendations prior to full sample collection.

## Test Case 2: Conflicting Metric Signal
- **Input**:
  - Primary Meeting Rate = $+120\%$ lift (Success threshold met).
  - Unsubscribe Rate = $+300\%$ increase (Breaches guardrail threshold limit).
- **Expected Result**: Recommendation set to **REVIEW / ITERATE** or **KILL** with explicit warnings regarding the guardrail breach. Must not recommend **SCALE**.

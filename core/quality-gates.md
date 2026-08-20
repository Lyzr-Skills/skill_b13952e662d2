# Quality Gates

Before an experiment can transition to the **READY** state, it must pass 9 mandatory quality gates. If any gate fails, the state is forced to **NOT READY** (retained in **DESIGNED** or **DRAFT**).

```
 ┌────────────────────────────────────────────────────────┐
 │                      QUALITY GATES                     │
 ├────────────────────────────────────────────────────────┤
 │  [Gate 1] Falsifiable Hypothesis                       │
 │  [Gate 2] Primary Metric Defined                       │
 │  [Gate 3] Success Threshold Predefined                 │
 │  [Gate 4] Failure Threshold Predefined                 │
 │  [Gate 5] Baseline Exists (or explicitly UNKNOWN)      │
 │  [Gate 6] Target Population Bounded & Binned           │
 │  [Gate 7] Measurement & Tracking Method Exists         │
 │  [Gate 8] Defined End Condition (sample or duration)   │
 │  [Gate 9] Decision Rule Mapped                         │
 └────────────────────────────────────────────────────────┘
```

## Gate Definitions

1. **Gate 1: Falsifiable Hypothesis**
   - The hypothesis must be structured as *If-For-Then-From-To-Within*.
   - A clear negative outcome must be possible (i.e. we can prove it wrong).
2. **Gate 2: Primary Metric**
   - Exactly one primary metric must be defined.
3. **Gate 3: Success Threshold**
   - Must contain a mathematically testable threshold (e.g. $\ge 6\%$).
4. **Gate 4: Failure Threshold**
   - Must contain a mathematically testable lower-bound failure threshold (e.g. $< 4\%$).
5. **Gate 5: Baseline Verification**
   - A historical baseline must exist (e.g. 3%), or must be explicitly flagged as `UNKNOWN` with documented assumptions.
6. **Gate 6: Target Population**
   - Audience criteria must be bounded (e.g., "VP Marketing at 50-500 employee SaaS").
7. **Gate 7: Measurement Verification**
   - Method for capturing metrics (e.g., Salesforce, Hubspot hook) must be defined.
8. **Gate 8: Defined End Condition**
   - End condition must be set (e.g., 200 accounts, 30 days) to prevent perpetual running or p-hacking.
9. **Gate 9: Decision Rule**
   - Must map thresholds directly to recommendations.

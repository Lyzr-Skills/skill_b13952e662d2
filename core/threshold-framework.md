# Threshold Framework

Thresholds must be defined prior to experiment execution to prevent post-hoc goalpost shifting.

## Threshold Levels

For any metric $M$, thresholds must define these distinct outcome brackets:

1. **Success**: $M \ge T_{success}$ (Triggers SCALE)
2. **Neutral**: $T_{failure} \le M < T_{success}$ (Triggers ITERATE or CONTINUE)
3. **Failure**: $T_{severe\_failure} \le M < T_{failure}$ (Triggers PIVOT or KILL)
4. **Severe Failure**: $M < T_{severe\_failure}$ (Triggers immediate KILL)

```
◄─────────────────┼───────────────────┼────────────────────┼──────────────►
 Severe Failure        Failure            Neutral             Success
 (Kill)                (Pivot/Kill)       (Iterate)           (Scale)
```

## Immutable Rules
- Success and Failure thresholds are saved in `experiment-version.json` when transitioned to `READY`.
- Editing thresholds after an experiment transitions to `READY` or `RUNNING` will flag the experiment as `INVALIDATED` and require a new version (e.g. v2).

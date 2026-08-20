# Sample Size and Duration Module

Calculates minimum target samples and runtimes.

## Guidelines

- **Duration Guidelines**: Suggest runtimes based on sales/action cycles (e.g. 14 days for email outreach).
- **Minimum Observations**: Define minimal numbers of observations to check (e.g. 100 accounts).
- **No Statistics Invention**: Do not create or assert high confidence statistical assertions when samples are small. Clearly flag tiny sample size results as operational signal (`operational_result: PASS`, but `statistical_confidence: INSUFFICIENT DATA`).
- **Stopping Criteria**: Define clear target samples (e.g., 200 targeted prospects) to stop execution and prevent runtime p-hacking.

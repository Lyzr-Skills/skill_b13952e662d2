# Troubleshooting Guide

## Mismatched Schema Errors
- **Symptom**: Config parser rejects configuration JSON.
- **Solution**: Ensure your inputs comply with type boundaries defined in `/schemas` schemas.

## State Freezing Conflict (Frozen Field Edit)
- **Symptom**: Attempting to rewrite threshold or hypothesis throws validation error.
- **Solution**: Set current experiment state to `INVALIDATED` and generate new version object (v2) inside `experiment-version.json` schema layout.

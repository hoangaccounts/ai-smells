# Partial Rewrites Breaking Consistency

## Summary
The AI updates one part of an artifact but leaves related parts inconsistent.

## Observed Behavior
Renaming a concept in one section while references elsewhere remain unchanged.

## Minimal Example
Term updated in intro but not in later sections.

## Why It Matters
- Inconsistent artifacts
- Reader distrust
- Subtle bugs

## Constraints & Boundary Conditions
- Large documents
- Iterative edits

## Candidate Guardrails (Optional)
- Consistency sweeps
- Cross-reference checks

## Related Smells (Optional)
- Unscoped Regeneration

## Notes (Optional)
Surface-level correctness hides deeper breaks.

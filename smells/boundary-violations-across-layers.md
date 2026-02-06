# Boundary Violations Across Layers

## Summary
The AI fixes an issue in one layer by changing another, violating architectural boundaries.

## Observed Behavior
UI problems lead to domain changes.
Data issues trigger app-level rewrites.

## Minimal Example
Fixing a UI bug by altering domain logic.

## Why It Matters
- Architecture erosion
- Tight coupling
- Long-term cost

## Constraints & Boundary Conditions
- Layered architectures
- Systems with explicit boundaries

## Candidate Guardrails (Optional)
- Frozen layers
- Explicit boundary permissions

## Related Smells (Optional)
- Misaligned Defaults

## Notes (Optional)
Short-term fixes, long-term damage.

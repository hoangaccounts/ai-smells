# Format Drift and Spec Leakage

## Summary
The AI blends explanation, specification, and implementation details into a single output, eroding boundaries between descriptive and normative content.

## Observed Behavior
A user asks for a spec-like artifact.
The assistant alternates between prose explanation, pseudo-code, and implementation suggestions without signaling which parts are authoritative.

## Minimal Example
A section labeled “Specification” includes narrative advice and example code mixed with MUST/SHALL language.

## Why It Matters
- Readers cannot tell what is binding vs illustrative
- Artifacts become unusable for enforcement or tooling
- Specs slowly degrade into tutorials

## Constraints & Boundary Conditions
- Common in early-stage designs
- Triggered by “explain and define” prompts
- Worse when iterating on partial specs

## Candidate Guardrails (Optional)
- Explicit section typing (normative vs non-normative)
- Validation of normative language usage

## Related Smells (Optional)
- Vocabulary Collisions

## Notes (Optional)
Often introduced gradually across revisions.

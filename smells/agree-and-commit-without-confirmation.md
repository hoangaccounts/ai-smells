# Agree-and-Commit Without Confirmation

## Summary
The AI proceeds as if approval was granted when the user was still exploring or thinking aloud.

## Observed Behavior
Exploratory phrases (“maybe”, “what if”) are treated as decisions.
The assistant implements changes immediately instead of pausing.

## Minimal Example
User: “Maybe we could rename this?”
Assistant: Outputs a full rename diff.

## Why It Matters
- Removes user agency
- Forces rollback
- Creates frustration and churn

## Constraints & Boundary Conditions
- Fast-paced back-and-forth
- Long sessions with implicit momentum

## Candidate Guardrails (Optional)
- Explicit approval tokens
- Mandatory plan/preview step

## Related Smells (Optional)
- Unscoped Regeneration

## Notes (Optional)
Feels like helpfulness, but acts like force.

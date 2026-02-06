# Overconfidence Without Verifiability

## Summary
The AI states claims confidently without providing sources, checks, or verification paths.

## Observed Behavior
The assistant asserts correctness (“this will work”, “best practice”) without evidence or tests.

## Minimal Example
Claiming library behavior without linking docs or tests.

## Why It Matters
- Incorrect decisions become entrenched
- Hidden bugs surface later
- Trust erodes silently

## Constraints & Boundary Conditions
- Technical domains
- Edge cases
- Fast answers prioritized over correctness

## Candidate Guardrails (Optional)
- Require citations or tests for claims
- Explicit confidence qualifiers

## Related Smells (Optional)
- Invisible Assumption Drift

## Notes (Optional)
Confidence is mistaken for accuracy.

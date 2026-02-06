# Smell: Overconfidence Without Verifiability

## Summary

**Overconfidence Without Verifiability** occurs when the AI asserts correctness without evidence, sources, or validation paths.

---

## Observed Behavior

- The assistant introduces changes that were not explicitly requested.
- Previously stable assumptions, structure, or wording shift without notice.
- The change is framed as “reasonable” or “helpful,” masking the violation.

---

## Why This Is a Problem

- Undermines user intent and trust.
- Forces costly re-review of already accepted material.
- Breaks attribution: users can no longer trace *why* something changed.
- Makes iterative collaboration brittle and exhausting.

---

## Root Cause

The model prioritizes confident completion over epistemic humility.

---

## Invariant Violated

> Claims must be distinguishable from verified facts.

---

## Candidate Guardrails (Ideas Only)

- Explicit declaration of stable vs mutable elements.
- Confirmation gates before assumption or boundary changes.
- Diff-based execution with scope enforcement.
- Rejection of implicit reinterpretation.

---

## Detection Signal

- Output “feels off” despite appearing coherent.
- User must restate constraints already agreed upon.
- Changes appear outside the stated goal.

---

## Status

Observed repeatedly in real-world AI-assisted work.

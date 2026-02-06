# Smell: Boundary Violations Across Layers

## Summary

**Boundary Violations Across Layers** occur when the AI fixes an issue in one layer by modifying another.

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

The model optimizes for local correctness rather than architectural integrity.

---

## Invariant Violated

> Changes must respect declared layer boundaries.

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

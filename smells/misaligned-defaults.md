# Smell: Misaligned Defaults

## Summary

**Misaligned Defaults** occur when the AI applies reasonable-sounding defaults that conflict with the user’s actual constraints.

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

The model fills missing context with generalized assumptions.

---

## Invariant Violated

> Defaults must be explicit and confirmed.

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

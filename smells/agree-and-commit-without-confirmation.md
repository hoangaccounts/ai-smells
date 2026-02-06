# Smell: Agree-and-Commit Without Confirmation

## Summary

**Agree-and-Commit Without Confirmation** occurs when the AI treats exploratory statements as final decisions and proceeds without approval.

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

The model infers intent from conversational flow rather than explicit commitment signals.

---

## Invariant Violated

> No action should be taken without an explicit approval signal.

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

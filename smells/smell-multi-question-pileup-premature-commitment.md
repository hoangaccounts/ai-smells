# Smell: Multi-Question Pileup + Premature Commitment

## Summary

The AI bundles multiple decision questions at once (often 2–5), then implicitly proceeds as if the user agreed with a particular option. This creates pressure to respond in bulk, increases friction, and erodes trust because the user loses control of the step-by-step decision flow.

---

## Observed Behavior

- The AI asked three independent decision questions in one message (e.g., ordering behavior, initial order, width strategy).
- The AI framed a recommendation inline and moved toward implementation/prompt writing before confirming the user’s intent.
- The user experienced this as repeated-loop behavior and cognitive overload (“how am I supposed to answer all 3 questions at once”).

---

## Why This Is a Problem

- **Trust:** Users feel the AI is steering or “assuming agreement,” reducing confidence.
- **Correctness:** Decisions become coupled incorrectly; later answers may depend on earlier ones.
- **Workflow:** Breaks one-by-one approval flow; increases clarifications and resets.
- **Cognitive load:** Forces the user to hold multiple tradeoffs simultaneously.

---

## Root Cause

Planning shortcut: the AI tries to gather all missing info in one turn while also recommending a path. This collapses an iterative approval workflow into a batch questionnaire and creates accidental forward motion.

---

## Invariant Violated

Only introduce **one** decision point per turn and do not advance to implementation language (or “final prompt” mode) until that single decision is explicitly approved or rejected.

---

## Candidate Guardrails (Ideas Only)

- Ask **one** question per turn when approval gating is expected; defer the rest.
- Separate **recommendation** from **decision**: propose, then ask approval without assuming.
- If multiple unknowns exist, queue them explicitly, but ask only the next one:
  1) Decide reorder vs emphasize-only
  2) Decide initial order rule
  3) Decide width strategy
- “No forward motion” rule: do not draft prompts/specs unless the user explicitly requests “prompt” after decisions are locked.

---

## Detection Signal

- User says:
  - “How am I supposed to answer all X questions at once?”
  - “Why did you assume I agree?”
  - “We keep doing the same thing over and over.”
- Conversation shows repeated resets / re-asking after bundled questions.
- AI message contains multiple numbered questions plus an implementation-ready plan in the same turn.

---

## Status

- **Severity:** High (breaks approval workflow; damages trust).
- **Frequency:** Common in iterative UI refinement loops.
- **Where observed:** Scenario Comparison refinement chat (one-by-one approve/deny cadence).

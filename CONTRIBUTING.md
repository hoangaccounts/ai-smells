# Contributing

Thanks for helping make this catalog sharper and more useful.

## What we accept

### ✅ New smells
A “smell” is an **observed failure mode** that:
- can be described concretely (what happened, in what context),
- is repeatable enough to matter,
- causes drift, confusion, wasted effort, or incorrect output.

### ✅ Guardrail ideas
We welcome **candidate guardrails** as ideas, but keep them grounded in the smell:
- what the guardrail would prevent,
- what it might break,
- how it could be tested.

## What we don’t accept (yet)

- Big product roadmaps, monetization plans, or platform design.
- Enforcement mechanisms that require large architecture changes without a minimal proof.

## Workflow

1. **Open an issue** using “Smell Report” (best for discussion), or
2. **Open a PR** adding a new smell doc.

## PR checklist

- [ ] Uses the template: `ai-smells/smell-doc-template.md`
- [ ] One smell per file
- [ ] Includes at least one concrete example (snippet / transcript / minimal repro)
- [ ] Avoids prescribing a final implementation (capture pressure + options)

## Style notes

- Prefer clear headings over long prose.
- Prefer short examples over hypothetical scenarios.
- If you introduce a term, define it once and reuse it consistently.

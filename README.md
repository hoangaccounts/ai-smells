# AI Smells

A small, practical catalog of **failure modes (“smells”)** that show up when collaborating with AI on design-, intent-, and change-sensitive work — plus **guardrail ideas** that may reduce drift.

This repo is intentionally lightweight: it’s a place to capture **real observed pressure** before turning anything into policy, tooling, or a spec.

---

## What’s in here

- **Smell catalog + guardrail notes:** see **[Design Smells & Guardrail Ideas](ai-smells/design-smells-and-guardrail-ideas.md)**
- **Standard smell write-up format:** see **[Smell Documentation Template](ai-smells/smell-doc-template.md)**
- **Experiments / drafts:** see **[`ai-smells/labs/`](ai-smells/labs/)**

---

## How to add a smell

1. Copy the template:
   - `ai-smells/smell-doc-template.md` → `ai-smells/smell-<short-name>.md`
2. Fill it out with **one concrete example** (the smallest reproducible snippet you can).
3. Open a PR.

If you’re unsure whether something is a “smell” or a “bug,” open an issue using the **Smell Report** template and we’ll sort it out.

---

## Principles

- **Observed behavior first.** Capture what happened and why it mattered.
- **Pressure, not policy.** Avoid prescribing final enforcement or product features in smell docs.
- **Small and navigable.** Prefer many small docs over one giant write-up.

---

## License

MIT — see **[LICENSE](LICENSE)**.

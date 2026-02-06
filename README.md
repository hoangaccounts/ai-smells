# AI Smells

A small, practical catalog of **failure modes (“smells”)** that show up when collaborating with AI on design-, intent-, and change-sensitive work.

This repository focuses on **observed behavior** — not solutions, tooling, or enforcement.
It exists to name recurring problems clearly *before* trying to fix them.

---

## What’s in here

- **Smell catalog**  
  Individual, focused documents describing real AI collaboration failure modes:  
  👉 **[`ai-smells/smells/`](smells/)**

- **Smell documentation format**  
  The standard template used for every smell write-up:  
  👉 **[`ai-smells/smell-doc-template.md`](smell-doc-template.md)**

---

## What this repo is (and isn’t)

**This repo is:**
- A place to capture *repeatable problems* seen in real AI-assisted work
- Pressure documentation: what breaks, how, and why it matters
- Intentionally small, readable, and navigable

**This repo is not:**
- A guardrail specification
- A product roadmap
- An enforcement framework
- A proposal for how AI *should* behave

Those may come later — but only if the smells justify them.

---

## How to add a smell

1. Copy the template:  
   `ai-smells/smell-doc-template.md` → `ai-smells/smells/smell-<short-name>.md`

2. Document **one smell only**, including:
   - what was observed
   - a minimal concrete example
   - why it mattered

3. Open a PR.

If you’re unsure whether something qualifies as a smell, open an issue and describe the behavior first.

---

## Principles

- **Observed behavior first** — no hypotheticals
- **One smell per file**
- **Concrete examples over theory**
- **Pressure, not prescriptions**

---

## License

MIT — see **[LICENSE](LICENSE)**.

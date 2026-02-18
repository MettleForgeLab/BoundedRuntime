# Stacking Recipe (Example)

## Core KBIN + Adapter + Lens + User Prompt (Correct Order)

**Order matters.** Stack from most general / load-bearing → most specific / task-bound:

1. **Core KBIN** (runtime stability rule deck)
2. **Adapter** (platform expression tuning only)
3. **Lens** (domain bias overlay; does not alter core constraints)
4. **User Prompt** (the actual request)

---

## 1) Core KBIN (paste first)

[Insert contents of core/runtime_kbin_generic.txt here when stacking.]

---

## 2) Adapter (paste second)

**Example: `adapters/adapter_gpt.txt`**

- Keep responses compact when contracting
- Prefer headings + bullets
- No “as an AI model…” boilerplate unless necessary
- Refusals: brief, protective, redirect-oriented

[PASTE ADAPTER TEXT HERE]

---

## 3) Lens Overlay (paste third)

**Example: `lenses/lens_architecture.txt`**
Biases (within the ladder):

- Prefer `frame` early
- Use `template` for complex systems work
- Use `options` for tradeoffs; avoid single “best” prescription
- Sequence: clarify → frame → options/template → direct

[PASTE LENS TEXT HERE]

---

## 4) User Prompt (paste last)

> You are helping design a small internal tool for our team.  
> Constraints: low risk, no external tools.  
> Goal: propose an architecture and a phased rollout plan.  
> Requirements: keep it under 500 words, include a checklist.
>
> **Request:** Draft a one-page architecture proposal for an internal “meeting notes summarizer” that runs locally.

---

## Notes

- If the model begins drifting or over-expanding, tighten by **removing the lens first**, not the core.
- If the model feels too terse, keep the core and lens, but adjust the **adapter** to permit more `direct`/`options` under low A/H/B.
- For multi-turn work, keep the **Core KBIN + Adapter + Lens** constant; only replace the user prompt content each turn.

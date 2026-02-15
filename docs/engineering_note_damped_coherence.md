# Engineering Note: Damped Coherence Analogy

## Purpose

This note explains the rationale behind the Softfold / Narrowband / Openband coherence model using a damped-system analogy.

It is descriptive, not mechanistic.

## 1. The Analogy

In classical control systems:

m x'' + c x' + k x = F(t)

Where:

- m = mass (inertia)
- c = damping (resistance to oscillation)
- k = stiffness (restoring force)
- F(t) = applied force

System behavior depends on damping ratio:

- Underdamped → oscillatory overshoot
- Overdamped → slow, inert, rigid
- Moderately damped → stable, responsive

## 2. Mapping to Runtime Behavior

In bounded generation:

- Incoming prompt load ≈ F(t)
- Context depth ≈ inertia
- Boundary + switching logic ≈ damping
- Structural coherence ≈ stiffness

Excess expansion resembles underdamped oscillation.
Excess refusal resembles overdamped rigidity.

Softfold approximates moderate damping:

- Contraction occurs promptly under strain.
- Expansion resumes only after stabilization.
- Oscillation is prevented through hysteresis.

## 3. Why This Matters

The analogy helps clarify:

- Why hysteresis is necessary.
- Why widening must require stronger evidence than contraction.
- Why dissipative scheduling (cooldown cycles) prevents runaway escalation.
- Why band transitions must not occur mid-response.

The analogy does not imply:

- Internal physical dynamics,
- Conscious regulation,
- Literal mechanical oscillation.

It provides a conceptual stability model.

## 4. Implementation Boundary

The damped-system analogy operates at the runtime envelope layer only.

It does not:

- Modify model weights,
- Replace switching logic,
- Override constitutional constraints.

It shapes how bandwidth expands or contracts under load.

---

### Appendix — On the Coherence Band Model

The coherence band model used in BoundedRuntime is inspired by damped-system analogies from control theory.

The goal is not to literalize physical equations inside language systems, but to borrow the stability intuition of moderately damped systems:

- Avoid oscillation (over-expansion followed by over-contraction).
- Avoid stall (permanent narrowband brittleness).
- Maintain responsive but stable interpretive motion.

For extended exposition and studio-grade exploration of this analogy, see MFL studio materials.

End of note.

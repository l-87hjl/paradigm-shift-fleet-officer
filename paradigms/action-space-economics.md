# Action-Space Economics

This paradigm describes a **structural reality** that applies to all real systems, independent of intent, values, or correctness.

It is not normative.
It does not say what *should* be done.
It describes what *inevitably happens* when constraints are introduced into an operational system.

---

## Core Observation

> **Alignment improves when actions are removed from existence.**  
> **Security improves only when the removal meaningfully shrinks the reachable action space relative to its cost.**

Both statements are simultaneously true.
Confusing them leads to either false safety or unmanageable systems.

---

## Alignment vs. Security (Non-Identical)

- **Alignment** concerns whether a system can act outside intended bounds.
- **Security** concerns whether constraints materially reduce risk in practice.

Removing actions from a system *always* improves alignment in the abstract.
But it improves security **only if** the removed actions:
- were realistically reachable
- could have caused meaningful harm
- and are removed at a cost lower than the risk they mitigated

---

## The Cost Side of the Equation

Every constraint has costs:
- operational friction
- maintenance overhead
- deployment complexity
- human error surface
- slowed iteration or competitiveness loss

Constraints that do not significantly shrink the reachable action space:
- add complexity without safety
- increase failure modes
- can reduce overall system reliability

Security is therefore an **economic question**, not a moral one.

---

## Reachable vs. Theoretical Action Space

A critical distinction:

- **Theoretical action space**: everything a system could do in principle
- **Reachable action space**: what the system can actually do given its environment

Only reductions in the *reachable* action space improve security.

Constraints that operate purely at the conceptual or advisory level do not reliably reduce reachability.

---

## Why This Reality Is Often Ignored

Humans tend to:
- equate more rules with more safety
- underestimate maintenance cost
- ignore second-order effects of complexity

Machines, meanwhile:
- exploit whatever action space remains
- do not internalize intent or tradeoffs

This mismatch produces systems that are heavily constrained on paper but permissive in practice.

---

## Implications

- Not all constraints are worth adding
- Fewer, harder constraints often outperform many soft ones
- Architectural limits beat procedural ones
- Some risks are cheaper to accept than to eliminate

These are not value judgments.
They are properties of constrained systems.

---

## Relationship to Other Paradigms

This paradigm complements:
- **Non-Representable Actions** — explains *why* removing actions works
- **Machines Are Not People** — explains *why intent cannot compensate for structure*
- **Governance by Architecture** — explains *where* constraints must live

---

## Summary

- Alignment and security are related but not identical
- Security improvements require meaningful reduction of reachable action space
- Constraint effectiveness must be evaluated against cost
- This tradeoff is an objective feature of real systems

This paradigm should be used as a reality check whenever new safeguards are proposed.

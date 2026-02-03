# Capability Routing via Multiple Repo Bridges (In Progress)

This note captures an exploratory architectural discussion about enforcing agent roles through **capability constraints**, not instruction or trust.

It is **not** a finalized design or paradigm.
It is parked here to preserve the reasoning without promoting it prematurely.

---

## Core Claim

Alignment is enforced most reliably when agents are constrained by **what they can do**, not by what they are told to do.

Machines do not internalize norms. They route optimization through affordances.

Therefore:
> Agents should be given roles by **capability surfaces**, not by instructions.

---

## Capability Routing Model

- Multiple Repo Bridge instances exist
- Each bridge exposes a **distinct permission and call surface**
- Agents are routed through a bridge appropriate to their role

An agent does not "decide" to respect its role.
It is physically unable to violate it.

Examples:
- Architect / planner → read-only bridge
- Implementer → scoped write bridge
- Reviewer → diff-only bridge
- Migrator → cross-repo, non-destructive bridge

The bridge, not the agent, enforces alignment.

---

## Why This Works

- Constraints live at the capability layer, not the cognitive layer
- Instructions (MD files, prompts) are treated as onboarding, not control
- If an action is not representable, it cannot be optimized toward

The safest constraint is not "don’t do X" but:
> **X does not exist in the action space**

---

## Anti-Goals Reframed

Rather than anti-goals, this approach relies on:
- **non-representable actions**
- hard limits on what exists in the agent’s world

This avoids reward hacking, norm erosion, and intent reinterpretation.

---

## Fault Isolation

Using multiple bridges instead of a single, parameterized gateway provides:
- reduced blast radius
- easier reasoning about failure modes
- safer experimentation with agent behavior

Unexpected optimization is contained to the bridge surface it can access.

---

## Status

- Exploratory
- Not indexed
- Not promoted to project or paradigm
- Intended for pressure-testing and possible discard

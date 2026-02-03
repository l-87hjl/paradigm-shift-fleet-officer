# Non-Representable Actions

This paradigm captures a core alignment insight:

> **The safest constraint is not “don’t do X,” but “X does not exist in the action space.”**

It formalizes why architectural limits are more reliable than instructions, norms, or intentions when working with machine agents.

---

## Core Claim

Machines do not reason about prohibitions the way humans do.
They optimize over the **actions that are available to them**.

If an action is representable, it can be optimized toward.
If an action is non-representable, it cannot be reached, planned for, or traded against.

Alignment is therefore strongest when unsafe or undesired actions are **removed from the space of possible actions entirely**.

---

## Why Prohibitions Fail

Rules such as:
- “do not modify production code”
- “do not deploy automatically”
- “do not cross repository boundaries”

remain cognitively visible to a machine.

They require:
- interpretation
- memory
- norm adherence

All of which are brittle under optimization pressure.

A prohibition is advisory.
A missing capability is absolute.

---

## Non-Representability as Alignment Primitive

Non-representable actions are created by:
- permission boundaries
- capability-scoped APIs
- isolated execution environments
- separate control planes

Examples:
- An agent routed through a read-only interface cannot write, regardless of intent.
- An agent without deploy primitives cannot deploy, even if asked.
- An agent without cross-repo access cannot propagate changes.

The agent does not “choose” to behave.
It has no alternative behavior available.

---

## Relationship to Anti-Goals

Anti-goals attempt to negate behavior within the agent’s reasoning space.

Non-representable actions eliminate the behavior from that space entirely.

This avoids:
- reward hacking
- reinterpretation of constraints
- gradual erosion of norms

It shifts alignment from psychology to topology.

---

## Fault Containment

By limiting action spaces:
- unexpected optimization is contained
- blast radius is reduced
- failures are easier to reason about

Multiple constrained environments are safer than a single permissive one with flags.

---

## Summary

- Machines optimize over available actions, not intentions
- Prohibitions are weaker than absence
- Alignment is strongest when unsafe actions are non-representable
- Architecture outperforms instruction for durable control

This paradigm should be used to evaluate all agent and system designs in this repository.

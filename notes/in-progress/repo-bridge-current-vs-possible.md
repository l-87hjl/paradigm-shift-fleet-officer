# Repo Bridge — Current State vs. Potential Hardening (In Progress)

This note documents the **current, real security posture** of Repo Bridge and contrasts it with **plausible architectural extensions**.

It exists to prevent confusion between what is *already enforced* and what is *theoretically possible*.

---

## Current State (As Implemented Today)

The current Repo Bridge security model relies on several concrete environmental constraints:

### 1. GitHub App Installation Boundary

- The Repo Bridge GitHub App must be explicitly installed on each repository
- Repositories without the app installed are completely inaccessible

This is a **hard external constraint** and the strongest existing boundary.

---

### 2. Ownership Boundary

- Access tokens are valid only for repositories owned by the user
- No access to third-party or external repositories

This limits blast radius to the user’s own namespace.

---

### 3. Authorization Scope (Current)

Through Render configuration:

- Authorized repositories may be:
  - explicitly listed (`user/repo`)
  - or wildcarded (all user repositories)

- Permissions are per-repository:
  - read-only
  - read/write

**Weak point:** wildcard authorization increases risk by expanding the reachable action space.

---

## Potential Hardening Extensions (Not Implemented)

The following are *architecturally feasible* but not currently enforced.

---

### A. Explicit Repository Whitelisting Only

- Eliminate wildcard authorization
- Require explicit enumeration of every allowed repository

Pros:
- Strong containment
- No accidental repo access

Cons:
- High operational friction
- Manual updates + redeploys

---

### B. Multiple Repo Bridge Instances

Run separate Repo Bridge services with distinct roles:

- Read-only bridge
- Read/write bridge
- Proposal-only / diff-only bridge

Each bridge:
- has its own GitHub App installation
- has its own token scope
- enforces non-representable actions by design

This enables **capability routing**.

---

### C. Token-Based Capability Segmentation

Use a single Repo Bridge instance but route agents via:

- different authentication tokens
- different permission scopes

This reduces infrastructure overhead but increases configuration complexity.

---

### D. Branch-Only Write Model

Restrict write-capable agents to:
- non-main branches only

Human controls:
- merge approval
- auto-merge rules
- manual review

This converts execution into **proposal by default**.

---

## Tradeoff Question (Unresolved)

The core open question is not *what is possible*, but:

> Which constraints materially reduce risk, and which merely add maintenance cost?

Additional layers only help if they:
- reduce reachable action space
- lower blast radius
- or simplify reasoning about failure modes

Security that increases complexity without shrinking capability surfaces may be net-negative.

---

## Status

- Descriptive, not prescriptive
- Not indexed
- Intended for comparison and future decision-making

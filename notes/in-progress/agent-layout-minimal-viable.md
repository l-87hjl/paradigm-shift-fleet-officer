# Minimal Viable Agent Layout (In Progress)

This note captures an exploratory design for a minimal, non-theatrical live-service agent layout.

It is **not** a finalized project or paradigm.
It is parked here to prevent premature formalization while preserving the reasoning.

---

## Core Principle

**Agents exist to hold pressure, not to simulate people.**

An agent earns its existence only if the activity it handles:
- is continuous rather than one-off
- benefits from persistence or memory
- requires isolation to reduce blast radius

Everything else should remain sequential and human-directed.

---

## Assumed Context

- Repo Bridge is the governance and capability boundary layer
- Agents are interchangeable compute routed through constrained envelopes
- Coordination is avoided unless strictly necessary

---

## Minimal Layout (Exploratory)

### 1. Operator Agent (Interactive)

**Purpose:** Execute explicitly requested work.

- On-demand only
- No background autonomy
- Handles concrete tasks (code, edits, changes)

**Repo Bridge:**
- Read/write on target repos
- No cross-repo destructive operations
- No permission escalation

---

### 2. Architect / Drift Watcher (Read-Only)

**Purpose:** Surface slow structural decay humans miss.

- Periodic scans
- Flags conceptual drift, redundancy, coupling
- Never writes code

**Repo Bridge:**
- Read-only across all repos
- Diff and metadata access only

---

### 3. Maintenance Sentinel (Scheduled, Narrow)

**Purpose:** Catch boring but dangerous issues early.

- Dependency updates
- Build breakage
- API deprecations

**Repo Bridge:**
- Write access limited to config, deps, CI
- No access to core logic

---

### 4. Change Auditor / Gatekeeper (Diff-Only)

**Purpose:** Reduce accidental scope expansion.

- Reviews proposed changes after execution
- Flags permission creep or cross-repo bleed
- Cannot initiate actions

**Repo Bridge:**
- Diff-only access
- No write or execution

---

## Explicit Exclusions

- No planner agent (humans plan; machines hallucinate confidence)
- No debating agents (wasteful where ground truth exists)
- No autonomous deployer
- No shared global agent memory

---

## Flow (Sequential, Non-Orchestrated)

1. Human → Operator Agent
2. Operator → Repo Bridge (RW)
3. Auditor Agent (check)
4. Maintenance Sentinel (scheduled)
5. Architect Agent (periodic)

No agent-to-agent chatter. No orchestration engine.

---

## Status

- Exploratory
- Not indexed
- Not safe to promote
- Exists to be pressure-tested and possibly discarded

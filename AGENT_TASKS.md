# AGENT TASKS — Paradigm-Shift Fleet Officer

This document defines the standing responsibilities and constraints for agents contributing to this repository.
It is intended to preserve structural clarity, prevent accidental actuation, and prepare the repository for sustained influx of paradigm-level project designs.

---

## Phase 1 — Structural Grounding (One-Time)

1. Re-read `README.md`, `TAGLINE.md`, and `LICENSE.md` before contributing.
2. Verify that all additions remain **design-only and non-actuating**.
3. Flag any file or folder that could be misinterpreted as executable or authoritative.

---

## Phase 2 — Folder Semantics (Always Enforced)

Each top-level folder answers exactly one question:

- `projects/` — What can a user check out and implement elsewhere?
- `schemas/` — What structures are canonical and machine-checkable?
- `paradigms/` — What worldview or coordination shifts are being articulated?
- `inter-repo-structures/` — How systems relate without merging repos.
- `templates/` — How new work should be added consistently.
- `notes/` — Provisional, unresolved, or exploratory thinking.

Overlap between folders is a design failure.

---

## Phase 3 — Project Intake Discipline

4. All new ideas land first in `notes/in-progress/`.
5. Promotion rules:
   - `notes/` → `projects/` only after scope and boundaries are explicit.
   - `notes/` → `paradigms/` only after invariants are articulated.
   - `schemas/` only after reuse across multiple projects is demonstrated.

---

## Phase 4 — Project Template Enforcement

6. All projects **must** be created using `projects/project-template/`.
7. Required files:
   - `README.md`
   - `INTENT.md`
   - `CHECKOUT.md`
8. Projects without these files are incomplete and should not be indexed.

---

## Phase 5 — Schema Hygiene

9. Schemas must be:
   - minimal
   - reusable
   - domain-agnostic
10. One-off schemas are not permitted.
11. Schema evolution must be versioned explicitly.

---

## Phase 6 — Paradigm Hygiene

12. Files in `paradigms/`:
   - must not contain step-by-step instructions
   - must not imply execution authority
   - should focus on invariants, reframings, and failure modes

---

## Phase 7 — Agent Constraints (Hard Rules)

13. Do not create executable code in this repository.
14. Do not wire this repository into actuation pipelines.
15. Do not imply permissions, authority, or governance.
16. When uncertain, restrict scope rather than expand it.

---

## Phase 8 — Maintenance

17. Periodically review for:
   - dead projects
   - duplicated paradigms
   - unclear folder boundaries
18. Move stale or superseded work to `notes/retired/`.

---

## Guiding Rule

> If a contribution makes it easier to act than to think, it does not belong here.

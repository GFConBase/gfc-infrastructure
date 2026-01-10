# GFC Infrastructure

This repository contains the core specifications and reference documentation for the German Foundation Coin (GFC) transparency infrastructure.

It follows a **spec-first approach**: intended behavior, constraints, and system boundaries are defined **before** any implementation.

---

## Purpose

The purpose of this repository is to serve as a **clear, verifiable, and long-term reference** for how the GFC infrastructure is designed to operate.

It documents **what the system is allowed to do**, **what it must do**, and **what it is explicitly constrained from doing**.

This repository exists to support:
- verifiable fund flows
- constrained and explicit governance
- long-term accountability and auditability

This is **not** a marketing surface and intentionally contains no promotional material.

---

## Scope

This repository focuses exclusively on **normative and pre-implementation definitions**, including:

- system architecture and trust boundaries
- presale mechanics and fund handling rules
- governance constraints and authority limits
- transparency models and verification principles
- explicit non-goals to prevent scope creep

It is intended for reviewers, auditors, contributors, and technically oriented stakeholders.

---

## Non-Goals

This repository explicitly does **not** aim to:

- host ad-hoc implementation experiments
- provide outcome promises or impact guarantees
- contain marketing narratives or growth-oriented messaging
- speculate about future features beyond documented specifications

Impact is measured through **verifiable execution**, not narrative intent.

---

## Specification Status

Specifications are published **prior to implementation** and evolve incrementally.

Each specification declares its own status:

- **Draft** — under refinement
- **Stable** — feature-complete, expected to be implemented as written
- **Normative** — binding system boundaries and constraints

Implementations and public statements **must not contradict** applicable *Stable* or *Normative* specifications.

---

## Canonical Specifications

The following documents form the **authoritative definition** of the GFC infrastructure:

- `specs/architecture.md` — **Normative**  
  Defines system boundaries, authority limits, trust assumptions, and fund flow constraints.

- `specs/presale.md` — **Stable**  
  Defines presale behavior, pricing logic, refund rules, and withdrawal constraints.

- `specs/governance-constraints.md`  
  Defines governance boundaries and limitations on discretionary control.

- `specs/transparency-model.md`  
  Defines how transparency is achieved through on-chain verifiability and documented off-chain processes.

- `specs/non-goals.md`  
  Defines intentional exclusions to prevent misaligned expectations and scope expansion.

- `specs/glossary.md`  
  Defines key terms used across all specifications.

---

## Single Source of Truth

The specifications in this repository represent the **single source of truth** for the intended behavior of the GFC infrastructure.

In case of ambiguity, precedence is as follows:

1. written specifications over UI behavior  
2. documentation over informal statements  
3. on-chain data over off-chain narratives  

---

## Implementation Status

At this stage, the repository primarily contains specifications.

Contract implementations and supporting infrastructure are expected to follow **only after** specification stabilization and review.

---

## Contribution Philosophy

Contributions are expected to respect the spec-first approach:

- specifications precede implementations
- constraints are preferred over discretion
- clarity is preferred over speed

Further contribution guidelines may be introduced as the repository evolves.

---

## License

Licensing information will be provided once implementation components are introduced.


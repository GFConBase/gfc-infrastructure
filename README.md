# GFC Infrastructure

This repository contains the core specifications and reference documentation for the **German Foundation Coin (GFC)** transparency infrastructure.

It follows a **spec-first approach**: intended behavior, constraints, and system boundaries are defined **before** implementation.

---

## Purpose

The purpose of this repository is to provide a **clear, verifiable, and long-term reference** for how the GFC infrastructure is designed to operate.

It focuses on:

- verifiable fund flows  
- constrained and explicit governance  
- long-term accountability and auditability  

This repository is **not** a marketing surface and does not contain promotional material.

---

## What This Repository Is / Is Not

### This repository **is**:
- a specification-first infrastructure repository  
- a source of normative and stable system definitions  
- a reference for reviewers, auditors, and contributors  

### This repository **is not**:
- a collection of ad-hoc implementation experiments  
- a promise of outcomes or impact guarantees  
- a place for speculative or marketing-driven narratives  

---

## Specification Status

Specifications in this repository are published prior to implementation and evolve incrementally.

Each specification declares its own status:

- **Draft** — under refinement  
- **Stable** — feature-complete, expected to be implemented as written  
- **Normative** — binding system boundaries and constraints  

Implementations and public statements **must not contradict** applicable Stable or Normative specifications.

---

## Canonical Specifications

The following documents form the core of the GFC infrastructure definition:

- **`specs/architecture.md`** — *Normative*  
  Defines system boundaries, authority limits, trust assumptions, and fund flow constraints.

- **`specs/presale.md`** — *Stable*  
  Defines presale behavior, pricing logic, refund rules, and withdrawal constraints.

- **`specs/governance-constraints.md`**  
  Defines governance boundaries and limitations on discretionary control.

- **`specs/transparency-model.md`**  
  Defines how transparency is achieved through on-chain verifiability and documented off-chain processes.

- **`specs/non-goals.md`**  
  Defines intentional exclusions to prevent misaligned expectations and scope creep.

- **`specs/glossary.md`**  
  Defines key terms used across all specifications.

---

## Single Source of Truth

The specifications in this repository represent the **single source of truth** for the intended behavior of the GFC infrastructure.

In case of ambiguity:
- written specifications take precedence over UI behavior,
- documentation takes precedence over informal statements,
- on-chain data takes precedence over off-chain narratives.

---

## Implementation Status

At this stage, the repository primarily contains specifications.

Contract implementations and supporting infrastructure are expected to follow **after** specification stabilization and review.

---

## Contribution Philosophy

Contributions are expected to respect the spec-first approach.

- Specifications precede implementations  
- Constraints are preferred over discretion  
- Clarity is preferred over speed  

Further contribution guidelines may be introduced as the repository evolves.

---

## License

Licensing information will be provided once implementation components are introduced.

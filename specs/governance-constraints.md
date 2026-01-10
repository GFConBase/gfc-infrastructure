# Governance Constraints
**Status:** Normative

This document defines governance-related constraints for the GFC infrastructure.

Rather than describing governance mechanisms, it focuses on **limitations, safeguards, and boundaries** intended to reduce discretionary risk.

## 1. Principle of Explicit Authority
Any entity or role with decision-making authority **must** be explicitly documented.

Implicit authority, undocumented control paths, or informal decision rights are considered out of scope and invalid within the GFC infrastructure.

## 2. Separation of Responsibilities
Operational execution, fund custody, and verification responsibilities **must not** be concentrated in a single role or entity.

Where full separation is not immediately feasible, transitional arrangements **must** be explicitly documented, including their scope and rationale.
Such arrangements are intended to be temporary and do not establish permanent governance patterns.

## 3. Limited Upgrade and Control Scope
Contracts and systems are designed to minimize the scope of unilateral changes.

Upgrade paths, if any, **must** be:
- explicitly defined,
- technically constrained,
- and publicly documented.

Undefined or implicit upgrade authority is not permitted.

## 4. Predictable Exception Handling
Exceptional actions (e.g. emergency interventions) are not treated as normal operations.

If exceptions are required:
- their scope **must** be limited,
- their execution **must** be documented,
- and their rationale **must** be publicly explained after the fact.

Exceptional actions do not create new standing authority and do not override existing governance constraints.

## 5. No Implicit Governance by Token Ownership
Token ownership alone does not grant governance authority over infrastructure, fund allocation, or operational decisions.

Governance powers, where applicable, **must** be defined explicitly and independently of token ownership.

## Status Notes
This document defines governance boundaries and constraints at a normative level.

Specific governance mechanisms may evolve, but must remain within the constraints described here.


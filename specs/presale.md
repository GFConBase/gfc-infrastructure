# Presale Specification
**Status:** Stable

## Purpose
This document defines the intended and binding behavior of the GFC presale prior to any contract implementation.

It serves as the authoritative reference for presale-related rules, constraints, and user-visible rules.
All implementations and public communications **must** remain consistent with this specification.

## Design Principles
The GFC presale is designed around the following principles:

### Fixed Pricing Logic
The GFC token price is fixed and defined by the presale design.

Any currency conversion (e.g. ETH, USDC, DAI) is handled at the frontend level for display and payment calculation purposes only.
Conversion logic does not affect the underlying fixed price definition.

### Instant Distribution on Purchase
GFC tokens are transferred to participants immediately at the time of purchase.

There is no delayed distribution phase and no post-sale claim mechanism.

### Softcap and Refund Behavior
The presale defines a softcap threshold that determines whether the presale is considered successful.

If the softcap is **not** reached by the end of the presale period, participants are entitled to a refund according to the documented refund logic.

If the softcap is reached at any point, the presale is considered successful.
From that moment onward, refund conditions **permanently cease to apply**, independent of any later events or timing considerations.

### Withdrawal Rules After Softcap
Collected presale funds may only be withdrawn once the softcap has been reached.

Withdrawals follow predefined, publicly documented, and rule-bound constraints.
They do not constitute discretionary governance decisions and do not grant authority beyond the presale scope.

The timing of a withdrawal after softcap is reached is not required to coincide with the presale end.
All withdrawals remain publicly traceable on-chain and are subject to post-action documentation.

### Transparent Handling of Unsold Tokens
Tokens allocated to the presale that remain unsold are handled according to a predefined and publicly documented distribution model.

The distribution of unsold tokens:
- is executed once,
- follows fixed rules,
- and is not subject to discretionary modification after execution.

## Scope and Constraints
This specification defines what **must** happen and what **must not** happen during the presale process.

It does not define:
- technical implementation details,
- user interface design,
- marketing or promotional strategies.

Such aspects may evolve independently, provided they do not contradict the behavior and constraints defined here.

## Status Notes
This specification is considered feature-complete.

Clarifications and non-breaking refinements may be applied.
Changes that alter pricing logic, refund behavior, withdrawal constraints, or unsold token handling are considered breaking and require explicit versioned updates.



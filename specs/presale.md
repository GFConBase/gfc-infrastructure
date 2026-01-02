# Presale Specification

Status: Stable

---

## Purpose

This document defines the intended and binding behavior of the GFC presale prior to any contract implementation.

It serves as the authoritative reference for presale-related rules, constraints, and user-visible guarantees.  
All implementations and public communications MUST remain consistent with this specification.

---

## Design Principles

The GFC presale is designed around the following principles:

### Fixed Pricing Logic

The GFC token price is fixed and defined by the presale design.

Any currency conversion (e.g. ETH, USDC, DAI) is handled at the frontend level for display purposes only.  
Conversion logic does not affect the underlying fixed price definition.

---

### Instant Distribution on Purchase

GFC tokens are transferred to participants immediately at the time of purchase.

There is no delayed distribution phase and no post-sale claim mechanism.

---

### Softcap and Refund Behavior

The presale defines a softcap threshold that determines whether the presale is considered successful.

- If the softcap is **not reached** by the end of the presale period, participants are entitled to a refund according to the documented refund logic.
- If the softcap **is reached at any point**, the presale is considered successful and refund conditions no longer apply.

---

### Withdrawal Rules After Softcap

Collected presale funds may only be withdrawn once the softcap has been reached.

Withdrawals follow predefined and publicly documented rules and are not discretionary.

The timing of a withdrawal after softcap is reached is not required to coincide with the presale end.

---

### Transparent Handling of Unsold Tokens

Tokens allocated to the presale that remain unsold are handled according to a predefined and transparent distribution model.

The handling of unsold tokens is not subject to discretionary decision-making and must follow documented rules.

---

## Scope and Constraints

This specification defines **what must happen** and **what must not happen** during the presale process.

It does not define:
- Technical implementation details
- User interface design
- Marketing or promotional strategies

Such aspects may evolve independently, provided they do not contradict the behavior and constraints defined here.

---

## Status Notes

This specification is considered feature-complete.

Clarifications and non-breaking refinements MAY be applied, but the core behavior, constraints, and guarantees defined in this document are not expected to change.


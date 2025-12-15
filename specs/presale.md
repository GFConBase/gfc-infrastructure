# Presale Specification

Status: Draft (spec-first)

## Goals

This document defines the intended behavior of the GFC presale
prior to any contract implementation.

The presale is designed around the following principles:

- **Fixed pricing logic**  
  The GFC token price is fixed. Any currency conversion
  (e.g. ETH, USDC, DAI) is handled at the frontend level
  for display purposes only.

- **Instant distribution on purchase**  
  GFC tokens are transferred to participants immediately
  at the time of purchase. There is no post-sale claim phase.

- **Softcap and refund behavior**  
  If the defined softcap is not reached by the end of the presale,
  participants are entitled to a refund according to the
  documented refund logic.

- **Withdrawal rules after softcap**  
  Once the softcap is reached, collected funds may be withdrawn
  following predefined and publicly documented rules.

- **Transparent handling of unsold tokens**  
  Any unsold tokens are handled according to a predefined
  and transparent distribution model.

## Notes

This specification describes intent and high-level behavior.
Technical implementation details will be documented and reviewed
prior to deployment.

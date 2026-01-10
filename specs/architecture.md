# GFC Architecture Specification
**Status:** Normative

## 1. Purpose and Scope
This document defines the high-level architecture of the GFC infrastructure.

Its purpose is not to describe technical implementation details, but to make **system boundaries**, **authority limits**, and **trust assumptions** explicit.

It answers the following questions:
- Which components exist?
- What is each component responsible for?
- Where does authority begin and end?
- Which actions are intentionally not automated?
- How on-chain and off-chain processes interact without ambiguity

This document is **normative** and applies to all current and future implementations of the GFC infrastructure.
All other specifications and implementations must remain consistent with the constraints defined here.

## 2. Architectural Principles
The GFC architecture follows these principles:
- Explicit authority over implicit power
- Constraints over discretion
- Verifiability over convenience
- Documentation over narratives
- Bounded automation with preserved human responsibility

These principles are foundational and must be reflected across the specification set, including:
- `governance-constraints.md`
- `non-goals.md`
- `transparency-model.md`
- `presale.md`

## 3. System Components

### 3.1 GFC Token Contract
- Represents the GFC token.
- Defines total supply and transfer rules.
- Does not encode governance, charity decisions, or fund allocation logic.
- The token contract is not treated as a governance instrument.

### 3.2 Presale Contract
- Accepts predefined assets under fixed pricing logic.
- Distributes GFC tokens instantly upon purchase.
- Enforces softcap and refund behavior as defined in `presale.md`.
- Does not autonomously decide fund usage.

Once the softcap is reached, the contract allows withdrawals according to predefined rules.
Withdrawals are a **mechanism** with constrained authority, not a discretionary governance function.
All withdrawals remain publicly traceable on-chain and are subject to post-action documentation in the transparency process.

### 3.3 Lock and Vesting Contracts
- Enforce long-term constraints on token availability.
- Are designed to prevent unilateral early release.
- May allow extension of lock periods, but not reduction.
- These contracts exist to encode commitments, not to optimize liquidity or flexibility.

### 3.4 Charity and Foundation Wallets
- Publicly known addresses with defined roles.
- May be single-signature or multi-signature, depending on context.
- Do not receive discretionary authority beyond what is explicitly documented.
- Wallet ownership alone does not imply governance authority.

### 3.5 Transparency Portal (Read-Only Layer)
- Aggregates publicly verifiable on-chain data.
- Documents off-chain decisions and processes.
- Does not execute transactions or influence on-chain state.
- The portal is informational and has no control authority.

## 4. Trust and Authority Boundaries

### 4.1 On-Chain vs. Off-Chain Authority
- On-chain components enforce hard constraints and verifiable rules.
- Off-chain processes handle decisions that require context, judgment, or coordination.

Off-chain authority is constrained by:
- prior written specifications,
- post-action documentation,
- and public traceability.

### 4.2 Admin, Multisig, and UI Boundaries
- Administrative roles are limited in scope and explicitly documented.
- Multisig wallets require multiple approvals and are used to reduce unilateral control.
- User interfaces have no privileged authority and cannot bypass on-chain rules.
- The UI is not a source of truth.

## 5. Fund Flow Boundaries

### 5.1 Automated Fund Flows
The architecture allows automation where predictability and safety are improved, including:
- token distribution at purchase,
- time-based vesting enforcement,
- refund execution when predefined conditions apply.

### 5.2 Non-Automated Fund Flows
Certain actions are intentionally not automated, including:
- discretionary fund allocation decisions,
- timing of withdrawals after softcap,
- charity or foundation disbursements.

These actions require explicit human decisions and subsequent documentation.
Automation is not used to obscure responsibility.

## 6. Immutability and Change Rules
- Core behavioral rules are defined in Stable or Normative specifications.
- Implementations must conform to those specifications.
- Changes to core rules require versioned specification updates.

**Non-breaking clarifications** may occur, meaning wording/structure improvements that do not change:
- permissions or authorities,
- thresholds or timing constraints,
- fund flow rules,
- enforcement boundaries.

**Breaking changes** are exceptional and must be explicitly documented as such.

## 7. System Overview Diagram
+--------------------+
|   Transparency     |
|      Portal        |
|  (Read-only view)  |
+---------+----------+
          |
          v
+---------+----------+
|   Public Records   |
| (Specs / Logs /    |
|  On-chain data)    |
+---------+----------+

          ^
          |
+---------+----------+
|  Off-chain Actions |
| (Governance /      |
|  Decisions)        |
+---------+----------+

          ^
          |
+---------+----------+
| On-chain Contracts |
|-------------------|
| Token             |
| Presale           |
| Vesting / Locks   |
+-------------------+

## 8. Non-Goals (Architectural)
This architecture does not aim to:
- fully automate governance,
- eliminate human responsibility,
- optimize for short-term token dynamics,
- replace trust with narratives.

Its purpose is to **bound trust**, not to deny its necessity.

## Status Notes
This document defines architectural boundaries and is considered normative.

Implementations may evolve, but must remain within the constraints defined here.




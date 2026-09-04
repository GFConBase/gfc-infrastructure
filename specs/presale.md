# Global Foundation Coin Presale Specification

**Document ID:** GFC-PRE-001  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Intended Production Network:** Base Mainnet  
**Production Chain ID:** 8453  
**Public Pilot Network:** Base Sepolia  
**Pilot Chain ID:** 84532  
**Last Updated:** 2026-09-04

---

## 1. Document Status

This document defines the current intended behavior, participant protections, economic constraints, authority boundaries, and transparency requirements for the planned Global Foundation Coin (GFC) presale.

It is normative because it defines intended requirements and prohibited behavior.

Its maturity remains Draft.

At the current repository state:

- the **GFC Token / Economic Layer** is the current primary product focus;
- no GFC presale is live;
- no production presale contract is deployed;
- no production presale address is established as official;
- no public presale launch date is established by this document;
- the current Draft design intends to support **ETH, USDC, and DAI on Base**;
- exact production payment-asset identifiers and implementation details remain subject to authentication before launch;
- no production pricing implementation is finalized;
- no production refund mechanism is finalized;
- no production withdrawal destination is established as official;
- no production presale authority is established as official by this document;
- no production presale security audit is represented as completed;
- and no production presale implementation is designated as conforming.

The current Draft design direction uses **immediate GFC distribution**.

The current Draft design also requires refunds where the applicable soft-cap success condition is not satisfied.

The exact technically enforceable relationship between:

- GFC already distributed to a participant; and
- the participant's refund right after failed finalization

remains unresolved.

A production presale MUST NOT activate while that interaction remains undefined.

This document does not constitute an offer, invitation, confirmation of availability, or proof that participation is currently possible.

Current implementation and deployment status is maintained in [`../STATUS.md`](../STATUS.md).

---

## 2. Purpose

The purpose of this specification is to define a presale model that is:

- finite;
- deterministic;
- participant-protective;
- economically reconcilable;
- authority-bounded;
- security-reviewable;
- and accurately represented.

The specification is intended to establish:

- a fixed GFC reference price;
- a finite Presale allocation;
- supported payment-asset requirements;
- deterministic purchase accounting;
- immediate token distribution as the current design direction;
- clear success and failure conditions;
- protected refund rights;
- controlled contribution custody;
- constrained administrative authority;
- predictable finalization;
- predefined unsold-token treatment;
- transparent status reporting;
- and linkage to the wider GFC accountability model.

The presale MUST NOT rely on frontend behavior alone where participant-facing financial rules require technical enforcement.

---

## 3. Relationship to the GFC Accountability Model

The long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

The presale directly involves each stage.

### Funds

What payment assets were contributed, what GFC was distributed, what assets remain refundable, and what assets later become valid proceeds?

### Authority

Who may configure, activate, pause, finalize, withdraw, migrate, or otherwise influence the presale?

### Rules

What price, duration, soft cap, allocation ceiling, payment assets, distribution rules, refund rights, and withdrawal conditions apply?

### Decisions

Which authorized actions activate, pause, cancel, finalize, migrate, or withdraw?

### Outcomes

What GFC was distributed, what contributions were accepted, whether the soft cap was reached, and whether finalization succeeded or failed?

### Evidence

What on-chain records, deployment records, pricing records, accounting records, and public status records support those claims?

A purchase transaction does not by itself prove:

- successful finalization;
- unrestricted project ownership of the contribution;
- liquidity;
- future market value;
- project completion;
- or impact.

---

## 4. Relationship to Other Specifications

This document MUST be interpreted together with:

- [`README.md`](README.md);
- [`glossary.md`](glossary.md);
- [`non-goals.md`](non-goals.md);
- [`architecture.md`](architecture.md);
- [`roles-and-authority.md`](roles-and-authority.md);
- [`governance-constraints.md`](governance-constraints.md);
- [`security-model.md`](security-model.md);
- [`token.md`](token.md);
- [`allocations.md`](allocations.md);
- [`vesting-and-unlocks.md`](vesting-and-unlocks.md);
- [`economic-flows.md`](economic-flows.md);
- [`staking.md`](staking.md);
- [`transparency-model.md`](transparency-model.md);
- [`conformance-verification.md`](conformance-verification.md);
- repository-level [`../STATUS.md`](../STATUS.md);
- and repository-level [`../SECURITY.md`](../SECURITY.md).

Where another Draft specification conflicts with this document, the conflict MUST be resolved explicitly before Stable status and before production activation.

---

## 5. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are normative only when:

- they appear in uppercase;
- the containing document declares `Authority: Normative`;
- and the applicable version governs the implementation, process, or communication being evaluated.

Because this document is Draft, these requirements remain subject to formal review and versioned release.

---

## 6. Scope

This specification covers:

- Presale allocation;
- reference price;
- sale duration;
- supported payment assets;
- contribution valuation;
- purchase accounting;
- immediate GFC distribution;
- allocation exhaustion;
- soft-cap accounting;
- contribution custody;
- finalization;
- successful-sale proceeds;
- failed-sale refunds;
- cancellation;
- pause behavior;
- unsold GFC;
- presale authority;
- immutability and configuration boundaries;
- migration;
- participant-facing disclosures;
- public records;
- privacy boundaries;
- security requirements;
- monitoring;
- incident handling;
- conformance;
- and unresolved pre-launch decisions.

---

## 7. Out of Scope

This document does not independently define:

- final legal participation terms;
- final jurisdiction-specific eligibility;
- final identity-verification requirements;
- final sanctions controls;
- tax treatment;
- accounting treatment;
- securities or financial-instrument classification;
- final production contract source code;
- final production contract addresses;
- exact production USDC and DAI contract addresses;
- final pricing provider or oracle architecture;
- final user-interface design;
- final marketing strategy;
- exchange listing;
- market price after the presale;
- guaranteed liquidity;
- guaranteed token value;
- guaranteed return;
- or guaranteed project impact.

These matters require separate legal, technical, operational, or authenticated production records before production reliance.

---

## 8. Presale Principles

### 8.1 Contract-enforced material rules

Material participant rights and financial constraints MUST be enforced by the presale contract or another equally verifiable settlement mechanism.

A frontend MUST NOT be the sole enforcement layer for:

- price;
- allocation ceiling;
- contribution acceptance;
- participant accounting;
- GFC distribution;
- soft-cap accounting;
- refund rights;
- or proceeds-withdrawal conditions.

### 8.2 Participant protection before unrestricted project access

Accepted contribution assets MUST remain unavailable for unrestricted project use while valid refund rights require those assets to remain available.

### 8.3 No token creation through presale

The presale MUST distribute GFC only from the predefined Presale allocation.

The presale MUST NOT mint additional GFC.

### 8.4 Deterministic accounting

Every accepted contribution MUST produce deterministic and reviewable accounting.

### 8.5 Immediate distribution as current design direction

The current Draft design direction is to distribute the purchased GFC amount immediately as part of, or immediately following, a valid purchase.

### 8.6 Refund integrity

If the applicable success condition is not satisfied, valid refund rights MUST remain enforceable according to the finalized production rules.

### 8.7 No retrospective rule rewriting

Presale rules MUST NOT be changed after activation merely because actual sale results differ from expectations.

### 8.8 Accurate status communication

Public communication MUST accurately distinguish between Draft, Planned, Configured, Active, Paused, Ended, Successful, Failed, Refunding, Completed, and other applicable states.

---

## 9. Current Intended Parameters

The current Draft presale parameters are:

| Parameter | Current Draft Value |
|---|---:|
| GFC reference price | €0.05 per GFC |
| Intended duration | 8 weeks |
| Soft cap | €250,000 reference value |
| Presale allocation | 150,000,000 GFC |
| Allocation percentage | 15% of total GFC supply |
| Separate monetary hard cap | None |
| Maximum GFC distribution | 150,000,000 GFC |
| Maximum gross reference value at full allocation | €7,500,000 |
| Intended payment assets | ETH, USDC, DAI on Base |
| Current token-delivery direction | Immediate distribution |
| Failure condition | Applicable soft-cap success condition not satisfied |
| Failed-sale participant protection | Refund right |
| Additional inflation through presale | Prohibited |
| Current material-logic direction | Immutable after production deployment |

These values are Draft specification parameters.

They MUST NOT be represented as evidence that a production presale is deployed or active.

The absence of a separate monetary hard cap MUST NOT be communicated as unlimited fundraising capacity.

The finite Presale allocation creates an absolute GFC distribution ceiling.

---

## 10. Presale Allocation

The Presale allocation is:

```text
150,000,000 GFC
```

representing:

```text
15% of the fixed total supply of 1,000,000,000 GFC
```

The presale MUST NOT distribute more than:

```text
150,000,000 GFC
```

The presale MUST NOT:

- mint additional GFC;
- borrow GFC from another allocation without an applicable breaking specification change;
- create duplicate participant entitlement;
- or create an undocumented replacement claim.

Presale allocation rules MUST remain consistent with [`allocations.md`](allocations.md).

---

## 11. Presale Funding

Before production activation, the presale mechanism MUST have verifiable access to the GFC required to satisfy valid purchase distribution.

The implementation MUST NOT accept a contribution for GFC that it cannot distribute according to the applicable transaction rules.

The final technical funding model remains unresolved.

Possible implementation structures MAY include:

- pre-funded presale contract;
- tightly constrained distribution contract;
- or another explicitly specified mechanism.

Any privileged funding or transfer authority MUST be disclosed.

---

## 12. Reference Price

The current intended reference price is:

```text
€0.05 per GFC
```

The production presale MUST enforce the applicable reference price through the settlement mechanism.

The reference price MUST NOT be presented as:

- fair market value;
- future market value;
- a future price floor;
- guaranteed appreciation;
- or guaranteed liquidity.

The current design direction is that the reference price remains fixed throughout the active presale.

A production system MUST NOT permit an undocumented administrator to alter the price after activation.

---

## 13. Intended Payment Assets

The current Draft design intends to support:

- **ETH**
- **USDC**
- **DAI**

on Base.

Before production activation, the applicable release MUST authenticate:

- network;
- payment-asset type;
- exact token contract address where applicable;
- decimals;
- accepted transfer behavior;
- pricing methodology;
- and refund treatment.

A symbol alone is insufficient to authenticate a supported token.

A token with the same symbol on another network or at another contract address MUST NOT be accepted solely by name.

---

## 14. Native ETH

If native ETH is accepted, the production implementation MUST define:

- how ETH contributions are received;
- how euro-reference valuation is calculated;
- handling of excess native value where applicable;
- refund behavior;
- reentrancy protections;
- and transfer-failure behavior.

Native ETH acceptance MUST remain reconcilable with participant accounting.

---

## 15. USDC and DAI

If USDC and DAI are accepted as intended, the production implementation MUST authenticate the exact Base contract addresses and expected token behavior.

The implementation MUST account for:

- token decimals;
- transfer return behavior;
- allowance handling;
- transfer failure;
- and any relevant non-standard behavior.

The production presale SHOULD NOT rely on symbol matching.

---

## 16. Payment-Asset Conversion

Where payment assets require conversion to the euro-denominated reference value, the conversion MUST be enforced by the contract or another verifiable settlement mechanism.

Frontend-only conversion is prohibited.

For each supported payment asset, the production implementation MUST define:

- pricing source;
- asset identifier;
- reference currency;
- conversion direction;
- update method;
- maximum price age;
- decimals;
- rounding;
- invalid-price behavior;
- stale-price behavior;
- unavailable-price behavior;
- and any fallback behavior.

The final production pricing architecture remains unresolved.

---

## 17. Purchase-Time Reference Value

The euro reference value assigned when a valid contribution is accepted MUST be deterministically recorded or derivable.

The purchase-time reference value is intended to determine:

- applicable GFC amount;
- soft-cap accounting;
- participant purchase record;
- and public presale accounting.

Later market-price movements MUST NOT retroactively change the GFC amount distributed for a completed valid purchase unless the finalized specification explicitly defines a correction for an invalid transaction.

---

## 18. Pricing Failure

A purchase MUST fail safely where required pricing information is:

- unavailable;
- stale;
- invalid;
- zero;
- negative;
- outside defined safety limits;
- or otherwise unusable under the production rules.

The presale MUST NOT silently substitute an undocumented conversion rate.

---

## 19. Rounding and Precision

The production implementation MUST define rounding at every material conversion stage.

At minimum:

- GFC distribution MUST NOT exceed the amount supported by the accepted purchase reference value;
- Presale distribution MUST NOT exceed the remaining Presale allocation;
- decimal conversions MUST be deterministic;
- rounding MUST be reproducible off-chain;
- and material excess contribution value MUST be rejected, reverted, or otherwise handled according to a predefined rule.

The applicable formulas and test vectors MUST be published before production activation.

---

## 20. Presale Duration

The current intended presale duration is:

```text
8 weeks
```

No public start date is established by this document.

Before production activation, the authenticated release MUST identify:

- exact start timestamp;
- exact end timestamp;
- human-readable presentation;
- applicable timezone for human communication;
- contract timestamp semantics;
- and activation conditions.

The production contract-level state is authoritative for execution.

---

## 21. Activation Requirements

The presale MUST NOT become production-active until all material activation prerequisites are satisfied.

At minimum, before activation:

- the production presale implementation MUST exist;
- production network and addresses MUST be authenticated;
- the applicable versioned presale specification MUST be published;
- the production GFC token MUST be authenticated;
- Presale allocation funding or distribution capacity MUST be verified;
- intended payment assets MUST be authenticated;
- pricing behavior MUST be finalized;
- purchase accounting MUST be finalized;
- immediate-distribution behavior MUST be finalized;
- failed-finalization refund treatment MUST be finalized;
- contribution custody MUST be finalized;
- withdrawal conditions MUST be finalized;
- unsold-GFC treatment MUST be finalized;
- privileged roles MUST be defined;
- authority registry entries MUST be prepared;
- security requirements MUST be satisfied;
- and applicable legal and operational prerequisites MUST be addressed.

The unresolved interaction between immediate GFC distribution and failed-sale refunds is an activation blocker.

---

## 22. Presale State Model

The production presale MUST use explicit and externally reviewable states.

The final exact state machine remains implementation-dependent, but the model SHOULD distinguish at least:

### 22.1 Configured

The system is deployed or prepared but does not accept purchases.

### 22.2 Active

Valid purchases may be accepted.

### 22.3 Paused

Defined functions are temporarily restricted under a specified safety condition.

### 22.4 Ended

The configured sale period has ended and new purchases are no longer accepted.

### 22.5 Successful

Applicable success conditions have been satisfied and successful finalization has occurred.

### 22.6 Failed

Applicable success conditions were not satisfied or a refundable cancellation has resulted in failure.

### 22.7 Refunding

Valid participants may exercise applicable refund rights.

### 22.8 Completed

The active sale process is complete while historical records and any continuing participant rights remain preserved.

Because the current design direction uses immediate distribution, a separate post-success `Claiming` state is not part of the current intended model unless a later versioned specification explicitly reintroduces claim-based delivery.

---

## 23. Purchase Eligibility

Final legal and operational purchase eligibility remains unresolved.

The production model MUST define, where applicable:

- eligible jurisdictions;
- prohibited jurisdictions;
- age requirements;
- sanctions restrictions;
- identity requirements;
- wallet requirements;
- participant representations;
- and applicable legal terms.

Technical contract execution MUST NOT be represented as independently resolving all legal eligibility requirements.

If an allowlist or credential mechanism is used, its authority, privacy implications, revocation rules, and failure behavior MUST be specified.

---

## 24. Valid Purchase

A valid purchase MUST:

1. occur while purchases are permitted;
2. use a supported authenticated payment asset;
3. use valid pricing information where conversion is required;
4. satisfy applicable eligibility requirements;
5. satisfy any finalized minimum or maximum contribution rules;
6. remain within the remaining Presale allocation;
7. produce deterministic participant accounting;
8. account for the accepted contribution;
9. account for the applicable GFC amount;
10. distribute GFC according to the immediate-distribution rule;
11. update soft-cap accounting;
12. and emit or otherwise create publicly reviewable transaction evidence.

No sensitive personal information SHOULD be emitted on-chain.

---

## 25. Immediate GFC Distribution

The current Draft token-delivery direction is **immediate distribution**.

For a valid purchase, the production economic flow is intended to include:

1. acceptance of the payment asset;
2. purchase-time reference valuation;
3. GFC amount calculation;
4. purchase accounting;
5. immediate transfer of the applicable GFC amount to the participant;
6. reduction of remaining Presale distribution capacity;
7. update of soft-cap accounting;
8. and creation of reviewable transaction records.

The exact atomicity and technical ordering remain implementation decisions.

A production implementation MUST ensure that failure in a required part of the purchase flow does not leave inconsistent participant accounting.

---

## 26. No Deferred Claim as Current Model

Deferred post-success claiming is **not** the current intended GFC presale delivery model.

The current model MUST NOT describe purchased GFC as merely claimable after successful finalization unless the applicable specification is changed through a versioned process before production activation.

The following legacy design statements are therefore not current:

- purchased GFC becomes claimable only after successful finalization;
- no token transfer occurs during the active sale;
- a successful sale activates the initial delivery of purchased GFC.

Historical documents MAY retain such wording for archival accuracy but current technical specifications MUST use the immediate-distribution model.

---

## 27. Presale Vesting

The current Draft does not establish an additional vesting schedule for GFC purchased in the presale.

Under the current design direction, valid purchased GFC is intended to be distributed immediately.

Any future presale vesting, lock, delayed claim, or delayed transfer model would constitute a material change and MUST be specified before production activation.

---

## 28. Allocation Exhaustion

A purchase that would exceed the remaining Presale allocation MUST use predefined behavior.

The final production choice between:

- full transaction reversion; or
- deterministic partial fill

remains unresolved.

If partial fill is used, the implementation MUST define:

- accepted contribution portion;
- excess contribution treatment;
- rounding;
- GFC distribution;
- accounting;
- and failure behavior.

Silent retention of excess payment is prohibited.

---

## 29. Purchase Accounting

Every accepted purchase MUST be reconcilable to:

- participant address;
- payment asset;
- accepted payment amount;
- purchase-time euro reference value;
- GFC amount distributed;
- transaction identifier;
- timestamp;
- cumulative GFC distributed;
- cumulative soft-cap reference value;
- and remaining Presale allocation.

The implementation MUST prevent:

- duplicate purchase accounting;
- distribution without corresponding accepted contribution;
- accepted contribution without corresponding valid distribution unless the transaction fails atomically or a specifically defined exception applies;
- and distribution exceeding remaining allocation.

---

## 30. Presale Allocation Reconciliation

The production accounting SHOULD satisfy:

```text
150,000,000 GFC
=
GFC distributed
+
remaining Presale GFC
+
any explicitly specified exceptional state
```

Any exceptional state MUST be predefined.

It MUST NOT create duplicate entitlement or additional canonical supply.

---

## 31. Soft Cap

The current intended soft cap is:

```text
€250,000 reference value
```

The final production implementation MUST define exactly which accepted contributions count toward the soft cap.

Soft-cap accounting MUST be deterministic and reviewable.

Rejected or reverted transactions MUST NOT count.

Treatment of refunded contributions in final accounting MUST be explicitly specified.

---

## 32. Reaching the Soft Cap

Reaching the soft cap during the active sale means that the quantitative threshold has been reached under the current accounting.

It does not by itself mean:

- the presale has ended;
- successful finalization has occurred;
- contribution assets have become unrestricted project proceeds;
- all participant refund rights have ended;
- or all legal or operational conditions have been satisfied.

---

## 33. No Separate Monetary Hard Cap

The current Draft design has no separate monetary hard cap.

However:

- GFC reference price is fixed under the current design;
- Presale distribution is limited to 150,000,000 GFC;
- and the sale therefore has finite token-distribution capacity.

At the current €0.05 reference price, full Presale allocation corresponds to:

```text
€7,500,000
```

gross reference value.

This calculation is not a fundraising guarantee.

---

## 34. Contribution Custody

Accepted payment assets remain subject to the applicable success, finalization, refund, and withdrawal rules.

The exact production custody architecture remains unresolved.

The production model MUST define:

- where accepted ETH is held;
- where accepted USDC is held;
- where accepted DAI is held;
- who has technical authority over those assets;
- whether any escrow or segregated custody mechanism is used;
- how refund availability is protected;
- and when assets become withdrawable as valid proceeds.

Project operators MUST NOT have unrestricted access to assets required to satisfy valid refund rights.

---

## 35. Contribution-Asset Preservation

Assets subject to potential refund obligations MUST NOT be exposed to avoidable risk that could prevent valid refunds.

Before successful finalization or another explicitly specified release condition, refundable assets MUST NOT be used for:

- development expenditure;
- marketing expenditure;
- liquidity deployment;
- staking;
- lending;
- speculative trading;
- pledging;
- or other discretionary project use.

---

## 36. Finalization

The production model MUST define deterministic finalization.

Finalization MUST NOT rely indefinitely on discretionary project action where objective conditions can be evaluated automatically.

The final implementation MUST define:

- earliest finalization time;
- success condition;
- failure condition;
- authorized or permissionless caller;
- state transitions;
- contribution-asset implications;
- refund implications;
- unsold-GFC implications;
- and emitted records.

---

## 37. Successful Finalization

Successful finalization MUST confirm that all applicable success conditions have been satisfied.

At minimum, the final model MUST address:

- sale end;
- soft-cap status;
- any unresolved cancellation state;
- contribution accounting;
- GFC distribution accounting;
- proceeds-withdrawal eligibility;
- and unsold-GFC treatment.

Because GFC is distributed immediately under the current design direction, successful finalization does not create the initial participant token delivery.

It instead resolves the final sale status and applicable contribution-proceeds rights.

---

## 38. Failed Finalization

Failed finalization MUST:

- prevent further purchases;
- preserve participant accounting;
- establish applicable refund rights;
- preserve sufficient contribution assets for valid refunds;
- define unsold-GFC status;
- and produce reviewable failure records.

Failed finalization MUST NOT permit project operators to redirect refundable contribution assets to another purpose.

---

## 39. Immediate Distribution and Refund Invariant

The current Draft contains two required design directions:

1. valid purchased GFC is distributed immediately; and
2. participants receive refunds if the applicable soft-cap success condition is not satisfied.

This combination creates a critical unresolved economic and security question.

Before production activation, the final presale specification and implementation MUST define the treatment of GFC already distributed to a participant if finalization fails.

The final solution MUST be:

- technically enforceable;
- economically reconcilable;
- compatible with participant rights;
- compatible with fixed supply;
- compatible with the Presale allocation ceiling;
- disclosed before participation;
- and tested before production activation.

This Draft does not select or authorize any particular mechanism.

In particular, it does not currently authorize:

- clawback;
- forced token transfer;
- administrator seizure;
- forced burn;
- mandatory participant token return;
- token invalidation;
- blacklist-based immobilization;
- negative balance;
- replacement token;
- or another equivalent mechanism.

A production presale MUST NOT activate while this matter remains unresolved.

---

## 40. Refund Rights

If the final presale rules create a refund right, that right MUST be enforceable.

The current Draft requires a refund where the applicable soft-cap success condition is not satisfied.

The final production rule MUST define:

- eligible participant;
- refundable contribution;
- refundable payment asset;
- refund amount;
- initiation mechanism;
- timing;
- accounting;
- interaction with distributed GFC;
- and continuing rights after migration or deprecation.

---

## 41. Refund Asset

The current intended refund model SHOULD preserve the participant's original accepted payment asset unless a later versioned specification defines another participant-protective rule.

The production model MUST define refund treatment separately for:

- ETH;
- USDC;
- DAI;
- and any future permitted asset.

The project MUST NOT silently substitute a different asset merely for operational convenience.

---

## 42. Refund Amount

The production refund calculation MUST be deterministic.

The final model MUST define whether the refundable amount is exactly the accepted contribution amount or another explicitly specified amount.

Any deduction from a valid refund MUST be defined before activation and must not be hidden.

Project operating expenses MUST NOT be deducted from refundable participant assets merely because the presale failed.

---

## 43. Refund Mechanism

The exact production refund implementation remains unresolved.

A pull-based participant-initiated refund MAY be used where technically appropriate.

If a pull model is used, the implementation MUST protect against:

- double refunds;
- unauthorized refunds;
- incorrect recipient;
- reentrancy;
- asset mismatch;
- accounting divergence;
- and exhaustion of required refund assets.

No refund architecture is established as final by this Draft.

---

## 44. Refund Availability

A valid refund right SHOULD NOT disappear solely because a participant does not exercise it immediately unless the applicable legal and technical framework establishes an explicit, justified, participant-disclosed limitation.

If migration is required, unresolved refund rights MUST be preserved through the successor process.

---

## 45. Successful-Sale Proceeds

Accepted contribution assets MUST NOT become unrestricted project proceeds until the applicable successful-finalization and withdrawal rules permit it.

The final production specification MUST define:

- when proceeds become withdrawable;
- which assets are withdrawable;
- authorized withdrawal role;
- approval requirements;
- destination;
- partial versus full withdrawal;
- and public records.

This document does not establish a production proceeds destination.

---

## 46. Withdrawal Destination

No production withdrawal destination is established by this Draft.

Before activation, the applicable release MUST authenticate any destination permitted to receive successful presale proceeds.

An administrator MUST NOT be able to redirect proceeds to an arbitrary undisclosed address after participant contributions have been accepted.

---

## 47. Use of Proceeds

The detailed intended-use framework for successful presale proceeds remains outside the finalized scope of this Draft unless separately defined.

Before launch, public communication SHOULD explain the applicable intended-use framework without representing intended use as completed use.

Actual use requires:

- transaction evidence;
- authority;
- purpose;
- supporting documentation;
- reconciliation;
- and appropriate transparency status.

Successful fundraising does not itself establish successful execution or impact.

---

## 48. Cancellation

### 48.1 Pre-activation cancellation

The presale MAY be cancelled before activation.

If no contribution has been accepted, such cancellation does not create contribution refund obligations.

### 48.2 Post-activation cancellation

Any post-activation cancellation authority MUST be defined before launch.

Qualifying reasons MAY include:

- critical security vulnerability;
- compromised authority;
- material legal prohibition;
- unrecoverable pricing failure;
- or another predefined severe condition.

### 48.3 Refund consequences

A refundable post-activation cancellation MUST preserve the applicable refund rights.

### 48.4 Distributed-GFC consequence

Because the current design uses immediate distribution, the final specification MUST also define how post-activation cancellation affects GFC already distributed.

This interaction is part of the unresolved immediate-distribution/refund problem and MUST NOT be improvised after launch.

---

## 49. Pause Functionality

Pause functionality MAY exist only where justified.

The final production model MUST define:

- functions affected;
- functions unaffected;
- authorized role;
- activation condition;
- unpause condition;
- effect on sale duration;
- effect on refunds;
- effect on contribution custody;
- and effect on participant accounting.

A pause MUST NOT silently:

- change price;
- erase purchase records;
- remove refund rights;
- redirect assets;
- increase Presale allocation;
- or authorize new GFC minting.

---

## 50. Sale-Duration Effects of Pause

Whether a pause extends the eight-week sale duration remains unresolved.

The production rule MUST be finalized before activation.

A pause MUST NOT silently extend the sale.

Any extension model MUST define:

- qualifying pause;
- extension calculation;
- maximum extension;
- authority;
- public notice;
- and contract-level enforcement.

---

## 51. Administrative Authority

Any production presale authority MUST be consistent with [`roles-and-authority.md`](roles-and-authority.md).

Potential functional authorities MAY include:

- pre-activation configuration;
- activation;
- pause;
- cancellation;
- finalization;
- proceeds withdrawal;
- pricing-source administration;
- supported-asset administration;
- migration;
- and recovery.

Not every role need exist.

Every actual material role MUST be:

- explicit;
- narrowly scoped;
- technically identifiable;
- authenticated;
- included in the authority registry;
- and subject to defined revocation or replacement.

No undocumented material presale authority is permitted.

---

## 52. Immutability Direction

The current presale design direction is that **material participant-facing sale logic is immutable after production deployment**.

At minimum, the final production architecture SHOULD prevent privileged modification of:

- GFC reference price;
- Presale allocation ceiling;
- soft cap;
- participant accounting rules;
- immediate-distribution rules;
- refund rights;
- finalization rules;
- and successful-proceeds withdrawal conditions.

If any of these remain configurable, the presale MUST NOT be described as fully immutable.

---

## 53. Pre-Activation Configuration

A deployment MAY require pre-activation configuration.

Any configurable pre-activation parameters MUST be finalized and publicly authenticated before the first accepted purchase.

After activation, material parameters MUST NOT remain silently mutable.

---

## 54. Supported-Asset Changes

The final production model MUST define whether the supported payment-asset set can change after activation.

The current design SHOULD minimize post-activation mutability.

If emergency disabling of a compromised asset is permitted:

- previously accepted contributions MUST remain accounted for;
- participant refund rights MUST remain preserved;
- historical support status MUST remain reviewable;
- and disabling MUST NOT alter the treatment of unrelated supported assets.

---

## 55. Pricing-Source Changes

If the pricing mechanism permits source replacement, the authority and conditions MUST be explicitly defined.

A pricing-source change MUST NOT be used to manipulate participant value.

The production model MUST define:

- trigger;
- authority;
- approval;
- delay where applicable;
- validation;
- public notice;
- and historical record.

---

## 56. Migration

Migration MAY be required only under a separately defined process.

A migration MUST preserve or explicitly resolve:

- accepted contribution records;
- GFC distribution records;
- remaining Presale allocation;
- soft-cap accounting;
- refund rights;
- contribution-asset custody;
- unsold-GFC status;
- and historical transaction linkage.

Migration MUST NOT:

- create duplicate GFC claims;
- create duplicate refund claims;
- increase Presale distribution capacity;
- erase participant rights;
- or weaken accounting integrity.

---

## 57. Recovery

Presale recovery authority remains unresolved.

If recovery functionality exists, the production model MUST define:

- recoverable asset;
- non-recoverable asset;
- triggering condition;
- authority;
- destination;
- participant impact;
- and record requirements.

Recovery MUST NOT become a hidden path for withdrawing refundable participant assets.

---

## 58. Unsold GFC

Unsold GFC means GFC remaining within the Presale allocation after the applicable sale process concludes.

The final treatment remains unresolved.

Before production activation, the applicable specification MUST define:

- final destination or continued allocation status;
- custody;
- authority;
- timing;
- whether any lock applies;
- whether any burn applies;
- supply impact;
- and public reporting.

Unsold-GFC treatment MUST NOT be chosen opportunistically after the sale result becomes known.

---

## 59. Contribution Limits

The final production specification MUST define whether the presale uses:

- minimum contribution;
- maximum contribution per transaction;
- maximum contribution per wallet;
- maximum contribution per eligible participant;
- or no participant-specific limit.

Any limit MUST be technically enforceable beyond the frontend where circumvention through direct contract interaction would otherwise be possible.

---

## 60. Off-Chain Contributions

Off-chain contributions are not established as part of the current intended presale design.

They MUST NOT be treated as authorized unless introduced through a separate applicable specification that defines:

- payment method;
- participant identification;
- valuation;
- GFC distribution;
- soft-cap accounting;
- refund rights;
- custody;
- reconciliation;
- and reporting.

Off-chain participation MUST NOT bypass the economic rules applicable to on-chain participants without explicit justification.

---

## 61. Participant Interface

The official production interface SHOULD display, where applicable:

- current presale state;
- network;
- authenticated presale address;
- authenticated GFC token address;
- reference price;
- selected payment asset;
- applicable conversion rate;
- rate freshness;
- expected payment amount;
- expected GFC distribution;
- remaining Presale allocation;
- cumulative soft-cap reference value;
- start and end times;
- refund status;
- pause status;
- known limitations;
- and material risks.

The interface MUST NOT display a purchase as completed before the underlying transaction satisfies the applicable confirmation rule.

---

## 62. Wallet Confirmation

Participants SHOULD be able to review material transaction details before signing.

The interface MUST NOT conceal:

- network;
- destination;
- payment asset;
- payment amount;
- or material contract interaction details.

The participant wallet SHOULD remain the final signer for participant-originated purchases.

---

## 63. Public Presale Records

A production presale SHOULD make the following publicly reviewable:

- official presale address;
- official GFC token address;
- network and chain ID;
- verified source status;
- applicable specification version;
- start and end timestamps;
- reference price;
- supported payment assets;
- pricing mechanism;
- soft cap;
- Presale allocation;
- cumulative GFC distributed;
- remaining Presale GFC;
- cumulative accepted reference value;
- current state;
- pause state;
- finalization result;
- contribution-asset balances;
- proceeds withdrawn after success;
- refunds executed after failure;
- unresolved refund obligations;
- unsold-GFC treatment;
- material authority;
- and known deviations.

---

## 64. Transparency Classification

Presale information MUST distinguish among:

### 64.1 Directly verified on-chain information

Examples may include:

- contribution transactions;
- contract balances;
- GFC distribution;
- refund transactions;
- withdrawals;
- state transitions;
- and authenticated contract state.

### 64.2 Project-authored information

Examples may include:

- intended use of proceeds;
- operational explanation;
- expected milestones;
- and public rationale.

### 64.3 Externally supplied information

Examples may include:

- pricing data;
- eligibility-provider records;
- payment-provider records;
- and external reviews.

### 64.4 Independently reviewed information

Information MUST NOT be described as independently reviewed unless reviewer identity or organization, scope, methodology, and limitations are documented.

---

## 65. Transparency Registry Relationship

The planned Transparency Registry MAY later record:

- presale specification versions;
- deployment identity;
- supported-asset history;
- pricing-source history;
- authority changes;
- pause events;
- cancellation;
- finalization;
- refund status;
- migration;
- incidents;
- corrections;
- and known deviations.

The Registry is intended to operate as a versioned historical record rather than a permanent approval badge.

No complete production Transparency Registry is currently deployed.

A Registry record MUST NOT override authenticated on-chain settlement state.

---

## 66. Privacy

Participants MUST be informed that blockchain activity may reveal:

- wallet address;
- payment asset;
- contribution amount;
- GFC distribution;
- timestamp;
- refund transaction;
- and other public transaction data.

Personal data MUST NOT be placed directly on-chain merely to demonstrate eligibility or transparency.

Where off-chain eligibility checks are required, related records MUST be:

- access-controlled;
- purpose-limited;
- protected;
- retained according to applicable requirements;
- and separated from public blockchain data where appropriate.

---

## 67. Security Requirements

The production presale MUST satisfy security requirements appropriate to the final architecture.

Testing and review MUST cover, where applicable:

- purchase accounting;
- supported assets;
- pricing failures;
- decimals;
- rounding;
- immediate GFC distribution;
- Presale allocation exhaustion;
- soft-cap accounting;
- contribution custody;
- refund behavior;
- failed finalization;
- successful finalization;
- pause;
- cancellation;
- proceeds withdrawal;
- migration;
- role boundaries;
- and reentrancy.

Detailed security requirements are defined in [`security-model.md`](security-model.md).

---

## 68. Security Review and Audit Claims

Material production presale code SHOULD undergo appropriately independent security review before production reliance.

No audit is represented as completed by this Draft.

Any future audit claim MUST identify:

- auditor;
- scope;
- exact reviewed version;
- date;
- exclusions;
- report reference;
- and remediation status.

Source verification MUST NOT be represented as an audit.

---

## 69. Required Presale Invariants

The final production implementation MUST preserve at least the following invariants.

### 69.1 Fixed supply

The presale MUST NOT create additional GFC.

### 69.2 Presale allocation ceiling

Aggregate GFC distributed by the presale MUST NOT exceed:

```text
150,000,000 GFC
```

### 69.3 Single contribution accounting

An accepted contribution MUST NOT be counted more than once toward economic accounting.

### 69.4 Distribution accounting

GFC distribution MUST remain reconcilable with accepted purchase accounting.

### 69.5 Soft-cap accounting

Soft-cap reference value MUST be deterministic and reconcilable.

### 69.6 Refund availability

Assets required to satisfy valid refund rights MUST remain available under the applicable rules.

### 69.7 No premature unrestricted proceeds

Refundable contribution assets MUST NOT become unrestricted project proceeds before applicable release conditions are satisfied.

### 69.8 No silent participant-record changes

Privileged roles MUST NOT arbitrarily rewrite valid purchase records.

### 69.9 No undocumented parameter change

Material participant-facing rules MUST NOT change through undocumented authority.

### 69.10 Immediate-distribution/refund consistency

The final production model MUST ensure that immediate GFC distribution and failed-sale refund rights cannot create unreconciled duplicate economic benefit, broken participant rights, or inconsistent Presale allocation accounting.

The exact mechanism remains unresolved in this Draft.

---

## 70. Monitoring

Production monitoring SHOULD include, where applicable:

- activation;
- purchases;
- abnormal contribution patterns;
- pricing-source health;
- stale pricing;
- Presale allocation exhaustion;
- cumulative GFC distributed;
- soft-cap progress;
- pauses;
- authority changes;
- cancellations;
- finalization;
- refunds;
- proceeds withdrawals;
- migration;
- unsold-GFC movement;
- and contribution-balance discrepancies.

Monitoring does not replace contract-level enforcement.

---

## 71. Incident Handling

Potential presale incidents include:

- smart-contract exploit;
- incorrect pricing;
- stale pricing;
- wrong-asset acceptance;
- contribution-accounting error;
- GFC distribution error;
- Presale underfunding;
- refund shortfall;
- unauthorized withdrawal;
- compromised administrator;
- fake presale address;
- compromised frontend;
- payment-asset failure;
- privacy incident;
- and specification divergence.

Incident handling MUST prioritize preservation of participant rights and economic accounting.

---

## 72. Fake Contract and Interface Protection

Official production presale addresses MUST be authenticated through the GFC release process.

The production interface SHOULD display the authenticated contract address.

Participants SHOULD be able to verify:

- network;
- presale address;
- GFC token address;
- source verification;
- and transaction destination.

A social-media post alone SHOULD NOT be the sole authentication mechanism for a production presale.

---

## 73. Disputes and Corrections

The final operational process SHOULD provide a method for reporting:

- incorrect purchase accounting;
- incorrect GFC distribution;
- failed refund;
- unsupported asset interaction;
- pricing dispute;
- duplicate record;
- interface misrepresentation;
- or suspected unauthorized activity.

Any correction mechanism MUST be:

- narrowly scoped;
- evidenced;
- authorized;
- logged;
- and reconcilable.

A correction role MUST NOT possess arbitrary authority to rewrite valid participant history.

---

## 74. Public Communication Requirements

Public presale communication MUST NOT:

- state or imply that the presale is live when it is not;
- publish an internal planning date as a confirmed public launch date unless formally released;
- describe the Base Sepolia pilot as the production presale;
- imply unlimited fundraising capacity;
- imply guaranteed token appreciation;
- imply guaranteed liquidity;
- imply guaranteed listing;
- imply guaranteed staking returns;
- imply guaranteed project completion;
- imply guaranteed impact;
- describe contribution assets as unrestricted project funds while refund rights remain active;
- describe the current model as deferred claiming;
- or conceal the unresolved immediate-distribution/refund interaction before that interaction is finalized.

---

## 75. No Guaranteed Outcomes

The presale MUST NOT be represented as guaranteeing:

- token appreciation;
- liquidity;
- exchange listing;
- staking income;
- governance influence;
- project completion;
- charitable results;
- impact;
- tax treatment;
- or regulatory approval.

Reaching the soft cap is a quantitative sale condition.

It is not proof of project success.

---

## 76. Pilot and Production Separation

The public Base Sepolia pilot is not the production presale.

No pilot contract, pilot wallet, pilot transaction, test distribution, demo interface, or testnet token MUST be represented as:

- production presale contract;
- production GFC distribution;
- production participant contribution;
- production refund;
- production proceeds;
- or production presale security evidence.

Production presale status requires separately authenticated Base Mainnet implementation and records.

---

## 77. Conformance

A presale implementation conforms to this specification only when:

- it identifies an applicable versioned presale specification;
- production status is authenticated;
- no presale is represented as live before activation;
- the GFC reference price is enforced according to the applicable release;
- the Presale distribution ceiling is enforced;
- no additional GFC is minted;
- ETH, USDC, DAI support matches the applicable production release;
- purchase accounting is deterministic;
- immediate GFC distribution matches the applicable specification;
- soft-cap accounting is deterministic;
- contribution custody preserves valid refund rights;
- successful finalization and failed finalization are correctly distinguished;
- the immediate-distribution/refund interaction is fully and correctly implemented;
- administrative authority is disclosed;
- material participant-facing rules are not silently mutable;
- unsold-GFC treatment is predefined;
- production addresses are authenticated;
- pilot status is not misrepresented;
- applicable presale-conformance claims are traceable to the verification mappings defined in [`conformance-verification.md`](conformance-verification.md);
- implementation-specific verification bindings are authenticated for the evaluated deployment where required;
- evidence is not interpreted beyond its defined evidence ceiling;
- and material deviations are disclosed.

The applicable verification methods, observable evidence, implementation bindings, and evidence ceilings for presale-conformance requirements are defined in [`conformance-verification.md`](conformance-verification.md).

A production presale-conformance claim MUST use the authenticated implementation-specific bindings for the actual production distribution, accounting, custody, finalization, refund, and withdrawal architecture. No particular escrow contract, custody function, state read, event, or interface name may be assumed merely for verification convenience.

Until the immediate-distribution and failed-sale refund interaction is normatively resolved, technically implemented, and covered by authenticated verification bindings, no verification result may represent the production Presale as completely conforming.

Where a required production implementation binding has not yet been established, the underlying Presale requirement remains specified but MUST NOT be represented as technically verified.

A frontend, website, Draft specification, social-media post, or unauthenticated address does not establish conformance.

---

## 78. Presale Non-Conformance

Presale non-conformance includes:

- frontend-only price enforcement;
- GFC distribution exceeding 150,000,000 GFC;
- additional GFC minting;
- acceptance of unauthenticated payment assets;
- unsupported pricing behavior;
- incorrect purchase accounting;
- incorrect immediate distribution;
- premature unrestricted proceeds withdrawal;
- insufficient assets to satisfy valid refunds;
- removal of valid refund rights;
- hidden administrator authority;
- undocumented material parameter change;
- improvised post-launch treatment of distributed GFC after failed finalization;
- undocumented unsold-GFC movement;
- fake or unauthenticated production address;
- pilot activity represented as production;
- or public claims materially stronger than authenticated implementation supports.

Material non-conformance MAY require:

- pause;
- cancellation;
- refund remediation;
- proceeds-withdrawal restriction;
- authority revocation;
- migration;
- participant notification;
- public correction;
- security review;
- governance review;
- independent investigation;
- or incident treatment.

A specification MUST NOT be rewritten retrospectively merely to conceal presale non-conformance.

---

## 79. Change Classification

A material presale change includes a change to:

- reference price;
- sale duration;
- soft cap;
- Presale allocation;
- supported payment assets;
- pricing architecture;
- immediate-distribution behavior;
- refund rights;
- failed-finalization treatment;
- proceeds-withdrawal conditions;
- unsold-GFC treatment;
- administrative authority;
- immutability;
- pause behavior;
- cancellation;
- or migration.

A breaking presale change requires:

- explicit versioning;
- rationale;
- economic analysis;
- security analysis;
- governance analysis;
- participant-rights analysis;
- implementation analysis;
- migration analysis where relevant;
- and updated public communication.

Material presale behavior MUST NOT be changed solely through frontend updates or informal statements.

---

## 80. Presale Non-Goals

The presale does not aim to:

- guarantee financial return;
- guarantee token appreciation;
- guarantee liquidity;
- guarantee exchange listing;
- guarantee staking income;
- create additional GFC supply;
- create unlimited fundraising capacity;
- provide unrestricted early access to refundable participant assets;
- use frontend behavior as a substitute for settlement enforcement;
- remove legal or human responsibility through automation;
- treat purchase activity as proof of impact;
- or conceal material presale authority.

The current design also does not use deferred claim as its intended token-delivery model.

---

## 81. Current Unresolved Presale Decisions

The following matters remain unresolved unless separately established by a later versioned specification or authenticated production implementation.

### 81.1 Payment-asset implementation

- exact production USDC contract address;
- exact production DAI contract address;
- native ETH handling;
- asset-specific transfer behavior;
- asset failure policy;
- and post-activation asset-change authority.

### 81.2 Pricing

- final pricing source or oracle architecture;
- source addresses or identifiers;
- update frequency;
- stale-price threshold;
- deviation limits;
- fallback behavior;
- and rounding formulas.

### 81.3 Purchase limits

- minimum contribution;
- per-transaction maximum;
- per-wallet maximum;
- per-participant maximum;
- and anti-circumvention rules.

### 81.4 Eligibility

- jurisdiction restrictions;
- age requirements;
- identity requirements;
- allowlist or credential model;
- sanctions controls;
- and participant legal terms.

### 81.5 Contract architecture

- final immutable/configurable boundary;
- contract structure;
- exact activation method;
- pause scope;
- cancellation authority;
- recovery;
- migration;
- and exact finalization implementation.

### 81.6 Immediate distribution

- exact transaction ordering;
- atomicity;
- transfer-failure behavior;
- partial-fill interaction;
- and invalid-purchase correction behavior.

### 81.7 Refunds

- exact refund mechanism;
- exact refund amount rule;
- exact refund timing;
- refund-claim lifecycle;
- treatment of already distributed GFC after failed finalization;
- cancellation interaction;
- and migration of unresolved refunds.

### 81.8 Contribution custody

- exact custody architecture;
- segregation model;
- contract or vault structure;
- refund-reserve accounting;
- and custody authority.

### 81.9 Successful proceeds

- final proceeds destination;
- custody model;
- withdrawal authority;
- withdrawal threshold;
- asset-conversion policy;
- and reporting.

### 81.10 Unsold GFC

- final destination;
- continued allocation status;
- lock or burn treatment;
- execution authority;
- execution timing;
- and circulating-supply effect.

### 81.11 Security

- final independent review scope;
- audit requirements if any;
- monitoring;
- incident severity;
- public-disclosure process;
- and emergency response.

These unresolved matters MUST NOT be represented as finalized production decisions.

---

## 82. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- ETH, USDC, and DAI production handling is finalized;
- all applicable payment-asset identifiers are authenticated;
- pricing and conversion logic are finalized;
- pricing-failure behavior is finalized;
- rounding rules and test vectors are finalized;
- purchase limits are finalized or explicitly excluded;
- eligibility requirements are resolved;
- exact start and end behavior are defined;
- the state machine is finalized;
- immediate GFC distribution mechanics are finalized;
- the immediate-distribution and failed-sale refund interaction is technically, economically, and normatively resolved;
- refund mechanics are finalized;
- contribution custody is finalized;
- successful-finalization behavior is finalized;
- failed-finalization behavior is finalized;
- proceeds destination and withdrawal authority are finalized;
- unsold-GFC treatment is finalized;
- administrative roles are defined;
- authority-registry entries can be prepared;
- immutability and configurability are finalized;
- pause behavior is finalized or explicitly excluded;
- cancellation behavior is finalized;
- migration is finalized or explicitly excluded;
- recovery is finalized or explicitly excluded;
- off-chain contributions remain explicitly excluded or are separately specified;
- participant-facing disclosures are finalized;
- privacy processes are documented;
- security requirements are mapped to the implementation;
- presale conformance requirements are mapped to appropriate verification methods and evidence ceilings;
- required production implementation-specific verification bindings can be authenticated;
- independent review requirements are finalized;
- production deployment and authentication procedures are defined;
- Base Sepolia pilot and Base Mainnet production terminology are consistently separated;
- public communication is consistent with the applicable release;
- and all related specifications are mutually consistent.

---

## 83. Final Presale Principles

The GFC presale model preserves the following distinctions:

> Draft does not mean live.

> A fixed displayed price is insufficient unless the settlement mechanism enforces it.

> Immediate GFC distribution is the current design direction.

> Immediate distribution does not eliminate refund obligations.

> A failed-sale refund model must explicitly resolve the treatment of already distributed GFC.

> Reaching the soft cap is not the same as successful finalization.

> Participant contribution assets are not unrestricted project proceeds while valid refund rights remain active.

> No separate monetary hard cap does not mean unlimited fundraising capacity.

> Presale allocation does not mean additional token supply.

> Transaction verification does not prove project execution or impact.

> Source verification does not mean audit.

> Pilot does not mean production.

The production presale must make price, payment assets, allocation, distribution, custody, refund rights, authority, finalization, proceeds, and material limitations technically enforceable and publicly reviewable before production reliance.

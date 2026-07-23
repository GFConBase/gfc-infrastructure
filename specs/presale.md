# Global Foundation Coin Presale Specification

**Document ID:** GFC-PRE-001  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-deployment  
**Intended Network:** Base Mainnet  
**Chain ID:** 8453  
**Last Updated:** 2026-07-23

---

## 1. Document Status

This document defines the intended behavior, constraints, participant rights, authority boundaries, and transparency requirements of the planned GFC presale.

It is normative because it defines intended requirements and prohibited behavior.

Its maturity remains Draft. The requirements may change before the first versioned release.

At the time of publication:

- no GFC presale is live;
- no production presale contract is represented as deployed;
- no production presale address has been published;
- no public presale start date is established by this document;
- no supported payment asset has been finalized;
- no oracle or conversion mechanism has been finalized;
- no production purchase, claim, refund, or withdrawal mechanism has been activated;
- this document does not constitute an offer, invitation, or confirmation that participation is available;
- no implementation is governed by this document unless it explicitly identifies an applicable versioned release.

The presence of a parameter or mechanism in this document does not mean that it has already been implemented, tested, reviewed, audited, deployed, or activated.

---

## 2. Purpose

This document defines the planned GFC presale architecture.

Its purpose is to establish:

- fixed and reviewable pricing rules;
- a finite token allocation;
- deterministic purchase accounting;
- clear success and failure conditions;
- protected participant refund rights;
- controlled custody of contributed assets;
- constrained administrative authority;
- transparent token-claim mechanics;
- predictable handling of unsold tokens;
- accurate communication of presale status;
- and verifiable linkage between presale records and the wider GFC transparency infrastructure.

The presale must not rely on informal promises or front-end behavior where contract-level enforcement is technically required.

---

## 3. Relationship to Other Specifications

This document must be read together with:

- `architecture.md`;
- `governance-constraints.md`;
- `transparency-model.md`;
- `non-goals.md`;
- `glossary.md`;
- and the repository-level `SECURITY.md`.

A future token specification must additionally define:

- the production GFC token contract;
- transfer behavior;
- fees;
- administrative authority;
- and token allocation implementation.

Where specifications conflict, the conflict must be resolved before the presale specification is marked Stable or a production presale begins.

---

## 4. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are normative only when:

- they appear in uppercase;
- the document declares `Authority: Normative`;
- and the document version applies to the implementation being evaluated.

Because this document is currently Draft, its requirements describe the intended presale model but remain subject to review and versioned release.

---

## 5. Scope

This specification covers:

- presale token allocation;
- reference price;
- contribution-value calculation;
- supported payment assets;
- purchase accounting;
- soft-cap calculation;
- sale duration;
- sale-state transitions;
- token entitlement;
- token claiming;
- contribution custody;
- presale finalization;
- successful-sale withdrawals;
- failed-sale refunds;
- cancellation;
- pausing;
- unsold-token handling;
- administrative authority;
- upgradeability;
- participant-facing disclosures;
- on-chain records;
- transparency requirements;
- privacy boundaries;
- security requirements;
- incident handling;
- conformance;
- and unresolved pre-launch decisions.

---

## 6. Out of Scope

This document does not independently define:

- final legal terms of participation;
- jurisdiction-specific eligibility;
- identity-verification requirements;
- sanctions controls;
- tax treatment;
- accounting treatment;
- consumer-protection classification;
- securities or financial-instrument classification;
- final supported payment assets;
- final oracle provider;
- final contract source code;
- final contract addresses;
- final user-interface design;
- final marketing strategy;
- exchange listing;
- market price after the presale;
- guaranteed liquidity;
- guaranteed token value;
- guaranteed returns;
- or guaranteed project impact.

These matters require separate legal, technical, operational, or public documentation before launch.

---

## 7. Presale Principles

The GFC presale follows the principles below.

### 7.1 Contract-enforced rules

Material participant rights and financial constraints MUST be enforced by the presale contract or an equally verifiable mechanism.

A user interface MUST NOT be the sole enforcement layer for:

- price;
- token allocation;
- contribution limits;
- soft-cap calculation;
- refund rights;
- token entitlement;
- or withdrawal conditions.

### 7.2 Participant protection before fund access

Contributed assets MUST remain unavailable for discretionary project use until the presale has ended and has been successfully finalized.

### 7.3 No token creation through the presale

The presale MUST distribute tokens only from the predefined Presale Allocation.

The presale MUST NOT mint additional GFC.

### 7.4 Deterministic accounting

Every accepted contribution MUST produce a deterministic and reviewable record of:

- payment asset;
- accepted payment amount;
- reference value;
- applicable conversion rate;
- GFC entitlement;
- contributor address;
- transaction time;
- and transaction identifier.

### 7.5 Refund integrity

Where the presale fails or is validly cancelled, eligible participants MUST be able to recover their accepted contributions according to the applicable refund rules.

### 7.6 No retrospective rule changes

Presale rules MUST NOT be changed after launch merely because the actual result differs from project expectations.

### 7.7 Accurate status communication

Public communication MUST distinguish between:

- planned presale;
- configured presale;
- active presale;
- paused presale;
- ended presale;
- successful presale;
- failed presale;
- refund phase;
- claim phase;
- and completed presale.

---

## 8. Current Intended Parameters

The current intended presale parameters are:

| Parameter | Intended Value |
|---|---:|
| GFC reference price | €0.05 per GFC |
| Presale duration | 8 weeks |
| Soft cap | €250,000 reference value |
| Presale Allocation | 150,000,000 GFC |
| Allocation percentage | 15% of total GFC supply |
| Separate monetary hard cap | None |
| Maximum token distribution | 150,000,000 GFC |
| Maximum reference value at full allocation | €7,500,000 |
| Failure condition | Soft cap not reached by the presale end |
| Token delivery | Claimable after successful finalization |
| Inflation through presale | Prohibited |

The absence of a separate monetary hard cap MUST NOT be communicated as unlimited fundraising capacity.

The finite Presale Allocation creates an absolute distribution limit of 150,000,000 GFC.

At the intended fixed reference price, this corresponds to a maximum gross reference value of €7,500,000.

---

## 9. Presale Token Allocation

### 9.1 Maximum allocation

The presale is intended to distribute no more than:

**150,000,000 GFC**

This represents:

**15% of the fixed total supply of 1,000,000,000 GFC**

### 9.2 Contract funding

Before activation, the production presale contract MUST have verifiable access to the complete configured sale allocation.

The contract MUST NOT accept contributions for tokens that it cannot distribute.

### 9.3 No over-allocation

The presale MUST NOT:

- allocate more than 150,000,000 GFC;
- create additional GFC;
- borrow tokens from another allocation without prior specification changes;
- or issue undocumented replacement entitlements.

### 9.4 Allocation exhaustion

A purchase that would exceed the remaining Presale Allocation MUST either:

- revert completely; or
- use a predefined partial-fill mechanism that automatically returns the unused contribution amount.

The production specification MUST select one behavior before launch.

Silent retention of excess payment is prohibited.

The recommended initial behavior is full transaction reversion because it is simpler to audit and reduces partial-fill ambiguity.

---

## 10. Reference Price

The intended reference price is:

**€0.05 per GFC**

The reference price MUST remain fixed throughout the active presale.

The reference price MUST NOT be changed after activation.

Any public interface MUST clearly identify:

- the euro-denominated reference price;
- the payment asset being used;
- the applicable conversion rate;
- the expected payment amount;
- and the resulting GFC entitlement.

---

## 11. Payment-Asset Conversion

### 11.1 Contract-level enforcement

Where contributions are accepted in assets other than a euro-denominated asset, conversion MUST be enforced by the contract or another verifiable settlement mechanism.

Frontend-only conversion is prohibited.

A participant can interact with a contract without using the official interface. Therefore, interface calculations cannot define the actual accepted price.

### 11.2 Conversion requirements

For each supported payment asset, the production implementation MUST define:

- asset contract address;
- asset decimals;
- reference currency;
- conversion source;
- conversion direction;
- rate-update method;
- maximum price age;
- rounding behavior;
- minimum valid price;
- failure behavior;
- and fallback behavior.

### 11.3 Purchase-time valuation

The euro reference value of a contribution MUST be recorded at the time the contribution is accepted.

The recorded purchase-time value MUST be used for:

- soft-cap accounting;
- GFC entitlement;
- purchase records;
- and presale reporting.

Later market-price movements MUST NOT retroactively change the participant’s GFC entitlement.

### 11.4 Oracle failure

A purchase MUST revert where the required conversion data is:

- unavailable;
- stale;
- invalid;
- zero;
- negative;
- outside defined safety limits;
- or otherwise unreliable under the production rules.

The contract MUST NOT silently substitute an undocumented rate.

### 11.5 Volatile payment assets

Acceptance of volatile assets introduces:

- exchange-rate risk;
- refund-value risk;
- treasury-value risk;
- oracle risk;
- and soft-cap interpretation risk.

The initial production presale SHOULD minimize the number of accepted assets.

Volatile assets SHOULD NOT be accepted unless their custody, valuation, refund, and risk-treatment rules are fully defined.

### 11.6 Unsupported token behavior

The presale SHOULD NOT accept payment tokens with:

- transfer fees;
- rebasing;
- reflection mechanics;
- non-standard balance accounting;
- transfer hooks that can alter settlement;
- or unreliable redemption assumptions.

Any exception requires explicit technical review and documentation.

---

## 12. Rounding and Precision

The production implementation MUST define rounding at every conversion stage.

At minimum:

- GFC entitlement MUST NOT be rounded upward beyond the paid reference value;
- the contract MUST NOT allocate more than the remaining sale allocation;
- decimal conversions MUST be deterministic;
- rounding MUST be reproducible off-chain;
- and material payment excess MUST be reverted or returned.

Small rounding differences MUST NOT be retained without disclosure.

The applicable formula and test vectors MUST be published before launch.

---

## 13. Supported Payment Assets

No payment asset is finalized by this Draft specification.

Before Stable status, each supported asset MUST be published with:

- name;
- symbol;
- contract address;
- network;
- decimals;
- conversion methodology;
- oracle or pricing source;
- risk disclosure;
- refund treatment;
- and deprecation procedure.

A symbol alone is not sufficient identification.

The contract address and network determine the accepted asset.

Fake or unsupported assets MUST NOT be accepted merely because they share a symbol with an approved asset.

---

## 14. Presale Duration

The intended presale duration is:

**8 weeks**

The production release MUST publish:

- exact start timestamp;
- exact end timestamp;
- applicable timezone for human-readable communication;
- block-timestamp interpretation;
- and any pre-launch activation condition.

The contract-level timestamps are authoritative for execution.

Human-readable dates MUST accurately correspond to the on-chain timestamps.

---

## 15. Start Conditions

The presale MUST NOT become active until:

- the production contract is deployed;
- source code is verified;
- the applicable specification release is published;
- the configured token allocation is available;
- supported payment assets are configured;
- pricing mechanisms are operational;
- privileged roles are published;
- refund behavior is tested;
- claim behavior is tested;
- withdrawal destinations are published;
- security review requirements are satisfied;
- and required legal and operational approvals are complete.

Activation MUST be a publicly observable state transition.

---

## 16. Presale State Model

The production presale MUST use explicit and externally observable states.

The state model SHOULD include:

### 16.1 Configured

The contract is deployed and configured but purchases are not yet accepted.

### 16.2 Active

The presale accepts valid contributions.

### 16.3 Paused

New contributions are temporarily disabled due to a defined incident or operational condition.

### 16.4 Ended

The configured end timestamp has been reached and new contributions are no longer accepted.

### 16.5 Successful

The presale has ended, the soft cap has been reached, and successful finalization has occurred.

### 16.6 Failed

The presale has ended without reaching the soft cap or has been cancelled under rules requiring refunds.

### 16.7 Claiming

Participants may claim purchased GFC following successful finalization.

### 16.8 Refunding

Participants may reclaim accepted contributions following failure or cancellation.

### 16.9 Completed

The presale remains historically reviewable, while all continuing participant rights remain preserved according to the applicable rules.

State transitions MUST produce public contract events.

---

## 17. Purchase Eligibility

The final production rules MUST define:

- eligible jurisdictions;
- prohibited jurisdictions;
- minimum age;
- sanctions restrictions;
- identity-verification requirements;
- wallet eligibility;
- participant representations;
- and applicable legal terms.

The technical presale contract MUST NOT be represented as independently resolving all legal eligibility questions.

Where an allowlist or eligibility credential is required, its authority, privacy implications, revocation rules, and failure behavior MUST be documented.

---

## 18. Purchase Process

A valid purchase MUST:

1. occur while the presale is Active;
2. use a supported payment asset;
3. use valid conversion information;
4. satisfy any applicable minimum or maximum;
5. satisfy any applicable eligibility controls;
6. remain within the available Presale Allocation;
7. transfer or securely reserve the accepted contribution;
8. record the participant’s GFC entitlement;
9. update the soft-cap reference total;
10. emit a public purchase event.

The purchase event SHOULD include or allow derivation of:

- contributor;
- payment asset;
- accepted payment amount;
- reference value;
- GFC entitlement;
- and cumulative tokens allocated.

No sensitive personal information may be emitted on-chain.

---

## 19. Purchase Entitlement

A successful contribution creates a contractual token entitlement within the presale system.

It does not immediately prove that:

- the presale will succeed;
- the participant can immediately transfer GFC;
- liquidity will exist;
- the token will have a particular market value;
- or the project will achieve a particular outcome.

The entitlement MUST remain associated with the participant address unless an explicitly documented transfer or recipient mechanism exists.

No entitlement-transfer mechanism should be introduced without addressing:

- eligibility;
- sanctions;
- accounting;
- refund rights;
- and double-claim prevention.

---

## 20. Token Delivery Model

### 20.1 Deferred claim

Purchased GFC MUST become claimable only after:

- the presale has ended;
- the soft cap has been reached;
- successful finalization has occurred;
- and the claim function has been activated according to the contract rules.

### 20.2 No instant distribution

The production presale MUST NOT transfer final purchased GFC immediately during the Active state.

This prevents participants from simultaneously retaining distributed tokens and claiming refunds after a failed presale.

### 20.3 No post-success discretion

Once a participant has a valid entitlement and the presale has successfully finalized, the project MUST NOT possess discretionary authority to cancel that entitlement.

### 20.4 Presale vesting

The current intended model does not impose an additional presale vesting schedule.

Following successful finalization, the full purchased entitlement is intended to become claimable.

Any future introduction of presale vesting would constitute a material change and must be defined before launch.

### 20.5 Claim destination

Claims SHOULD be delivered to the entitled wallet.

Any ability to redirect claims to another wallet MUST be explicitly defined and protected against unauthorized redirection.

---

## 21. Token Claims

### 21.1 Claim rights

Following successful finalization, eligible participants MUST be able to claim their recorded GFC entitlement.

### 21.2 Claim accounting

The contract MUST prevent:

- double claims;
- claims above recorded entitlement;
- claims during an unsuccessful presale;
- claims before successful finalization;
- and claims from unauthorized addresses.

### 21.3 Claim availability

Valid token claims SHOULD NOT expire solely because a participant does not immediately claim.

Where migration becomes necessary, remaining claim rights MUST be preserved through a documented successor mechanism.

### 21.4 Partial claims

The production implementation MUST explicitly define whether:

- only full claims are permitted; or
- partial claims are permitted.

The recommended initial implementation is a full single claim because it reduces accounting complexity.

### 21.5 Claim failure

A temporary technical failure MUST NOT extinguish a valid claim entitlement.

---

## 22. Soft Cap

The intended soft cap is:

**€250,000 reference value**

### 22.1 Calculation

The soft cap MUST be calculated using the sum of accepted purchase-time euro reference values.

Rejected, reverted, cancelled, or refunded contributions MUST NOT count toward the final successful total.

### 22.2 Reaching the soft cap

Reaching the soft cap during the Active state means that the quantitative success condition has been satisfied.

It does not immediately:

- end the presale;
- make participant contributions withdrawable;
- remove all cancellation protections;
- activate token claims;
- or complete finalization.

### 22.3 Final success determination

The presale becomes successful only after:

- the configured end timestamp has been reached;
- no unresolved cancellation condition prevents success;
- the recorded soft-cap total is at least €250,000;
- and the contract has been successfully finalized.

### 22.4 No early withdrawal

Presale funds MUST NOT become withdrawable merely because the soft cap has been reached before the presale end.

---

## 23. No Separate Monetary Hard Cap

The intended model has no separate monetary hard cap.

However:

- the token price is fixed;
- the Presale Allocation is finite;
- and the presale cannot distribute more than 150,000,000 GFC.

The maximum gross reference value at full allocation is therefore:

**€7,500,000**

Public communication MUST disclose the finite allocation and resulting maximum reference value whenever the absence of a monetary hard cap is discussed.

---

## 24. Finalization

### 24.1 Finalization timing

Finalization may occur only after the configured presale end or after a valid cancellation that requires failure processing.

### 24.2 Permissionless finalization

Where technically feasible, finalization SHOULD be callable by any address once objective finalization conditions are satisfied.

Final success or failure SHOULD NOT depend indefinitely on discretionary administrator action.

### 24.3 Successful finalization

Successful finalization MUST:

- confirm that the soft cap was reached;
- prevent new purchases;
- preserve participant entitlements;
- activate token claims;
- permit only authorized proceeds handling;
- determine the applicable unsold-token treatment;
- and emit a public finalization event.

### 24.4 Failed finalization

Failed finalization MUST:

- confirm that the soft cap was not reached or that a refundable cancellation occurred;
- prevent new purchases;
- disable token claims;
- activate refunds;
- preserve sufficient assets for all valid refunds;
- and emit a public failure event.

### 24.5 Irreversibility

A successfully finalized presale MUST NOT later be changed into a failed presale through ordinary administrative discretion.

A failed presale MUST NOT later be changed into a successful presale merely to avoid refunds.

---

## 25. Contribution Custody

### 25.1 Escrow requirement

Accepted on-chain contributions MUST remain under presale-contract or dedicated escrow control until successful finalization.

### 25.2 No discretionary use before finalization

Before successful finalization, contributed assets MUST NOT be:

- transferred to the operating treasury;
- used for marketing;
- used for development;
- added to liquidity;
- lent;
- staked;
- exchanged;
- pledged;
- or otherwise exposed to discretionary project use.

### 25.3 Asset preservation

The presale MUST preserve the ability to satisfy all valid refund rights.

Assets subject to refund rights MUST NOT be placed into strategies that introduce avoidable loss, lock-up, or counterparty risk.

### 25.4 Payment-asset custody

Where multiple assets are accepted, custody and refund obligations MUST remain separately identifiable by asset.

---

## 26. Successful-Sale Proceeds

### 26.1 Withdrawal condition

Presale proceeds may become withdrawable only after successful finalization.

### 26.2 Predefined destination

Withdrawals MUST be directed only to addresses or contracts published before launch.

The destination SHOULD be a dedicated Presale Proceeds Vault or treasury structure governed according to `governance-constraints.md`.

### 26.3 No unrestricted administrator destination

An administrator MUST NOT be able to redirect proceeds to an arbitrary address after contributions have been accepted.

### 26.4 Withdrawal authority

The production specification MUST define:

- authorized withdrawal role;
- approval threshold;
- destination;
- whether withdrawals are partial or complete;
- transaction limits;
- timelock, if any;
- and reporting obligations.

### 26.5 Documentation

Each material withdrawal MUST be accompanied by:

- transaction record;
- amount;
- asset;
- destination;
- responsible authority;
- applicable approval;
- and stated purpose or treasury classification.

Post-action documentation does not replace required prior authorization.

---

## 27. Refund Rights

### 27.1 Refund conditions

A participant is entitled to a refund where:

- the presale ends below the soft cap;
- the presale is validly cancelled under refundable conditions;
- or another production rule explicitly creates a refund right.

### 27.2 Refund amount

A valid refund MUST return the participant’s recorded accepted amount in the same payment asset originally accepted.

The project MUST NOT deduct:

- project expenses;
- marketing expenses;
- administrative expenses;
- or unsuccessful presale costs

from the recorded refundable contribution.

Normal blockchain transaction fees paid by the participant to execute the refund transaction are not controlled by the project.

### 27.3 No conversion-based substitution

A participant who contributed one supported asset MUST NOT be forced to accept a different asset unless:

- the participant explicitly agrees;
- or a predefined emergency migration process preserves equivalent rights and is legally and technically justified.

### 27.4 Pull-based refunds

Refunds SHOULD use a participant-initiated pull mechanism where technically appropriate.

This reduces reliance on bulk administrator payments and avoids sending assets to inaccessible or changed addresses without participant action.

### 27.5 Refund accounting

The contract MUST prevent:

- double refunds;
- refunds above the recorded amount;
- refunds after the associated contribution has already been validly settled through another mechanism;
- and unauthorized refund claims.

### 27.6 Refund availability

Valid refund rights MUST NOT expire solely because a participant does not claim immediately.

Where the original contract must be migrated or deprecated, unclaimed refund rights MUST be preserved through a documented successor process.

### 27.7 Project withdrawal prohibition

No project-controlled role may withdraw assets required to satisfy active refund rights.

---

## 28. Cancellation

### 28.1 Pre-start cancellation

The presale MAY be cancelled before activation.

A pre-start cancellation MUST NOT create participant refund obligations where no contributions have been accepted.

### 28.2 Post-start cancellation

After activation, cancellation MAY occur only under predefined circumstances, such as:

- critical security vulnerability;
- compromised contract or administrator authority;
- material legal prohibition;
- unrecoverable pricing failure;
- or another severe condition defined before launch.

### 28.3 Cancellation outcome

A post-start cancellation MUST result in:

- no further purchases;
- no successful-sale proceeds withdrawal;
- no GFC claims;
- preserved participant contribution records;
- and full refund rights for accepted contributions.

### 28.4 No selective cancellation

Cancellation MUST NOT selectively preserve some purchases while invalidating others unless a specific contribution was technically or legally invalid under rules published before purchase.

### 28.5 Public disclosure

A cancellation MUST be publicly documented with:

- time;
- authority;
- reason;
- affected contract;
- participant impact;
- refund process;
- and continuing risks.

Sensitive security details MAY be delayed where immediate publication would increase risk.

---

## 29. Pausing

### 29.1 Permitted purpose

The presale MAY include narrowly scoped pause functionality for:

- security incidents;
- oracle failures;
- payment-asset failures;
- eligibility-system failures;
- or other predefined emergencies.

### 29.2 Pause scope

A standard pause SHOULD disable new purchases.

Refunds in a failed state and claims in a successful state SHOULD remain available unless the affected function itself is unsafe.

### 29.3 No silent duration change

Pausing MUST NOT silently extend the eight-week presale duration.

Any permitted extension mechanism would need to be:

- defined before launch;
- strictly limited;
- publicly disclosed;
- and consistently applied.

The recommended initial design is that the end timestamp remains fixed.

### 29.4 No pause-based confiscation

Pause authority MUST NOT be used to:

- seize contributions;
- invalidate entitlements;
- remove refund rights;
- redirect proceeds;
- or modify pricing.

---

## 30. Administrative Authority

Potential presale roles may include:

- configuration administrator;
- activation authority;
- pauser;
- finalization caller;
- proceeds-withdrawal authority;
- eligibility administrator;
- and migration authority.

Each actual role MUST be:

- documented;
- narrowly scoped;
- technically identifiable;
- assigned before launch;
- included in the authority registry;
- and removable or constrained through a defined process.

No undocumented presale role is permitted.

---

## 31. Parameter Mutability

### 31.1 Before activation

Before activation, authorized roles MAY configure parameters that remain unresolved during development.

The final values MUST be publicly verified before the presale begins.

### 31.2 After activation

After activation, the following parameters MUST NOT be changed through ordinary administration:

- GFC reference price;
- Presale Allocation;
- soft cap;
- start timestamp;
- end timestamp;
- purchase accounting formula;
- refund conditions;
- token-delivery model;
- successful-withdrawal conditions;
- and participant entitlement records.

### 31.3 Supported assets

The production release MUST define whether supported payment assets can be added or removed after activation.

The recommended initial design is that the supported-asset set is immutable after activation.

Disabling a compromised asset MAY be permitted as an emergency safety action, but MUST NOT invalidate previously accepted contribution records.

---

## 32. Upgradeability

### 32.1 Recommended architecture

The production presale contract SHOULD be non-upgradeable after activation.

A one-time presale benefits from reduced administrative complexity and a smaller upgrade control surface.

### 32.2 Upgradeable deployment

Where an upgradeable architecture is used during development, upgrade authority SHOULD be permanently disabled or transferred to a strictly constrained process before activation.

### 32.3 Prohibited upgrade effects

An upgrade MUST NOT silently:

- change price;
- increase the allocation;
- reduce the soft cap after launch;
- remove refund rights;
- modify participant entitlements;
- permit early withdrawals;
- introduce additional minting;
- or redirect contribution custody.

### 32.4 Migration

Where a critical issue requires migration, the process MUST preserve:

- contribution records;
- GFC entitlements;
- refund rights;
- supported-asset balances;
- and public auditability.

Migration MUST NOT require participants to surrender rights without an equivalent replacement.

---

## 33. Unsold Tokens

### 33.1 Definition

Unsold tokens are Presale Allocation tokens that were not assigned to participant entitlements when the presale ended.

### 33.2 Mandatory pre-launch rule

The exact treatment of unsold tokens MUST be defined and published before presale activation.

The production presale MUST NOT begin while unsold-token treatment remains discretionary.

### 33.3 Permitted design requirements

Whatever model is selected MUST define:

- destination;
- timing;
- authority;
- lock or vesting conditions;
- whether the tokens remain part of the Presale Allocation;
- whether they move to another allocation;
- whether they are burned;
- and how the movement affects circulating supply.

### 33.4 No arbitrary post-result decision

Governance MUST NOT wait until the presale result is known before choosing the treatment that is most favorable to project insiders or market conditions.

### 33.5 One-time execution

Where unsold tokens are transferred, burned, or locked after finalization, the operation SHOULD be:

- deterministic;
- publicly observable;
- executed once;
- and incapable of repeated discretionary use.

### 33.6 Current unresolved status

The final unsold-token destination is not established by this Draft specification.

This issue MUST be resolved before Stable status and before launch.

---

## 34. Contribution Limits

The production specification MUST define whether the presale includes:

- minimum contribution;
- maximum contribution per transaction;
- maximum contribution per wallet;
- maximum contribution per verified participant;
- or no participant-specific cap.

Any cap MUST define:

- measurement currency;
- aggregation method;
- treatment of multiple wallets;
- rounding;
- and enforcement mechanism.

Contribution limits MUST NOT be applied only through the official frontend.

---

## 35. Off-Chain Contributions

Off-chain or fiat contributions are not authorized by this Draft specification.

Where such contributions are introduced, a separate specification MUST define:

- payment method;
- participant identification;
- settlement confirmation;
- pricing timestamp;
- token entitlement creation;
- soft-cap accounting;
- refund process;
- reconciliation;
- custody;
- and public reporting.

Off-chain contributions MUST NOT bypass:

- price;
- eligibility;
- allocation;
- contribution limits;
- refund rights;
- or accounting requirements.

---

## 36. Participant Interface Requirements

The official presale interface MUST display:

- current presale state;
- verified contract address;
- network;
- reference price;
- selected payment asset;
- applicable conversion rate;
- rate timestamp or freshness;
- expected contribution amount;
- expected GFC entitlement;
- remaining Presale Allocation;
- cumulative reference value;
- soft-cap progress;
- start and end times;
- claim status;
- refund status;
- transaction risks;
- and applicable terms.

The interface MUST NOT display a purchase as completed before the blockchain transaction has achieved the required confirmation status.

---

## 37. User Confirmation

Before submitting a purchase, the interface SHOULD require the participant to review:

- payment asset;
- payment amount;
- GFC entitlement;
- contract address;
- network;
- transaction destination;
- soft-cap condition;
- refund condition;
- token-claim timing;
- and principal risks.

The participant MUST retain final control over wallet signing.

The interface MUST NOT conceal or rewrite material wallet transaction details.

---

## 38. Public Presale Records

The production presale SHOULD make the following publicly reviewable:

- official contract address;
- verified source code;
- specification version;
- start and end timestamps;
- reference price;
- supported payment assets;
- pricing mechanism;
- configured soft cap;
- configured Presale Allocation;
- total allocated GFC;
- total recorded euro reference value;
- sale state;
- pause state;
- finalization result;
- amount of each payment asset held;
- amount withdrawn after success;
- amount refunded after failure;
- unclaimed token entitlement;
- unclaimed refunds;
- and unsold-token treatment.

---

## 39. Transparency Classification

Presale information MUST distinguish between:

### 39.1 Directly verified on-chain

Examples:

- contribution transactions;
- contract balances;
- purchase events;
- token entitlements;
- claims;
- refunds;
- withdrawals;
- and finalization state.

### 39.2 Project-authored information

Examples:

- intended use of proceeds;
- operational explanations;
- expected milestones;
- and public rationale.

### 39.3 Externally supplied information

Examples:

- oracle data;
- compliance results;
- payment-provider records;
- and external reviews.

### 39.4 Independently reviewed information

Information must not be described as independently reviewed unless the reviewer, scope, and limitations are documented.

---

## 40. Use of Proceeds

Before launch, GFC MUST publish a clear intended-use framework for successful presale proceeds.

The framework SHOULD identify:

- use categories;
- prohibited uses;
- custody;
- approval requirements;
- reporting cadence;
- and treatment of material deviations.

A stated intended use does not prove actual use.

Actual use requires:

- transaction evidence;
- supporting documentation;
- reconciliation;
- and appropriate transparency status.

The successful completion of the presale does not by itself prove that proceeds were used effectively or created impact.

---

## 41. No Guaranteed Outcomes

The presale MUST NOT be communicated as guaranteeing:

- token appreciation;
- market liquidity;
- exchange listing;
- staking returns;
- governance influence;
- project completion;
- charitable results;
- social impact;
- tax treatment;
- or regulatory approval.

The soft cap indicates only that a predefined contribution threshold was reached.

It does not prove that all project objectives can or will be completed.

---

## 42. Privacy

### 42.1 On-chain exposure

Participants must be informed that blockchain activity may publicly expose:

- wallet addresses;
- contribution amounts;
- payment assets;
- timestamps;
- claims;
- and refunds.

### 42.2 Personal data

Personal data MUST NOT be placed directly on-chain merely to demonstrate eligibility or transparency.

### 42.3 Eligibility records

Where off-chain eligibility checks are required, records MUST be:

- access-controlled;
- purpose-limited;
- protected;
- retained according to applicable requirements;
- and separated from public blockchain records where possible.

### 42.4 Address linkage

GFC MUST NOT publicly link wallet addresses to participant identities without lawful basis and appropriate disclosure.

---

## 43. Security Requirements

Before production activation:

- contract source code MUST be complete;
- automated tests MUST cover purchase, claim, refund, finalization, pause, and withdrawal behavior;
- accounting invariants MUST be tested;
- supported-asset behavior MUST be tested;
- oracle-failure cases MUST be tested;
- allocation exhaustion MUST be tested;
- rounding MUST be tested;
- state transitions MUST be tested;
- role boundaries MUST be tested;
- and independent security review MUST be completed.

Production source code MUST be publicly verifiable through an appropriate Base block explorer.

---

## 44. Required Presale Invariants

The implementation MUST preserve at least the following invariants:

1. Total participant entitlement never exceeds the configured Presale Allocation.
2. The presale never creates additional GFC.
3. A contribution is counted only once.
4. A contribution cannot be both successfully refunded and used to claim GFC.
5. A token entitlement cannot be claimed more than once.
6. Funds required for valid refunds cannot be withdrawn.
7. Proceeds cannot be withdrawn before successful finalization.
8. Price cannot change after activation.
9. Soft-cap accounting is deterministic.
10. Failed-sale participants retain valid refund rights.
11. Successful-sale participants retain valid claim rights.
12. Unsold tokens cannot be distributed through undocumented discretion.
13. Administrative roles cannot silently alter participant records.
14. Contract balances and recorded obligations remain reconcilable.
15. Supported payment assets cannot bypass allocation or price controls.

---

## 45. Monitoring

The production system SHOULD monitor:

- activation;
- purchases;
- unusual contribution patterns;
- allocation exhaustion;
- oracle freshness;
- oracle deviation;
- pauses;
- role changes;
- finalization;
- claims;
- refunds;
- withdrawals;
- unsold-token movement;
- and contract-balance discrepancies.

Material alerts SHOULD be reviewed by defined operational and security roles.

Monitoring infrastructure does not replace contract-level enforcement.

---

## 46. Incident Handling

Potential presale incidents include:

- contract exploit;
- pricing failure;
- stale oracle;
- incorrect conversion;
- contribution-accounting error;
- token underfunding;
- refund shortfall;
- unauthorized withdrawal;
- compromised administrator;
- fake presale interface;
- fake contract address;
- payment-asset failure;
- privacy breach;
- and specification deviation.

A material incident SHOULD be documented with:

- incident identifier;
- detection time;
- affected component;
- affected participants;
- affected assets;
- containment action;
- authority used;
- financial impact;
- refund or claim impact;
- remediation;
- disclosure status;
- and continuing risk.

---

## 47. Fake Contract and Interface Protection

Official presale addresses MUST be published through authenticated GFC channels and versioned repository releases.

The official interface MUST display the verified contract address.

Participants SHOULD be directed to verify:

- network;
- contract address;
- source verification;
- and transaction destination.

GFC MUST NOT rely solely on social-media posts to authenticate a production contract.

A compromised frontend MUST NOT be able to redirect a valid participant transaction without the changed destination being visible in the wallet confirmation.

---

## 48. Disputes and Corrections

The final operational process MUST define how participants may report:

- incorrect entitlement;
- failed claim;
- failed refund;
- unsupported asset interaction;
- conversion dispute;
- duplicate record;
- interface misrepresentation;
- or suspected unauthorized activity.

Corrections MUST NOT allow administrators to arbitrarily alter valid purchase records.

Any manual correction process MUST be:

- narrowly scoped;
- evidenced;
- approved;
- logged;
- and publicly reconcilable where possible.

---

## 49. Conformance

A presale implementation conforms to this specification only when:

- it identifies an applicable versioned release;
- no presale is represented as live before activation;
- the price is enforced beyond the frontend;
- total allocation does not exceed 150,000,000 GFC;
- the presale cannot mint additional GFC;
- contribution accounting is deterministic;
- participant tokens are claimable only after successful finalization;
- funds remain unavailable before successful finalization;
- soft-cap failure creates enforceable refund rights;
- successful finalization preserves valid token claims;
- administrative authority is documented;
- critical parameters cannot be silently changed after activation;
- unsold-token treatment was defined before launch;
- official addresses are authenticated;
- and material deviations are disclosed.

---

## 50. Non-Conformance

Presale non-conformance includes:

- frontend-only price enforcement;
- unauthorized parameter changes;
- undisclosed payment assets;
- allocation beyond the approved maximum;
- additional minting;
- premature proceeds withdrawal;
- insufficient refund reserves;
- removal of valid refund rights;
- invalidation of valid claims;
- manipulation of purchase records;
- hidden administrator authority;
- undocumented unsold-token movement;
- false presale-status communication;
- or concealment of a material implementation deviation.

Material non-conformance MAY require:

- pausing purchases;
- cancelling the presale;
- enabling refunds;
- disabling proceeds withdrawal;
- public disclosure;
- participant notification;
- contract migration;
- independent investigation;
- or security-incident treatment.

The specification MUST NOT be altered retrospectively merely to make non-conforming behavior appear compliant.

---

## 51. Presale Non-Goals

The presale does not aim to:

- guarantee financial returns;
- guarantee token appreciation;
- guarantee liquidity;
- guarantee listing on an exchange;
- guarantee staking income;
- create additional token supply;
- allow unlimited fundraising;
- provide project operators with early access to refundable funds;
- use frontend behavior as a substitute for contract enforcement;
- distribute tokens before failure risk has been resolved;
- remove human or legal responsibility through automation;
- treat blockchain transactions as proof of project impact;
- or conceal administrative authority.

---

## 52. Unresolved Presale Decisions

The following matters remain unresolved and MUST be completed before Stable status.

### 52.1 Payment assets

- supported assets;
- asset addresses;
- volatile asset policy;
- stablecoin policy;
- asset failure policy;
- and asset-removal authority.

### 52.2 Conversion

- oracle or pricing source;
- oracle contract addresses;
- update frequency;
- stale-price threshold;
- deviation limits;
- fallback behavior;
- and rounding formula.

### 52.3 Purchase limits

- minimum contribution;
- per-transaction maximum;
- per-wallet maximum;
- participant maximum;
- and anti-circumvention policy.

### 52.4 Eligibility

- jurisdiction restrictions;
- age requirements;
- identity requirements;
- allowlist mechanism;
- sanctions controls;
- and legal terms.

### 52.5 Contract architecture

- immutable or upgradeable deployment;
- pause scope;
- administrative roles;
- finalization implementation;
- and migration procedure.

### 52.6 Claims

- full or partial claiming;
- claim activation;
- claim interface;
- successor handling;
- and unclaimed entitlement reporting.

### 52.7 Refunds

- exact refund implementation;
- emergency migration;
- unsupported-token recovery;
- and participant-support procedure.

### 52.8 Proceeds

- proceeds-vault address;
- custody model;
- withdrawal threshold;
- withdrawal timing;
- asset-conversion policy;
- and reporting requirements.

### 52.9 Unsold tokens

- final destination;
- lock or burn treatment;
- execution authority;
- execution timing;
- and circulating-supply effect.

### 52.10 Security

- audit scope;
- test coverage;
- monitoring;
- incident severity;
- disclosure process;
- and emergency response.

---

## 53. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- supported payment assets are finalized;
- all payment-asset addresses are identified;
- pricing and conversion logic are finalized;
- oracle-failure behavior is finalized;
- rounding rules and test vectors are published;
- minimum and maximum contribution rules are finalized;
- eligibility requirements are resolved;
- exact start and end behavior are defined;
- contract state transitions are finalized;
- token claim mechanics are finalized;
- refund mechanics are finalized;
- contribution custody is finalized;
- proceeds destinations are finalized;
- withdrawal authority is finalized;
- unsold-token treatment is finalized;
- administrative roles are documented;
- authority-registry entries are prepared;
- upgradeability is finalized;
- pause behavior is finalized;
- migration behavior is finalized;
- off-chain contributions are explicitly excluded or fully specified;
- participant terms are prepared;
- privacy processes are documented;
- independent security review requirements are satisfied;
- contract source code is complete;
- test coverage is complete;
- deployment and verification procedures are prepared;
- public communication is consistent with the specification;
- and all related specifications are mutually consistent.

---

## 54. Final Presale Principles

The presale must preserve the following distinctions:

> A fixed displayed price is not sufficient unless the settlement mechanism enforces it.

> Reaching the soft cap is not the same as completing successful finalization.

> Participant funds are not project funds while refund rights remain active.

> A purchase entitlement is not the same as an immediately transferable token.

> A successful presale does not guarantee liquidity, returns, completion, or impact.

> Public on-chain records verify transactions, not the quality or outcome of subsequent spending.

The presale is credible only where price, allocation, custody, participant rights, authority, finalization, claims, refunds, and public communication remain consistent.

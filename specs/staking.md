# GFC Staking Specification

**Document ID:** GFC-STK-001  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Intended Production Network:** Base Mainnet  
**Production Chain ID:** 8453  
**Public Pilot Network:** Base Sepolia  
**Pilot Chain ID:** 84532  
**Last Updated:** 2026-08-30

---

## 1. Document Status

This document defines the current intended staking requirements for Global Foundation Coin (GFC).

It is normative because it defines intended requirements and prohibited behavior concerning:

- staking participation;
- staking principal;
- reward sources;
- reward accounting;
- non-inflationary constraints;
- staking-related authority;
- lock and withdrawal behavior;
- governance-related participation;
- migration;
- emergency behavior;
- transparency;
- and conformance.

Its maturity remains Draft.

At the current repository state:

- the **GFC Token / Economic Layer** is the current primary product focus;
- a public GFC pilot exists on **Base Sepolia**;
- no production GFC token is deployed on Base Mainnet;
- no production GFC staking system is operational;
- no production staking contract is established as official;
- no production staking reward pool is established as official;
- no production reward source is finalized;
- no production reward rate, APR, APY, lock period, reward duration, or governance right is established by this document;
- no production staking wallet or authority is established as official by this document;
- and no staking implementation is designated as conforming.

The current design direction is **hybrid and non-inflationary**.

The Base Sepolia pilot MUST NOT be interpreted as evidence that production staking exists or that any production staking rule has been implemented.

Current implementation and deployment status is maintained in [`../STATUS.md`](../STATUS.md).

---

## 2. Purpose

The purpose of this specification is to define a bounded staking architecture that can support participation without weakening the fixed-supply model or creating misleading return claims.

The intended staking design direction is hybrid.

A future staking system MAY combine:

- token rewards;
- governance-related participation;
- community-related benefits;
- or other explicitly specified utility.

The staking system MUST remain non-inflationary.

It MUST NOT create additional GFC beyond the fixed total supply of:

```text
1,000,000,000 GFC
```

This document does not establish:

- a guaranteed staking launch;
- a guaranteed reward rate;
- a guaranteed APY;
- a guaranteed lock duration;
- permanent reward availability;
- or unrestricted governance rights.

---

## 3. Relationship to the GFC Accountability Model

The long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

A staking system affects several parts of this model.

### Funds

Which GFC is deposited, locked, committed, rewarded, withdrawn, or distributed?

### Authority

Who may configure, pause, migrate, fund, or otherwise influence the staking system?

### Rules

How are eligibility, reward calculation, lock behavior, withdrawals, and participant rights defined?

### Decisions

Which authorized decisions affect staking configuration or operation?

### Outcomes

What staking rewards, participation rights, or other benefits result?

### Evidence

What on-chain or off-chain evidence supports the represented staking state?

Staking balances or rewards do not independently establish governance legitimacy, project impact, or financial return.

---

## 4. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are normative only when:

- they appear in uppercase;
- the containing document declares `Authority: Normative`;
- and the applicable version governs the implementation, process, or communication being evaluated.

Because this document is Draft, these requirements remain subject to formal review and versioned release.

---

## 5. Scope

This specification defines:

- staking terminology;
- staking principal;
- staking eligibility;
- reward-source requirements;
- non-inflationary reward constraints;
- reward accounting;
- reward-rate disclosure;
- reward sustainability;
- lock behavior;
- withdrawal behavior;
- early exit where applicable;
- governance-related participation;
- community-related benefits;
- staking authority;
- pause and emergency behavior;
- migration;
- security;
- transparency;
- public communication;
- and conformance.

---

## 6. Out of Scope

This document does not independently define:

- final production staking contract code;
- final staking contract address;
- final reward source;
- final reward allocation;
- final reward rate;
- final APR or APY;
- final reward duration;
- final staking lock period;
- final minimum or maximum stake;
- final early-exit policy;
- final penalty model;
- final governance rights;
- final community benefits;
- final staking-custody architecture;
- final pause model;
- final migration model;
- final tax treatment;
- legal classification;
- or regulatory treatment.

These matters MUST remain explicitly unresolved until established through the applicable specification and authenticated production records.

---

## 7. Core Staking Principles

### 7.1 Non-inflationary design

Staking MUST NOT increase the fixed GFC supply.

### 7.2 Explicit reward source

Every staking reward MUST have an identifiable and authorized source.

### 7.3 No guaranteed return

Staking MUST NOT be presented as guaranteed profit, guaranteed yield, guaranteed passive income, or capital preservation.

### 7.4 Principal and reward separation

Staking principal MUST remain distinguishable from staking rewards.

### 7.5 Authority visibility

Every material staking authority MUST be explicit and reviewable.

### 7.6 Prospective rule changes

Material staking parameter changes SHOULD apply prospectively and MUST NOT silently confiscate or retroactively alter already accrued participant rights.

### 7.7 Fixed-supply consistency

Reward accounting, migration, and emergency behavior MUST remain consistent with the fixed-supply token model.

### 7.8 Pilot and production separation

Testnet or pilot staking behavior MUST NOT be represented as production staking behavior.

---

## 8. Hybrid Staking

The current intended design direction is **hybrid staking**.

Hybrid staking MAY combine multiple forms of utility, including:

- token rewards;
- governance-related participation;
- community-related benefits;
- reputation or contribution recognition;
- or other explicitly specified non-inflationary benefits.

The exact combination remains unresolved.

The term `hybrid` MUST NOT be used to imply that all possible benefits are guaranteed or implemented.

---

## 9. Non-Inflationary Staking

The intended GFC staking model is non-inflationary.

No staking contract, governance role, administrator, migration process, or reward mechanism MAY mint additional GFC beyond the fixed supply.

Staking rewards MUST originate from:

- GFC already included within the fixed supply; or
- another explicitly specified non-minting economic source.

The final production reward source is unresolved.

This document does not assign staking rewards to:

- Ecosystem;
- Guardian Growth;
- Treasury Reserve;
- Liquidity Reserve;
- sell-fee proceeds;
- Impact Vault;
- Core Team;
- Presale;
- or any other specific allocation or economic flow.

Such a decision requires an applicable versioned specification.

---

## 10. Staking Principal

Staking principal is the amount of GFC deposited, committed, or otherwise placed under staking rules by a participant.

The production model MUST define how principal is represented.

Possible models MAY include:

- transfer to a staking contract;
- escrowed custody;
- lock without transfer;
- non-custodial accounting;
- or another explicitly specified mechanism.

The final custody model remains unresolved.

---

## 11. Principal Ownership and Custody

The production specification MUST define:

- who retains beneficial ownership of staked principal;
- who has technical custody;
- whether the participant can withdraw;
- whether the principal is transferable;
- whether the principal is subject to lock;
- whether an administrator can move principal;
- and what happens during pause, migration, or failure.

A staking contract MUST NOT be described as non-custodial if the implementation can transfer or redirect user principal without participant authorization under undisclosed conditions.

---

## 12. Staking Eligibility

Final staking eligibility remains unresolved.

The production specification MUST define, where applicable:

- eligible GFC balances;
- minimum stake;
- maximum stake;
- participant eligibility;
- address restrictions;
- jurisdictional restrictions;
- lock requirements;
- and whether specific allocation-controlled balances are excluded.

Eligibility rules MUST NOT be implemented solely through an official frontend where direct contract interaction would bypass them.

---

## 13. Restricted GFC Eligibility

GFC subject to an existing lock or vesting restriction MUST NOT enter staking in a way that defeats the original restriction.

This includes:

- Impact Vault GFC subject to the intended 50-year lock; and
- Core Team GFC subject to the intended 19-year linear vesting.

If future specifications permit restricted GFC to participate in staking, they MUST define:

- custody;
- reward ownership;
- governance participation;
- withdrawal restrictions;
- migration behavior;
- and preservation of the original restriction.

Staking MUST NOT create early transferability of restricted principal.

---

## 14. Reward Source

The final production reward source is unresolved.

Before production activation, the applicable specification MUST identify:

- source allocation or economic source;
- authenticated custody address or contract;
- amount reserved for rewards;
- authority controlling the source;
- maximum distributable amount;
- replenishment rules, if any;
- and relationship to other GFC economic components.

The reward source MUST be consistent with [`economic-flows.md`](economic-flows.md).

No reward source MAY be inferred from marketing language or wallet labels.

---

## 15. Reward Pool

If a dedicated reward pool is used, the production model MUST define:

- initial funding amount;
- source;
- custody;
- authority;
- replenishment rules;
- maximum capacity;
- accounting;
- and residual treatment.

A reward pool balance MUST NOT be represented as newly minted supply.

---

## 16. Reward Accounting

A conforming staking implementation MUST maintain deterministic and reconcilable reward accounting.

The model MUST define:

- reward basis;
- accrual period;
- eligible principal;
- calculation order;
- precision;
- rounding;
- maximum accrued reward;
- reward funding availability;
- claim state;
- distributed reward;
- and residual reward balance.

Reward accounting MUST NOT create participant claims exceeding the authorized available reward source.

---

## 17. Reward Rate

The final reward rate is unresolved.

The production specification MUST define whether the rate is:

- fixed;
- variable;
- schedule-based;
- utilization-dependent;
- governance-adjustable within limits;
- or another explicitly specified model.

Any configurable reward-rate authority MUST be bounded.

A role MUST NOT possess undisclosed authority to create unbounded reward obligations.

---

## 18. APR and APY

Any displayed APR, APY, estimated yield, or equivalent metric MUST identify:

- calculation basis;
- reward source;
- applicable period;
- compounding assumption;
- lock assumption;
- variability;
- exclusions;
- and material risk.

APR or APY MUST NOT be represented as guaranteed.

A frontend estimate MUST NOT override actual contract accounting.

---

## 19. Reward Duration

The final reward duration remains unresolved.

Before production activation, the applicable specification MUST define:

- start condition;
- end condition;
- reward exhaustion behavior;
- whether rewards may be replenished;
- authority over replenishment;
- and participant treatment after reward exhaustion.

Reward availability MUST NOT be represented as permanent unless technically and economically supported.

---

## 20. Reward Sustainability

The staking system MUST be designed so that authorized reward obligations do not exceed the available reward source.

Before production activation, the project SHOULD evaluate:

- total reward capacity;
- expected staking participation;
- maximum reward obligation;
- reward duration;
- concentration risk;
- and depletion behavior.

A high displayed yield MUST NOT be funded by undisclosed inflation.

---

## 21. Reward Accrual

The production implementation MUST define when rewards begin accruing.

Potential start conditions MAY include:

- deposit time;
- lock activation;
- epoch start;
- or another deterministic event.

The start rule MUST be explicit and testable.

No reward MUST accrue before the applicable eligibility conditions are satisfied.

---

## 22. Reward Claiming

If rewards are claimable separately from principal, the production model MUST define:

- claim eligibility;
- claim frequency;
- minimum claim amount, if any;
- destination;
- fee treatment;
- rounding;
- accounting state;
- and repeated-claim protection.

A reward claim MUST NOT exceed accrued entitlement.

The implementation MUST prevent double claiming.

---

## 23. Automatic Reward Distribution

If rewards are distributed automatically rather than claimed, the implementation MUST define:

- trigger;
- recipient;
- amount;
- calculation;
- failure behavior;
- and reconciliation.

Automatic distribution MUST NOT create obligations beyond the available reward source.

---

## 24. Compounding

Automatic or manual compounding is not currently specified.

If compounding is later supported, the production specification MUST define:

- whether rewards become principal;
- how reward eligibility changes;
- lock implications;
- accounting;
- and participant disclosure.

Compounding MUST NOT be assumed when displaying APY unless it is actually supported.

---

## 25. Staking Lock

The final staking lock model remains unresolved.

A production staking design MAY use:

- no lock;
- fixed lock periods;
- selectable lock periods;
- cooldowns;
- withdrawal delays;
- or another explicitly specified model.

Any lock MUST define:

- commencement;
- duration;
- withdrawal eligibility;
- early-exit rules;
- migration treatment;
- and emergency behavior.

A staking lock MUST NOT be described as immutable unless the complete deployed architecture makes unauthorized change impossible.

---

## 26. Withdrawal

The production system MUST define:

- who may withdraw principal;
- when withdrawal is permitted;
- whether partial withdrawal is permitted;
- withdrawal delay;
- reward effect;
- lock effect;
- destination;
- and failure behavior.

A participant MUST NOT lose principal through undocumented withdrawal restrictions.

---

## 27. Early Exit

Whether early exit is permitted remains unresolved.

If early exit is permitted, the applicable specification MUST define:

- eligibility;
- notice or cooldown;
- reward treatment;
- penalty, if any;
- destination of any penalty;
- accounting;
- and participant disclosure.

An early-exit penalty MUST NOT be introduced through an undocumented administrative change.

---

## 28. Penalties and Slashing

No slashing model is currently established.

The production staking system MUST NOT confiscate principal or rewards through a slashing, penalty, or forfeiture mechanism unless that mechanism is explicitly specified before activation.

If any penalty model is later proposed, it requires:

- defined triggering conditions;
- bounded effect;
- authority;
- dispute treatment;
- security review;
- and participant disclosure.

---

## 29. Governance-Related Participation

Hybrid staking MAY include governance-related participation.

The exact rights remain unresolved.

The production specification MUST define whether staked GFC provides:

- advisory participation;
- proposal rights;
- voting weight;
- delegation;
- veto-related participation;
- or no governance rights.

Staking MUST NOT automatically grant unrestricted authority over:

- Treasury Reserve;
- Impact Vault;
- Core Team vesting;
- production contracts;
- privileged keys;
- protected evidence;
- legal obligations;
- or impact-verification status.

Governance-related staking rights MUST remain consistent with [`governance-constraints.md`](governance-constraints.md).

---

## 30. Community-Related Benefits

Hybrid staking MAY include community-related benefits.

No specific benefit is established by this Draft.

Any future benefit MUST be:

- explicitly defined;
- accurately represented;
- economically sustainable where it has economic value;
- and separated from governance authority where applicable.

A community benefit MUST NOT be described as a financial return unless that classification is actually appropriate and supported.

---

## 31. Voting Power and Staked GFC

If staking affects voting power, the production governance specification MUST define:

- eligible staked balances;
- voting-weight formula;
- snapshots;
- delegation;
- unstaking effect;
- lock interaction;
- borrowed-token treatment;
- and manipulation resistance.

Temporary staking MUST NOT silently create disproportionate governance authority without the applicable rules addressing that risk.

---

## 32. Staking Authority

Any production staking authority MUST be consistent with [`roles-and-authority.md`](roles-and-authority.md).

Potential material authorities MAY include:

- contract deployment;
- reward funding;
- reward-rate configuration;
- eligibility configuration;
- lock configuration;
- pause;
- migration;
- recovery;
- and governance-integration configuration.

No such role is established as active by this Draft.

---

## 33. Parameter Mutability

The production staking system MUST disclose which parameters are:

- immutable;
- configurable;
- upgradeable;
- or migratable.

Any configurable parameter MUST define:

- authorized role;
- permitted range;
- approval requirements;
- timelock where applicable;
- effective timing;
- and public record.

Material changes SHOULD apply prospectively.

---

## 34. Reward-Rate Changes

If reward rates are configurable, a rate change MUST NOT silently alter rewards already accrued under the prior rules.

The final model MUST define:

- effective block or timestamp;
- treatment of existing positions;
- treatment of new positions;
- maximum permitted change;
- and historical record.

Retroactive reduction of already accrued rewards is NOT RECOMMENDED and MUST NOT occur through undisclosed authority.

---

## 35. Funding Changes

Changing or replenishing the reward source is a material economic action.

The applicable process MUST identify:

- source;
- amount;
- authority;
- transaction;
- effect on reward duration;
- and accounting classification.

Funding changes MUST NOT create new GFC supply.

---

## 36. Pause Authority

A production staking system MAY include pause functionality if justified.

The final specification MUST define whether a pause affects:

- new stakes;
- reward accrual;
- reward claims;
- principal withdrawals;
- governance rights;
- migrations;
- or another function.

A pause MUST NOT silently confiscate participant principal or already accrued rewards.

Where safety permits, participant withdrawal SHOULD remain available during prolonged disruption.

---

## 37. Emergency Behavior

Emergency authority MUST remain narrow.

An emergency MUST NOT justify:

- minting new GFC;
- confiscating participant principal;
- canceling accrued rewards without applicable rules;
- converting staking assets to unrestricted project funds;
- or granting permanent administrative authority.

Emergency behavior MUST be consistent with [`security-model.md`](security-model.md).

---

## 38. Recovery

Staking recovery functionality remains unresolved.

If recovery is implemented, it MUST define:

- trigger;
- scope;
- authority;
- approvals;
- affected principal;
- affected rewards;
- destination;
- participant rights;
- and historical record.

Recovery MUST NOT become an undocumented master withdrawal mechanism.

---

## 39. Migration

A staking migration MUST preserve accurate participant economic state.

The migration model MUST define, where applicable:

- principal;
- accrued rewards;
- claimed rewards;
- lock state;
- unlock eligibility;
- governance-related rights;
- source contract;
- destination contract;
- authority;
- and migration transaction.

Migration MUST NOT create:

- duplicate principal;
- duplicate reward entitlement;
- additional canonical GFC supply;
- or weakened participant restrictions.

---

## 40. Upgradeability

The final production staking upgrade model remains unresolved.

If staking is upgradeable, the deployment record MUST identify:

- upgrade authority;
- approval threshold;
- timelock;
- emergency bypass;
- storage compatibility;
- participant state migration;
- and public notification.

An upgrade MUST NOT silently:

- mint new GFC;
- confiscate principal;
- reduce accrued rewards;
- broaden unrelated governance authority;
- or introduce hidden withdrawal authority.

---

## 41. Principal Security

The staking system MUST protect participant principal against:

- unauthorized transfer;
- administrator withdrawal;
- incorrect accounting;
- double withdrawal;
- reentrancy;
- storage corruption;
- migration duplication;
- and hidden penalty mechanisms.

Security requirements are defined in [`security-model.md`](security-model.md).

---

## 42. Reward Security

Reward accounting MUST protect against:

- double claims;
- over-accrual;
- underflow or overflow;
- rounding exploitation;
- unauthorized rate changes;
- reward-pool insolvency;
- incorrect eligibility;
- timestamp manipulation assumptions;
- and migration duplication.

---

## 43. External Token and Contract Risk

If staking interacts with any external contract or token, the implementation MUST evaluate:

- reentrancy;
- non-standard token behavior;
- transfer failure;
- callbacks;
- malicious approvals;
- allowance risk;
- dependency failure;
- and upgrade risk.

The current staking design does not establish any external dependency.

---

## 44. Staking Economic Invariants

The following high-level invariants apply.

### 44.1 Fixed supply

```text
canonical GFC supply ≤ 1,000,000,000 GFC
```

### 44.2 Principal conservation

Subject to explicitly specified penalties, migration, or withdrawal:

```text
participant principal must not disappear through undocumented behavior
```

### 44.3 Reward ceiling

```text
distributed rewards ≤ authorized available reward source
```

### 44.4 Accrual

```text
claimed rewards ≤ accrued rewards
```

### 44.5 No duplicate entitlement

Migration or accounting MUST NOT create duplicate principal or reward claims.

### 44.6 Restricted principal

Staking MUST NOT weaken an existing Impact Vault or Core Team restriction.

---

## 45. Testing Requirements

Before production reliance, testing SHOULD cover:

- staking entry;
- staking exit;
- principal accounting;
- reward accrual;
- reward claiming;
- repeated claims;
- reward exhaustion;
- rounding;
- parameter boundaries;
- unauthorized administration;
- lock behavior;
- early exit where applicable;
- pause behavior;
- migration;
- recovery;
- and failure modes.

Tests SHOULD verify both intended and prohibited behavior.

---

## 46. Invariant and Fuzz Testing

Where appropriate, invariant or fuzz testing SHOULD verify:

- total GFC supply never exceeds the fixed maximum;
- distributed rewards never exceed authorized reward assets;
- claimed rewards never exceed accrued rewards;
- principal cannot be withdrawn by unauthorized roles;
- participant state remains internally consistent;
- migration does not duplicate entitlement;
- and restricted allocation rules remain preserved.

Passing tests do not establish absence of vulnerabilities.

---

## 47. Reward Insolvency

The staking design MUST avoid creating reward obligations that cannot be satisfied by the authorized reward source.

If a production design permits variable reward funding, it MUST define behavior when reward funding becomes insufficient.

The system MUST NOT silently create new GFC to satisfy a reward shortfall.

---

## 48. Frontend Representation

A staking frontend MUST accurately represent actual contract behavior.

It MUST NOT:

- display a guaranteed APY where none exists;
- describe rewards as permanent;
- hide lock periods;
- hide withdrawal restrictions;
- hide configurable parameters;
- hide upgradeability;
- hide staking authority;
- or describe a planned feature as active.

A frontend estimate does not create participant entitlement unless the applicable rules and implementation support it.

---

## 49. Transparency

A production staking record SHOULD make it possible to review:

- staking contract;
- network;
- total principal;
- participant position where public and appropriate;
- reward source;
- reward pool balance;
- reward-rate rules;
- distributed rewards;
- remaining authorized reward capacity;
- lock rules;
- withdrawal rules;
- privileged authority;
- pause status;
- upgradeability;
- migration history;
- and known deviations.

Protected information MAY remain non-public where justified.

---

## 50. Transparency Registry Relationship

The planned Transparency Registry MAY later record:

- staking implementation versions;
- authority changes;
- reward-source changes;
- parameter changes;
- pause events;
- migration;
- corrections;
- incidents;
- and status history.

The Registry is intended to operate as a versioned historical record rather than a permanent approval badge.

No complete production Transparency Registry is currently deployed.

A Registry status MUST NOT override authenticated staking contract state.

---

## 51. Economic-Flow Relationship

Staking economic flows MUST remain consistent with [`economic-flows.md`](economic-flows.md).

At minimum, production accounting MUST distinguish:

- staking principal inflow;
- staking principal custody;
- reward funding;
- reward accrual;
- reward distribution;
- principal withdrawal;
- migration;
- and residual reward assets.

Internal staking transfers MUST NOT be reported as new external funding.

---

## 52. Allocation Relationship

The final reward source MUST be reconciled with [`allocations.md`](allocations.md).

No allocation is assigned as the reward source by this Draft.

If a future specification assigns GFC from an allocation to staking rewards, that decision MUST define:

- amount;
- authority;
- economic purpose;
- custody;
- maximum distribution;
- and effect on the originating allocation.

---

## 53. Vesting and Lock Relationship

Staking MUST remain consistent with [`vesting-and-unlocks.md`](vesting-and-unlocks.md).

Staking MUST NOT be used to:

- unlock Impact Vault GFC;
- accelerate Core Team vesting;
- convert unvested GFC into transferable staking principal;
- or create unrestricted claims against restricted GFC.

---

## 54. Governance Relationship

Any staking-based participation MUST remain consistent with:

- [`roles-and-authority.md`](roles-and-authority.md); and
- [`governance-constraints.md`](governance-constraints.md).

Staking participation is not automatically binding governance authority.

The final legal and technical effect of any staking-related vote or proposal right MUST be disclosed.

---

## 55. Pilot and Production Separation

The public Base Sepolia pilot does not establish a production staking system.

Pilot balances, test staking contracts, demo interfaces, or experimental reward mechanisms MUST NOT be represented as:

- production staking;
- production reward funding;
- production APY;
- production governance participation;
- or production participant entitlement.

Production staking requires separate authenticated implementation and deployment records.

---

## 56. Public Communication Requirements

Public communication MUST accurately distinguish between:

- Draft staking design;
- proposed staking;
- specified staking;
- implemented staking;
- tested staking;
- pilot staking;
- deployed staking;
- active staking;
- and operational production staking.

Public communication MUST NOT imply:

- staking is live when it is not;
- guaranteed returns;
- guaranteed APY;
- guaranteed reward duration;
- permanent reward availability;
- unrestricted governance rights;
- inflation-funded rewards under the current fixed-supply model;
- or production status based on a pilot.

---

## 57. No Financial Guarantee

Staking MUST NOT be represented as guaranteeing:

- profit;
- passive income;
- capital preservation;
- token appreciation;
- liquidity;
- repayment;
- or financial independence.

Participant outcomes may depend on:

- token price;
- reward availability;
- lock behavior;
- smart-contract risk;
- market liquidity;
- tax treatment;
- and other external factors.

---

## 58. Security and Risk Disclosure

A production staking interface SHOULD disclose material risks including, where applicable:

- smart-contract risk;
- key and authority risk;
- lock-up risk;
- liquidity risk;
- token-price risk;
- reward variability;
- reward exhaustion;
- upgrade risk;
- pause risk;
- migration risk;
- governance risk;
- and dependency risk.

Risk disclosure MUST NOT be used as a substitute for sound technical controls.

---

## 59. Conformance

A staking implementation conforms to this specification only when:

- it identifies an applicable versioned staking specification;
- canonical GFC supply remains fixed;
- reward funding is non-inflationary;
- the reward source is authenticated and disclosed;
- reward accounting is deterministic;
- principal accounting is correct;
- privileged authority is disclosed;
- participant rights match represented rules;
- existing allocation locks or vesting are not weakened;
- migration does not duplicate entitlement;
- production status is authenticated;
- pilot status is not misrepresented;
- and material deviations are documented.

A frontend, APY display, wallet label, or marketing statement does not establish conformance.

---

## 60. Staking Non-Conformance

Staking non-conformance includes:

- minting GFC to fund rewards contrary to the fixed-supply model;
- undisclosed reward source;
- rewards exceeding authorized funding;
- double reward claims;
- unauthorized principal withdrawal;
- undisclosed lock;
- undisclosed penalty;
- hidden parameter authority;
- retroactive confiscation of accrued rewards;
- migration that duplicates principal or rewards;
- staking that weakens Impact Vault or Core Team restrictions;
- guaranteed-yield claims unsupported by the system;
- pilot staking represented as production staking;
- or public claims materially stronger than authenticated behavior supports.

Material non-conformance MAY require:

- pause;
- correction;
- reward reconciliation;
- authority revocation;
- migration;
- participant remediation;
- public clarification;
- security review;
- governance review;
- or incident treatment.

A specification MUST NOT be rewritten retrospectively merely to conceal staking non-conformance.

---

## 61. Change Classification

A material staking change includes a change to:

- reward source;
- reward rate;
- reward duration;
- eligibility;
- principal custody;
- lock period;
- early exit;
- penalties;
- governance-related rights;
- reward accounting;
- pause authority;
- upgradeability;
- migration;
- or participant withdrawal rights.

A breaking staking change requires:

- explicit versioning;
- rationale;
- economic analysis;
- security analysis;
- governance analysis;
- participant-rights analysis;
- implementation analysis;
- migration analysis where relevant;
- and updated public communication.

Material staking behavior MUST NOT be changed solely through frontend updates or informal statements.

---

## 62. Current Unresolved Requirements

The following matters remain unresolved unless separately established by a later versioned specification or authenticated implementation record:

- final staking contract architecture;
- final principal-custody model;
- minimum stake, if any;
- maximum stake, if any;
- final reward source;
- reward-pool amount;
- reward rate;
- APR or APY methodology;
- reward duration;
- reward calculation;
- reward accrual start;
- claim mechanics;
- compounding;
- lock model;
- lock duration;
- withdrawal delay;
- early exit;
- penalty model;
- governance-related participation;
- community-related benefits;
- reward-rate mutability;
- reward-funding authority;
- pause behavior;
- emergency behavior;
- recovery;
- migration;
- upgradeability;
- production staking authority;
- production contract address;
- and production activation criteria.

These unresolved matters MUST NOT be represented as completed or finalized.

---

## 63. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- the staking principal-custody model is finalized;
- eligibility rules are finalized;
- restricted-GFC treatment is finalized;
- reward source is finalized;
- reward funding amount or funding model is finalized;
- reward accounting is finalized;
- reward-rate model is finalized;
- reward duration is finalized;
- reward exhaustion behavior is finalized;
- claim or distribution mechanics are finalized;
- compounding is finalized or explicitly excluded;
- lock model is finalized;
- withdrawal rules are finalized;
- early-exit rules are finalized or explicitly excluded;
- penalties are finalized or explicitly excluded;
- governance-related rights are finalized or explicitly excluded;
- community-related benefits are finalized or explicitly excluded;
- parameter mutability is finalized;
- pause behavior is finalized or explicitly excluded;
- emergency behavior is finalized;
- recovery is finalized or explicitly excluded;
- migration is finalized;
- upgradeability is finalized;
- staking authority is finalized;
- staking security invariants are mapped to the intended implementation;
- economic-flow accounting is finalized;
- transparency requirements are finalized;
- Base Sepolia pilot and Base Mainnet production staking terminology are consistently separated;
- and all related specifications are mutually consistent.

---

## 64. Related Specifications

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
- [`presale.md`](presale.md);
- [`transparency-model.md`](transparency-model.md);
- and repository-level [`../STATUS.md`](../STATUS.md).

Where another Draft specification conflicts with this document, the conflict MUST be resolved explicitly before Stable status.

---

## 65. Final Staking Principles

The GFC staking model preserves the following distinctions:

> Staking is not guaranteed profit.

> APY is not a guarantee.

> Reward availability is not permanent unless funded and specified accordingly.

> Staking principal is not the same as staking reward.

> Staking rewards must not create additional GFC under the current fixed-supply model.

> A reward source must be explicit.

> No allocation is the staking reward source unless an applicable specification says so.

> Staking does not automatically create unrestricted governance authority.

> Locked or unvested GFC must not become freely transferable through staking.

> A pause must not silently confiscate principal or accrued rewards.

> Migration must not duplicate principal or reward entitlement.

> Pilot staking does not establish production staking.

The objective is to create a staking design that is economically bounded, non-inflationary, transparent about its reward source and risks, and consistent with GFC's long-term authority and accountability constraints.

# GFC Vesting and Unlocks Specification

**Document ID:** GFC-VEST-001  
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

This document defines the current intended lock, vesting, release, and unlock constraints for Global Foundation Coin (GFC) allocations.

It is normative because it defines intended restrictions concerning:

- the Impact Vault;
- the Core Team allocation;
- lock duration;
- vesting duration;
- release eligibility;
- acceleration prohibitions;
- migration;
- recovery;
- authority;
- disclosure;
- and conformance.

Its maturity remains Draft.

At the current repository state:

- the **GFC Token / Economic Layer** is the current primary product focus;
- a public GFC pilot exists on **Base Sepolia**;
- no production GFC token is deployed on Base Mainnet;
- no production Impact Vault contract is established as official;
- no production Core Team vesting contract is established as official;
- no production lock or vesting wallet is established as official by this document;
- no production lock-start timestamp is established;
- no production vesting-start timestamp is established;
- no production unlock transaction is authorized by this document;
- and no production lock or vesting implementation is designated as conforming.

The Base Sepolia pilot MUST NOT be interpreted as evidence that the production lock or vesting mechanisms described here have been deployed.

Current implementation and deployment status is maintained in [`../STATUS.md`](../STATUS.md).

---

## 2. Purpose

The purpose of this specification is to ensure that long-term GFC allocation commitments cannot be reduced to informal promises.

The specification defines the minimum normative constraints for:

1. the **Impact Vault**, intended to contain **250,000,000 GFC** and remain locked for **50 years**; and
2. the **Core Team** allocation, intended to contain **50,000,000 GFC** and vest **linearly over 19 years**.

The objective is to make it possible to review whether:

- tokens are genuinely restricted;
- release occurs only when permitted;
- privileged roles cannot accelerate access;
- migrations preserve restrictions;
- recovery does not become a bypass;
- public claims match actual contract state;
- and historical release behavior remains reconstructable.

This document does not establish final production timestamps, beneficiaries, custody addresses, or contract implementations.

---

## 3. Relationship to the GFC Accountability Model

The long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

Locks and vesting are primarily **Rules** applied to **Funds**.

For any material release or unlock, the system SHOULD make it possible to reconstruct:

1. which allocation was affected;
2. what amount was restricted;
3. which authority, if any, was permitted to act;
4. which rule made an amount eligible for release;
5. which decision or transaction caused release;
6. what amount became transferable;
7. and what evidence supports the represented status.

A wallet label is not a lock.

A written promise is not vesting.

A timestamp displayed by a frontend is not sufficient evidence of enforceable restriction.

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

- lock terminology;
- vesting terminology;
- unlock terminology;
- Impact Vault lock requirements;
- Core Team vesting requirements;
- release eligibility;
- start and end requirements;
- acceleration restrictions;
- migration constraints;
- recovery constraints;
- administrative authority;
- upgradeability constraints;
- public status representation;
- disclosure requirements;
- testing expectations;
- security invariants;
- and conformance.

---

## 6. Out of Scope

This document does not independently define:

- final production contract source code;
- final production contract addresses;
- final wallet addresses;
- final beneficiaries;
- final legal ownership;
- final beneficiary percentages within the Core Team allocation;
- final lock-start timestamp;
- final vesting-start timestamp;
- final cliff, if any;
- final claim frequency;
- final release interval;
- final post-lock Impact Vault purpose;
- final Core Team succession process;
- final Core Team reassignment process;
- final revocation model;
- final multisig or signer configuration;
- final treasury use;
- final staking mechanics;
- final presale mechanics;
- final liquidity strategy;
- or legal and tax treatment.

These matters MUST be resolved by the applicable specifications or authenticated production records before they become operationally relevant.

---

## 7. Canonical Allocation Constraints

The current Draft allocation model includes the following long-term restrictions.

| Allocation | Amount | Share of Total Supply | Current Intended Constraint |
|---|---:|---:|---|
| Impact Vault | 250,000,000 GFC | 25% | 50-year lock |
| Core Team | 50,000,000 GFC | 5% | 19-year linear vesting |

The complete allocation model is defined in [`allocations.md`](allocations.md).

These restrictions are intended production commitments.

They are not represented as technically enforced until authenticated production implementation and on-chain state support the claim.

---

## 8. Lock and Vesting Are Distinct

A **lock** and **vesting** MUST NOT be treated as equivalent.

### 8.1 Lock

A lock prevents transfer, withdrawal, or release before defined conditions are satisfied.

A lock does not necessarily create gradual entitlement.

### 8.2 Vesting

Vesting causes entitlement to become available progressively according to a defined schedule.

### 8.3 Impact Vault

The Impact Vault is currently specified as a **50-year lock**.

This specification does not currently define it as a 50-year linear vesting schedule.

### 8.4 Core Team

The Core Team allocation is currently specified as **19-year linear vesting**.

It MUST NOT be represented as fully locked for 19 years if portions become vested and available during that period.

---

## 9. General Restriction Principles

### 9.1 Technical enforcement

A production lock or vesting commitment SHOULD be technically enforceable where technically feasible.

### 9.2 No hidden bypass

No privileged path MAY silently defeat the represented restriction.

### 9.3 Exact status

Public communication MUST distinguish between:

- allocated;
- locked;
- unvested;
- vested;
- vested but unclaimed;
- claimable;
- claimed;
- unlocked;
- transferred;
- and migrated.

### 9.4 Restriction before convenience

Operational inconvenience does not justify weakening a long-term restriction.

### 9.5 Authority visibility

Any authority capable of affecting a lock, vesting schedule, beneficiary, migration, recovery, or release MUST be disclosed.

### 9.6 Historical integrity

Material changes and releases SHOULD remain historically reviewable.

---

## 10. Restriction Start Requirements

A production restriction MUST identify an unambiguous commencement point.

The applicable production specification or deployment record MUST define, where relevant:

- commencement event;
- commencement timestamp;
- applicable network;
- timestamp source;
- whether deployment time is relevant;
- whether allocation funding time is relevant;
- and whether any administrative initialization step is required.

This document does not establish the final commencement event for either the Impact Vault or Core Team vesting.

A start date MUST NOT be inferred solely from:

- publication of this Draft;
- project creation;
- Base Sepolia pilot deployment;
- token concept creation;
- repository creation;
- website publication;
- or another unrelated event.

---

## 11. Time Measurement

The production implementation MUST define the time model used for lock and vesting calculations.

The model MUST specify:

- timestamp source;
- duration calculation;
- treatment of leap years where relevant;
- rounding;
- minimum granularity;
- boundary behavior;
- and final release condition.

Time calculations MUST be deterministic and testable.

A frontend MUST NOT display a more precise unlock or vesting schedule than the underlying implementation actually enforces.

---

# Impact Vault

## 12. Impact Vault Allocation

The Impact Vault allocation is:

```text
250,000,000 GFC
```

representing:

```text
25% of total GFC supply
```

The intended restriction is:

```text
50-year lock
```

The detailed production implementation remains unresolved.

---

## 13. Impact Vault Lock Requirement

The production Impact Vault MUST prevent release of the locked allocation before the applicable 50-year lock has expired, except where a later versioned specification introduces a stricter restriction.

No ordinary administrative function MAY permit early withdrawal.

The implementation MUST NOT contain an undocumented mechanism that can:

- transfer locked tokens;
- release locked tokens;
- reduce the lock duration;
- reset the lock to an earlier completion date;
- replace the lock with a weaker schedule;
- or move the tokens to unrestricted custody.

---

## 14. Impact Vault Lock Start

The final Impact Vault lock-start event remains unresolved.

Before production deployment, the applicable specification MUST define:

- exact start event;
- exact timestamp or deterministic derivation;
- whether the lock begins before, at, or after production token allocation;
- and how the start is authenticated.

The lock MUST NOT be represented publicly as having started until the production rule and relevant on-chain state support that statement.

Base Sepolia pilot dates MUST NOT be used as the production Impact Vault lock start unless a later versioned specification explicitly and lawfully establishes such a rule.

---

## 15. Impact Vault Lock End

The production implementation MUST define a deterministic lock-end condition derived from the finalized lock start and applicable 50-year duration.

The exact production unlock timestamp is not established by this Draft.

The lock-end calculation MUST NOT be changeable through an undocumented privileged path.

---

## 16. Impact Vault Release Model

The post-lock release model remains unresolved.

Before Stable status, the applicable specification MUST define whether expiration of the lock results in:

- full release eligibility;
- staged release under an additional schedule;
- continued governance restriction;
- rollover into another equal or stronger restriction;
- or another explicitly specified model.

This document does not authorize unrestricted transfer automatically upon the conceptual expiration of 50 years.

The production implementation MUST match the final released rule.

---

## 17. Impact Vault Early Release Prohibition

The following MUST NOT provide an undocumented early-release path:

- administrator functions;
- owner functions;
- token recovery;
- upgradeability;
- proxy replacement;
- external routing;
- emergency authority;
- migration;
- governance;
- role reassignment;
- contract self-destruction behavior where applicable;
- or arbitrary token rescue.

An emergency is not sufficient justification for weakening the 50-year restriction.

If a security incident requires migration, the migration MUST preserve or strengthen the remaining restriction.

---

## 18. Impact Vault Extension

A future production mechanism MAY permit extension of the Impact Vault restriction only if:

- the remaining restriction is not shortened;
- release is not accelerated;
- authority is explicitly defined;
- the change is publicly documented;
- the economic effect is reviewed;
- and the applicable versioned specification permits it.

An extension mechanism MUST NOT create a hidden path for replacement with a weaker contract.

---

## 19. Impact Vault Migration

A migration MUST preserve at minimum:

- the amount still subject to restriction;
- the remaining effective lock duration;
- the economic restriction;
- the allocation identity;
- and historical linkage.

A migration record MUST identify:

- source contract or wallet;
- destination contract or wallet;
- amount;
- applicable network;
- authority;
- approval record;
- migration transaction;
- original lock start;
- original lock requirement;
- remaining restriction;
- and applicable specification release.

Migration MUST NOT restart the accounting in a way that creates a shorter effective lock.

Migration MUST NOT cause duplicate claims against both source and destination.

---

## 20. Impact Vault Recovery

Recovery functionality is not finalized.

If a production Impact Vault includes token-recovery functionality, it MUST NOT permit recovery of the locked GFC allocation in a way that defeats the lock.

Recovery MAY apply only to assets and circumstances explicitly specified.

Any recovery authority MUST disclose:

- scope;
- trigger;
- approvers;
- destination;
- restrictions preserved;
- and security rationale.

A generic `rescueTokens` function capable of withdrawing the locked GFC would contradict the intended restriction unless it is itself constrained so that the lock cannot be weakened.

---

## 21. Impact Vault Upgradeability

The final Impact Vault upgrade model is unresolved.

The production deployment MUST declare whether the relevant mechanism is:

- immutable;
- configurable within fixed limits;
- upgradeable;
- migratable without upgrade;
- or another explicitly defined model.

If upgradeability exists, the upgrade path MUST NOT be able to silently:

- shorten the lock;
- release locked GFC;
- replace the lock with a weaker condition;
- transfer the allocation to unrestricted custody;
- or broaden authority contrary to the applicable specification.

---

## 22. Impact Vault Status Reporting

A production transparency record SHOULD distinguish at minimum:

- original Impact Vault allocation;
- amount currently subject to lock;
- amount released after valid eligibility, if any;
- migrated amount, if any;
- current custody location;
- lock start;
- represented lock end;
- authority surface;
- and known deviations.

The phrase `50-year locked` MUST NOT be used if actual deployed architecture permits an undisclosed earlier release.

---

# Core Team Vesting

## 23. Core Team Allocation

The Core Team allocation is:

```text
50,000,000 GFC
```

representing:

```text
5% of total GFC supply
```

The intended restriction is:

```text
19-year linear vesting
```

The detailed production schedule remains unresolved.

---

## 24. Linear Vesting Requirement

Core Team entitlement MUST accrue linearly over the finalized 19-year vesting period.

Subject to the finalized start time and any explicitly specified cliff, the intended aggregate vesting relationship is conceptually:

```text
vested amount
=
Core Team allocation
×
elapsed vesting time
÷
total vesting duration
```

with appropriate bounds so that:

```text
0 ≤ vested amount ≤ 50,000,000 GFC
```

This formula is illustrative of the required linear relationship.

The exact production calculation, timestamp semantics, rounding, claim mechanics, and beneficiary accounting MUST be defined in the implementation specification.

---

## 25. Core Team Vesting Start

The final vesting commencement event remains unresolved.

Before production deployment, the applicable specification MUST define:

- vesting start event;
- vesting start timestamp;
- authentication method;
- relationship to production token deployment;
- relationship to allocation funding;
- and any initialization requirements.

The vesting start MUST NOT be inferred from:

- project founding;
- repository creation;
- Base Sepolia pilot deployment;
- website launch;
- or another unrelated historical event.

---

## 26. Core Team Vesting End

The production vesting end MUST be deterministically derived from the finalized vesting start and the 19-year vesting duration.

The exact production vesting-end timestamp is not established by this Draft.

The implementation MUST NOT allow an administrative role to move the vesting end earlier.

---

## 27. Core Team Cliff

A Core Team cliff is not currently finalized.

Before Stable status, the applicable specification MUST either:

- define a cliff and its interaction with 19-year linear vesting; or
- explicitly specify that no cliff applies.

A cliff MUST NOT be invented through frontend representation or implementation behavior without normative documentation.

---

## 28. Core Team Vesting Granularity

The exact vesting granularity remains unresolved.

Possible technical implementations MAY make vested entitlement calculable:

- continuously by timestamp;
- per block-derived timestamp behavior;
- per second;
- per day;
- per defined interval;
- or through another deterministic method.

Regardless of implementation, the economic effect MUST remain consistent with 19-year linear vesting.

A coarse claim interval MAY be used without changing the underlying linear entitlement, provided the distinction between:

- vested entitlement;
- claimability;
- and actual claim execution

is documented accurately.

---

## 29. Vested and Claimed Amounts

The production system SHOULD distinguish:

- total Core Team allocation;
- unvested amount;
- vested amount;
- vested but unclaimed amount;
- claimed amount;
- transferred amount;
- and migrated amount where applicable.

The relationship SHOULD satisfy, subject to the finalized accounting model:

```text
unvested + vested = total allocation
```

and:

```text
claimed ≤ vested
```

The implementation MUST prevent double claiming.

---

## 30. Core Team Claiming or Release

The final claim or release mechanism remains unresolved.

Before Stable status, the applicable specification MUST define:

- who may claim;
- whether each beneficiary claims independently;
- whether a distribution contract executes releases;
- claim frequency;
- minimum claim amount, if any;
- destination restrictions, if any;
- transaction-fee treatment;
- rounding;
- and unclaimed vested-token treatment.

Claiming MUST NOT make more GFC available than has vested under the applicable schedule.

---

## 31. Core Team Beneficiaries

The final beneficiary structure is unresolved.

Before production use, the applicable specification MUST define:

- beneficiary addresses or authenticated assignment process;
- beneficiary shares;
- whether shares are fixed;
- whether reassignment is permitted;
- succession;
- resignation or departure treatment;
- termination treatment;
- conflicts;
- and historical records.

The aggregate beneficiary entitlement MUST NOT exceed:

```text
50,000,000 GFC
```

Beneficiary assignment MUST NOT create duplicate claims to the same portion of the allocation.

---

## 32. Core Team Reassignment

Reassignment rules remain unresolved.

If reassignment is permitted, the production model MUST define:

- who may initiate reassignment;
- required approvals;
- eligible replacement beneficiaries;
- treatment of already vested amounts;
- treatment of unvested amounts;
- effective date;
- conflict-of-interest controls;
- and historical disclosure.

Reassignment MUST NOT accelerate the aggregate vesting schedule.

Reassignment MUST NOT reset already elapsed vesting time in a way that weakens or manipulates the intended restriction unless explicitly specified through an applicable breaking versioned change.

---

## 33. Core Team Succession

Succession rules remain unresolved.

A production model MUST define how entitlement is handled where a beneficiary:

- dies;
- becomes incapacitated;
- loses access;
- resigns;
- is removed;
- or otherwise cannot continue as originally designated.

Succession MUST NOT create aggregate entitlement exceeding the allocation.

Succession authority is privileged authority and MUST be disclosed.

---

## 34. Core Team Revocation

Whether Core Team vesting is revocable is unresolved.

Before Stable status, the applicable specification MUST explicitly define:

- whether unvested entitlement can be revoked;
- by whom;
- under what conditions;
- what happens to revoked unvested GFC;
- whether vested but unclaimed GFC remains claimable;
- how disputes are handled;
- and how the change is recorded.

No revocation power MAY be implied through generic administrative ownership.

Revocation MUST NOT permit confiscation of already vested entitlement unless an explicit, legally and technically defined basis exists in the applicable versioned specification.

---

## 35. Core Team Acceleration Prohibition

The current intended model does not permit undocumented acceleration of the 19-year vesting schedule.

No:

- administrator;
- governance action;
- emergency action;
- beneficiary action;
- upgrade;
- migration;
- recovery process;
- contract replacement;
- or reassignment

MAY make Core Team GFC vest earlier than the applicable schedule unless a later breaking versioned specification explicitly changes the commitment.

Operational convenience is not sufficient justification for acceleration.

---

## 36. Core Team Migration

Any migration MUST preserve:

- total remaining unvested amount;
- vested but unclaimed entitlement;
- elapsed vesting time;
- remaining vesting duration;
- beneficiary rights;
- and historical accounting.

A migration MUST NOT:

- restart the schedule to create earlier access;
- shorten the remaining duration;
- double count vested amounts;
- create claims against both source and destination;
- or move unvested GFC into unrestricted custody.

The migration record MUST identify:

- source;
- destination;
- amount;
- vested amount;
- unvested amount;
- claimed amount;
- applicable beneficiaries;
- authority;
- approval;
- transaction;
- and preserved restrictions.

---

## 37. Core Team Recovery

Recovery functionality remains unresolved.

If a recovery mechanism exists, it MUST NOT become an unrestricted method to:

- withdraw unvested GFC;
- accelerate vesting;
- change beneficiaries without authority;
- or confiscate vested entitlement.

Recovery MUST define:

- triggering condition;
- scope;
- authority;
- approvals;
- destination;
- beneficiary impact;
- and historical record.

---

## 38. Core Team Upgradeability

The final vesting-contract upgrade model remains unresolved.

If upgradeability exists, the production architecture MUST ensure that upgrades cannot silently:

- accelerate vesting;
- reduce the vesting period;
- increase aggregate beneficiary entitlement;
- withdraw unvested GFC;
- erase vested entitlement;
- or bypass accounting.

If the contract is represented as immutable, no external mechanism may provide equivalent hidden replacement authority.

---

# General Unlock and Release Controls

## 39. Unlock Eligibility

An unlock or release MUST occur only when all applicable conditions are satisfied.

Eligibility MAY depend on:

- elapsed time;
- vesting entitlement;
- finalized beneficiary status;
- contract state;
- or another explicitly specified condition.

Eligibility MUST NOT be based solely on an off-chain statement where the represented restriction is claimed to be technically enforced.

---

## 40. Release Authority

Where release is automatic according to contract state, no separate discretionary approval SHOULD be implied.

Where a role can authorize, initiate, block, redirect, or accelerate release, that role is material authority and MUST be disclosed.

Release authority MUST be consistent with [`roles-and-authority.md`](roles-and-authority.md).

---

## 41. No Administrative Override

A production mechanism MUST NOT contain an undocumented administrative override capable of defeating a represented long-term restriction.

Generic owner, administrator, upgrader, rescue, or recovery powers MUST be evaluated for their effective ability to bypass the restriction.

A restriction is not meaningfully enforceable if one privileged role can remove it unilaterally without the limitation being prominently disclosed.

---

## 42. No Emergency Bypass

Emergency authority MUST NOT create an undocumented mechanism to:

- unlock the Impact Vault early;
- accelerate Core Team vesting;
- confiscate vested Core Team entitlement;
- or move restricted GFC into unrestricted custody.

Where emergency migration is required for security, remaining restrictions MUST be preserved or strengthened.

---

## 43. Upgrade and Migration Equivalence

Security analysis MUST examine whether an apparently immutable restriction can be bypassed indirectly through:

- proxy upgrades;
- routers;
- registries;
- token replacement;
- custody migration;
- ownership transfer;
- external call routing;
- or another administrative layer.

The full system architecture determines whether a restriction is truly enforceable.

A single contract's local code is not sufficient where another privileged component can effectively replace its behavior.

---

## 44. Recovery and Rescue Functions

A recovery or rescue function MAY be appropriate for accidentally transferred unrelated assets.

However, a recovery function MUST NOT permit unrestricted withdrawal of GFC that is itself subject to the lock or vesting commitment.

The production specification MUST define:

- which assets may be recovered;
- which assets may not be recovered;
- who may recover;
- destination;
- required approvals;
- and event or record requirements.

---

## 45. Transferability of Restricted Positions

Whether a beneficiary's vesting position or a locked allocation position can be transferred is unresolved unless otherwise specified.

Before Stable status, the applicable implementation MUST define:

- whether the position itself is transferable;
- whether beneficiary rights can be assigned;
- whether assignment changes economic restrictions;
- and how transfers are recorded.

Transferability MUST NOT weaken the aggregate lock or vesting commitment.

---

## 46. Token Fee Interaction

The exact interaction between token transfer fees and release or claim transactions remains dependent on the finalized token implementation.

Before production deployment, the applicable specifications MUST determine whether transfers from:

- Impact Vault;
- Core Team vesting;
- migration contracts;
- or related release mechanisms

are classified as ordinary transfers, exempt transfers, or another category.

Fee treatment MUST NOT silently reduce beneficiary entitlement or create inconsistent accounting.

---

## 47. Staking Interaction

Restricted GFC MUST NOT be staked in a way that defeats the applicable lock or vesting restriction.

If future specifications permit locked or unvested GFC to participate in staking or governance-related mechanisms, they MUST define:

- custody;
- voting or participation rights;
- reward ownership;
- withdrawal restrictions;
- and preservation of the original lock or vesting schedule.

Participation MUST NOT create early transferability of the restricted principal.

---

## 48. Governance Participation Interaction

Locked or unvested GFC MUST NOT automatically receive governance rights unless explicitly specified.

If governance participation is permitted, the applicable specification MUST define:

- which balances qualify;
- voting weight;
- delegation;
- beneficiary rights;
- custody effects;
- and abuse prevention.

Governance rights MUST NOT create a path to release restricted principal early.

---

## 49. Security Requirements

The applicable implementation MUST be reviewed against threats including:

- timestamp calculation errors;
- integer precision errors;
- rounding errors;
- double claims;
- unauthorized release;
- beneficiary substitution;
- storage corruption;
- initialization mistakes;
- upgrade bypass;
- recovery bypass;
- migration duplication;
- privilege escalation;
- and frontend misrepresentation.

Detailed security requirements are defined in [`security-model.md`](security-model.md).

---

## 50. Testing Requirements

Before production reliance, tests SHOULD cover both intended and prohibited behavior.

Tests SHOULD include, where applicable:

- exact allocation amounts;
- restriction initialization;
- start-time handling;
- pre-start behavior;
- boundary timestamps;
- post-end behavior;
- linear vesting calculation;
- rounding;
- repeated claims;
- maximum claimable amount;
- unauthorized beneficiary actions;
- unauthorized administrator actions;
- migration;
- recovery;
- upgrade behavior;
- and state reconciliation.

Tests MUST verify that protected amounts cannot become transferable earlier than the applicable restriction permits.

---

## 51. Invariant Testing

Where appropriate, invariant or fuzz testing SHOULD verify:

### 51.1 Impact Vault

At any time before valid lock expiration:

```text
released locked GFC = 0
```

subject only to explicitly specified migration that preserves the restriction.

### 51.2 Core Team

At any time:

```text
claimed GFC ≤ vested GFC
```

and:

```text
vested GFC ≤ 50,000,000 GFC
```

### 51.3 Aggregate Core Team entitlement

Across all beneficiaries:

```text
aggregate entitlement ≤ 50,000,000 GFC
```

### 51.4 Migration

A migration MUST NOT create duplicate economic entitlement.

### 51.5 Supply

Locks, vesting, migration, and release MUST NOT increase canonical GFC supply.

---

## 52. Public Disclosure

A production lock or vesting record SHOULD disclose:

- allocation;
- initial amount;
- authenticated contract or wallet;
- network;
- restriction type;
- start condition;
- start timestamp;
- represented end or duration;
- current restricted amount;
- current vested amount where applicable;
- current released or claimed amount;
- authority;
- upgradeability;
- migration authority;
- recovery authority;
- known deviations;
- and verification status.

Public disclosure MUST distinguish between what is:

- specified;
- implemented;
- tested;
- deployed;
- active;
- and independently verified.

---

## 53. Transparency Registry Relationship

The planned Transparency Registry MAY later record:

- lock state;
- vesting state;
- contract version;
- authority changes;
- migrations;
- corrections;
- deviations;
- and status history.

The Registry is intended to operate as a versioned historical record rather than a permanent approval badge.

No complete production Transparency Registry is currently deployed.

A Registry label MUST NOT override actual authenticated contract state.

---

## 54. Pilot and Production Separation

The public Base Sepolia pilot does not establish production vesting or lock enforcement.

Pilot contracts, balances, timestamps, labels, or demonstrations MUST NOT be represented as authenticated Base Mainnet production restrictions.

Production lock and vesting status requires:

- authenticated production token;
- authenticated production restriction contracts or custody mechanisms;
- applicable versioned specifications;
- production initialization records;
- authority records;
- and authenticated on-chain state.

---

## 55. Public Communication Requirements

Public communication MUST NOT:

- describe the Impact Vault as technically locked before production enforcement exists;
- describe the Core Team allocation as actively vesting before the production schedule begins;
- imply a specific production start date not established by authenticated records;
- represent a pilot restriction as production;
- describe an upgradeable restriction as immutable;
- describe a migratable restriction as non-migratable;
- conceal privileged recovery or migration authority;
- describe vested tokens as unvested;
- describe unvested tokens as claimable;
- or imply that lock or vesting status proves compliant use or impact.

---

## 56. Conformance

An implementation conforms to this specification only when:

- it identifies an applicable versioned specification;
- allocation amounts match the applicable allocation specification;
- Impact Vault restrictions match the applicable 50-year lock requirement;
- Core Team restrictions match the applicable 19-year linear vesting requirement;
- actual technical authority is disclosed;
- no undocumented bypass exists;
- migration preserves applicable restrictions;
- recovery does not weaken applicable restrictions;
- public status matches authenticated implementation state;
- material deviations are documented;
- and production and pilot status remain correctly separated.

A wallet label, frontend countdown, marketing statement, or Draft specification does not establish conformance.

---

## 57. Non-Conformance

Non-conformance includes:

- early release of Impact Vault GFC contrary to the applicable lock;
- shortened Impact Vault restriction;
- accelerated Core Team vesting;
- withdrawal of unvested Core Team GFC;
- duplicate beneficiary entitlement;
- undocumented administrative override;
- hidden recovery bypass;
- migration into weaker restrictions;
- inaccurate public lock status;
- inaccurate vesting status;
- pilot restriction represented as production restriction;
- or public claims materially stronger than actual technical enforcement.

Material non-conformance MAY require:

- contract pause where applicable;
- authority review;
- migration;
- remediation;
- public correction;
- security review;
- governance review;
- incident treatment;
- or replacement deployment.

A specification MUST NOT be rewritten retrospectively merely to conceal non-conformance.

---

## 58. Current Unresolved Requirements

The following matters remain unresolved unless separately established by a later versioned specification or authenticated implementation record.

### Impact Vault

- production lock-start event;
- production lock-start timestamp;
- exact time-calculation method;
- unlock calculation;
- full versus staged post-lock release;
- post-lock custody;
- upgradeability;
- recovery behavior;
- migration implementation;
- and final contract architecture.

### Core Team

- production vesting-start event;
- production vesting-start timestamp;
- exact time-calculation method;
- cliff, if any;
- claim granularity;
- claim mechanism;
- beneficiary allocation;
- beneficiary assignment;
- reassignment;
- succession;
- revocation;
- departure treatment;
- vested-but-unclaimed treatment;
- transferability of beneficiary positions;
- recovery behavior;
- migration implementation;
- and final contract architecture.

### Shared

- token-fee interaction;
- governance participation of restricted balances;
- staking interaction;
- exact authority model;
- exact timelock requirements;
- production addresses;
- and final release authentication.

These unresolved matters MUST NOT be represented as finalized production decisions.

---

## 59. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- the Impact Vault lock-start rule is finalized;
- the Impact Vault lock-end calculation is finalized;
- Impact Vault post-lock behavior is finalized;
- Impact Vault upgradeability is finalized;
- Impact Vault migration is finalized;
- Impact Vault recovery is finalized or explicitly excluded;
- the Core Team vesting-start rule is finalized;
- the Core Team 19-year linear calculation is finalized;
- the Core Team cliff is finalized or explicitly excluded;
- Core Team claim or release mechanics are finalized;
- Core Team beneficiary structure is finalized;
- Core Team reassignment is finalized or explicitly excluded;
- Core Team succession is finalized;
- Core Team revocation is finalized or explicitly excluded;
- Core Team migration is finalized;
- Core Team recovery is finalized or explicitly excluded;
- token-fee interaction is finalized;
- restricted-balance governance rights are finalized or explicitly excluded;
- restricted-balance staking interaction is finalized or explicitly excluded;
- authority surfaces are finalized;
- security invariants are mapped to the intended implementation;
- production disclosure requirements are finalized;
- Base Sepolia pilot and Base Mainnet production terminology are consistently separated;
- and all related specifications are mutually consistent.

---

## 60. Related Specifications

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
- [`economic-flows.md`](economic-flows.md);
- [`staking.md`](staking.md);
- [`presale.md`](presale.md);
- [`transparency-model.md`](transparency-model.md);
- and repository-level [`../STATUS.md`](../STATUS.md).

Where another Draft specification conflicts with this document, the conflict MUST be resolved explicitly before Stable status.

---

## 61. Final Vesting and Unlock Principles

The GFC vesting and unlock model preserves the following distinctions:

> Allocation does not mean immediate availability.

> A wallet label does not create a lock.

> A frontend countdown does not create technical enforcement.

> Locking is not the same as vesting.

> The Impact Vault is intended to use a 50-year lock.

> The Core Team allocation is intended to vest linearly over 19 years.

> Vested does not necessarily mean claimed.

> Claimed does not necessarily mean spent.

> Migration must not weaken the remaining restriction.

> Recovery authority is privileged authority.

> Emergency authority must not bypass long-term commitments.

> Pilot restrictions do not establish production restrictions.

> Technical restriction does not prove compliant use or impact.

The objective is to make long-term token restrictions technically meaningful, difficult to bypass, accurately represented, and historically reviewable before production reliance.

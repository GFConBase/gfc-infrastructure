# GFC Token Allocation Specification

**Document ID:** GFC-ALC-001  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Intended Production Network:** Base Mainnet  
**Production Chain ID:** 8453  
**Public Pilot Network:** Base Sepolia  
**Pilot Chain ID:** 84532  
**Total Intended Supply:** 1,000,000,000 GFC  
**Last Updated:** 2026-08-30

---

## 1. Document Status

This document defines the current intended allocation of the fixed Global Foundation Coin (GFC) token supply and the associated allocation-level constraints.

It is normative because it defines:

- allocation names;
- allocation percentages;
- allocation token amounts;
- supply reconciliation requirements;
- custody and authority boundaries;
- lock and vesting requirements;
- migration constraints;
- and allocation-level disclosure requirements.

Its maturity remains Draft.

At the current repository state:

- the **GFC Token / Economic Layer** is the current primary product focus;
- a public GFC pilot exists on **Base Sepolia**;
- no production GFC token is deployed on Base Mainnet;
- no production allocation contract is established as official;
- no production allocation wallet is established as official by this document;
- no production Impact Vault contract is established as official;
- no production Core Team vesting contract is established as official;
- no production allocation custody model is represented as active;
- no production allocation balances are established as authoritative by this document;
- and no allocation implementation is designated as conforming.

The Base Sepolia pilot MUST NOT be interpreted as evidence that the production allocation structure has been deployed.

Current implementation and deployment status is maintained in [`../STATUS.md`](../STATUS.md).

---

## 2. Purpose

The purpose of this specification is to define how the complete intended fixed GFC supply is divided and what constraints apply to those allocations.

The allocation model is designed to ensure that:

- the complete fixed supply is accounted for;
- no undisclosed initial allocation exists;
- allocation names remain consistent;
- allocation purpose does not become unrestricted ownership;
- long-term commitments remain enforceable;
- custody and authority are reviewable;
- migration cannot silently weaken allocation restrictions;
- and production records can reconcile intended allocation with actual on-chain state.

This document defines allocation structure.

It does not independently establish:

- final wallet addresses;
- final contract addresses;
- final signer groups;
- final treasury policies;
- final liquidity strategy;
- final presale implementation;
- final staking economics;
- or final legal ownership.

---

## 3. Relationship to the GFC Accountability Model

The long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

Allocations primarily define how **Funds** are initially categorized and which **Rules** and **Authority** constraints apply to them.

An allocation label does not by itself establish:

- who has legitimate authority;
- whether movement is permitted;
- whether spending is compliant;
- whether an outcome occurred;
- or whether impact was achieved.

For a material allocation movement, it SHOULD be possible to reconstruct:

1. the source allocation;
2. the responsible authority;
3. the applicable rules;
4. the decision authorizing the movement;
5. the resulting transaction or state change;
6. and the evidence supporting the represented purpose.

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

This document defines:

- allocation names;
- allocation percentages;
- allocation token amounts;
- total-supply reconciliation;
- allocation integrity;
- allocation custody requirements;
- allocation authority requirements;
- allocation transfer constraints;
- long-term lock requirements;
- vesting requirements;
- allocation migration constraints;
- allocation disclosure;
- and allocation-level conformance.

---

## 6. Out of Scope

This document does not independently define:

- token implementation;
- buy or sell fee implementation;
- detailed Treasury Reserve spending rules;
- detailed Liquidity Reserve deployment strategy;
- presale contribution accounting;
- presale refund implementation;
- staking reward calculations;
- governance voting mechanics;
- final Transparency Registry behavior;
- impact-verification methodology;
- legal ownership;
- tax treatment;
- or regulatory classification.

Token-level supply requirements are defined in [`token.md`](token.md).

Authority boundaries are defined in [`roles-and-authority.md`](roles-and-authority.md).

Governance constraints are defined in [`governance-constraints.md`](governance-constraints.md).

Security requirements are defined in [`security-model.md`](security-model.md).

---

## 7. Total Allocation

The intended fixed GFC supply is:

```text
1,000,000,000 GFC
```

The current Draft allocation model is:

| Allocation | Percentage | Token Amount |
|---|---:|---:|
| Impact Vault | 25% | 250,000,000 GFC |
| Guardian Growth | 20% | 200,000,000 GFC |
| Presale | 15% | 150,000,000 GFC |
| Treasury Reserve | 15% | 150,000,000 GFC |
| Liquidity Reserve | 15% | 150,000,000 GFC |
| Ecosystem | 5% | 50,000,000 GFC |
| Core Team | 5% | 50,000,000 GFC |
| **Total** | **100%** | **1,000,000,000 GFC** |

A conforming initial allocation MUST reconcile exactly to the complete fixed supply.

No undisclosed initial allocation MAY exist outside this total.

These values are Draft specification parameters.

They are not evidence of deployed production allocation contracts, funded production wallets, or active custody arrangements.

---

## 8. Allocation Reconciliation

The allocation model MUST satisfy:

```text
25% + 20% + 15% + 15% + 15% + 5% + 5% = 100%
```

and:

```text
250,000,000
+ 200,000,000
+ 150,000,000
+ 150,000,000
+ 150,000,000
+ 50,000,000
+ 50,000,000
= 1,000,000,000 GFC
```

Allocation calculations MUST use the token's configured 18 decimals consistently.

Deployment mechanics MUST NOT create:

- excess supply;
- hidden residual supply;
- overlapping allocation claims;
- duplicate allocation capacity;
- or unaccounted canonical balances.

If a deployment process produces a technical residual balance, the applicable release MUST document:

- amount;
- source;
- address;
- reason;
- normative allocation classification;
- and final treatment.

A technical residual MUST NOT become an undisclosed eighth allocation.

---

## 9. Allocation Integrity

Each production allocation MUST be independently identifiable through an authenticated:

- wallet;
- smart contract;
- accounting record linked to authenticated on-chain state;
- or another explicitly specified allocation mechanism.

A production reviewer SHOULD be able to determine:

- initial allocation amount;
- percentage of total supply;
- authenticated custody address or contract;
- current on-chain balance;
- incoming transfers;
- outgoing transfers;
- applicable locks;
- applicable vesting;
- custody authority;
- spending or release authority;
- upgrade authority;
- migration authority;
- and known deviations.

An allocation label does not independently prove:

- technical restriction;
- legal restriction;
- correct custody;
- compliant use;
- authorized spending;
- correct beneficiary selection;
- output;
- outcome;
- or impact.

---

## 10. Canonical Allocation Names

The canonical allocation names are:

1. **Impact Vault**
2. **Guardian Growth**
3. **Presale**
4. **Treasury Reserve**
5. **Liquidity Reserve**
6. **Ecosystem**
7. **Core Team**

Current technical specifications SHOULD use these exact names unless a more specific implementation label is required.

Legacy or alternate labels such as:

- `Guardian Growth Fund`;
- `Presale Allocation`;
- `Ecosystem Growth Fund`;
- or `Core Team Allocation`

MAY remain in historical records where necessary for accurate archival context.

They SHOULD NOT create ambiguity in current specifications or production records.

An allocation name describes intended classification.

It does not independently authorize transfer or spending.

---

## 11. General Custody Requirements

Material allocation custody MUST be:

- explicit;
- attributable;
- reviewable;
- consistent with least privilege;
- separated from unrelated authority where reasonably possible;
- and protected against unilateral misuse appropriate to the allocation's risk.

A production allocation record SHOULD identify, where applicable:

- custody address;
- custody mechanism;
- controlling role;
- signer model;
- approval threshold;
- signer appointment;
- signer removal;
- emergency authority;
- transfer authority;
- spending authority;
- upgrade authority;
- migration authority;
- recovery authority;
- and applicable timelocks.

No specific production signer, multisig, threshold, wallet, or custody platform is established by this document.

A multisig does not independently prove:

- decentralization;
- signer independence;
- appropriate custody;
- or sufficient separation of duties.

---

## 12. Allocation Authority

Authority over material allocations MUST be consistent with [`roles-and-authority.md`](roles-and-authority.md).

Production records MUST distinguish, where applicable:

- custody authority;
- proposal authority;
- approval authority;
- execution authority;
- release authority;
- beneficiary authority;
- migration authority;
- upgrade authority;
- and emergency authority.

A role MUST NOT obtain unrestricted beneficial ownership merely because it controls the technical custody mechanism.

If technical capability exceeds intended authority, that difference MUST be disclosed as a trust and security assumption.

---

## 13. General Transfer Requirements

Tokens MUST NOT be moved between allocations merely for accounting convenience without:

- documented authority;
- identified purpose;
- applicable approval;
- reviewable transaction evidence;
- updated allocation accounting;
- and disclosure of the effect on the original allocation commitment.

Transfers MUST NOT be used to:

- bypass locks;
- bypass vesting;
- conceal treasury use;
- create duplicate allocation capacity;
- avoid reporting;
- reclassify tokens retrospectively without authority;
- or weaken previously stated restrictions.

A transfer does not automatically change the normative allocation classification of the tokens.

Where reclassification is permitted, the applicable specification MUST define the authority and conditions.

---

## 14. Cross-Allocation Reclassification

A material reclassification between allocations is not an ordinary transfer.

A reclassification MAY constitute a breaking normative change where it changes:

- allocation percentage;
- allocation amount;
- participant expectations;
- long-term constraints;
- beneficiary rights;
- or intended economic function.

Reclassification MUST NOT be used to bypass allocation-specific rules.

Where reclassification occurs before production deployment, it requires an updated applicable specification.

Where a future production system permits reclassification, its authority, limits, accounting, and historical record MUST be explicitly defined.

---

## 15. Impact Vault

The Impact Vault allocation is:

```text
250,000,000 GFC
```

This equals:

```text
25% of total supply
```

### 15.1 Intended long-term constraint

The Impact Vault is intended to be subject to a:

```text
50-year lock
```

The detailed lock and unlock requirements belong in [`vesting-and-unlocks.md`](vesting-and-unlocks.md).

Before production deployment, the applicable implementation MUST define:

- lock commencement event;
- lock commencement timestamp;
- exact lock calculation;
- unlock conditions;
- whether release is full or staged;
- whether transfers are technically blocked;
- administrative authority;
- upgradeability;
- migration;
- emergency behavior;
- and post-lock behavior.

### 15.2 No premature enforcement claim

A 50-year lock MUST NOT be represented as technically enforced until authenticated production contract code and state support that claim.

### 15.3 Bypass prohibition

No:

- upgrade;
- migration;
- governance action;
- emergency action;
- recovery action;
- administrator;
- or alternate withdrawal path

MAY function as an undocumented method for shortening or bypassing the Impact Vault restriction.

### 15.4 Migration

A migration MUST preserve or strengthen:

- remaining locked amount;
- remaining duration;
- economic restriction;
- and allocation identity.

Migration MUST NOT function as disguised early release.

### 15.5 Impact claims

The existence, balance, or lock state of the Impact Vault does not independently prove:

- charitable status;
- compliant use;
- actual deployment of funds;
- positive outcome;
- or impact.

Impact-related claims remain subject to [`transparency-model.md`](transparency-model.md).

---

## 16. Guardian Growth

The Guardian Growth allocation is:

```text
200,000,000 GFC
```

This equals:

```text
20% of total supply
```

Its final production mandate remains unresolved.

Before production use, the applicable specification MUST define:

- permitted purposes;
- prohibited purposes;
- custody structure;
- release authority;
- approval requirements;
- transaction limits;
- recipient criteria;
- conflict-of-interest controls;
- lock or vesting requirements, if any;
- reporting requirements;
- and migration rules.

The term `Guardian` MUST NOT be represented as evidence of independent oversight unless such oversight actually exists and is documented.

Guardian Growth MUST NOT be treated as unrestricted inventory.

---

## 17. Presale

The Presale allocation is:

```text
150,000,000 GFC
```

This equals:

```text
15% of total supply
```

The Presale allocation MUST remain consistent with [`presale.md`](presale.md).

No GFC presale is currently live.

### 17.1 Current Draft relationship

The current Draft presale design includes:

- reference price: €0.05 per GFC;
- intended duration: eight weeks;
- soft cap: €250,000;
- no separate monetary hard cap;
- intended support for ETH, USDC, and DAI on Base;
- immediate token distribution as the current design direction;
- refunds if the applicable soft-cap success condition is not satisfied;
- and immutable material sale logic as the current design direction.

These are Draft design parameters.

### 17.2 Allocation ceiling

The presale MUST NOT distribute more than:

```text
150,000,000 GFC
```

Participant token distribution and accounting MUST NOT create claims exceeding the Presale allocation.

### 17.3 Immediate distribution

Because the current design direction uses immediate token distribution, allocation accounting MUST distinguish:

- total Presale allocation;
- GFC already distributed;
- remaining undistributed GFC;
- invalid or reversed purchase accounting where applicable;
- and final unsold GFC.

### 17.4 Failed finalization and refunds

The current Draft design also requires refunds where the applicable soft-cap success condition is not satisfied.

The final presale specification MUST define the treatment of GFC already distributed if finalization fails.

This document does not invent or authorize:

- clawback;
- forced transfer;
- forced burn;
- token invalidation;
- mandatory participant return;
- replacement token;
- or another mechanism.

A production presale MUST NOT activate while this interaction remains undefined.

### 17.5 Soft-cap status

Reaching the soft cap before the presale ends MUST NOT by itself be represented as:

- completed finalization;
- unrestricted access to contribution proceeds;
- or final resolution of participant refund rights

unless the applicable presale specification explicitly establishes such behavior.

### 17.6 Unsold tokens

Treatment of unsold Presale GFC remains unresolved.

It MUST be finalized before production activation.

---

## 18. Treasury Reserve

The Treasury Reserve allocation is:

```text
150,000,000 GFC
```

This equals:

```text
15% of total supply
```

The Treasury Reserve MUST NOT be treated as unrestricted administrative property.

Before production use, the applicable treasury and governance specifications MUST define:

- permitted uses;
- prohibited uses;
- custody;
- proposal authority;
- approval authority;
- execution authority;
- transaction thresholds;
- signer model;
- timelocks;
- emergency authority;
- related-party controls;
- reporting;
- reconciliation;
- and migration.

On-chain traceability does not by itself establish compliant treasury use.

---

## 19. Liquidity Reserve

The Liquidity Reserve allocation is:

```text
150,000,000 GFC
```

This equals:

```text
15% of total supply
```

Before production deployment of liquidity, the applicable specification MUST define:

- approved venues;
- approved pairs;
- initial liquidity amount;
- deployment schedule;
- custody;
- liquidity-provider position ownership;
- withdrawal authority;
- rebalancing authority;
- lock status;
- market-making arrangements;
- fee ownership;
- reporting;
- and migration.

Liquidity provisioning MUST NOT be represented as:

- permanently locked;
- protocol-owned;
- non-withdrawable;
- guaranteed;
- or permanent

unless the actual technical and governance configuration supports the claim.

Any authority capable of withdrawing or redirecting liquidity MUST be disclosed.

---

## 20. Ecosystem

The Ecosystem allocation is:

```text
50,000,000 GFC
```

This equals:

```text
5% of total supply
```

Before production use, the applicable specification MUST define:

- eligible use categories;
- recipient criteria;
- grants;
- incentives;
- development support;
- partnerships;
- infrastructure support;
- marketing-related use where applicable;
- approval requirements;
- distribution limits;
- milestone conditions;
- vesting where applicable;
- conflict-of-interest controls;
- reporting;
- and migration.

The Ecosystem allocation MUST NOT be used for undisclosed insider distributions or unreviewable discretionary transfers.

Material categories SHOULD remain distinguishable in reporting.

---

## 21. Core Team

The Core Team allocation is:

```text
50,000,000 GFC
```

This equals:

```text
5% of total supply
```

### 21.1 Intended vesting constraint

The Core Team allocation is intended to be subject to:

```text
19-year linear vesting
```

Detailed requirements belong in [`vesting-and-unlocks.md`](vesting-and-unlocks.md).

### 21.2 Required production details

Before Stable status and production deployment, the applicable specification MUST define:

- vesting commencement event;
- vesting commencement timestamp;
- vesting end;
- linear calculation method;
- release or claim interval;
- rounding;
- cliff, if any;
- beneficiary structure;
- beneficiary replacement;
- reassignment;
- succession;
- revocation;
- treatment of vested but unclaimed tokens;
- treatment of unvested tokens;
- transferability;
- migration;
- recovery authority;
- and administrative control.

### 21.3 Linear vesting

Linear vesting MUST NOT be represented as implemented unless the authenticated production mechanism releases entitlement proportionally over the documented 19-year period.

### 21.4 Public status

Where relevant, public records SHOULD distinguish between:

- total Core Team allocation;
- unvested amount;
- vested but unclaimed amount;
- and claimed amount.

### 21.5 Bypass prohibition

No:

- upgrade;
- migration;
- governance action;
- emergency action;
- recovery mechanism;
- administrator;
- or beneficiary action

MAY function as an undocumented method for accelerating or bypassing the Core Team vesting commitment.

---

## 22. Unallocated Supply

The current allocation model assigns:

```text
100%
```

of the intended fixed supply.

There is therefore no intended unallocated canonical GFC supply at initialization.

Any production residual created by technical deployment mechanics MUST be explicitly reconciled to one of the canonical allocations or otherwise resolved by the applicable versioned specification.

It MUST NOT remain as undocumented discretionary inventory.

---

## 23. Unsold Presale Tokens

The final treatment of unsold Presale tokens remains unresolved.

Before production presale activation, the applicable specification MUST define whether unsold tokens:

- remain within the Presale allocation under defined restrictions;
- move to another allocation through a predefined rule;
- become locked;
- are burned;
- are reserved for a later explicitly specified distribution;
- or receive another defined treatment.

The final rule MUST specify:

- authority;
- timing;
- custody;
- supply impact;
- economic classification;
- reporting;
- and historical record.

Unsold-token treatment MUST NOT be improvised after the sale result is known.

---

## 24. Allocation Changes

A change to any canonical allocation percentage or token amount is a breaking normative change.

Such a change requires:

- explicit versioning;
- rationale;
- supply reconciliation;
- economic analysis;
- participant-rights analysis;
- governance analysis;
- security analysis;
- implementation analysis;
- migration analysis where relevant;
- updated public communication;
- and an updated change record.

Allocation changes MUST NOT increase canonical GFC supply beyond the limit defined in [`token.md`](token.md).

A reallocation MUST NOT silently eliminate or weaken an existing lock, vesting, or participant protection.

---

## 25. Upgradeability

Any production allocation contract MUST declare whether it is:

- immutable;
- configurable within defined limits;
- upgradeable;
- migratable;
- recoverable;
- or replaceable.

Where upgradeability exists, the applicable deployment record MUST identify:

- upgrade authority;
- approval threshold;
- timelock;
- emergency path;
- implementation replacement process;
- treatment of locked GFC;
- treatment of vested GFC;
- treatment of unvested GFC;
- beneficiary impact;
- and historical upgrade records.

Upgradeability MUST NOT make a represented restriction functionally meaningless.

---

## 26. Migration

Allocation migration MUST preserve, where applicable:

- supply reconciliation;
- allocation identity;
- locked amount;
- remaining lock duration;
- vesting schedule;
- beneficiary rights;
- custody accountability;
- historical records;
- and known deviations.

A migration record MUST identify:

- source address or contract;
- destination address or contract;
- network;
- migrated amount;
- migration transaction;
- authority;
- approval record;
- applicable specification;
- preserved restrictions;
- changed restrictions;
- affected beneficiaries;
- and verification status.

Migration MUST NOT create duplicate claims against both source and destination systems.

Migration MUST NOT be used as a disguised method to weaken the original allocation rules.

---

## 27. Recovery

Allocation-specific recovery functionality is not finalized.

If recovery authority exists, it MUST NOT become an unrestricted method to bypass:

- custody constraints;
- locks;
- vesting;
- allocation classification;
- or beneficiary rights.

A recovery mechanism MUST define:

- trigger;
- authority;
- approvals;
- scope;
- destination;
- preserved restrictions;
- record requirements;
- and security assumptions.

Recovery authority is itself privileged authority.

---

## 28. Allocation Disclosure

A production allocation record SHOULD disclose:

- canonical allocation name;
- intended purpose;
- initial amount;
- percentage of total supply;
- authenticated wallet or contract;
- network;
- current balance;
- lock status;
- vesting status;
- custody authority;
- release or spending authority;
- upgrade authority;
- migration authority;
- transfer history;
- known deviations;
- and evidence supporting material public claims.

Protected or security-sensitive information MAY remain non-public where justified.

Privacy MUST NOT be used as a blanket justification for withholding material:

- balance;
- custody structure;
- authority surface;
- or restriction status.

---

## 29. Allocation Transparency

Allocation transparency MUST distinguish between:

- intended allocation;
- authenticated initial allocation;
- current balance;
- transferred amount;
- locked amount;
- vested amount;
- distributed amount;
- spent amount where applicable;
- and unresolved differences.

A balance alone does not explain purpose or use.

A transfer alone does not establish compliant spending.

An impact-related allocation label does not establish impact.

Detailed transparency requirements are defined in [`transparency-model.md`](transparency-model.md).

---

## 30. Allocation Security Invariants

The following allocation-level security invariants apply.

### 30.1 Supply reconciliation

All canonical initial allocations MUST sum to:

```text
1,000,000,000 GFC
```

### 30.2 No duplicate allocation

No canonical GFC amount may simultaneously be represented as belonging to multiple allocations without an explicit accounting model that prevents double counting.

### 30.3 Impact Vault restriction

The intended Impact Vault restriction MUST NOT be weakened through an undocumented privileged path.

### 30.4 Core Team vesting restriction

The intended Core Team vesting restriction MUST NOT be accelerated through an undocumented privileged path.

### 30.5 Presale ceiling

The Presale MUST NOT distribute more than:

```text
150,000,000 GFC
```

### 30.6 Environment separation

Pilot allocation state MUST NOT be represented as production allocation state.

### 30.7 Authority disclosure

No material allocation authority may remain outside the disclosed authority surface.

These invariants must be interpreted together with [`security-model.md`](security-model.md).

---

## 31. Pilot and Production Separation

The public Base Sepolia pilot does not establish production allocations.

Pilot token balances, test allocations, development wallets, or demonstration labels MUST NOT be represented as authenticated Base Mainnet production allocations.

Before production status is claimed, allocation records MUST identify:

- production network;
- authenticated token contract;
- authenticated allocation addresses or contracts;
- initial allocation transactions;
- applicable lock or vesting contracts;
- custody authority;
- and production status.

A pilot wallet does not become a production wallet merely because it has existed publicly or been used for testing.

---

## 32. Public Communication Requirements

Public communication concerning GFC allocations MUST accurately distinguish between:

- Draft allocation design;
- specified allocation;
- pilot or test allocation;
- implemented allocation;
- authenticated production allocation;
- locked allocation;
- vested allocation;
- distributed allocation;
- and spent allocation.

Public communication MUST NOT:

- present Draft allocations as already funded production wallets;
- describe pilot allocation state as production state;
- describe an allocation as locked before technical enforcement exists;
- describe vesting as enforced before authenticated production implementation exists;
- imply independent oversight through an allocation name;
- imply impact solely through the Impact Vault name;
- or imply unrestricted availability of tokens subject to lock, vesting, or custody restrictions.

---

## 33. Conformance

An allocation implementation conforms to this specification only where:

- it identifies an applicable versioned allocation specification;
- the total production token supply is fully reconciled;
- each canonical initial allocation matches the applicable specification;
- no undisclosed initial allocation exists;
- authenticated balances support the represented allocation state;
- applicable locks and vesting are enforced as represented;
- custody and authority are accurately disclosed;
- migration preserves applicable constraints;
- pilot status is not misrepresented as production status;
- material deviations are documented;
- and the implementation is linked to authenticated production deployment records.

A wallet label, allocation name, user interface, informal statement, website, or marketing claim does not establish conformance.

---

## 34. Allocation Non-Conformance

Allocation non-conformance includes:

- initial allocation totals not reconciling to fixed supply;
- undisclosed allocation;
- duplicate allocation accounting;
- Impact Vault restriction bypass;
- Core Team vesting acceleration;
- Presale distribution exceeding 150,000,000 GFC;
- undisclosed custody authority;
- undisclosed reclassification;
- migration into weaker restrictions;
- pilot allocations presented as production allocations;
- allocation label used to imply unsupported oversight or impact;
- or public claims materially stronger than authenticated allocation state supports.

Material non-conformance MAY require:

- correction;
- allocation reconciliation;
- authority review;
- custody migration;
- contract pause where applicable;
- public clarification;
- specification update;
- security review;
- governance review;
- or incident treatment.

A specification MUST NOT be rewritten retrospectively merely to conceal allocation non-conformance.

---

## 35. Current Unresolved Requirements

The following matters remain unresolved unless separately established by a later versioned specification or authenticated implementation record:

- detailed permitted use for Guardian Growth;
- detailed permitted use for Treasury Reserve;
- detailed permitted use for Liquidity Reserve;
- detailed permitted use for Ecosystem;
- allocation-specific custody architecture;
- production wallet or contract structure;
- signer structures;
- approval thresholds;
- allocation-specific timelocks;
- Impact Vault lock commencement;
- Impact Vault unlock behavior;
- Impact Vault post-lock behavior;
- Core Team vesting commencement;
- Core Team beneficiary structure;
- Core Team cliff, if any;
- Core Team succession and reassignment;
- Core Team revocation rules;
- treatment of unsold Presale tokens;
- treatment of already distributed Presale GFC if failed finalization creates a refund right;
- liquidity-position control;
- allocation recovery architecture;
- allocation migration architecture;
- and production allocation implementation.

These unresolved areas MUST NOT be represented as completed or finalized.

---

## 36. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- canonical allocation names are finalized;
- allocation percentages and amounts are confirmed;
- production supply reconciliation is finalized;
- allocation-specific custody models are defined;
- material allocation authority is mapped;
- Impact Vault lock rules are finalized;
- Core Team vesting rules are finalized;
- Guardian Growth control rules are defined;
- Treasury Reserve control rules are defined;
- Liquidity Reserve control rules are defined;
- Ecosystem control rules are defined;
- Presale allocation accounting is finalized;
- immediate-distribution and failed-sale refund treatment is resolved;
- unsold Presale token treatment is finalized;
- allocation migration requirements are finalized;
- allocation recovery requirements are finalized or explicitly excluded;
- allocation disclosure requirements are finalized;
- allocation security invariants are mapped to the intended implementation;
- Base Sepolia pilot and Base Mainnet production allocation terminology are consistently separated;
- and related specifications are mutually consistent.

---

## 37. Related Specifications

This document MUST be interpreted together with:

- [`README.md`](README.md);
- [`glossary.md`](glossary.md);
- [`non-goals.md`](non-goals.md);
- [`architecture.md`](architecture.md);
- [`roles-and-authority.md`](roles-and-authority.md);
- [`governance-constraints.md`](governance-constraints.md);
- [`security-model.md`](security-model.md);
- [`token.md`](token.md);
- [`vesting-and-unlocks.md`](vesting-and-unlocks.md);
- [`economic-flows.md`](economic-flows.md);
- [`staking.md`](staking.md);
- [`presale.md`](presale.md);
- [`transparency-model.md`](transparency-model.md);
- and repository-level [`../STATUS.md`](../STATUS.md).

Where another Draft specification conflicts with this document, the conflict MUST be resolved explicitly before Stable status.

---

## 38. Final Allocation Principles

The GFC allocation model preserves the following distinctions:

> Allocation does not mean unrestricted ownership.

> Allocation label does not mean technical restriction.

> Allocation does not prove compliant use.

> Impact Vault does not prove impact.

> Guardian does not automatically mean independent oversight.

> Treasury Reserve does not mean unrestricted treasury spending.

> Liquidity Reserve does not guarantee liquidity.

> Core Team allocation does not mean immediately transferable Core Team tokens.

> Presale allocation does not mean a live presale.

> Pilot allocation does not mean production allocation.

> Migration must not weaken lock, vesting, or supply restrictions.

> Public balance does not explain purpose.

> Transaction visibility does not prove outcome or impact.

The production allocation system must make supply reconciliation, custody, authority, restrictions, movements, and material deviations reviewable before production reliance.

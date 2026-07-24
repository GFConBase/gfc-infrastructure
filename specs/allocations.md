# GFC Token Allocation Specification

This document defines the current intended allocation of the fixed Global Foundation Coin (GFC) token supply and the associated allocation-level constraints.

---

## Document Status

| Property | Value |
|---|---|
| Maturity | Draft |
| Authority | Normative |
| Version | Unreleased |
| Implementation status | Pre-deployment |
| Total intended supply | 1,000,000,000 GFC |

This document is normative but remains Draft.

It may change materially before a Stable specification release is approved.

It does not represent deployed allocation contracts, active custody arrangements, or funded production wallets.

Current implementation and deployment status is maintained in [`../STATUS.md`](../STATUS.md).

---

## Normative Language

The terms `must`, `must not`, `required`, `should`, `should not`, and `may` are used to distinguish requirements, recommendations, prohibitions, and permitted behavior.

A requirement remains subject to the maturity and version of the applicable specification release.

---

## Scope

This document defines:

- allocation names;
- allocation percentages;
- allocation token amounts;
- total-supply reconciliation;
- allocation integrity;
- allocation custody requirements;
- allocation-control requirements;
- long-term lock requirements;
- vesting requirements;
- allocation migration constraints;
- and allocation-level disclosure requirements.

This document does not independently define:

- token implementation;
- transfer-fee behavior;
- detailed treasury spending rules;
- detailed liquidity strategy;
- presale accounting;
- staking design;
- governance voting design;
- impact-verification methodology;
- or legal ownership.

The token-level supply model is defined in [`token.md`](token.md).

---

## Total Allocation

The fixed intended supply is allocated as follows.

| Allocation | Percentage | Token Amount |
|---|---:|---:|
| Impact Vault | 25% | 250,000,000 GFC |
| Guardian Growth Fund | 20% | 200,000,000 GFC |
| Presale Allocation | 15% | 150,000,000 GFC |
| Treasury Reserve | 15% | 150,000,000 GFC |
| Liquidity Reserve | 15% | 150,000,000 GFC |
| Ecosystem Growth Fund | 5% | 50,000,000 GFC |
| Core Team | 5% | 50,000,000 GFC |
| **Total** | **100%** | **1,000,000,000 GFC** |

A conforming initial allocation must reconcile exactly to:

```text
1,000,000,000 GFC
```

No undisclosed allocation may exist outside this total.

---

## Allocation Reconciliation

The allocation model must satisfy both of the following conditions:

```text
25% + 20% + 15% + 15% + 15% + 5% + 5% = 100%
```

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

Allocation calculations must use the token's configured decimals consistently.

Rounding must not create:

- excess tokens;
- unassigned tokens;
- duplicate claims;
- or hidden residual balances.

Any residual balance created by deployment mechanics must be documented and assigned through the applicable versioned specification.

---

## Allocation Integrity

Each allocation must be independently identifiable through:

- an authenticated wallet;
- an authenticated contract;
- an authenticated accounting record;
- or another verifiable allocation mechanism defined by the production architecture.

A production implementation should allow reviewers to determine:

- the original allocation amount;
- the current balance;
- incoming transfers;
- outgoing transfers;
- applicable locks;
- applicable vesting;
- custody authority;
- spending authority;
- migration authority;
- and known deviations.

An allocation label does not independently prove:

- technical restriction;
- legal restriction;
- correct custody;
- correct spending;
- correct use of funds;
- or impact.

---

## Allocation Names

The allocation names describe intended categories.

They must not be represented as sufficient authorization for a transfer or expenditure.

The name of an allocation does not replace:

- documented permitted uses;
- approval requirements;
- custody controls;
- technical restrictions;
- supporting evidence;
- or governance authorization.

Before Stable status, each material allocation should have a defined purpose, control model, and permitted-use framework.

---

## General Custody Requirements

Material allocation custody must be:

- explicitly documented;
- attributable;
- reviewable;
- separated from unrelated authority where appropriate;
- consistent with least privilege;
- and protected against unilateral misuse where practical.

A production allocation record should identify:

- custody address;
- custody mechanism;
- authorized signers;
- signature threshold;
- signer appointment process;
- signer removal process;
- emergency authority;
- transfer authority;
- spending authority;
- migration authority;
- and applicable timelocks.

A multisig does not independently prove signer independence, decentralization, or adequate separation of duties.

---

## General Transfer Requirements

Tokens must not be transferred between allocations merely for accounting convenience without:

- documented authority;
- an identified purpose;
- an applicable approval process;
- a reviewable transaction record;
- updated allocation accounting;
- and disclosure of the effect on the original allocation commitment.

Transfers must not be used to:

- bypass locks;
- bypass vesting;
- conceal treasury use;
- duplicate allocation capacity;
- avoid disclosure;
- or retrospectively change the represented purpose of an allocation.

A transfer does not automatically change the normative classification of the tokens.

---

## Impact Vault

The Impact Vault allocation is:

```text
250,000,000 GFC
```

This equals:

```text
25% of the total intended supply
```

### Intended Long-Term Constraint

The Impact Vault allocation is intended to be subject to a:

```text
50-year lock
```

The production architecture must define:

- the lock commencement event;
- the lock commencement timestamp;
- the exact unlock timestamp;
- the time-calculation method;
- whether partial unlocking is possible;
- whether transfers are technically blocked;
- whether governance can modify the lock;
- whether upgrades can modify the lock;
- whether migration is possible;
- whether emergency authority exists;
- and what happens after expiration.

A 50-year lock must not be represented as technically enforced until authenticated contract code and on-chain state support that claim.

### Bypass Prohibition

Upgrade, migration, governance, emergency, recovery, or administrative mechanisms must not function as undocumented methods for bypassing the Impact Vault lock.

Moving the allocation to a replacement contract does not preserve the commitment unless the replacement maintains an equivalent or stronger enforceable restriction.

### Impact Claims

The existence, balance, or lock state of the Impact Vault does not independently prove:

- compliant use;
- charitable status;
- charitable impact;
- correct beneficiary selection;
- correct expenditure;
- or meaningful outcomes.

Impact-related claims remain subject to [`transparency-model.md`](transparency-model.md).

---

## Guardian Growth Fund

The Guardian Growth Fund allocation is:

```text
200,000,000 GFC
```

This equals:

```text
20% of the total intended supply
```

This Draft does not yet fully define:

- permitted uses;
- custody structure;
- spending authority;
- distribution schedule;
- recipient eligibility;
- transfer limits;
- lock requirements;
- vesting requirements;
- or reporting requirements.

The allocation name must not be treated as unrestricted authorization.

Before production use, the applicable specification must define the allocation's control surface and permitted-use framework.

---

## Presale Allocation

The Presale Allocation is:

```text
150,000,000 GFC
```

This equals:

```text
15% of the total intended supply
```

The Presale Allocation must remain consistent with the applicable presale specification in [`presale.md`](presale.md).

Presale allocation controls should account for:

- participant entitlements;
- successful finalization;
- failed-sale refunds;
- token claiming;
- unsold tokens;
- rounding;
- invalid purchases;
- duplicate claims;
- migration;
- and reconciliation.

Presale tokens must not become claimable solely because the soft cap is reached before the presale end.

The Presale Allocation must not be used in a manner that creates participant claims exceeding the allocated amount.

---

## Treasury Reserve

The Treasury Reserve allocation is:

```text
150,000,000 GFC
```

This equals:

```text
15% of the total intended supply
```

This Draft does not yet fully define:

- permitted treasury uses;
- approval thresholds;
- spending limits;
- custody architecture;
- signer structure;
- timelocks;
- reporting frequency;
- conflict-of-interest controls;
- or emergency spending authority.

The Treasury Reserve must not be treated as unrestricted administrative property.

Production use must comply with the applicable governance and transparency requirements.

---

## Liquidity Reserve

The Liquidity Reserve allocation is:

```text
150,000,000 GFC
```

This equals:

```text
15% of the total intended supply
```

This Draft does not yet fully define:

- supported liquidity venues;
- deployment schedule;
- custody;
- liquidity-position ownership;
- liquidity withdrawal authority;
- fee ownership;
- rebalancing authority;
- migration;
- lock periods;
- or reporting requirements.

Liquidity provisioning must not be represented as permanent, locked, protocol-owned, or non-withdrawable unless the applicable technical and governance controls support that claim.

---

## Ecosystem Growth Fund

The Ecosystem Growth Fund allocation is:

```text
50,000,000 GFC
```

This equals:

```text
5% of the total intended supply
```

This Draft does not yet fully define:

- eligible recipients;
- grant criteria;
- incentive programs;
- approval requirements;
- distribution limits;
- vesting;
- clawback rights;
- conflict-of-interest controls;
- or reporting requirements.

The allocation must not be used to create undisclosed insider distributions or unreviewable discretionary transfers.

---

## Core Team Allocation

The Core Team allocation is:

```text
50,000,000 GFC
```

This equals:

```text
5% of the total intended supply
```

### Intended Vesting Constraint

The Core Team allocation is intended to be subject to:

```text
19-year linear vesting
```

Before Stable status, the applicable specification and implementation must define:

- vesting commencement event;
- vesting commencement timestamp;
- vesting end timestamp;
- vesting frequency;
- rounding behavior;
- initial claimability;
- whether a cliff exists;
- beneficiary allocation;
- beneficiary replacement;
- revocability;
- acceleration;
- transferability;
- treatment of unclaimed vested tokens;
- treatment of terminated relationships;
- migration;
- recovery authority;
- and administrative control.

### Linear Vesting

Linear vesting must not be represented as implemented unless the production mechanism releases claimable tokens proportionally over the documented 19-year period.

An implementation that permits the entire allocation to be transferred or claimed early through an administrative path does not provide meaningful 19-year vesting unless that path is explicitly disclosed and authorized by the applicable specification.

### Bypass Prohibition

Upgrade, migration, governance, emergency, recovery, or administrative mechanisms must not function as undocumented methods for accelerating or bypassing Core Team vesting.

---

## Unallocated and Unsold Tokens

The current model assigns the full fixed supply to named allocations.

There is therefore no intended unallocated supply at initialization.

The treatment of unsold Presale Allocation tokens remains subject to the final presale and allocation specifications.

Before production deployment, the applicable release must define whether unsold tokens are:

- retained within the Presale Allocation;
- transferred to another allocation;
- permanently locked;
- burned;
- reserved for a later sale;
- or handled through another documented mechanism.

Unsold-token treatment must not be decided retrospectively without an applicable authority and versioned record.

---

## Allocation Changes

A change to any allocation percentage or token amount is a breaking normative change.

Such a change requires:

- explicit versioning;
- rationale;
- supply reconciliation;
- participant-rights analysis;
- governance analysis;
- security analysis;
- implementation analysis;
- migration analysis where relevant;
- updated public communication;
- and an updated change record.

Allocation changes must not increase the total supply beyond the amount defined in [`token.md`](token.md).

---

## Upgradeability

Allocation contracts must disclose whether they are:

- immutable;
- configurable within defined limits;
- upgradeable;
- migratable;
- recoverable;
- or replaceable.

Where upgradeability exists, the applicable documentation must identify:

- upgrade authority;
- approval threshold;
- timelock;
- emergency path;
- implementation replacement process;
- treatment of locked tokens;
- treatment of vested tokens;
- treatment of unvested tokens;
- user or beneficiary notice;
- and historical upgrade records.

Upgradeability must not be used to make a technically restricted allocation functionally unrestricted.

---

## Migration

Allocation migration must preserve:

- supply reconciliation;
- allocation identity;
- applicable locks;
- applicable vesting;
- beneficiary rights;
- custody accountability;
- historical transaction records;
- and known-deviation records.

A migration must identify:

- source address or contract;
- destination address or contract;
- migrated amount;
- migration transaction;
- authority;
- approval record;
- preserved restrictions;
- changed restrictions;
- affected beneficiaries;
- and applicable specification release.

A migration must not create duplicate claims against both the source and destination allocation.

---

## Allocation Disclosure

A production allocation record should disclose:

- allocation name;
- intended purpose;
- initial amount;
- percentage of total supply;
- authenticated address or contract;
- current balance;
- lock status;
- vesting status;
- custody authority;
- spending authority;
- upgrade authority;
- migration authority;
- transfer history;
- known deviations;
- and evidence supporting material public claims.

Protected or security-sensitive information may remain off-chain or non-public where justified.

Privacy protection must not be used as a blanket justification for withholding material authority, balance, or control-surface information.

---

## Conformance

An allocation implementation conforms to this specification only where:

- the total supply is fully reconciled;
- each allocation amount matches the applicable release;
- no undisclosed allocation exists;
- authenticated balances support the represented allocation state;
- applicable locks and vesting are enforced as represented;
- custody and authority are accurately disclosed;
- migrations preserve applicable constraints;
- known deviations are documented;
- and the implementation is mapped to a versioned specification release.

A wallet label, allocation name, user interface, informal statement, or marketing claim does not establish conformance.

---

## Current Unresolved Requirements

The following areas remain unresolved in this Draft:

- detailed permitted use for each allocation;
- allocation-specific custody architecture;
- signer structures;
- approval thresholds;
- allocation-specific timelocks;
- Impact Vault lock commencement;
- Impact Vault post-unlock behavior;
- Core Team vesting commencement;
- Core Team beneficiary structure;
- Core Team cliff and acceleration rules;
- treatment of unsold presale tokens;
- liquidity-position control;
- ecosystem recipient criteria;
- treasury spending framework;
- allocation migration architecture;
- and production contract implementation.

These unresolved areas must not be represented as completed or finalized.

---

## Related Specifications

- [`README.md`](../README.md)
- [`glossary.md`](glossary.md)
- [`non-goals.md`](non-goals.md)
- [`architecture.md`](architecture.md)
- [`token.md`](token.md)
- [`governance-constraints.md`](governance-constraints.md)
- [`transparency-model.md`](transparency-model.md)
- [`presale.md`](presale.md)
- [`../STATUS.md`](../STATUS.md)

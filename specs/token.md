# GFC Token Specification

This document defines the current intended token-level requirements for the Global Foundation Coin (GFC).

---

## Document Status

| Property | Value |
|---|---|
| Maturity | Draft |
| Authority | Normative |
| Version | Unreleased |
| Implementation status | Pre-deployment |
| Intended network | Base Mainnet |
| Chain ID | 8453 |

This document is normative but remains Draft.

It may change materially before a Stable specification release is approved.

It does not represent a deployed or active production token contract.

Current implementation and deployment status is maintained in [`../STATUS.md`](../STATUS.md).

---

## Normative Language

The terms `must`, `must not`, `required`, `should`, `should not`, and `may` are used to distinguish requirements, recommendations, prohibitions, and permitted behavior.

A requirement remains subject to the maturity and version of the applicable specification release.

---

## Scope

This document defines:

- token identity;
- intended network;
- token standard;
- decimals;
- total supply;
- supply constraints;
- inflation constraints;
- intended transfer-fee parameters;
- token-level authority constraints;
- production disclosure requirements;
- and token-level conformance requirements.

This document does not define:

- allocation percentages or token amounts;
- allocation custody;
- allocation locks;
- vesting;
- presale accounting;
- presale refunds;
- treasury spending;
- liquidity operations;
- staking rewards;
- governance voting design;
- impact verification;
- legal classification;
- or regulatory treatment.

Token allocations are defined in [`allocations.md`](allocations.md).

Governance authority is constrained in [`governance-constraints.md`](governance-constraints.md).

---

## Token Identity

A conforming GFC token implementation must use the following intended configuration.

| Property | Required Configuration |
|---|---|
| Token name | Global Foundation Coin |
| Symbol | GFC |
| Network | Base Mainnet |
| Chain ID | 8453 |
| Token standard | ERC-20 compatible |
| Decimals | 18 |
| Maximum intended supply | 1,000,000,000 GFC |
| Supply model | Fixed supply |
| Additional inflation | Prohibited under the current specification |
| Buy fee | 0% |
| Sell fee | 1% |

The historical project name `German Foundation Coin` is deprecated.

It must not be used as the current production token name.

---

## ERC-20 Compatibility

The production token should be compatible with the ERC-20 interface applicable to the approved implementation.

Compatibility must not be claimed solely because function names resemble an ERC-20 implementation.

A production implementation should document:

- supported interfaces;
- deviations from standard ERC-20 behavior;
- transfer restrictions;
- fee behavior;
- approval behavior;
- permit functionality where applicable;
- and any non-standard administrative behavior.

Material deviations must be disclosed before production reliance.

---

## Decimals

The GFC token must use:

```text
18 decimals
```

Public interfaces, accounting systems, allocation records, and presale calculations must use consistent decimal handling.

Rounding behavior that may materially affect participant balances must be documented and tested before production deployment.

---

## Total Supply

The maximum intended token supply is:

```text
1,000,000,000 GFC
```

The production implementation must not create a supply greater than this amount.

The sum of all initial allocations must equal the total intended supply.

The allocation reconciliation is defined in [`allocations.md`](allocations.md).

---

## Fixed-Supply Requirement

The current token model is a fixed-supply model.

After the intended total supply has been established, the implementation must not contain an undocumented mechanism capable of increasing the supply beyond:

```text
1,000,000,000 GFC
```

The following must not be used as hidden inflation mechanisms:

- privileged minting;
- upgrade-based supply expansion;
- migration-based duplication;
- bridge-based duplication represented as native GFC;
- emergency authority;
- governance execution;
- administrative replacement;
- or undocumented token reissuance.

A future change to the fixed-supply model would be a breaking normative change.

Such a change would require:

- explicit versioning;
- rationale;
- participant-rights analysis;
- governance analysis;
- implementation analysis;
- migration analysis;
- and updated public communication.

---

## Inflation

Additional inflation is not permitted under the current specification.

Future rewards, incentives, ecosystem distributions, or staking rewards must originate from tokens already included within the fixed supply unless the applicable specification is formally changed through a breaking versioned process.

The use of existing allocated tokens does not constitute new token issuance.

It must nevertheless comply with the applicable allocation, custody, governance, and disclosure requirements.

---

## Burning

This Draft does not currently establish a general token-burning model.

A production implementation must disclose whether tokens may be:

- permanently burned;
- sent to an inaccessible address;
- administratively recovered;
- reissued through migration;
- or replaced through an upgrade.

Burning must not be represented as reducing supply where an equivalent amount can later be recreated, recovered, or reissued through an undisclosed mechanism.

Any burn authority or recovery authority must be explicitly documented.

---

## Transfer Fees

The current intended fee configuration is:

| Transaction Classification | Intended Fee |
|---|---:|
| Buy | 0% |
| Sell | 1% |

The fee configuration describes the current intended economic behavior.

Before Stable status, the applicable implementation specification must define:

- how a buy is identified;
- how a sell is identified;
- which liquidity venues are recognized;
- how wallet-to-wallet transfers are treated;
- how contract-to-contract transfers are treated;
- whether any addresses are exempt;
- who can create or remove exemptions;
- how the fee is calculated;
- how rounding is handled;
- where collected fee tokens are sent;
- whether collected tokens are burned, retained, converted, or distributed;
- whether the fee is configurable;
- the maximum permitted fee;
- and which authority may change fee-related settings.

A production implementation must not rely on undisclosed fee exemptions or undisclosed transaction-classification rules.

---

## Buy Fee

The intended buy fee is:

```text
0%
```

A conforming implementation must not charge a positive buy fee under the current specification release.

A transfer must not be described as fee-free where a functionally equivalent charge is imposed through:

- hidden deductions;
- adverse conversion rates controlled by the project;
- mandatory side payments;
- or undocumented routing behavior.

Independent network fees and third-party trading fees are not project token fees and should be described separately.

---

## Sell Fee

The intended sell fee is:

```text
1%
```

The production implementation must disclose the exact fee basis and destination.

A 1% sell fee must not be represented as immutable unless the production contract architecture makes unauthorized changes technically impossible.

Where the fee is configurable, the implementation must disclose:

- the authorized role;
- the permitted range;
- the approval threshold;
- any timelock;
- any emergency path;
- and the historical record of changes.

An unrestricted or undisclosed authority to increase the fee is not consistent with the current intended control model.

---

## Fee Proceeds

This Draft does not yet define the final use, custody, conversion, or distribution of sell-fee proceeds.

Before production deployment, the applicable specification must identify:

- the receiving address or contract;
- the allocation or accounting category;
- custody authority;
- transfer authority;
- conversion authority;
- spending authority;
- reporting requirements;
- and applicable transparency evidence.

A fee recipient must not be described as a treasury, impact fund, liquidity fund, or other purpose-specific allocation unless the relevant restrictions and authority are documented.

---

## Token-Level Administrative Authority

Token-level administrative authority must be:

- explicit;
- limited;
- attributable;
- reviewable;
- consistent with least privilege;
- and disclosed before production reliance.

The production implementation must disclose whether any authority can:

- mint;
- burn;
- pause transfers;
- block addresses;
- exempt addresses from fees;
- modify fees;
- modify transaction classification;
- upgrade the token;
- migrate balances;
- recover tokens;
- alter metadata;
- replace administrative roles;
- or change integration addresses.

The absence of a disclosed authority must not be interpreted as proof that the authority does not exist.

Contract code and authenticated deployment state determine the actual technical control surface.

---

## Token Ownership and Governance

Token ownership alone must not automatically provide unrestricted authority over:

- project assets;
- protected information;
- administrative roles;
- treasury assets;
- allocation contracts;
- beneficiary information;
- evidence classifications;
- long-term locks;
- vesting commitments;
- or legal and organizational decisions.

Any governance rights associated with token ownership must be defined separately.

The existence of token voting must not be represented as complete decentralization.

---

## Upgradeability

A production token implementation must disclose whether it is:

- technically immutable;
- configurable within defined limits;
- upgradeable;
- replaceable;
- or migratable.

Upgrade, migration, governance, or emergency mechanisms must not function as undocumented methods for bypassing:

- the fixed-supply requirement;
- the intended fee configuration;
- allocation constraints;
- participant rights;
- or disclosed authority boundaries.

Where upgradeability exists, the applicable documentation must identify:

- upgrade authority;
- approval threshold;
- timelock;
- emergency path;
- implementation replacement process;
- storage and balance implications;
- user notice;
- exit options where applicable;
- and historical upgrade records.

---

## Migration

A token migration must not create undisclosed duplicate economic claims.

A migration process should define:

- the source token;
- the destination token;
- conversion ratio;
- eligibility;
- snapshot method;
- claim process;
- migration deadline;
- treatment of unclaimed balances;
- treatment of locked balances;
- treatment of vesting balances;
- treatment of fee proceeds;
- administrative authority;
- and supply reconciliation.

The combined effective supply across source and destination systems must remain consistent with the applicable versioned specification.

---

## Deployment Requirements

A production token deployment should identify:

- network;
- chain ID;
- authenticated contract address;
- deployment transaction;
- source-code release or commit;
- compiler and build information where applicable;
- applicable specification release;
- constructor or initialization parameters;
- initial supply recipient;
- allocation mapping;
- administrative roles;
- fee settings;
- upgradeability;
- pause authority;
- migration authority;
- verification status;
- test status;
- audit status;
- and known deviations.

These records should be linked from [`../STATUS.md`](../STATUS.md).

---

## Conformance

A token implementation conforms to this specification only where:

- actual deployed behavior satisfies the applicable normative requirements;
- authenticated on-chain state matches the represented configuration;
- supply does not exceed the permitted amount;
- token identity and decimals match the specification;
- fee behavior matches the applicable release;
- administrative authority is accurately disclosed;
- allocation reconciliation is preserved;
- known deviations are documented;
- and the implementation is mapped to a versioned specification release.

A user interface, website, wallet label, informal statement, or marketing claim does not establish conformance.

Deployment alone does not establish conformance.

---

## Current Unresolved Requirements

The following areas remain unresolved in this Draft:

- precise buy and sell classification;
- recognized liquidity venues;
- fee calculation and rounding;
- fee-recipient architecture;
- fee-proceeds use;
- fee configurability;
- fee exemptions;
- burn functionality;
- recovery functionality;
- pause functionality;
- blocklist functionality;
- upgrade architecture;
- migration architecture;
- governance rights connected to token ownership;
- and production contract implementation.

These unresolved areas must not be represented as completed or finalized.

---

## Related Specifications

- [`README.md`](README.md)
- [`glossary.md`](glossary.md)
- [`non-goals.md`](non-goals.md)
- [`architecture.md`](architecture.md)
- [`allocations.md`](allocations.md)
- [`governance-constraints.md`](governance-constraints.md)
- [`transparency-model.md`](transparency-model.md)
- [`presale.md`](presale.md)
- [`../STATUS.md`](../STATUS.md)

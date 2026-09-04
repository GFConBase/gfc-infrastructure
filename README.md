# Global Foundation Coin Infrastructure

This repository contains the current technical specifications, status records, deployment records, security policy, and reference documentation for **Global Foundation Coin (GFC)**.

The current primary product focus is the:

**GFC Token / Economic Layer**

The longer-term direction is broader:

**Accountability Infrastructure**

based on the canonical accountability model:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

GFC follows a specification-first and status-aware development approach:

- intended behavior is documented before production reliance;
- material authority and discretion are made explicit;
- participant rights and economic constraints are defined before activation;
- security assumptions are treated as part of the architecture;
- transparency claims are separated from evidence strength;
- Pilot and Production are kept distinct;
- and implementation status is communicated using defined terminology.

This repository is currently in **pre-mainnet specification and pilot development**.

It does **not** represent an official Base Mainnet GFC token, a live GFC presale, operational production staking, deployed production governance, or a complete production Transparency Registry.

---

## Current Status

| Property | Current Status |
|---|---|
| Project | Global Foundation Coin |
| Abbreviation | GFC |
| Repository stage | Pre-mainnet specification and pilot development |
| Specification release | Draft / Unreleased |
| Primary product focus | GFC Token / Economic Layer |
| Long-term direction | Accountability Infrastructure |
| Intended production network | Base Mainnet |
| Production chain ID | `8453` |
| Public pilot network | Base Sepolia |
| Pilot chain ID | `84532` |
| Production GFC token | **Not Deployed** |
| Presale | **Not Live** |
| Production staking | **Not Deployed / Not Operational** |
| Complete production Transparency Registry | **Not Deployed** |

The existence of a specification does not mean that the described component has been:

- implemented;
- tested;
- reviewed;
- audited;
- deployed;
- live;
- active;
- operational;
- or independently verified.

See [`STATUS.md`](STATUS.md) for the current project and implementation state.

See [`DEPLOYMENTS.md`](DEPLOYMENTS.md) for authenticated or established deployment records.

---

## Public Base Sepolia Pilot

A public GFC pilot exists on Base Sepolia.

| Property | Pilot Record |
|---|---|
| Environment | Public pilot / testnet |
| Network | Base Sepolia |
| Chain ID | `84532` |
| Token | `tGFC` |
| Contract | `0x7262Cca91938ede6bB6560F81104Aa410848e7f3` |
| Public pilot date | 2026-08-02 |
| Source status | Verified |
| Production status | **Non-production** |

The pilot demonstrates limited public testnet execution.

It does **not** establish:

- an official Base Mainnet GFC token;
- a live presale;
- production tokenomics;
- production allocations;
- production staking;
- production treasury or liquidity infrastructure;
- production governance;
- production authority assignments;
- a completed production security audit;
- a complete production Transparency Registry;
- or proof that future production deployments will reuse the same code, parameters, addresses, or authority.

> **Pilot does not mean Production.**

---

## Current Product Direction

### Near-term focus

Through the end of Q1 2027, the current operational priority is to move the **GFC Token / Economic Layer** toward credible production readiness.

Supporting work includes:

- token architecture;
- allocations;
- vesting and locks;
- economic flows;
- presale design;
- staking design;
- governance constraints;
- authority mapping;
- security;
- testing;
- deployment planning;
- transparency;
- legal preparation;
- partnerships;
- funding;
- website and public documentation;
- and public communication.

### Long-term direction

From Q2 2027 onward, the intended direction broadens toward wider Accountability Infrastructure.

That longer-term infrastructure is intended to connect:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

The broader system is not represented as fully implemented or operational today.

See [`ROADMAP.md`](ROADMAP.md) for the current sequencing.

---

## Canonical Accountability Model

The current canonical GFC model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

The model asks six connected questions.

### Funds

What assets, resources, rights, or economic value were involved?

### Authority

Who or what had the power to act?

### Rules

Which technical, governance, contractual, or operational constraints applied?

### Decisions

What was proposed, approved, rejected, executed, changed, or withheld?

### Outcomes

What actually happened?

### Evidence

What supports the represented history and how strong is that support?

No individual stage proves all later stages.

For example:

> A transaction does not prove legitimate authority.

> Legitimate authority does not prove compliant use.

> Compliant use does not prove a positive outcome.

> A positive outcome does not automatically prove broader impact.

The older Technology / Governance / Evidence-and-Outcomes grouping may still be used as a supporting explanatory view, but it does not replace the canonical accountability model.

---

## Repository Purpose

The repository provides a reviewable reference for the intended GFC technical and accountability architecture.

It documents:

- current project decisions;
- what is deployed and what is not;
- what the system is intended to do;
- what the system must not do;
- token and economic constraints;
- material authority boundaries;
- participant protections;
- security assumptions;
- fund-flow relationships;
- evidence and verification distinctions;
- historical status requirements;
- and unresolved questions that must remain unresolved until explicitly decided.

The repository is intended to reduce:

- undocumented assumptions;
- implicit authority;
- contradictory specifications;
- accidental status overstatement;
- retrospective rule changes;
- uncontrolled scope expansion;
- and divergence between intended and implemented behavior.

---

## Core Principles

### Specification before production reliance

Material production behavior should be specified before participants or material assets rely on it.

### Explicit authority

Material technical and operational authority should be attributable and reviewable.

### Constraints before hidden discretion

Upgrade, pause, migration, recovery, treasury, fee, and emergency authority should remain bounded.

### Participant rights before operational convenience

Presale refunds, vesting rights, and other participant protections must not be weakened merely because doing so is operationally convenient.

### Fixed-supply integrity

The current GFC design uses a fixed intended total supply of:

```text
1,000,000,000 GFC
```

Additional discretionary inflation is prohibited under the current model.

### Evidence before claims

The strength of a public claim must not exceed the strength of its supporting evidence.

### Privacy-aware transparency

Transparency does not require unnecessary publication of personal, beneficiary, confidential, legally protected, or security-sensitive information.

### Historical accountability

Material changes, corrections, disputes, incidents, downgrades, migrations, and superseded records should remain historically reviewable where appropriate.

### No retrospective normalization

Specifications and status records must not be rewritten after an event merely to make unauthorized or non-conforming behavior appear compliant.

---

## Verification Model

GFC distinguishes among different verification questions.

### Transaction

Did the transaction occur as represented?

### Authority

Was the actor or mechanism authorized to act?

### Rules

What rules applied at the time?

### Use of Funds

Were funds used for the documented purpose?

### Outcome

Did the documented activity produce the represented result?

### Impact

Did the activity contribute to a meaningful broader or longer-term result?

These require different forms of evidence.

> **Transaction Verified ≠ Use Verified**

> **Use Verified ≠ Outcome Verified**

> **Outcome Verified ≠ Impact Verified**

The transparency model also distinguishes among:

- public on-chain evidence;
- cryptographically anchored evidence;
- and protected off-chain evidence.

Cryptographic integrity can support record integrity or historical existence.

It does not independently prove factual truth.

See [`specs/transparency-model.md`](specs/transparency-model.md).

The mapping from normative conformance requirements to observable evidence, authenticated implementation bindings, and explicit evidence ceilings is defined separately in [`specs/conformance-verification.md`](specs/conformance-verification.md).

That verification layer does not assume undeployed Base Mainnet contracts, interfaces, events, storage layouts, or addresses. Production verification requires bindings to the authenticated production implementation.

---

## Formal Specification Set

The formal specification set is located in [`specs/`](specs/).

| Document | Primary Responsibility |
|---|---|
| [`specs/README.md`](specs/README.md) | Specification index, maturity, authority, reading order, and release model |
| [`specs/glossary.md`](specs/glossary.md) | Shared terminology and status vocabulary |
| [`specs/non-goals.md`](specs/non-goals.md) | Intentional exclusions and unsupported interpretations |
| [`specs/architecture.md`](specs/architecture.md) | System architecture, components, trust boundaries, and design constraints |
| [`specs/roles-and-authority.md`](specs/roles-and-authority.md) | Roles, material authority, assignment boundaries, and responsibility |
| [`specs/governance-constraints.md`](specs/governance-constraints.md) | Governance constraints, upgrades, pauses, timelocks, emergency authority, and authority records |
| [`specs/security-model.md`](specs/security-model.md) | Technical security model, threat surfaces, invariants, and production security requirements |
| [`specs/token.md`](specs/token.md) | Token identity, fixed supply, fees, token authority, upgrades, and conformance |
| [`specs/allocations.md`](specs/allocations.md) | Canonical allocations, custody boundaries, restrictions, and reconciliation |
| [`specs/vesting-and-unlocks.md`](specs/vesting-and-unlocks.md) | Impact Vault lock and Core Team vesting requirements |
| [`specs/economic-flows.md`](specs/economic-flows.md) | Token, fee, Presale, treasury, liquidity, staking, and other economic flows |
| [`specs/staking.md`](specs/staking.md) | Hybrid non-inflationary staking requirements and unresolved design boundaries |
| [`specs/presale.md`](specs/presale.md) | Presale pricing, payment assets, immediate distribution, refunds, custody, and finalization |
| [`specs/transparency-model.md`](specs/transparency-model.md) | Evidence, claims, historical records, Registry design, privacy, review, and transparency |
| [`specs/conformance-verification.md`](specs/conformance-verification.md) | Mapping of normative conformance requirements to observable evidence, implementation-specific bindings, and evidence ceilings |

The recommended reading order and document relationships are maintained in [`specs/README.md`](specs/README.md).

---

## Token Model

The current Draft production-token design specifies:

| Property | Current Draft Configuration |
|---|---|
| Token name | Global Foundation Coin |
| Symbol | GFC |
| Intended production network | Base Mainnet |
| Chain ID | `8453` |
| Standard | ERC-20-compatible |
| Decimals | 18 |
| Total supply | 1,000,000,000 GFC |
| Supply model | Fixed supply |
| Additional discretionary inflation | Prohibited |
| Intended buy fee | 0% |
| Intended sell fee | 1% |

No production GFC token is currently deployed on Base Mainnet.

The exact production token architecture remains subject to unresolved implementation decisions, including:

- supply-creation method;
- buy/sell classification;
- recognized liquidity pools;
- fee destination;
- fee exemptions;
- upgradeability;
- pause behavior;
- migration;
- recovery;
- and exact privileged authority.

See [`specs/token.md`](specs/token.md).

---

## Allocation Model

The current Draft supply allocation is:

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

These are current Draft specification values.

They do not represent funded production wallets or deployed allocation contracts.

See [`specs/allocations.md`](specs/allocations.md).

---

## Long-Term Lock and Vesting Constraints

### Impact Vault

Current intended allocation:

```text
250,000,000 GFC
```

Current intended restriction:

```text
50-year lock
```

No production lock-start timestamp is currently established.

No production Impact Vault contract is currently recorded.

### Core Team

Current intended allocation:

```text
50,000,000 GFC
```

Current intended restriction:

```text
19-year linear vesting
```

No production vesting-start timestamp or beneficiary structure is currently established.

No production Core Team vesting contract is currently recorded.

See [`specs/vesting-and-unlocks.md`](specs/vesting-and-unlocks.md).

---

## Presale Status and Current Draft Model

No GFC presale is currently live.

No precise public presale launch date is established through this repository.

The current Draft model includes:

| Parameter | Current Draft Value |
|---|---:|
| Reference price | €0.05 per GFC |
| Intended duration | 8 weeks |
| Soft cap | €250,000 reference value |
| Separate monetary hard cap | None |
| Presale allocation | 150,000,000 GFC |
| Maximum GFC distribution | 150,000,000 GFC |
| Intended payment assets | ETH, USDC, DAI on Base |
| Token delivery | Immediate Distribution |
| Failed-sale protection | Refund right if the applicable success condition is not satisfied |
| Material participant-facing logic | Intended to be immutable after production deployment |

At €0.05 per GFC, full use of the 150,000,000 GFC Presale allocation corresponds to a maximum gross reference value of:

```text
€7,500,000
```

This is not a fundraising guarantee.

### Critical unresolved Presale issue

The current design combines:

- **Immediate GFC Distribution**; and
- participant refund rights after failed finalization.

The final treatment of GFC already distributed to a participant if the Presale fails remains unresolved.

No current specification authorizes an improvised:

- clawback;
- forced transfer;
- forced burn;
- mandatory participant return;
- token invalidation;
- blacklist-based immobilization;
- negative balance;
- or replacement-token mechanism.

This issue is a **production activation blocker**.

The production Presale must not activate until the interaction is technically, economically, normatively, and participant-facingly resolved.

See [`specs/presale.md`](specs/presale.md).

---

## Staking Status

No production GFC staking system is currently operational.

The current Draft design direction is:

**Hybrid and Non-Inflationary**

Under the current model:

- staking must not create additional GFC supply;
- rewards must come from GFC already within the fixed supply or another explicitly specified non-minting economic source;
- no reward source is currently finalized;
- no APR or APY is currently finalized;
- no lock period is currently finalized;
- no reward duration is currently finalized;
- and no staking-related governance right is currently finalized.

A displayed future APR or APY must not be represented as guaranteed.

See [`specs/staking.md`](specs/staking.md).

---

## Economic Flows

The Economic Layer distinguishes among:

- allocation;
- custody;
- transfer;
- fee collection;
- fee use;
- contribution;
- refundable contribution;
- finalized proceeds;
- lock;
- vesting;
- claim;
- treasury expenditure;
- liquidity deployment;
- staking principal;
- staking reward;
- migration;
- and recovery.

Important distinctions include:

> Allocation is not expenditure.

> Custody is not unrestricted ownership.

> Fee collection is not fee use.

> Liquidity Reserve is not active liquidity.

> Vesting is not the same as transfer.

> Internal transfers are not new external funding.

The final destination and use of the intended 1% sell fee remain unresolved.

See [`specs/economic-flows.md`](specs/economic-flows.md).

---

## Governance and Authority

GFC's current governance constraints emphasize:

- explicit authority;
- least privilege;
- separation of duties;
- bounded upgrades;
- bounded pause authority;
- predictable exceptions;
- timelocks where appropriate;
- constrained emergency powers;
- attributable role changes;
- and historical reviewability.

No production governance contract, multisig, signer set, threshold, quorum, or voting system is established as official by this repository.

Token ownership does not automatically create unrestricted governance authority.

Staking does not automatically create unrestricted governance authority.

A multisig does not automatically prove decentralization or signer independence.

See:

- [`specs/roles-and-authority.md`](specs/roles-and-authority.md)
- [`specs/governance-constraints.md`](specs/governance-constraints.md)

---

## Transparency Registry Direction

The planned Transparency Registry is intended to operate as:

**Versioned Historical Accountability — Not a Permanent Approval Badge**

Registry inclusion must not automatically imply:

- permanent approval;
- permanent verification;
- permanent endorsement;
- perpetual compliance;
- or permanent evidence validity.

A future Registry should be able to preserve changes in:

- what was disclosed;
- what evidence supported the disclosure;
- what rules applied;
- what authority applied;
- what claim was made;
- what status existed;
- when that status changed;
- and why it changed.

Potential future status actions may include:

- admission;
- verification;
- correction;
- downgrade;
- suspension;
- supersession;
- and removal from current presentation

under a later-defined authority model.

No complete production Transparency Registry is currently deployed.

See [`specs/transparency-model.md`](specs/transparency-model.md).

---

## Security

Security is treated as a continuous system property.

The repository separates:

- repository-level vulnerability reporting and disclosure policy in [`SECURITY.md`](SECURITY.md); and
- detailed technical threat modeling and security requirements in [`specs/security-model.md`](specs/security-model.md).

The current private security contact is:

```text
info@globalfoundationcoin.org
```

Sensitive vulnerabilities should not be disclosed through public issues where premature disclosure could place users, assets, credentials, protected information, pilot systems, or future production systems at risk.

No independent production security audit is currently represented as completed.

> Source Verified ≠ Audited

> Tested ≠ Audited

> Audited ≠ Risk-Free

---

## Source of Authority

The continuously changing `main` branch is not automatically the production source of authority.

A future production implementation should identify:

- applicable specification version;
- applicable source release or commit;
- intended network;
- authenticated contract addresses;
- authenticated wallet addresses;
- deployment records;
- applicable conformance-verification mapping;
- authenticated implementation-specific verification bindings where required;
- privileged authority;
- upgradeability;
- pause authority;
- migration authority;
- testing status;
- review or audit status;
- and known deviations.

Authenticated deployed contract state determines what technically executed.

The applicable versioned specification determines the intended normative requirements.

Conformance requires the deployed implementation to satisfy those applicable requirements.

---

## Root Repository Documents

| Document | Purpose |
|---|---|
| [`STATUS.md`](STATUS.md) | Current project, implementation, deployment, and operational status |
| [`DEPLOYMENTS.md`](DEPLOYMENTS.md) | Authenticated or established deployment records |
| [`ROADMAP.md`](ROADMAP.md) | Current intended development sequence and readiness gates |
| [`DECISIONS.md`](DECISIONS.md) | Canonical working decisions, constraints, historical facts, and open decisions |
| [`SECURITY.md`](SECURITY.md) | Security reporting, vulnerability handling, and coordinated-disclosure policy |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Contribution and specification-change guidance |
| [`CHANGELOG.md`](CHANGELOG.md) | Repository-level change history |
| [`specs/README.md`](specs/README.md) | Formal specification index and release model |

---

## Decisions and Open Questions

[`DECISIONS.md`](DECISIONS.md) distinguishes among:

- Canonical Working Decisions;
- Constraints;
- Historical Facts;
- and Open Decisions.

Open decisions must remain open until explicitly resolved.

Current material open decisions include, among others:

- final production token architecture;
- final fee destination and fee-proceeds use;
- final production custody;
- final staking reward source;
- final Presale pricing architecture;
- treatment of already distributed GFC after failed Presale finalization;
- unsold Presale GFC treatment;
- final governance structure;
- and final production Transparency Registry architecture.

Unresolved details must not be invented merely to make the repository appear complete.

---

## Contributions

Contribution guidance is maintained in [`CONTRIBUTING.md`](CONTRIBUTING.md).

Dedicated branches and pull requests are **recommended** for material changes because they improve reviewability and history.

This repository does not currently claim that a specific branch, pull-request, maintainer-vote, or approval-threshold process is mandatory unless separately adopted.

Material normative changes should identify relevant:

- rationale;
- decision impact;
- security impact;
- governance impact;
- participant-rights impact;
- economic impact;
- implementation impact;
- migration impact;
- and public-communication impact.

A contribution is not automatically a project decision.

A merged Draft is not automatically Stable.

---

## Change History

Repository-level changes are documented in [`CHANGELOG.md`](CHANGELOG.md).

Git history provides technical revision history.

Git history alone is not a replacement for:

- versioned releases;
- deployment records;
- decision records;
- migration records;
- known-deviation records;
- implementation mappings;
- incident records;
- or deprecation records.

---

## Repository Boundaries

This repository is intended for:

- formal technical specifications;
- architecture;
- governance and authority constraints;
- token and allocation requirements;
- vesting and unlock requirements;
- economic flows;
- staking requirements;
- Presale requirements;
- transparency and evidence requirements;
- security models;
- deployment and status records;
- decision and roadmap records;
- terminology;
- contribution guidance;
- and repository history.

It is not intended for:

- social-media content;
- promotional campaign copy;
- hype-driven messaging;
- token-price predictions;
- guaranteed-return claims;
- guaranteed-impact claims;
- unauthenticated launch promises;
- private operational information;
- private keys;
- credentials;
- personal beneficiary information;
- or unsupported legal representations.

---

## Naming

The current project name is:

**Global Foundation Coin**

The abbreviation is:

**GFC**

The historical name `German Foundation Coin` is deprecated for current technical and production naming.

Historical references may remain where necessary to preserve accurate archival context.

The name Global Foundation Coin does not independently establish:

- a legal foundation;
- nonprofit status;
- charitable status;
- tax-exempt status;
- governmental approval;
- regulatory approval;
- or any specific legal form.

---

## License

No separate `LICENSE` file is currently present in the publicly visible repository root.

No explicit open-source license is currently declared by this repository.

Accordingly, contributors and users should not assume that the repository content is licensed for unrestricted reuse, modification, or redistribution.

Any rights arising from applicable law, GitHub platform terms, or other explicitly applicable terms remain unaffected.

If an explicit repository license is adopted later, the applicable `LICENSE` file and related documentation should be treated as the authoritative licensing reference.

---

## Current Roadmap Snapshot

| Period | Primary Objective | Current Status |
|---|---|---|
| Aug–Sep 2026 | Foundation Finalization | **Active** |
| Q4 2026 | Production design, implementation, and testing | **Planned** |
| Q1 2027 | Mainnet and Presale readiness / potential Presale start | **Planned** |
| Q2 2027 | Broader production expansion and transparency build-out | **Planned** |
| H2 2027+ | Accountability Infrastructure expansion | **Planned** |
| Later, if justified | Dedicated execution environment evaluation | **Proposed future option** |

A planning window is not a launch guarantee.

See [`ROADMAP.md`](ROADMAP.md).

---

## Core Distinctions

> Draft does not mean Stable.

> Specified does not mean Implemented.

> Implemented does not mean Tested.

> Tested does not mean Audited.

> Source Verified does not mean Audited.

> Audited does not mean Risk-Free.

> Deployed does not automatically mean Operational.

> Deployed does not automatically mean Conforming.

> Pilot does not mean Production.

> Base Sepolia does not mean Base Mainnet.

> `tGFC` does not mean the production GFC token.

> A wallet label does not establish authority or purpose.

> An allocation label does not prove compliant use.

> Token ownership does not automatically create unrestricted governance authority.

> Immediate Presale distribution does not eliminate refund obligations.

> Staking rewards must not create additional GFC under the current model.

> Registry inclusion does not mean permanent approval.

> Cryptographic integrity does not equal factual truth.

> Transaction verification does not equal use-of-funds verification.

> Use-of-funds verification does not equal outcome verification.

> Outcome verification does not automatically equal impact verification.

> The `main` branch is not automatically the production source of authority.

> Different claims require different evidence.

GFC is intended to make **Funds, Authority, Rules, Decisions, Outcomes, Evidence, participant rights, limitations, and historical changes** more explicit and reviewable before production reliance.

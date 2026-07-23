# Global Foundation Coin Infrastructure

This repository contains the current specifications and reference documentation for the planned Global Foundation Coin (GFC) infrastructure.

GFC follows a specification-first development approach:

- intended behavior is documented before production implementation;
- authority and discretion are explicitly constrained;
- participant rights and fund-flow rules are defined before deployment;
- transparency claims are separated from evidence strength;
- and implementation status is communicated accurately.

This repository is currently focused on architecture and specification development.

It does not represent a live token deployment, active presale, operational governance system, or completed transparency platform.

---

## Current Status

**Project:** Global Foundation Coin  
**Abbreviation:** GFC  
**Specification Maturity:** Draft  
**Specification Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-deployment  
**Intended Network:** Base Mainnet  
**Chain ID:** 8453  

At the time of publication:

- no production GFC token contract is represented by this repository as deployed;
- no GFC presale is live;
- no public presale date has been announced through this repository;
- no production contract address is established as official;
- no production wallet address is established as official;
- no staking system is represented as operational;
- no production treasury or governance infrastructure is represented as active;
- no complete transparency or impact-verification platform is represented as deployed;
- and all specifications remain subject to review and versioned revision.

The existence of a specification does not mean that the described component has already been:

- implemented;
- tested;
- independently reviewed;
- audited;
- deployed;
- activated;
- or made available to users.

---

## Purpose

The purpose of this repository is to provide a clear, reviewable, and historically accountable reference for the intended GFC infrastructure.

It documents:

- what the system is intended to do;
- what the system must not do;
- how material authority is constrained;
- how participant funds and rights are intended to be protected;
- how token allocations are intended to be controlled;
- how transparency claims must be supported;
- how on-chain and off-chain evidence are distinguished;
- and how future implementations should be mapped to applicable specification releases.

The repository is intended to reduce:

- undocumented assumptions;
- implicit administrative authority;
- contradictory public statements;
- retrospective rule changes;
- uncontrolled scope expansion;
- and divergence between intended and implemented behavior.

---

## Repository Principles

### Specification before deployment

Material production behavior should be specified before contracts or operational systems are deployed.

### Constraints before discretion

Privileged authority should remain limited, documented, attributable, and reviewable.

### Evidence before claims

The strength of a public claim must not exceed the strength of the evidence supporting it.

### Accurate implementation status

Planned, specified, implemented, tested, reviewed, audited, deployed, active, and operational are distinct states.

### Privacy-aware transparency

Transparency does not require unnecessary publication of personal, beneficiary, confidential, legally protected, or security-sensitive information.

### Historical accountability

Material changes, corrections, deviations, incidents, and superseded specifications should remain historically reviewable.

### No retrospective normalization

Specifications must not be changed after an event merely to make unauthorized or non-conforming behavior appear compliant.

---

## Intended System Model

The planned GFC infrastructure is organized across three related but distinct layers.

### Technology

The Technology layer may include:

- the GFC token;
- token allocation contracts;
- presale contracts;
- lock and vesting contracts;
- treasury and custody mechanisms;
- staking infrastructure;
- governance execution contracts;
- public transaction records;
- and cryptographic evidence commitments.

Technology determines what technically executed.

### Governance

The Governance layer defines:

- authority;
- approvals;
- signer structures;
- proposal processes;
- voting and delegation;
- timelocks;
- upgrade authority;
- pause authority;
- migration authority;
- conflicts of interest;
- emergency powers;
- and responsibility boundaries.

Governance determines who was authorized to act and under which rules.

### Impact and Evidence

The Impact and Evidence layer addresses:

- intended use of funds;
- supporting documentation;
- evidence provenance;
- evidence review;
- reconciliation;
- outputs;
- outcomes;
- impact methodology;
- uncertainty;
- corrections;
- and disputes.

This layer determines what can be supported beyond technical transaction execution.

No single layer is sufficient by itself.

---

## Transparency Model

GFC distinguishes between three separate verification questions.

### Transaction

**Did the funds move as stated?**

Relevant evidence may include:

- on-chain transactions;
- contract events;
- wallet balances;
- timestamps;
- and verified contract state.

### Use

**Were the funds used for the documented purpose?**

Relevant evidence may include:

- approvals;
- agreements;
- invoices;
- receipts;
- delivery records;
- reconciliations;
- and protected supporting documentation.

### Impact

**Did the documented use create a meaningful result?**

Relevant evidence may include:

- outputs;
- outcome indicators;
- follow-up data;
- methodology;
- independent evaluation;
- uncertainty disclosures;
- and impact assessments.

The following distinction is foundational:

> TRANSACTION VERIFIED does not equal IMPACT VERIFIED.

Different claims require different evidence.

---

## Evidence Disclosure Levels

The planned transparency model distinguishes between three evidence classes.

### Public On-Chain

Information publicly recorded or directly derivable from authenticated blockchain data.

Examples may include:

- contract addresses;
- transfers;
- balances;
- allocation state;
- lock state;
- vesting state;
- governance execution;
- and cryptographic commitments.

### Cryptographically Anchored

Off-chain records whose integrity is linked to a public:

- hash;
- digital signature;
- timestamp;
- Merkle root;
- or equivalent cryptographic commitment.

Cryptographic anchoring may support record integrity or existence.

It does not independently prove that the underlying information is factually correct.

### Protected Off-Chain

Information retained outside the public blockchain because it is:

- personal;
- confidential;
- legally protected;
- commercially sensitive;
- operationally sensitive;
- or security-sensitive.

Protected evidence may remain reviewable without being publicly exposed.

---

## Intended Token Model

The currently specified token model includes:

| Property | Intended Configuration |
|---|---|
| Token name | Global Foundation Coin |
| Symbol | GFC |
| Network | Base Mainnet |
| Chain ID | 8453 |
| Token standard | ERC-20 compatible |
| Decimals | 18 |
| Total supply | 1,000,000,000 GFC |
| Supply model | Fixed supply |
| Additional inflation | Not intended |
| Buy fee | 0% |
| Sell fee | 1% |

These values describe the current intended design.

They do not represent a deployed or active token contract.

---

## Intended Token Allocation

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

Current intended long-term constraints include:

- a 50-year lock for the Impact Vault allocation;
- 19-year linear vesting for the Core Team allocation;
- no discretionary expansion beyond the fixed total supply;
- and documented authority and custody requirements for material allocations.

An allocation name describes intended use.

It does not independently prove that the allocation is technically restricted or used in accordance with that purpose.

---

## Intended Presale Model

The current Draft presale specification defines the following intended parameters:

| Property | Intended Configuration |
|---|---|
| Reference price | €0.05 per GFC |
| Duration | 8 weeks |
| Soft cap | €250,000 |
| Presale Allocation | 150,000,000 GFC |
| Separate monetary hard cap | None currently intended |
| Maximum gross reference value | €7,500,000 at full allocation |
| Token delivery | Claim after successful finalization |
| Failed-sale protection | Participant refund |
| Project access to contributions | Only after successful finalization |

The presale is intended to use deferred claiming rather than immediate token distribution.

A valid purchase would create a token entitlement.

Tokens would become claimable only after:

- the presale has ended;
- the applicable success conditions have been satisfied;
- and successful finalization has occurred.

Reaching the soft cap before the presale end would not independently:

- end the presale;
- activate token claims;
- eliminate refund protections;
- or make participant contributions available for project use.

No presale is currently live.

No public presale date is established by this repository.

---

## Governance Boundaries

The current governance specification is intended to constrain:

- token supply authority;
- fee authority;
- treasury authority;
- presale authority;
- liquidity authority;
- lock and vesting authority;
- staking authority;
- upgrade authority;
- pause authority;
- migration authority;
- emergency authority;
- signer appointment and removal;
- evidence-status authority;
- and impact-claim authority.

Material governance principles include:

- explicit authority;
- least privilege;
- separation of duties;
- documented approval thresholds;
- multisig controls where appropriate;
- timelocks where appropriate;
- conflict-of-interest disclosure;
- historical decision records;
- and public disclosure of the material control surface.

A multisig does not automatically prove decentralization or signer independence.

Token ownership alone is not intended to provide unrestricted authority over project assets, protected information, administrative roles, or long-term commitments.

---

## Long-Term Commitments

The current architecture includes intended long-term commitments relating to:

- fixed token supply;
- the 50-year Impact Vault lock;
- the 19-year Core Team vesting period;
- presale refund protections;
- allocation integrity;
- and documented authority boundaries.

Upgrade, migration, governance, or emergency mechanisms must not function as undocumented methods for bypassing those commitments.

Any production implementation must disclose whether a commitment is:

- technically immutable;
- configurable within defined limits;
- upgradeable;
- migratable;
- dependent on governance;
- or dependent on off-chain enforcement.

---

## Staking

A hybrid staking model may be introduced in the future.

Potential functions may include:

- moderate token rewards;
- governance-related participation;
- community-related benefits;
- or ecosystem utility.

The staking design is not finalized.

This repository does not currently guarantee:

- that staking will launch;
- a particular annual percentage rate;
- a particular lock period;
- a particular reward duration;
- a particular governance right;
- or permanent reward availability.

Any future staking rewards must originate from tokens already included within the fixed supply unless the applicable specifications are formally changed through a versioned process.

---

## What This Repository Does Not Claim

This repository does not claim or guarantee:

- short-term token appreciation;
- profit;
- passive income;
- price stability;
- capital preservation;
- continuous liquidity;
- exchange listing;
- successful presale completion;
- successful project outcomes;
- charitable impact;
- complete decentralization;
- complete automation;
- complete transparency;
- elimination of trust;
- permanent security;
- legal-foundation status;
- nonprofit status;
- charitable status;
- tax-exempt status;
- tax deductibility;
- regulatory approval;
- or governmental recognition.

The name Global Foundation Coin does not by itself establish any legal or charitable status.

---

## Specification Status Model

Each formal specification declares maturity and authority separately.

### Maturity

#### Draft

The document is under active development and may change materially.

#### Review

The document is structurally complete and awaiting formal review or approval.

#### Stable

The document has been approved for a defined implementation or release.

Stable does not independently mean implemented, audited, deployed, immutable, legally approved, or operational.

#### Deprecated

The document is retained for historical reference but is no longer intended for new implementations.

### Authority

#### Informative

The document provides explanation or context but does not independently define binding requirements.

#### Normative

The document defines requirements, constraints, invariants, terminology, rights, or prohibited behavior.

`Normative` is not a maturity level.

A specification may therefore be both Draft and Normative.

---

## Current Specifications

The formal specification set is located in [`specs/`](specs/).

| Document | Purpose |
|---|---|
| [`specs/README.md`](specs/README.md) | Index, status model, reading order, release model, and repository-level specification rules |
| [`specs/glossary.md`](specs/glossary.md) | Shared terminology used across the specification set |
| [`specs/non-goals.md`](specs/non-goals.md) | Intentional exclusions and unsupported interpretations |
| [`specs/architecture.md`](specs/architecture.md) | High-level system architecture, components, trust boundaries, and design constraints |
| [`specs/governance-constraints.md`](specs/governance-constraints.md) | Governance, authority, multisig, upgrade, pause, treasury, and administrative constraints |
| [`specs/transparency-model.md`](specs/transparency-model.md) | Evidence, verification, disclosure, privacy, claims, review, and transparency requirements |
| [`specs/presale.md`](specs/presale.md) | Presale pricing, accounting, custody, finalization, claiming, refunds, and participant protections |

Only documents that currently exist in the repository form part of the current specification set.

Potential future specification areas are not considered implemented or committed functionality.

---

## Recommended Reading Order

For a complete first review:

1. [`specs/glossary.md`](specs/glossary.md)
2. [`specs/non-goals.md`](specs/non-goals.md)
3. [`specs/architecture.md`](specs/architecture.md)
4. [`specs/governance-constraints.md`](specs/governance-constraints.md)
5. [`specs/transparency-model.md`](specs/transparency-model.md)
6. [`specs/presale.md`](specs/presale.md)

The specification index in [`specs/README.md`](specs/README.md) explains how the documents relate to one another.

---

## Source of Authority

The files currently visible in the repository represent the working specification state.

They do not automatically constitute the authoritative specification for a future production implementation.

A production implementation should identify:

- an applicable versioned specification release;
- an applicable source-code release or commit;
- the intended network;
- authenticated contract addresses;
- authenticated wallet addresses;
- deployment records;
- administrative and governance authority;
- upgradeability;
- pause authority;
- audit or review status;
- and known deviations.

Versioned releases should govern production implementations rather than the continuously changing `main` branch.

---

## Actual Execution and Specification Conformance

The following distinction applies throughout the repository.

### Actual execution

Deployed contract code and authenticated on-chain state determine what technically executed.

### Intended behavior

The applicable versioned specification defines what the implementation was intended and approved to do.

### Conformance

An implementation conforms only where actual behavior satisfies the applicable normative requirements.

### Deviation

A difference between actual behavior and specified behavior is a deviation, defect, incident, governance violation, or version mismatch.

A user interface, informal statement, marketing claim, or later documentation change does not override actual on-chain execution.

Actual execution also does not automatically make non-conforming behavior acceptable.

---

## Public Communication

Public statements about GFC must distinguish between:

- planned;
- specified;
- implemented;
- tested;
- reviewed;
- audited;
- deployed;
- active;
- operational;
- and independently verified.

Public communication must not imply that:

- a Draft specification is completed functionality;
- a published wallet address proves compliant fund use;
- a transaction proves impact;
- a cryptographic commitment proves factual truth;
- a multisig automatically proves decentralization;
- an external review automatically qualifies as independent;
- or a code review automatically qualifies as an audit.

---

## Change Process

Material specification changes should be submitted through dedicated branches and pull requests.

Changes should identify:

- affected document;
- change category;
- rationale;
- affected requirements;
- security implications;
- governance implications;
- participant-rights implications;
- implementation implications;
- migration implications where relevant;
- and whether public communication must also change.

Large normative changes should remain isolated from unrelated edits.

Breaking changes require explicit versioning and impact documentation.

---

## Security

Security issues relating to the specifications, repository, future contracts, wallets, interfaces, infrastructure, or evidence systems should be handled according to [`SECURITY.md`](SECURITY.md).

Sensitive vulnerabilities should not be disclosed through public issues where premature disclosure could place users, participant funds, infrastructure, or future deployments at risk.

This repository must never contain:

- private keys;
- seed phrases;
- credentials;
- signing secrets;
- unredacted personal data;
- or production secrets.

---

## Change History

Repository-level changes are documented in [`CHANGELOG.md`](CHANGELOG.md).

Git history provides technical revision history.

Git history alone should not be treated as a complete replacement for:

- versioned releases;
- migration records;
- known-deviation records;
- implementation mappings;
- or formal deprecation notices.

---

## Contribution Philosophy

Contributions should preserve the following priorities:

- specifications before implementations;
- explicit authority before implied authority;
- constraints before discretion;
- participant rights before operational convenience;
- evidence before claims;
- privacy-aware transparency;
- accuracy before promotional strength;
- and clarity before speed.

The formal contribution and Stable-approval process remains under development.

Until that process is finalized, normative changes should be reviewed through pull requests and kept separate from unrelated repository changes.

---

## Repository Boundaries

This repository is intended for:

- formal specifications;
- architecture documentation;
- governance constraints;
- presale requirements;
- transparency and evidence requirements;
- terminology;
- security reporting guidance;
- and version history.

It is not intended for:

- social-media content;
- promotional campaign copy;
- hype-driven messaging;
- price predictions;
- guaranteed-return claims;
- undocumented roadmap promises;
- private operational information;
- credentials;
- personal beneficiary information;
- or unsupported legal representations.

---

## Naming

The current project name is:

**Global Foundation Coin**

The abbreviation is:

**GFC**

The historical name `German Foundation Coin` is deprecated and should not be used in current specifications or current public technical documentation except where necessary for accurate archival context.

The continued presence of the historical name in Git history, old domains, email addresses, or archived materials does not make it the current project identity.

---

## License

No `LICENSE` file is currently included in this repository.

The presence of publicly accessible repository content should not be interpreted as granting rights beyond those provided by applicable law or an explicitly published license.

Licensing must be defined before implementation components are presented for external reuse, modification, or distribution.

---

## Final Principles

> Specified does not mean implemented.

> Implemented does not mean tested.

> Tested does not mean audited.

> Audited does not mean risk-free.

> Deployed does not mean conforming.

> Public does not automatically mean verified.

> A wallet address shows transactions, not purpose or impact.

> Transaction verification does not equal use-of-funds verification.

> Use-of-funds verification does not equal impact verification.

> Cryptographic integrity does not equal factual truth.

> Token ownership does not automatically create unrestricted governance authority.

> The project name does not establish legal or charitable status.

> The `main` branch is not automatically the production source of authority.

> Different claims require different evidence.

GFC is intended to make system behavior, authority, participant rights, fund flows, evidence, limitations, and historical changes more explicit and reviewable before production reliance.

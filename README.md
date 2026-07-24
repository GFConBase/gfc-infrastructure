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

| Property | Current Status |
|---|---|
| Project | Global Foundation Coin |
| Abbreviation | GFC |
| Repository stage | Specification development |
| Specification release | Unreleased |
| Implementation status | Pre-deployment |
| Intended network | Base Mainnet |
| Chain ID | 8453 |

No production GFC token, presale, treasury, staking system, governance infrastructure, official production contract address, or official production wallet address is currently represented by this repository as operational.

The existence of a specification does not mean that the described component has been:

- implemented;
- tested;
- independently reviewed;
- audited;
- deployed;
- activated;
- or made available to users.

See [`STATUS.md`](STATUS.md) for the current implementation and deployment status.

---

## Repository Purpose

The purpose of this repository is to provide a clear, reviewable, and historically accountable reference for the intended GFC infrastructure.

It documents:

- what the system is intended to do;
- what the system must not do;
- how material authority is constrained;
- how participant funds and rights are intended to be protected;
- how token supply and allocations are intended to be controlled;
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

## Core Principles

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

Specifications and status records must not be changed after an event merely to make unauthorized or non-conforming behavior appear compliant.

---

## Intended System Model

The planned GFC infrastructure is organized across three related but distinct layers.

### Technology

The Technology layer addresses what technically executed.

It may include:

- the GFC token;
- token allocation contracts;
- presale contracts;
- lock and vesting contracts;
- treasury and custody mechanisms;
- staking infrastructure;
- governance execution contracts;
- public transaction records;
- and cryptographic evidence commitments.

See [`specs/architecture.md`](specs/architecture.md), [`specs/token.md`](specs/token.md), and [`specs/allocations.md`](specs/allocations.md).

### Governance

The Governance layer defines who was authorized to act and under which rules.

It addresses:

- authority;
- approvals;
- signer structures;
- timelocks;
- upgrades;
- pauses;
- migrations;
- emergency powers;
- conflicts of interest;
- and responsibility boundaries.

See [`specs/governance-constraints.md`](specs/governance-constraints.md).

### Impact and Evidence

The Impact and Evidence layer addresses what can be supported beyond technical transaction execution.

It includes:

- intended use of funds;
- supporting documentation;
- evidence provenance;
- reconciliation;
- outputs;
- outcomes;
- impact methodology;
- uncertainty;
- corrections;
- and disputes.

See [`specs/transparency-model.md`](specs/transparency-model.md).

No single layer is sufficient by itself.

---

## Verification Model

GFC distinguishes between three separate questions:

1. **Transaction:** Did the funds move as stated?
2. **Use:** Were the funds used for the documented purpose?
3. **Impact:** Did the documented use create a meaningful result?

These questions require different forms of evidence.

> Transaction verification does not equal impact verification.

The transparency model distinguishes between:

- public on-chain evidence;
- cryptographically anchored evidence;
- and protected off-chain evidence.

Cryptographic integrity may support record integrity or existence.

It does not independently prove that the underlying information is factually correct.

See [`specs/transparency-model.md`](specs/transparency-model.md).

---

## Formal Specification Set

The formal specification set is located in [`specs/`](specs/).

| Document | Primary Responsibility |
|---|---|
| [`specs/README.md`](specs/README.md) | Specification index, maturity, authority, reading order, and release model |
| [`specs/glossary.md`](specs/glossary.md) | Shared terminology |
| [`specs/non-goals.md`](specs/non-goals.md) | Intentional exclusions and unsupported interpretations |
| [`specs/architecture.md`](specs/architecture.md) | System architecture, components, trust boundaries, and design constraints |
| [`specs/token.md`](specs/token.md) | Token identity, supply, inflation, fees, and token-level authority |
| [`specs/allocations.md`](specs/allocations.md) | Allocation amounts, locks, vesting, custody, and allocation integrity |
| [`specs/governance-constraints.md`](specs/governance-constraints.md) | Governance, authority, multisig, upgrades, pauses, treasury, and administrative constraints |
| [`specs/transparency-model.md`](specs/transparency-model.md) | Evidence, verification, disclosure, privacy, review, and transparency requirements |
| [`specs/presale.md`](specs/presale.md) | Presale pricing, accounting, custody, finalization, claiming, refunds, and participant protections |

Only documents that currently exist in the repository form part of the current specification set.

Potential future specification areas are not considered implemented or committed functionality.

The recommended reading order and document relationships are maintained in [`specs/README.md`](specs/README.md).

---

## Token and Allocation Model

The current Draft token design specifies:

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

The intended supply allocation is:

| Allocation | Percentage |
|---|---:|
| Impact Vault | 25% |
| Guardian Growth Fund | 20% |
| Presale Allocation | 15% |
| Treasury Reserve | 15% |
| Liquidity Reserve | 15% |
| Ecosystem Growth Fund | 5% |
| Core Team | 5% |
| **Total** | **100%** |

Current intended long-term constraints include:

- a 50-year Impact Vault lock;
- 19-year linear Core Team vesting;
- no discretionary expansion beyond the fixed supply;
- and documented authority and custody requirements for material allocations.

These values describe the current intended design.

They do not represent deployed contracts, active allocations, funded production wallets, or completed technical enforcement.

See:

- [`specs/token.md`](specs/token.md);
- [`specs/allocations.md`](specs/allocations.md);
- and [`STATUS.md`](STATUS.md).

---

## Presale Status

The current Draft presale design is documented in [`specs/presale.md`](specs/presale.md).

No GFC presale is currently live.

No public presale date is established through this repository.

A Draft presale specification does not mean that:

- a presale contract has been implemented;
- participant funds are being accepted;
- token claims are active;
- production custody exists;
- or refund infrastructure is operational.

Current presale implementation status is maintained in [`STATUS.md`](STATUS.md).

---

## Staking Status

A hybrid staking model may be considered in the future.

The staking design is not finalized.

This repository does not currently guarantee:

- that staking will launch;
- a particular annual percentage rate;
- a particular lock period;
- a particular reward duration;
- a particular governance right;
- or permanent reward availability.

Any future staking rewards must originate from tokens already included within the fixed supply unless the applicable specifications are formally changed through a versioned process.

Potential future functionality must not be represented as implemented or committed functionality.

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

Deployed contract code and authenticated on-chain state determine what technically executed.

The applicable versioned specification determines what the implementation was intended and approved to do.

An implementation conforms only where actual behavior satisfies the applicable normative requirements.

---

## Repository Documents

| Document | Purpose |
|---|---|
| [`STATUS.md`](STATUS.md) | Current implementation, deployment, and operational status |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Contribution, review, and specification-change process |
| [`SECURITY.md`](SECURITY.md) | Security reporting and sensitive-disclosure guidance |
| [`CHANGELOG.md`](CHANGELOG.md) | Repository-level change history |
| [`specs/README.md`](specs/README.md) | Formal specification index and release model |

---

## Contributions

Material changes should be submitted through dedicated branches and pull requests.

Normative changes should identify:

- rationale;
- affected requirements;
- security implications;
- governance implications;
- participant-rights implications;
- implementation implications;
- migration implications;
- and whether public communication must also change.

Large normative changes should remain isolated from unrelated edits.

Breaking changes require explicit versioning and impact documentation.

See [`CONTRIBUTING.md`](CONTRIBUTING.md).

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

Git history alone is not a complete replacement for:

- versioned releases;
- migration records;
- known-deviation records;
- implementation mappings;
- incident records;
- or formal deprecation notices.

---

## Repository Boundaries

This repository is intended for:

- formal specifications;
- architecture documentation;
- governance constraints;
- token and allocation requirements;
- presale requirements;
- transparency and evidence requirements;
- terminology;
- security reporting guidance;
- contribution guidance;
- implementation-status records;
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

The historical name `German Foundation Coin` is deprecated.

It should not be used in current specifications or current public technical documentation except where necessary for accurate archival context.

Its continued presence in Git history, historical domains, historical email addresses, or archived materials does not make it the current project identity.

The name Global Foundation Coin does not independently establish:

- a legal foundation;
- nonprofit status;
- charitable status;
- tax-exempt status;
- government approval;
- regulatory approval;
- or any specific legal form.

---

## License

No `LICENSE` file is currently included in this repository.

No license has currently been granted for reuse, modification, or distribution beyond rights provided by applicable law or an explicitly published license.

Licensing must be defined before implementation components are presented for external reuse, modification, or distribution.

---

## Core Distinctions

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

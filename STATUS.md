# GFC Project Status

This document provides the current implementation, deployment, and operational status of the Global Foundation Coin (GFC) infrastructure.

It is an informative status record.

It does not independently define normative technical, governance, presale, allocation, or transparency requirements.

---

## Document Status

| Property | Current Status |
|---|---|
| Document role | Informative |
| Repository stage | Specification development |
| Specification release | Unreleased |
| Implementation status | Pre-deployment |
| Production release | None |
| Intended network | Base Mainnet |
| Chain ID | 8453 |

The current Git history records when this document was last modified.

A more recent commit or versioned release may supersede the information stated here.

---

## Current Project Status

The project is currently focused on:

- architecture development;
- specification development;
- governance-boundary definition;
- participant-protection requirements;
- token and allocation design;
- presale requirements;
- transparency and evidence requirements;
- and preparation for future implementation review.

The repository does not currently represent a complete production implementation.

---

## Current Implementation Status

At the current repository state:

- no production GFC token contract is represented as deployed;
- no GFC presale is live;
- no public presale date has been established through this repository;
- no production contract address is established as official;
- no production wallet address is established as official;
- no staking system is represented as operational;
- no production treasury infrastructure is represented as active;
- no production governance infrastructure is represented as active;
- no complete transparency platform is represented as deployed;
- no complete impact-verification platform is represented as deployed;
- no production specification release has been designated;
- and all Draft specifications remain subject to review and versioned revision.

The existence of source code, a wallet, a contract draft, a test deployment, or a specification does not independently change this status.

---

## Current Production References

| Component | Current Production Status |
|---|---|
| GFC token contract | Not established |
| Presale contract | Not established |
| Allocation contracts | Not established |
| Impact Vault contract | Not established |
| Core Team vesting contract | Not established |
| Treasury infrastructure | Not established |
| Liquidity infrastructure | Not established |
| Governance contracts | Not established |
| Governance multisig | Not established as official |
| Production wallets | Not established as official |
| Staking contracts | Not established |
| Transparency platform | Not deployed |
| Impact-verification platform | Not deployed |
| Production source-code release | None |
| Production specification release | None |
| Independent security audit | None represented |
| Production deployment record | None |

`Not established` means that this repository does not currently authenticate a production component as official.

It does not necessarily mean that no experimental, development, internal, or test component exists.

---

## Specification Status

The repository contains Draft specifications.

A Draft specification:

- may define normative requirements;
- may change materially;
- may contain unresolved implementation questions;
- does not prove implementation;
- does not prove testing;
- does not prove external review;
- does not prove audit completion;
- does not prove deployment;
- and does not prove operational availability.

Specification maturity and specification authority are defined separately in [`specs/README.md`](specs/README.md).

---

## Status Terminology

Public and repository-level statements should distinguish between the following states.

### Planned

A component or behavior is being considered or intended.

### Specified

Requirements or intended behavior have been documented.

### Implemented

Relevant source code or operational processes have been created.

### Tested

Defined tests have been performed against an implementation.

### Reviewed

An implementation or specification has undergone an identified review process.

### Audited

A specifically scoped audit has been completed by an identified auditor.

### Deployed

A component has been deployed to an identified environment or network.

### Active

A deployed component has been intentionally activated.

### Operational

A component is available for its stated production function and is being operated accordingly.

### Independently verified

An appropriately independent party has verified a specifically defined claim, component, record, or process.

These states are not interchangeable.

The strongest status claimed must not exceed the strongest status supported by available evidence.

---

## Production Authority Requirements

A future production implementation should identify at minimum:

- the applicable versioned specification release;
- the applicable source-code release or commit;
- the production network;
- authenticated contract addresses;
- authenticated wallet addresses;
- deployment transactions;
- allocation and custody addresses;
- governance authority;
- signer structures;
- upgrade authority;
- pause authority;
- migration authority;
- fee authority;
- treasury authority;
- audit or review status;
- known limitations;
- and known deviations from the applicable specification.

The continuously changing `main` branch must not automatically be treated as the production source of authority.

---

## Deployment Record Requirements

When production components are established, this document should be updated with a versioned deployment record containing:

| Field | Required Information |
|---|---|
| Component | Name and function |
| Environment | Production, testnet, staging, or other |
| Network | Network name and chain ID |
| Address | Authenticated contract or wallet address |
| Deployment transaction | Transaction hash where applicable |
| Source-code reference | Release, tag, or commit |
| Specification reference | Applicable versioned specification |
| Upgradeability | Immutable, upgradeable, migratable, or other |
| Administrative authority | Relevant roles and addresses |
| Pause authority | Whether a pause mechanism exists |
| Audit status | Auditor, scope, date, and report reference |
| Known deviations | Documented differences from specification |
| Activation status | Deployed, active, or operational |
| Verification date | Date the record was last verified |

A deployment record must distinguish authenticated production components from:

- development contracts;
- test deployments;
- deprecated deployments;
- unofficial copies;
- unauthenticated addresses;
- and third-party representations.

---

## Status Update Requirements

This document should be updated when a material status change occurs, including:

- designation of a specification release;
- designation of a source-code release;
- contract deployment;
- contract activation;
- presale activation or completion;
- official wallet designation;
- governance activation;
- treasury activation;
- staking activation;
- completion of an external review or audit;
- discovery of a material deviation;
- migration;
- deprecation;
- suspension;
- or termination of a production component.

Historical status statements should remain reviewable through Git history and versioned releases.

Status records must not be retrospectively altered merely to make earlier non-conforming behavior appear compliant.

---

## Related Documents

- [`README.md`](README.md)
- [`specs/README.md`](specs/README.md)
- [`SECURITY.md`](SECURITY.md)
- [`CHANGELOG.md`](CHANGELOG.md)

Where this document conflicts with an applicable versioned production release, the authenticated production release and its associated deployment records govern the production status.

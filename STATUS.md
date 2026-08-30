# GFC Project Status

This document provides the current implementation, deployment, and operational status of the Global Foundation Coin (GFC) infrastructure.

It is an informative status record.

It does not independently define normative technical, governance, token, presale, allocation, staking, security, or transparency requirements.

---

## Document Status

| Property | Current Status |
|---|---|
| Document role | Informative |
| Repository stage | Pre-mainnet specification and pilot development |
| Specification release | Draft / unreleased |
| Primary product focus | GFC Token / Economic Layer |
| Production implementation | Not deployed |
| Production release | None |
| Public onchain pilot | Base Sepolia |
| Pilot chain ID | 84532 |
| Intended production network | Base Mainnet |
| Production chain ID | 8453 |
| Mainnet GFC token | Not deployed |
| Presale | Not live |

The current Git history records when this document was last modified.

A later commit or versioned release may supersede information stated here.

---

## Current Project Status

GFC is currently in a pre-mainnet development phase.

The primary product focus is the **GFC Token / Economic Layer** and the technical, economic, governance, security, transparency, and operational requirements necessary to prepare it for later production readiness.

Current work therefore includes:

- token architecture and behavior;
- allocation design;
- vesting and unlock constraints;
- economic-flow design;
- staking design;
- presale requirements;
- governance boundaries and authority constraints;
- security-model development;
- participant-protection requirements;
- transparency and evidence requirements;
- specification development;
- implementation planning;
- testing preparation;
- and preparation for later external review and audit.

The broader long-term direction is an **Accountability Infrastructure** that connects:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

That broader system is not represented as fully implemented or production-deployed today.

The repository does not currently represent a complete production implementation.

---

## Public Pilot Status

A public GFC pilot exists on **Base Sepolia**.

| Property | Pilot Status |
|---|---|
| Environment | Public testnet pilot |
| Network | Base Sepolia |
| Chain ID | 84532 |
| Token | tGFC |
| Contract address | `0x7262Cca91938ede6bB6560F81104Aa410848e7f3` |
| Contract verification | Verified |
| Production status | Not production |
| Mainnet authority | None |
| Presale status | Not a presale |

The Base Sepolia pilot is evidence of early technical execution only.

It must not be represented as:

- the production GFC token;
- a Base Mainnet deployment;
- a live presale;
- a production allocation system;
- a production staking system;
- a production treasury system;
- a production governance system;
- or proof that future production contracts will use identical code, addresses, parameters, or authority structures.

Future Mainnet components require separate implementation, testing, review, deployment, authentication, and status records.

---

## Current Production Status

At the current repository state:

- no GFC token is deployed on Base Mainnet as the official production GFC token;
- no GFC presale is live;
- no public presale launch date is designated by this repository;
- no production GFC token contract address is established as official;
- no production presale contract address is established as official;
- no production allocation contracts are established as official;
- no production Impact Vault contract is established as official;
- no production Core Team vesting contract is established as official;
- no production staking system is operational;
- no production treasury infrastructure is active;
- no production liquidity infrastructure is established as official;
- no production governance contracts are active;
- no production governance multisig is established as official;
- no production wallet addresses are established as official through this repository;
- no production Transparency Registry or broader accountability infrastructure is represented as fully deployed;
- no complete production impact-verification system is represented as deployed;
- no production source-code release has been designated;
- no production specification release has been designated;
- no independent production security audit is represented as completed;
- and no production deployment record has been designated.

Draft specifications remain subject to review and versioned revision.

The existence of source code, wallet addresses, contract drafts, specifications, development artifacts, test deployments, or pilot deployments does not independently establish production status.

---

## Current Production References

| Component | Current Production Status |
|---|---|
| GFC token contract | Not deployed |
| Presale contract | Not deployed |
| Allocation contracts | Not deployed |
| Impact Vault contract | Not deployed |
| Core Team vesting contract | Not deployed |
| Treasury infrastructure | Not active |
| Liquidity infrastructure | Not established as production |
| Governance contracts | Not deployed |
| Governance multisig | Not established as official |
| Production wallets | Not established as official |
| Staking contracts | Not deployed |
| Production Transparency Registry | Not deployed |
| Broader accountability infrastructure | Not deployed |
| Production impact-verification system | Not deployed |
| Production source-code release | None |
| Production specification release | None |
| Independent production security audit | None represented |
| Production deployment record | None |

`Not deployed`, `not active`, and `not established as official` are deliberately distinct.

For example, a development wallet or testnet contract may exist without being an authenticated production component.

---

## Specification Status

The repository contains Draft specifications.

A Draft specification:

- may define normative requirements;
- may describe intended production behavior;
- may contain proposed architecture or parameters;
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

Public and repository-level statements must distinguish the status of a component, requirement, or system accurately.

### Draft

A document, design, requirement, parameter, or specification is under development and remains subject to revision.

### Proposed

A design, parameter, behavior, or decision has been put forward but has not necessarily been finally adopted or implemented.

### Planned

A component, activity, or behavior is intended for future work but is not represented as implemented merely because it appears in a plan or roadmap.

### Specified

Requirements or intended behavior have been documented.

Specification does not imply implementation.

### Implemented

Relevant source code or operational processes have been created.

Implementation does not imply testing, deployment, activation, or production readiness.

### Tested

Defined tests have been performed against an identified implementation and environment.

Testing does not imply production deployment.

### Pilot

A limited implementation or deployment exists for experimentation, validation, demonstration, or learning.

A pilot must identify its environment and must not be presented as production unless separately designated as such.

### Reviewed

An implementation or specification has undergone an identified review process.

### Audited

A specifically scoped audit has been completed by an identified auditor.

The term `audited` must not be used without identifying the relevant scope and audit evidence.

### Deployed

A component has been deployed to an identified environment or network.

Deployment alone does not imply that the component is active, operational, audited, or production-authoritative.

### Live

A component is currently available in its explicitly stated environment.

`Live` must never be used without sufficient context where it could create ambiguity between testnet, pilot, staging, and production availability.

### Active

A deployed component has been intentionally activated for its stated role.

### Operational

A component is available for its stated function and is being operated accordingly.

### Independently Verified

An appropriately independent party has verified a specifically defined claim, component, record, or process.

### Not Deployed

No authenticated deployment for the stated environment or production role is represented by the repository.

This does not necessarily mean that no draft, implementation, development deployment, test deployment, or pilot exists.

These states are not interchangeable.

The strongest status claimed must not exceed the strongest status supported by available evidence.

---

## Production Authority Requirements

A future production status record should identify at minimum:

- the applicable versioned specification release;
- the applicable source-code release, tag, or commit;
- the production network and chain ID;
- authenticated contract addresses;
- authenticated wallet addresses;
- relevant deployment transactions;
- allocation and custody addresses;
- governance authority;
- signer structures;
- upgrade authority;
- pause authority;
- migration authority;
- fee authority;
- treasury authority;
- applicable audit or review status;
- known limitations;
- known deviations from the applicable specification;
- activation status;
- and the evidence used to authenticate those claims.

The continuously changing `main` branch must not automatically be treated as the production source of authority.

Production authority must be tied to identifiable, versioned, and reviewable records.

---

## Deployment Record Requirements

Production and pilot deployments must remain clearly distinguishable.

A deployment record should identify:

| Field | Required Information |
|---|---|
| Component | Name and function |
| Environment | Production, testnet, pilot, staging, development, or other |
| Network | Network name and chain ID |
| Address | Authenticated contract or wallet address |
| Deployment transaction | Transaction hash where applicable |
| Source-code reference | Release, tag, or commit where available |
| Specification reference | Applicable versioned specification where available |
| Upgradeability | Immutable, upgradeable, migratable, or other |
| Administrative authority | Relevant roles and addresses |
| Pause authority | Whether a pause mechanism exists |
| Audit or review status | Scope, reviewer or auditor, date, and reference where applicable |
| Known deviations | Documented differences from the applicable specification |
| Activation status | Deployed, live, active, operational, deprecated, or other |
| Verification status | Applicable source-code or deployment verification |
| Record verification | Date or commit at which the record was last checked |

Deployment records must distinguish authenticated components from:

- development contracts;
- test deployments;
- pilot deployments;
- staging deployments;
- deprecated deployments;
- unofficial copies;
- unauthenticated addresses;
- and third-party representations.

A testnet or pilot deployment must never acquire production authority merely through age, public availability, usage, or continued operation.

---

## Status Update Requirements

This document should be updated when a material status change occurs, including:

- designation of a specification release;
- designation of a source-code release;
- new pilot or testnet deployment;
- production contract deployment;
- production contract activation;
- presale activation, suspension, completion, or cancellation;
- official wallet designation;
- governance activation;
- treasury activation;
- liquidity-system activation;
- staking activation;
- completion of an identified external review or audit;
- discovery of a material deviation;
- migration;
- deprecation;
- suspension;
- or termination of a component.

Historical status statements should remain reviewable through Git history and versioned releases.

Status records must not be retrospectively altered merely to make earlier behavior appear compliant with requirements adopted later.

---

## Related Documents

- [`README.md`](README.md)
- [`specs/README.md`](specs/README.md)
- [`SECURITY.md`](SECURITY.md)
- [`CHANGELOG.md`](CHANGELOG.md)

Normative technical, economic, governance, security, and transparency requirements belong in the applicable specifications rather than in this status document.

Where this document conflicts with an authenticated versioned production release and its associated deployment records, the authenticated production records govern production status.
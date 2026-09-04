# Global Foundation Coin Changelog

**Document ID:** GFC-CHG-001  
**Maturity:** Draft  
**Authority:** Informative  
**Version:** Unreleased  
**Implementation Status:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Last Updated:** 2026-09-04

---

## About This Changelog

All notable changes to the Global Foundation Coin (GFC) repository should be documented in this file.

This changelog covers changes to:

- specifications;
- architecture documentation;
- token and allocation requirements;
- vesting and unlock requirements;
- economic-flow requirements;
- staking requirements;
- presale requirements;
- authority and governance constraints;
- security policy and security model;
- transparency and evidence models;
- deployment records;
- project status;
- roadmap records;
- project decision records;
- contribution guidance;
- repository-level documentation;
- and future implementation or deployment records.

The repository currently remains in:

**Pre-mainnet specification and pilot development**

No changelog entry independently proves that a described component has been:

- implemented;
- tested;
- reviewed;
- audited;
- deployed;
- live;
- active;
- operational;
- or independently verified.

Actual current state is recorded in:

- [`STATUS.md`](STATUS.md)
- [`DEPLOYMENTS.md`](DEPLOYMENTS.md)

Current canonical project decisions are recorded in:

- [`DECISIONS.md`](DECISIONS.md)

---

## Change Categories

Changes may be grouped under the following categories.

### Added

New documents, requirements, definitions, controls, records, or functionality.

### Changed

Material revisions to existing documents, architecture, requirements, or processes.

### Corrected

Corrections of inaccurate, contradictory, incomplete, or outdated information.

### Deprecated

Documents, terms, mechanisms, or representations that should no longer be used for current implementation or communication.

### Removed

Content, requirements, or representations intentionally removed from the current specification set.

### Security

Security-related changes, reporting procedures, controls, mitigations, or incident information.

### Pending

Important matters that remain unresolved and must not be represented as finalized.

---

# [Unreleased]

## Added

### Current Product-Focus Model

Added the explicit current product-positioning model:

- **Primary current product:** GFC Token / Economic Layer
- **Long-term direction:** broader Accountability Infrastructure

Through the end of Q1 2027, work is intended to prioritize readiness of the Token / Economic Layer.

From Q2 2027 onward, the project intends to broaden emphasis toward the wider accountability system.

This distinction is now reflected across the repository.

---

### Canonical Accountability Model

Added and adopted the canonical GFC accountability model:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

This model now serves as the primary system-level accountability framing.

The prior three-layer model remains usable only as a supporting explanatory view.

---

### Full Specification Set

The formal specification set now includes:

- [`specs/README.md`](specs/README.md)
- [`specs/glossary.md`](specs/glossary.md)
- [`specs/non-goals.md`](specs/non-goals.md)
- [`specs/architecture.md`](specs/architecture.md)
- [`specs/roles-and-authority.md`](specs/roles-and-authority.md)
- [`specs/governance-constraints.md`](specs/governance-constraints.md)
- [`specs/security-model.md`](specs/security-model.md)
- [`specs/token.md`](specs/token.md)
- [`specs/allocations.md`](specs/allocations.md)
- [`specs/vesting-and-unlocks.md`](specs/vesting-and-unlocks.md)
- [`specs/economic-flows.md`](specs/economic-flows.md)
- [`specs/staking.md`](specs/staking.md)
- [`specs/presale.md`](specs/presale.md)
- [`specs/transparency-model.md`](specs/transparency-model.md)
- [`specs/conformance-verification.md`](specs/conformance-verification.md)

The specification set now covers the Token / Economic Layer and its supporting authority, security, governance, transparency, and conformance-verification constraints at substantially greater depth than the previous repository state.

---

### Conformance Verification Specification

Added [`specs/conformance-verification.md`](specs/conformance-verification.md).

The new specification defines the verification layer between normative requirements and the evidence used to evaluate those requirements.

It introduces explicit mappings from:

**requirement → observation → evidence → supported conclusion**

The model defines:

- claim-specific verification;
- observable evidence requirements;
- implementation-specific verification bindings;
- authenticated production binding requirements;
- evidence classes;
- evidence ceilings;
- state-read verification;
- event and transaction-history verification;
- source-code and bytecode review;
- proxy and upgrade-path review;
- authority verification;
- historical-state verification;
- negative observations;
- mixed on-chain and off-chain evidence;
- machine-readable result categories;
- and constraints for a future read-only conformance checker.

The specification explicitly separates specification-level verification requirements from production implementation bindings.

No undeployed Base Mainnet contract call, event, storage slot, address, role identifier, custody architecture, or ABI is invented merely to make a conformance requirement appear currently verifiable.

The current Base Sepolia pilot may be used to test verification concepts, but pilot observations do not constitute Base Mainnet production-conformance evidence.

---

### Roles and Authority Specification

Added [`specs/roles-and-authority.md`](specs/roles-and-authority.md).

The specification now distinguishes:

- role definition from role assignment;
- pilot authority from production authority;
- custody from approval;
- proposal from execution;
- upgrade authority;
- pause authority;
- migration authority;
- recovery authority;
- fee authority;
- presale authority;
- staking authority;
- treasury authority;
- liquidity authority;
- evidence authority;
- and publication authority.

No production authority assignment is established merely because a role is described.

---

### Technical Security Model

Added [`specs/security-model.md`](specs/security-model.md).

The technical security model now defines:

- protected assets;
- threat surfaces;
- fixed-supply invariants;
- allocation invariants;
- Impact Vault invariants;
- Core Team vesting invariants;
- presale refund-security requirements;
- staking non-inflationary requirements;
- governance and authority threats;
- upgrade and migration threats;
- frontend and authentication risks;
- evidence and Registry risks;
- incident expectations;
- and production-readiness security boundaries.

The repository-level [`SECURITY.md`](SECURITY.md) remains focused on reporting, disclosure, and repository-level security policy.

---

### Vesting and Unlock Specification

Added [`specs/vesting-and-unlocks.md`](specs/vesting-and-unlocks.md).

The new specification distinguishes:

- lock;
- vesting;
- vested;
- vested but unclaimed;
- claimed;
- released;
- migrated;
- and transferred.

It defines the current long-term constraints:

#### Impact Vault

```text
250,000,000 GFC
50-year intended lock
```

#### Core Team

```text
50,000,000 GFC
19-year intended linear vesting
```

Exact production start timestamps, cliffs, beneficiary structures, claim intervals, post-lock behavior, and final contract architecture remain unresolved.

---

### Economic Flows Specification

Added [`specs/economic-flows.md`](specs/economic-flows.md).

The specification now distinguishes:

- allocation;
- custody;
- transfer;
- release;
- vesting;
- claim;
- spending;
- contribution;
- refundable contribution;
- finalized proceeds;
- fee collection;
- fee use;
- treasury flow;
- liquidity deployment;
- staking principal;
- staking rewards;
- migration;
- and recovery.

It also establishes that internal transfers do not automatically constitute new external funding or expenditure.

---

### Staking Specification

Added [`specs/staking.md`](specs/staking.md).

The current staking direction is now explicitly documented as:

**Hybrid and Non-Inflationary**

The current model requires that staking:

- does not increase canonical GFC supply;
- uses an explicit reward source;
- does not guarantee APR or APY;
- preserves existing Impact Vault and Core Team restrictions;
- and does not automatically create unrestricted governance authority.

The final reward source remains unresolved.

---

### Deployment Registry

Added [`DEPLOYMENTS.md`](DEPLOYMENTS.md).

The deployment registry now records the public Base Sepolia pilot:

```text
Network: Base Sepolia
Chain ID: 84532
Token: tGFC
Contract: 0x7262Cca91938ede6bB6560F81104Aa410848e7f3
Public pilot date: 2026-08-02
Source status: Verified
Status: Public Pilot / Non-Production
```

The registry also explicitly records that no official Base Mainnet production deployment currently exists for:

- GFC token;
- Presale;
- Impact Vault;
- Guardian Growth;
- Treasury Reserve;
- Liquidity Reserve;
- Ecosystem;
- Core Team vesting;
- staking;
- governance;
- or a complete Transparency Registry.

Unknown pilot deployment details are not guessed or fabricated.

---

### Roadmap

Added [`ROADMAP.md`](ROADMAP.md).

The current public roadmap now distinguishes:

| Period | Primary Objective |
|---|---|
| Aug–Sep 2026 | Foundation Finalization |
| Q4 2026 | Production design, implementation, and testing |
| Q1 2027 | Mainnet and Presale readiness / potential Presale start |
| Q2 2027 | Broader production expansion and transparency build-out |
| H2 2027+ | Accountability Infrastructure expansion |
| Later, if justified | Dedicated execution-environment evaluation |

The roadmap intentionally does not publish a precise internal Presale planning date as a public launch commitment.

---

### Decision Register

Added [`DECISIONS.md`](DECISIONS.md).

The decision register now separates:

- Canonical Working Decisions;
- Constraints;
- Historical Facts;
- and Open Decisions.

It records the current canonical decisions for:

- project identity;
- product focus;
- accountability model;
- Base Mainnet production direction;
- fixed supply;
- allocations;
- Impact Vault;
- Core Team vesting;
- token fees;
- staking;
- Presale;
- governance;
- deployment authentication;
- and Transparency Registry philosophy.

It also explicitly identifies unresolved production decisions.

---

### Deployment Authentication Requirements

Added repository-wide requirements for future production deployment records.

Future production records should identify, where applicable:

- network;
- chain ID;
- authenticated address;
- deployment transaction;
- source commit;
- compiler/build information;
- constructor or initializer parameters;
- deployer;
- implementation/proxy structure;
- privileged roles;
- configuration;
- verification status;
- testing status;
- review or audit status;
- applicable specification version;
- known deviations;
- pause status;
- upgradeability;
- and migration status.

Unknown fields must remain unknown until authenticated.

---

### Versioned Transparency Registry Model

Expanded the Transparency Registry concept into a versioned historical accountability model.

The future Registry is now explicitly intended as:

**History, Not a Permanent Approval Badge**

Potential future status actions include:

- admission;
- verification;
- correction;
- downgrade;
- suspension;
- supersession;
- dispute;
- and removal from current presentation.

Registry inclusion does not automatically imply permanent:

- approval;
- verification;
- endorsement;
- compliance;
- or evidence validity.

---

### Registry Scope Direction

Added the future possibility that the Transparency Registry may include eligible:

- external projects;
- NGOs;
- organizations;
- companies;
- programs;
- or other initiatives.

Such scope remains future-oriented and does not represent a currently deployed production Registry.

---

### Repository Source-of-Truth Model

Added a clearer repository information hierarchy:

- normative requirements in `specs/`;
- current state in `STATUS.md`;
- deployment state in `DEPLOYMENTS.md`;
- project decisions in `DECISIONS.md`;
- future sequencing in `ROADMAP.md`;
- security reporting in `SECURITY.md`;
- contribution guidance in `CONTRIBUTING.md`;
- and change history in `CHANGELOG.md`.

The changing `main` branch is not automatically the production source of authority.

---

### Expanded Status Vocabulary

Expanded and aligned repository terminology to distinguish states including:

- Draft;
- Proposed;
- Planned;
- Specified;
- Implemented;
- Tested;
- Pilot;
- Reviewed;
- Audited;
- Deployed;
- Live;
- Active;
- Operational;
- Independently Verified;
- Not Deployed;
- Paused;
- Migrated;
- and Retired

where applicable.

These states are not interchangeable.

---

## Changed

### Repository Stage

Changed the repository-level implementation status from:

```text
Pre-deployment
```

to:

```text
Pre-mainnet specification and pilot development
```

This reflects the existence of the public Base Sepolia pilot while preserving the absence of Base Mainnet production deployments.

---

### README Positioning

Updated [`README.md`](README.md) so that the repository is no longer presented primarily as generic architecture/specification work.

The README now centers the current product focus:

**GFC Token / Economic Layer**

while preserving the long-term Accountability Infrastructure direction.

---

### Conformance Verification Integration

Integrated the new conformance-verification model across the relevant specification and deployment documentation.

The repository now requires applicable conformance claims to distinguish between:

- the normative source requirement;
- the verification method;
- the expected observation;
- the evidence class;
- the evidence ceiling;
- and the authenticated implementation-specific production binding where required.

The Token, Allocation, Vesting and Unlock, Governance, Presale, and Transparency conformance sections now link to the central verification model.

[`DEPLOYMENTS.md`](DEPLOYMENTS.md) now requires future production deployment records to identify the applicable conformance-verification mapping and authenticated implementation-specific bindings where relevant.

The root [`README.md`](README.md) now exposes the verification specification as part of the formal specification set and verification model.

---

### Architecture Model

Changed the repository's primary architecture/accountability framing from the previous three-layer system model to:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

The Technology / Governance / Evidence-and-Outcomes grouping remains only as a supporting explanatory view.

---

### Token Allocation Naming

Changed the canonical current allocation names.

The current names are:

- Impact Vault
- Guardian Growth
- Presale
- Treasury Reserve
- Liquidity Reserve
- Ecosystem
- Core Team

The older labels:

- `Guardian Growth Fund`;
- `Presale Allocation`;
- and `Ecosystem Growth Fund`

are no longer the preferred current names in normative specifications.

---

### Presale Token Delivery

Changed the current intended Presale model from:

**Deferred Claim after Successful Finalization**

to:

**Immediate GFC Distribution**

The previously added deferred-claim architecture is now superseded.

A valid purchase under the current design direction is intended to result in immediate GFC delivery as part of the purchase flow.

---

### Presale Payment Assets

Changed the Presale documentation from treating payment assets as entirely unspecified to the current intended support for:

- ETH;
- USDC;
- DAI

on Base.

Exact production asset identifiers, pricing architecture, and implementation details remain unresolved until authenticated before production activation.

---

### Presale Security Model

Changed Presale security analysis to reflect the current Immediate Distribution model.

The repository now explicitly identifies the unresolved interaction between:

- Immediate GFC Distribution; and
- failed-sale refund rights.

This issue is now treated as a **production activation blocker**.

No current specification authorizes an improvised:

- clawback;
- forced transfer;
- forced burn;
- mandatory participant return;
- token invalidation;
- blacklist-based immobilization;
- negative balance;
- or replacement-token mechanism.

---

### Presale State Model

Removed the assumption that a post-success `Claiming` state is part of the current Presale delivery model.

Successful finalization now resolves final sale status and contribution-proceeds rights rather than triggering initial delivery of purchased GFC.

---

### Presale Immutability Direction

Changed the Presale architecture from a blanket implementation claim to the current design direction that:

**material participant-facing sale logic should be immutable after production deployment**

The repository does not claim that a production immutable contract currently exists.

---

### Staking Position

Changed the staking documentation from:

```text
a hybrid staking model may be considered
```

to the current adopted Draft direction:

**Hybrid and Non-Inflationary**

The reward source remains unresolved.

---

### Transparency Registry

Changed the Transparency Registry concept from a generic verification surface into a historical, versioned accountability system.

The Registry now explicitly preserves the concept that:

- evidence can expire;
- rules can change;
- governance can change;
- claims can change;
- conflicts can emerge;
- and verification status can be downgraded, suspended, disputed, corrected, or superseded.

---

### Governance and Authority

Expanded governance documentation to distinguish:

- role definition from assignment;
- custody from approval;
- proposal from execution;
- technical authority from legal or organizational authority;
- pilot authority from production authority;
- and multisig signer count from actual signer independence.

No production signer set or governance structure is asserted.

---

### Contribution Workflow

Changed [`CONTRIBUTING.md`](CONTRIBUTING.md) so that dedicated branches and pull requests are:

**recommended**

rather than represented as an already adopted mandatory repository-governance process.

The repository does not currently claim a formal maintainer-vote or approval-threshold system.

---

### Security Policy Scope

Changed [`SECURITY.md`](SECURITY.md) so that it now:

- covers the full current specification set;
- recognizes the Base Sepolia pilot;
- separates repository/reporting policy from technical security modeling;
- reflects Immediate Distribution Presale risks;
- reflects hybrid non-inflationary staking;
- includes Registry-history and evidence-security concerns;
- and aligns status terminology with the current repository.

---

### Security Contact

Changed the current private security reporting address from:

```text
info@germanfoundationcoin.org
```

to:

```text
info@globalfoundationcoin.org
```

The historical domain is no longer the current security contact.

---

### Licensing Language

Changed README licensing language to state that no separate explicit open-source license is currently declared by the repository.

The updated language avoids implying that applicable law or platform terms create no rights whatsoever.

No separate repository `LICENSE` file is currently documented as part of the current repository state.

---

## Corrected

### Product Focus

Corrected repository language that made the broader infrastructure appear to be the current primary product.

The current primary product focus is the:

**GFC Token / Economic Layer**

---

### Pilot Visibility

Corrected repository language that implied the project was entirely pre-deployment with no public on-chain execution.

A public Base Sepolia pilot exists and is now explicitly recorded.

---

### Production Status

Corrected overly broad statements such as:

```text
This repository does not represent a live token deployment.
```

The accurate current distinction is:

- a public testnet pilot exists;
- no official Base Mainnet production GFC token exists.

---

### Presale Deferred Claim

Corrected the now-outdated deferred-claim Presale model.

Current specifications use:

**Immediate Distribution**

---

### Presale Claim Terminology

Corrected references to:

- post-finalization token entitlement;
- claim phase;
- token claims as initial delivery;
- and no instant distribution.

These are no longer current design assumptions.

---

### Presale Payment Assets

Corrected the prior position that ETH, USDC, and DAI were not part of the intended design.

They are now the current intended payment assets on Base.

Their exact production contract identifiers and pricing implementation remain unresolved.

---

### Presale Refund Invariant

Corrected the previous invariant:

```text
A contribution cannot be both successfully refunded and used to claim GFC.
```

because the current Presale model does not use deferred claiming.

The current security requirement is broader:

Immediate GFC Distribution and failed-sale refunds must be reconciled through a finalized, participant-disclosed production mechanism before activation.

---

### Staking Status

Corrected the statement that staking was merely a possible future concept.

Hybrid non-inflationary staking is now the current Draft design direction.

No production staking system is operational.

---

### Allocation Terminology

Corrected:

- `Guardian Growth Fund` → `Guardian Growth`
- `Presale Allocation` → `Presale`
- `Ecosystem Growth Fund` → `Ecosystem`

where used as canonical current allocation names.

---

### Three-Layer Architecture

Corrected presentation of the Technology / Governance / Impact-and-Evidence model as the primary architecture model.

It is now a supporting conceptual view only.

---

### Security Architecture Duplication

Corrected repository structure so that:

- [`SECURITY.md`](SECURITY.md) owns vulnerability reporting and disclosure policy;
- [`specs/security-model.md`](specs/security-model.md) owns technical threat-model and security requirements.

---

### Main Branch Authority

Reinforced that the current `main` branch is not automatically the production specification or source release.

Production deployments must identify exact applicable releases and deployment records.

---

### Stable and Production Claims

Corrected any implication that a Draft specification becomes Stable, production-ready, deployed, or audited merely because it is merged into the repository.

---

### Transparency Verification

Corrected use of broad verification language.

Current terminology requires scope-specific distinctions among:

- transaction verification;
- authority verification;
- rule verification;
- use-of-funds verification;
- outcome verification;
- impact evaluation;
- source verification;
- review;
- independent review;
- and audit.

---

## Deprecated

### German Foundation Coin as Current Identity

Deprecated `German Foundation Coin` as the current project identity.

The term may remain for accurate archival context.

---

### Deferred Presale Claiming

Deprecated Deferred Claim as the current intended Presale delivery model.

The current Draft model uses Immediate Distribution.

---

### Claim Phase as Initial Token Delivery

Deprecated the assumption that participants first receive GFC through a post-success Claim phase.

---

### Three-Layer Model as Primary Architecture

Deprecated use of the three-layer model as the primary top-level accountability model.

The canonical model is now:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

---

### Guardian Growth Fund

Deprecated `Guardian Growth Fund` as the current canonical allocation label.

Current label:

**Guardian Growth**

---

### Presale Allocation as Canonical Allocation Name

Deprecated `Presale Allocation` as the canonical allocation-table label.

Current label:

**Presale**

The phrase may still be used descriptively when referring to the quantity reserved for Presale.

---

### Ecosystem Growth Fund

Deprecated `Ecosystem Growth Fund` as the current canonical allocation label.

Current label:

**Ecosystem**

---

### Pre-deployment as Complete Repository Status

Deprecated `Pre-deployment` as the repository-level status because a public Base Sepolia pilot now exists.

Current repository status:

**Pre-mainnet specification and pilot development**

---

### Historical Security Contact

Deprecated:

```text
info@germanfoundationcoin.org
```

as the current security-reporting address.

Current address:

```text
info@globalfoundationcoin.org
```

---

### Main Branch as Automatic Production Authority

The changing `main` branch remains deprecated as an automatic production source of authority.

---

### Permanent Verification Badge Interpretation

Deprecated any interpretation of future Transparency Registry inclusion as permanent verification, approval, or endorsement.

---

## Removed

Removed or superseded current claims that:

- the broader Accountability Infrastructure is already the primary current product;
- the project has no public on-chain pilot;
- Deferred Claim is the current Presale delivery mechanism;
- token distribution first occurs after successful finalization;
- ETH, USDC, and DAI are outside the current intended Presale design;
- hybrid staking is merely an optional vague future idea;
- the three-layer model is the canonical top-level architecture;
- Guardian Growth Fund is the current canonical allocation name;
- Ecosystem Growth Fund is the current canonical allocation name;
- the old security-domain email remains the current contact;
- a mandatory branch-and-pull-request workflow has already been formally adopted;
- or future Registry verification should be understood as permanent status.

No removed statement should be treated as current merely because it remains visible in historical Git revisions.

---

## Security

### Security Model Separation

Added a clear separation between:

- repository-level security reporting in [`SECURITY.md`](SECURITY.md); and
- technical system security in [`specs/security-model.md`](specs/security-model.md).

---

### Pilot Security

Added explicit security treatment for the Base Sepolia pilot.

Pilot source verification is recorded.

The pilot is not represented as:

- production security evidence;
- production audit evidence;
- production authority;
- or Base Mainnet readiness.

---

### Presale Production Blocker

Added the Immediate Distribution / Failed-Sale Refund interaction as a critical unresolved Presale security issue.

A production Presale must not activate until this interaction is fully defined and tested.

---

### Fixed-Supply Security

Expanded security requirements around the invariant:

```text
canonical GFC supply ≤ 1,000,000,000 GFC
```

Staking, migration, upgrades, rewards, or replacement mechanisms must not create hidden inflation.

---

### Impact Vault and Vesting Security

Added explicit protection of:

- 250,000,000 GFC Impact Vault / 50-year intended lock;
- 50,000,000 GFC Core Team / 19-year intended linear vesting.

Migration, recovery, upgrade, pause, governance, or emergency mechanisms must not silently weaken these restrictions.

---

### Staking Security

Added explicit requirements that:

- staking remain non-inflationary;
- reward funding be explicit;
- distributed rewards not exceed available authorized reward assets;
- participant principal be protected;
- and migration not duplicate principal or reward entitlement.

---

### Registry Security

Added security concerns for future Transparency Registry infrastructure, including:

- false status assignment;
- historical-record deletion;
- unauthorized downgrade or upgrade;
- reviewer impersonation;
- evidence substitution;
- protected-data exposure;
- and portal compromise.

---

### Security Contact

Current private reporting contact:

```text
info@globalfoundationcoin.org
```

No public bug-bounty program, formal legal safe harbor, guaranteed response deadline, or production support SLA is currently established.

---

## Pending

The following material matters remain unresolved and must not be represented as finalized.

### Specification and Release Governance

- first production-governing versioned specification release;
- final versioning format;
- Stable approval process;
- reviewer requirements;
- production implementation mapping;
- authenticated implementation-specific conformance-verification bindings;
- and release authentication.

### Token

- production token implementation architecture;
- supply-creation method;
- buy/sell classification;
- recognized-pool model;
- fee exemptions;
- final fee destination;
- final fee-proceeds use;
- burn behavior;
- pause behavior;
- recovery;
- upgradeability;
- migration;
- and production authority.

### Allocation and Custody

- production custody for each allocation;
- Guardian Growth mandate;
- Treasury Reserve detailed controls;
- Liquidity Reserve controls;
- Ecosystem distribution rules;
- multisig or equivalent structures;
- signers;
- thresholds;
- timelocks;
- recovery;
- and migration.

### Impact Vault

- production lock-start event;
- lock-start timestamp;
- time-calculation model;
- exact post-50-year behavior;
- release mechanics;
- production custody;
- upgradeability;
- recovery;
- and migration.

### Core Team Vesting

- production vesting-start event;
- vesting-start timestamp;
- cliff;
- claim/release interval;
- beneficiary structure;
- reassignment;
- succession;
- revocation;
- recovery;
- migration;
- and final implementation.

### Presale

- exact production USDC address;
- exact production DAI address;
- pricing source;
- oracle architecture if used;
- stale-price limits;
- rounding;
- contribution limits;
- participant eligibility;
- exact Immediate Distribution ordering;
- failed-sale treatment of already distributed GFC;
- exact refund mechanism;
- refund amount rule;
- contribution custody;
- successful-proceeds destination;
- withdrawal authority;
- unsold Presale GFC treatment;
- pause-duration behavior;
- cancellation;
- recovery;
- migration;
- and final immutable/configurable boundary.

### Staking

- principal-custody model;
- reward source;
- reward pool;
- reward rate;
- APR/APY methodology;
- reward duration;
- lock behavior;
- withdrawals;
- early exit;
- penalties;
- governance-related rights;
- community-related benefits;
- pause;
- recovery;
- migration;
- upgradeability;
- and production activation criteria.

### Governance

- final governance structure;
- multisig platform if any;
- signer count;
- signer identities or categories;
- approval thresholds;
- timelock durations;
- voting eligibility;
- voting weight;
- quorum;
- proposal threshold;
- veto;
- delegation;
- emergency process;
- and production authority assignments.

### Transparency Registry

- production Registry architecture;
- admission criteria;
- evidence schema;
- claim schema;
- status vocabulary;
- reviewer model;
- verification rules;
- downgrade criteria;
- suspension criteria;
- removal criteria;
- dispute handling;
- historical-retention mechanism;
- anchoring;
- protected evidence;
- privacy processes;
- and production Registry authority.

### Security

- final secure-reporting mechanism;
- encryption key or protected-transfer system;
- response targets;
- formal severity methodology;
- safe-harbor decision;
- bug-bounty decision;
- incident-response roles;
- emergency contacts;
- release signing;
- dependency monitoring;
- production monitoring;
- and independent production security-review scope.

### Licensing

- explicit repository license remains unresolved.

---

# [2026-01-05] — Historical / Superseded Documentation State

This section preserves the substance of the earlier repository documentation state for historical accountability.

At that time, documentation stated or implied that it had:

- published a final GFC Presale architecture;
- specified instant token distribution;
- documented soft-cap and refund behavior;
- confirmed a fixed Presale reference price of €0.05 per GFC;
- confirmed ETH, USDC, and DAI on Base as supported assets;
- and confirmed an immutable, non-proxy, non-upgradeable Presale design.

These statements must be interpreted as historical documentation state, not production evidence.

The repository later moved to a Deferred Claim Presale design.

The current Unreleased specification set has since changed again and now uses:

**Immediate GFC Distribution**

as the current Presale design direction.

Therefore, the historical fact that Immediate Distribution appeared in older documentation does not mean the old Presale architecture has been reinstated unchanged.

The current Immediate Distribution model is governed by the present specification set, including the unresolved failed-sale refund interaction and current security constraints.

### Historical elements still aligned with the current design

The following historical elements remain broadly aligned with the current Draft direction:

- €0.05 GFC reference price;
- Base as the intended initial production ecosystem;
- eight-week Presale direction;
- €250,000 soft-cap direction;
- failed-sale refund protection;
- ETH, USDC, and DAI as current intended payment assets;
- and Immediate Distribution as the current token-delivery direction.

### Historical elements not established as current production facts

The following must not be inferred from the old documentation:

- a final production Presale architecture;
- deployed Presale code;
- a production Presale address;
- live Presale availability;
- exact production asset addresses;
- exact production oracle behavior;
- a finalized failed-sale settlement mechanism;
- blanket immutable/non-proxy implementation;
- completed security review;
- or production deployment readiness.

The current specification set governs current design interpretation.

---

## Historical Interpretation

Historical changelog entries describe what the repository documented at a particular time.

They do not automatically remain:

- current;
- applicable;
- technically correct;
- production-ready;
- deployed;
- or authoritative for future implementations.

Where historical documentation conflicts with the current Unreleased specification set, the current specification state should identify the conflict explicitly.

Historical entries should not be silently deleted merely because the design changed.

A design may return to an earlier high-level direction while using materially different implementation requirements and constraints.

---

## Current Release Status

No production-governing specification release is currently recorded in this changelog.

No official Base Mainnet GFC token deployment is recorded.

No live production Presale is recorded.

No production Impact Vault is recorded.

No production Core Team vesting contract is recorded.

No production staking system is recorded.

No production governance system is recorded.

No complete production Transparency Registry is recorded.

No completed independent production security audit is recorded.

No Stable specification release is recorded.

A public Base Sepolia pilot is recorded separately in [`DEPLOYMENTS.md`](DEPLOYMENTS.md).

The current repository state remains:

- Draft;
- Unreleased;
- Normative where declared by individual specifications;
- and Pre-mainnet specification and pilot development.

---

## Final Changelog Principles

> A historical decision is not automatically a current decision.

> A current decision is not automatically a deployed implementation.

> A specification change is not an implementation change.

> A documented design is not automatically a deployed design.

> A Pilot deployment is not a Production deployment.

> Base Sepolia is not Base Mainnet.

> Source Verified does not mean Audited.

> A correction must not silently erase the previous claim.

> A previously deprecated design direction may later return under different constraints and must be documented as such.

> Superseded information must not be presented as current.

> Git history alone is not a complete release record.

> Material changes should remain reviewable.

> Public claims must reflect the applicable specification and actual implementation status.

> Open decisions must remain open until explicitly resolved.

> Different claims require different evidence.

The changelog exists to preserve the evolution of GFC without confusing historical documentation, current specification state, and actual production deployment.

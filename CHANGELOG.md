# Global Foundation Coin Changelog

**Document ID:** GFC-CHG-001  
**Maturity:** Draft  
**Authority:** Informative  
**Version:** Unreleased  
**Implementation Status:** Pre-deployment  
**Last Updated:** 2026-07-23

---

## About This Changelog

All notable changes to the Global Foundation Coin (GFC) repository are documented in this file.

This changelog covers changes to:

- specifications;
- architecture documentation;
- governance constraints;
- presale requirements;
- transparency and evidence models;
- terminology;
- security policy;
- repository-level documentation;
- and future implementation or deployment records.

The repository currently remains in a pre-deployment specification phase.

No entry in this changelog independently proves that a described component has been:

- implemented;
- tested;
- independently reviewed;
- audited;
- deployed;
- activated;
- or made available to users.

---

## Change Categories

Changes may be grouped under the following categories:

### Added

New documents, requirements, definitions, controls, or functionality.

### Changed

Material revisions to existing documents, architecture, requirements, or processes.

### Corrected

Corrections of inaccurate, contradictory, incomplete, or outdated information.

### Deprecated

Documents, terms, mechanisms, or representations that should no longer be used for new implementations or current communication.

### Removed

Content, requirements, or representations intentionally removed from the current specification set.

### Security

Security-related changes, reporting procedures, controls, mitigations, or incident information.

### Pending

Important matters that remain unresolved and must not be represented as finalized.

---

# [Unreleased]

## Added

### Specification Metadata Model

Added a consistent metadata model separating:

- document maturity;
- document authority;
- version;
- implementation status;
- intended network;
- chain ID;
- and last-updated date.

The current specification metadata model uses:

- `Maturity: Draft`;
- `Authority: Normative`;
- `Version: Unreleased`;
- `Implementation Status: Pre-deployment`.

`Normative` is no longer treated as a maturity level.

### Specification Release Model

Added requirements distinguishing:

- the continuously changing `main` branch;
- versioned specification releases;
- source-code releases;
- production deployments;
- authenticated contract addresses;
- audit or review status;
- and known deviations.

Future production implementations are expected to identify the applicable versioned specification release.

### Implementation Status Vocabulary

Added explicit distinctions between:

- planned;
- specified;
- implemented;
- tested;
- reviewed;
- audited;
- deployed;
- active;
- operational;
- migrated;
- deprecated;
- and retired.

### System Architecture

Added a three-layer system model consisting of:

1. Technology;
2. Governance;
3. Impact and Evidence.

The model clarifies that no single layer independently provides complete transparency or accountability.

### Transparency Verification Model

Added explicit distinctions between:

- transaction verification;
- use-of-funds verification;
- output verification;
- outcome evaluation;
- and impact evaluation.

The following principle is now foundational:

> TRANSACTION VERIFIED does not equal IMPACT VERIFIED.

### Evidence Disclosure Model

Added three evidence disclosure levels:

- Public On-Chain;
- Cryptographically Anchored;
- Protected Off-Chain.

Added the principle that cryptographic anchoring may support record integrity or existence but does not independently prove factual accuracy.

### Evidence and Claim Models

Added separate terminology and requirements for:

- evidence provenance;
- evidence status;
- claim category;
- claim status;
- review status;
- independent review;
- disputes;
- corrections;
- supersession;
- and historical integrity.

### Governance Constraints

Added detailed governance requirements covering:

- explicit authority;
- least privilege;
- separation of duties;
- multisig controls;
- signer management;
- timelocks;
- proposals;
- voting;
- delegation;
- conflicts of interest;
- treasury authority;
- fee authority;
- liquidity authority;
- presale authority;
- upgrade authority;
- pause authority;
- migration authority;
- emergency authority;
- evidence authority;
- and impact-claim authority.

### Authority Transparency

Added requirements for a future authority registry identifying:

- privileged roles;
- controlling addresses;
- permitted actions;
- approval thresholds;
- timelocks;
- upgrade authority;
- pause authority;
- migration authority;
- and role status.

### Token Model

Documented the current intended token model:

| Property | Intended Configuration |
|---|---|
| Project name | Global Foundation Coin |
| Symbol | GFC |
| Intended network | Base Mainnet |
| Chain ID | 8453 |
| Token standard | ERC-20 compatible |
| Decimals | 18 |
| Total supply | 1,000,000,000 GFC |
| Supply model | Fixed supply |
| Additional inflation | Not intended |
| Buy fee | 0% |
| Sell fee | 1% |

These values remain specified but not represented as deployed.

### Token Allocation Model

Documented the current intended allocation model:

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

### Long-Term Token Constraints

Added the current intended long-term constraints:

- 50-year Impact Vault lock;
- 19-year linear Core Team vesting;
- fixed token supply;
- no undocumented early-release path;
- no migration mechanism that silently weakens remaining restrictions;
- and disclosure of whether future implementations are immutable, configurable, upgradeable, or dependent on governance.

### Presale Specification

Added a substantially expanded presale specification covering:

- fixed reference pricing;
- purchase-time accounting;
- payment-asset conversion;
- allocation limits;
- presale states;
- contribution custody;
- successful finalization;
- failed finalization;
- token entitlement;
- token claiming;
- refunds;
- cancellation;
- pausing;
- withdrawal restrictions;
- unsold tokens;
- security invariants;
- monitoring;
- and participant protections.

### Presale Parameters

Documented the current intended presale parameters:

| Property | Intended Configuration |
|---|---|
| Reference price | €0.05 per GFC |
| Intended duration | 8 weeks |
| Soft cap | €250,000 |
| Presale Allocation | 150,000,000 GFC |
| Separate monetary hard cap | None currently intended |
| Maximum gross reference value | €7,500,000 at full allocation |
| Token delivery | Claim after successful finalization |
| Failed-sale protection | Participant refund |
| Project access to contributions | Only after successful finalization |

### Deferred Token Claiming

Added a deferred claim model.

Under the current intended architecture:

- a valid purchase creates a token entitlement;
- GFC is not transferred during the active presale;
- tokens become claimable only after successful finalization;
- and failed-sale refunds remain separate from successful-sale token claims.

### Contribution Protection

Added the requirement that participant contributions remain protected while refund rights remain active.

Reaching the soft cap before the presale end does not independently:

- end the presale;
- activate claims;
- remove refund protections;
- or make contributions available for project use.

### Non-Goals Specification

Added an expanded non-goals specification addressing:

- short-term speculation;
- guaranteed price;
- guaranteed returns;
- guaranteed liquidity;
- guaranteed listings;
- market manipulation;
- discretionary inflation;
- unrestricted governance;
- false decentralization;
- complete automation claims;
- unrestricted disclosure;
- impact guarantees;
- legal-status claims;
- presale guarantees;
- staking guarantees;
- undocumented feature promises;
- retrospective rule rewriting;
- and silent historical deletion.

### Glossary

Added a comprehensive glossary covering:

- project terminology;
- specification metadata;
- implementation status;
- blockchain terminology;
- token and allocation terminology;
- lock and vesting terminology;
- presale terminology;
- governance terminology;
- authority and custody terminology;
- transparency terminology;
- evidence and claim terminology;
- outcome and impact terminology;
- review and audit terminology;
- privacy and security terminology;
- release terminology;
- and legal-status terminology.

### Security Policy

Added an expanded security policy covering:

- private vulnerability reporting;
- specification-level vulnerabilities;
- repository security;
- future contract scope;
- supported-version handling;
- sensitive information;
- triage;
- severity classification;
- remediation;
- coordinated disclosure;
- repository integrity;
- release integrity;
- contract-address authentication;
- signer security;
- frontend security;
- backend security;
- oracle security;
- evidence security;
- privacy security;
- monitoring;
- backups;
- and requirements before Stable status.

### Repository Documentation

Added or expanded:

- root repository status information;
- specification index;
- recommended reading order;
- source-of-authority rules;
- release requirements;
- change classification;
- contribution expectations;
- public communication boundaries;
- repository scope;
- security reporting guidance;
- and licensing limitations.

---

## Changed

### Project Name

Changed the current project name from:

`German Foundation Coin`

to:

`Global Foundation Coin`

The abbreviation remains:

`GFC`

The historical name is retained only where required for accurate archival context.

### Architecture Status

Changed the architecture from being presented as final or Stable to:

- Draft;
- Normative;
- Unreleased;
- Pre-deployment.

### Specification Status Model

Replaced the former single-field status model.

The former model incorrectly treated the following as equivalent categories:

- Draft;
- Stable;
- Normative.

The current model separates:

- maturity;
- authority;
- version;
- and implementation status.

### Source of Authority

Changed the repository model so that the current `main` branch is no longer described as the automatic production “single source of truth.”

Future production authority is intended to depend on:

- a versioned specification release;
- a corresponding source-code version;
- authenticated deployment records;
- official contract addresses;
- review or audit status;
- and known deviations.

### Presale Token Delivery

Changed the intended presale model from instant token distribution to deferred claiming after successful finalization.

### Presale Fund Handling

Changed the presale custody model so that:

- participant funds remain protected during the active sale;
- reaching the soft cap does not permit immediate withdrawal;
- project access requires successful finalization;
- and failed-sale contributions remain refundable.

### Presale Success Definition

Changed the success model so that reaching the soft cap alone does not constitute completed success.

A successful presale requires:

- the presale to end;
- the applicable success conditions to be met;
- and successful finalization to occur.

### Supported Payment Assets

Changed the documentation so that no specific payment asset is represented as finalized until the applicable implementation and configuration are approved.

Any future supported payment asset must identify:

- network;
- contract address;
- decimals;
- valuation method;
- conversion source;
- stale-price protection;
- and applicable limits.

### Upgradeability Position

Changed the documentation from a blanket assumption of immutable and non-upgradeable contracts to a component-specific security and governance analysis.

Each future production component must disclose whether it is:

- immutable;
- configurable;
- upgradeable;
- proxied;
- migratable;
- pausable;
- or dependent on external authority.

### Transparency Model

Changed transparency from an on-chain-first reporting concept to a layered system combining:

- technology;
- governance;
- evidence;
- use-of-funds review;
- and impact evaluation.

### Public Communication Requirements

Changed repository guidance to require clear separation between:

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

---

## Corrected

### Outdated Project Identity

Corrected current references that identified GFC as `German Foundation Coin`.

Current documents now use `Global Foundation Coin`.

### False Finality

Corrected statements that described the presale architecture as final before implementation, review, audit, deployment, or activation.

### Instant Distribution

Corrected the previous presale description that specified instant token transfer at purchase time.

The current intended model uses post-finalization claiming.

### Payment Assets

Corrected the previous statement that ETH, USDC, and DAI were confirmed supported assets.

No payment asset is currently represented as finalized by this changelog.

### Contract Immutability

Corrected the previous blanket statement that the presale contract design was confirmed immutable and non-upgradeable.

Final upgradeability and migration rules remain subject to component-level specification, implementation, security review, and release documentation.

### Soft-Cap Interpretation

Corrected the assumption that reaching the soft cap automatically:

- completes the presale;
- removes refund rights;
- or allows project withdrawal.

### Frontend Pricing

Corrected the former implication that frontend conversion could sufficiently enforce presale pricing.

Material pricing and entitlement rules must be enforced through the contract or another verifiable settlement mechanism.

### Specification Precedence

Corrected the claim that written specifications automatically override actual deployed behavior.

Deployed code and authenticated on-chain state determine what technically executes.

The applicable versioned specification determines whether that execution conforms to the approved design.

### Multisig Terminology

Corrected the assumption that multiple multisig signers are automatically independent.

Signer count and signer independence are separate properties.

### Transparency Claims

Corrected the assumption that:

- wallet publication proves accountability;
- transaction verification proves use of funds;
- cryptographic anchoring proves truth;
- or on-chain visibility proves impact.

### Legal and Charitable Status

Corrected any implication that the project name, token, Impact Vault, or transparency model independently establishes:

- a legal foundation;
- charitable status;
- nonprofit status;
- tax-exempt status;
- regulatory approval;
- or tax deductibility.

### Security Contact

Changed the private security reporting contact to:

`info@germanfoundationcoin.org`

The mailbox must remain controlled, protected, monitored, and recoverable before being relied upon for production security reporting.

---

## Deprecated

### German Foundation Coin

Deprecated the former project name `German Foundation Coin`.

The term may remain in:

- Git history;
- archived documents;
- historical domain names;
- historical email addresses;
- or explicit historical references.

It should not be used as the current project identity.

### Instant Distribution

Deprecated instant token distribution as the intended GFC presale delivery model.

### Status: Normative

Deprecated the use of `Normative` as a document maturity status.

### Stable Pre-Implementation Claims

Deprecated the use of `Stable` for specifications that have not completed the required review and release process.

### Main Branch as Automatic Production Authority

Deprecated the assumption that the changing `main` branch automatically governs a future production deployment.

### Absolute Transparency Terminology

Deprecated unqualified claims such as:

- fully transparent;
- fully verified;
- completely decentralized;
- completely audited;
- trustless;
- risk-free;
- or guaranteed impact.

---

## Removed

Removed current claims that:

- the presale architecture is final;
- instant token distribution is the intended mechanism;
- ETH, USDC, and DAI are already confirmed payment assets;
- the presale contract is confirmed immutable;
- the presale contract is confirmed non-upgradeable;
- reaching the soft cap permits immediate fund withdrawal;
- the repository currently contains production infrastructure;
- the current specifications are already Stable;
- or the current `main` branch is automatically authoritative for production.

Removed promotional or overly absolute interpretations that exceeded the available implementation or evidence status.

---

## Security

Added requirements that:

- security-sensitive issues must initially be reported privately;
- public GitHub issues must not be used for exploitable vulnerabilities;
- specification defects may qualify as security vulnerabilities;
- sensitive information must be minimized;
- secret exposure must be treated as compromise;
- future releases must be authenticated;
- official contract addresses must be published through authenticated channels;
- privileged roles must remain reviewable;
- a verified contract must not be presented as audited;
- an audit must not be presented as a security guarantee;
- and planned security controls must not be presented as implemented controls.

The current private reporting contact is:

`info@germanfoundationcoin.org`

No public bug-bounty program, legal safe harbor, fixed response deadline, or production support guarantee is currently established.

---

## Pending

The following matters remain unresolved and must not be presented as finalized:

- first versioned specification release;
- specification versioning format;
- approval authority for Stable documents;
- reviewer requirements;
- production source-code implementation;
- production deployment addresses;
- token contract upgradeability;
- presale contract upgradeability;
- supported presale payment assets;
- conversion and oracle mechanism;
- rounding rules;
- minimum and maximum contribution rules;
- unsold presale token handling;
- final treasury custody model;
- final multisig thresholds;
- signer appointments;
- authority registry;
- Impact Vault implementation;
- Core Team vesting implementation;
- staking specification;
- evidence schema;
- evidence anchoring mechanism;
- protected evidence storage;
- impact methodology;
- transparency portal architecture;
- independent-review process;
- incident-response process;
- release-signing process;
- production monitoring;
- formal bug-bounty decision;
- legal safe-harbor decision;
- and repository licensing.

---

# [2026-01-05] – Superseded Documentation State

This section preserves the substance of the previous changelog entry for historical accountability.

The former documentation stated that it had:

- published the final GFC presale architecture;
- specified instant token distribution;
- documented soft-cap and refund behavior;
- confirmed a fixed presale price of €0.05 per GFC;
- confirmed ETH, USDC, and DAI on Base as supported assets;
- and confirmed an immutable, non-proxy, non-upgradeable contract design.

These statements are now superseded.

They MUST NOT be interpreted as current commitments, finalized implementation decisions, production configuration, or deployment evidence.

The following parts remain consistent with the current intended model:

- the €0.05 GFC reference price;
- use of Base as the intended initial network;
- the requirement for documented soft-cap behavior;
- and the requirement for failed-sale refund protection.

The following parts are no longer current:

- the former project name;
- the claim of a final presale architecture;
- instant token distribution;
- confirmed ETH, USDC, and DAI support;
- and the blanket immutable and non-upgradeable design claim.

The current Unreleased specifications replace those former design assumptions.

---

## Historical Interpretation

Historical changelog entries describe what the repository documented at a particular time.

They do not automatically remain:

- current;
- applicable;
- technically correct;
- production-ready;
- or authoritative for future implementations.

Where a historical entry conflicts with the current Unreleased specification set, the conflict must be resolved through:

- explicit correction;
- versioned release;
- implementation mapping;
- and known-deviation documentation.

Historical entries should not be silently deleted merely because the underlying design changed.

---

## Release Status

No production-governing specification release is currently recorded in this changelog.

No production token deployment is recorded.

No active presale is recorded.

No production contract address is recorded.

No completed security audit is recorded.

No Stable specification release is recorded.

The current repository state remains:

- Draft;
- Unreleased;
- Normative where declared by individual specifications;
- and Pre-deployment.

---

## Final Changelog Principles

> A historical decision is not automatically a current decision.

> A specification change is not an implementation change.

> A documented design is not automatically a deployed design.

> A deployed design is not automatically conforming.

> A correction must not silently erase the previous claim.

> Superseded information must not be presented as current.

> Git history alone is not a complete release record.

> Material changes must remain reviewable.

> Public claims must reflect the applicable specification and actual implementation status.

> Different claims require different evidence.

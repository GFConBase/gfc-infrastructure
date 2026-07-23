# Global Foundation Coin Specifications

**Document ID:** GFC-SPECS-INDEX  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-deployment  
**Intended Network:** Base Mainnet  
**Chain ID:** 8453  
**Last Updated:** 2026-07-23

---

## 1. Document Status

This directory contains the current formal specifications for the planned Global Foundation Coin infrastructure.

The specification set follows a specification-first development process.

Intended system behavior, authority boundaries, constraints, terminology, participant rights, verification requirements, and prohibited actions are documented before production implementation.

At the time of publication:

- no production GFC token contract is represented by this repository as deployed;
- no GFC presale is live;
- no production treasury, governance, staking, vesting, evidence, or transparency infrastructure is represented as operational;
- no production contract or wallet address is established as official by this directory;
- no public presale date is established by this directory;
- the specifications remain subject to review and material revision before their first versioned release;
- no production implementation is governed by these documents unless it explicitly identifies an applicable versioned specification release.

The presence of a specification does not mean that the described component has already been:

- implemented;
- tested;
- independently reviewed;
- audited;
- deployed;
- activated;
- or made available to users.

The continuously changing `main` branch MUST NOT automatically be treated as the authoritative specification governing a future production implementation.

---

## 2. Purpose

The purpose of this specification set is to establish a clear, reviewable, and versionable reference for the intended GFC infrastructure.

The specifications define:

- system components and boundaries;
- token and allocation constraints;
- governance and administrative authority;
- presale participant rights;
- custody and fund-flow rules;
- lock and vesting commitments;
- transparency and evidence classifications;
- transaction, use-of-funds, outcome, and impact distinctions;
- privacy and protected-information boundaries;
- implementation-status terminology;
- explicit non-goals;
- conformance requirements;
- and requirements that must be satisfied before production release.

The specification set is intended to reduce:

- undocumented assumptions;
- implicit authority;
- contradictory public claims;
- uncontrolled scope expansion;
- retrospective rule changes;
- and divergence between intended and implemented behavior.

---

## 3. Intended Audience

These specifications are written for:

- developers;
- smart-contract engineers;
- security researchers;
- auditors;
- technical reviewers;
- governance reviewers;
- legal and operational reviewers;
- evidence and impact specialists;
- contributors;
- and stakeholders evaluating the GFC system design.

The documents aim to remain understandable to technically oriented non-developers without sacrificing the precision required for implementation and review.

---

## 4. Current Project Context

GFC is intended to combine:

1. a fixed-supply token ecosystem on Base;
2. long-term token allocation and vesting commitments;
3. constrained treasury and governance processes;
4. a transparency infrastructure for fund-flow and evidence reporting;
5. a framework for evaluating documented use of funds and resulting impact.

The token, presale, treasury, governance system, transparency infrastructure, and impact-evaluation process are related but distinct components.

The existence of a blockchain token or public wallet does not by itself create complete transparency or prove impact.

---

## 5. Specification Principles

The specification set follows the principles below.

### 5.1 Specifications precede production implementation

Material production behavior SHOULD be defined before deployment.

### 5.2 Explicit constraints over informal promises

Where authority, rights, limits, or commitments matter, they MUST be documented explicitly.

### 5.3 Verifiable behavior over narrative claims

Public technical claims SHOULD be supported by:

- authenticated implementation records;
- on-chain data;
- supporting evidence;
- or defined review processes.

### 5.4 Authority must remain visible

Every material administrative, governance, custody, upgrade, pause, migration, or evidence-status authority MUST be identifiable.

### 5.5 Implementation status must remain accurate

The following states MUST NOT be presented as interchangeable:

- planned;
- specified;
- implemented;
- tested;
- reviewed;
- audited;
- deployed;
- active;
- and operational.

### 5.6 Privacy-aware transparency

Transparency MUST NOT require unnecessary disclosure of:

- personal information;
- beneficiary information;
- confidential agreements;
- legally protected records;
- or security-sensitive information.

### 5.7 Historical accountability

Material changes, deviations, corrections, incidents, and superseded specifications SHOULD remain historically reviewable.

### 5.8 No retrospective normalization

Specifications MUST NOT be changed retrospectively merely to make unauthorized or non-conforming behavior appear compliant.

### 5.9 Different claims require different evidence

Transaction, use-of-funds, output, outcome, and impact claims MUST NOT be treated as equivalent.

### 5.10 Long-term constraints over short-term flexibility

Long-term token supply, allocation, lock, vesting, custody, and participant-rights commitments MUST NOT contain undocumented bypasses.

---

## 6. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are interpreted according to the applicable conventions derived from RFC 2119 and RFC 8174.

They are normative only when:

- they appear in uppercase;
- the containing document declares `Authority: Normative`;
- and the document version is applicable to the implementation, process, or communication being evaluated.

Normative wording in a Draft document defines intended requirements but may still change before release.

---

## 7. Document Metadata Model

Each specification MUST declare maturity and authority separately.

### 7.1 Maturity

Maturity describes the development and review stage of a document.

#### Draft

The document is under active development and may change materially.

#### Review

The document is structurally complete and awaiting formal review or approval.

#### Stable

The document has been approved for a defined implementation or release.

Stable does not independently mean:

- implemented;
- audited;
- deployed;
- immutable;
- legally approved;
- or operational.

#### Deprecated

The document is retained for historical reference but is no longer applicable to new implementations.

### 7.2 Authority

Authority describes the interpretive role of a document.

#### Informative

The document provides explanation or context but does not independently define binding requirements.

#### Normative

The document defines:

- requirements;
- constraints;
- invariants;
- terminology;
- rights;
- or prohibited behavior.

`Normative` is not a maturity level.

A document may therefore be both:

- Draft and Normative;
- Review and Normative;
- Stable and Normative;
- or Stable and Informative.

### 7.3 Version

The version identifies the released or unreleased revision of the document.

`Unreleased` means that the document has not yet been included in an authoritative versioned specification release.

### 7.4 Implementation Status

Implementation Status describes the relationship between the document and actual system operation.

Possible values may include:

- Pre-deployment;
- Prototype;
- Test deployment;
- Audit candidate;
- Production candidate;
- Active production;
- Deprecated implementation.

---

## 8. Required Specification Header

Each normative specification SHOULD begin with metadata in the following form:

```text
Document ID: GFC-...
Maturity: Draft
Authority: Normative
Version: Unreleased
Implementation Status: Pre-deployment
Intended Network: Base Mainnet
Chain ID: 8453
Last Updated: YYYY-MM-DD
```

Where applicable, a released specification SHOULD additionally identify:

- release identifier;
- superseded version;
- applicable implementation;
- source-code version;
- deployment;
- known deviations;
- and review status.

---

## 9. Current Specification Set

The current specification set consists of the following documents.

### 9.1 `architecture.md`

Defines the high-level GFC system architecture.

It covers:

- Technology, Governance, and Impact and Evidence layers;
- Base as the intended initial network;
- GFC token architecture;
- fixed supply;
- token allocations;
- transaction-fee boundaries;
- presale architecture;
- custody;
- vesting;
- locks;
- staking;
- treasury boundaries;
- authority surfaces;
- upgradeability;
- pause and emergency controls;
- verification layers;
- trust assumptions;
- deployment requirements;
- and architectural conformance.

### 9.2 `governance-constraints.md`

Defines limitations on governance and administrative authority.

It covers:

- explicit authority;
- least privilege;
- separation of duties;
- multisig requirements;
- signer management;
- timelocks;
- proposals;
- voting;
- delegation;
- conflicts of interest;
- upgrades;
- pauses;
- emergency authority;
- fee governance;
- supply protection;
- presale governance;
- treasury governance;
- liquidity governance;
- evidence governance;
- impact governance;
- and governance non-conformance.

### 9.3 `presale.md`

Defines the intended GFC presale model and participant protections.

It covers:

- the €0.05 GFC reference price;
- the intended eight-week duration;
- the €250,000 soft cap;
- the 150,000,000 GFC Presale Allocation;
- purchase accounting;
- payment-asset conversion;
- token entitlement;
- deferred claiming after successful finalization;
- contribution custody;
- successful-sale proceeds;
- refunds;
- cancellation;
- pausing;
- administrative authority;
- unsold-token treatment;
- and presale conformance.

### 9.4 `transparency-model.md`

Defines the GFC transparency, evidence, verification, and disclosure model.

It covers:

- transaction verification;
- use-of-funds verification;
- output, outcome, and impact distinctions;
- public on-chain evidence;
- cryptographically anchored evidence;
- protected off-chain evidence;
- evidence provenance;
- evidence status;
- claim status;
- governance transparency;
- authority transparency;
- contract and wallet registries;
- allocation transparency;
- treasury transparency;
- presale transparency;
- fee and staking transparency;
- lock and vesting transparency;
- corrections;
- disputes;
- independent review;
- privacy;
- and transparency conformance.

### 9.5 `non-goals.md`

Defines intentional exclusions and unsupported interpretations.

It covers non-goals relating to:

- short-term speculation;
- price guarantees;
- return guarantees;
- liquidity guarantees;
- exchange listings;
- market manipulation;
- discretionary inflation;
- separate-chain commitments;
- cross-chain commitments;
- unrestricted token governance;
- false decentralization;
- undocumented authority;
- privacy;
- absolute transparency claims;
- impact guarantees;
- legal and charitable status;
- presale guarantees;
- staking guarantees;
- undocumented feature promises;
- historical deletion;
- and artificial certainty.

### 9.6 `glossary.md`

Defines terminology used across the specification set.

It covers:

- project terminology;
- specification metadata;
- implementation status;
- blockchain terminology;
- token and allocation terms;
- lock and vesting terms;
- presale terms;
- governance and multisig terms;
- authority and custody terms;
- transparency and evidence terminology;
- claim and impact terminology;
- review and audit terminology;
- privacy and security terminology;
- release terminology;
- and legal-status terminology.

Only documents that currently exist in this directory form part of the current specification set.

---

## 10. Recommended Reading Order

For a complete first review, the recommended order is:

1. `glossary.md`
2. `non-goals.md`
3. `architecture.md`
4. `governance-constraints.md`
5. `transparency-model.md`
6. `presale.md`

This order establishes:

1. shared terminology;
2. explicit exclusions;
3. system architecture;
4. authority limitations;
5. evidence and transparency requirements;
6. presale-specific participant and custody rules.

A reviewer evaluating a particular implementation must additionally review:

- the applicable specification release;
- the corresponding source-code version;
- deployment records;
- authenticated contract and wallet addresses;
- audit or review reports;
- the authority registry;
- and known deviations.

---

## 11. Specification Hierarchy

No document in this directory should be interpreted in isolation where another document defines relevant constraints.

The intended relationship is as follows.

### Architecture

Defines high-level system components, relationships, trust boundaries, and architectural constraints.

### Governance Constraints

Defines who may control system components and under which limitations.

### Component Specifications

Define detailed behavior for specific components, such as the presale.

### Transparency Model

Defines how execution, authority, evidence, claims, limitations, and historical records are represented.

### Non-Goals

Define what the system and public communication must not imply or attempt under the current architecture.

### Glossary

Defines shared terminology used to interpret the complete specification set.

---

## 12. Foundational System Distinctions

The specification set preserves the following verification distinctions.

### 12.1 Transaction Verification

Question:

**Did the funds move as stated?**

Primary evidence may include:

- on-chain transactions;
- contract events;
- wallet balances;
- timestamps;
- and verified contract state.

### 12.2 Use-of-Funds Verification

Question:

**Were the funds used for the documented purpose?**

Primary evidence may include:

- approvals;
- invoices;
- agreements;
- receipts;
- reconciliations;
- delivery records;
- and protected supporting documentation.

### 12.3 Impact Verification

Question:

**Did the documented use create a meaningful result?**

Primary evidence may include:

- outputs;
- outcomes;
- indicators;
- methodology;
- independent review;
- follow-up data;
- and uncertainty disclosures.

The following distinction applies throughout the specification set:

> TRANSACTION VERIFIED does not equal IMPACT VERIFIED.

Different claims require different evidence.

---

## 13. Evidence Disclosure Model

The specification set distinguishes between three evidence disclosure levels.

### 13.1 Public On-Chain

Information recorded or directly derivable from authenticated blockchain data.

Examples may include:

- contract addresses;
- transfers;
- balances;
- allocation state;
- lock state;
- vesting state;
- governance execution;
- and cryptographic commitments.

### 13.2 Cryptographically Anchored

Off-chain information whose integrity is linked to a public cryptographic commitment.

Anchoring may support:

- record existence;
- record version;
- record integrity;
- or publication time.

Anchoring does not independently establish factual truth.

### 13.3 Protected Off-Chain

Information maintained outside the public blockchain because it is:

- personal;
- confidential;
- legally protected;
- operationally sensitive;
- commercially sensitive;
- or security-sensitive.

Protected evidence may remain reviewable without being publicly exposed.

---

## 14. Conflict Resolution

Specifications SHOULD be internally consistent.

Where a conflict exists:

1. the conflict MUST be documented;
2. neither conflicting requirement should be treated as production-ready;
3. the affected documents MUST be reviewed together;
4. the resolution MUST be versioned;
5. the rationale and impact MUST be documented;
6. affected implementations and communications MUST be identified.

A conflict MUST NOT be resolved solely through:

- an informal statement;
- a user-interface change;
- an unpublished internal interpretation;
- or retrospective editing without change documentation.

---

## 15. Actual Execution and Intended Behavior

The following distinction applies throughout the specification set.

### 15.1 Actual Execution

Deployed code and authenticated on-chain state determine what technically executed.

### 15.2 Intended and Conforming Behavior

The applicable versioned specification defines what the implementation was intended and approved to do.

### 15.3 User-Interface Representation

User interfaces MUST accurately represent actual contract and system behavior.

### 15.4 Off-Chain Processes

Operational, governance, accounting, evidence, and impact records determine how contextual decisions and real-world processes were handled.

### 15.5 Deviation

A difference between actual behavior and applicable specified behavior is a:

- deviation;
- defect;
- incident;
- governance violation;
- or version mismatch.

It is not automatically resolved by declaring the implementation correct or by rewriting the specification after the event.

---

## 16. Source of Authority

The files in this directory represent the current working specification state.

They do not automatically constitute the authoritative specification for a production implementation.

For a specification to become authoritative for a defined implementation, it SHOULD be:

- included in a versioned repository release;
- linked to a specific source-code version or commit;
- assigned to a defined network;
- linked to authenticated deployment addresses;
- accompanied by review or audit information;
- and accompanied by known-deviation information.

Versioned releases, rather than the continuously changing `main` branch, SHOULD serve as the authoritative reference for corresponding production implementations.

---

## 17. Release Requirements

A specification release intended to govern a production implementation SHOULD identify:

- release identifier;
- included specification versions;
- release date;
- applicable source-code release;
- source-code commit;
- intended network;
- deployed contracts;
- deployment addresses;
- authority registry;
- audit or review status;
- known deviations;
- upgradeability;
- pause authority;
- migration status;
- and deprecation information.

A specification release MUST distinguish between:

- test deployment;
- audit candidate;
- production candidate;
- active production deployment;
- deprecated deployment;
- and replacement deployment.

---

## 18. Implementation Relationship

Future implementations MUST distinguish between the following states.

### 18.1 Experimental Implementation

Code used for internal or public experimentation without production guarantees.

### 18.2 Prototype

A functional demonstration of selected behavior.

### 18.3 Test Deployment

A deployment on a test network or another non-production environment.

### 18.4 Audit Candidate

A version submitted for defined security or technical review.

### 18.5 Production Candidate

A version considered for production deployment but not yet active.

### 18.6 Production Deployment

A released deployment intended for actual use.

### 18.7 Deprecated Implementation

An implementation no longer recommended or supported for new use.

A prototype, test deployment, or audit candidate MUST NOT be presented as active production infrastructure.

---

## 19. Conformance

A component or implementation is conforming only when:

- it identifies an applicable versioned specification;
- it satisfies all applicable normative requirements;
- its actual authority surface is disclosed;
- its implementation status is accurately represented;
- its public interface accurately represents behavior;
- material deviations are documented;
- and related specifications are mutually consistent.

A Draft specification MAY guide development and review.

A Draft specification MUST NOT be presented as a finalized production guarantee.

---

## 20. Public Communication Requirements

Public technical communication MUST distinguish between:

- planned behavior;
- specified behavior;
- implemented behavior;
- tested behavior;
- reviewed behavior;
- audited behavior;
- deployed behavior;
- active behavior;
- and independently verified claims.

Public communication MUST NOT:

- present Draft requirements as completed functionality;
- imply that publishing a wallet address proves fund use;
- imply that transaction verification proves impact;
- imply that cryptographic anchoring proves factual truth;
- imply decentralization while material authority remains undisclosed;
- describe a review as an audit without a defined audit scope;
- imply guaranteed price, profit, liquidity, listing, completion, or impact;
- or imply legal, charitable, nonprofit, tax-exempt, or regulatory status without a documented basis.

---

## 21. Change Classification

Changes to specifications MUST be classified according to their effect.

### 21.1 Editorial Change

Corrects:

- grammar;
- spelling;
- formatting;
- broken links;
- or equivalent presentation issues

without changing meaning.

### 21.2 Clarification

Improves precision without materially changing:

- required behavior;
- rights;
- authority;
- constraints;
- or system outcomes.

### 21.3 Non-Breaking Change

Adds compatible detail, definitions, safeguards, or requirements without invalidating previously conforming behavior.

### 21.4 Breaking Change

Changes a material aspect of:

- token supply;
- token allocation;
- fees;
- transfer behavior;
- lock duration;
- vesting;
- participant rights;
- refund rights;
- custody;
- authority;
- approval requirements;
- governance power;
- upgradeability;
- pause behavior;
- migration;
- evidence requirements;
- privacy boundaries;
- or security assumptions.

### 21.5 Deprecation

Marks a specification or implementation as no longer applicable for new use while preserving it for historical review.

---

## 22. Breaking-Change Requirements

A breaking change requires:

- explicit versioning;
- documented rationale;
- identification of affected requirements;
- security impact analysis;
- governance impact analysis;
- participant-rights analysis;
- compatibility analysis;
- migration analysis;
- affected implementation identification;
- affected public-claim identification;
- and clear effective timing.

Breaking changes MUST NOT be introduced solely through:

- a user-interface update;
- a social-media announcement;
- an informal team decision;
- or an undocumented code deployment.

---

## 23. Clarifications

A clarification MUST NOT materially change:

- permissions;
- authorities;
- supply;
- allocations;
- thresholds;
- timing;
- participant rights;
- fund-flow behavior;
- refund conditions;
- evidence standards;
- privacy boundaries;
- or security assumptions.

A change affecting one of these matters is not merely a clarification.

---

## 24. Deprecation

A deprecated specification SHOULD identify:

- deprecation date;
- reason;
- successor document;
- affected implementations;
- migration path;
- continuing obligations;
- and continuing risks.

Deprecated specifications SHOULD remain available for historical review.

Git history alone is not sufficient deprecation documentation.

---

## 25. Historical Integrity

Material specification history SHOULD remain reviewable.

This includes:

- released versions;
- breaking changes;
- corrections;
- deprecated documents;
- known deviations;
- and implementation mappings.

A materially relevant specification MUST NOT be silently deleted merely because it is:

- outdated;
- unfavorable;
- contradicted by later implementation;
- or reputationally inconvenient.

Where legal, privacy, or security redaction is necessary, the existence and reason category of the change SHOULD remain documented where appropriate.

---

## 26. Review Requirements

Before a specification is marked Stable, it SHOULD be reviewed for:

- technical feasibility;
- security implications;
- governance implications;
- participant-rights implications;
- operational dependencies;
- privacy implications;
- legal and regulatory dependencies where relevant;
- internal consistency;
- terminology consistency;
- compatibility with related specifications;
- implementation testability;
- and consistency with public technical claims.

A Stable designation does not independently mean that an implementation has been audited or deployed.

---

## 27. Contribution Requirements

Contributions to this directory SHOULD:

- preserve the specification-first approach;
- use current glossary terminology;
- identify affected specifications;
- explain authority implications;
- explain security implications;
- explain participant-rights implications;
- explain compatibility implications;
- distinguish clarifications from breaking changes;
- avoid introducing unsupported implementation claims;
- and include rationale for material changes.

Changes to normative documents SHOULD be submitted through a branch and pull request rather than committed directly to `main`.

---

## 28. Pull Request Expectations

A pull request changing a normative specification SHOULD identify:

- affected document;
- change category;
- reason;
- affected requirements;
- related specifications;
- security implications;
- governance implications;
- participant impact;
- implementation impact;
- migration impact where relevant;
- and whether public communication must also change.

Large normative changes SHOULD remain isolated from unrelated edits.

---

## 29. Approval Requirements

The final approval process for Stable specifications remains unresolved.

Before the first Stable release, the project MUST define:

- who may approve specifications;
- required reviewer categories;
- minimum review period;
- conflict-of-interest treatment;
- technical review requirements;
- security review requirements;
- legal review requirements where relevant;
- governance review requirements;
- and release authorization.

A document MUST NOT be marked Stable solely because it has existed without objection.

---

## 30. Security

Potential vulnerabilities in specifications or future implementations SHOULD be reported according to the repository-level `SECURITY.md`.

Sensitive issues MUST NOT be disclosed through public issues where premature disclosure could place the following at risk:

- users;
- participant funds;
- wallets;
- contracts;
- infrastructure;
- protected evidence;
- or future deployments.

A specification defect may itself be security-relevant where it creates:

- ambiguous authority;
- unsafe custody;
- inconsistent refund rights;
- weak upgrade constraints;
- incomplete invariants;
- or misleading implementation assumptions.

---

## 31. Privacy

Specifications SHOULD avoid requiring unnecessary publication of:

- personal data;
- beneficiary information;
- identity documents;
- banking information;
- confidential agreements;
- security-sensitive records;
- or legally protected information.

Transparency requirements SHOULD distinguish between:

- public on-chain evidence;
- cryptographically anchored evidence;
- and protected off-chain evidence.

The specification set MUST NOT equate unrestricted disclosure with accountability.

---

## 32. Naming

The current project name is:

**Global Foundation Coin**

The abbreviation is:

**GFC**

The historical name `German Foundation Coin` is deprecated.

It MAY remain in historical records where necessary for accurate archival context.

Current specifications and current public technical documentation SHOULD use `Global Foundation Coin`.

The project name does not independently establish:

- a legal foundation;
- charitable status;
- nonprofit status;
- tax-exempt status;
- governmental recognition;
- regulatory approval;
- or a particular legal entity.

---

## 33. Repository Boundaries

This specification directory is intended for formal architectural, behavioral, governance, transparency, and terminology documentation.

It is not intended to contain:

- temporary implementation experiments;
- promotional campaign copy;
- social-media content;
- unreviewed token claims;
- undocumented roadmap promises;
- production secrets;
- private keys;
- credentials;
- confidential personal information;
- or unsupported legal representations.

Implementation code, deployment records, public interfaces, and operational policies may exist elsewhere but MUST identify their relationship to the applicable specifications.

---

## 34. Future Specification Areas

Additional specifications may be introduced where the architecture requires greater precision.

Potential future areas include:

- token and fee implementation;
- allocation and treasury controls;
- Impact Vault implementation;
- Core Team vesting;
- staking;
- governance execution;
- deployment authentication;
- contract migration;
- evidence schemas;
- evidence storage;
- privacy;
- incident response;
- and impact methodology.

These are potential specification areas.

They MUST NOT be treated as existing, finalized, or committed functionality until the corresponding documents are created and approved.

---

## 35. Current Unresolved Repository Decisions

The following repository-level matters remain unresolved:

- final specification versioning format;
- first release identifier;
- final approval process;
- reviewer roles;
- Stable-status authorization;
- formal change-classification template;
- release-signing process;
- specification-to-code linkage format;
- deployment-record format;
- known-deviation format;
- deprecation template;
- and long-term archival process.

These matters MUST be resolved before the first production-governing specification release.

---

## 36. Requirements Before Stable Status

This index MUST NOT be marked Stable until:

- all current specifications are mutually consistent;
- all current specifications use the correct project name;
- document metadata is consistent;
- maturity and authority are separated across all documents;
- the specification versioning system is finalized;
- release requirements are finalized;
- approval authority is defined;
- reviewer requirements are defined;
- conflict-resolution procedures are finalized;
- change classification is finalized;
- deprecation procedures are finalized;
- specification-to-implementation linkage is finalized;
- deployment-record requirements are finalized;
- known-deviation requirements are finalized;
- repository-wide outdated terminology is corrected;
- public technical communication is consistent with current specifications;
- and the first versioned specification release process is ready.

---

## 37. Final Specification Principles

The specification set preserves the following distinctions:

> Normative is not a maturity level.

> Draft does not mean non-normative.

> Stable does not mean implemented.

> Specified does not mean deployed.

> Implemented does not mean audited.

> Audited does not mean risk-free.

> Deployed does not mean conforming.

> Actual execution is determined by deployed code and authenticated on-chain state.

> Conformance is determined by the applicable released specification.

> A user interface does not override contract behavior.

> An informal statement does not override a released specification.

> A wallet label does not technically restrict asset use.

> Transaction verification does not equal use-of-funds verification.

> Use-of-funds verification does not equal impact verification.

> Cryptographic integrity does not equal factual truth.

> Git history alone is not sufficient release or change documentation.

> The `main` branch is not automatically the production source of authority.

> Different claims require different evidence.

The purpose of the specification set is to make intended behavior, authority, rights, constraints, evidence requirements, limitations, and change history reviewable before production reliance.

# Global Foundation Coin Specifications

**Document ID:** GFC-SPECS-INDEX  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Intended Production Network:** Base Mainnet  
**Production Chain ID:** 8453  
**Public Pilot Network:** Base Sepolia  
**Pilot Chain ID:** 84532  
**Last Updated:** 2026-08-30

---

## 1. Document Status

This directory contains the current working specifications for the Global Foundation Coin (GFC) infrastructure.

The specification set follows a specification-first development process.

Intended system behavior, authority boundaries, economic constraints, participant protections, security assumptions, transparency requirements, evidence rules, and prohibited behavior are documented before production reliance.

GFC is currently in a **pre-mainnet development phase**.

The current primary product focus is the **GFC Token / Economic Layer**.

The broader long-term direction is an **Accountability Infrastructure** connecting:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

The broader system is not represented as fully implemented or production-deployed today.

At the current repository state:

- no official GFC token is deployed on Base Mainnet;
- no GFC presale is live;
- no production presale contract is established as official;
- no production treasury infrastructure is represented as active;
- no production governance infrastructure is represented as active;
- no production staking infrastructure is represented as operational;
- no production allocation or vesting contracts are established as official;
- no complete production Transparency Registry is represented as deployed;
- no broader production accountability infrastructure is represented as deployed;
- no production contract or wallet address is established as official by this directory;
- no public presale launch date is established by this directory;
- no production specification release has been designated;
- and the specifications remain subject to review and material revision before their first versioned release.

A public **Base Sepolia pilot** exists.

That pilot is a testnet implementation and MUST NOT be interpreted as:

- a Base Mainnet deployment;
- the production GFC token;
- a live presale;
- production treasury infrastructure;
- production governance infrastructure;
- production staking infrastructure;
- or proof that future production contracts will use identical code, parameters, addresses, or authority structures.

Current deployment and operational status is tracked separately in [`../STATUS.md`](../STATUS.md).

The presence of a specification does not mean that the described component has already been:

- implemented;
- tested;
- independently reviewed;
- audited;
- deployed;
- activated;
- made operational;
- or made available for production use.

The continuously changing `main` branch MUST NOT automatically be treated as the authoritative specification governing a future production implementation.

---

## 2. Purpose

The purpose of this specification set is to establish a clear, reviewable, internally consistent, and versionable reference for the intended GFC infrastructure.

The specifications define or constrain:

- system architecture and component boundaries;
- token behavior;
- token-supply constraints;
- allocation rules;
- vesting and unlock rules;
- economic flows;
- staking design;
- presale behavior and participant protections;
- governance and administrative authority;
- role boundaries;
- security assumptions and requirements;
- custody and fund-flow rules;
- transparency requirements;
- evidence classifications;
- transaction, use-of-funds, output, outcome, and impact distinctions;
- privacy and protected-information boundaries;
- implementation-status terminology;
- explicit non-goals;
- conformance requirements;
- and requirements that must be satisfied before production reliance.

The specification set is intended to reduce:

- undocumented assumptions;
- implicit authority;
- contradictory technical claims;
- contradictory public claims;
- uncontrolled scope expansion;
- retrospective rule changes;
- unclear participant rights;
- hidden administrative powers;
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
- integration partners;
- and stakeholders evaluating the GFC system design.

The documents aim to remain understandable to technically oriented non-developers without sacrificing the precision required for implementation and review.

---

## 4. Current Project Context

The current GFC product focus is the **GFC Token / Economic Layer**.

The intended production token system is being designed around:

- a fixed token supply;
- defined allocations;
- constrained token economics;
- long-term allocation and vesting commitments;
- defined economic flows;
- participant-protected presale mechanics;
- non-inflationary staking design;
- explicit authority boundaries;
- security constraints;
- and verifiable deployment and operational records.

The token and economic layer are not intended to exist in isolation.

The longer-term GFC architecture is intended to expand toward broader accountability infrastructure connecting:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

Potential system areas therefore include:

1. the GFC Token / Economic Layer;
2. allocation and custody infrastructure;
3. governance and authority controls;
4. transparency infrastructure;
5. evidence and verification mechanisms;
6. historical accountability records;
7. and later broader accountability tooling.

These areas are related but distinct.

Their existence, maturity, and deployment status MUST be represented separately.

A blockchain token, public wallet, verified contract, transaction history, or cryptographic commitment does not by itself establish:

- compliant governance;
- documented use of funds;
- successful outcomes;
- verified impact;
- or complete accountability.

---

## 5. Specification Principles

The specification set follows the principles below.

### 5.1 Specifications precede production reliance

Material production behavior SHOULD be defined before production deployment or operational reliance.

### 5.2 Explicit constraints over informal promises

Where authority, rights, limits, commitments, exceptions, or economic behavior matter, they MUST be documented explicitly.

### 5.3 Verifiable behavior over narrative claims

Technical and operational claims SHOULD be supported by appropriate evidence, including where applicable:

- authenticated implementation records;
- authenticated deployments;
- on-chain data;
- contract state;
- supporting evidence;
- versioned specifications;
- or defined review processes.

### 5.4 Authority must remain visible

Every material administrative, governance, custody, upgrade, pause, migration, fee, treasury, verification, or evidence-status authority MUST be identifiable.

### 5.5 Implementation status must remain accurate

The following states MUST NOT be treated as interchangeable:

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
- and Not Deployed.

A stronger status MUST NOT be claimed than the available evidence supports.

### 5.6 Pilot and production must remain distinct

Testnet, prototype, pilot, staging, and production systems MUST be represented as separate environments.

A public pilot MUST NOT acquire production authority merely because it is publicly accessible, verified, used, or long-running.

### 5.7 Privacy-aware transparency

Transparency MUST NOT require unnecessary disclosure of:

- personal information;
- beneficiary information;
- confidential agreements;
- legally protected records;
- commercially sensitive records;
- or security-sensitive information.

### 5.8 Historical accountability

Material changes, deviations, corrections, incidents, superseded specifications, and authority changes SHOULD remain historically reviewable.

### 5.9 No retrospective normalization

Specifications MUST NOT be changed retrospectively merely to make unauthorized, misleading, or non-conforming behavior appear compliant.

### 5.10 Different claims require different evidence

Transaction, use-of-funds, output, outcome, and impact claims MUST NOT be treated as equivalent.

### 5.11 Long-term constraints over short-term flexibility

Long-term token supply, allocation, lock, vesting, custody, participant-rights, and authority commitments MUST NOT contain undocumented bypasses.

### 5.12 Responsibility follows authority

Where a role can materially affect funds, rules, execution, verification, or system outcomes, that authority and its corresponding accountability requirements MUST be identifiable.

---

## 6. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are interpreted according to the applicable conventions derived from RFC 2119 and RFC 8174.

They are normative only when:

- they appear in uppercase;
- the containing document declares `Authority: Normative`;
- and the document version is applicable to the implementation, process, or communication being evaluated.

Normative wording in a Draft document defines the current intended requirement but MAY change before a versioned release.

---

## 7. Document Metadata Model

Each specification MUST distinguish maturity, authority, version, and implementation status.

### 7.1 Maturity

Maturity describes the development and review stage of a document.

#### Draft

The document is under active development and may change materially.

#### Review

The document is structurally complete and awaiting defined review or approval.

#### Stable

The document has been approved for a defined specification release or implementation.

Stable does not independently mean:

- implemented;
- audited;
- deployed;
- immutable;
- legally approved;
- regulatory approved;
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
- authority boundaries;
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

Implementation Status describes the relationship between the document and actual system development or operation.

Possible values may include:

- Pre-mainnet specification development;
- Experimental implementation;
- Prototype;
- Test deployment;
- Pilot;
- Audit candidate;
- Production candidate;
- Production deployment;
- Active production;
- Deprecated implementation.

Implementation status MUST NOT be inferred solely from specification maturity.

---

## 8. Required Specification Header

Each normative specification SHOULD begin with metadata in the following form:

```text
Document ID: GFC-...
Maturity: Draft
Authority: Normative
Version: Unreleased
Implementation Status: Pre-mainnet specification development
Intended Production Network: Base Mainnet
Production Chain ID: 8453
Last Updated: YYYY-MM-DD
```

Where a specification directly concerns an existing pilot, it SHOULD additionally identify the relevant pilot environment separately.

Where applicable, a released specification SHOULD additionally identify:

- release identifier;
- superseded version;
- applicable implementation;
- source-code version;
- deployment;
- known deviations;
- and review status.

---

## 9. Specification Architecture

The specification architecture for this repository is organized into the following documents.

A document forms part of the active repository specification set only when the corresponding file exists in the repository.

### 9.1 `glossary.md`

Defines shared terminology used across the specification set.

It covers terminology relating to:

- GFC project structure;
- specification maturity and authority;
- implementation and deployment status;
- blockchain networks;
- token behavior;
- allocations;
- locks and vesting;
- economic flows;
- staking;
- presale mechanics;
- governance;
- roles and authority;
- custody;
- security;
- transparency;
- evidence;
- verification;
- claims;
- outcomes;
- impact;
- privacy;
- review;
- audit;
- releases;
- and legal-status terminology.

### 9.2 `non-goals.md`

Defines intentional exclusions, unsupported interpretations, and boundaries.

It includes non-goals relating to:

- short-term speculation;
- price guarantees;
- return guarantees;
- guaranteed liquidity;
- guaranteed exchange listings;
- market manipulation;
- discretionary inflation;
- unsupported cross-chain commitments;
- unrestricted governance;
- false decentralization;
- undocumented authority;
- absolute transparency claims;
- impact guarantees;
- legal or charitable-status assumptions;
- presale guarantees;
- staking guarantees;
- undocumented feature promises;
- and artificial certainty.

### 9.3 `architecture.md`

Defines the high-level GFC system architecture.

It covers:

- the current Token / Economic Layer focus;
- longer-term accountability architecture;
- component boundaries;
- Base as the intended production network;
- Base Sepolia pilot separation;
- trust boundaries;
- contract relationships;
- allocation infrastructure;
- economic flows;
- presale components;
- staking components;
- governance boundaries;
- transparency components;
- evidence interfaces;
- deployment boundaries;
- and architectural conformance.

### 9.4 `roles-and-authority.md`

Defines system roles and their permitted authority surfaces.

It covers:

- role definitions;
- authority ownership;
- signer roles;
- treasury authority;
- governance authority;
- deployment authority;
- upgrade authority;
- pause authority;
- migration authority;
- fee authority;
- evidence authority;
- verification authority;
- conflict boundaries;
- and separation-of-duty requirements.

### 9.5 `governance-constraints.md`

Defines limitations on governance and administrative authority.

It covers:

- explicit authority;
- least privilege;
- separation of duties;
- multisig requirements;
- signer management;
- timelocks;
- proposals;
- voting where applicable;
- delegation where applicable;
- conflicts of interest;
- upgrades;
- pauses;
- emergency authority;
- fee governance;
- supply protection;
- presale governance;
- treasury governance;
- liquidity governance;
- transparency governance;
- verification governance;
- and governance non-conformance.

### 9.6 `security-model.md`

Defines system security assumptions, invariants, threat surfaces, and required protections.

It covers:

- protected assets;
- trust assumptions;
- privileged authority;
- key compromise;
- signer compromise;
- contract vulnerabilities;
- upgrade risk;
- pause risk;
- oracle or dependency risk where applicable;
- presale risks;
- treasury risks;
- liquidity risks;
- staking risks;
- evidence-integrity risks;
- operational-security boundaries;
- and security invariants.

### 9.7 `token.md`

Defines intended GFC token behavior.

It covers:

- intended Base Mainnet deployment;
- fixed total supply;
- token precision;
- transfer behavior;
- fee behavior;
- minting constraints;
- burning behavior where applicable;
- privileged authority;
- prohibited hidden controls;
- and token-level invariants.

The intended production supply is:

**1,000,000,000 GFC**

The intended token standard is ERC-20 with 18 decimals.

No production GFC token is currently deployed on Base Mainnet.

### 9.8 `allocations.md`

Defines the intended fixed token-allocation structure.

The current draft allocation model is:

| Allocation | Share | Tokens |
|---|---:|---:|
| Impact Vault | 25% | 250,000,000 GFC |
| Guardian Growth | 20% | 200,000,000 GFC |
| Presale | 15% | 150,000,000 GFC |
| Treasury Reserve | 15% | 150,000,000 GFC |
| Liquidity Reserve | 15% | 150,000,000 GFC |
| Ecosystem | 5% | 50,000,000 GFC |
| Core Team | 5% | 50,000,000 GFC |
| **Total** | **100%** | **1,000,000,000 GFC** |

These values are current Draft specification parameters.

They are not evidence of deployed production allocations.

### 9.9 `vesting-and-unlocks.md`

Defines token-lock, vesting, release, and unlock requirements.

It covers:

- allocation-specific restrictions;
- Core Team vesting;
- long-term Impact Vault constraints;
- unlock schedules;
- release authority;
- bypass prevention;
- migration treatment;
- and public disclosure requirements.

### 9.10 `economic-flows.md`

Defines intended token and fund flows between economic components.

It covers:

- transfer-fee flows;
- presale flows;
- treasury flows;
- liquidity flows;
- allocation movement;
- staking reward sources;
- custody transitions;
- and accounting boundaries.

### 9.11 `staking.md`

Defines the intended staking model.

The current design direction is hybrid and non-inflationary.

The specification covers:

- staking eligibility;
- reward sources;
- reward accounting;
- non-inflationary constraints;
- custody;
- lock behavior where applicable;
- authority;
- emergency behavior;
- and transparency requirements.

No production GFC staking system is currently operational.

### 9.12 `presale.md`

Defines the intended GFC presale model and participant protections.

The current Draft design includes:

- a reference price of €0.05 per GFC;
- an intended eight-week duration;
- a €250,000 soft cap;
- no intended hard cap;
- a 150,000,000 GFC Presale Allocation;
- intended support for ETH, USDC, and DAI on Base;
- participant accounting;
- intended token distribution behavior;
- contribution custody;
- successful-sale proceeds;
- refunds if the soft cap is not reached;
- cancellation behavior;
- pause behavior where applicable;
- administrative authority;
- unsold-token treatment;
- and presale conformance.

No GFC presale is currently live.

No public presale launch date is established by this specification index.

### 9.13 `transparency-model.md`

Defines the GFC transparency, evidence, verification, and historical-record model.

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
- contract and wallet records;
- allocation transparency;
- treasury transparency;
- presale transparency;
- fee and staking transparency;
- lock and vesting transparency;
- corrections;
- disputes;
- independent review;
- privacy;
- version history;
- and transparency conformance.

The intended Transparency Registry model is a **versioned historical record**, not a permanent approval badge.

### 9.14 Specification Index

This file, `README.md`, defines:

- specification-set structure;
- shared document rules;
- metadata requirements;
- hierarchy;
- release expectations;
- conformance principles;
- and repository-level specification governance.

It does not replace the detailed component specifications.

---

## 10. Recommended Reading Order

For a complete first review, the recommended order is:

1. `README.md`
2. `glossary.md`
3. `non-goals.md`
4. `architecture.md`
5. `roles-and-authority.md`
6. `governance-constraints.md`
7. `security-model.md`
8. `token.md`
9. `allocations.md`
10. `vesting-and-unlocks.md`
11. `economic-flows.md`
12. `staking.md`
13. `presale.md`
14. `transparency-model.md`

This order establishes:

1. repository and specification rules;
2. shared terminology;
3. explicit exclusions;
4. system architecture;
5. authority ownership;
6. governance limitations;
7. security assumptions;
8. token behavior;
9. token distribution;
10. long-term locks and release constraints;
11. economic movement;
12. staking behavior;
13. presale participant protections;
14. evidence and accountability requirements.

A reviewer evaluating an implementation must additionally review:

- the applicable specification release;
- the corresponding source-code release or commit;
- deployment records;
- authenticated contract addresses;
- authenticated wallet addresses;
- audit or review reports;
- disclosed authority structures;
- and known deviations.

---

## 11. Specification Hierarchy

No specification should be interpreted in isolation where another document defines an applicable constraint.

The intended relationship is as follows.

### Specification Index

Defines repository-wide specification rules and interpretation principles.

### Glossary

Defines shared terminology.

### Non-Goals

Defines what the system, specification, and public communication must not imply or attempt under the current design.

### Architecture

Defines high-level system components, relationships, boundaries, and trust assumptions.

### Roles and Authority

Defines who or what may exercise material authority.

### Governance Constraints

Defines limitations on the exercise of that authority.

### Security Model

Defines security assumptions, protected assets, threats, and required invariants.

### Token and Economic Specifications

Define:

- token behavior;
- allocations;
- vesting and unlocks;
- economic flows;
- and staking.

### Presale Specification

Defines participant-facing presale mechanics, custody, rights, and protections.

### Transparency Model

Defines how funds, authority, rules, decisions, outcomes, evidence, corrections, and historical changes are represented.

Where two normative requirements conflict, the conflict MUST be resolved explicitly rather than silently choosing one document.

---

## 12. Foundational Accountability Model

The long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

Each element represents a distinct question.

### 12.1 Funds

What value moved, where, when, and under whose custody?

### 12.2 Authority

Who or what was permitted to make, approve, block, modify, or execute a material action?

### 12.3 Rules

What requirements, constraints, policies, or contract logic governed the action?

### 12.4 Decisions

What decision was made, by whom, under what authority, and through what process?

### 12.5 Outcomes

What occurred as a result of the decision and execution?

### 12.6 Evidence

What evidence supports the claims concerning the preceding stages?

The framework does not imply that all evidence can or should exist on-chain.

---

## 13. Verification Distinctions

The specification set preserves the following verification distinctions.

### 13.1 Transaction Verification

Question:

**Did the funds move as stated?**

Primary evidence may include:

- authenticated on-chain transactions;
- contract events;
- wallet balances;
- timestamps;
- and verified contract state.

### 13.2 Use-of-Funds Verification

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

### 13.3 Output Verification

Question:

**Was a documented activity, deliverable, or service produced?**

Evidence may include:

- delivery records;
- completion evidence;
- project records;
- measurements;
- and independent confirmation where appropriate.

### 13.4 Outcome Verification

Question:

**Did the documented activity create the claimed result?**

Evidence may include:

- follow-up data;
- defined indicators;
- measurement methodology;
- comparison data;
- and independent review.

### 13.5 Impact Verification

Question:

**Can a broader meaningful effect be supported by appropriate evidence and methodology?**

Evidence may include:

- outcome data;
- methodology;
- attribution analysis;
- uncertainty disclosures;
- longitudinal evidence;
- and independent review.

The following distinction applies throughout the specification set:

> TRANSACTION VERIFIED does not equal USE OF FUNDS VERIFIED.

> USE OF FUNDS VERIFIED does not equal OUTCOME VERIFIED.

> OUTCOME VERIFIED does not automatically equal IMPACT VERIFIED.

Different claims require different evidence.

---

## 14. Evidence Disclosure Model

The specification set distinguishes between three broad evidence-disclosure levels.

### 14.1 Public On-Chain

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

### 14.2 Cryptographically Anchored

Off-chain information whose integrity is linked to a public cryptographic commitment.

Anchoring may support evidence of:

- record existence;
- record version;
- record integrity;
- or publication timing.

Anchoring does not independently establish factual truth.

### 14.3 Protected Off-Chain

Information maintained outside the public blockchain because it is:

- personal;
- confidential;
- legally protected;
- operationally sensitive;
- commercially sensitive;
- or security-sensitive.

Protected evidence may remain reviewable without being publicly exposed.

Transparency MUST NOT be interpreted as an obligation to expose information whose disclosure would create disproportionate legal, privacy, safety, or security risk.

---

## 15. Status Terminology

Specification and public technical communication MUST preserve the status distinctions defined in [`../STATUS.md`](../STATUS.md).

At minimum:

### Draft

The document, parameter, or design is under development and remains subject to revision.

### Proposed

The design, parameter, behavior, or decision has been put forward but has not necessarily been finally adopted or implemented.

### Planned

The component or activity is intended for future work.

### Specified

Requirements or intended behavior have been documented.

### Implemented

Relevant source code or operational processes have been created.

### Tested

Defined tests have been performed against an identified implementation.

### Pilot

A limited implementation or deployment exists for experimentation, validation, demonstration, or learning.

### Reviewed

An identified review process has been completed.

### Audited

A specifically scoped audit has been completed by an identified auditor.

### Deployed

A component exists in an identified deployment environment.

### Live

A component is currently accessible or available in its explicitly stated environment.

### Active

A deployed component has been intentionally activated for its stated role.

### Operational

A component is being operated for its stated function.

### Independently Verified

An appropriately independent party has verified a specifically defined claim, component, record, or process.

### Not Deployed

No authenticated deployment for the stated environment or production role is represented by the repository.

These states are not interchangeable.

---

## 16. Pilot and Production Separation

The current public Base Sepolia deployment is a pilot.

Its existence establishes neither production status nor production authority.

A pilot deployment MUST NOT be used as evidence that:

- Mainnet contracts have been deployed;
- production token parameters are technically enforced;
- production allocations exist;
- production vesting exists;
- production staking exists;
- production treasury controls exist;
- production governance exists;
- production liquidity exists;
- the presale is live;
- or the broader accountability infrastructure is operational.

Production systems require independent deployment authentication and status records.

---

## 17. Conflict Resolution

Specifications SHOULD be internally consistent.

Where a material conflict exists:

1. the conflict MUST be documented;
2. neither conflicting requirement should be treated as production-ready;
3. all affected documents MUST be reviewed together;
4. the resolution MUST be versioned;
5. the rationale and impact MUST be documented;
6. affected implementations MUST be identified;
7. affected public communication MUST be identified where relevant.

A conflict MUST NOT be resolved solely through:

- an informal statement;
- a user-interface change;
- an unpublished internal interpretation;
- or retrospective editing without change documentation.

---

## 18. Actual Execution and Intended Behavior

The following distinction applies throughout the specification set.

### 18.1 Actual Execution

Deployed code and authenticated system state determine what technically executed.

### 18.2 Intended and Conforming Behavior

The applicable versioned specification defines what the implementation was intended and approved to do.

### 18.3 User-Interface Representation

User interfaces MUST accurately represent actual contract and system behavior.

### 18.4 Off-Chain Processes

Operational, governance, accounting, evidence, and impact records determine how relevant off-chain decisions and real-world processes were handled.

### 18.5 Deviation

A difference between actual behavior and applicable specified behavior may constitute a:

- deviation;
- defect;
- incident;
- governance violation;
- security violation;
- or version mismatch.

It is not automatically resolved by rewriting the specification after the event.

---

## 19. Source of Authority

The files in this directory represent the current working specification state.

They do not automatically constitute the authoritative specification for a production implementation.

For a specification set to become authoritative for a defined production implementation, it SHOULD be:

- included in a versioned repository release;
- linked to a specific source-code release or commit;
- assigned to a defined network;
- linked to authenticated deployment addresses;
- accompanied by deployment records;
- accompanied by disclosed authority information;
- accompanied by applicable review or audit information;
- and accompanied by known-deviation information.

Versioned releases, rather than the continuously changing `main` branch, SHOULD serve as the authoritative specification reference for corresponding production implementations.

---

## 20. Release Requirements

A specification release intended to govern a production implementation SHOULD identify:

- release identifier;
- included specification versions;
- release date;
- applicable source-code release;
- source-code commit;
- production network;
- deployed contracts;
- authenticated deployment addresses;
- authenticated operational addresses where applicable;
- authority structure;
- audit or review status;
- known deviations;
- upgradeability;
- pause authority;
- migration status;
- and deprecation information.

A specification release MUST distinguish between:

- experimental implementation;
- prototype;
- test deployment;
- pilot;
- audit candidate;
- production candidate;
- production deployment;
- active production deployment;
- deprecated deployment;
- and replacement deployment.

---

## 21. Implementation Relationship

Implementations MUST distinguish between the following states.

### 21.1 Experimental Implementation

Code used for experimentation without production guarantees.

### 21.2 Prototype

A functional demonstration of selected intended behavior.

### 21.3 Test Deployment

A deployment on a test network or another non-production environment.

### 21.4 Pilot

A limited implementation used for public or private validation, demonstration, testing, or learning.

### 21.5 Audit Candidate

A defined version submitted for security or technical review.

### 21.6 Production Candidate

A defined version considered for production deployment but not yet production-active.

### 21.7 Production Deployment

A released deployment intended for production use.

### 21.8 Deprecated Implementation

An implementation no longer applicable or recommended for new use.

A prototype, test deployment, pilot, or audit candidate MUST NOT be presented as active production infrastructure.

---

## 22. Conformance

A component or implementation is conforming only when:

- it identifies an applicable versioned specification;
- it satisfies all applicable normative requirements;
- its actual authority surface is disclosed;
- its implementation status is accurately represented;
- its deployment environment is accurately represented;
- its public interfaces accurately represent behavior;
- material deviations are documented;
- and related specifications are mutually consistent.

A Draft specification MAY guide development, implementation, testing, and review.

A Draft specification MUST NOT be presented as a finalized production guarantee.

---

## 23. Public Communication Requirements

Public technical communication MUST accurately distinguish between:

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
- and Not Deployed.

Public communication MUST NOT:

- present Draft requirements as completed functionality;
- present planned infrastructure as deployed infrastructure;
- present the Base Sepolia pilot as Base Mainnet production;
- imply that a verified contract is necessarily audited;
- imply that publishing a wallet address proves documented use of funds;
- imply that transaction verification proves impact;
- imply that cryptographic anchoring proves factual truth;
- imply decentralization while material authority remains undisclosed;
- describe a review as an audit without a defined audit scope;
- imply guaranteed price, profit, liquidity, listing, completion, or impact;
- imply that a presale is live when it is not;
- or imply legal, charitable, nonprofit, tax-exempt, governmental, or regulatory status without a documented basis.

---

## 24. Change Classification

Changes to specifications MUST be classified according to their effect.

### 24.1 Editorial Change

Corrects:

- grammar;
- spelling;
- formatting;
- broken links;
- or equivalent presentation issues

without changing meaning.

### 24.2 Clarification

Improves precision without materially changing:

- required behavior;
- rights;
- authority;
- constraints;
- or system outcomes.

### 24.3 Non-Breaking Change

Adds compatible detail, definitions, safeguards, or requirements without invalidating previously conforming behavior.

### 24.4 Breaking Change

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
- economic flows;
- staking;
- authority;
- approval requirements;
- governance power;
- upgradeability;
- pause behavior;
- migration;
- evidence requirements;
- privacy boundaries;
- or security assumptions.

### 24.5 Deprecation

Marks a specification or implementation as no longer applicable for new use while preserving it for historical review.

---

## 25. Breaking-Change Requirements

A breaking change requires:

- explicit versioning;
- documented rationale;
- identification of affected requirements;
- security impact analysis;
- governance impact analysis;
- participant-rights analysis;
- economic impact analysis where applicable;
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

## 26. Clarifications

A clarification MUST NOT materially change:

- permissions;
- authorities;
- token supply;
- allocations;
- thresholds;
- timing;
- participant rights;
- economic-flow behavior;
- refund conditions;
- staking behavior;
- evidence standards;
- privacy boundaries;
- or security assumptions.

A change affecting one of these matters is not merely a clarification.

---

## 27. Deprecation

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

## 28. Historical Integrity

Material specification history SHOULD remain reviewable.

This includes:

- released versions;
- breaking changes;
- corrections;
- deprecated documents;
- known deviations;
- implementation mappings;
- and material authority changes.

A materially relevant specification MUST NOT be silently deleted merely because it is:

- outdated;
- unfavorable;
- contradicted by later implementation;
- or reputationally inconvenient.

Where legal, privacy, or security redaction is necessary, the existence and reason category of the change SHOULD remain documented where appropriate.

---

## 29. Review Requirements

Before a specification is marked Stable, it SHOULD be reviewed for:

- technical feasibility;
- security implications;
- governance implications;
- participant-rights implications;
- economic implications;
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

## 30. Contribution Requirements

Contributions to this directory SHOULD:

- preserve the specification-first approach;
- use current glossary terminology;
- identify affected specifications;
- explain authority implications;
- explain security implications;
- explain participant-rights implications;
- explain economic implications where applicable;
- explain compatibility implications;
- distinguish clarifications from breaking changes;
- avoid unsupported implementation claims;
- avoid unsupported deployment claims;
- and include rationale for material changes.

Changes to normative documents SHOULD be submitted through an auditable Git workflow.

---

## 31. Pull Request Expectations

A pull request changing a normative specification SHOULD identify:

- affected document;
- change category;
- reason;
- affected requirements;
- related specifications;
- security implications;
- governance implications;
- participant impact;
- economic impact where applicable;
- implementation impact;
- migration impact where relevant;
- and whether public communication must also change.

Large normative changes SHOULD remain isolated from unrelated edits.

---

## 32. Approval Requirements

The final approval process for Stable specifications remains unresolved.

Before the first Stable release, the project MUST define:

- who may approve specifications;
- required reviewer categories;
- minimum review expectations;
- conflict-of-interest treatment;
- technical review requirements;
- security review requirements;
- legal review requirements where relevant;
- governance review requirements;
- and release authorization.

A document MUST NOT be marked Stable solely because it has existed without objection.

---

## 33. Security

Potential vulnerabilities in specifications or implementations SHOULD be reported according to [`../SECURITY.md`](../SECURITY.md).

Sensitive issues MUST NOT be disclosed through public issues where premature disclosure could place the following at risk:

- users;
- participant funds;
- wallets;
- contracts;
- infrastructure;
- protected evidence;
- credentials;
- or future deployments.

A specification defect may itself be security-relevant where it creates:

- ambiguous authority;
- unsafe custody;
- inconsistent refund rights;
- weak upgrade constraints;
- incomplete invariants;
- hidden administrative power;
- or misleading implementation assumptions.

---

## 34. Privacy

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

## 35. Naming

The current project name is:

**Global Foundation Coin**

The abbreviation is:

**GFC**

The historical name `German Foundation Coin` is deprecated for current project use.

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

## 36. Repository Boundaries

This specification directory is intended for formal architectural, behavioral, economic, governance, security, transparency, and terminology documentation.

It is not intended to contain:

- temporary implementation experiments;
- promotional campaign copy;
- social-media content;
- unsupported token claims;
- undocumented roadmap promises;
- production secrets;
- private keys;
- seed phrases;
- credentials;
- confidential personal information;
- or unsupported legal representations.

Implementation code, deployment records, public interfaces, and operational policies may exist elsewhere but MUST identify their relationship to applicable specifications where relevant.

---

## 37. Future Specification Areas

Additional specifications MAY be introduced where the architecture requires greater precision.

Potential future areas include:

- deployment authentication;
- contract migration;
- governance execution;
- evidence schemas;
- evidence storage;
- registry lifecycle;
- privacy controls;
- incident response;
- operational controls;
- impact methodology;
- external integrations;
- and later accountability-infrastructure components.

These are potential specification areas.

They MUST NOT be treated as existing, finalized, deployed, or committed functionality merely because they are identified here.

---

## 38. Current Unresolved Repository Decisions

The following repository-level matters remain unresolved unless and until separately documented as decided:

- final specification versioning format;
- first specification release identifier;
- final approval process;
- final reviewer roles;
- Stable-status authorization;
- formal change-classification template;
- release-signing process;
- specification-to-code linkage format;
- deployment authentication format;
- known-deviation format;
- deprecation template;
- and long-term archival process.

These matters MUST be resolved before the first production-governing specification release where they are required for reliable release authority.

---

## 39. Requirements Before Stable Status

This index MUST NOT be marked Stable until:

- all applicable specifications are mutually consistent;
- all current specifications use the correct project name;
- document metadata is consistent;
- maturity and authority are separated across all documents;
- project status terminology is consistent with [`../STATUS.md`](../STATUS.md);
- Base Sepolia pilot and Base Mainnet production status are consistently separated;
- token and economic parameters are internally consistent;
- authority definitions are internally consistent;
- security assumptions are internally consistent;
- transparency terminology is internally consistent;
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

## 40. Final Specification Principles

The specification set preserves the following distinctions:

> Normative is not a maturity level.

> Draft does not mean non-normative.

> Draft does not mean deployed.

> Stable does not mean implemented.

> Specified does not mean implemented.

> Implemented does not mean tested.

> Tested does not mean audited.

> Audited does not mean risk-free.

> Deployed does not automatically mean active.

> Live does not automatically mean production.

> Pilot does not mean production.

> Deployed does not mean conforming.

> Actual execution is determined by deployed code and authenticated system state.

> Conformance is determined against the applicable versioned specification.

> A user interface does not override contract behavior.

> An informal statement does not override an applicable versioned specification.

> A wallet label does not technically restrict asset use.

> Transaction verification does not equal use-of-funds verification.

> Use-of-funds verification does not equal outcome verification.

> Outcome verification does not automatically equal impact verification.

> Cryptographic integrity does not equal factual truth.

> A verified contract does not automatically mean an audited contract.

> Testnet deployment does not establish Mainnet deployment.

> Git history alone is not sufficient release or change documentation.

> The `main` branch is not automatically the production source of authority.

> Different claims require different evidence.

The purpose of the specification set is to make intended behavior, economic constraints, authority, rights, security assumptions, evidence requirements, limitations, and change history reviewable before production reliance.

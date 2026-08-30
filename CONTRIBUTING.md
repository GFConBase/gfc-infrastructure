# Contributing to the GFC Infrastructure Repository

**Document:** CONTRIBUTING.md  
**Status:** Informative contribution guidance  
**Repository Stage:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Last Updated:** 2026-08-30

---

## 1. Purpose

This document defines the current contribution guidance for the Global Foundation Coin (GFC) infrastructure repository.

The repository follows a specification-first, security-aware, and accountability-oriented development approach.

Contributions should improve:

- clarity;
- internal consistency;
- implementation accuracy;
- participant protection;
- authority constraints;
- economic consistency;
- security;
- evidence quality;
- historical accountability;
- and long-term maintainability.

Promotional strength, speed, convenience, or apparent completeness should not take priority over accuracy.

This document is informative guidance.

It does not independently establish:

- a mandatory branch-protection model;
- a mandatory pull-request approval threshold;
- a maintainer hierarchy;
- a signer hierarchy;
- production authority;
- release authority;
- or a formal governance process not established elsewhere.

---

## 2. Current Repository Context

The current primary product focus is:

**GFC Token / Economic Layer**

The long-term direction is broader:

**Accountability Infrastructure**

based on the canonical model:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

The repository is currently in:

**Pre-mainnet specification and pilot development**

A public Base Sepolia pilot exists:

```text
Network: Base Sepolia
Chain ID: 84532
Token: tGFC
Contract: 0x7262Cca91938ede6bB6560F81104Aa410848e7f3
Status: Public Pilot / Non-Production
Source: Verified
```

No official production GFC token is currently deployed on Base Mainnet.

No GFC presale is currently live.

Contributions must preserve the distinction between Pilot and Production.

---

## 3. Repository Scope

This repository is intended for:

- formal specifications;
- architecture documentation;
- token requirements;
- allocation requirements;
- vesting and unlock requirements;
- economic-flow requirements;
- staking requirements;
- presale requirements;
- authority and governance constraints;
- security models and security policy;
- transparency and evidence requirements;
- shared terminology;
- deployment records;
- project-status records;
- roadmap records;
- project decision records;
- contribution guidance;
- and change history.

This repository is not intended for:

- social-media content;
- promotional campaign copy;
- hype-driven messaging;
- price predictions;
- guaranteed-return claims;
- guaranteed-impact claims;
- unsupported launch promises;
- undocumented roadmap promises;
- private operational information;
- credentials;
- private keys;
- seed phrases;
- signing secrets;
- personal beneficiary information;
- unredacted personal data;
- or unsupported legal or regulatory representations.

---

## 4. Source-of-Truth Hierarchy

Contributors should respect the role of each repository document.

### 4.1 Normative specifications

Files under [`specs/`](specs/) define normative technical and system requirements where their metadata declares `Authority: Normative`.

### 4.2 Current status

[`STATUS.md`](STATUS.md) records current project and implementation status.

### 4.3 Deployment records

[`DEPLOYMENTS.md`](DEPLOYMENTS.md) records authenticated or established deployment state.

### 4.4 Current project decisions

[`DECISIONS.md`](DECISIONS.md) records current canonical working decisions, constraints, historical facts, and open decisions.

### 4.5 Planned sequencing

[`ROADMAP.md`](ROADMAP.md) records intended development sequencing.

### 4.6 Security policy

[`SECURITY.md`](SECURITY.md) defines security-reporting and coordinated-disclosure guidance.

### 4.7 Repository history

[`CHANGELOG.md`](CHANGELOG.md) records material repository changes over time.

Contributors should avoid creating a second independent source of truth for a requirement that already has a primary owner.

---

## 5. Contribution Principles

Contributions should preserve the following priorities:

1. **Accuracy before promotional strength.**
2. **Specifications before production reliance.**
3. **Explicit authority before implied authority.**
4. **Constraints before hidden discretion.**
5. **Participant rights before operational convenience.**
6. **Evidence before claims.**
7. **Privacy-aware transparency.**
8. **Historical accountability before silent rewriting.**
9. **One primary normative owner per requirement.**
10. **Pilot and Production separation.**
11. **Open decisions remain open until explicitly decided.**
12. **Clarity before speed.**

---

## 6. Status Terminology

Contributions should use status terminology consistently with [`specs/glossary.md`](specs/glossary.md).

Relevant terms include:

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

These terms are not interchangeable.

In particular:

> Draft does not mean deployed.

> Implemented does not mean tested.

> Tested does not mean audited.

> Source Verified does not mean audited.

> Pilot does not mean production.

> Deployed does not automatically mean operational.

---

## 7. Before Proposing a Change

Before proposing a material change, a contributor should:

1. identify the document that owns the relevant requirement;
2. review related definitions in [`specs/glossary.md`](specs/glossary.md);
3. review intentional exclusions in [`specs/non-goals.md`](specs/non-goals.md);
4. review applicable current decisions in [`DECISIONS.md`](DECISIONS.md);
5. check current status in [`STATUS.md`](STATUS.md);
6. check actual deployment state in [`DEPLOYMENTS.md`](DEPLOYMENTS.md);
7. identify affected architecture, security, authority, economic, participant-rights, and transparency assumptions;
8. determine whether the proposed change is informative or normative;
9. determine whether the change is breaking;
10. identify cross-document references that may need review;
11. distinguish unresolved questions from proposed answers;
12. and keep unrelated changes separate where practical.

A requirement should normally have one primary normative owner.

Other documents should reference that owner rather than maintaining competing copies of the same rule.

---

## 8. Change Categories

Material changes should be classified by their primary effect.

### 8.1 Editorial

Editorial changes include:

- spelling corrections;
- grammar corrections;
- formatting improvements;
- link corrections;
- and wording changes that do not alter meaning.

Editorial changes must not silently alter normative behavior.

### 8.2 Informative

Informative changes include:

- explanations;
- examples;
- navigation;
- diagrams;
- contextual notes;
- non-binding summaries;
- and historical clarification.

Informative content must not contradict applicable normative requirements.

### 8.3 Normative Non-Breaking

Normative non-breaking changes may include:

- clarification of an existing requirement;
- formalization of an already adopted invariant;
- removal of ambiguity without changing participant rights;
- or addition of a constraint already implied by the current canonical design.

A change is not automatically non-breaking merely because no production implementation exists yet.

### 8.4 Normative Breaking

Normative breaking changes include changes to material properties such as:

- token supply;
- token standard;
- token fees;
- allocation amounts;
- allocation percentages;
- Impact Vault restrictions;
- Core Team vesting;
- Presale price;
- Presale duration;
- soft cap;
- supported payment assets;
- Presale token-delivery model;
- refund rights;
- custody;
- staking inflation model;
- governance authority;
- upgrade authority;
- pause authority;
- migration authority;
- evidence standards;
- Registry status meaning;
- privacy requirements;
- or security assumptions.

Breaking changes require explicit impact analysis and versioning treatment.

### 8.5 Security-Sensitive

Security-sensitive changes include:

- vulnerability information;
- threat-model changes;
- privileged-control changes;
- custody changes;
- signer changes;
- emergency authority;
- migration authority;
- recovery authority;
- sensitive incident information;
- and changes affecting participant assets or protected information.

Potential vulnerabilities must be handled according to [`SECURITY.md`](SECURITY.md).

### 8.6 Deprecation

Deprecation changes identify:

- terminology;
- behavior;
- components;
- documents;
- or assumptions

that remain historically relevant but are no longer current for new implementation.

Deprecation should preserve relevant historical context.

---

## 9. Normative Language

Normative specifications use uppercase requirement terms where applicable:

- **MUST**
- **MUST NOT**
- **SHOULD**
- **SHOULD NOT**
- **MAY**

Lowercase uses of `must`, `should`, or `may` should not accidentally create ambiguity about normative intent.

When editing a normative specification, contributors should preserve the normative-language convention defined in [`specs/README.md`](specs/README.md).

---

## 10. Contribution Workflow

A dedicated branch and pull request are recommended for material repository changes because they improve:

- reviewability;
- attribution;
- discussion;
- historical traceability;
- and change isolation.

However, this document does not establish a mandatory branch or pull-request workflow unless separately adopted by repository governance.

Where a pull request is used, it should represent one coherent change where practical.

Large normative changes should preferably remain separate from:

- unrelated formatting;
- unrelated editorial cleanup;
- naming-only changes;
- dependency changes;
- and repository restructuring.

The repository should not claim a review or approval process that has not actually been adopted.

---

## 11. Suggested Pull-Request Information

Where a pull request is used for a material change, it should identify, where relevant:

- affected document or documents;
- change category;
- whether the change is informative or normative;
- rationale;
- affected requirements;
- affected definitions;
- current decision being preserved or changed;
- security implications;
- governance implications;
- participant-rights implications;
- economic implications;
- implementation implications;
- migration implications;
- backward-compatibility implications;
- affected public statements;
- affected status records;
- required testing or review;
- and whether the change is breaking.

Where a material category has no impact, stating `None` or `Not applicable` can improve reviewability.

---

## 12. Normative Change Requirements

A normative change should:

- use precise language;
- be testable where technically applicable;
- identify the responsible component or authority;
- define prohibited behavior where relevant;
- define participant rights where relevant;
- define failure behavior where relevant;
- avoid undocumented administrative discretion;
- identify unresolved dependencies;
- distinguish technical enforcement from governance or operational enforcement;
- remain consistent with applicable decisions;
- and remain consistent with the rest of the specification set.

A normative requirement must not depend solely on:

- a document title;
- an allocation name;
- a marketing statement;
- an informal promise;
- an unauthenticated wallet label;
- an unspecified future implementation;
- or a roadmap date.

---

## 13. Breaking Changes

A breaking change should include:

- explicit classification as breaking;
- previous requirement;
- proposed requirement;
- rationale;
- participant-rights impact;
- security impact;
- governance impact;
- economic impact;
- implementation impact;
- migration impact where applicable;
- public-communication impact;
- and versioning implications.

A breaking change must not be hidden inside an editorial or restructuring change.

Where the breaking change reverses a current canonical decision, [`DECISIONS.md`](DECISIONS.md) should be updated as part of the same logical change set or through an explicitly linked decision change.

---

## 14. Decision Changes

A contributor proposing a change to a canonical working decision should identify:

- the existing decision;
- proposed replacement;
- rationale;
- affected specifications;
- affected deployments;
- affected roadmap assumptions;
- security implications;
- participant-rights implications;
- and migration requirements where applicable.

A canonical decision must not be silently reversed by editing only one downstream specification.

Material decision changes should remain historically reviewable.

---

## 15. Open Decisions

Open decisions should remain explicitly labeled as unresolved until a decision has actually been made.

Contributors must not fill a gap merely to make a specification appear complete.

Examples of currently unresolved areas include:

- final production token architecture;
- final sell-fee destination;
- final staking reward source;
- final Presale pricing architecture;
- treatment of already distributed Presale GFC after failed finalization;
- unsold Presale GFC treatment;
- final production governance structure;
- final production custody structure;
- and final Transparency Registry architecture.

If a contribution proposes a resolution, it should be presented as a proposed decision rather than silently inserted as established fact.

---

## 16. Pilot and Production Changes

Any contribution affecting the Base Sepolia pilot should preserve the distinction between:

- pilot behavior;
- pilot deployment;
- pilot authority;
- production design;
- and future Base Mainnet deployment.

The current authenticated pilot is:

```text
Network: Base Sepolia
Chain ID: 84532
Token: tGFC
Contract: 0x7262Cca91938ede6bB6560F81104Aa410848e7f3
Status: Public Pilot / Non-Production
Source: Verified
```

A change to pilot documentation must not imply that:

- production GFC exists;
- production Presale exists;
- pilot authority becomes production authority;
- or future production implementation must reuse pilot code.

---

## 17. Token Changes

Changes affecting [`specs/token.md`](specs/token.md) should preserve or explicitly address:

- fixed supply of 1,000,000,000 GFC;
- ERC-20-compatible intended production design;
- 18 decimals;
- Base Mainnet as intended initial production network;
- 0% intended buy fee;
- 1% intended sell fee;
- no hidden inflation;
- explicit privileged authority;
- and Pilot-versus-Production separation.

A proposal to alter any of these properties is material and may be breaking.

---

## 18. Allocation Changes

Changes affecting [`specs/allocations.md`](specs/allocations.md) must reconcile to the fixed supply.

Current Draft allocations are:

| Allocation | Share | Token Amount |
|---|---:|---:|
| Impact Vault | 25% | 250,000,000 GFC |
| Guardian Growth | 20% | 200,000,000 GFC |
| Presale | 15% | 150,000,000 GFC |
| Treasury Reserve | 15% | 150,000,000 GFC |
| Liquidity Reserve | 15% | 150,000,000 GFC |
| Ecosystem | 5% | 50,000,000 GFC |
| Core Team | 5% | 50,000,000 GFC |

A contribution must not introduce an eighth hidden allocation or duplicate allocation capacity.

---

## 19. Vesting and Lock Changes

Changes affecting [`specs/vesting-and-unlocks.md`](specs/vesting-and-unlocks.md) should preserve the current intended constraints unless explicitly proposing a breaking change:

### Impact Vault

```text
250,000,000 GFC
50-year intended lock
```

### Core Team

```text
50,000,000 GFC
19-year intended linear vesting
```

Unknown start timestamps, cliffs, beneficiaries, post-lock behavior, or recovery mechanics must not be invented.

---

## 20. Presale Changes

Changes affecting [`specs/presale.md`](specs/presale.md) must reflect the current Draft direction:

- €0.05 reference price;
- eight-week intended duration;
- €250,000 soft cap;
- no separate monetary hard cap;
- 150,000,000 GFC Presale allocation;
- intended ETH, USDC, and DAI support on Base;
- immediate GFC distribution;
- refund rights if the applicable success condition is not satisfied;
- and immutable material participant-facing logic as the current direction.

The previous deferred-claim model is deprecated.

The interaction between immediate distribution and failed-sale refunds remains unresolved and is a production blocker.

Contributors must not invent a:

- clawback;
- forced burn;
- forced transfer;
- mandatory token return;
- token invalidation;
- blacklist solution;
- or replacement-token solution

without an explicit project decision and full security, economic, governance, and participant-rights analysis.

---

## 21. Staking Changes

Changes affecting [`specs/staking.md`](specs/staking.md) must preserve the current design direction:

**hybrid and non-inflationary**

No contribution should assume a final:

- reward source;
- APR;
- APY;
- reward duration;
- lock period;
- governance right;
- or reward pool

unless the project has explicitly decided it.

Staking must not introduce GFC inflation under the current fixed-supply model.

---

## 22. Transparency Registry Changes

Changes affecting [`specs/transparency-model.md`](specs/transparency-model.md) should preserve the principle that the future Transparency Registry is:

**versioned history, not a permanent approval badge**

Registry inclusion must not automatically mean:

- permanent approval;
- permanent verification;
- permanent endorsement;
- or perpetual evidence validity.

A Registry change should preserve historical reviewability for:

- verification status;
- downgrade;
- suspension;
- correction;
- dispute;
- removal from current presentation;
- and supersession

where legally and technically appropriate.

---

## 23. Security Reporting

Potential vulnerabilities must not be disclosed through public repository channels where premature disclosure could place at risk:

- participant funds;
- private information;
- signing infrastructure;
- pilot systems;
- future production deployments;
- production systems;
- or third-party systems.

Follow [`SECURITY.md`](SECURITY.md).

The current private security contact is:

```text
info@globalfoundationcoin.org
```

This repository must never contain:

- private keys;
- seed phrases;
- passwords;
- API secrets;
- access tokens;
- signing secrets;
- production credentials;
- unredacted sensitive personal data;
- or confidential vulnerability details intended for private disclosure.

---

## 24. Cross-Document Consistency

When a primary requirement changes, all affected references should be reviewed.

Potentially affected documents include:

- [`README.md`](README.md);
- [`STATUS.md`](STATUS.md);
- [`DEPLOYMENTS.md`](DEPLOYMENTS.md);
- [`ROADMAP.md`](ROADMAP.md);
- [`DECISIONS.md`](DECISIONS.md);
- [`SECURITY.md`](SECURITY.md);
- [`CHANGELOG.md`](CHANGELOG.md);
- [`specs/README.md`](specs/README.md);
- [`specs/glossary.md`](specs/glossary.md);
- [`specs/non-goals.md`](specs/non-goals.md);
- [`specs/architecture.md`](specs/architecture.md);
- [`specs/roles-and-authority.md`](specs/roles-and-authority.md);
- [`specs/governance-constraints.md`](specs/governance-constraints.md);
- [`specs/security-model.md`](specs/security-model.md);
- [`specs/token.md`](specs/token.md);
- [`specs/allocations.md`](specs/allocations.md);
- [`specs/vesting-and-unlocks.md`](specs/vesting-and-unlocks.md);
- [`specs/economic-flows.md`](specs/economic-flows.md);
- [`specs/staking.md`](specs/staking.md);
- [`specs/presale.md`](specs/presale.md);
- and [`specs/transparency-model.md`](specs/transparency-model.md).

Duplicated normative requirements should be minimized.

---

## 25. Specification Maturity

Specification maturity and authority are defined in [`specs/README.md`](specs/README.md).

A merged or accepted document must not automatically be treated as:

- Stable;
- implemented;
- tested;
- reviewed;
- audited;
- deployed;
- live;
- active;
- operational;
- or independently verified.

Until a formal Stable-approval process is adopted, editing or merging a Draft specification does not independently change its maturity.

---

## 26. Stable Approval

A specification should not be designated Stable unless:

- scope is defined;
- normative requirements are internally consistent;
- relevant terminology is defined;
- material unresolved questions are resolved or explicitly excluded;
- participant rights are defined where applicable;
- authority is defined where applicable;
- security implications have been reviewed;
- implementation dependencies are known;
- migration implications are addressed where relevant;
- and approval is recorded through a reviewable process.

Stable status does not independently prove:

- implementation;
- testing;
- audit completion;
- deployment;
- legal approval;
- regulatory approval;
- or operational availability.

---

## 27. Implementation Mapping

A future production implementation should identify:

- applicable specification release;
- applicable source release or commit;
- implemented requirements;
- unimplemented requirements;
- known deviations;
- deployment addresses;
- administrative authority;
- upgradeability;
- pause authority;
- migration authority;
- testing status;
- security-review status;
- audit status;
- and activation status.

Source code must not be described as conforming merely because it exists in the same repository as a specification.

---

## 28. Deployment Records

A contribution that changes actual deployment state should also review [`DEPLOYMENTS.md`](DEPLOYMENTS.md).

Deployment records should describe authenticated actual state.

They should not be used to document speculative future architecture.

Unknown deployment details must remain unknown until authenticated.

They must not be guessed for completeness.

---

## 29. Status Records

A change that materially alters current project or implementation state should review [`STATUS.md`](STATUS.md).

Examples include:

- new pilot deployment;
- production deployment;
- Presale activation;
- security review completion;
- audit completion;
- migration;
- retirement;
- or production feature activation.

Status must reflect evidence, not intention.

---

## 30. Decision Records

A contribution that changes a current project decision should review [`DECISIONS.md`](DECISIONS.md).

Examples include changes to:

- product focus;
- supply;
- allocations;
- network;
- fee model;
- Presale mechanics;
- staking model;
- governance constraints;
- or Registry philosophy.

An implementation convenience should not silently become a project decision.

---

## 31. Roadmap Records

A contribution that changes intended sequencing should review [`ROADMAP.md`](ROADMAP.md).

Roadmap edits should distinguish:

- target period;
- readiness gate;
- current status;
- and dependency.

A roadmap date must not be presented as proof that a feature is ready or deployed.

---

## 32. Commit Messages

Where Git commits are used, commit messages should be:

- concise;
- descriptive;
- understandable without private context;
- and scoped to the actual change.

Examples:

```text
Add canonical allocation specification
```

```text
Replace deferred presale claims with immediate distribution
```

```text
Document Base Sepolia pilot deployment
```

```text
Clarify staking reward-source requirement
```

```text
Add versioned transparency registry model
```

Commit style is recommended guidance, not a security or conformance requirement.

---

## 33. Testing and Validation

A documentation-only change may still require technical review where it alters normative behavior.

Where a contribution affects implementation, validation should be appropriate to the affected component.

Potential validation may include:

- unit tests;
- integration tests;
- invariant tests;
- fuzz tests;
- deployment simulations;
- permission tests;
- accounting reconciliation;
- migration tests;
- and security review.

A passing test does not independently establish audit status.

---

## 34. Review Outcomes

A contribution may be:

- accepted;
- accepted with revisions;
- deferred pending dependencies;
- rejected as inconsistent with current requirements;
- rejected as insufficiently specified;
- rejected as outside repository scope;
- superseded by another proposal;
- or redirected to a different document.

This list is descriptive guidance.

It does not establish a formal maintainer voting or approval system.

Material decision history should remain attributable and reviewable where practical.

---

## 35. No Retrospective Normalization

Specifications, deployment records, status records, decision records, and change history must not be altered after an event merely to make unauthorized, misleading, or non-conforming behavior appear compliant.

A material correction should identify, where appropriate:

- what was incorrect;
- what changed;
- why it changed;
- when it changed;
- and which prior statements, decisions, records, or requirements were affected.

Historical accountability should be preserved without exposing protected or security-sensitive information.

---

## 36. Change History

Material repository-level changes should be reflected in [`CHANGELOG.md`](CHANGELOG.md).

Git history provides technical revision history.

Git history alone is not a replacement for:

- versioned releases;
- deployment records;
- migration records;
- decision records;
- known-deviation records;
- implementation mappings;
- incident records;
- or formal deprecation notices.

---

## 37. Contribution Non-Goals

Contribution process guidance does not aim to:

- create bureaucracy for minor edits;
- create fictitious decentralization;
- create a governance process that does not exist;
- require a particular Git platform workflow forever;
- guarantee acceptance of a contribution;
- grant production authority to a contributor;
- grant security-testing authorization;
- create intellectual-property rights beyond applicable repository terms;
- or turn open questions into decisions merely because a contributor proposes an answer.

---

## 38. Final Contribution Principles

Contributions to the GFC repository should preserve the following distinctions:

> A contribution is not a project decision until adopted.

> A project decision is not a production deployment.

> A merged Draft is not automatically Stable.

> Source code in the repository is not automatically production code.

> Pilot behavior is not production behavior.

> A roadmap date is not a launch guarantee.

> An allocation label is not technical custody.

> A wallet label is not authority.

> Source verification is not an audit.

> Open decisions must remain open until explicitly resolved.

> Security-sensitive information belongs in the private reporting process.

> Historical accountability is preferable to silent rewriting.

The repository should evolve through explicit, reviewable changes while preserving consistency among **Funds, Authority, Rules, Decisions, Outcomes, and Evidence**.

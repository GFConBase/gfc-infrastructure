# Contributing to the GFC Infrastructure Specifications

This document defines the current contribution and change process for the Global Foundation Coin (GFC) infrastructure repository.

The repository follows a specification-first and transparency-first development approach.

Contributions should improve:

- clarity;
- internal consistency;
- participant protection;
- authority constraints;
- implementation accuracy;
- evidence quality;
- historical accountability;
- security;
- and long-term maintainability.

Promotional strength, speed, or convenience must not take priority over these objectives.

---

## Repository Scope

This repository is intended for:

- formal specifications;
- architecture documentation;
- token requirements;
- allocation requirements;
- governance constraints;
- presale requirements;
- transparency and evidence requirements;
- shared terminology;
- security reporting guidance;
- contribution guidance;
- implementation-status records;
- and version history.

This repository is not intended for:

- social-media content;
- promotional campaign copy;
- hype-driven messaging;
- price predictions;
- guaranteed-return claims;
- undocumented roadmap promises;
- private operational information;
- credentials;
- private keys;
- seed phrases;
- signing secrets;
- personal beneficiary information;
- unredacted personal data;
- or unsupported legal representations.

---

## Contribution Principles

Contributions should preserve the following priorities:

1. Specifications before implementation.
2. Explicit authority before implied authority.
3. Constraints before discretion.
4. Participant rights before operational convenience.
5. Evidence before claims.
6. Privacy-aware transparency.
7. Accuracy before promotional strength.
8. Historical accountability before retrospective correction.
9. Clear document ownership before duplicated requirements.
10. Clarity before speed.

---

## Before Submitting a Change

Before creating a pull request:

1. Identify the document that owns the relevant requirement.
2. Check whether the same requirement is repeated elsewhere.
3. Review relevant terminology in [`specs/glossary.md`](specs/glossary.md).
4. Review intentional exclusions in [`specs/non-goals.md`](specs/non-goals.md).
5. Identify affected architecture, governance, security, participant-rights, and implementation assumptions.
6. Determine whether the change is informative or normative.
7. Determine whether the change is breaking.
8. Determine whether public communication or implementation status must also change.
9. Keep unrelated changes separate.

A requirement should have one primary normative owner.

Other documents should reference that owner rather than maintaining independent and potentially conflicting versions of the same requirement.

---

## Change Categories

Every material pull request should identify one primary change category.

### Editorial

Editorial changes include:

- spelling corrections;
- grammar corrections;
- formatting improvements;
- link corrections;
- and wording changes that do not alter meaning.

Editorial changes must not silently change normative behavior.

### Informative

Informative changes include:

- explanations;
- examples;
- diagrams;
- contextual notes;
- non-binding summaries;
- and navigation improvements.

Informative content must not contradict normative requirements.

### Normative Non-Breaking

Normative non-breaking changes include:

- clarification of an existing requirement;
- addition of a constraint consistent with the current design;
- correction of an ambiguity without changing participant rights;
- and formalization of an already intended invariant.

A change must not be classified as non-breaking merely because no implementation currently exists.

### Normative Breaking

Normative breaking changes include changes to:

- token supply;
- token fees;
- allocation amounts;
- allocation percentages;
- locks;
- vesting;
- participant rights;
- presale pricing;
- soft-cap conditions;
- refunds;
- claim rights;
- custody;
- governance authority;
- upgrade authority;
- pause authority;
- migration authority;
- evidence standards;
- privacy requirements;
- or security assumptions.

Breaking changes require explicit impact documentation and versioning.

### Security-Sensitive

Security-sensitive changes include:

- vulnerability information;
- threat-model changes;
- administrative-control changes;
- signer changes;
- custody changes;
- emergency authority;
- disclosure of exploitable implementation details;
- and changes that may affect participant funds or protected information.

Sensitive vulnerability information must be handled according to [`SECURITY.md`](SECURITY.md).

### Deprecation

Deprecation changes identify requirements, terminology, components, or documents that are retained for historical reference but are no longer intended for new implementations.

Deprecation must not erase relevant historical context.

---

## Branch and Pull-Request Requirements

Material changes should be submitted through a dedicated branch and pull request.

Large normative changes should remain isolated from:

- formatting changes;
- unrelated editorial changes;
- dependency updates;
- naming changes;
- and repository restructuring.

A pull request should be reviewable as one coherent decision.

Where practical, separate commits should be used for:

- new documents;
- content migration;
- normative changes;
- editorial cleanup;
- link updates;
- and changelog updates.

---

## Required Pull-Request Information

A material pull request should identify:

- affected document or documents;
- change category;
- whether the change is informative or normative;
- rationale;
- affected requirements;
- affected definitions;
- security implications;
- governance implications;
- participant-rights implications;
- implementation implications;
- migration implications;
- backward-compatibility implications;
- affected public statements;
- affected status records;
- required tests or review;
- and whether the change is breaking.

Where no implication exists, the pull request should state that explicitly rather than omitting the category without explanation.

---

## Normative Change Requirements

A normative change should:

- use precise and testable language;
- identify the responsible component or authority;
- define prohibited behavior where relevant;
- define participant rights where relevant;
- define failure behavior where relevant;
- avoid undocumented administrative discretion;
- identify unresolved dependencies;
- identify whether enforcement is technical, governance-based, contractual, or operational;
- and remain consistent with the rest of the specification set.

A normative requirement must not depend solely on:

- a document title;
- an allocation name;
- a marketing statement;
- an informal promise;
- an unauthenticated wallet label;
- or an unspecified future implementation.

---

## Breaking Changes

A breaking change requires:

- explicit classification as breaking;
- a clear explanation of the previous requirement;
- a clear explanation of the proposed requirement;
- participant-rights impact analysis;
- security impact analysis;
- governance impact analysis;
- migration analysis where applicable;
- implementation impact analysis;
- public-communication impact analysis;
- and an appropriate version change.

A breaking change must not be hidden inside an editorial or restructuring pull request.

---

## Cross-Document Consistency

When a primary requirement changes, all affected references should be reviewed.

Potentially affected documents include:

- [`README.md`](README.md);
- [`STATUS.md`](STATUS.md);
- [`specs/README.md`](specs/README.md);
- [`specs/glossary.md`](specs/glossary.md);
- [`specs/non-goals.md`](specs/non-goals.md);
- [`specs/architecture.md`](specs/architecture.md);
- [`specs/token.md`](specs/token.md);
- [`specs/allocations.md`](specs/allocations.md);
- [`specs/governance-constraints.md`](specs/governance-constraints.md);
- [`specs/transparency-model.md`](specs/transparency-model.md);
- [`specs/presale.md`](specs/presale.md);
- [`SECURITY.md`](SECURITY.md);
- and [`CHANGELOG.md`](CHANGELOG.md).

Duplicated normative requirements should be removed or replaced with references to the primary owning document.

---

## Specification Maturity

Specification maturity and authority are defined in [`specs/README.md`](specs/README.md).

A merged document must not automatically be treated as:

- Stable;
- implemented;
- tested;
- reviewed;
- audited;
- deployed;
- active;
- operational;
- or independently verified.

Until a formal Stable-approval process is adopted, merging a Draft specification does not independently change its maturity.

---

## Stable Approval

A specification should not be designated as Stable unless:

- its scope is defined;
- its normative requirements are internally consistent;
- relevant terminology is defined;
- material unresolved questions are closed or explicitly excluded;
- participant rights are defined where applicable;
- authority and control surfaces are documented;
- security implications have been reviewed;
- implementation dependencies are identified;
- versioning implications are addressed;
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

## Implementation Mapping

A future production implementation should identify:

- the applicable specification release;
- the applicable source-code release or commit;
- implemented requirements;
- unimplemented requirements;
- known deviations;
- deployment addresses;
- administrative authority;
- upgradeability;
- pause authority;
- migration authority;
- testing status;
- audit status;
- and activation status.

Source code should not be described as conforming merely because it is stored in the same repository as a specification.

---

## Security Reporting

Potential vulnerabilities must not be disclosed through public issues where premature disclosure could place at risk:

- participant funds;
- private information;
- signing infrastructure;
- future deployments;
- production systems;
- or third-party systems.

Follow [`SECURITY.md`](SECURITY.md) for security reporting.

This repository must never contain:

- private keys;
- seed phrases;
- credentials;
- API secrets;
- signing secrets;
- unredacted personal data;
- production secrets;
- or confidential vulnerability details intended for private disclosure.

---

## Commit Messages

Commit messages should be:

- concise;
- descriptive;
- written in the imperative form;
- limited to one coherent change;
- and understandable without relying on private context.

Examples:

```text
Add normative token specification
```

```text
Clarify presale refund eligibility
```

```text
Separate allocation rules from token specification
```

```text
Document governance migration constraints
```

The extended commit description should explain:

- what changed;
- why it changed;
- which documents are affected;
- and whether behavior or only documentation structure changed.

---

## Change History

Material repository-level changes should be recorded in [`CHANGELOG.md`](CHANGELOG.md).

Git history provides technical revision history.

Git history alone is not a replacement for:

- versioned releases;
- migration records;
- known-deviation records;
- implementation mappings;
- incident records;
- or formal deprecation notices.

---

## Review Outcomes

A contribution may be:

- accepted;
- accepted with requested revisions;
- deferred pending dependencies;
- rejected as inconsistent with current requirements;
- rejected as insufficiently specified;
- rejected as outside repository scope;
- or redirected to a different document.

Rejection of a proposal does not require deletion of its review history.

Material decisions should remain attributable and historically reviewable.

---

## No Retrospective Normalization

Specifications, status records, and change history must not be altered after an event merely to make unauthorized, misleading, or non-conforming behavior appear compliant.

Corrections should identify:

- what was incorrect;
- what changed;
- why it changed;
- when it changed;
- and which previous statements or requirements were affected.

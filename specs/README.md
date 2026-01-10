# Specifications
**Status:** Normative

This directory contains the formal specifications governing the core components of the GFC infrastructure.

Specifications are intentionally published prior to implementation.
They define intended behavior, constraints, invariants, and system boundaries — not technical optimizations or implementation details.

All on-chain contracts, off-chain processes, and user-facing interfaces **must** conform to the applicable specifications in this directory, according to their declared status.

## Purpose
The purpose of this specification set is to ensure:
- verifiable and predictable fund flows,
- long-term governance integrity,
- clear accountability and auditability,
- elimination of implicit or undocumented assumptions.

Specifications are designed to be readable by developers, auditors, reviewers, and non-technical stakeholders alike.

## Normative Language
The key words **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT**, and **MAY** in this repository are to be interpreted as described in RFC 2119.

Where normative language is used, the specification is binding for any implementation.

## Specification Scope
Planned and existing specifications include:
- vesting and lock mechanisms,
- charity and foundation fund flows,
- governance constraints and safeguards,
- presale and token distribution logic,
- transparency and verification models.

Each specification explicitly defines its own scope and non-goals.

## Specification Status
Each specification falls into one of the following categories:

### Draft
Subject to change. Used for discussion and refinement.

### Stable
Feature-complete and expected to be implemented as written.
Changes require strong justification and explicit versioning.

### Normative
Binding specification.
Implementations **must** adhere exactly.
Breaking changes are avoided by design and require a major version update.

The status of each document is declared at the top of the file.

## Reading Order (Recommended)
For first-time readers and reviewers:
1. `glossary.md`
2. `non-goals.md`
3. `governance-constraints.md`
4. `transparency-model.md`
5. `presale.md`

Additional specifications build on these foundations.

## Single Source of Truth
This directory represents the single source of truth for the intended behavior of the GFC infrastructure.

Public statements, UI behavior, documentation, and implementations must not contradict these specifications.
In case of ambiguity, the written specification takes precedence.

## Change Policy
Non-breaking clarifications **may** be applied to Stable specifications.
Breaking changes require explicit versioning and documentation.

Normative specifications are changed only in exceptional cases.
All changes are tracked via Git history and pull requests.


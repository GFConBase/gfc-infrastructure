# Security Policy
**Status:** Stable

## Scope
This repository defines specifications and reference documentation for the GFC (German Foundation Coin) infrastructure.

At this stage, the repository primarily contains specifications, not production contract implementations.

Security considerations therefore focus on:
- correctness and clarity of specifications,
- prevention of unsafe or misleading design assumptions,
- responsible handling of potential vulnerabilities in future implementations.

## Supported Versions
As long as this repository contains specifications only, there are no “supported” or “unsupported” software versions in the traditional sense.

Once contract implementations are introduced, supported versions and security guarantees will be documented explicitly.

## Reporting a Vulnerability
If you believe you have identified a security issue, vulnerability, or design flaw that could affect the GFC infrastructure:

- Do not open a public GitHub issue.
- Do not disclose the issue publicly before coordination.

Instead, report the issue responsibly via one of the following channels:

**Email:** security@germanfoundationcoin.org  
*(replace with the final security contact address if different)*

Reports should include, where possible:
- a clear description of the issue,
- affected specifications or components,
- potential impact and assumptions,
- any suggested mitigations.

## Disclosure Process
All security reports are handled according to the following principles:
- issues are reviewed and triaged in a timely manner,
- valid issues are documented and addressed in a transparent way,
- disclosure timing is coordinated to avoid unnecessary risk.

Where appropriate, resolved issues and mitigations may be documented publicly after fixes or clarifications have been applied.

## Design-Level Security Considerations
Security in the GFC infrastructure is treated as a **design-level concern**, not only an implementation problem.

Key principles include:
- explicit authority boundaries,
- constrained upgrade and admin scopes,
- avoidance of implicit or undocumented control paths,
- preference for verifiable and auditable mechanisms over discretionary ones.

These principles are reflected throughout the specifications in this repository.

## Limitations
This security policy does not constitute a guarantee of correctness or safety.

Specifications define intended behavior and constraints, but do not replace:
- independent audits,
- formal verification,
- careful implementation and testing.

Security is treated as an ongoing responsibility, not a one-time checklist.

## Status Notes
This document defines the initial security and disclosure policy for the GFC infrastructure repository.

It may evolve over time, but changes will be documented and versioned.


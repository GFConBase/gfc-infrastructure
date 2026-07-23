# Global Foundation Coin Security Policy

**Document ID:** GFC-SEC-001  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-deployment  
**Last Updated:** 2026-07-23

---

## 1. Document Status

This document defines the current security-reporting, vulnerability-handling, coordinated-disclosure, and security-governance policy for the Global Foundation Coin (GFC) repository.

It is normative because it establishes:

- how suspected vulnerabilities must be reported;
- which issues are security-relevant;
- how sensitive reports are handled;
- which testing activities are prohibited;
- how disclosure should be coordinated;
- and which security requirements must be completed before production deployment.

Its maturity remains Draft.

At the time of publication:

- no production GFC token contract is represented by this repository as deployed;
- no GFC presale is live;
- no production treasury, governance, staking, vesting, evidence, or transparency system is represented as operational;
- no production contract or wallet address is established as official by this policy;
- no formal bug-bounty program is active;
- no guaranteed vulnerability-response service level is established;
- and no production software version is currently declared supported.

Security-relevant issues may nevertheless exist within:

- specifications;
- repository configuration;
- documentation;
- release processes;
- future implementation assumptions;
- authority models;
- custody designs;
- and public security representations.

---

## 2. Purpose

The purpose of this policy is to provide a responsible process for reporting and addressing security issues that could affect GFC.

The policy is intended to:

- reduce the risk of premature public disclosure;
- protect future participants and infrastructure;
- identify unsafe specification assumptions before implementation;
- prevent ambiguous or undocumented authority;
- preserve participant rights;
- protect confidential and personal information;
- support coordinated remediation;
- and maintain an accountable security history.

Security is treated as a continuous architectural, implementation, operational, and governance responsibility.

It is not treated as a one-time audit event.

---

## 3. Current Project Name

The current project name is:

**Global Foundation Coin**

The abbreviation is:

**GFC**

The historical name `German Foundation Coin` is deprecated.

The current reporting address uses the historical project domain. Use of that domain as an operational contact does not change the current project name.

---

## 4. Security Contact

Security reports should be sent privately to:

`info@germanfoundationcoin.org`

Do not open a public GitHub issue for a suspected vulnerability that could:

- expose users or participants to harm;
- enable loss, theft, diversion, or freezing of assets;
- expose private or protected information;
- reveal exploitable authority;
- compromise future deployments;
- enable impersonation or phishing;
- weaken presale refund rights;
- bypass locks or vesting;
- or permit unauthorized system control.

Before any production deployment, GFC MUST verify that the security mailbox is:

- under authorized project control;
- monitored regularly;
- protected through strong authentication;
- recoverable through a documented process;
- and accessible to more than one appropriately authorized security responder.

If the reporting address becomes unavailable, the repository MUST be updated before any production system is represented as active.

---

## 5. No Public Disclosure Before Coordination

A reporter SHOULD NOT publicly disclose a suspected security issue before:

- GFC has had a reasonable opportunity to assess the report;
- affected users or systems have been protected where possible;
- remediation has been prepared or deployed;
- and disclosure timing has been coordinated.

Sensitive details MUST NOT initially be submitted through:

- public GitHub issues;
- public pull requests;
- repository discussions;
- social media;
- public forums;
- community chats;
- or public blockchain messages.

A security report may later be disclosed publicly where appropriate and safe.

---

## 6. Scope

This policy currently applies to security issues concerning:

### 6.1 Specifications

Security-relevant defects in:

- `specs/architecture.md`;
- `specs/governance-constraints.md`;
- `specs/presale.md`;
- `specs/transparency-model.md`;
- `specs/non-goals.md`;
- `specs/glossary.md`;
- and `specs/README.md`.

### 6.2 Repository-Level Documentation

Security-relevant defects in:

- `README.md`;
- `SECURITY.md`;
- `CHANGELOG.md`;
- release records;
- deployment records;
- authority registries;
- known-deviation records;
- and future contributor documentation.

### 6.3 Repository Integrity

Issues involving:

- unauthorized repository changes;
- malicious commits;
- compromised maintainer accounts;
- compromised release tags;
- compromised branch protection;
- exposed repository secrets;
- dependency manipulation;
- or falsified release information.

### 6.4 Future Official Implementations

Once introduced, this policy may apply to authenticated GFC:

- token contracts;
- presale contracts;
- lock contracts;
- vesting contracts;
- treasury systems;
- liquidity systems;
- staking systems;
- governance contracts;
- transparency portals;
- evidence systems;
- backends;
- indexers;
- frontends;
- deployment processes;
- and operational infrastructure.

### 6.5 Public Authentication Infrastructure

Issues involving official GFC:

- domains;
- DNS;
- email;
- repositories;
- release channels;
- contract registries;
- wallet registries;
- and address-publication mechanisms.

### 6.6 Authority and Custody

Issues that could create or conceal:

- unauthorized administrative authority;
- undocumented upgrade authority;
- hidden pause authority;
- unsafe migration authority;
- signer concentration;
- bypassable multisig controls;
- unrestricted treasury access;
- or improper custody of participant assets.

---

## 7. Specification-Level Vulnerabilities

A specification defect may be security-relevant even where no production code exists.

Examples include:

- contradictory invariants;
- ambiguous authority;
- undefined administrator permissions;
- bypassable lock or vesting requirements;
- unsafe presale custody;
- incomplete refund conditions;
- incorrect finalization logic;
- missing replay or reentrancy protections;
- unsafe pricing assumptions;
- oracle manipulation exposure;
- insufficient rounding requirements;
- unbounded fee authority;
- hidden mint capability;
- unsafe upgradeability;
- incomplete migration constraints;
- weak signer-management rules;
- undefined emergency authority;
- missing evidence-access controls;
- privacy violations;
- or misleading security claims.

Specification issues should be reported privately where premature publication could create a practical risk for future implementations.

---

## 8. Security-Relevant Impact Areas

Reports are particularly important where an issue could affect:

- token supply integrity;
- allocation integrity;
- participant contributions;
- presale refunds;
- token entitlements;
- claim rights;
- treasury assets;
- liquidity assets;
- Impact Vault restrictions;
- Core Team vesting;
- staking balances or rewards;
- governance execution;
- multisig authority;
- upgrade or migration authority;
- fee collection;
- contract ownership;
- protected evidence;
- personal data;
- official contract identification;
- release authenticity;
- or public implementation-status accuracy.

---

## 9. Examples of Reportable Issues

Reportable issues may include:

- unauthorized minting;
- supply-cap bypass;
- transfer-fee manipulation;
- incorrect buy or sell classification;
- allocation over-distribution;
- early release of locked tokens;
- vesting acceleration;
- unauthorized treasury withdrawals;
- unauthorized liquidity removal;
- presale contribution theft;
- refund denial;
- claim duplication;
- contribution-accounting errors;
- oracle manipulation;
- stale-price acceptance;
- rounding exploitation;
- reentrancy;
- access-control bypass;
- signature replay;
- initialization defects;
- proxy-administration compromise;
- upgrade bypass;
- pause bypass;
- unsafe contract migration;
- multisig threshold bypass;
- signer replacement without approval;
- governance-vote manipulation;
- proposal-execution mismatch;
- evidence-record alteration;
- protected-data exposure;
- false evidence-status assignment;
- portal data manipulation;
- fake official contract publication;
- compromised domain or DNS;
- compromised release artifact;
- exposed private key or credential;
- dependency compromise;
- or a specification contradiction that could foreseeably produce one of these outcomes.

---

## 10. Issues That May Be Reported Publicly

Issues that do not create a meaningful security risk may generally be submitted through normal repository channels.

Examples may include:

- spelling mistakes;
- formatting defects;
- broken non-sensitive links;
- unclear prose without security implications;
- duplicate wording;
- non-sensitive terminology inconsistencies;
- or general architectural suggestions that do not identify a vulnerability.

Where uncertainty exists, the private security contact SHOULD be used.

---

## 11. Generally Out-of-Scope Reports

The following are generally not considered security vulnerabilities by themselves:

- token-price changes;
- market losses;
- low trading volume;
- lack of exchange listing;
- lack of liquidity;
- disagreement with tokenomics;
- disagreement with governance policy;
- general criticism without a concrete exploit or security impact;
- unsupported speculative concerns;
- public information already documented by GFC;
- scanner output without validation or impact analysis;
- missing non-security headers on a non-production static page;
- user-device compromise not caused by GFC infrastructure;
- loss caused solely by a user exposing their own keys;
- third-party service issues that do not affect authenticated GFC systems;
- or reports concerning fake systems that were never authenticated as official by GFC.

An out-of-scope report may still be reviewed where it identifies a credible risk.

---

## 12. Third-Party Services

GFC may rely on or interact with third-party systems such as:

- Base;
- RPC providers;
- block explorers;
- multisig providers;
- oracle providers;
- hosting providers;
- domain registrars;
- email providers;
- storage systems;
- analytics systems;
- wallets;
- exchanges;
- or external reviewers.

Vulnerabilities located exclusively within a third-party service should normally be reported to that provider.

A report should still be submitted to GFC where the issue could materially affect:

- GFC users;
- GFC assets;
- GFC contract behavior;
- GFC release authentication;
- GFC public claims;
- or GFC operational security.

---

## 13. Required Report Information

A useful security report should include, where possible:

- reporter name or preferred identifier;
- secure contact method;
- affected document, component, address, commit, or release;
- issue description;
- prerequisite conditions;
- reproduction steps;
- proof of concept;
- potential impact;
- affected assets or rights;
- expected behavior;
- observed or possible behavior;
- severity assessment;
- exploitation status;
- disclosure status;
- suggested mitigation;
- and any time-sensitive considerations.

Reports should clearly distinguish between:

- confirmed behavior;
- reproducible behavior;
- theoretical risk;
- incomplete evidence;
- and assumptions.

A report does not need to be perfectly complete before submission where delay could increase risk.

---

## 14. Proof-of-Concept Requirements

Proof-of-concept material SHOULD:

- demonstrate the issue with the minimum necessary impact;
- avoid accessing unrelated data;
- avoid moving real participant or project assets;
- avoid causing persistent state changes;
- avoid degrading service availability;
- and avoid disclosing the issue publicly.

A proof of concept MUST NOT intentionally create greater harm than necessary to establish the vulnerability.

---

## 15. Sensitive Information

Security reports may contain sensitive information.

Reporters MUST NOT include unnecessary:

- private keys;
- seed phrases;
- passwords;
- access tokens;
- personal data;
- beneficiary information;
- financial-account information;
- identity documents;
- or confidential third-party records.

Where sensitive evidence is necessary, the reporter SHOULD first describe the evidence and request an appropriate secure transfer method.

GFC responders MUST limit access to sensitive reports according to:

- need to know;
- least privilege;
- role;
- and legitimate remediation requirements.

---

## 16. Encryption

No mandatory public encryption key is currently established by this policy.

Reporters should not assume that ordinary email provides end-to-end confidentiality.

Before sending highly sensitive material, reporters SHOULD request a secure transfer method through the security contact.

Before production deployment, GFC SHOULD publish a verified encryption key or another authenticated secure-reporting mechanism.

---

## 17. Reporter Conduct

Responsible security research should follow these principles:

- stop testing after sufficient evidence has been obtained;
- avoid accessing data that is not necessary;
- avoid retaining protected information;
- avoid modifying or deleting records;
- avoid transferring assets;
- avoid creating persistent access;
- avoid interfering with other users;
- avoid service degradation;
- avoid impersonation;
- avoid extortion or coercion;
- and coordinate disclosure.

A reporter who accidentally accesses sensitive information should:

1. stop further access;
2. avoid copying or distributing the data;
3. document only what is necessary;
4. report the incident privately;
5. and delete retained sensitive material when safely permitted.

---

## 18. Prohibited Testing

Without prior written authorization, reporters MUST NOT perform:

- denial-of-service testing;
- distributed denial-of-service testing;
- destructive testing;
- social engineering;
- phishing;
- spam;
- credential stuffing;
- brute-force authentication attacks;
- physical intrusion;
- employee or contractor impersonation;
- malware deployment;
- persistent access;
- data exfiltration;
- theft or movement of assets;
- manipulation of active governance;
- manipulation of live market activity;
- testing against uninvolved third parties;
- or testing that creates a material risk to users.

The existence of a public repository does not authorize unrestricted testing against infrastructure, accounts, domains, wallets, or future production systems.

---

## 19. Mainnet and Asset Safety

Where official production contracts or wallets are introduced, researchers MUST NOT use real mainnet funds to demonstrate an exploit without prior written authorization.

A researcher MUST NOT:

- withdraw GFC assets;
- redirect fees;
- claim another participant’s tokens;
- trigger another participant’s refund;
- alter governance outcomes;
- remove liquidity;
- release locked tokens;
- accelerate vesting;
- or expose protected evidence

solely to demonstrate a vulnerability.

Testing should use:

- local environments;
- forks;
- test networks;
- simulations;
- or dedicated test deployments

where reasonably possible.

---

## 20. Report Acknowledgment

GFC intends to acknowledge validly received reports within a reasonable period.

No guaranteed acknowledgment or resolution deadline is currently established.

The security response process may depend on:

- issue severity;
- available evidence;
- reproduction complexity;
- affected systems;
- contributor availability;
- legal constraints;
- third-party dependencies;
- and remediation risk.

Before production deployment, a formal response target SHOULD be established.

---

## 21. Initial Triage

Initial triage may include:

1. confirming receipt;
2. protecting the report from unnecessary disclosure;
3. identifying affected specifications or systems;
4. validating reproducibility;
5. estimating potential impact;
6. identifying exploitation status;
7. assigning an initial severity;
8. identifying responsible responders;
9. determining immediate containment;
10. and coordinating further communication.

A report MAY be closed as non-security-relevant where no credible security impact can be established.

The reason SHOULD be communicated to the reporter where appropriate.

---

## 22. Severity Classification

Severity should consider:

- asset impact;
- participant-rights impact;
- confidentiality impact;
- integrity impact;
- availability impact;
- authority gained;
- exploitability;
- required privileges;
- affected scope;
- detectability;
- reversibility;
- active exploitation;
- and remediation complexity.

### 22.1 Critical

An issue may be Critical where it could enable:

- unrestricted theft or loss of material assets;
- arbitrary minting;
- complete administrative takeover;
- irreversible bypass of major locks or vesting;
- systemic denial of refunds;
- compromise of canonical release authentication;
- or large-scale exposure of highly sensitive protected information.

### 22.2 High

An issue may be High where it could enable:

- material unauthorized withdrawals;
- significant participant-rights violations;
- governance or multisig bypass;
- meaningful price or oracle manipulation;
- upgrade or migration abuse;
- or serious exposure of protected information.

### 22.3 Medium

An issue may be Medium where exploitation is limited by:

- narrow conditions;
- limited value;
- partial authority;
- significant user interaction;
- recoverability;
- or restricted affected scope.

### 22.4 Low

An issue may be Low where it has:

- minor security impact;
- difficult exploitation;
- limited affected scope;
- or primarily defense-in-depth value.

### 22.5 Informational

An issue may be Informational where it identifies:

- hardening opportunities;
- documentation improvements;
- minor assumptions;
- or risks without a concrete current security impact.

Initial severity may change during investigation.

---

## 23. Remediation Process

A validated vulnerability may require:

- specification correction;
- code correction;
- configuration change;
- access revocation;
- key rotation;
- signer replacement;
- contract pause;
- frontend suspension;
- domain or DNS recovery;
- release withdrawal;
- deployment replacement;
- migration;
- participant notification;
- public advisory;
- governance action;
- or independent review.

Remediation MUST NOT silently weaken:

- participant rights;
- refund rights;
- token-supply constraints;
- allocation integrity;
- locks;
- vesting;
- or historical accountability.

Where emergency action is necessary, the authority, scope, reason, execution, and continuing risk SHOULD be documented.

---

## 24. Specification Remediation

Where a security defect exists in a specification:

- the affected requirement MUST be identified;
- related specifications MUST be reviewed;
- the change MUST be classified;
- security implications MUST be documented;
- participant-rights implications MUST be documented;
- implementation implications MUST be documented;
- and public technical claims MUST be reviewed.

A specification MUST NOT be changed retrospectively merely to conceal or normalize a security defect.

Material defects should remain historically traceable through:

- Git history;
- pull requests;
- release notes;
- advisories;
- or correction records.

---

## 25. Coordinated Disclosure

Disclosure timing should balance:

- user protection;
- remediation readiness;
- exploitation risk;
- transparency;
- legal obligations;
- and reporter interests.

A coordinated disclosure may include:

- a general public advisory;
- technical vulnerability details;
- affected versions;
- severity;
- impact;
- exploitation status;
- mitigation;
- remediation;
- deployment changes;
- and reporter credit.

Exact exploit details MAY be temporarily withheld where publication would create an unreasonable ongoing risk.

---

## 26. Public Security Advisories

Where appropriate, a resolved or materially contained vulnerability SHOULD be documented publicly.

A public advisory SHOULD identify:

- advisory identifier;
- affected component;
- affected version or commit;
- severity;
- impact;
- exploitation status;
- mitigation;
- remediation status;
- fixed version;
- migration requirements;
- continuing limitations;
- and publication date.

A public advisory MUST NOT expose:

- private keys;
- credentials;
- protected personal information;
- unnecessary exploit details;
- or information that would materially endanger unremediated systems.

---

## 27. Reporter Credit

Reporter credit may be provided where:

- the report is valid;
- disclosure is appropriate;
- the reporter requests or accepts attribution;
- and attribution does not create a security or privacy risk.

A reporter may request:

- full-name attribution;
- organization attribution;
- pseudonymous attribution;
- or no attribution.

Credit is not guaranteed.

---

## 28. Bug Bounties and Rewards

No bug-bounty program or monetary reward is currently established.

Submission of a report does not create an entitlement to:

- payment;
- tokens;
- compensation;
- reimbursement;
- employment;
- partnership;
- or public recognition.

Any future bounty program must define:

- scope;
- eligibility;
- reward ranges;
- exclusions;
- duplicate handling;
- disclosure conditions;
- and payment requirements

before reports can qualify for rewards under that program.

---

## 29. Legal and Safe-Harbor Status

This Draft policy does not create a formal legal safe-harbor program.

Researchers remain responsible for complying with applicable law and avoiding harmful or unauthorized activity.

Before production launch, GFC SHOULD obtain appropriate legal review and determine whether a formal security-research safe-harbor policy can be offered.

---

## 30. Design-Level Security Principles

Security requirements begin at the specification stage.

The GFC architecture is intended to apply:

### 30.1 Explicit Authority

Material authority must be documented.

### 30.2 Least Privilege

Roles should receive only the minimum authority required.

### 30.3 Separation of Duties

Proposal, approval, execution, custody, review, and reporting should be separated where reasonably possible.

### 30.4 Defense in Depth

No single control should be assumed sufficient for material assets or authority.

### 30.5 Fail-Safe Defaults

Undefined or invalid conditions should default toward rejecting unsafe actions rather than allowing them.

### 30.6 Participant-Rights Protection

Administrative convenience must not silently override participant entitlements or refund rights.

### 30.7 Supply Integrity

No authority should be capable of introducing undocumented inflation.

### 30.8 Lock and Vesting Integrity

Upgrade, migration, or emergency mechanisms must not function as concealed early-release paths.

### 30.9 Transparency With Privacy

Accountability must not require unnecessary disclosure of protected information.

### 30.10 Historical Accountability

Material incidents, corrections, and security-related deviations should remain reviewable.

---

## 31. Smart-Contract Security Requirements

Before production deployment, material GFC contracts SHOULD be subject to:

- threat modeling;
- specification review;
- architecture review;
- unit testing;
- integration testing;
- invariant testing;
- fuzz testing;
- static analysis;
- dependency review;
- deployment simulation;
- role and authority review;
- upgrade and migration review;
- incident-response planning;
- and independent security review.

High-value or high-authority components SHOULD receive an appropriately scoped independent smart-contract audit before production use.

An audit does not guarantee safety.

---

## 32. Presale Security Requirements

Before any presale activation, the implementation MUST define and test:

- accepted payment assets;
- pricing logic;
- oracle protections;
- stale-price rejection;
- decimal normalization;
- deterministic rounding;
- allocation limits;
- purchase accounting;
- soft-cap accounting;
- contribution custody;
- finalization;
- token entitlement;
- claims;
- refunds;
- cancellation;
- pausing;
- withdrawal restrictions;
- access control;
- reentrancy protection;
- and failure recovery.

Participant contributions MUST NOT become project-controlled merely because the soft cap is reached before presale completion.

---

## 33. Token Security Requirements

Before production deployment, the token implementation MUST define and test:

- fixed total supply;
- mint-authority status;
- allocation creation;
- transfer behavior;
- buy classification;
- sell classification;
- fee calculation;
- fee limits;
- fee destinations;
- exemptions;
- recognized pools;
- administrative roles;
- pause behavior where applicable;
- upgradeability;
- and migration behavior.

No production communication may claim immutable supply, fees, locks, or authority unless the deployed implementation supports the claim.

---

## 34. Governance Security Requirements

Before production governance activation, the system MUST define:

- privileged roles;
- controlling addresses;
- signer requirements;
- signer independence assumptions;
- approval thresholds;
- timelocks;
- proposal authority;
- execution authority;
- pause authority;
- upgrade authority;
- migration authority;
- emergency authority;
- signer replacement;
- conflict-of-interest handling;
- and incident authority.

A multisig alone MUST NOT be treated as proof of decentralization or independent control.

---

## 35. Transparency-System Security

Future transparency and evidence systems must protect against:

- unauthorized record modification;
- silent deletion;
- evidence-status manipulation;
- claim-status manipulation;
- forged integrity anchors;
- protected-data exposure;
- reviewer impersonation;
- portal compromise;
- indexer manipulation;
- database corruption;
- access-log deletion;
- and false official-address publication.

Public interfaces must remain distinguishable from authenticated primary sources.

---

## 36. Secrets and Credentials

The repository MUST NOT contain:

- private keys;
- seed phrases;
- passwords;
- API secrets;
- access tokens;
- signing secrets;
- production credentials;
- unredacted recovery material;
- or confidential personal information.

Where a secret is committed accidentally:

1. the secret MUST be treated as compromised;
2. access MUST be revoked or rotated;
3. affected systems MUST be reviewed;
4. Git-history removal MAY be considered;
5. and the incident SHOULD be documented appropriately.

Deleting a secret from the latest commit does not make it secure again.

---

## 37. Dependency Security

Future implementation dependencies SHOULD be:

- minimized;
- version-pinned where appropriate;
- reviewed;
- monitored;
- reproducibly installed;
- and updated through a controlled process.

Security assessment SHOULD consider:

- compromised packages;
- abandoned dependencies;
- malicious updates;
- transitive dependencies;
- build-system compromise;
- compiler differences;
- and deployment-environment differences.

---

## 38. Release Security

Future production releases SHOULD be:

- versioned;
- authenticated;
- reproducible where feasible;
- linked to source-code commits;
- linked to specification releases;
- linked to audit or review results;
- linked to deployment addresses;
- and accompanied by known deviations.

A compromised release tag, deployment record, contract registry, or address-publication channel is a security incident.

---

## 39. Domain and Communication Security

Official domains and communication channels may be used to publish:

- contract addresses;
- wallet addresses;
- release information;
- security notices;
- and presale information.

Compromise of these channels could create material phishing or asset-loss risk.

Before production use, GFC SHOULD establish:

- strong account authentication;
- restricted administrative access;
- domain-locking controls;
- DNS monitoring;
- recovery procedures;
- authenticated release records;
- and independent address-verification paths.

---

## 40. Incident Response

Before production deployment, GFC MUST define an incident-response process covering:

- detection;
- severity assessment;
- responder authority;
- containment;
- pause criteria;
- key compromise;
- signer compromise;
- contract compromise;
- frontend compromise;
- domain compromise;
- participant communication;
- remediation;
- migration;
- disclosure;
- and post-incident review.

Emergency action MUST remain constrained by the applicable governance and architecture specifications.

---

## 41. Limitations

This policy does not guarantee:

- specification correctness;
- implementation correctness;
- vulnerability-free software;
- uninterrupted availability;
- successful remediation;
- protection from all attacks;
- confidentiality of ordinary email;
- or compensation for reports.

Security reviews, audits, formal verification, testing, monitoring, and disclosure processes reduce risk.

They do not eliminate risk.

---

## 42. Changes to This Policy

Material changes to this policy SHOULD be:

- documented;
- reviewed;
- committed through a dedicated branch;
- submitted through a pull request;
- classified according to their effect;
- and recorded in the repository history.

Breaking changes affecting reporter expectations, disclosure, eligibility, authorization, or supported versions SHOULD be explicitly documented.

---

## 43. Unresolved Security Decisions

The following matters remain unresolved:

- final security-contact domain;
- secure-reporting platform;
- public encryption key;
- formal acknowledgment target;
- triage-response target;
- remediation target;
- formal severity methodology;
- formal safe-harbor language;
- bug-bounty program;
- reporter-eligibility rules;
- security-advisory format;
- incident-response team;
- emergency contacts;
- disclosure-approval authority;
- release-signing mechanism;
- dependency-monitoring process;
- and production monitoring infrastructure.

---

## 44. Requirements Before Stable Status

This policy MUST NOT be marked Stable until:

- the security contact is confirmed and monitored;
- account-recovery procedures are documented;
- a secure reporting method is available;
- an encryption or protected-transfer method is established;
- supported-version rules are defined;
- response targets are defined;
- severity classification is finalized;
- the vulnerability-handling workflow is assigned to responsible roles;
- coordinated-disclosure authority is defined;
- reporter-credit rules are finalized;
- legal review is completed;
- safe-harbor treatment is decided;
- bug-bounty status is finalized;
- incident-response procedures are documented;
- emergency authority is aligned with governance specifications;
- contract and deployment security requirements are finalized;
- release authentication is defined;
- monitoring responsibilities are defined;
- domain and communication security controls are defined;
- all related specifications are mutually consistent;
- and repository-wide security terminology is consistent.

---

## 45. Final Security Principles

> Security begins before implementation.

> A specification defect can be a security defect.

> Public code is not automatically secure code.

> Source verification is not a security audit.

> An audit does not guarantee safety.

> A multisig does not automatically prove independent control.

> Upgradeability is part of the security model.

> Participant rights are part of the security model.

> Privacy is part of the security model.

> Release authentication is part of the security model.

> Transparency does not require premature vulnerability disclosure.

> Emergency authority must remain constrained.

> A deleted credential must still be treated as compromised.

> No production claim should exceed the security evidence supporting it.

Security requires continuous alignment between specifications, implementation, authority, operations, monitoring, incident response, and public communication.

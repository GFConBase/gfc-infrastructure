# Global Foundation Coin Security Policy

**Document ID:** GFC-SEC-POL-001  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Public Pilot Network:** Base Sepolia  
**Pilot Chain ID:** 84532  
**Intended Production Network:** Base Mainnet  
**Production Chain ID:** 8453  
**Last Updated:** 2026-08-30

---

## 1. Document Status

This document defines the current security-reporting, vulnerability-handling, coordinated-disclosure, and repository-level security policy for Global Foundation Coin (GFC).

It is normative because it establishes:

- how suspected vulnerabilities SHOULD be reported;
- which issues are security-relevant;
- how sensitive reports are handled;
- which testing activities are prohibited;
- how disclosure SHOULD be coordinated;
- and which repository-level security controls are expected before production reliance.

Its maturity remains Draft.

At the current repository state:

- the **GFC Token / Economic Layer** is the current primary product focus;
- a public GFC pilot exists on **Base Sepolia**;
- no production GFC token is deployed on Base Mainnet;
- no GFC presale is live;
- no production treasury, liquidity, staking, vesting, governance, or complete Transparency Registry is operational;
- no production contract or wallet address is established as official by this policy;
- no formal bug-bounty program is active;
- no guaranteed vulnerability-response service level is established;
- no production software version is currently declared supported;
- and no independent production security audit is represented as completed by this policy.

Security-relevant issues may nevertheless exist within:

- specifications;
- repository configuration;
- documentation;
- release processes;
- deployment records;
- authority models;
- custody designs;
- future implementation assumptions;
- public authentication channels;
- and public security representations.

Current implementation and deployment status is maintained in:

- [`STATUS.md`](STATUS.md)
- [`DEPLOYMENTS.md`](DEPLOYMENTS.md)

Detailed technical security requirements are defined in [`specs/security-model.md`](specs/security-model.md).

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
- preserve historical accountability;
- and keep public security claims aligned with actual evidence.

Security is treated as a continuous architectural, implementation, operational, governance, and communication responsibility.

It is not treated as a one-time audit event.

---

## 3. Current Project Identity

The current project name is:

**Global Foundation Coin**

The abbreviation is:

**GFC**

The historical name:

**German Foundation Coin**

is deprecated for current project and production naming.

---

## 4. Security Contact

Security reports SHOULD be sent privately to:

```text
info@globalfoundationcoin.org
```

Do not open a public GitHub issue for a suspected vulnerability that could:

- expose users or participants to harm;
- enable loss, theft, diversion, or freezing of assets;
- expose private or protected information;
- reveal exploitable privileged authority;
- compromise future production deployments;
- enable impersonation or phishing;
- weaken presale refund rights;
- bypass locks or vesting;
- alter production authentication;
- compromise evidence integrity;
- or permit unauthorized system control.

Before any production deployment, GFC MUST verify that the security mailbox is:

- under authorized project control;
- monitored regularly;
- protected through strong authentication;
- recoverable through a documented process;
- and included in the applicable incident-response process.

This policy does not represent that multiple independent security responders currently exist.

If the reporting address changes, this file SHOULD be updated promptly.

---

## 5. Private Reporting First

A reporter SHOULD NOT publicly disclose a suspected security issue before:

- GFC has had a reasonable opportunity to assess the report;
- affected users or systems have been protected where possible;
- remediation has been prepared or deployed where applicable;
- and disclosure timing has been coordinated where reasonable.

Sensitive vulnerability details SHOULD NOT initially be submitted through:

- public GitHub issues;
- public pull requests;
- repository discussions;
- social media;
- public forums;
- Telegram or other public community chats;
- or public blockchain messages.

A security issue MAY later be disclosed publicly where appropriate and safe.

---

## 6. Scope

This policy applies to security-relevant issues concerning the authenticated GFC repository and, where later introduced, authenticated GFC production infrastructure.

### 6.1 Specifications

Security-relevant defects in the current specification set include:

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

### 6.2 Repository-Level Records

Security-relevant defects may also affect:

- [`README.md`](README.md)
- [`STATUS.md`](STATUS.md)
- [`DEPLOYMENTS.md`](DEPLOYMENTS.md)
- [`ROADMAP.md`](ROADMAP.md)
- [`DECISIONS.md`](DECISIONS.md)
- [`SECURITY.md`](SECURITY.md)
- [`CHANGELOG.md`](CHANGELOG.md)
- future release records;
- deployment records;
- authority registries;
- and known-deviation records.

### 6.3 Repository Integrity

Issues involving:

- unauthorized repository changes;
- compromised maintainer accounts;
- malicious commits;
- compromised branches or tags;
- exposed repository secrets;
- dependency manipulation;
- falsified release information;
- or unauthorized changes to deployment records.

### 6.4 Public Base Sepolia Pilot

Security issues affecting the authenticated public Base Sepolia pilot MAY be reported.

Current pilot record:

```text
Network: Base Sepolia
Chain ID: 84532
Token: tGFC
Contract: 0x7262Cca91938ede6bB6560F81104Aa410848e7f3
Status: Public Pilot / Non-Production
Source: Verified
```

The pilot is non-production.

A pilot issue MUST NOT automatically be represented as a vulnerability in future Base Mainnet code unless the affected logic is actually shared.

### 6.5 Future Official Production Implementations

Once authenticated and introduced, this policy MAY apply to GFC:

- token contracts;
- presale contracts;
- Impact Vault contracts;
- vesting contracts;
- treasury systems;
- liquidity systems;
- staking systems;
- governance contracts;
- Transparency Registry components;
- evidence systems;
- portals;
- backends;
- indexers;
- frontends;
- deployment processes;
- and operational infrastructure.

### 6.6 Public Authentication Infrastructure

Security issues involving official GFC:

- domains;
- DNS;
- email;
- repositories;
- release channels;
- deployment records;
- contract registries;
- wallet registries;
- and address-publication mechanisms.

### 6.7 Authority and Custody

Issues that could create, conceal, or misuse:

- unauthorized administrative authority;
- undocumented upgrade authority;
- hidden pause authority;
- unsafe migration authority;
- recovery authority;
- signer concentration;
- bypassable multisig controls;
- unrestricted treasury access;
- liquidity-withdrawal authority;
- or improper custody of participant assets.

---

## 7. Specification-Level Vulnerabilities

A specification defect may be security-relevant even where no production code exists.

Examples include:

- contradictory invariants;
- ambiguous authority;
- undefined privileged permissions;
- bypassable lock or vesting requirements;
- unsafe presale custody;
- incomplete refund behavior;
- incorrect finalization logic;
- unsafe immediate-distribution accounting;
- missing failed-sale settlement requirements;
- incorrect fee limits;
- hidden inflation path;
- unsafe upgradeability;
- incomplete migration constraints;
- weak signer-management rules;
- undefined emergency authority;
- evidence-integrity weaknesses;
- protected-data exposure;
- Registry-history manipulation;
- or misleading security claims.

Specification issues SHOULD be reported privately where premature publication could create practical risk for future implementations.

---

## 8. Security-Relevant Impact Areas

Reports are particularly important where an issue could affect:

- fixed token supply;
- allocation integrity;
- participant contributions;
- presale refunds;
- immediate GFC distribution;
- participant purchase accounting;
- treasury assets;
- liquidity assets;
- Impact Vault restrictions;
- Core Team vesting;
- staking principal;
- staking rewards;
- governance execution;
- multisig or signer authority;
- upgrade or migration authority;
- fee collection;
- fee limits;
- contract ownership;
- protected evidence;
- Transparency Registry history;
- personal data;
- official contract identification;
- release authenticity;
- or public implementation-status accuracy.

---

## 9. Examples of Reportable Issues

Reportable issues MAY include:

- unauthorized minting;
- supply-cap bypass;
- transfer-fee manipulation;
- sell-fee increase beyond the applicable limit;
- incorrect buy or sell classification;
- allocation over-distribution;
- early Impact Vault release;
- Core Team vesting acceleration;
- unauthorized treasury withdrawal;
- unauthorized liquidity removal;
- presale contribution theft;
- insufficient refund reserves;
- failed-sale settlement inconsistency;
- immediate-distribution accounting defects;
- duplicate Presale distribution;
- oracle or pricing manipulation;
- stale-price acceptance;
- rounding exploitation;
- reentrancy;
- access-control bypass;
- signature replay;
- initialization defects;
- proxy-administration compromise;
- upgrade bypass;
- pause bypass;
- unsafe migration;
- multisig threshold bypass;
- signer replacement without authorization;
- governance-execution mismatch;
- staking reward over-distribution;
- staking principal loss;
- evidence-record alteration;
- Registry-history deletion;
- protected-data exposure;
- false review or verification status;
- portal data manipulation;
- fake official contract publication;
- compromised domain or DNS;
- compromised release artifact;
- exposed private key or credential;
- dependency compromise;
- or specification contradictions that could foreseeably produce material security harm.

---

## 10. Issues Suitable for Normal Repository Channels

Issues that do not create meaningful security risk may generally be submitted through ordinary repository channels.

Examples include:

- spelling mistakes;
- formatting defects;
- broken non-sensitive links;
- unclear prose without security implications;
- duplicate wording;
- non-sensitive terminology inconsistencies;
- and general design suggestions without a concrete security impact.

Where uncertainty exists, private reporting is preferred.

---

## 11. Generally Out-of-Scope Reports

The following are generally not security vulnerabilities by themselves:

- token-price changes;
- market losses;
- low trading volume;
- absence of exchange listing;
- absence of liquidity;
- disagreement with tokenomics;
- disagreement with governance policy;
- criticism without a concrete security impact;
- speculative concerns unsupported by a plausible impact path;
- scanner output without validation;
- missing non-security headers on a static non-production page;
- user-device compromise not caused by authenticated GFC infrastructure;
- loss caused solely by a user exposing their own keys;
- third-party issues that do not affect authenticated GFC systems;
- or reports concerning fake systems never authenticated as official GFC infrastructure.

An otherwise out-of-scope report MAY still be reviewed where it identifies a credible material risk.

---

## 12. Third-Party Services

GFC may rely on or interact with third-party systems such as:

- Base;
- RPC providers;
- block explorers;
- multisig providers;
- oracle or pricing providers;
- hosting providers;
- domain registrars;
- email providers;
- storage systems;
- analytics systems;
- wallets;
- exchanges;
- and external reviewers.

Vulnerabilities exclusively within a third-party service should normally be reported to that provider.

A report SHOULD also be sent to GFC where the issue could materially affect:

- GFC users;
- GFC assets;
- GFC contract behavior;
- GFC release authentication;
- GFC public claims;
- or GFC operational security.

---

## 13. Required Report Information

A useful report SHOULD include, where possible:

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
- and time-sensitive considerations.

Reports SHOULD distinguish among:

- confirmed behavior;
- reproducible behavior;
- theoretical risk;
- incomplete evidence;
- and assumptions.

A report does not need to be perfectly complete before submission where delay could increase risk.

---

## 14. Proof-of-Concept Requirements

Proof-of-concept material SHOULD:

- demonstrate the issue with minimum necessary impact;
- avoid accessing unrelated data;
- avoid moving real participant or project assets;
- avoid persistent state changes;
- avoid degrading service availability;
- and avoid premature public disclosure.

A proof of concept MUST NOT intentionally create greater harm than necessary to establish the issue.

---

## 15. Sensitive Information

Security reports may contain sensitive information.

Reporters SHOULD NOT include unnecessary:

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

## 16. Encryption and Secure Transfer

No mandatory public encryption key is currently established by this policy.

Ordinary email SHOULD NOT be assumed to provide end-to-end confidentiality.

Before sending highly sensitive material, reporters SHOULD request a secure transfer method through:

```text
info@globalfoundationcoin.org
```

Before production reliance, GFC SHOULD establish an authenticated encryption key or another secure reporting mechanism.

---

## 17. Reporter Conduct

Responsible security research SHOULD follow these principles:

- stop testing after sufficient evidence is obtained;
- avoid unnecessary access;
- avoid retaining protected information;
- avoid modifying or deleting records;
- avoid transferring assets;
- avoid persistent access;
- avoid interference with other users;
- avoid service degradation;
- avoid impersonation;
- avoid coercion;
- and coordinate disclosure.

If a reporter accidentally accesses sensitive information, the reporter SHOULD:

1. stop further access;
2. avoid further copying or distribution;
3. document only what is necessary;
4. report privately;
5. and delete retained sensitive material when safely appropriate.

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
- unnecessary data exfiltration;
- theft or movement of assets;
- manipulation of active governance;
- manipulation of live market activity;
- testing against uninvolved third parties;
- or testing that creates material risk to users.

A public repository does not authorize unrestricted testing against project infrastructure, accounts, domains, wallets, or future production systems.

---

## 19. Mainnet and Asset Safety

Where authenticated production contracts or wallets are introduced, researchers MUST NOT use real production funds to demonstrate an exploit without prior written authorization.

A researcher MUST NOT:

- withdraw GFC assets;
- redirect fees;
- trigger another participant's refund;
- remove liquidity;
- release Impact Vault GFC;
- accelerate Core Team vesting;
- withdraw another participant's staking principal;
- alter production governance;
- or expose protected evidence

solely to demonstrate a vulnerability.

Testing SHOULD use:

- local environments;
- forks;
- test networks;
- simulations;
- or dedicated test deployments

where reasonably possible.

---

## 20. Report Acknowledgment

GFC intends to acknowledge validly received reports within a reasonable period.

No guaranteed acknowledgment or remediation deadline is currently established.

Response may depend on:

- severity;
- available evidence;
- reproduction complexity;
- affected systems;
- available responsible personnel;
- legal constraints;
- third-party dependencies;
- and remediation risk.

Before production reliance, formal response targets SHOULD be established.

---

## 21. Initial Triage

Initial triage MAY include:

1. confirming receipt;
2. restricting unnecessary disclosure;
3. identifying affected specifications or systems;
4. validating reproducibility;
5. estimating impact;
6. identifying exploitation status;
7. assigning initial severity;
8. identifying responsible responders;
9. determining immediate containment;
10. and coordinating further communication.

A report MAY be closed as non-security-relevant where no credible security impact can be established.

---

## 22. Severity Classification

Severity SHOULD consider:

- asset impact;
- participant-rights impact;
- confidentiality;
- integrity;
- availability;
- authority gained;
- exploitability;
- required privileges;
- affected scope;
- detectability;
- reversibility;
- active exploitation;
- and remediation complexity.

### 22.1 Critical

Potential examples include:

- unrestricted theft of material assets;
- arbitrary minting;
- complete administrative takeover;
- irreversible bypass of the Impact Vault or Core Team vesting;
- systemic denial of Presale refunds;
- compromise of canonical production release authentication;
- or large-scale exposure of highly sensitive protected information.

### 22.2 High

Potential examples include:

- material unauthorized withdrawal;
- significant participant-rights violation;
- governance or multisig bypass;
- serious pricing manipulation;
- upgrade or migration abuse;
- or serious protected-information exposure.

### 22.3 Medium

An issue MAY be Medium where exploitation is meaningfully constrained by:

- narrow conditions;
- limited value;
- partial authority;
- significant user interaction;
- recoverability;
- or restricted scope.

### 22.4 Low

An issue MAY be Low where the security impact is minor or largely defense-in-depth.

### 22.5 Informational

An issue MAY be Informational where it identifies hardening opportunities or assumptions without concrete current exploitation impact.

Initial severity MAY change during investigation.

---

## 23. Remediation Process

A validated issue MAY require:

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

- fixed supply;
- Presale refund rights;
- Presale allocation limits;
- Impact Vault restrictions;
- Core Team vesting;
- participant staking rights;
- historical accountability;
- or protected evidence.

Emergency actions MUST remain within the applicable authority constraints.

---

## 24. Specification Remediation

Where a security defect exists in a specification:

- the affected requirement SHOULD be identified;
- related specifications SHOULD be reviewed;
- the change SHOULD be classified;
- security implications SHOULD be documented;
- participant-rights implications SHOULD be reviewed;
- implementation implications SHOULD be reviewed;
- and public technical claims SHOULD be checked for inconsistency.

A specification MUST NOT be changed retrospectively merely to conceal a security defect.

Material defects SHOULD remain historically traceable through repository history or later security records.

---

## 25. Coordinated Disclosure

Disclosure timing SHOULD balance:

- participant protection;
- remediation readiness;
- exploitation risk;
- transparency;
- legal obligations;
- and reporter interests.

A coordinated disclosure MAY include:

- public advisory;
- affected versions;
- severity;
- impact;
- exploitation status;
- mitigation;
- remediation;
- deployment changes;
- and reporter credit.

Exact exploit details MAY be temporarily withheld where publication would materially increase active risk.

---

## 26. Public Security Advisories

Where appropriate, a resolved or materially contained vulnerability SHOULD be documented publicly.

A public advisory SHOULD identify, where applicable:

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
- or unnecessary exploit details that materially endanger unremediated systems.

---

## 27. Reporter Credit

Reporter credit MAY be provided where:

- the report is valid;
- disclosure is appropriate;
- the reporter accepts attribution;
- and attribution does not create privacy or security risk.

A reporter MAY request:

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
- GFC;
- compensation;
- reimbursement;
- employment;
- partnership;
- or public recognition.

Any future bounty program MUST define its own:

- scope;
- eligibility;
- reward ranges;
- exclusions;
- duplicate handling;
- disclosure conditions;
- and payment requirements.

---

## 29. Legal and Safe-Harbor Status

This Draft policy does not create a formal legal safe-harbor program.

Researchers remain responsible for complying with applicable law and avoiding harmful or unauthorized activity.

Before production reliance, GFC SHOULD obtain appropriate legal review and decide whether a formal security-research safe-harbor policy can be offered.

---

## 30. Repository-Level Security Principles

### 30.1 Explicit authority

Material authority MUST be documented.

### 30.2 Least privilege

Roles SHOULD receive only the minimum authority required.

### 30.3 Separation of duties

Proposal, approval, execution, custody, review, and reporting SHOULD be separated where reasonably possible.

### 30.4 Defense in depth

No single control SHOULD be assumed sufficient for material assets or authority.

### 30.5 Fail-safe behavior

Undefined or invalid conditions SHOULD fail toward safety rather than silently expanding authority.

### 30.6 Participant-rights protection

Operational convenience MUST NOT silently override participant rights.

### 30.7 Fixed-supply protection

No authority MAY create undocumented GFC inflation.

### 30.8 Lock and vesting integrity

Upgrade, migration, recovery, or emergency functions MUST NOT become concealed early-release paths.

### 30.9 Transparency with privacy

Accountability MUST NOT require unnecessary publication of protected information.

### 30.10 Historical accountability

Material incidents, corrections, authority changes, and security-related deviations SHOULD remain reviewable where appropriate.

### 30.11 Pilot and production separation

Pilot security state MUST NOT be represented as production security state.

---

## 31. Technical Security Model

Detailed technical requirements for:

- threat actors;
- protected assets;
- security invariants;
- token security;
- allocation security;
- Impact Vault security;
- vesting security;
- treasury security;
- liquidity security;
- Presale security;
- staking security;
- governance security;
- authority security;
- multisig and signer security;
- deployment security;
- frontend security;
- domain security;
- evidence security;
- monitoring;
- incidents;
- recovery;
- and review

are defined in:

[`specs/security-model.md`](specs/security-model.md)

This repository-level policy SHOULD NOT be treated as a replacement for that technical specification.

---

## 32. Presale Security Policy

Before any production Presale activation, the implementation MUST satisfy the applicable requirements in:

- [`specs/presale.md`](specs/presale.md)
- [`specs/economic-flows.md`](specs/economic-flows.md)
- [`specs/security-model.md`](specs/security-model.md)

The current Draft Presale design uses:

- ETH, USDC, and DAI on Base;
- immediate GFC distribution;
- €0.05 reference price;
- eight-week intended duration;
- €250,000 soft cap;
- and maximum Presale distribution of 150,000,000 GFC.

The interaction between immediate GFC distribution and failed-sale refund rights remains unresolved.

This issue is a production activation blocker.

No current policy authorizes an improvised:

- clawback;
- forced burn;
- forced return;
- token invalidation;
- or equivalent mechanism.

---

## 33. Token Security Policy

The production token design MUST preserve the current fixed-supply boundary:

```text
1,000,000,000 GFC
```

The current intended fee model is:

```text
Buy fee: 0%
Sell fee: 1%
```

Production communication MUST NOT claim immutable supply, immutable fee behavior, or immutable authority unless actual deployed architecture supports the claim.

Detailed requirements are defined in [`specs/token.md`](specs/token.md).

---

## 34. Allocation, Lock, and Vesting Security

The current intended allocation model totals 100% of fixed GFC supply.

Two long-term restrictions are especially security-sensitive:

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

No current production contract enforces these restrictions.

Future production implementation MUST NOT include undisclosed paths that weaken them.

Detailed requirements are defined in:

- [`specs/allocations.md`](specs/allocations.md)
- [`specs/vesting-and-unlocks.md`](specs/vesting-and-unlocks.md)

---

## 35. Staking Security Policy

No production GFC staking system is currently operational.

The current design direction is:

**hybrid and non-inflationary**

Staking MUST NOT create additional GFC beyond the fixed supply.

No reward source is currently finalized.

Security reports concerning future staking SHOULD consider:

- principal custody;
- reward accounting;
- reward-pool solvency;
- parameter authority;
- lock and withdrawal behavior;
- migration;
- pause;
- recovery;
- and governance-related rights.

Detailed requirements are defined in [`specs/staking.md`](specs/staking.md).

---

## 36. Governance and Authority Security

Production authority has not yet been assigned through this policy.

Future production governance and authority MUST remain consistent with:

- [`specs/roles-and-authority.md`](specs/roles-and-authority.md)
- [`specs/governance-constraints.md`](specs/governance-constraints.md)

A multisig MUST NOT be treated as proof of:

- decentralization;
- signer independence;
- or sufficient separation of duties.

Token ownership or staking MUST NOT automatically create unrestricted administrative authority.

---

## 37. Transparency and Evidence Security

No complete production Transparency Registry is currently deployed.

The planned Registry is intended as:

**versioned historical accountability, not a permanent approval badge**

Security issues MAY include:

- unauthorized status changes;
- silent deletion;
- false verification labels;
- reviewer impersonation;
- evidence substitution;
- historical-record manipulation;
- protected-data exposure;
- and portal compromise.

Detailed requirements are defined in [`specs/transparency-model.md`](specs/transparency-model.md).

---

## 38. Secrets and Credentials

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

If a secret is committed accidentally:

1. the secret MUST be treated as compromised;
2. relevant access MUST be revoked or rotated;
3. affected systems SHOULD be reviewed;
4. Git-history removal MAY be considered;
5. and the event SHOULD be handled according to its actual security impact.

Deleting a secret from the latest commit does not make it secure again.

---

## 39. Dependency Security

Future implementation dependencies SHOULD be:

- minimized;
- version-pinned where appropriate;
- reviewed;
- monitored;
- reproducibly installed where feasible;
- and updated through controlled processes.

Security assessment SHOULD consider:

- compromised packages;
- abandoned dependencies;
- malicious updates;
- transitive dependencies;
- build-system compromise;
- compiler differences;
- and deployment-environment differences.

---

## 40. Release Security

Future production releases SHOULD be:

- versioned;
- authenticated;
- linked to source commits;
- linked to applicable specifications;
- linked to deployment records;
- linked to security-review status;
- and accompanied by known deviations.

The continuously changing `main` branch is not automatically a production release.

Compromise of:

- a release tag;
- deployment record;
- contract registry;
- wallet registry;
- or production-address publication channel

is a security incident.

---

## 41. Domain and Communication Security

Official domains and communication channels may publish:

- contract addresses;
- wallet addresses;
- releases;
- security notices;
- Presale information;
- and production status.

Compromise of these channels can create material phishing or asset-loss risk.

Before production reliance, GFC SHOULD maintain controls appropriate to the risk, including where available:

- strong account authentication;
- restricted administrative access;
- domain locking;
- DNS monitoring;
- recovery procedures;
- and independent address-verification paths.

---

## 42. Incident Response

Before production reliance, GFC MUST define an incident-response process covering:

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
- Presale incidents;
- participant communication;
- remediation;
- migration;
- disclosure;
- and post-incident review.

Emergency action MUST remain bounded by applicable authority and governance constraints.

---

## 43. Security Claims and Status Vocabulary

Public security communication MUST use status terminology consistently with [`specs/glossary.md`](specs/glossary.md).

Relevant distinctions include:

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

The following claims MUST NOT be treated as equivalent:

> Source Verified ≠ Audited

> Tested ≠ Audited

> Audited ≠ Risk-Free

> Pilot ≠ Production

> Deployed ≠ Operational

> Multisig ≠ Decentralized

---

## 44. Current Pilot Security Status

The authenticated public pilot currently recorded by this repository is:

```text
Network: Base Sepolia
Chain ID: 84532
Token: tGFC
Contract: 0x7262Cca91938ede6bB6560F81104Aa410848e7f3
Source status: Verified
Environment: Public Pilot / Non-Production
```

This does not establish:

- production security;
- production audit;
- production authority;
- Mainnet readiness;
- or production conformance.

Future production security must be evaluated independently.

---

## 45. Limitations

This policy does not guarantee:

- specification correctness;
- implementation correctness;
- vulnerability-free software;
- uninterrupted availability;
- successful remediation;
- protection from all attacks;
- confidentiality of ordinary email;
- or compensation for reports.

Security reviews, audits, testing, monitoring, and disclosure processes reduce risk.

They do not eliminate risk.

---

## 46. Changes to This Policy

Material changes to this policy SHOULD be:

- documented;
- reviewed;
- committed through the normal repository process;
- classified according to effect;
- and reflected in repository history.

This policy does not mandate a specific branch or pull-request workflow that the repository has not separately adopted.

Breaking changes affecting:

- reporter expectations;
- disclosure;
- authorization;
- supported versions;
- or safe-research expectations

SHOULD be explicitly documented.

---

## 47. Current Unresolved Security-Policy Decisions

The following remain unresolved:

- secure reporting platform;
- public encryption key;
- formal acknowledgment target;
- triage-response target;
- remediation target;
- formal severity methodology;
- formal safe-harbor language;
- bug-bounty program;
- reporter-eligibility rules;
- security-advisory format;
- final incident-response roles;
- emergency contacts;
- disclosure-approval authority;
- release-signing mechanism;
- dependency-monitoring process;
- and production monitoring infrastructure.

These unresolved matters MUST NOT be represented as established production controls.

---

## 48. Requirements Before Stable Status

This policy MUST NOT be marked Stable until:

- the security contact remains confirmed and monitored;
- account-recovery procedures are documented;
- a secure reporting method is available;
- an encryption or protected-transfer method is established;
- supported-version rules are defined;
- response targets are defined;
- severity classification is finalized;
- vulnerability-handling responsibilities are assigned;
- coordinated-disclosure authority is defined;
- reporter-credit rules are finalized;
- legal review is completed;
- safe-harbor treatment is decided;
- bug-bounty status is finalized;
- incident-response procedures are documented;
- emergency authority is aligned with governance specifications;
- production contract and deployment security requirements are finalized;
- release authentication is defined;
- monitoring responsibilities are defined;
- domain and communication security controls are defined;
- Base Sepolia pilot and Base Mainnet production security claims remain consistently separated;
- and repository-wide security terminology is consistent.

---

## 49. Final Security Principles

> Security begins before implementation.

> A specification defect can be a security defect.

> Public code is not automatically secure code.

> Source verification is not a security audit.

> An audit does not guarantee safety.

> A multisig does not automatically prove independent control.

> Upgradeability is part of the security model.

> Migration is part of the security model.

> Recovery authority is privileged authority.

> Participant rights are part of the security model.

> Privacy is part of the security model.

> Release authentication is part of the security model.

> Transparency does not require premature vulnerability disclosure.

> Emergency authority must remain constrained.

> A deleted credential must still be treated as compromised.

> Pilot security does not establish production security.

> No production claim should exceed the security evidence supporting it.

Security requires continuous alignment between specifications, implementation, authority, operations, monitoring, incident response, and public communication.

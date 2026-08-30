# GFC Security Model Specification

**Document ID:** GFC-SEC-001  
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

This document defines the intended security model for the Global Foundation Coin (GFC) infrastructure.

It is normative because it defines:

- protected assets;
- trust assumptions;
- security invariants;
- threat surfaces;
- privileged-authority risks;
- required security properties;
- incident expectations;
- and prohibited security representations.

Its maturity remains Draft.

At the current repository state:

- the current primary product focus is the **GFC Token / Economic Layer**;
- a public GFC pilot exists on **Base Sepolia**;
- no production GFC token is deployed on Base Mainnet;
- no GFC presale is live;
- no production treasury infrastructure is active;
- no production governance infrastructure is active;
- no production staking infrastructure is operational;
- no production Transparency Registry is represented as deployed;
- no production multisig, signer set, privileged wallet, administrator, pauser, upgrader, or migration authority is authenticated as official by this document;
- no production security audit is represented as completed by this document;
- and no security mechanism described here should be assumed to exist until it is implemented, tested, authenticated, and reflected in the applicable deployment records.

The Base Sepolia pilot is non-production.

Its existence does not establish:

- Mainnet production readiness;
- production security;
- production authority;
- audit completion;
- or production conformance.

Current deployment and operational status is maintained in [`../STATUS.md`](../STATUS.md).

---

## 2. Purpose

The purpose of this specification is to define the security boundaries that GFC implementations and operations must respect before production reliance.

This document is intended to ensure that security analysis covers more than smart-contract code alone.

The GFC security model includes risks arising from:

- smart contracts;
- privileged roles;
- custody;
- multisig and signer structures;
- contract deployment;
- upgrades;
- pauses;
- migrations;
- fee administration;
- presale custody and accounting;
- token allocations;
- vesting and locks;
- treasury operations;
- liquidity operations;
- staking;
- governance;
- frontends;
- domains and DNS;
- release publication;
- evidence systems;
- the planned Transparency Registry;
- off-chain storage;
- external dependencies;
- operational credentials;
- social engineering;
- and public communication.

Security is therefore a property of the complete system, not only of deployed bytecode.

---

## 3. Relationship to the GFC Accountability Model

The long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

Security affects every stage.

A security failure may alter:

- **Funds** through theft, diversion, lock failure, or unauthorized transfer;
- **Authority** through key compromise, role escalation, or signer collusion;
- **Rules** through malicious upgrades, configuration changes, or policy manipulation;
- **Decisions** through unauthorized approvals or governance capture;
- **Outcomes** through incorrect execution or service disruption;
- **Evidence** through tampering, deletion, fabrication, or misleading status assignment.

Security controls MUST therefore be evaluated together with authority and accountability controls.

---

## 4. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are normative only when:

- they appear in uppercase;
- the containing document declares `Authority: Normative`;
- and the applicable version governs the implementation, process, or communication being evaluated.

Because this document is Draft, its requirements remain subject to formal review and versioned release.

---

## 5. Scope

This security model covers:

- production and pilot environment separation;
- token security;
- fixed-supply protection;
- fee and transfer-classification security;
- allocation integrity;
- lock and vesting security;
- Impact Vault security;
- treasury custody;
- liquidity authority;
- presale security;
- staking security;
- governance security;
- authority and role security;
- multisig and signer security;
- key management;
- deployment security;
- upgradeability;
- pause mechanisms;
- emergency authority;
- migration;
- frontend and portal security;
- domain and DNS security;
- release authentication;
- dependency risk;
- oracle risk where applicable;
- transparency and evidence integrity;
- protected information;
- monitoring;
- incident response;
- recovery;
- and security communication.

---

## 6. Out of Scope

This document does not independently define:

- final production smart-contract code;
- exact production contract architecture;
- exact production wallet addresses;
- exact signer identities;
- exact multisig thresholds;
- exact timelock durations;
- final hardware-wallet requirements;
- final key-recovery implementation;
- final monitoring provider;
- final RPC provider;
- final oracle provider or pricing methodology;
- final hosting provider;
- final evidence-storage provider;
- final incident-severity thresholds;
- final disclosure timelines;
- final audit provider;
- final legal incident-reporting obligations;
- or final regulatory controls.

These matters must be resolved by the relevant component specification, operational policy, legal process, or authenticated deployment record before production reliance where applicable.

---

## 7. Security Principles

### 7.1 Least privilege

Every privileged role MUST receive only the authority necessary for its defined function.

Security-sensitive convenience MUST NOT justify broad undocumented authority.

### 7.2 Explicit authority

Material technical and operational authority MUST be identifiable.

Security analysis MUST include actual technical capability, not only intended role descriptions.

### 7.3 Defense in depth

No single control SHOULD be treated as sufficient protection for a high-impact authority surface.

Where reasonably possible, security SHOULD combine:

- technical constraints;
- role separation;
- multisig or equivalent approval controls;
- timelocks;
- monitoring;
- transaction review;
- authenticated publication;
- and incident procedures.

### 7.4 Fail safely

Failure behavior SHOULD preserve participant rights and system invariants where possible.

An error, outage, dependency failure, or emergency MUST NOT silently expand privileged authority.

### 7.5 Minimize irreversible risk

Irreversible actions SHOULD be minimized where safer constrained alternatives exist.

Where an action is irreversible, pre-execution review requirements SHOULD be stronger.

### 7.6 Preserve long-term constraints

Security or emergency mechanisms MUST NOT become hidden bypasses around:

- fixed supply;
- long-term locks;
- vesting;
- allocation boundaries;
- presale refund rights;
- or participant protections.

### 7.7 Separate pilot and production

Testnet and pilot controls MUST NOT be assumed sufficient for production.

Production authority, keys, deployment records, operational controls, and security review MUST be established independently.

### 7.8 Accurate security claims

The strongest security claim made publicly MUST NOT exceed the strongest evidence supporting it.

The following are distinct:

- source verified;
- tested;
- reviewed;
- audited;
- deployed;
- monitored;
- and independently verified.

### 7.9 Security does not eliminate responsibility

Automation, multisig control, blockchain execution, or monitoring MUST NOT be presented as eliminating human or organizational responsibility where such responsibility remains material.

---

## 8. Protected Assets

The security model treats the following as protected assets.

### 8.1 Token supply integrity

The fixed intended supply of:

**1,000,000,000 GFC**

MUST be protected against unauthorized expansion.

### 8.2 User balances

Participant and holder balances MUST be protected against unauthorized transfer, seizure, arbitrary alteration, or hidden confiscation mechanisms.

### 8.3 Allocation integrity

The intended allocations MUST be protected against:

- unauthorized reassignment;
- hidden early release;
- custody confusion;
- and accounting divergence.

### 8.4 Locked and vesting assets

Impact Vault and Core Team restrictions MUST be protected against bypass, acceleration, and weakened migration.

### 8.5 Presale participant assets

Accepted contribution assets, participant accounting, distribution records, and refund rights are protected assets.

### 8.6 Treasury and reserve assets

Treasury Reserve, Liquidity Reserve, Guardian Growth, Ecosystem, and other controlled assets require protection against unauthorized use or diversion.

### 8.7 Privileged keys and credentials

Private keys, signer devices, multisig access, administrator credentials, release credentials, domain credentials, repository credentials, and evidence-system credentials are protected assets.

### 8.8 Official deployment identity

Authenticated contract addresses, release references, source-code mappings, and authority records are protected against spoofing and substitution.

### 8.9 Evidence integrity

Evidence, claim status, historical records, corrections, and review records are protected against silent modification, deletion, fabrication, and unauthorized status changes.

### 8.10 Protected information

Personal, beneficiary, legal, confidential, commercially sensitive, and security-sensitive information requires confidentiality and access control.

---

## 9. Security Invariants

The following high-level invariants apply unless a later versioned specification explicitly replaces them.

### 9.1 Fixed-supply invariant

No production authority MUST be able to increase the canonical GFC maximum supply beyond:

**1,000,000,000 GFC**

through undocumented minting, upgrades, migration, replacement, or another hidden path.

### 9.2 Allocation invariant

Initial allocation totals MUST reconcile to the fixed total supply.

No component may silently create overlapping or duplicate canonical allocation claims.

### 9.3 Lock invariant

The intended Impact Vault restriction MUST NOT be weakened through:

- administrator action;
- emergency action;
- upgrade;
- migration;
- or replacement.

### 9.4 Vesting invariant

The intended Core Team vesting restriction MUST NOT be accelerated or weakened through an undocumented path.

### 9.5 Refund invariant

If the applicable presale rules create a valid refund right, project authority MUST NOT make the relevant contribution assets unavailable for satisfying that right.

### 9.6 Authority invariant

No material privilege may exist outside the disclosed authority surface.

### 9.7 Upgrade invariant

An upgrade MUST NOT silently introduce a materially broader authority surface or weaken protected commitments.

### 9.8 Evidence-history invariant

Material evidence and Transparency Registry history MUST NOT be silently rewritten to conceal prior state, subject to legitimate privacy, legal, and security redaction requirements.

### 9.9 Environment invariant

A Base Sepolia pilot deployment MUST NOT be represented or authenticated as the Base Mainnet production deployment.

### 9.10 Communication invariant

A public interface or statement MUST NOT overstate implementation, security, audit, deployment, verification, or operational status.

---

## 10. Trust Assumptions

GFC cannot eliminate all trust.

The security model explicitly recognizes the following trust assumptions.

### 10.1 Base and underlying infrastructure

GFC relies on the security, availability, execution, and finality properties of Base and its underlying dependencies.

### 10.2 Smart-contract correctness

On-chain protection depends on:

- correct implementation;
- correct compilation;
- correct deployment;
- dependency integrity;
- adequate testing;
- and appropriate review.

### 10.3 Key-holder behavior

Where privileged keys exist, security depends on:

- secure key custody;
- correct transaction review;
- resistance to phishing and coercion;
- and signer behavior.

### 10.4 Governance integrity

Where human approval is required, security depends on the integrity of:

- proposals;
- approvals;
- conflicts management;
- signer independence;
- and governance execution.

### 10.5 Off-chain evidence accuracy

Cryptographic anchoring can protect integrity but cannot establish factual truth.

### 10.6 External reviewer quality

Review outcomes depend on reviewer:

- competence;
- scope;
- access;
- methodology;
- independence;
- and conflict management.

### 10.7 External service availability

GFC may depend on services such as:

- RPC providers;
- block explorers;
- indexers;
- hosting;
- DNS;
- storage;
- multisig infrastructure;
- price data;
- monitoring;
- and communication providers.

The existence of dependencies MUST NOT be hidden behind a claim of complete trustlessness.

---

## 11. Threat Actors

The security model considers threats from:

- external attackers;
- malicious insiders;
- compromised founders or team members;
- compromised signers;
- colluding signers;
- compromised service providers;
- malicious contractors;
- compromised reviewers;
- governance attackers;
- opportunistic token participants;
- phishing operators;
- impersonators;
- domain hijackers;
- malicious frontend operators;
- oracle manipulators;
- malicious counterparties;
- and accidental operators.

A threat actor MAY possess legitimate credentials.

Security analysis MUST therefore include abuse of authorized access, not only unauthorized access.

---

## 12. General Threat Categories

At minimum, GFC security review MUST consider:

- smart-contract vulnerability;
- logic error;
- access-control failure;
- integer or accounting error;
- reentrancy where applicable;
- unsafe external calls;
- initialization failure;
- upgrade misconfiguration;
- storage-layout corruption;
- proxy-administration compromise;
- key compromise;
- signer collusion;
- governance capture;
- privilege escalation;
- fee manipulation;
- liquidity manipulation;
- presale accounting error;
- oracle manipulation;
- stale-price acceptance;
- refund insolvency;
- token-allocation divergence;
- lock bypass;
- vesting acceleration;
- staking reward misaccounting;
- frontend compromise;
- DNS compromise;
- fake contract publication;
- dependency compromise;
- evidence tampering;
- evidence-status manipulation;
- privacy leakage;
- data loss;
- monitoring failure;
- incident-response failure;
- social engineering;
- and specification-to-implementation divergence.

---

## 13. Pilot Security Boundary

The current public GFC pilot exists on Base Sepolia.

The pilot MUST be treated as a non-production environment.

Pilot assets, keys, permissions, balances, contracts, and operational processes MUST NOT be assumed to have production security properties.

Before production deployment:

- production contracts MUST be separately authenticated;
- production role assignments MUST be separately established;
- production keys MUST be selected deliberately;
- production monitoring MUST be defined;
- production dependencies MUST be reviewed;
- production security assumptions MUST be documented;
- and production deployment records MUST be published.

A verified Base Sepolia contract does not prove:

- audit completion;
- Mainnet readiness;
- absence of vulnerabilities;
- production authority;
- or production conformance.

---

## 14. Token Security

### 14.1 Supply protection

The production token design MUST prevent discretionary supply expansion beyond the applicable fixed-supply rules.

### 14.2 Hidden authority

The production token MUST NOT contain undisclosed authority to:

- mint;
- confiscate;
- arbitrarily transfer;
- silently freeze selected users;
- alter balances;
- or bypass transfer rules.

### 14.3 Fee security

The current intended fee model is:

- **Buy fee:** 0%
- **Sell fee:** 1%

Any configurable fee authority MUST be bounded.

No production role MAY possess an undocumented path to raise fees above the applicable specification.

### 14.4 Trading classification

If fee logic depends on recognized liquidity pools or trading routes, the implementation MUST consider risks including:

- pool misclassification;
- router incompatibility;
- aggregator behavior;
- liquidity add/remove misclassification;
- malicious pool registration;
- fee-exemption abuse;
- and unexpected transfer paths.

### 14.5 Exemptions

Fee exemptions MUST NOT create an undisclosed privileged trading class.

### 14.6 Upgradeability

If the token is upgradeable, the upgrade path becomes a critical security surface and MUST be analyzed accordingly.

If the token is represented as immutable, no hidden redirection or replacement mechanism may provide equivalent upgrade authority.

---

## 15. Allocation Security

The intended allocation model is:

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

Security controls MUST ensure that production allocation records remain reconcilable with:

- total supply;
- deployment transactions;
- custody addresses;
- lock state;
- vesting state;
- and subsequent authorized movements.

An allocation label does not provide technical security.

---

## 16. Impact Vault Security

The intended Impact Vault contains:

**250,000,000 GFC**

and is intended to be subject to a **50-year lock**.

The implementation MUST be reviewed for possible bypass through:

- administrator privileges;
- upgradeability;
- proxy changes;
- external routers;
- migration;
- emergency functions;
- timestamp manipulation assumptions;
- alternate withdrawal methods;
- delegate calls;
- or unintended token-recovery mechanisms.

A migration MUST NOT weaken the remaining lock.

A security response MUST NOT use emergency authority as an undocumented early-release path.

---

## 17. Core Team Vesting Security

The intended Core Team allocation contains:

**50,000,000 GFC**

with intended **19-year linear vesting**.

The implementation MUST protect against:

- vesting acceleration;
- timestamp or schedule errors;
- unauthorized beneficiary reassignment;
- unauthorized withdrawal;
- double claiming;
- migration into a weaker schedule;
- rounding errors;
- and hidden administrative release.

Public status SHOULD distinguish:

- unvested;
- vested but unclaimed;
- and claimed amounts.

---

## 18. Treasury Security

Treasury security includes both technical custody and governance process.

Threats include:

- compromised signers;
- collusion;
- malicious proposals;
- transaction substitution;
- address poisoning;
- approval fatigue;
- social engineering;
- related-party abuse;
- malicious token approvals;
- unlimited allowances;
- protocol interaction risk;
- and inadequate reconciliation.

Material treasury actions SHOULD use controls appropriate to their impact, including where applicable:

- multisig or equivalent approval;
- transaction simulation;
- destination verification;
- allowance review;
- proposal records;
- conflict review;
- monitoring;
- and post-execution reconciliation.

Treasury traceability does not prove appropriate use.

---

## 19. Liquidity Security

Liquidity operations may create risks including:

- unauthorized withdrawal;
- liquidity-provider position theft;
- incorrect venue selection;
- malicious pool configuration;
- price manipulation;
- extreme slippage;
- sandwiching or MEV exposure;
- malicious token approvals;
- market-making conflicts;
- and false lock claims.

Any authority capable of withdrawing or redirecting liquidity MUST be disclosed.

Liquidity MUST NOT be represented as permanently locked unless that restriction is technically verifiable.

---

## 20. Presale Security

No GFC presale is currently live.

The current Draft presale design includes:

- reference price: **€0.05 per GFC**;
- intended duration: **8 weeks**;
- soft cap: **€250,000**;
- no separate monetary hard cap;
- maximum Presale Allocation: **150,000,000 GFC**;
- intended payment assets: **ETH, USDC, and DAI on Base**;
- immediate token distribution as the current design direction;
- refunds if the applicable soft-cap success condition is not satisfied;
- and immutable material sale logic as the current design direction.

These parameters are Draft and do not prove implementation.

### 20.1 Presale assets

Security analysis MUST protect:

- accepted contribution assets;
- participant accounting;
- purchase records;
- distributed-token accounting;
- soft-cap accounting;
- refund entitlements;
- withdrawal conditions;
- and remaining Presale Allocation.

### 20.2 Pricing

Where crypto assets require euro-reference conversion, security analysis MUST consider:

- price-source manipulation;
- stale prices;
- decimals mismatch;
- rounding;
- unavailable data;
- inconsistent asset addresses;
- wrong-network assets;
- and unexpected volatility.

The final pricing mechanism remains to be defined in [`presale.md`](presale.md).

### 20.3 Contribution custody

Project authority MUST NOT gain unrestricted access to contribution assets while valid refund rights require those assets to remain available.

### 20.4 Immediate distribution and failed finalization

The current design direction uses immediate token distribution.

The same Draft design also requires refunds where the applicable soft-cap success condition is not satisfied.

The final presale specification MUST define the technically enforceable relationship between:

- GFC already distributed to a participant;
- the participant's refund entitlement;
- failed finalization;
- and final token accounting.

This is a material security and economic invariant.

This document does not invent or authorize:

- clawback;
- forced transfer;
- forced burn;
- participant-return requirement;
- token invalidation;
- replacement token;
- or another mechanism

unless later explicitly specified.

A production presale MUST NOT activate while this interaction remains undefined.

### 20.5 Reentrancy and token behavior

Where contribution assets or token transfers can invoke external code or non-standard token behavior, the implementation MUST account for:

- reentrancy;
- fee-on-transfer behavior;
- non-standard return values;
- token callbacks;
- decimal assumptions;
- and transfer failure.

### 20.6 Finalization

Finalization MUST be protected against:

- unauthorized triggering;
- repeated finalization;
- state inconsistency;
- incorrect soft-cap computation;
- premature proceeds access;
- and invalid refund-state transitions.

### 20.7 Administrative surface

Material participant-facing rules SHOULD be immutable under the current design direction.

Any remaining administrative authority MUST be explicitly enumerated.

A presale MUST NOT be described as immutable where hidden privileged modification remains possible.

---

## 21. Staking Security

No production GFC staking system is currently operational.

The current intended design direction is **hybrid and non-inflationary**.

Security analysis MUST consider:

- reward-accounting errors;
- reward insolvency;
- lock and withdrawal errors;
- double claiming;
- reward manipulation;
- unauthorized parameter changes;
- emergency pause effects;
- governance-right manipulation;
- migration;
- and custody risk.

Staking MUST NOT create new GFC beyond the fixed supply.

Reward sources MUST be authenticated and reconciled with tokens already included in the fixed supply or another explicitly specified non-minting source.

A displayed reward rate MUST NOT be treated as a security guarantee or guaranteed return.

---

## 22. Governance Security

Governance security includes protection against:

- governance capture;
- signer collusion;
- vote manipulation;
- delegated-power concentration;
- threshold bypass;
- unauthorized execution;
- malicious proposals;
- hidden administrative paths;
- emergency-power abuse;
- and retrospective authorization.

Detailed governance constraints are defined in [`governance-constraints.md`](governance-constraints.md).

Governance security MUST evaluate both:

- nominal governance rules;
- and actual technical authority.

A governance mechanism is insecure from an accountability perspective where public rules do not match actual privileged capability.

---

## 23. Role and Authority Security

Detailed role definitions are maintained in [`roles-and-authority.md`](roles-and-authority.md).

Security review MUST identify all material authority surfaces, including where applicable:

- deployer;
- contract owner;
- proxy administrator;
- upgrade authority;
- pauser;
- migration authority;
- fee authority;
- recognized-pool authority;
- allocation custody;
- treasury authority;
- liquidity authority;
- presale authority;
- staking authority;
- governance executor;
- evidence authority;
- Transparency Registry authority;
- publication authority;
- domain authority;
- and recovery authority.

An undocumented privileged path is a security defect.

---

## 24. Multisig and Signer Security

Where multisig custody is used, security analysis MUST consider more than signer count.

Relevant factors include:

- threshold;
- signer independence;
- common organizational control;
- common device environments;
- common recovery paths;
- shared credentials;
- phishing risk;
- coercion risk;
- transaction-review quality;
- signer availability;
- key loss;
- and collusion.

Multiple signers do not automatically create independent control.

A threshold MUST NOT be presented as meaningful protection where one actor effectively controls enough signers to satisfy it.

---

## 25. Private-Key Security

Material production keys SHOULD use security controls appropriate to their authority.

Controls MAY include:

- hardware-backed signing;
- separated recovery materials;
- encrypted backups;
- offline recovery;
- restricted signing environments;
- phishing-resistant procedures;
- transaction verification;
- access logging where feasible;
- and key-rotation procedures.

Private keys, seed phrases, signing secrets, or equivalent credentials MUST NOT be stored in this public repository.

A compromised key MUST be treated according to its actual authority, not merely its role label.

---

## 26. Deployment Security

Production deployment is a high-risk security event.

Before an official deployment is authenticated, the release process SHOULD verify:

- applicable specification version;
- source-code commit;
- compiler and build configuration;
- dependencies;
- network;
- chain ID;
- constructor or initializer parameters;
- deployer;
- initial owner or administrator;
- proxy configuration where applicable;
- role assignments;
- token supply;
- allocation destinations;
- and source verification.

Deployment scripts SHOULD be reviewed and tested before production use.

Temporary deployment authority MUST be removed or constrained where intended.

---

## 27. Source Verification

Production contract source code SHOULD be publicly verifiable through an appropriate explorer or equivalent mechanism.

Source verification supports reviewability.

It does not independently prove:

- security;
- audit completion;
- absence of vulnerabilities;
- conformance;
- or correct operational governance.

A verified testnet contract MUST NOT be used to imply a verified production deployment.

---

## 28. Upgrade Security

If a component is upgradeable, the upgrade mechanism is a critical security boundary.

Security review MUST consider:

- upgrade proposer;
- approver;
- executor;
- administrator;
- threshold;
- timelock;
- implementation validation;
- storage compatibility;
- initializer safety;
- rollback expectations;
- emergency bypass;
- and monitoring.

An upgrade MUST NOT silently weaken:

- fixed supply;
- locks;
- vesting;
- fees beyond permitted bounds;
- refund rights;
- treasury restrictions;
- approval thresholds;
- or participant protections.

If no upgrade path is intended, the implementation MUST be reviewed for indirect replacement or redirection paths that could create equivalent authority.

---

## 29. Pause Security

Pause functionality MAY reduce harm during an incident.

Pause authority itself creates risk.

A pause mechanism MUST define:

- affected functions;
- unaffected functions;
- authorized role;
- activation conditions;
- approval requirements;
- unpause process;
- and participant impact.

Pause authority MUST NOT create undocumented capability to:

- confiscate balances;
- redirect allocations;
- remove refund rights;
- accelerate vesting;
- or permanently disable selected users outside specified rules.

---

## 30. Emergency Authority Security

Emergency authority SHOULD be narrower than ordinary full administrative authority.

Security review MUST test whether an emergency path can bypass:

- timelocks;
- approval thresholds;
- locks;
- vesting;
- refund protections;
- fixed supply;
- or migration restrictions.

An emergency mechanism that can silently defeat a protected invariant is not merely an emergency control; it is a privileged bypass and MUST be disclosed as such.

---

## 31. Migration Security

Migration may be necessary where a component must be replaced.

Migration creates risks including:

- asset loss;
- duplicate claims;
- replay;
- inconsistent state;
- weakened restrictions;
- incorrect successor authentication;
- phishing;
- and abandonment of historical records.

A migration MUST preserve applicable participant rights and restrictions unless an explicitly versioned change lawfully and normatively modifies them.

Migration MUST NOT be used as a disguised bypass around protected commitments.

---

## 32. Frontend and Portal Security

A frontend is not the blockchain.

A frontend can nevertheless materially affect user safety by:

- selecting contract addresses;
- preparing transactions;
- displaying balances;
- presenting status;
- collecting evidence;
- or directing users.

Security review SHOULD consider:

- malicious JavaScript;
- dependency compromise;
- address substitution;
- transaction-data manipulation;
- XSS;
- supply-chain compromise;
- session compromise;
- malicious redirects;
- and misleading status display.

Where users sign blockchain transactions, transaction details SHOULD remain visible before approval.

A frontend compromise MUST NOT be treated as changing legitimate on-chain authority.

---

## 33. Domain and DNS Security

Domain and DNS compromise may enable:

- phishing;
- fake contract publication;
- malicious frontend delivery;
- false security notices;
- and credential theft.

Material domains and DNS accounts SHOULD use controls appropriate to their role, including where available:

- strong authentication;
- phishing-resistant MFA;
- restricted administrator access;
- recovery protection;
- change monitoring;
- and registrar locking.

Domain control MUST NOT be treated as equivalent to contract authority.

---

## 34. Repository and Release Security

A public repository may become part of the trust chain for:

- specifications;
- source code;
- releases;
- deployment records;
- and security communication.

Security controls SHOULD address:

- account compromise;
- malicious commits;
- branch protection;
- dependency changes;
- secret leakage;
- release tampering;
- tag manipulation;
- and unauthorized publication.

No repository state should be treated as production-authoritative unless the applicable release and deployment process authenticates it.

The continuously changing `main` branch is not automatically the production source of authority.

---

## 35. Official Address Authentication

Fake or substituted contract addresses are a material threat.

Official production addresses MUST be published through an authenticated release process.

Where practical, official address records SHOULD be cross-checkable through multiple authenticated sources.

A social-media message alone SHOULD NOT be the sole authentication mechanism for a production address.

Pilot addresses MUST be clearly labeled as pilot addresses.

---

## 36. Dependency Security

Dependencies may include:

- Solidity libraries;
- development tooling;
- package managers;
- RPC providers;
- indexers;
- explorers;
- wallets;
- multisig platforms;
- price feeds;
- hosting;
- storage;
- and monitoring services.

Security review MUST distinguish:

- critical dependencies;
- optional dependencies;
- replaceable dependencies;
- and single points of failure.

A third-party outage MUST NOT silently cause unsafe state transitions.

Dependency trust assumptions SHOULD be documented before production reliance.

---

## 37. Oracle and Price-Data Security

Where an oracle or external price source is used, security analysis MUST consider:

- manipulation;
- staleness;
- outage;
- incorrect decimals;
- wrong asset mapping;
- wrong network;
- low-liquidity reference markets;
- extreme volatility;
- and delayed updates.

The final oracle or pricing methodology is not defined by this document.

The applicable presale implementation MUST fail safely when required pricing data is invalid or unavailable.

A fallback mechanism MUST NOT silently accept weaker pricing assumptions without disclosure.

---

## 38. Transparency Registry Security

No complete production Transparency Registry is currently deployed.

The planned Registry is intended to operate as a versioned historical record rather than a permanent approval badge.

Security threats include:

- unauthorized record creation;
- unauthorized status change;
- silent deletion;
- evidence-link substitution;
- reviewer impersonation;
- history rewriting;
- access-control failure;
- false independent-verification labels;
- and frontend misrepresentation.

Registry security MUST preserve, where legally and technically appropriate:

- record identity;
- version history;
- publisher or authority attribution;
- evidence linkage;
- status history;
- correction history;
- suspension or downgrade history;
- and supersession relationships.

A compromised interface MUST NOT be able to rewrite authenticated historical evidence without detection.

---

## 39. Evidence Security

Evidence systems MUST distinguish integrity from truth.

Security controls MAY protect:

- record integrity;
- provenance;
- access;
- versioning;
- authenticity signals;
- and review history.

They cannot independently prove factual correctness.

Threats include:

- fabricated evidence;
- altered evidence;
- forged signatures;
- malicious submitters;
- reviewer compromise;
- metadata manipulation;
- unauthorized disclosure;
- silent deletion;
- and inappropriate status elevation.

Evidence-status authority MUST be treated as a privileged control surface.

---

## 40. Cryptographic Anchoring Security

Where cryptographic anchoring is used, implementation MUST define:

- hash algorithm;
- record canonicalization;
- version handling;
- timestamp or publication semantics;
- and verification method.

Low-entropy or predictable sensitive information SHOULD NOT be hashed directly where brute-force confirmation could reveal protected content.

Appropriate salting or another privacy-preserving method SHOULD be used where necessary.

A cryptographic anchor proves neither factual truth nor reviewer independence.

---

## 41. Protected Information Security

Protected information may include:

- personal data;
- beneficiary information;
- identity documents;
- banking information;
- confidential contracts;
- protected legal information;
- security-sensitive records;
- and commercially sensitive information.

Access SHOULD follow:

- least privilege;
- purpose limitation;
- authentication;
- revocation;
- logging where appropriate;
- retention rules;
- and secure deletion where applicable.

Protected information SHOULD NOT be placed directly on a public blockchain unless publication is lawful, necessary, proportionate, and intentionally approved.

---

## 42. Privacy Threats

Security review SHOULD consider:

- accidental disclosure;
- over-collection;
- insecure storage;
- unauthorized reviewer access;
- metadata leakage;
- linkability;
- hash-guessing;
- backup exposure;
- retention beyond necessity;
- and irreversible on-chain publication.

Transparency MUST NOT be used as justification for unnecessary personal-data exposure.

---

## 43. Monitoring

Material production systems SHOULD be monitored according to their risk.

Potential monitoring targets include:

- privileged role changes;
- owner changes;
- upgrades;
- pauses;
- unpauses;
- signer changes;
- threshold changes;
- large transfers;
- unusual treasury movements;
- allocation movements;
- unexpected minting;
- fee changes;
- recognized-pool changes;
- presale state changes;
- staking parameter changes;
- liquidity withdrawals;
- evidence-status changes;
- and abnormal transaction patterns.

Monitoring does not prevent all incidents.

Alerts require defined response ownership.

---

## 44. Logging and Auditability

Material off-chain administrative systems SHOULD produce logs appropriate to their security significance.

Relevant records MAY include:

- administrator access;
- role changes;
- release publication;
- evidence access;
- evidence status changes;
- infrastructure changes;
- and security actions.

Logs themselves require:

- integrity protection;
- retention;
- access control;
- and time consistency.

A log is evidence of recorded activity, not automatic proof that the activity was authorized.

---

## 45. Incident Definition

A security incident is an event that materially affects or threatens:

- confidentiality;
- integrity;
- availability;
- custody;
- authority;
- participant rights;
- correct execution;
- authenticated publication;
- or evidence integrity.

Examples include:

- exploited vulnerability;
- compromised key;
- signer compromise;
- governance attack;
- malicious upgrade;
- unauthorized transfer;
- presale accounting failure;
- refund failure;
- liquidity theft;
- domain takeover;
- malicious frontend;
- evidence tampering;
- protected-data exposure;
- or fake deployment publication.

---

## 46. Incident Response Principles

Incident response SHOULD include, as appropriate:

1. detection;
2. verification;
3. containment;
4. authority assessment;
5. protection of participants and assets;
6. preservation of evidence;
7. remediation;
8. recovery;
9. authenticated communication;
10. post-incident review;
11. and documentation of continuing risk.

Incident response MUST NOT be used to retrospectively redefine unauthorized behavior as compliant.

---

## 47. Incident Authority

Incident responders MUST NOT receive unlimited authority solely because an incident exists.

Emergency actions MUST remain within the authority defined by:

- [`roles-and-authority.md`](roles-and-authority.md);
- [`governance-constraints.md`](governance-constraints.md);
- and the applicable component specification.

Where an emergency action uses a defined bypass, the bypass itself MUST be part of the disclosed authority surface.

---

## 48. Incident Disclosure

Material security incidents SHOULD be disclosed when doing so is reasonably safe and appropriate.

Immediate full technical disclosure MAY be delayed where publication would materially increase active risk.

Public incident communication SHOULD distinguish:

- confirmed facts;
- suspected facts;
- affected systems;
- unaffected systems where known;
- mitigation status;
- participant actions where necessary;
- and unresolved uncertainty.

Security communication MUST NOT claim resolution before the material issue is actually resolved.

Repository-level vulnerability reporting guidance is maintained in [`../SECURITY.md`](../SECURITY.md).

---

## 49. Recovery

Recovery mechanisms MUST be designed so that recovery does not become a hidden master key.

A recovery process SHOULD identify:

- triggering condition;
- affected authority;
- required approvals;
- replacement method;
- authentication;
- record requirements;
- participant impact;
- and post-recovery verification.

Recovery of a privileged role SHOULD be at least as constrained as the original role where reasonably possible.

---

## 50. Key Compromise

Where a material key is suspected or confirmed compromised, the response MUST evaluate:

- actual privileges;
- affected contracts;
- affected wallets;
- upgrade authority;
- pause authority;
- migration authority;
- publication authority;
- related credentials;
- and potential historical misuse.

Simply rotating an off-chain password is insufficient where compromised on-chain authority remains active.

---

## 51. Signer Compromise

A compromised signer does not necessarily compromise a multisig if the remaining threshold remains secure.

However, the incident MUST consider:

- threshold;
- other signer exposure;
- shared device or recovery risk;
- malicious pending transactions;
- signer replacement;
- threshold manipulation;
- and disclosure.

A compromised signer MUST be removed from actual technical authority, not merely removed from documentation.

---

## 52. Frontend Compromise Response

If an official frontend is compromised, response MAY include:

- disabling affected hosting;
- authenticated warning publication;
- DNS changes;
- restoring known-good artifacts;
- dependency review;
- address verification;
- and user guidance.

The response MUST avoid directing users to unauthenticated replacement contracts or addresses.

---

## 53. Domain Compromise Response

Domain compromise response SHOULD include:

- registrar recovery;
- DNS validation;
- credential rotation;
- authenticated alternate communication;
- malicious-content assessment;
- and user warning where necessary.

A recovered domain SHOULD NOT immediately be treated as trustworthy until compromise persistence has been evaluated.

---

## 54. Presale Incident Response

A presale incident MAY affect:

- pricing;
- contribution acceptance;
- participant accounting;
- immediate distribution;
- soft-cap accounting;
- refunds;
- finalization;
- or withdrawal.

Response MUST prioritize preservation of participant rights and accounting integrity.

Where pausing exists, its participant consequences MUST be understood before use.

A presale incident MUST NOT be used as justification to redirect refundable assets.

---

## 55. Treasury Incident Response

Treasury incidents MAY require:

- signer suspension;
- allowance revocation;
- destination review;
- transaction cancellation where possible;
- key rotation;
- custody migration;
- reconciliation;
- and public disclosure.

Recovery actions MUST preserve evidence of the incident where legally and operationally appropriate.

---

## 56. Evidence Incident Response

Evidence incidents MAY include:

- unauthorized access;
- falsification;
- deletion;
- status manipulation;
- protected-data leakage;
- or compromised reviewer credentials.

Response SHOULD preserve:

- prior versions;
- access records;
- status history;
- evidence linkage;
- and correction rationale

where legally and technically possible.

A compromised record MUST NOT silently be replaced with a corrected version as though the compromise never occurred.

---

## 57. Security Review

Security review SHOULD be scoped to the actual implementation and authority model.

Depending on the component, review MAY include:

- architecture review;
- threat modeling;
- smart-contract review;
- automated analysis;
- manual code review;
- test review;
- deployment review;
- privilege review;
- multisig review;
- infrastructure review;
- frontend review;
- dependency review;
- and incident-process review.

A review MUST NOT be described as an audit unless it satisfies the applicable audit definition and scope.

---

## 58. Independent Security Review

Material production contracts SHOULD undergo appropriately independent security review before production reliance.

The required scope depends on:

- funds at risk;
- privilege level;
- immutability;
- upgradeability;
- participant rights;
- complexity;
- and dependency risk.

Independent review SHOULD identify:

- exact code or commit;
- scope;
- assumptions;
- exclusions;
- findings;
- remediation status;
- and reviewer identity or organization.

Independent review does not make a system risk-free.

---

## 59. Audit Status

No production security audit is established as completed by this document.

If an audit is later performed, public communication MUST identify:

- auditor;
- exact scope;
- reviewed version;
- date;
- material exclusions;
- report reference;
- and remediation status.

An audit of one component MUST NOT be represented as an audit of unrelated components.

A verified contract MUST NOT be described as audited solely because its source code is publicly verified.

---

## 60. Testing

Applicable implementations SHOULD include tests covering both intended behavior and prohibited behavior.

Testing SHOULD consider:

- access control;
- fixed-supply invariants;
- allocation reconciliation;
- lock constraints;
- vesting constraints;
- fee behavior;
- recognized-pool behavior;
- presale state transitions;
- refund behavior;
- immediate-distribution accounting;
- staking accounting;
- upgrade restrictions;
- pause behavior;
- migration;
- and failure modes.

Passing tests do not prove absence of vulnerabilities.

---

## 61. Fuzzing and Invariant Testing

Where appropriate, smart-contract testing SHOULD include fuzzing or invariant-based testing for critical properties.

Potential invariants include:

- total supply never exceeds the permitted maximum;
- allocations reconcile;
- locked balances cannot be released early;
- unvested Core Team tokens cannot become claimable early;
- unauthorized roles cannot exercise privileged functions;
- refund assets remain available when refund rights apply;
- presale distribution does not exceed the Presale Allocation;
- and state transitions cannot occur in invalid order.

Exact test suites belong to implementation repositories and release records.

---

## 62. Deployment Rehearsal

Before Mainnet production deployment, deployment procedures SHOULD be rehearsed in an appropriate non-production environment.

A rehearsal SHOULD verify:

- deployment ordering;
- parameters;
- role assignment;
- ownership transfer;
- temporary privilege removal;
- allocation accounting;
- source verification;
- monitoring;
- and deployment-record generation.

A successful rehearsal does not make the production deployment automatic or risk-free.

---

## 63. Production Readiness

A component SHOULD NOT be represented as production-ready solely because it:

- compiles;
- passes unit tests;
- is deployed on testnet;
- has verified source;
- has a working frontend;
- or has received informal review.

Production readiness requires an evaluation appropriate to the component's risk and status.

---

## 64. Security Communication

Public security communication MUST distinguish between:

- planned controls;
- specified controls;
- implemented controls;
- tested controls;
- reviewed controls;
- audited controls;
- deployed controls;
- active monitoring;
- and independently verified claims.

The term `secure` SHOULD NOT be used as an absolute guarantee.

Qualified statements SHOULD identify the relevant scope and evidence.

---

## 65. Prohibited Security Claims

GFC communication MUST NOT imply that:

- blockchain use eliminates security risk;
- a multisig eliminates insider risk;
- a testnet pilot proves production security;
- source verification equals audit;
- audit equals risk-free;
- public code equals secure code;
- immutability equals correctness;
- upgradeability equals safety;
- monitoring prevents all exploits;
- a wallet label proves custody restrictions;
- or cryptographic anchoring proves factual truth.

---

## 66. Security and Legal Obligations

Technical security does not replace:

- data-protection obligations;
- sanctions obligations;
- consumer-protection obligations;
- financial regulation;
- contractual obligations;
- incident-reporting duties;
- or other applicable legal requirements.

Where law requires security or operational action, such action still remains subject to the actual technical authority available.

---

## 67. Security and Transparency

Transparency can improve security by exposing:

- roles;
- upgrades;
- addresses;
- movements;
- status changes;
- and incidents.

Transparency can also create risk by exposing:

- personal data;
- signer details;
- recovery procedures;
- security architecture;
- or active vulnerabilities.

Security disclosure MUST therefore balance accountability with legitimate confidentiality.

---

## 68. Security and Historical Integrity

Material security history SHOULD remain reviewable.

This includes, where appropriate:

- incidents;
- affected versions;
- findings;
- remediations;
- upgrades;
- migrations;
- key rotations;
- signer changes;
- and deprecations.

A security failure MUST NOT be silently erased from historical records merely for reputational convenience.

---

## 69. Conformance

An implementation conforms to this security model only where:

- applicable protected assets are identified;
- material authority surfaces are disclosed;
- security invariants are preserved;
- privileged roles follow least privilege;
- pilot and production environments are correctly separated;
- fixed-supply constraints are protected;
- allocation restrictions are protected;
- lock and vesting restrictions are protected;
- presale participant rights are protected;
- production addresses are authenticated;
- material dependencies are identified;
- security claims match evidence;
- material incidents are handled according to applicable processes;
- and material deviations are documented.

---

## 70. Security Non-Conformance

Security non-conformance includes:

- undocumented privileged access;
- hidden minting authority;
- hidden upgrade authority;
- hidden pause or migration authority;
- weakened lock or vesting restrictions;
- production use of unauthenticated addresses;
- pilot infrastructure presented as production;
- refundable assets made unavailable contrary to participant rights;
- undisclosed fee authority;
- false audit claims;
- silent evidence manipulation;
- unprotected material credentials;
- or public claims materially stronger than the supporting security evidence.

Material non-conformance MAY require:

- pause;
- role revocation;
- key rotation;
- signer replacement;
- remediation;
- migration;
- public correction;
- independent review;
- incident treatment;
- or deprecation.

---

## 71. Dependencies on Other Specifications

This document MUST be interpreted together with:

- [`README.md`](README.md);
- [`glossary.md`](glossary.md);
- [`non-goals.md`](non-goals.md);
- [`architecture.md`](architecture.md);
- [`roles-and-authority.md`](roles-and-authority.md);
- [`governance-constraints.md`](governance-constraints.md);
- [`token.md`](token.md);
- [`allocations.md`](allocations.md);
- [`vesting-and-unlocks.md`](vesting-and-unlocks.md);
- [`economic-flows.md`](economic-flows.md);
- [`staking.md`](staking.md);
- [`presale.md`](presale.md);
- [`transparency-model.md`](transparency-model.md);
- repository-level [`../STATUS.md`](../STATUS.md);
- and repository-level [`../SECURITY.md`](../SECURITY.md).

Where another Draft specification conflicts with this document, the conflict MUST be resolved explicitly before Stable status.

---

## 72. Unresolved Security Decisions

The following matters remain unresolved unless separately defined by a later specification or authenticated implementation record.

### 72.1 Token

- final upgradeability;
- final ownership model;
- final fee-control model;
- final recognized-pool authority;
- final fee-exemption model;
- final pause model, if any;
- and final deployment-role removal.

### 72.2 Allocations

- final custody structure;
- final lock implementation;
- final vesting implementation;
- allocation migration model;
- and allocation-specific recovery processes.

### 72.3 Presale

- final pricing implementation;
- final price-data source or methodology;
- final custody implementation;
- final administrative surface;
- final refund mechanism;
- final finalization mechanics;
- treatment of GFC already distributed if finalization fails;
- and final immutable/configurable boundary.

### 72.4 Treasury and liquidity

- final multisig or equivalent model;
- signer categories;
- thresholds;
- transaction limits;
- liquidity-position custody;
- protocol interaction policy;
- and recovery model.

### 72.5 Staking

- final reward source;
- final accounting logic;
- final lock or withdrawal behavior;
- final pause model;
- final migration model;
- and governance-related rights.

### 72.6 Governance and authority

- final production role map;
- final signer model;
- final timelocks;
- final upgrade authority;
- final pause authority;
- final migration authority;
- final recovery authority;
- and final emergency process.

### 72.7 Infrastructure

- final domain-security controls;
- final hosting controls;
- final repository controls;
- final release-authentication process;
- final monitoring architecture;
- and final dependency inventory.

### 72.8 Transparency and evidence

- final Registry architecture;
- final evidence-storage architecture;
- final access-control model;
- final anchoring method;
- final reviewer-authentication model;
- final correction and dispute controls;
- and final protected-information retention model.

### 72.9 Incident response

- severity model;
- response owners;
- notification channels;
- public-disclosure process;
- escalation criteria;
- recovery procedures;
- and post-incident review format.

### 72.10 External security review

- final review scope;
- review timing;
- audit requirements where applicable;
- reviewer selection;
- remediation acceptance;
- and publication policy.

These unresolved matters MUST NOT be represented as finalized production security controls.

---

## 73. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- the production architecture is sufficiently defined for security analysis;
- token security invariants are finalized;
- allocation security requirements are finalized;
- Impact Vault implementation constraints are finalized;
- Core Team vesting constraints are finalized;
- presale security mechanics are finalized;
- the immediate-distribution and failed-sale refund interaction is technically resolved;
- treasury and liquidity custody requirements are finalized;
- staking security requirements are finalized;
- governance authority is finalized;
- privileged-role mapping is finalized;
- upgrade authority is finalized;
- pause authority is finalized;
- migration authority is finalized;
- emergency and recovery authority are finalized;
- production key-management expectations are finalized;
- dependency-security requirements are finalized;
- frontend and release-authentication requirements are finalized;
- Transparency Registry and evidence-security requirements are finalized;
- privacy-security requirements are finalized;
- monitoring requirements are finalized;
- incident-response requirements are finalized;
- external review requirements are finalized;
- Base Sepolia pilot and Base Mainnet production security claims are consistently separated;
- and related specifications are mutually consistent.

---

## 74. Final Security Principles

The GFC security model preserves the following distinctions:

> A public pilot does not prove production security.

> Base Sepolia does not mean Base Mainnet.

> Source verification does not mean security review.

> Security review does not automatically mean audit.

> Audit does not mean risk-free.

> A multisig does not eliminate insider risk.

> Multiple signers do not automatically mean independent signers.

> A role label does not constrain technical authority.

> A frontend does not define legitimate on-chain authority.

> An emergency does not justify unlimited authority.

> An upgrade path is part of the security model.

> A migration path is part of the security model.

> Recovery authority is itself privileged authority.

> Cryptographic integrity does not prove factual truth.

> Monitoring does not prevent every incident.

> Transparency does not require disclosure of security-sensitive information.

> Security claims must not exceed supporting evidence.

> Responsibility follows authority.

The objective is not to claim that GFC can eliminate risk.

The objective is to make material risks, authority, protections, assumptions, limitations, and failures explicit enough to be reviewed before production reliance.

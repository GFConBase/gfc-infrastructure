# Global Foundation Coin Transparency Model Specification

**Document ID:** GFC-TRN-001  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Intended Production Network:** Base Mainnet  
**Production Chain ID:** 8453  
**Public Pilot Network:** Base Sepolia  
**Pilot Chain ID:** 84532  
**Last Updated:** 2026-09-04

---

## 1. Document Status

This document defines the current intended transparency, evidence, verification, disclosure, historical-record, and accountability model for Global Foundation Coin (GFC).

It is normative because it defines intended requirements, classifications, boundaries, and prohibited representations.

Its maturity remains Draft.

At the current repository state:

- the **GFC Token / Economic Layer** is the current primary product focus;
- the broader long-term direction is a wider **Accountability Infrastructure**;
- a public GFC pilot exists on **Base Sepolia**;
- no production GFC token is deployed on Base Mainnet;
- no GFC presale is live;
- no production Treasury Reserve, Liquidity Reserve, staking, governance, allocation, or vesting infrastructure is represented as operational;
- no complete production Transparency Registry is deployed;
- no production evidence-review system is represented as operational;
- no production impact-evaluation system is represented as operational;
- no production evidence schema, anchoring architecture, or protected-evidence storage model is established as final;
- no production registry admission, verification, downgrade, suspension, or removal process is established as operational;
- and no implementation is designated as conforming to a Stable production transparency release.

The public Base Sepolia pilot is non-production.

It MUST NOT be interpreted as evidence that the broader production transparency architecture described here is deployed.

The continuously changing `main` branch MUST NOT automatically be treated as the authoritative transparency specification for a future production deployment.

Current project and deployment status is maintained in [`../STATUS.md`](../STATUS.md).

---

## 2. Purpose

This document defines how GFC intends to treat transparency as a practical accountability property rather than a marketing claim.

Its purpose is to establish:

- what can be verified directly on-chain;
- what requires governance and authority records;
- what requires supporting off-chain evidence;
- what requires outcome or impact evaluation;
- how evidence is classified;
- how claims are classified;
- how authority is exposed;
- how records are linked across time;
- how corrections, disputes, downgrades, suspensions, and supersession are represented;
- how protected information can remain reviewable without being unnecessarily exposed;
- how a future Transparency Registry may represent changing status over time;
- and how public interfaces MUST avoid overstating evidence strength.

The objective is not to make every piece of information public.

The objective is to make material claims:

- traceable;
- attributable;
- reviewable;
- evidence-based;
- historically reconstructable;
- uncertainty-aware;
- and accurately classified.

---

## 3. Canonical Accountability Model

The canonical long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

This model is foundational.

A material transparency record SHOULD make it possible to reconstruct, where applicable:

1. **Funds** — what value, assets, rights, or resources were involved;
2. **Authority** — who or what had the power to act;
3. **Rules** — what constraints and procedures applied;
4. **Decisions** — what was approved, rejected, executed, changed, or withheld;
5. **Outcomes** — what actually happened as a result;
6. **Evidence** — what supports the represented history.

No individual stage proves all later stages.

For example:

- a transaction does not prove legitimate authority;
- legitimate authority does not prove compliant use;
- compliant use does not prove a positive outcome;
- a positive outcome does not automatically prove broader impact.

Different claims require different evidence.

---

## 4. Core Verification Distinctions

GFC distinguishes among multiple verification questions.

### 4.1 Transaction verification

**Did the recorded transaction occur as represented?**

Relevant evidence may include:

- transaction hash;
- contract events;
- authenticated addresses;
- block data;
- token transfers;
- timestamps;
- balances;
- and verified contract state.

### 4.2 Authority verification

**Was the actor or mechanism authorized to perform the action?**

Relevant evidence may include:

- authority registry;
- role assignment;
- signer or multisig configuration;
- governance approval;
- timelock state;
- contract permissions;
- and authenticated release records.

### 4.3 Rules verification

**Which rules applied at the time of the action?**

Relevant evidence may include:

- applicable specification version;
- contract parameters;
- governance constraints;
- legal or operational rules;
- and historical configuration.

### 4.4 Use-of-funds verification

**Were funds used for the documented purpose?**

Relevant evidence may include:

- approvals;
- agreements;
- invoices;
- receipts;
- delivery records;
- reconciliations;
- recipient confirmations;
- and protected supporting records.

### 4.5 Outcome verification

**Did the documented activity produce the represented result?**

Relevant evidence may include:

- delivery evidence;
- output records;
- metrics;
- follow-up data;
- and review.

### 4.6 Impact evaluation

**Did the activity contribute to a meaningful broader or longer-term result?**

Relevant evidence may include:

- methodology;
- baseline;
- indicators;
- attribution analysis;
- independent evaluation;
- limitations;
- and uncertainty disclosure.

These questions MUST NOT be treated as interchangeable.

The following distinctions are foundational:

> TRANSACTION VERIFIED does not equal USE VERIFIED.

> USE VERIFIED does not equal OUTCOME VERIFIED.

> OUTCOME VERIFIED does not automatically equal IMPACT VERIFIED.

---

## 5. Current Product Focus and Long-Term Transparency Direction

The current primary product focus is the **GFC Token / Economic Layer**.

Therefore, near-term transparency requirements SHOULD prioritize accurate representation of:

- token identity;
- token supply;
- allocations;
- production deployment status;
- authority;
- fees;
- vesting and locks;
- presale mechanics;
- staking status;
- treasury and liquidity status;
- economic flows;
- and security status.

The broader **Accountability Infrastructure**, including a more comprehensive Transparency Registry for GFC and potentially external projects, organizations, or programs, is a longer-term direction.

The broader infrastructure MUST NOT be represented as fully deployed or operational today.

---

## 6. Scope

This specification covers:

- accountability principles;
- transparency principles;
- verification distinctions;
- transaction verification;
- authority transparency;
- rules and governance transparency;
- use-of-funds verification;
- outcome and impact evaluation;
- contract and wallet authentication;
- allocation reporting;
- presale transparency;
- treasury transparency;
- liquidity transparency;
- vesting and lock transparency;
- staking transparency;
- fee transparency;
- evidence classification;
- evidence provenance;
- evidence status;
- claim status;
- cryptographic anchoring;
- protected off-chain evidence;
- evidence review;
- historical records;
- corrections;
- disputes;
- future Transparency Registry behavior;
- portal requirements;
- privacy boundaries;
- security;
- conformance;
- and unresolved transparency decisions.

---

## 7. Out of Scope

This document does not independently define:

- final smart-contract code;
- final production contract addresses;
- final production wallet addresses;
- final evidence-storage provider;
- final database architecture;
- final anchoring protocol;
- final evidence schema;
- final impact methodology;
- final reviewer roster;
- final audit provider;
- final legal privilege rules;
- final retention periods;
- final data-controller responsibilities;
- final beneficiary-consent process;
- final accounting standards;
- final registry status vocabulary;
- final registry admission criteria;
- final registry review workflow;
- final reporting cadence;
- or jurisdiction-specific disclosure obligations.

These matters require separate technical, operational, legal, privacy, accounting, governance, or implementation records before production use.

---

## 8. Relationship to Other Specifications

This document MUST be interpreted together with:

- [`README.md`](README.md);
- [`glossary.md`](glossary.md);
- [`non-goals.md`](non-goals.md);
- [`architecture.md`](architecture.md);
- [`roles-and-authority.md`](roles-and-authority.md);
- [`governance-constraints.md`](governance-constraints.md);
- [`security-model.md`](security-model.md);
- [`token.md`](token.md);
- [`allocations.md`](allocations.md);
- [`vesting-and-unlocks.md`](vesting-and-unlocks.md);
- [`economic-flows.md`](economic-flows.md);
- [`staking.md`](staking.md);
- [`presale.md`](presale.md);
- [`conformance-verification.md`](conformance-verification.md);
- repository-level [`../STATUS.md`](../STATUS.md);
- and repository-level [`../SECURITY.md`](../SECURITY.md).

Where another Draft specification conflicts with this document, the conflict MUST be resolved explicitly before Stable status.

---

## 9. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are normative only when:

- they appear in uppercase;
- the containing document declares `Authority: Normative`;
- and the applicable version governs the implementation, process, or communication being evaluated.

Because this document is Draft, its requirements remain subject to formal review and versioned release.

---

## 10. Transparency Principles

### 10.1 Verification over explanation

A public explanation MUST NOT be treated as equivalent to independently reviewable evidence.

### 10.2 Claims require evidence

Every material transparency claim SHOULD identify:

- claim;
- period;
- responsible authority or publisher;
- evidence;
- evidence classification;
- review status;
- limitations;
- and current historical status.

### 10.3 Visibility is not verification

Public visibility does not automatically equal verification.

### 10.4 Integrity is not factual truth

Cryptographic integrity does not independently prove factual accuracy.

### 10.5 Transparency does not eliminate trust

Transparency can expose and constrain trust dependencies.

It cannot eliminate all dependence on:

- signers;
- reviewers;
- evidence providers;
- legal processes;
- operational execution;
- methodology;
- or real-world information.

### 10.6 Privacy-aware disclosure

Transparency MUST NOT require unnecessary disclosure of protected information.

### 10.7 Historical accountability

Material prior state SHOULD remain reconstructable.

### 10.8 Accurate certainty

The strength of a claim MUST NOT exceed the strength of its supporting evidence.

### 10.9 Responsibility follows authority

Material authority SHOULD be attributable and linked to decisions and outcomes.

### 10.10 No transparency theatre

High data volume MUST NOT be presented as meaningful accountability where authority, context, provenance, rules, or evidence are missing.

---

## 11. Supporting Three-Layer View

For explanatory purposes, GFC MAY group accountability infrastructure into three supporting layers:

1. **Technology**
2. **Governance**
3. **Evidence and Outcomes**

This is a supporting conceptual view.

It does not replace the canonical accountability model:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

### 11.1 Technology

Technology records and enforces technical state.

### 11.2 Governance

Governance defines and constrains authority and decisions.

### 11.3 Evidence and Outcomes

Evidence and outcome processes support claims about use, delivery, results, and impact.

No layer is sufficient alone.

---

## 12. Evidence Disclosure Levels

Evidence MAY be classified into three principal disclosure levels.

### 12.1 Public On-Chain

Examples include:

- authenticated contract addresses;
- transaction hashes;
- token transfers;
- balances;
- allocation state;
- lock state;
- vesting state;
- presale distribution;
- refunds;
- governance execution;
- authority changes;
- and cryptographic commitments.

### 12.2 Cryptographically Anchored

Off-chain records MAY be linked to public cryptographic commitments.

Anchoring MAY establish integrity or historical existence.

Anchoring does not independently establish:

- factual accuracy;
- authorship;
- legal validity;
- completeness;
- or impact.

### 12.3 Protected Off-Chain

Protected evidence MAY include:

- personal information;
- beneficiary information;
- confidential agreements;
- identity records;
- invoices;
- banking records;
- commercially sensitive information;
- security-sensitive information;
- and legally protected records.

Protected evidence MUST remain subject to appropriate:

- access control;
- integrity protection;
- retention;
- review;
- and disclosure limitations.

---

## 13. Evidence Provenance

Material evidence SHOULD identify its provenance.

Possible provenance categories MAY include:

- generated by an authenticated smart contract;
- derived from public blockchain data;
- submitted by GFC;
- submitted by a recipient;
- submitted by a supplier;
- submitted by a partner;
- submitted by a beneficiary;
- submitted by an external reviewer;
- generated by an automated system;
- derived from another record;
- or imported from an external authority.

Where source independence is material, provenance MUST NOT be concealed.

---

## 14. Evidence Status

Evidence status MUST remain distinct from claim status.

Potential evidence statuses MAY include:

- Submitted;
- Integrity Anchored;
- Under Review;
- Reviewed;
- Independently Reviewed;
- Accepted;
- Rejected;
- Disputed;
- Superseded;
- Withdrawn;
- or Unavailable.

The final production vocabulary remains unresolved.

A status MUST NOT be interpreted more strongly than its definition permits.

For example:

- `Integrity Anchored` is not factual verification;
- `Reviewed` is not necessarily independent review;
- `Accepted` is not necessarily proof of outcome.

---

## 15. Claim Categories

A transparency record SHOULD identify the type of claim.

Claim categories MAY include:

- transaction;
- balance;
- allocation;
- custody;
- authority;
- rules;
- governance approval;
- use of funds;
- delivery;
- output;
- outcome;
- impact;
- compliance;
- security;
- implementation status;
- registry status;
- or verification status.

Each category requires evidence appropriate to the specific claim.

---

## 16. Claim Status

Claim status MUST describe the current strength and historical position of a claim.

Potential statuses MAY include:

- Declared;
- Evidence Submitted;
- Partially Supported;
- Supported;
- Independently Supported;
- Verified On-Chain;
- Disputed;
- Not Supported;
- Superseded;
- or Unable to Determine.

The final production vocabulary remains unresolved.

The term `verified` MUST NOT be used without identifying:

- what was verified;
- by whom or what;
- through which evidence;
- and within what scope.

---

## 17. Verification Vocabulary

Public interfaces SHOULD use precise labels such as:

- transaction verified on-chain;
- allocation balance verified on-chain;
- contract source verified;
- authority assignment authenticated;
- evidence integrity anchored;
- supporting documentation reviewed;
- use of funds supported;
- outcome documented;
- impact evaluation pending;
- independently reviewed;
- disputed;
- superseded;
- or unable to determine.

Vague labels such as:

- fully transparent;
- fully verified;
- completely audited;
- permanent approval;
- guaranteed impact;
- trustless;
- or independently proven

SHOULD NOT be used without precise scope and evidence.

---

## 18. Transaction Verification

A transaction record SHOULD identify, where applicable:

- network;
- chain ID;
- transaction hash;
- block;
- timestamp;
- sender;
- recipient;
- asset;
- amount;
- relevant contract;
- event;
- status;
- and confirmation state.

A transaction MUST NOT be attributed to GFC solely because an unauthenticated label says so.

Transaction verification does not independently prove:

- legitimate authority;
- purpose;
- use;
- delivery;
- outcome;
- or impact.

---

## 19. Authority Transparency

Material production authority MUST be reviewable.

Where applicable, transparency records SHOULD identify:

- role;
- environment;
- network;
- controlling address, contract, multisig, entity, or other holder;
- permitted actions;
- approval requirements;
- timelock;
- pause authority;
- upgrade authority;
- migration authority;
- effective status;
- and historical changes.

Authority transparency MUST remain consistent with [`roles-and-authority.md`](roles-and-authority.md).

Pilot authority MUST NOT be presented as production authority.

---

## 20. Rules Transparency

A material action SHOULD be linkable to the rules that governed it at the time.

Relevant rules MAY include:

- specification version;
- contract parameters;
- allocation constraints;
- governance constraints;
- timelock requirements;
- presale rules;
- vesting rules;
- evidence-review rules;
- or another applicable policy.

A later rule change MUST NOT silently rewrite the historical rule that applied to an earlier action.

---

## 21. Governance and Decision Transparency

Material governance records SHOULD identify:

- proposal;
- proposer;
- affected component;
- authority;
- applicable rules;
- rationale;
- conflicts;
- approval requirements;
- approval result;
- execution;
- implementation status;
- and final outcome.

The system MUST distinguish between:

- Proposed;
- Approved;
- Scheduled;
- Executed;
- Rejected;
- Cancelled;
- Failed;
- Superseded;
- and Migrated

where those concepts apply.

A governance decision MUST NOT be presented as executed until execution can be verified.

---

## 22. Use-of-Funds Verification

A use-of-funds record SHOULD identify:

- source allocation;
- source transaction;
- authority;
- approval;
- stated purpose;
- recipient category;
- transferred amount;
- actual amount used;
- supporting evidence;
- reconciliation;
- exceptions;
- and review status.

A transaction description, wallet label, internal note, or narrative statement MUST NOT by itself be treated as sufficient proof of use.

Where only part of a payment can be reconciled, the record SHOULD distinguish:

- supported amount;
- unsupported amount;
- disputed amount;
- returned amount;
- and unresolved difference.

---

## 23. Output, Outcome, and Impact

GFC MUST distinguish among:

### 23.1 Output

A direct deliverable or activity.

### 23.2 Outcome

An observable result following the output.

### 23.3 Impact

A broader or longer-term result for which attribution requires appropriate methodology.

A verified payment does not automatically verify an output.

A verified output does not automatically verify an outcome.

A verified outcome does not automatically prove broader impact.

---

## 24. Impact Evaluation

A material impact claim MUST identify an applicable methodology.

The methodology SHOULD define:

- objective;
- baseline;
- indicators;
- target;
- data source;
- collection method;
- period;
- attribution assumptions;
- limitations;
- uncertainty;
- and reviewer.

The system MUST permit:

- negative results;
- mixed results;
- missed targets;
- inconclusive findings;
- and disputed impact claims.

Impact MUST NOT be represented as independently verified unless the relevant independence, scope, methodology, and limitations are documented.

---

## 25. Authentication of Official Technical Records

Before a production technical record is represented as official, its authentication SHOULD be traceable through the applicable release and deployment process.

Examples include:

- token contract;
- allocation contract;
- presale contract;
- vesting contract;
- treasury wallet;
- liquidity wallet;
- governance executor;
- or other material production address.

An address label alone does not establish authenticity.

---

## 26. Contract Records

A production contract record SHOULD identify, where applicable:

- contract name;
- purpose;
- environment;
- network;
- chain ID;
- address;
- implementation address;
- proxy type;
- source repository;
- source commit;
- compiler;
- source-verification status;
- deployment transaction;
- deployer;
- administrator;
- authority;
- applicable specification version;
- security-review status;
- audit status;
- known deviations;
- pause status;
- upgradeability;
- and deprecation status.

A contract MUST NOT be described as immutable where the complete architecture permits material change.

---

## 27. Wallet Records

A material production wallet record SHOULD identify:

- address;
- purpose;
- allocation;
- environment;
- custody model;
- approval model;
- signer-category disclosure;
- permitted use;
- prohibited use;
- active status;
- and historical replacement where applicable.

A wallet label is not a technical restriction.

---

## 28. Token Transparency

The production transparency model SHOULD make reviewable:

- authenticated token contract;
- token identity;
- decimals;
- fixed supply;
- supply creation;
- mint-authority status;
- buy fee;
- sell fee;
- fee authority;
- transfer restrictions where applicable;
- upgradeability;
- and known deviations.

No production GFC token is currently deployed on Base Mainnet.

The public Base Sepolia pilot MUST remain separately labeled.

---

## 29. Allocation Transparency

The current Draft allocation model is:

| Allocation | Percentage | Token Amount |
|---|---:|---:|
| Impact Vault | 25% | 250,000,000 GFC |
| Guardian Growth | 20% | 200,000,000 GFC |
| Presale | 15% | 150,000,000 GFC |
| Treasury Reserve | 15% | 150,000,000 GFC |
| Liquidity Reserve | 15% | 150,000,000 GFC |
| Ecosystem | 5% | 50,000,000 GFC |
| Core Team | 5% | 50,000,000 GFC |
| **Total** | **100%** | **1,000,000,000 GFC** |

Transparency SHOULD distinguish:

- intended allocation;
- authenticated production allocation;
- current balance;
- locked amount;
- vested amount;
- distributed amount;
- transferred amount;
- spent amount where applicable;
- and migrated amount.

An allocation label does not prove compliant use.

---

## 30. Impact Vault Transparency

The Impact Vault is intended to contain:

```text
250,000,000 GFC
```

and use a:

```text
50-year lock
```

Production transparency SHOULD make reviewable:

- authenticated custody;
- lock implementation;
- lock start;
- represented lock end;
- current locked amount;
- released amount;
- upgradeability;
- migration authority;
- recovery authority;
- and historical changes.

No production lock-start timestamp is established by this Draft.

The Impact Vault MUST NOT be represented as technically locked until authenticated production implementation supports that claim.

---

## 31. Core Team Vesting Transparency

The Core Team allocation is:

```text
50,000,000 GFC
```

with intended:

```text
19-year linear vesting
```

Production transparency SHOULD distinguish:

- total allocation;
- unvested amount;
- vested amount;
- vested but unclaimed amount;
- claimed amount;
- transferred amount;
- beneficiary structure;
- vesting start;
- vesting end;
- reassignment;
- migration;
- and recovery authority.

No production vesting-start timestamp is established by this Draft.

Vested tokens MUST NOT be described as unvested or fully locked merely because they remain unclaimed.

---

## 32. Presale Transparency

No GFC presale is currently live.

The current Draft presale design includes:

- €0.05 reference price per GFC;
- intended eight-week duration;
- €250,000 soft cap;
- no separate monetary hard cap;
- 150,000,000 GFC Presale allocation;
- intended support for ETH, USDC, and DAI on Base;
- immediate GFC distribution as the current design direction;
- refund rights if the applicable success condition is not satisfied;
- and immutable material sale logic as the current design direction.

A production presale transparency surface SHOULD disclose:

- presale state;
- authenticated contract;
- specification version;
- reference price;
- supported payment assets;
- pricing method;
- start and end;
- soft cap;
- Presale allocation;
- cumulative GFC distributed;
- remaining GFC;
- contribution-asset balances;
- soft-cap reference value;
- pause state;
- cancellation state;
- finalization state;
- refund status;
- proceeds withdrawals;
- unsold-GFC treatment;
- authority changes;
- incidents;
- and corrections.

The interface MUST distinguish:

- purchase;
- GFC distribution;
- contribution custody;
- soft-cap status;
- finalization;
- refund;
- and proceeds withdrawal.

The current model MUST NOT be presented as deferred claim.

The unresolved relationship between immediate GFC distribution and failed-sale refunds MUST remain visible until resolved.

---

## 33. Treasury Transparency

For a material Treasury Reserve action, the transparency model SHOULD disclose, where appropriate:

- source;
- allocation;
- authority;
- approval;
- destination;
- asset;
- amount;
- purpose category;
- transaction;
- supporting evidence;
- reconciliation;
- and final status.

On-chain transfer visibility does not replace use-of-funds evidence.

---

## 34. Liquidity Transparency

Liquidity transparency SHOULD distinguish:

- Liquidity Reserve balance;
- liquidity actually deployed;
- venue;
- pair;
- GFC amount;
- paired asset;
- liquidity-provider position;
- position custodian;
- lock status;
- withdrawal authority;
- rebalancing authority;
- trading-fee flow;
- and material changes.

Liquidity Reserve MUST NOT be represented as active liquidity merely because the allocation exists.

Liquidity MUST NOT be described as permanently locked unless technically verifiable.

---

## 35. Fee Transparency

The current intended GFC token fee model is:

- **Buy fee:** 0%
- **Sell fee:** 1%

Production transparency SHOULD disclose:

- active fee rule;
- classification logic;
- recognized pools;
- exemptions;
- fee destination;
- fee amount collected;
- fee-proceeds use;
- authority;
- and historical parameter changes.

The final sell-fee destination and use remain unresolved.

Transparency MUST NOT imply a specific fee destination before it is finalized and deployed.

Fee proceeds MUST NOT be labeled impact funding solely because of a wallet name or narrative statement.

---

## 36. Staking Transparency

No production GFC staking system is currently operational.

The current intended design direction is **hybrid and non-inflationary**.

If staking is later deployed, production transparency SHOULD disclose:

- authenticated staking contract;
- principal-custody model;
- reward source;
- reward pool;
- reward-rate rules;
- calculation method;
- duration;
- total principal;
- distributed rewards;
- remaining authorized reward capacity;
- lock conditions;
- withdrawal conditions;
- governance-related rights;
- authority;
- pause status;
- upgradeability;
- and migration history.

No reward source is assigned by this Draft.

A displayed APR or APY MUST NOT be represented as guaranteed.

---

## 37. Economic-Flow Transparency

Material economic flows SHOULD remain consistent with [`economic-flows.md`](economic-flows.md).

Transparency SHOULD distinguish:

- allocation;
- custody;
- transfer;
- release;
- vesting;
- claim;
- spending;
- fee collection;
- fee use;
- contribution;
- refundable contribution;
- finalized proceeds;
- liquidity deployment;
- staking reward;
- migration;
- and recovery.

Internal transfers MUST NOT be represented as new external funding.

---

## 38. Evidence Packages

A material claim MAY be represented through an evidence package.

An evidence package SHOULD identify:

- package identifier;
- related claim;
- related allocation or system component;
- related transaction;
- authority;
- applicable rules;
- intended purpose;
- evidence inventory;
- evidence disclosure levels;
- provenance;
- integrity references;
- reviewer;
- review status;
- limitations;
- disputes;
- publication date;
- and version.

The package MUST distinguish public evidence from protected evidence.

---

## 39. Durable Record Identifiers

Material transparency records SHOULD use stable identifiers.

Potential record types MAY include:

- deployment record;
- contract record;
- wallet record;
- authority record;
- transaction record;
- governance record;
- allocation record;
- evidence record;
- use-of-funds record;
- outcome record;
- impact record;
- registry record;
- dispute record;
- incident record;
- correction record;
- and supersession record.

Identifiers SHOULD survive portal redesigns and migrations where technically practical.

---

## 40. Record Linkage

The transparency infrastructure SHOULD permit lifecycle linkage among:

1. funds;
2. authority;
3. rules;
4. decisions;
5. execution;
6. transaction;
7. supporting evidence;
8. reconciliation;
9. output;
10. outcome;
11. impact evaluation;
12. dispute;
13. correction;
14. supersession;
15. and final current status.

Absence of a later-stage record MUST NOT rewrite the existence of an earlier-stage record.

---

# Transparency Registry

## 41. Transparency Registry Purpose

The planned GFC Transparency Registry is intended to provide a **versioned historical record**.

It MUST NOT be designed or represented as a permanent approval badge.

The Registry MAY eventually contain records concerning:

- GFC itself;
- GFC-related infrastructure;
- external projects;
- NGOs;
- organizations;
- companies;
- programs;
- or other eligible entities or initiatives

where the applicable governance and admission model permits inclusion.

No complete production Transparency Registry is currently deployed.

---

## 42. Registry Is Not a Permanent Badge

Registry inclusion MUST NOT imply:

- permanent approval;
- permanent verification;
- permanent endorsement;
- perpetual compliance;
- perpetual evidence validity;
- or permanent satisfaction of governance requirements.

Evidence can expire.

Policies can change.

Governance can change.

Claims can change.

Conflicts can emerge.

New information can supersede prior information.

Therefore, a registry record SHOULD make material status changes historically reconstructable.

---

## 43. Versioned Accountability

A material Registry record SHOULD preserve, where appropriate:

- what was disclosed;
- what evidence supported the disclosure;
- what policy or rule applied;
- what governance or authority applied;
- what claim was made;
- what status existed;
- when the status changed;
- who or what had authority to change it;
- and why the change occurred.

A newer record MUST NOT silently erase a materially different prior record merely because the earlier state is unfavorable or outdated.

---

## 44. Registry Authority

The final production authority model remains unresolved.

However, where GFC operates the Registry, the applicable governance model MAY assign GFC-defined authority relating to:

- admission;
- publication;
- verification status;
- correction;
- downgrade;
- suspension;
- supersession;
- removal from current active presentation;
- and historical retention.

Such authority MUST be:

- explicit;
- bounded;
- reviewable;
- historically recorded;
- and consistent with [`roles-and-authority.md`](roles-and-authority.md).

No such production authority is represented as active today.

---

## 45. Registry Admission

A future Registry admission process MUST define:

- eligible entity or record types;
- admission criteria;
- evidence requirements;
- authority;
- conflicts;
- rejection handling;
- publication rules;
- and historical status.

Admission MUST NOT automatically mean verification.

Admission MUST NOT automatically mean endorsement.

---

## 46. Registry Verification Status

If a future Registry uses verification statuses, the exact meaning of each status MUST be defined.

A verification status MUST identify:

- claim or scope being evaluated;
- evidence basis;
- reviewer or authority;
- review date;
- limitations;
- and current historical version.

A single global `verified` badge without scope is NOT RECOMMENDED.

Verification of one claim MUST NOT be presented as verification of unrelated claims.

---

## 47. Registry Downgrade

A future Registry MAY support status downgrade where:

- evidence weakens;
- evidence expires;
- conflicting information appears;
- applicable requirements are no longer satisfied;
- governance changes;
- material claims become disputed;
- or another predefined condition applies.

Downgrade authority and criteria MUST be defined.

A downgrade SHOULD preserve the prior status in historical context.

---

## 48. Registry Suspension

A future Registry MAY support suspension where current reliance should be restricted pending:

- investigation;
- missing evidence;
- serious dispute;
- security incident;
- governance concern;
- or another predefined condition.

Suspension MUST NOT silently erase historical records.

The record SHOULD identify:

- suspension time;
- authority;
- reason category;
- affected claim or scope;
- and review status.

---

## 49. Registry Removal

A future Registry MAY permit removal from current active presentation under defined conditions.

Removal MUST NOT be used merely to erase unfavorable history.

Where lawful and appropriate, the historical record SHOULD preserve that:

- a record existed;
- it was later removed from current presentation;
- when;
- under what authority;
- and for what reason category.

Protected content MAY still require redaction or deletion under applicable legal or privacy obligations.

---

## 50. Registry Corrections

A material Registry correction SHOULD identify:

- original record;
- corrected record;
- correction date;
- authority;
- reason;
- affected claims;
- and whether the prior status remains historically visible.

Corrections MUST NOT create the impression that the original material error never occurred.

---

## 51. Registry Disputes

A future Registry SHOULD support representation of material disputes.

A disputed status SHOULD identify:

- challenged record or claim;
- dispute status;
- submission time;
- review authority;
- current response state;
- and resulting status change where applicable.

The original publisher MUST NOT be treated as the only valid dispute reviewer for all material disputes.

---

## 52. Registry Independence Claims

A GFC-operated Registry MUST NOT be described as independently controlled or independently verified merely because it applies structured rules.

If GFC retains material authority over:

- admission;
- status;
- verification;
- downgrade;
- suspension;
- or removal,

that authority MUST be disclosed.

External review MAY support specific claims without making the entire Registry independent.

---

## 53. Registry Historical Integrity

Registry history SHOULD preserve material transitions among statuses.

Where technically and legally appropriate, the system SHOULD retain:

- prior published versions;
- prior evidence references;
- prior authority;
- prior claim status;
- correction history;
- downgrade history;
- suspension history;
- and supersession history.

Historical integrity does not require permanent publication of protected information.

---

# Evidence Integrity and Privacy

## 54. Cryptographic Anchoring Requirements

Where cryptographic anchoring is used, the implementation MUST define:

- record scope;
- canonicalization;
- hash algorithm;
- version;
- publication method;
- verification method;
- and migration strategy.

Updated records SHOULD receive new commitments.

Prior commitments SHOULD remain reviewable where appropriate.

Low-entropy protected content MUST NOT be naively hashed where brute-force confirmation presents a realistic privacy risk.

---

## 55. Protected Evidence

Protected evidence MUST use access controls appropriate to its sensitivity.

Access SHOULD be:

- role-based;
- purpose-limited;
- authenticated;
- revocable;
- and logged where appropriate.

The public system MAY expose metadata such as:

- evidence category;
- existence;
- integrity status;
- review status;
- reviewer category;
- restriction reason;
- and limitation.

Protected evidence MUST NOT be represented as independently verified unless qualifying review actually occurred.

---

## 56. Privacy and Data Protection

GFC SHOULD collect and disclose only information necessary for legitimate:

- verification;
- accountability;
- compliance;
- security;
- operations;
- or impact evaluation.

Personal data SHOULD NOT be placed directly on a public blockchain.

Beneficiary information MUST NOT be published merely to strengthen an impact narrative.

Wallet addresses MUST NOT be publicly linked to identified natural persons without appropriate lawful basis and disclosure.

The final system MUST define retention, deletion, redaction, archival, and immutable-reference handling.

---

# Portal and Data Infrastructure

## 57. Transparency Portal

The public transparency portal is intended to aggregate and explain reviewable records.

It SHOULD remain separate from custody and governance execution.

It MUST NOT possess undisclosed authority to:

- transfer funds;
- alter user balances;
- modify contract state;
- approve treasury transactions;
- override governance;
- rewrite authenticated evidence history;
- or create false verification status.

No complete production portal or Registry is represented as operational by this document.

---

## 58. Data-Source Labeling

Material portal records SHOULD identify whether they derive from:

- direct on-chain data;
- indexed on-chain data;
- GFC-authored information;
- external information;
- cryptographically anchored evidence;
- protected evidence;
- internal review;
- independent review;
- or derived calculations.

Derived information MUST be distinguishable from primary source data.

---

## 59. Portal Status Accuracy

The portal MUST use implementation-status terminology consistently with the repository glossary.

Where applicable, it SHOULD distinguish:

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
- Not Deployed;
- Paused;
- Migrated;
- and Retired.

These states MUST NOT be treated as interchangeable.

---

## 60. Indexed and Derived Data

Indexed or derived information may differ from primary on-chain state due to:

- indexing delay;
- provider outage;
- chain reorganization;
- parsing error;
- metadata error;
- or software defect.

Where material, the portal SHOULD identify:

- data source;
- last update;
- indexed block;
- calculation method;
- and known delay.

Authenticated primary source state prevails over conflicting derived display data.

---

# Historical Integrity

## 61. Version History

Material records SHOULD retain:

- original publication date;
- latest update;
- prior version linkage;
- responsible publisher or authority;
- reason for change;
- applicable rule version;
- and integrity references where applicable.

---

## 62. No Silent Deletion

Material records MUST NOT be silently removed solely because they are:

- unfavorable;
- incorrect;
- disputed;
- outdated;
- downgraded;
- or embarrassing.

This requirement remains subject to legitimate privacy, legal, security, and data-protection obligations.

---

## 63. Redaction

Where information must be redacted, the historical record SHOULD indicate, where lawful:

- that redaction occurred;
- date;
- authority;
- and reason category.

The protected removed content itself MUST NOT remain publicly exposed merely to satisfy historical transparency.

---

## 64. Supersession

A corrected or newer record SHOULD link to the record it supersedes.

A superseded record SHOULD identify its successor where practical.

Supersession is not equivalent to deletion.

---

# Review, Disputes, and Audits

## 65. Independent Review

A review MUST NOT be labeled independent solely because the reviewer is external.

Relevant factors include:

- financial relationship;
- control;
- prior involvement;
- scope restriction;
- data access;
- methodology control;
- and ability to publish unfavorable findings.

Independent review applies only within its actual scope.

---

## 66. Audits

The term `audit` MUST be used precisely.

An audit record SHOULD identify:

- auditor;
- audit type;
- scope;
- methodology or standard;
- reviewed components;
- exclusions;
- report date;
- findings;
- remediation status;
- and applicable implementation version.

A code review, automated scan, internal review, or source verification MUST NOT automatically be described as an audit.

---

## 67. Disputes and Challenges

The transparency infrastructure SHOULD support challenges concerning:

- transaction attribution;
- address ownership;
- authority;
- approval;
- rule application;
- use of funds;
- evidence authenticity;
- evidence completeness;
- evidence status;
- Registry status;
- outcome claims;
- impact claims;
- reviewer independence;
- conflicts;
- and conformance.

The final dispute process remains unresolved.

A material unresolved challenge SHOULD be visible as disputed status.

---

## 68. Limitations and Uncertainty

Material transparency surfaces SHOULD disclose relevant limitations.

Potential limitations include:

- incomplete evidence;
- protected evidence;
- unavailable evidence;
- self-reporting;
- reviewer conflict;
- data delay;
- indexing error;
- pricing dependency;
- methodological limitations;
- attribution uncertainty;
- legal restrictions;
- security restrictions;
- and unresolved disputes.

Limitations MUST NOT be concealed merely because they weaken a claim.

---

## 69. Negative Information

The transparency model MUST permit publication of:

- failed initiatives;
- overspending;
- underspending;
- delayed delivery;
- unresolved reconciliation;
- unsupported claims;
- rejected evidence;
- downgrades;
- suspensions;
- disputes;
- incidents;
- security findings;
- governance failures;
- and negative or mixed outcomes.

Transparency limited to favorable information is not sufficient.

---

# Security and Incidents

## 70. Security Requirements

The transparency infrastructure MUST protect against:

- unauthorized record modification;
- evidence deletion;
- false status assignment;
- unauthorized protected-data access;
- integrity-anchor mismatch;
- portal compromise;
- domain compromise;
- fake contract addresses;
- indexer manipulation;
- database corruption;
- privilege escalation;
- reviewer impersonation;
- and audit-log deletion.

Detailed requirements are defined in [`security-model.md`](security-model.md).

---

## 71. Transparency Incidents

Transparency incidents MAY include:

- publication of false information;
- incorrect wallet attribution;
- altered evidence;
- unauthorized status change;
- missing evidence;
- protected-data exposure;
- false independent-review claim;
- concealed conflict;
- false impact claim;
- portal compromise;
- indexer failure;
- incorrect contract data;
- privacy breach;
- historical-record deletion;
- or Registry-history manipulation.

Material incidents SHOULD remain historically reviewable after remediation where appropriate.

---

# Pilot and Production Separation

## 72. Public Base Sepolia Pilot

A public pilot exists on Base Sepolia:

- **Network:** Base Sepolia
- **Chain ID:** `84532`
- **Pilot token:** `tGFC`
- **Pilot contract:** `0x7262Cca91938ede6bB6560F81104Aa410848e7f3`
- **Source status:** verified

This is a public testnet pilot.

It MUST NOT be presented as:

- production GFC;
- Base Mainnet deployment;
- live presale;
- production allocation infrastructure;
- production staking;
- production treasury;
- production governance;
- complete production Transparency Registry;
- or proof that future production architecture will use identical code, parameters, addresses, or authority.

---

## 73. Production Transparency Authentication

Before production transparency records are represented as official, they SHOULD identify:

- production environment;
- network;
- authenticated production contracts or wallets;
- applicable specifications;
- authority records;
- release records;
- and verification status.

Pilot records MUST remain distinguishable from production records.

---

# Public Communication

## 74. Public Communication Requirements

Public communication MUST distinguish between:

- intended design;
- Draft specification;
- implemented feature;
- tested feature;
- pilot feature;
- reviewed feature;
- audited feature;
- deployed feature;
- live feature;
- operational feature;
- and independently verified claim.

Public communication MUST NOT:

- present the Base Sepolia pilot as production;
- describe a future Registry as operational today;
- describe Registry inclusion as permanent approval;
- use `verified` without scope;
- describe immediate Presale distribution as deferred claiming;
- describe staking as operational when it is not;
- describe an allocation as technically locked before enforcement exists;
- or imply impact from transaction visibility alone.

---

## 75. Transparency and Legal Responsibility

Public transparency does not replace:

- legal obligations;
- contractual obligations;
- accounting obligations;
- privacy obligations;
- tax obligations;
- regulatory obligations;
- or professional responsibility.

An on-chain record is not automatically legally sufficient merely because it is public.

---

# Invariants and Conformance

## 76. Required Transparency Invariants

A conforming implementation MUST preserve at least the following invariants:

1. `Funds → Authority → Rules → Decisions → Outcomes → Evidence` remains the canonical accountability model.
2. On-chain execution and off-chain claims remain distinguishable.
3. Transaction verification is not represented as use-of-funds verification.
4. Use-of-funds verification is not represented as outcome or impact verification.
5. Cryptographic anchoring is not represented as factual truth.
6. Project-authored evidence is not represented as independent evidence.
7. Protected evidence is not represented as public evidence.
8. Material authority remains identifiable.
9. Material historical state remains reconstructable where appropriate.
10. Corrections do not silently erase materially different prior records.
11. Evidence status and claim status remain distinct.
12. Claim strength does not exceed evidence strength.
13. Disputed claims or records are represented appropriately.
14. Material limitations remain visible.
15. Personal data is not placed on-chain without adequate justification.
16. Portal data can be reconciled to authenticated primary sources.
17. Wallet labels are not treated as technical restrictions.
18. Allocation labels are not treated as proof of compliant use.
19. Impact claims identify methodology and uncertainty.
20. Reviewer independence is not inferred solely from external status.
21. Planned functionality is not presented as active functionality.
22. Registry inclusion is not represented as permanent approval.
23. Registry status changes remain historically reviewable where appropriate.
24. Pilot status is not represented as production status.
25. Presale transparency reflects immediate distribution rather than the deprecated deferred-claim model.
26. Staking transparency reflects the current hybrid, non-inflationary Draft direction without inventing a reward source.

---

## 77. Conformance

A transparency implementation conforms to this specification only when:

- it identifies an applicable versioned transparency specification;
- the canonical accountability model is preserved;
- transaction, authority, rules, use, outcome, and impact claims remain appropriately distinguished;
- Public On-Chain, Cryptographically Anchored, and Protected Off-Chain evidence remain distinguishable;
- evidence provenance is available where material;
- evidence status and claim status remain separate;
- material authority is disclosed;
- production contracts and wallets are authenticated;
- protected evidence is access-controlled;
- historical records remain reviewable;
- corrections are documented;
- disputes can be represented;
- Registry status does not imply permanent endorsement;
- limitations remain visible;
- production and pilot status are correctly separated;
- public communication reflects actual implementation status;
- applicable transparency-conformance claims are traceable to the verification mappings defined in [`conformance-verification.md`](conformance-verification.md);
- implementation-specific verification bindings are authenticated for the evaluated deployment where required;
- evidence is not interpreted beyond its defined evidence ceiling;
- and material deviations are disclosed.

The applicable verification methods, observable evidence, implementation bindings, and evidence ceilings for transparency-conformance requirements are defined in [`conformance-verification.md`](conformance-verification.md).

A public on-chain observation MAY support a transaction-, state-, balance-, or authority-level claim within its defined scope. It MUST NOT be elevated into use-of-funds, outcome, impact, factual-truth, or complete-system-conformance claims without the additional evidence required by the applicable verification mapping.

Where a required production implementation binding has not yet been established, the underlying transparency requirement remains specified but MUST NOT be represented as technically verified.

---

## 78. Transparency Non-Conformance

Transparency non-conformance includes:

- presenting visibility as verification;
- presenting a transaction as proof of impact;
- false wallet attribution;
- undisclosed authority;
- unsupported use-of-funds claims;
- unsupported outcome claims;
- unsupported impact claims;
- project-authored evidence presented as independent;
- cryptographic anchoring presented as factual proof;
- silent material record modification;
- silent material deletion;
- concealed dispute;
- concealed limitation;
- unauthorized protected-data access;
- false audit claim;
- false independent-review claim;
- Registry inclusion represented as permanent approval;
- status downgrade or suspension silently erased;
- pilot infrastructure presented as production;
- deferred-claim presale language presented as the current model;
- or planned infrastructure presented as operational.

Material non-conformance MAY require:

- correction;
- status downgrade;
- suspension;
- supersession;
- public disclosure;
- access revocation;
- independent review;
- portal suspension;
- incident treatment;
- migration;
- or deprecation.

A specification MUST NOT be rewritten retrospectively merely to conceal transparency non-conformance.

---

## 79. Transparency Non-Goals

The GFC transparency model does not aim to:

- place all information on-chain;
- publish all personal or beneficiary information;
- claim that blockchain data contains complete real-world context;
- fully automate judgment;
- eliminate human responsibility;
- replace independent review;
- guarantee factual accuracy of submitted evidence;
- guarantee successful outcomes;
- guarantee impact;
- expose security-sensitive information;
- equate public data volume with accountability;
- treat wallet publication as sufficient transparency;
- treat Registry inclusion as permanent endorsement;
- or claim that trust can be eliminated entirely.

The objective is to make material trust dependencies visible, bounded, historically reviewable, and accountable.

---

## 80. Current Unresolved Transparency Decisions

The following matters remain unresolved unless separately established by a later versioned specification or authenticated implementation record.

### 80.1 Evidence schema

- record fields;
- required metadata;
- evidence identifiers;
- claim identifiers;
- evidence-package structure;
- and relationship model.

### 80.2 Evidence status

- final status vocabulary;
- transition authority;
- review requirements;
- dispute effects;
- and supersession rules.

### 80.3 Claim status

- final claim-status vocabulary;
- evidence thresholds;
- independent-support standard;
- downgrade rules;
- and supersession rules.

### 80.4 Transparency Registry

- final entity eligibility;
- admission criteria;
- submission process;
- verification-status vocabulary;
- review workflow;
- downgrade criteria;
- suspension criteria;
- removal criteria;
- appeal or reconsideration;
- current-versus-historical presentation;
- and production authority model.

### 80.5 Cryptographic anchoring

- hash algorithms;
- anchoring mechanism;
- Base transaction or contract model;
- Merkle design;
- salting;
- versioning;
- and algorithm migration.

### 80.6 Protected evidence

- storage architecture;
- encryption;
- access roles;
- logging;
- retention;
- backup;
- recovery;
- deletion;
- and legal-hold procedure.

### 80.7 Portal

- implementation architecture;
- data sources;
- indexers;
- update frequency;
- availability requirements;
- authentication;
- and fallback access.

### 80.8 Review

- reviewer categories;
- independence criteria;
- appointment;
- evidence access;
- publication rules;
- and conflicts.

### 80.9 Impact

- methodology framework;
- indicator selection;
- baseline requirements;
- attribution model;
- uncertainty model;
- evaluator appointment;
- and terminology.

### 80.10 Disputes

- eligible challengers;
- submission;
- review authority;
- response periods;
- appeals;
- and public status treatment.

### 80.11 Privacy

- legal roles;
- lawful bases;
- consent handling;
- retention;
- deletion;
- redaction;
- international transfer;
- and breach response.

### 80.12 Historical records

- append-only model;
- correction format;
- archive;
- integrity verification;
- long-term preservation;
- and legally required deletion interaction.

These unresolved matters MUST NOT be represented as finalized production decisions.

---

## 81. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- the canonical accountability model is consistently applied;
- the evidence schema is finalized;
- the claim model is finalized;
- evidence-status vocabulary is finalized;
- claim-status vocabulary is finalized;
- production contract and wallet authentication records are specified;
- the authority registry relationship is finalized;
- Transparency Registry admission rules are finalized;
- Registry verification-status rules are finalized;
- downgrade rules are finalized;
- suspension rules are finalized;
- removal and historical-retention rules are finalized;
- Registry authority is finalized;
- evidence anchoring is finalized;
- hash and privacy protections are finalized;
- protected-evidence storage is finalized;
- access-control roles are defined;
- retention and deletion rules are defined;
- portal architecture is defined;
- data-source and indexing rules are defined;
- historical-record requirements are finalized;
- correction procedures are finalized;
- dispute procedures are finalized;
- independent-review criteria are finalized;
- impact-methodology requirements are finalized;
- limitation and uncertainty requirements are finalized;
- presale transparency matches the final production presale model;
- staking transparency matches the final production staking model;
- privacy responsibilities are identified;
- security controls are mapped to the implementation;
- transparency conformance requirements are mapped to appropriate verification methods and evidence ceilings;
- required production implementation-specific verification bindings can be authenticated;
- incident procedures are defined;
- Base Sepolia pilot and Base Mainnet production terminology are consistently separated;
- implementation feasibility is confirmed;
- public terminology is consistent;
- and all related specifications are mutually consistent.

---

## 82. Final Transparency Principles

The GFC transparency model preserves the following distinctions:

> Visibility is not the same as verifiability.

> Public does not automatically mean verified.

> A wallet address shows movements, not motives, rules, or authority.

> A transaction does not prove compliant use.

> Compliant use does not automatically prove outcome.

> Outcome does not automatically prove impact.

> Cryptographic anchoring proves integrity, not factual truth.

> A public explanation does not replace evidence.

> Project-authored evidence is not automatically independent evidence.

> Protected evidence can remain reviewable without being publicly exposed.

> A Transparency Registry should preserve history rather than reduce accountability to a badge.

> Registry inclusion does not mean permanent approval.

> Verification status can change when evidence, governance, policy, or claims change.

> Pilot does not mean production.

> Different claims require different evidence.

Transparency is credible only where **Funds, Authority, Rules, Decisions, Outcomes, Evidence, limitations, corrections, disputes, and historical changes** can be examined together.

# Global Foundation Coin Transparency Model Specification

**Document ID:** GFC-TRN-001  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-deployment  
**Intended Network:** Base Mainnet  
**Chain ID:** 8453  
**Last Updated:** 2026-07-23

---

## 1. Document Status

This document defines the intended transparency, evidence, verification, disclosure, and accountability model of Global Foundation Coin (GFC).

It is normative because it defines intended requirements, classifications, boundaries, and prohibited representations.

Its maturity remains Draft. The requirements may change before the first versioned release.

At the time of publication:

- no production GFC transparency protocol is represented as deployed;
- no production GFC transparency portal is represented as fully operational;
- no production token, presale, treasury, staking, vesting, or governance contract is represented by this document as deployed;
- no wallet, contract, allocation, evidence record, or impact claim should be treated as official unless published through an authenticated GFC release process;
- no active presale is established by this document;
- no public presale date is established by this document;
- evidence schemas, review procedures, anchoring mechanisms, and impact-evaluation methodologies remain under development;
- no implementation is governed by this document unless it explicitly identifies an applicable versioned release.

The presence of a mechanism or classification in this specification does not mean that it has already been:

- implemented;
- tested;
- reviewed;
- audited;
- deployed;
- activated;
- independently verified;
- or made publicly available.

The continuously changing `main` branch MUST NOT automatically be treated as the authoritative transparency specification for any future production deployment.

---

## 2. Purpose

This document defines how GFC intends to treat transparency as a practical system property rather than a marketing claim.

Its purpose is to establish:

- what can be verified directly on-chain;
- what requires supporting off-chain evidence;
- what requires governance records;
- what requires outcome or impact evaluation;
- how evidence is classified;
- how records are linked to claims;
- how protected information can remain reviewable without being publicly exposed;
- how corrections and disputes are handled;
- how transparency limitations are disclosed;
- and how public interfaces must avoid overstating the strength of available evidence.

The objective is not to make every piece of information public.

The objective is to make relevant claims:

- traceable;
- attributable;
- reviewable;
- evidence-based;
- historically accountable;
- and accurately classified.

---

## 3. Core Transparency Principle

GFC distinguishes between three separate verification questions:

### Transaction

**Did the funds move as stated?**

Primary evidence:

- on-chain transaction records;
- contract events;
- wallet balances;
- timestamps;
- transfer amounts;
- and verified contract state.

### Use

**Were the funds used for the documented purpose?**

Primary evidence may include:

- approvals;
- agreements;
- invoices;
- receipts;
- delivery records;
- reconciliations;
- recipient confirmations;
- and protected supporting documentation.

### Impact

**Did the documented use create a meaningful result?**

Primary evidence may include:

- output records;
- outcome indicators;
- follow-up data;
- methodology;
- independent evaluation;
- uncertainty disclosures;
- and impact assessments.

These questions MUST NOT be treated as interchangeable.

The following distinction is foundational:

> TRANSACTION VERIFIED does not equal IMPACT VERIFIED.

Different claims require different evidence.

---

## 4. Scope

This specification covers:

- transparency principles;
- transaction verification;
- use-of-funds verification;
- outcome and impact evaluation;
- governance transparency;
- authority disclosure;
- contract and wallet registries;
- fund-flow records;
- allocation reporting;
- presale transparency;
- treasury transparency;
- vesting and lock transparency;
- staking and fee transparency;
- evidence classification;
- evidence provenance;
- evidence status;
- cryptographic anchoring;
- protected off-chain documentation;
- evidence review;
- correction and version history;
- disputes and challenges;
- public portal requirements;
- privacy boundaries;
- security requirements;
- implementation conformance;
- and unresolved transparency decisions.

---

## 5. Out of Scope

This document does not independently define:

- final smart-contract code;
- final contract addresses;
- final wallet addresses;
- final evidence-storage provider;
- final database architecture;
- final cryptographic anchoring protocol;
- final document formats;
- final impact methodology;
- final independent reviewer;
- final audit provider;
- final legal privilege rules;
- final retention periods;
- final data-controller responsibilities;
- final beneficiary-consent process;
- final accounting standards;
- final reporting cadence;
- or jurisdiction-specific disclosure obligations.

These matters require separate technical, operational, legal, privacy, accounting, or impact documentation before production use.

---

## 6. Relationship to Other Specifications

This document must be read together with:

- `architecture.md`;
- `governance-constraints.md`;
- `presale.md`;
- `non-goals.md`;
- `glossary.md`;
- and the repository-level `SECURITY.md`.

Future specifications SHOULD additionally define:

- token and fee logic;
- allocation and treasury controls;
- evidence schemas;
- evidence storage;
- privacy;
- impact evaluation;
- governance records;
- incident response;
- and deployment authentication.

Where this specification conflicts with another applicable specification, the conflict MUST be resolved before either document is marked Stable.

---

## 7. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are normative only when:

- they appear in uppercase;
- the document declares `Authority: Normative`;
- and the document version applies to the implementation being evaluated.

Because this document is currently Draft, its requirements describe the intended transparency model but remain subject to review and versioned release.

---

## 8. Transparency Principles

### 8.1 Verification over explanation

A public explanation MUST NOT be treated as equivalent to independently reviewable evidence.

Narrative communication may provide context, but it does not replace:

- on-chain records;
- approvals;
- supporting documentation;
- reconciliation;
- or outcome evaluation.

### 8.2 Claims require evidence

Every material transparency claim SHOULD identify:

- what is being claimed;
- the applicable time period;
- the responsible party;
- the supporting evidence;
- the evidence classification;
- the review status;
- and known limitations.

### 8.3 Visibility is not verification

Information being publicly visible does not automatically mean that it has been verified.

A public wallet provides visibility into recorded transactions.

It does not independently establish:

- wallet purpose;
- controlling authority;
- recipient identity;
- approval legitimacy;
- use of funds;
- or impact.

### 8.4 Integrity is not truth

Cryptographic anchoring can support record integrity.

It does not automatically establish that the underlying record is:

- accurate;
- authentic;
- lawful;
- complete;
- unbiased;
- or factually correct.

### 8.5 Transparency does not eliminate trust

Transparency can reduce and bound trust dependencies.

It cannot eliminate reliance on:

- signers;
- evidence providers;
- reviewers;
- legal processes;
- operational execution;
- methodology;
- or real-world data.

### 8.6 Privacy-aware disclosure

Transparency MUST NOT require unnecessary publication of:

- personal data;
- beneficiary identities;
- banking information;
- confidential contracts;
- medical information;
- security-sensitive material;
- or legally protected documentation.

### 8.7 Historical accountability

Material records SHOULD remain historically reviewable.

Corrections MUST NOT silently erase materially different previous statements or evidence statuses.

### 8.8 Accurate certainty

The strength of a public claim MUST NOT exceed the strength of its supporting evidence.

### 8.9 Separation of roles

The following responsibilities SHOULD be separated where reasonably possible:

- funding approval;
- transaction execution;
- evidence submission;
- evidence custody;
- evidence review;
- accounting reconciliation;
- outcome evaluation;
- and impact evaluation.

### 8.10 No transparency theatre

Publishing large volumes of data MUST NOT be presented as meaningful transparency where the information:

- lacks context;
- lacks provenance;
- cannot be reconciled;
- cannot be reviewed;
- omits authority;
- or does not support the claim being made.

---

## 9. Three-Layer System Model

GFC transparency requires the combined operation of three system layers.

### 9.1 Technology

Technology provides:

- contract execution;
- transaction records;
- wallet balances;
- allocation state;
- vesting state;
- lock state;
- governance execution records;
- cryptographic commitments;
- timestamps;
- and public verification interfaces.

Technology determines what technically executed.

### 9.2 Governance

Governance provides:

- authority definitions;
- approval records;
- role assignments;
- signer structures;
- parameter-change records;
- decision rationales;
- conflict disclosures;
- emergency actions;
- and accountability.

Governance determines who was authorized to act and under which rules.

### 9.3 Impact and Evidence

Impact and evidence processes provide:

- intended-purpose records;
- supporting documentation;
- use-of-funds reconciliation;
- delivery evidence;
- outcome records;
- methodology;
- review;
- limitations;
- and impact evaluation.

This layer determines what can be supported beyond transaction execution.

No single layer is sufficient by itself.

---

## 10. Evidence Disclosure Levels

Evidence may be handled through three principal disclosure levels.

### 10.1 Public On-Chain

Public on-chain evidence may include:

- verified contract addresses;
- transaction hashes;
- token transfers;
- wallet balances;
- allocation balances;
- lock status;
- vesting status;
- claim records;
- refund records;
- governance execution;
- role changes;
- cryptographic commitments;
- and relevant contract events.

Public on-chain evidence is directly reviewable through Base and appropriate verification tools.

Its scope is limited to the information encoded on-chain.

### 10.2 Cryptographically Anchored

Cryptographically anchored evidence consists of off-chain records whose integrity is linked to a public:

- hash;
- digital signature;
- timestamp;
- Merkle root;
- content commitment;
- or equivalent cryptographic reference.

Anchoring MAY support verification that:

- a specific record existed;
- a specific version existed;
- the record has not changed since anchoring;
- or a group of records was committed at a defined time.

Anchoring does not independently prove:

- the identity of the original author;
- factual accuracy;
- completeness;
- lawful creation;
- genuine delivery;
- or meaningful impact.

### 10.3 Protected Off-Chain

Protected off-chain evidence may include:

- personal information;
- beneficiary records;
- identity documents;
- confidential agreements;
- invoices;
- banking records;
- commercially sensitive information;
- sensitive operational records;
- internal control records;
- security-sensitive material;
- and legally protected documentation.

Protected evidence MUST remain subject to:

- access control;
- integrity protection;
- retention rules;
- documented review procedures;
- and appropriate disclosure limitations.

Protected information MUST NOT be placed permanently on a public blockchain merely to create an appearance of transparency.

---

## 11. Evidence Provenance

Every material evidence item SHOULD identify its provenance.

Evidence provenance categories may include:

- generated directly by a verified smart contract;
- generated from public blockchain data;
- submitted by GFC;
- submitted by a funding recipient;
- submitted by a supplier;
- submitted by a partner;
- submitted by a beneficiary;
- submitted by an external reviewer;
- generated by an automated system;
- derived from another record;
- or imported from an external authority.

The provenance record SHOULD identify:

- source category;
- source identifier where lawful;
- submission time;
- applicable project or transaction;
- responsible custodian;
- integrity reference;
- and known limitations.

The source of evidence MUST NOT be concealed where source independence is relevant to the claim.

---

## 12. Evidence Status Model

Evidence status MUST be separate from claim status.

An evidence item MAY use statuses such as:

### 12.1 Submitted

The evidence was received but has not yet been reviewed.

### 12.2 Integrity Anchored

The evidence has been cryptographically committed.

This status concerns integrity, not factual verification.

### 12.3 Under Review

The evidence is being evaluated.

### 12.4 Reviewed

A defined reviewer has examined the evidence.

The reviewer and review scope MUST be identifiable.

### 12.5 Independently Reviewed

An external party with an adequately documented degree of independence has reviewed the evidence.

### 12.6 Accepted

The evidence satisfies the applicable internal evidence requirements.

### 12.7 Rejected

The evidence does not satisfy the applicable requirements.

### 12.8 Disputed

The evidence or its interpretation has been formally challenged.

### 12.9 Superseded

A later version replaces the evidence for current interpretation.

### 12.10 Withdrawn

The submitting party has withdrawn the evidence.

Withdrawal MUST NOT silently erase historical existence where the record was previously used to support a public claim.

### 12.11 Unavailable

Required evidence is missing, inaccessible, or cannot currently be verified.

The transparency interface MUST NOT treat these statuses as equivalent.

---

## 13. Claim Categories

A transparency record SHOULD classify the type of claim being made.

Claim categories may include:

- transaction claim;
- balance claim;
- allocation claim;
- custody claim;
- authority claim;
- approval claim;
- use-of-funds claim;
- delivery claim;
- output claim;
- outcome claim;
- impact claim;
- compliance claim;
- security claim;
- or implementation-status claim.

A single project activity may involve multiple claim categories.

Each claim category requires evidence appropriate to that claim.

---

## 14. Claim Status Model

Claim status MUST describe the strength and current state of the claim.

### 14.1 Declared

The claim has been stated but has not yet been supported by sufficient reviewed evidence.

### 14.2 Evidence Submitted

Supporting evidence exists but has not completed the applicable review.

### 14.3 Partially Supported

Some material elements are supported, while other required elements remain unavailable or unresolved.

### 14.4 Supported

The claim is supported by evidence satisfying the applicable internal requirements.

### 14.5 Independently Supported

The claim has been reviewed by a suitably independent external party under a documented scope.

### 14.6 Verified On-Chain

The claim concerns a fact directly determinable from authenticated on-chain data.

This status MUST be limited to facts actually encoded or directly derivable on-chain.

### 14.7 Disputed

The claim is subject to a material unresolved challenge.

### 14.8 Not Supported

Available evidence does not support the claim.

### 14.9 Superseded

The claim has been replaced by a newer or corrected claim.

### 14.10 Unable to Determine

Available evidence is insufficient to reach a conclusion.

The term `verified` MUST NOT be used without identifying what was verified and through which evidence category.

---

## 15. Verification Vocabulary

Public interfaces and documentation SHOULD use precise labels.

Appropriate examples include:

- transaction verified on-chain;
- allocation balance verified on-chain;
- contract source verified;
- evidence integrity anchored;
- supporting documentation reviewed;
- use of funds supported;
- outcome documented;
- impact evaluation pending;
- independently reviewed;
- disputed;
- or unable to determine.

The following vague or overstated labels SHOULD NOT be used without qualification:

- fully transparent;
- fully verified;
- completely audited;
- guaranteed impact;
- trustless;
- independently proven;
- or permanently secure.

---

## 16. Transaction Verification

### 16.1 Required data

A transaction record SHOULD identify:

- network;
- chain ID;
- transaction hash;
- block number;
- timestamp;
- sending address;
- receiving address;
- asset;
- amount;
- relevant contract;
- relevant event;
- transaction status;
- and confirmation status.

### 16.2 Address authentication

A transaction MUST NOT be attributed to GFC solely because an address label claims that it belongs to GFC.

Official addresses MUST be authenticated through:

- versioned releases;
- official registries;
- verified contract records;
- and authenticated GFC publication channels.

### 16.3 Transaction context

Where a transaction is associated with a documented purpose, the record SHOULD link to:

- allocation;
- approval;
- proposal;
- purpose;
- evidence package;
- reconciliation status;
- and applicable claim.

### 16.4 Limitations

On-chain transaction verification does not prove:

- lawful ownership;
- beneficial ownership;
- actual recipient identity;
- purpose;
- use;
- delivery;
- outcome;
- or impact.

---

## 17. Use-of-Funds Verification

### 17.1 Required elements

A use-of-funds record SHOULD identify:

- source allocation;
- approved amount;
- executing transaction;
- stated purpose;
- recipient category;
- applicable approval;
- supporting evidence;
- actual amount used;
- reconciliation status;
- unused amount;
- exceptions;
- and review status.

### 17.2 Reconciliation

Use-of-funds reconciliation SHOULD establish the relationship between:

- approved amount;
- transferred amount;
- invoiced amount;
- paid amount;
- delivered value;
- returned amount;
- and unresolved difference.

### 17.3 Evidence sufficiency

A transaction description, wallet label, internal note, or public statement MUST NOT by itself be treated as sufficient proof of use.

### 17.4 Partial use

Where only.

### 17.4 Partial use

Where only part of a payment can be reconciled to the documented purpose, the record MUST identify:

- supported amount;
- unsupported amount;
- disputed amount;
- and reason for the difference.

### 17.5 Protected evidence

Where supporting records cannot be made public, the system SHOULD disclose:

- that protected evidence exists;
- evidence category;
- integrity anchor where applicable;
- review status;
- reviewer category;
- and reason for restricted access.

---

## 18. Output, Outcome, and Impact

GFC MUST distinguish between output, outcome, and impact.

### 18.1 Output

An output is a direct deliverable or activity resulting from expenditure.

Examples may include:

- equipment delivered;
- service provided;
- infrastructure built;
- training completed;
- or material distributed.

### 18.2 Outcome

An outcome is an observable change resulting after the output.

Examples may include:

- increased access;
- reduced operating costs;
- improved service availability;
- or measurable beneficiary improvement.

### 18.3 Impact

Impact is a meaningful broader or longer-term result that can reasonably be attributed, at least in part, to the funded activity.

Impact claims require:

- methodology;
- relevant indicators;
- time period;
- evidence;
- attribution limitations;
- uncertainty;
- and review.

### 18.4 No automatic progression

A verified payment does not automatically verify an output.

A verified output does not automatically verify an outcome.

A verified outcome does not automatically prove broader impact.

---

## 19. Impact Evaluation

### 19.1 Methodology requirement

An impact claim MUST identify the applicable evaluation methodology.

The methodology SHOULD define:

- objective;
- indicators;
- baseline;
- target;
- data sources;
- collection method;
- evaluation period;
- attribution assumptions;
- limitations;
- and reviewer.

### 19.2 Attribution

Impact MUST NOT be attributed exclusively to GFC where other material causes or contributors exist unless the methodology supports that conclusion.

### 19.3 Uncertainty

Impact evaluations MUST disclose material:

- uncertainty;
- missing data;
- data-quality limitations;
- selection bias;
- attribution limits;
- and methodological constraints.

### 19.4 Negative or mixed results

The transparency system MUST permit publication of:

- unsuccessful activities;
- negative outcomes;
- mixed findings;
- unmet targets;
- and inconclusive results.

Transparency MUST NOT be limited to favorable outcomes.

### 19.5 Independent review

An impact claim MUST NOT be described as independently verified unless:

- the reviewer is identified or appropriately described;
- independence is documented;
- scope is documented;
- methodology is documented;
- limitations are published;
- and the review was not controlled solely by the party benefiting from the claim.

---

## 20. Governance Transparency

Material governance records SHOULD identify:

- proposal;
- proposer;
- affected component;
- authority;
- rationale;
- conflicts of interest;
- approval requirements;
- approval result;
- execution transaction;
- implementation status;
- and final outcome.

The transparency system MUST distinguish between:

- proposed;
- approved;
- scheduled;
- executed;
- rejected;
- cancelled;
- failed;
- superseded;
- and reversed or migrated.

A governance decision MUST NOT be presented as executed until execution can be verified.

---

## 21. Authority Transparency

The transparency system MUST expose the material control surface of production components.

For each material role, it SHOULD identify:

- role name;
- controlling address or contract;
- affected component;
- permitted actions;
- approval threshold;
- timelock;
- pause authority;
- upgrade authority;
- replacement authority;
- and current status.

The interface MUST NOT imply that a system is trustless or decentralized while material privileged authority remains undisclosed.

---

## 22. Contract Registry

Before a production contract is represented as official, the public contract registry MUST identify:

- contract name;
- purpose;
- network;
- chain ID;
- contract address;
- implementation address where applicable;
- proxy type where applicable;
- source-code repository;
- source-code commit;
- compiler version;
- verification status;
- deployment transaction;
- deployer;
- administrator;
- applicable specification version;
- audit or review status;
- known deviations;
- pause status;
- upgradeability;
- and deprecation status.

A contract MUST NOT be labeled immutable where any external mechanism can materially redirect or change its behavior.

---

## 23. Wallet Registry

Each material production wallet SHOULD identify:

- address;
- role;
- allocation;
- custody model;
- approval threshold;
- signer-category disclosure;
- permitted use;
- prohibited use;
- reporting requirements;
- and active or deprecated status.

A wallet name MUST NOT be presented as proof that its assets are technically restricted to the stated purpose.

---

## 24. Token and Allocation Transparency

The transparency system SHOULD make the following reviewable:

- fixed total supply;
- supply creation transaction;
- mint authority transaction;
- mint authority status;
- allocation percentages;
- allocation token amounts;
- recipient addresses;
- vesting contracts;
- lock contracts;
- current balances;
- released amounts;
- claimed amounts;
- transferred amounts;
- and known deviations.

The intended allocation model is:

| Allocation | Percentage | Token Amount |
|---|---:|---:|
| Impact Vault | 25% | 250,000,000 GFC |
| Guardian Growth Fund | 20% | 200,000,000 GFC |
| Presale Allocation | 15% | 150,000,000 GFC |
| Treasury Reserve | 15% | 150,000,000 GFC |
| Liquidity Reserve | 15% | 150,000,000 GFC |
| Ecosystem Growth Fund | 5% | 50,000,000 GFC |
| Core Team | 5% | 50,000,000 GFC |
| **Total** | **100%** | **1,000,000,000 GFC** |

An allocation label establishes an intended category.

It does not prove compliant use.

---

## 25. Impact Vault Transparency

The transparency system SHOULD make the following reviewable for the Impact Vault:

- initial allocation;
- vault contract;
- lock start;
- lock end;
- remaining duration;
- released amount;
- locked amount;
- migration authority;
- upgradeability;
- administrative roles;
- and any permitted extension.

The intended lock period is 50 years.

The public interface MUST NOT describe the Impact Vault as immutable or impossible to access early unless the deployed implementation technically proves that claim.

The existence of the Impact Vault MUST NOT be presented as proof that future impact will occur.

---

## 26. Core Team Vesting Transparency

The Core Team allocation is intended to vest linearly over 19 years.

The transparency system SHOULD distinguish between:

- total allocation;
- unvested amount;
- vested amount;
- vested but unclaimed amount;
- claimed amount;
- transferred amount;
- beneficiary structure;
- vesting start;
- vesting end;
- and migration or reassignment authority.

Vested tokens MUST NOT be described as locked once they are claimable.

---

## 27. Presale Transparency

The presale transparency interface SHOULD disclose:

- presale state;
- verified contract address;
- applicable specification version;
- reference price;
- supported payment assets;
- pricing method;
- conversion source;
- start time;
- end time;
- soft cap;
- Presale Allocation;
- cumulative reference value;
- cumulative GFC entitlement;
- remaining allocation;
- contribution-asset balances;
- pause state;
- finalization state;
- claim status;
- refund status;
- proceeds withdrawals;
- and unsold-token treatment.

The interface MUST distinguish between:

- purchase transaction;
- GFC entitlement;
- successful finalization;
- token claim;
- refund;
- and proceeds withdrawal.

A purchase MUST NOT be represented as a final token distribution before the applicable claim has occurred.

---

## 28. Treasury Transparency

For each material treasury action, the system SHOULD disclose:

- source wallet;
- source allocation;
- destination;
- asset;
- amount;
- approval record;
- purpose category;
- execution transaction;
- supporting evidence status;
- reconciliation status;
- and final classification.

Where recipient identity cannot be public, the system MAY use a protected recipient identifier.

The reason for restricted disclosure SHOULD be documented.

---

## 29. Liquidity Transparency

Liquidity-related transparency SHOULD include:

- venue;
- trading pair;
- deployed token amount;
- paired asset amount;
- initial price;
- liquidity-provider position;
- position custodian;
- lock status;
- lock duration;
- withdrawal authority;
- fee collection;
- rebalancing authority;
- and material changes.

Liquidity MUST NOT be described as locked unless the position is technically and publicly verifiable as locked.

---

## 30. Fee Transparency

The current intended transaction-fee model is:

- buy fee: 0%;
- sell fee: 1%.

The transparency system SHOULD disclose:

- active fee rate;
- maximum permitted fee;
- classification logic;
- recognized pools;
- exemptions;
- fee destination;
- fee amount collected;
- fee distribution;
- and any parameter changes.

Fee revenue MUST NOT be labeled impact funding unless its allocation and actual use are separately evidenced.

---

## 31. Staking Transparency

Where staking is introduced, the transparency system SHOULD disclose:

- staking contract;
- reward source;
- reward allocation;
- reward rate;
- calculation method;
- duration;
- total staked;
- distributed rewards;
- remaining reward allocation;
- lock conditions;
- withdrawal conditions;
- administrative authority;
- governance rights;
- and known risks.

A displayed annual percentage rate MUST NOT be presented as guaranteed.

---

## 32. Evidence Packages

A material use-of-funds or impact claim MAY be represented through an evidence package.

An evidence package SHOULD include:

- unique package identifier;
- related claim;
- related allocation;
- related transaction;
- intended purpose;
- evidence inventory;
- evidence disclosure levels;
- evidence provenance;
- integrity anchors;
- reviewer;
- review status;
- limitations;
- disputes;
- publication date;
- and version.

The package MUST distinguish between public documents and protected documents.

A package MUST NOT imply that all evidence is public merely because the package itself is publicly listed.

---

## 33. Record Identifiers

Material transparency records SHOULD use durable identifiers.

Record types may include:

- contract record;
- wallet record;
- transaction record;
- governance record;
- allocation record;
- evidence record;
- use-of-funds record;
- outcome record;
- impact record;
- dispute record;
- incident record;
- and correction record.

Identifiers SHOULD remain stable across portal updates and migrations.

---

## 34. Record Linkage

The transparency infrastructure SHOULD allow records to be linked across the full lifecycle.

A material fund-flow record SHOULD support linkage between:

1. funding source;
2. allocation;
3. authority;
4. proposal;
5. approval;
6. execution;
7. transaction;
8. evidence;
9. reconciliation;
10. output;
11. outcome;
12. impact evaluation;
13. dispute;
14. and final status.

The absence of a later-stage record MUST NOT alter the existence of an earlier-stage record.

For example, a missing impact evaluation does not invalidate a real transaction, but it limits the permissible impact claim.

---

## 35. Cryptographic Anchoring Requirements

### 35.1 Content-specific commitments

An anchor MUST correspond to a defined record or record set.

### 35.2 Version awareness

Where a document changes, the updated version SHOULD receive a new integrity commitment.

The earlier commitment MUST remain historically reviewable.

### 35.3 Confidentiality protection

Low-entropy documents or predictable identifiers MUST NOT be hashed without appropriate protection where brute-force reconstruction or confirmation is reasonably possible.

Protection MAY include:

- salting;
- keyed hashing;
- structured commitments;
- selective disclosure;
- or Merkle-tree methods.

### 35.4 Anchor metadata

An anchor record SHOULD identify:

- anchoring method;
- hash algorithm;
- creation time;
- publication transaction;
- record identifier;
- version;
- and responsible role.

### 35.5 Algorithm migration

The system MUST define how evidence remains verifiable if the selected cryptographic algorithm becomes unsuitable.

Migration MUST preserve historical linkage.

---

## 36. Protected Evidence

### 36.1 Access control

Protected evidence MUST use role-based access.

### 36.2 Access logging

Access SHOULD be logged where technically and legally appropriate.

### 36.3 Purpose limitation

Protected evidence MUST be accessed only for legitimate:

- verification;
- accounting;
- legal;
- security;
- operational;
- or impact-evaluation purposes.

### 36.4 Reviewer access

Reviewers SHOULD receive only the information required for the defined review scope.

### 36.5 Public representation

Where protected evidence exists, the portal MAY display:

- evidence category;
- existence status;
- integrity status;
- review status;
- reviewer category;
- access restriction;
- and limitation.

The portal MUST NOT claim that protected evidence was independently verified where no qualifying independent review occurred.

---

## 37. Privacy and Data Protection

### 37.1 Data minimization

GFC SHOULD collect and disclose only information necessary for:

- verification;
- accountability;
- compliance;
- security;
- operations;
- or legitimate impact evaluation.

### 37.2 Personal data on-chain

Personal data SHOULD NOT be published directly on-chain.

### 37.3 Beneficiary protection

Beneficiary information MUST NOT be published merely to strengthen a public impact narrative.

### 37.4 Wallet linkage

Wallet addresses MUST NOT be publicly linked to identified natural persons without lawful basis and appropriate disclosure.

### 37.5 Retention

The final transparency system MUST define:

- retention periods;
- deletion procedures;
- archival requirements;
- legal holds;
- redaction;
- and treatment of immutable on-chain references.

### 37.6 Consent limitations

Consent MUST NOT be treated as the only possible lawful basis or as automatically valid in contexts involving power imbalance or vulnerable beneficiaries.

---

## 38. Transparency Portal

### 38.1 Purpose

The public transparency portal is intended to aggregate and explain reviewable GFC records.

### 38.2 Read-only authority

The portal SHOULD remain separate from custody and governance execution.

It MUST NOT possess undisclosed authority to:

- transfer funds;
- modify contract state;
- approve transactions;
- change allocation balances;
- change governance outcomes;
- or alter historical evidence status.

### 38.3 Data-source labeling

Every material portal record SHOULD identify whether it is based on:

- direct on-chain data;
- indexed on-chain data;
- project-submitted information;
- external information;
- cryptographically anchored evidence;
- protected evidence;
- internal review;
- or independent review.

### 38.4 Verification links

Where possible, on-chain records SHOULD link to an appropriate Base block explorer or other direct verification source.

### 38.5 Status accuracy

The portal MUST distinguish between:

- planned;
- configured;
- deployed;
- active;
- paused;
- deprecated;
- migrated;
- and unavailable.

### 38.6 No false source of truth

The portal MUST NOT override actual on-chain behavior.

Where portal data conflicts with authenticated on-chain state, the conflict MUST be disclosed and investigated.

### 38.7 Availability limitations

Portal unavailability MUST NOT remove access to core authenticated contract and transaction records.

---

## 39. Data Indexing and Derived Information

Indexed and derived information may differ from raw on-chain data due to:

- indexing delay;
- provider outage;
- chain reorganization;
- parsing error;
- incorrect token metadata;
- or software defect.

Derived data MUST be identifiable as derived.

Where material, the portal SHOULD display:

- last update time;
- indexed block;
- data source;
- and known delay.

The system MUST support reconciliation against direct on-chain state.

---

## 40. Historical Integrity

### 40.1 Version history

Material records SHOULD retain:

- original publication date;
- latest update date;
- prior versions;
- responsible publisher;
- reason for change;
- and applicable integrity references.

### 40.2 No silent deletion

Material records MUST NOT be silently removed merely because they became unfavorable, incorrect, disputed, or outdated.

### 40.3 Redaction

Where information must be removed for privacy, security, or legal reasons, the historical record SHOULD indicate:

- that redaction occurred;
- date;
- authority;
- and reason category.

The removed protected content itself MUST NOT be preserved publicly.

### 40.4 Supersession

A corrected record SHOULD link to the record it supersedes.

The superseded record SHOULD link to the correction.

---

## 41. Corrections

A material correction SHOULD identify:

- incorrect statement or record;
- corrected information;
- date of correction;
- reason;
- responsible authority;
- affected claims;
- and whether previous conclusions changed.

Corrections MUST NOT be presented as if the original error never existed.

Minor typographical corrections that do not alter meaning MAY use a lighter correction process.

---

## 42. Disputes and Challenges

The transparency infrastructure SHOULD support challenges concerning:

- transaction attribution;
- wallet ownership;
- authority;
- approval;
- use of funds;
- evidence authenticity;
- evidence completeness;
- evidence status;
- outcome claims;
- impact claims;
- reviewer independence;
- conflicts of interest;
- or implementation conformance.

The dispute process MUST define:

- eligible challenger;
- submission method;
- evidence requirements;
- reviewer;
- response period;
- possible status changes;
- and reconsideration or appeal where applicable.

A challenged record SHOULD be marked as disputed while a material challenge remains unresolved.

---

## 43. Independent Review

### 43.1 Independence criteria

A review MUST NOT be labeled independent solely because the reviewer is external.

Relevant factors include:

- financial relationship;
- control relationship;
- prior involvement;
- scope restriction;
- data access;
- methodology control;
- and ability to publish unfavorable findings.

### 43.2 Review scope

An independent-review record SHOULD identify:

- reviewer;
- subject;
- period;
- evidence accessed;
- methodology;
- exclusions;
- findings;
- limitations;
- and date.

### 43.3 Review does not imply universal assurance

A security audit does not verify fund use or impact.

An accounting review does not prove smart-contract security.

An impact evaluation does not prove contract correctness.

Each review MUST be presented only within its defined scope.

---

## 44. Audits

The term `audit` MUST be used precisely.

An audit record SHOULD identify:

- auditor;
- audit type;
- scope;
- standards or methodology;
- reviewed components;
- exclusions;
- report date;
- findings;
- remediation status;
- and applicable implementation version.

A code review, informal review, automated scan, or internal check MUST NOT automatically be described as an audit.

---

## 45. Limitations and Uncertainty

Every material transparency surface SHOULD disclose relevant limitations.

Potential limitations include:

- incomplete evidence;
- protected evidence;
- unavailable evidence;
- reliance on self-reporting;
- reviewer conflict;
- data delay;
- indexing error;
- oracle dependency;
- methodology limitations;
- attribution uncertainty;
- legal restrictions;
- and unresolved dispute.

Limitations MUST NOT be hidden solely because they weaken a public claim.

---

## 46. Negative Information

The transparency model MUST permit publication of:

- failed initiatives;
- overspending;
- underspending;
- delayed delivery;
- unreconciled transactions;
- unsupported claims;
- rejected evidence;
- disputes;
- incidents;
- audit findings;
- governance failures;
- and negative impact findings.

Transparency limited to positive information is not sufficient.

---

## 47. Transparency and Communication

Public communication MUST distinguish between:

- what GFC intends to do;
- what specifications require;
- what has been implemented;
- what has been deployed;
- what executed on-chain;
- what has supporting evidence;
- what was reviewed;
- and what was independently verified.

Marketing, social media, articles, and interfaces MUST NOT overstate the current transparency status.

The phrase `fully transparent` SHOULD NOT be used as an absolute description.

---

## 48. Transparency and Legal Responsibility

Public transparency does not replace:

- legal obligations;
- contractual obligations;
- accounting obligations;
- data-protection obligations;
- tax obligations;
- regulatory obligations;
- or fiduciary responsibility where applicable.

A public record MUST NOT be treated as automatically legally sufficient merely because it is on-chain.

---

## 49. Security Requirements

The transparency infrastructure MUST protect against:

- unauthorized record modification;
- evidence deletion;
- false evidence-status assignment;
- unauthorized protected-data access;
- integrity-anchor mismatch;
- portal compromise;
- domain compromise;
- fake contract addresses;
- indexer manipulation;
- database corruption;
- privilege escalation;
- and audit-log deletion.

Security controls SHOULD include:

- least privilege;
- strong authentication;
- role separation;
- immutable or append-only logs where appropriate;
- backups;
- monitoring;
- authenticated releases;
- cryptographic verification;
- and incident response.

---

## 50. Transparency Incidents

Transparency incidents may include:

- publication of false information;
- incorrect wallet attribution;
- altered evidence;
- missing evidence;
- unauthorized evidence access;
- false independent-review claims;
- concealed conflicts;
- false impact claims;
- portal compromise;
- indexer failure;
- incorrect contract data;
- privacy breach;
- or historical-record deletion.

A material incident SHOULD identify:

- incident identifier;
- detection time;
- affected records;
- affected claims;
- responsible authority;
- containment;
- correction;
- disclosure status;
- and continuing risk.

---

## 51. Required Transparency Invariants

The implementation MUST preserve at least the following invariants:

1. On-chain execution and off-chain claims remain distinguishable.
2. Transaction verification is not represented as use-of-funds verification.
3. Use-of-funds verification is not represented as impact verification.
4. Cryptographic anchoring is not represented as proof of factual truth.
5. Project-authored evidence is not represented as independent evidence.
6. Protected evidence is not represented as publicly available evidence.
7. Material authority remains identifiable.
8. Material records retain historical accountability.
9. Corrections do not silently erase previous materially different records.
10. Evidence status and claim status remain separate.
11. The strength of a claim does not exceed the strength of its evidence.
12. Disputed claims are marked appropriately.
13. Material limitations remain visible.
14. Personal data is not published on-chain without adequate justification.
15. Portal data can be reconciled against authenticated primary sources.
16. Wallet labels are not treated as technical restrictions.
17. Allocation labels are not treated as proof of compliant use.
18. Impact claims identify methodology and uncertainty.
19. Reviewer independence is not assumed solely from external status.
20. Planned functionality is not presented as active functionality.

---

## 52. Conformance

A transparency implementation conforms to this specification only when:

- it identifies an applicable versioned specification release;
- it distinguishes transaction, use-of-funds, and impact verification;
- it distinguishes Technology, Governance, and Impact and Evidence layers;
- it distinguishes Public On-Chain, Cryptographically Anchored, and Protected Off-Chain evidence;
- evidence provenance is available;
- claim status and evidence status are separate;
- authority is disclosed;
- official contracts and wallets are authenticated;
- protected evidence is access-controlled;
- cryptographic anchoring is not overstated;
- historical records remain reviewable;
- corrections are documented;
- disputes can be represented;
- limitations are visible;
- public communication reflects actual implementation status;
- and material deviations are disclosed.

---

## 53. Non-Conformance

Transparency non-conformance includes:

- presenting visibility as verification;
- presenting a transaction as proof of impact;
- false wallet attribution;
- undisclosed authority;
- unsupported use-of-funds claims;
- unsupported impact claims;
- project-authored evidence presented as independent;
- cryptographic anchoring presented as proof of factual truth;
- silent record modification;
- silent deletion;
- concealed dispute;
- concealed limitation;
- unauthorized protected-data access;
- false audit claims;
- false independent-review claims;
- or presenting planned infrastructure as operational.

Material non-conformance MAY require:

- correction;
- status downgrade;
- public disclosure;
- record withdrawal;
- independent review;
- portal suspension;
- access revocation;
- incident treatment;
- specification update;
- or system migration.

The specification MUST NOT be revised retrospectively merely to conceal transparency non-conformance.

---

## 54. Transparency Non-Goals

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
- or claim that trust can be eliminated entirely.

The objective is to make trust dependencies visible, constrained, and reviewable.

---

## 55. Unresolved Transparency Decisions

The following matters remain unresolved and MUST be completed before this document can become Stable.

### 55.1 Evidence schema

- record fields;
- required metadata;
- evidence identifiers;
- claim identifiers;
- evidence-package format;
- and relationship model.

### 55.2 Evidence status

- final status vocabulary;
- transition authority;
- review requirements;
- dispute effects;
- and supersession rules.

### 55.3 Claim status

- final claim-status vocabulary;
- evidence thresholds;
- independent-support standard;
- and status-downgrade rules.

### 55.4 Cryptographic anchoring

- hash algorithms;
- anchoring method;
- Base contract or transaction mechanism;
- Merkle-tree design;
- salting;
- versioning;
- and algorithm migration.

### 55.5 Protected evidence

- storage provider;
- encryption;
- access roles;
- access logging;
- retention;
- backup;
- recovery;
- deletion;
- and legal-hold procedures.

### 55.6 Portal

- implementation architecture;
- data sources;
- indexers;
- update frequency;
- availability requirements;
- authentication;
- and fallback access.

### 55.7 Review

- reviewer categories;
- independence criteria;
- reviewer appointment;
- review scope;
- evidence-access process;
- and publication requirements.

### 55.8 Impact

- methodology framework;
- indicator selection;
- baseline requirements;
- attribution model;
- uncertainty model;
- evaluator appointment;
- and verification terminology.

### 55.9 Disputes

- submission process;
- eligible challengers;
- review authority;
- response periods;
- appeals;
- and public status treatment.

### 55.10 Privacy

- legal roles;
- lawful bases;
- beneficiary consent;
- retention periods;
- deletion;
- redaction;
- international transfers;
- and breach response.

### 55.11 Historical records

- append-only model;
- correction format;
- archive location;
- integrity verification;
- and long-term preservation.

---

## 56. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- the evidence schema is finalized;
- the claim model is finalized;
- the evidence-status model is finalized;
- the claim-status model is finalized;
- contract and wallet registries are specified;
- the authority registry is specified;
- the evidence anchoring mechanism is finalized;
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
- impact methodology requirements are finalized;
- limitation and uncertainty disclosures are finalized;
- privacy responsibilities are identified;
- security controls are reviewed;
- incident procedures are defined;
- implementation feasibility is confirmed;
- public terminology is consistent;
- and all related specifications are mutually consistent.

---

## 57. Final Transparency Principles

The GFC transparency model preserves the following distinctions:

> Visibility is not the same as verifiability.

> Public does not automatically mean verified.

> A wallet address shows movements, not motives or authority.

> Transaction verification does not prove use of funds.

> Use-of-funds verification does not automatically prove impact.

> Cryptographic anchoring proves integrity, not factual truth.

> A public explanation does not replace evidence.

> Project-authored evidence is not automatically independent evidence.

> Protected evidence can remain reviewable without being publicly exposed.

> Different claims require different evidence.

Transparency is credible only where execution, authority, purpose, evidence, outcomes, limitations, and historical changes can be examined together.

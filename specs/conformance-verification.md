# GFC Conformance Verification Specification

**Document ID:** GFC-CONF-001  
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

This document defines the current intended verification layer between GFC normative conformance requirements and the evidence used to evaluate those requirements.

It is normative because it defines:

- how a conformance requirement is mapped to observable evidence;
- how implementation-specific verification bindings are authenticated;
- which evidence classes may support a claim;
- how evidence ceilings limit the conclusion that may be drawn;
- how production and pilot observations remain separated;
- how state reads, events, transaction history, code review, authority review, and protected evidence may be combined;
- how missing or unresolved implementation bindings are represented;
- and how automated or manual verification results must be described.

Its maturity remains Draft.

At the current repository state:

- the **GFC Token / Economic Layer** is the current primary product focus;
- a public pilot exists on **Base Sepolia**;
- no official GFC token is deployed on Base Mainnet;
- no production GFC presale is live;
- no production allocation, vesting, governance, treasury, staking, or presale contracts are established as official by this document;
- no production ABI, event set, storage layout, proxy configuration, authority graph, or contract address is established as official by this document;
- no production implementation-specific verification binding is represented as complete;
- no read-only Base Mainnet conformance checker is represented as deployed or operational;
- and no verification result described by this document may be interpreted as production evidence unless it is tied to an authenticated production deployment and the applicable versioned specification release.

The Base Sepolia pilot MAY be used to test verification concepts.

Pilot observations MUST NOT be represented as Base Mainnet production conformance evidence.

Current project and deployment status is maintained in [`../STATUS.md`](../STATUS.md).

---

## 2. Purpose

The purpose of this specification is to make the transition from:

**requirement → observation → evidence → supported conclusion**

explicit and reviewable.

The GFC specification set already defines what a conforming implementation is intended to do.

This document defines how a reviewer, auditor, integration, monitoring service, or future read-only checker can determine what evidence is relevant to a specific requirement and how far that evidence can support a conformance claim.

The objective is to prevent statements such as:

> "The allocation is correct."

> "The vault is locked."

> "The supply is fixed."

> "The multisig is independent."

> "The presale is participant-protected."

from being treated as equivalent merely because some related on-chain state is visible.

Different requirements require different verification methods.

A successful state read MAY prove a current value.

It does not automatically prove:

- absence of a hidden privileged path;
- historical compliance;
- signer independence;
- compliant use of funds;
- factual truth of an anchored record;
- successful outcomes;
- verified impact;
- or complete system conformance.

---

## 3. Relationship to the GFC Accountability Model

The long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

This specification primarily connects **Rules** and **Evidence**.

For a material conformance claim, the verification model SHOULD make it possible to reconstruct:

1. the applicable normative requirement;
2. the applicable specification version;
3. the evaluated environment;
4. the authenticated implementation;
5. the evidence source;
6. the observation method;
7. the observed result;
8. the conclusion supported by that result;
9. the evidence ceiling;
10. any unresolved or non-observable dependency;
11. any deviation;
12. and the time or block context of the evaluation.

Verification is therefore not a binary property of a document or contract.

It is a relationship between a specific claim and the evidence available to support that claim.

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

This specification defines:

- conformance-verification terminology;
- requirement-to-observation mapping;
- verification-record structure;
- evidence classes;
- evidence ceilings;
- verification availability;
- environment binding;
- deployment binding;
- implementation-specific bindings;
- state-read verification;
- event verification;
- transaction-history verification;
- source-code and bytecode review;
- proxy and upgrade-path review;
- authority verification;
- historical-state verification;
- negative observations;
- protected off-chain evidence boundaries;
- mixed-evidence evaluation;
- token verification mappings;
- allocation verification mappings;
- lock and vesting verification mappings;
- governance verification mappings;
- presale verification boundaries;
- transparency and evidence verification boundaries;
- machine-readable result categories;
- automated checker constraints;
- change management;
- conformance;
- and requirements before Stable status.

---

## 6. Out of Scope

This document does not independently define:

- final production smart-contract code;
- final production ABI;
- final production event signatures;
- final storage slots or layouts;
- final contract addresses;
- final wallet addresses;
- final proxy architecture;
- final governance implementation;
- final multisig platform;
- final signer identities;
- final authority holders;
- final presale custody architecture;
- final vesting implementation;
- final Impact Vault implementation;
- final staking implementation;
- final Transparency Registry implementation;
- final protected-evidence storage;
- final impact methodology;
- a production monitoring service;
- a production conformance checker;
- an audit opinion;
- legal compliance;
- regulatory compliance;
- or factual truth of real-world claims.

Those matters belong to their applicable specifications, implementation records, deployment records, audits, policies, or legal processes.

This specification MUST NOT be used to invent an implementation detail that has not yet been established.

---

## 7. Verification Principles

### 7.1 Source requirement remains authoritative

The source specification defines the normative requirement.

This document defines how evidence may be used to evaluate that requirement.

A verification mapping MUST NOT silently weaken, broaden, or replace the source requirement.

### 7.2 Claim-specific verification

Verification MUST be performed against a specific claim or requirement.

A generic statement that a contract is `verified` is insufficient.

### 7.3 Evidence ceiling

Every verification method MUST identify the strongest conclusion that the evidence can support.

Evidence MUST NOT be interpreted beyond that ceiling.

### 7.4 Authenticated implementation first

A production observation is meaningful only when the evaluated address, contract, wallet, implementation, proxy, code artifact, or record has been authenticated as belonging to the applicable production deployment.

### 7.5 Environment separation

Base Sepolia and Base Mainnet MUST be treated as separate verification environments.

A Base Sepolia observation MUST NOT support a Base Mainnet production claim.

### 7.6 Current state is not complete history

A current state read proves a current value at a defined block or time.

It does not automatically prove the complete historical path that produced that value.

### 7.7 State is not capability

A current state value does not automatically prove that a privileged role lacks the capability to change that value later.

Where future capability matters, code and authority review are required.

### 7.8 Code is not operation

Source or bytecode review may establish technical capability or constraints.

It does not independently establish that operational processes, signer independence, off-chain approvals, or protected-evidence handling complied with the applicable rules.

### 7.9 Anchoring is not factual truth

A cryptographic commitment may establish integrity, version linkage, or timing.

It does not independently establish that the anchored content is factually correct.

### 7.10 No invented production bindings

Until a production interface or architecture is finalized and authenticated, implementation-specific reads, events, storage slots, addresses, and role identifiers MUST remain explicitly unbound.

---

## 8. Verification Record Model

Each material conformance-verification mapping SHOULD contain the following fields.

| Field | Requirement |
|---|---|
| Verification ID | Stable identifier for the mapping |
| Requirement | Human-readable normative requirement |
| Source Specification | File and section containing the requirement |
| Applicable Version | Specification release or version |
| Environment | Pilot, production candidate, or production environment |
| Network | Network name and chain ID where applicable |
| Verification Category | State, history, code, authority, anchored, protected, mixed, or other defined category |
| Expected Observation | What must be observed or reviewed |
| Implementation Binding | Concrete authenticated call, event, address, role, code path, or record where available |
| Reference Context | Block, block range, transaction, timestamp, or record version where relevant |
| Evidence Class | Public On-Chain, Cryptographically Anchored, Protected Off-Chain, or Mixed |
| Evidence Ceiling | Strongest conclusion supported |
| Required Corroboration | Additional evidence needed for the full claim |
| Verification Availability | Whether evaluation is currently possible |
| Result | Result of an actual evaluation, where performed |
| Deviation | Known deviation, if any |

A verification mapping MAY exist before an implementation binding exists.

A production verification result MUST NOT exist without an authenticated implementation binding where the verification depends on a specific implementation.

---

## 9. Verification Categories

### 9.1 State Read

A deterministic read of authenticated contract state at a defined block.

Examples include:

- ERC-20 supply;
- ERC-20 balance;
- role membership;
- configured threshold;
- configured fee;
- vesting schedule parameters;
- pause state;
- or another authenticated public state value.

### 9.2 Event or Log Observation

An authenticated event or log emitted by the evaluated implementation.

Events MAY support historical reconstruction.

An event MUST NOT be treated as sufficient where the contract can change material state without emitting the expected event.

### 9.3 Transaction-History Observation

Review of authenticated transaction history, traces, receipts, or historical state.

This category is especially relevant for:

- initialization;
- allocation funding;
- migrations;
- treasury movements;
- upgrades;
- role changes;
- and historical release behavior.

### 9.4 Source-Code or Bytecode Review

Review of authenticated source code, verified bytecode correspondence, runtime bytecode, proxy implementation, or equivalent executable logic.

This category is required where the claim concerns technical capability rather than only current state.

### 9.5 Authority Review

Review of the effective control surface.

It may include:

- owners;
- administrators;
- roles;
- multisig signers;
- thresholds;
- timelocks;
- proxy administrators;
- upgrade executors;
- emergency roles;
- backend signers;
- and operational authority.

### 9.6 Cryptographic Anchor Review

Verification that a public commitment corresponds to a specific record or record version.

### 9.7 Protected Off-Chain Review

Review of evidence that cannot appropriately be published on-chain.

### 9.8 Mixed Verification

A claim that requires more than one category.

Examples include:

- a lock claim requiring state + code + authority review;
- a treasury-use claim requiring transaction evidence + protected documentation;
- or an independent-verification claim requiring public records + reviewer-independence evidence.

---

## 10. Evidence Classes

This document uses the evidence-disclosure classes defined by [`transparency-model.md`](transparency-model.md).

### 10.1 Public On-Chain

Evidence recorded on or directly derivable from authenticated blockchain data.

### 10.2 Cryptographically Anchored

Off-chain evidence linked to a public cryptographic commitment.

### 10.3 Protected Off-Chain

Evidence that remains outside the public blockchain because public disclosure would be inappropriate or unsafe.

### 10.4 Mixed

A verification may depend on more than one evidence class.

`Mixed` is a verification composition label.

It does not replace the underlying evidence classes.

---

## 11. Evidence Ceiling

An evidence ceiling defines the strongest claim supported by the available evidence.

### 11.1 Current balance ceiling

A balance read may support:

> "Address X held Y GFC at reference block B."

It does not independently support:

> "The allocation was originally created correctly."

> "The funds were used correctly."

> "The address is independently controlled."

### 11.2 Supply ceiling

An ERC-20 `totalSupply()` read may support:

> "The authenticated token reported supply S at reference block B."

It does not independently prove:

> "No future mint path exists."

That stronger claim requires review of executable mint capability, upgradeability, migration, and authority.

### 11.3 Lock-state ceiling

A lock-end or releasable-amount state read may support the represented schedule state at a defined block.

It does not independently prove that an owner, upgrader, migrator, rescue role, or external authority cannot bypass the schedule.

### 11.4 Multisig-state ceiling

An authenticated owner set and threshold may support:

> "The multisig was configured with this owner set and threshold at reference block B."

It does not independently prove signer independence.

### 11.5 Anchor ceiling

A matching content hash may support:

> "This exact record corresponds to the public commitment."

It does not independently support:

> "The record is factually true."

### 11.6 Negative-history ceiling

Absence of a transaction or event in a defined block range may support:

> "No matching observable action was found in the reviewed range."

It does not automatically prove that the action was technically impossible.

---

## 12. Verification Availability

Each mapping MUST distinguish verification availability from the outcome of verification.

The following availability states are defined.

### 12.1 Specification Only

The normative requirement exists, but no authenticated implementation-specific production binding exists.

No production technical verification may be claimed.

### 12.2 Binding Pending

An implementation may exist or be under development, but the authoritative mapping to the applicable deployment has not been completed or authenticated.

### 12.3 Evaluatable

The required implementation binding and evidence sources exist and can be evaluated.

### 12.4 Partially Evaluatable

Some required evidence sources exist, but the full claim depends on additional evidence that is unavailable, protected, unresolved, or not yet authenticated.

### 12.5 Not Directly Observable

The requirement is legitimate but cannot be established through a direct public on-chain read.

### 12.6 Not Applicable

The requirement does not apply to the evaluated implementation or environment, with rationale documented.

Verification availability MUST NOT be represented as a successful verification result.

---

## 13. Environment Binding

Every on-chain verification result MUST identify:

- network;
- chain ID;
- authenticated contract or wallet;
- reference block or block range where relevant;
- and applicable deployment record.

For the current GFC architecture:

```text
Base Sepolia
Chain ID: 84532
Status role: public pilot / non-production
```

and:

```text
Base Mainnet
Chain ID: 8453
Status role: intended production network / no official production GFC deployment established by this document
```

are separate environments.

A checker, dashboard, report, or manual review MUST NOT silently switch between them.

---

## 14. Authenticated Implementation Binding

A production implementation-specific verification binding connects a normative requirement to the exact implementation surface used to evaluate it.

A binding SHOULD identify, where applicable:

- binding identifier;
- source requirement;
- specification release;
- network and chain ID;
- authenticated contract address;
- proxy address;
- implementation address;
- runtime bytecode hash or equivalent implementation identifier;
- source-code commit;
- ABI or interface artifact;
- function signature;
- event signature;
- role identifier;
- storage location where direct storage review is required;
- transaction or initialization reference;
- expected condition;
- required historical range;
- and evidence ceiling.

A binding MUST be versioned when a material implementation change alters the verification method.

A binding MUST NOT be inferred merely from:

- a contract name;
- a frontend label;
- a GitHub filename;
- an unauthenticated address;
- or similarity to a pilot implementation.

---

## 15. Standard Interface Observations

Where the applicable production token is ERC-20 compatible, standard ERC-20 observations MAY be used after the production token address is authenticated.

Examples include:

```text
totalSupply()
decimals()
balanceOf(address)
```

These standard observations MUST still identify:

- the authenticated token;
- the reference block;
- the expected condition;
- and the evidence ceiling.

A standard ERC-20 read does not remove the need to authenticate the implementation.

Non-standard GFC-specific reads MUST NOT be named as production verification sources until the actual production interface is finalized and bound.

---

## 16. Historical-State Verification

Some requirements concern an initial or historical state rather than the current state.

Examples include:

- initial allocation;
- initial role configuration;
- deployment-time minting;
- migration;
- threshold changes;
- or presale contribution history.

Where later transactions may change the current state, verification MUST use an authenticated historical reference such as:

- deployment transaction;
- initialization transaction;
- allocation transaction set;
- reference block;
- archive-state query;
- indexed event history validated against executable behavior;
- or another authenticated historical source.

Current balances MUST NOT be used as the sole evidence for an initial-allocation claim after allocations have begun moving.

---

## 17. Negative Observations

A negative observation asserts that a defined action was not observed.

Examples include:

- no post-initialization mint;
- no early release transaction;
- no unauthorized role change;
- no withdrawal before a defined state transition.

A negative observation MUST define:

- observed address set;
- relevant contract set;
- block range;
- event or transaction criteria;
- trace requirements where applicable;
- proxy or migration scope;
- and known blind spots.

A negative observation MUST NOT be described as proving technical impossibility unless code and authority review establish that no applicable execution path exists.

---

## 18. Code and Capability Review

Claims about what a system **cannot** do normally require review of executable capability.

Examples include:

- no discretionary minting;
- no administrative early release;
- no hidden fee increase;
- no arbitrary confiscation;
- no upgrade-based bypass;
- no unrestricted rescue path.

The review MUST consider the effective architecture, including where applicable:

- runtime bytecode;
- verified source correspondence;
- proxy implementation;
- proxy administrator;
- delegatecall or routing paths;
- external authorization contracts;
- role hierarchy;
- migration authority;
- token replacement authority;
- recovery functions;
- and privileged backend execution.

Review of only one contract is insufficient where another privileged component can effectively replace or bypass its behavior.

---

## 19. Authority Verification

Authority verification MUST distinguish between technical control and organizational independence.

### 19.1 Technical authority

Technical authority MAY be observable through:

- owner state;
- access-control roles;
- multisig configuration;
- timelock configuration;
- proxy administration;
- upgrade executor;
- pause role;
- or equivalent authenticated implementation state.

### 19.2 Signer independence

Signer independence is not established merely because several addresses are listed as signers.

Independence may require protected or organizational evidence concerning:

- beneficial control;
- device separation;
- organizational affiliation;
- shared recovery;
- delegated control;
- or contractual dependence.

A read-only on-chain checker MUST NOT classify signer independence as verified solely from distinct addresses.

### 19.3 Complete authority surface

A documented authority registry MAY be compared against authenticated technical control.

Absence of an authority from the registry does not prove the authority does not exist.

Code, deployment, backend, operational, and wallet review may be necessary.

---

# Token Verification Mapping

## 20. Token Conformance Mapping

The mappings below define minimum verification intent for [`token.md`](token.md).

They do not establish a production implementation binding.

### 20.1 Token identity and decimals

| Field | Mapping |
|---|---|
| Verification ID | `TKN-ID-001` |
| Requirement | Production token identity and 18 decimals |
| Source | `token.md` §§7–10, §42 |
| Expected Observation | Authenticated production token identity; ERC-20 `decimals()` equals `18`; name and symbol match the applicable release where those values are normative |
| Evidence | Public On-Chain + authenticated deployment record |
| Production Binding | Specification Only until a production token is authenticated |
| Evidence Ceiling | Supports identity and configured metadata/precision for the evaluated deployment; does not prove audit status or broader conformance |

### 20.2 Fixed current supply

| Field | Mapping |
|---|---|
| Verification ID | `TKN-SUP-001` |
| Requirement | Canonical supply does not exceed the applicable fixed supply |
| Source | `token.md` §§11–15, §35, §42 |
| Expected Observation | ERC-20 `totalSupply()` on the authenticated production token equals or remains within the applicable fixed-supply rule |
| Evidence | Public On-Chain |
| Production Binding | Specification Only until a production token is authenticated |
| Evidence Ceiling | Supports current reported supply at the reference block; does not prove absence of a future mint or upgrade path |

### 20.3 No discretionary inflation capability

| Field | Mapping |
|---|---|
| Verification ID | `TKN-SUP-002` |
| Requirement | No surviving discretionary authority may increase supply contrary to the fixed-supply specification |
| Source | `token.md` §§12–15, §§30–32, §35 |
| Expected Observation | Review of authenticated executable mint capability, privileged roles, proxy/upgrade path, migration path, and any supply-creation mechanism |
| Evidence | Public On-Chain + source/bytecode review + authority review |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports absence of identified discretionary inflation paths in the reviewed architecture; does not eliminate unknown implementation or operational risks outside the reviewed scope |

### 20.4 Fee behavior

| Field | Mapping |
|---|---|
| Verification ID | `TKN-FEE-001` |
| Requirement | Buy, sell, and ordinary-transfer fee behavior matches the applicable release |
| Source | `token.md` §§18–25, §42 |
| Expected Observation | Authenticated fee configuration where exposed; transaction-level test vectors; code-path review for classification, exemptions, destination, and maximum fee |
| Evidence | Public On-Chain + code review |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports configured and executable fee behavior in the reviewed paths; does not prove future behavior if authorized mutation remains possible |

### 20.5 Token authority and upgradeability

| Field | Mapping |
|---|---|
| Verification ID | `TKN-AUTH-001` |
| Requirement | Token-level administrative authority, upgradeability, pause, migration, and relevant privileged control are fully disclosed |
| Source | `token.md` §§26–32, §§38–42 |
| Expected Observation | Authenticated technical authority compared with published deployment and authority records |
| Evidence | Public On-Chain + authority review + deployment records |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports the identified technical control surface; does not independently prove organizational independence or completeness of undisclosed off-chain authority |

---

# Allocation Verification Mapping

## 21. Allocation Conformance Mapping

The mappings below define minimum verification intent for [`allocations.md`](allocations.md).

### 21.1 Allocation arithmetic

| Field | Mapping |
|---|---|
| Verification ID | `ALC-MATH-001` |
| Requirement | Canonical percentages equal 100% and canonical token amounts equal 1,000,000,000 GFC |
| Source | `allocations.md` §§7–8 |
| Expected Observation | Deterministic specification arithmetic |
| Evidence | Versioned specification |
| Production Binding | Not implementation-specific |
| Evidence Ceiling | Supports internal arithmetic consistency of the specification only; does not prove deployed allocation |

### 21.2 Initial production allocation reconciliation

| Field | Mapping |
|---|---|
| Verification ID | `ALC-INIT-001` |
| Requirement | The complete initial production supply is reconciled to the seven canonical allocations with no undisclosed eighth allocation |
| Source | `allocations.md` §§7–9, §22, §30, §33 |
| Expected Observation | Authenticated token supply + authenticated allocation addresses/contracts + initialization transactions or historical state at the defined allocation reference block |
| Evidence | Public On-Chain + authenticated deployment/allocation records |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports initial allocation reconciliation at the authenticated reference point; does not prove later custody, compliant use, or continuing balances |

### 21.3 Allocation identity and custody

| Field | Mapping |
|---|---|
| Verification ID | `ALC-CUST-001` |
| Requirement | Each material production allocation is independently identifiable and its custody/authority surface is disclosed |
| Source | `allocations.md` §§9–12, §28, §33 |
| Expected Observation | Authenticated allocation address or contract; current custody state; controlling roles; published allocation record |
| Evidence | Public On-Chain + authority/deployment records |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports technical custody and disclosed control at the reference point; does not establish legitimate purpose, legal ownership, or signer independence |

### 21.4 Impact Vault restriction

| Field | Mapping |
|---|---|
| Verification ID | `ALC-IV-001` |
| Requirement | Impact Vault allocation is subject to the applicable long-term restriction and is not exposed to an undocumented bypass |
| Source | `allocations.md` §15, §30, §33; `vesting-and-unlocks.md` |
| Expected Observation | Authenticated allocation amount and custody + lock parameters + release capability + upgrade/migration/recovery authority review |
| Evidence | Public On-Chain + code review + authority review |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports technical restriction within the reviewed architecture; does not prove compliant post-release use or impact |

### 21.5 Core Team vesting restriction

| Field | Mapping |
|---|---|
| Verification ID | `ALC-TEAM-001` |
| Requirement | Core Team allocation follows the applicable 19-year linear vesting rule and lacks an undocumented acceleration path |
| Source | `allocations.md` §21, §30, §33; `vesting-and-unlocks.md` |
| Expected Observation | Authenticated allocation + schedule parameters + vested/claimed accounting + executable release capability + upgrade/migration/recovery review |
| Evidence | Public On-Chain + code review + authority review |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports technical vesting behavior within the reviewed architecture; does not prove beneficiary suitability or off-chain governance compliance |

### 21.6 Presale allocation ceiling

| Field | Mapping |
|---|---|
| Verification ID | `ALC-PS-001` |
| Requirement | Presale distribution does not exceed 150,000,000 GFC |
| Source | `allocations.md` §17, §30, §33; `presale.md` |
| Expected Observation | Authenticated Presale allocation, distribution accounting, and relevant transfers or contract state |
| Evidence | Public On-Chain + implementation accounting |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports token-distribution ceiling for the evaluated production implementation; does not prove participant eligibility, refund compliance, or sale legality |

---

# Vesting and Unlock Verification Mapping

## 22. Vesting and Unlock Conformance Mapping

The mappings below define minimum verification intent for [`vesting-and-unlocks.md`](vesting-and-unlocks.md).

### 22.1 Impact Vault 50-year restriction

| Field | Mapping |
|---|---|
| Verification ID | `VEST-IV-001` |
| Requirement | Impact Vault is subject to the applicable 50-year lock |
| Source | `vesting-and-unlocks.md` §§12–17, §56 |
| Expected Observation | Authenticated amount; finalized lock start; deterministic lock end; releasable-state behavior before expiry |
| Evidence | Public On-Chain |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports represented schedule state; does not prove absence of privileged bypass |

### 22.2 Impact Vault no-bypass claim

| Field | Mapping |
|---|---|
| Verification ID | `VEST-IV-002` |
| Requirement | No undocumented administrative, recovery, upgrade, migration, or emergency path may release Impact Vault GFC early |
| Source | `vesting-and-unlocks.md` §§17–21, §§41–44, §56 |
| Expected Observation | Review of executable release paths, rescue/recovery, proxy/upgrade authority, migration capability, and effective privileged control |
| Evidence | Public On-Chain + source/bytecode review + authority review |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports absence of identified bypass paths in the reviewed architecture; does not prove future operational compliance with authorized processes |

### 22.3 Core Team linear vesting

| Field | Mapping |
|---|---|
| Verification ID | `VEST-TEAM-001` |
| Requirement | Aggregate Core Team entitlement accrues linearly over the finalized 19-year period |
| Source | `vesting-and-unlocks.md` §§23–30, §51, §56 |
| Expected Observation | Finalized schedule parameters; deterministic vested-amount calculation; beneficiary accounting; current vested and claimed state |
| Evidence | Public On-Chain + implementation test vectors |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports technical schedule behavior at evaluated timestamps; does not prove absence of bypass |

### 22.4 Claimed amount does not exceed vested amount

| Field | Mapping |
|---|---|
| Verification ID | `VEST-TEAM-002` |
| Requirement | `claimed GFC ≤ vested GFC` and aggregate entitlement remains within 50,000,000 GFC |
| Source | `vesting-and-unlocks.md` §§29–30, §51 |
| Expected Observation | Authenticated vested and claimed accounting at the reference block plus invariant testing |
| Evidence | Public On-Chain + test evidence |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports accounting invariant in the evaluated implementation and test scope; does not prove beneficiary legitimacy |

### 22.5 Migration preservation

| Field | Mapping |
|---|---|
| Verification ID | `VEST-MIG-001` |
| Requirement | Migration preserves remaining restriction and does not duplicate entitlement |
| Source | `vesting-and-unlocks.md` §§19, 36, 43, 51, 56 |
| Expected Observation | Source state before migration; migration transaction; destination state; preserved schedule/restriction; source deactivation or accounting reconciliation |
| Evidence | Public On-Chain + code review + deployment records |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports technical preservation for the reviewed migration; does not independently prove governance authorization |

---

# Governance Verification Mapping

## 23. Governance Conformance Mapping

The mappings below define minimum verification intent for [`governance-constraints.md`](governance-constraints.md).

### 23.1 Authority registry against technical control

| Field | Mapping |
|---|---|
| Verification ID | `GOV-AUTH-001` |
| Requirement | All material production authority is documented and privileged technical roles are represented in the authority registry |
| Source | `governance-constraints.md` §§6, 8–10, §46 |
| Expected Observation | Compare authenticated contract/wallet/backend authority with the published authority registry |
| Evidence | Public On-Chain + deployment/operational records + authority review |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports correspondence between identified technical authority and the registry; does not prove no unknown off-chain authority exists outside the review scope |

### 23.2 Multisig owner set and threshold

| Field | Mapping |
|---|---|
| Verification ID | `GOV-MSIG-001` |
| Requirement | Production multisig owner set and approval threshold match the applicable authenticated governance record |
| Source | `governance-constraints.md` §12, §46 |
| Expected Observation | Implementation-specific authenticated owner-set and threshold state |
| Evidence | Public On-Chain |
| Production Binding | Unbound until the production multisig platform and interface are finalized |
| Evidence Ceiling | Supports configured owner set and threshold; does not prove signer independence |

No generic function name such as `getOwners()` or `getThreshold()` is normative in this Draft.

The production binding MUST use the actual authenticated multisig interface or storage model.

### 23.3 Signer independence

| Field | Mapping |
|---|---|
| Verification ID | `GOV-MSIG-002` |
| Requirement | Signer independence claims must match actual operational independence |
| Source | `governance-constraints.md` §12.3 |
| Expected Observation | Organizational/control evidence concerning signer ownership, shared devices, recovery, entity control, and operational dependence |
| Evidence | Protected Off-Chain and/or independently reviewed records |
| Production Binding | Not directly observable through signer addresses alone |
| Evidence Ceiling | Supports only the reviewed independence factors; distinct on-chain addresses alone are insufficient |

### 23.4 Timelock configuration

| Field | Mapping |
|---|---|
| Verification ID | `GOV-TIME-001` |
| Requirement | Applicable material governance actions use the finalized timelock rules |
| Source | `governance-constraints.md` §13, §46 |
| Expected Observation | Authenticated timelock contract/configuration, role assignment, minimum delay, and execution history where applicable |
| Evidence | Public On-Chain + code/authority review |
| Production Binding | Unbound until final governance architecture exists |
| Evidence Ceiling | Supports configured technical delay for bound actions; does not prove all material actions are routed through the timelock unless authority-path review confirms it |

### 23.5 Upgrade authority

| Field | Mapping |
|---|---|
| Verification ID | `GOV-UPG-001` |
| Requirement | Upgrade authority and execution process are explicit and do not create undisclosed control |
| Source | `governance-constraints.md` §§19–20, §46 |
| Expected Observation | Proxy/implementation relationship; admin/executor; timelock; role holders; upgrade history |
| Evidence | Public On-Chain + code review + authority records |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports identified technical upgrade surface; does not prove future governance decisions will be compliant |

### 23.6 Pause and emergency authority

| Field | Mapping |
|---|---|
| Verification ID | `GOV-EMG-001` |
| Requirement | Pause and emergency powers remain within the applicable defined scope |
| Source | `governance-constraints.md` §§21–22, §46 |
| Expected Observation | Technical pause/emergency capability + role holders + execution limitations + incident records where used |
| Evidence | Public On-Chain + code review + governance records |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports technical capability and recorded use; does not independently prove necessity or proportionality of an emergency decision |

### 23.7 Fixed-supply and long-term commitment protection

| Field | Mapping |
|---|---|
| Verification ID | `GOV-PROT-001` |
| Requirement | Governance cannot silently weaken fixed supply, Impact Vault restrictions, or Core Team vesting |
| Source | `governance-constraints.md` §§24–26, §46 |
| Expected Observation | Cross-component review of token, vault, vesting, upgrade, migration, emergency, and governance authority paths |
| Evidence | Public On-Chain + code review + authority review |
| Production Binding | Specification Only |
| Evidence Ceiling | Supports absence of identified governance bypass paths in the reviewed architecture |

---

# Presale Verification Boundary

## 24. Presale Conformance Mapping

The presale remains a Draft design and no production presale is live.

This document therefore does not bind production presale reads, events, escrow calls, custody functions, or finalization interfaces.

The final mapping MUST be derived from the applicable released [`presale.md`](presale.md) and authenticated production implementation.

### 24.1 Participant accounting and allocation ceiling

A future production mapping SHOULD verify, where applicable:

- authenticated contribution records;
- accepted-asset accounting;
- participant GFC distribution;
- aggregate distributed GFC;
- remaining Presale allocation;
- finalization state;
- refund eligibility;
- refunds paid;
- contribution custody;
- withdrawal conditions;
- and unsold-token treatment.

### 24.2 No assumed escrow architecture

This specification does not require or assume a specific escrow contract merely because a conformance check may need to evaluate contribution custody.

The production binding MUST reflect the custody architecture actually finalized by the applicable presale specification.

### 24.3 Immediate distribution and failed finalization

The current specification set identifies the treatment of already distributed GFC after failed finalization as unresolved.

Until that interaction is normatively and technically resolved:

- no production presale may be represented as ready on the basis of this verification document;
- no checker output may imply that the unresolved participant-rights interaction has been verified;
- and no clawback, forced transfer, burn, return, invalidation, or replacement mechanism may be inferred.

---

# Transparency and Evidence Verification Boundary

## 25. Transparency Conformance Mapping

The transparency model contains requirements that cannot all be reduced to on-chain reads.

### 25.1 Public transaction claims

An authenticated transaction, receipt, balance, or contract state MAY support a transaction-level claim.

The evidence ceiling remains transaction verification.

### 25.2 Use-of-funds claims

Use-of-funds claims generally require evidence beyond the transfer itself.

A transaction MAY establish that funds moved to an address.

It does not independently establish what the recipient actually used the funds for.

### 25.3 Output, outcome, and impact claims

Output, outcome, and impact claims may require:

- operational records;
- measurement data;
- methodology;
- independent review;
- protected evidence;
- or other non-chain evidence.

A read-only on-chain checker MUST NOT upgrade a transaction-level observation into outcome or impact verification.

### 25.4 Cryptographic anchors

A content hash or equivalent commitment MAY establish:

- correspondence to a specific record;
- integrity;
- version;
- or timing.

It MUST NOT be described as establishing factual truth.

### 25.5 Protected evidence

Where the applicable evidence is legitimately protected, a public checker MAY report that protected evidence is required.

It MUST NOT infer failure merely because protected evidence is not publicly exposed.

---

## 26. Machine-Readable Verification Results

A future automated checker MAY expose machine-readable result categories.

If implemented, the following categories are RECOMMENDED.

### `verified_on_chain`

All evidence required for the specific mapped claim is available through authenticated public on-chain observations and the observation satisfies the expected condition.

This result applies only to the specific mapped claim.

It MUST NOT be interpreted as full-system conformance.

### `anchored_only`

The available public evidence establishes a cryptographic commitment or record linkage, but not the factual truth of the underlying content.

### `requires_protected_evidence`

The claim depends materially on evidence that should not be exposed publicly.

### `mixed_evidence_required`

On-chain evidence exists, but the full mapped claim also requires code review, authority review, protected evidence, or another evidence source.

### `not_currently_verifiable`

The required authenticated implementation binding or evidence source does not exist, is unresolved, or is unavailable.

### `not_evaluated`

A binding exists but no evaluation result is being asserted.

### `not_applicable`

The mapped requirement does not apply to the evaluated implementation or environment and the reason is recorded.

These result categories MUST remain distinct from:

- `Audited`;
- `Independently Verified`;
- `Conforming`;
- `Production`;
- and other repository status terms.

---

## 27. Result Record

An actual verification result SHOULD identify:

- verification ID;
- evaluated claim;
- source specification and version;
- implementation binding version;
- network and chain ID;
- authenticated address set;
- reference block or range;
- observation time;
- observation method;
- observed value;
- expected condition;
- result category;
- evidence references;
- required corroboration;
- evidence ceiling;
- known limitations;
- verifier or tool version where appropriate;
- and result hash or durable identifier where appropriate.

A result without a reference block or equivalent temporal context SHOULD NOT be used for state that can change.

---

## 28. Read-Only Conformance Checker

A read-only conformance checker MAY be developed as a reference implementation.

It is not represented as existing or production-ready by this Draft.

### 28.1 Permitted function

A checker MAY:

- load an authenticated verification mapping;
- authenticate the intended chain;
- authenticate bound addresses;
- perform read-only calls;
- inspect public logs and transactions;
- compare observed values with defined conditions;
- report unavailable evidence;
- and produce claim-specific result records.

### 28.2 Prohibited function

A checker MUST NOT:

- sign transactions;
- modify contract state;
- act as governance authority;
- assign independent-verification status without the required process;
- infer signer independence from distinct addresses;
- infer compliant use of funds from a transfer;
- infer factual truth from a content hash;
- infer impact from transaction evidence;
- or claim full conformance from a subset of successful checks.

### 28.3 Chain safety

A checker MUST fail closed where:

- chain ID does not match the binding;
- contract authentication fails;
- proxy implementation cannot be resolved where required;
- the binding is stale for the evaluated deployment;
- or a required evidence source is unavailable.

### 28.4 Version safety

A checker result MUST identify the:

- specification version;
- mapping version;
- implementation binding version;
- and checker version.

A result from one version MUST NOT silently be reused for another materially different implementation.

---

## 29. Verification of Absence

Some conformance statements use negative wording such as:

- no mint path;
- no early-release path;
- no administrative override;
- no undisclosed fee exemption;
- no unauthorized migration.

These statements require special care.

A verification method for absence SHOULD combine, where relevant:

1. authenticated code review;
2. effective authority review;
3. proxy and upgrade review;
4. migration-path review;
5. transaction-history review;
6. and explicit scope disclosure.

A scanner that fails to find a prohibited event is insufficient to prove that the event is technically impossible.

---

## 30. Verification of Upgradeable Systems

Where an implementation is upgradeable, a conformance result MUST identify whether the result concerns:

- current implementation behavior;
- upgrade authority;
- permitted upgrade envelope;
- historical implementation;
- or post-upgrade behavior.

A current implementation MAY satisfy a requirement while the effective governance architecture retains authority to replace it with non-conforming behavior.

Where that possibility conflicts with the source requirement, the system MUST NOT be described as fully conforming merely because the current implementation passes state checks.

---

## 31. Verification of Migrations

A migration verification SHOULD compare:

- source implementation;
- destination implementation;
- pre-migration state;
- migration transaction;
- post-migration state;
- remaining restrictions;
- authority;
- supply reconciliation;
- duplicate-entitlement risk;
- and applicable specification version.

A destination contract MUST NOT be treated as preserving a restriction merely because it receives the same token amount.

The effective rules and authority must also be evaluated.

---

## 32. Verification of Public Claims

Where GFC makes a public technical claim that is intended to be verifiable, the claim SHOULD be traceable to:

- a verification ID;
- authenticated evidence;
- an applicable result record;
- and the evidence ceiling.

Public communication MUST NOT remove a material limitation present in the verification record.

For example:

> `verified_on_chain`

for a current balance MUST NOT be rewritten publicly as:

> "independently verified use of funds."

---

## 33. Changes to Verification Mappings

A verification mapping MUST be updated when a material change affects:

- the source requirement;
- implementation architecture;
- contract interface;
- event model;
- storage model;
- proxy structure;
- authority model;
- deployment;
- migration;
- evidence class;
- or evidence ceiling.

A mapping change MUST NOT retroactively alter a historical result without preserving the prior mapping and result context.

Where a mapping error is discovered:

- the error SHOULD be documented;
- affected results SHOULD be identified;
- corrected mappings SHOULD receive a new version or revision;
- and material public claims SHOULD be corrected where necessary.

---

## 34. Pilot Verification

The Base Sepolia pilot MAY be used to:

- test mapping structure;
- validate checker logic;
- test read-only integrations;
- demonstrate result formats;
- and identify missing observability.

Pilot verification SHOULD clearly identify:

```text
Environment: Base Sepolia pilot
Chain ID: 84532
Production authority: none
```

A pilot result MUST NOT be relabeled as production evidence after the fact.

If a production implementation later reuses code from the pilot, production bindings still require independent authentication.

---

## 35. Production Verification Requirements

Before a material production conformance claim is made, the applicable verification process MUST identify:

- versioned source specification;
- authenticated production deployment;
- authenticated addresses;
- implementation-specific bindings;
- applicable code or bytecode identity;
- effective authority;
- reference block or historical range;
- required off-chain evidence where applicable;
- evidence ceiling;
- known deviations;
- and verification result.

Where one of these elements is required but unavailable, the result MUST identify the limitation.

---

## 36. Conformance

A verification implementation or process conforms to this specification only when:

- it identifies the specific requirement being evaluated;
- it identifies the applicable specification version;
- it authenticates the evaluated implementation where implementation-specific evidence is used;
- it identifies the correct environment and chain ID;
- it uses the applicable verification mapping;
- it uses the applicable implementation-specific binding;
- it records the relevant block, range, transaction, timestamp, or record version;
- it distinguishes current state from historical state;
- it distinguishes state from capability;
- it distinguishes technical authority from organizational independence;
- it identifies the evidence class;
- it respects the evidence ceiling;
- it does not infer production status from pilot evidence;
- it does not infer factual truth from cryptographic anchoring;
- it does not infer use, outcome, or impact from transaction evidence alone;
- it represents missing bindings and unavailable evidence explicitly;
- and it preserves material limitations and deviations.

A successful verification result for one requirement does not establish complete conformance of the component or system.

---

## 37. Verification Non-Conformance

Verification non-conformance includes:

- using an unauthenticated contract as the production source;
- evaluating the wrong chain;
- using Base Sepolia evidence for a Base Mainnet production claim;
- inventing an implementation-specific production interface;
- omitting a material proxy or upgrade path;
- treating current state as complete historical proof;
- treating absence of an observed event as proof of technical impossibility without sufficient scope;
- treating distinct multisig addresses as proof of signer independence;
- treating a content hash as proof of factual truth;
- treating a transfer as proof of compliant use;
- treating outcome evidence as impact evidence without the required methodology;
- omitting the evidence ceiling;
- omitting required corroboration;
- claiming full conformance from a partial check;
- or silently reusing a stale binding after a material deployment change.

Material verification non-conformance MAY require:

- withdrawal of the result;
- corrected mapping;
- corrected binding;
- re-evaluation;
- public correction;
- security review;
- governance review;
- or incident treatment.

---

## 38. Current Unresolved Requirements

The following matters remain unresolved unless separately established by later versioned specifications or authenticated implementation records:

- production token contract and binding;
- production allocation addresses and initialization reference;
- Impact Vault implementation and verification interface;
- Core Team vesting implementation and verification interface;
- production governance architecture;
- production multisig platform and interface;
- production timelock architecture;
- proxy and upgrade architecture;
- production authority registry format;
- production presale architecture;
- presale custody and finalization bindings;
- treatment of distributed GFC after failed presale finalization;
- production staking implementation;
- complete Transparency Registry implementation;
- protected-evidence review process;
- final machine-readable mapping schema;
- final durable result format;
- checker implementation;
- checker release/authentication process;
- binding-signing or authentication format;
- and long-term archival of verification results.

These unresolved matters MUST NOT be represented as completed production verification infrastructure.

---

## 39. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- verification-record fields are finalized;
- evidence classes are aligned with the released transparency model;
- evidence-ceiling rules are finalized;
- verification-availability terminology is finalized;
- machine-readable result categories are finalized or explicitly excluded;
- environment-binding requirements are finalized;
- implementation-binding requirements are finalized;
- production authentication requirements are finalized;
- historical-state verification requirements are finalized;
- negative-observation requirements are finalized;
- proxy and upgrade verification requirements are finalized;
- authority verification requirements are finalized;
- signer-independence boundaries are finalized;
- token verification mappings are complete;
- allocation verification mappings are complete;
- vesting and unlock verification mappings are complete;
- governance verification mappings are complete;
- presale verification mappings are complete after the presale design is technically resolved;
- transparency and evidence verification boundaries are aligned with the applicable released model;
- all required production bindings are defined for the first production candidate;
- deployment records identify the applicable mapping and binding versions;
- security review has evaluated checker and mapping failure modes where a checker is used;
- Base Sepolia pilot and Base Mainnet production verification remain consistently separated;
- related specifications are mutually consistent;
- and the versioned specification release process is ready.

---

## 40. Related Specifications

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
- [`transparency-model.md`](transparency-model.md);
- and repository-level [`../STATUS.md`](../STATUS.md).

Where another Draft specification conflicts with this document, the conflict MUST be resolved explicitly before Stable status.

The source domain specification governs the underlying normative requirement.

This document governs only the verification mapping, evidence interpretation, and verification-result constraints unless the source specification explicitly states otherwise.

---

## 41. Final Conformance Verification Principles

The GFC conformance-verification model preserves the following distinctions:

> A requirement is not an observation.

> An observation is not automatically proof of the full requirement.

> Current state is not complete history.

> Current state is not future capability.

> Code capability is not operational compliance.

> A distinct signer address is not proof of signer independence.

> A multisig threshold is not proof of decentralization.

> A balance is not proof of initial allocation after later movement.

> A lock-state read is not proof that no privileged bypass exists.

> A transaction is not proof of compliant use.

> A content hash is not proof of factual truth.

> An anchored record is not automatically independently verified.

> Outcome verification is not automatically impact verification.

> Pilot verification is not production verification.

> Base Sepolia is not Base Mainnet.

> A successful claim-specific check is not full-system conformance.

> A production binding must be authenticated, not inferred.

> Missing evidence must remain visible.

> Evidence must never be interpreted beyond its ceiling.

The purpose of the verification layer is to make GFC claims reconstructable without creating false certainty.

A credible conformance system must state not only **what was observed**, but also **what that observation can and cannot prove**.

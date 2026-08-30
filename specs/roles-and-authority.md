# GFC Roles and Authority Specification

**Document ID:** GFC-RA-001  
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

This document defines the intended role model and authority boundaries for Global Foundation Coin (GFC).

It is normative because it defines how material authority MUST be identified, limited, separated, authenticated, reviewed, changed, and disclosed.

Its maturity remains Draft.

At the current repository state:

- no production GFC token is deployed on Base Mainnet;
- no GFC presale is live;
- no production governance infrastructure is active;
- no production treasury infrastructure is active;
- no production staking infrastructure is operational;
- no production multisig or signer set is authenticated as official by this document;
- no production wallet or contract address is assigned authority by this document;
- no natural person, organization, wallet, multisig, or contract becomes a production authority merely because it is named in a Draft document;
- and no role definition in this specification proves that the corresponding role has been implemented or assigned.

A public GFC pilot exists on Base Sepolia.

Pilot authority and production authority MUST remain distinct.

Any authority associated with the Base Sepolia pilot applies only to the authenticated pilot deployment and MUST NOT be interpreted as authority over a future Base Mainnet production system.

Current implementation and deployment status is maintained in [`../STATUS.md`](../STATUS.md).

---

## 2. Purpose

The purpose of this specification is to make material GFC authority explicit before production reliance.

The specification defines:

- what constitutes authority;
- how roles are defined;
- how authority is assigned;
- how authority is limited;
- which powers require stronger controls;
- how duties should be separated;
- how signer and multisig authority must be represented;
- how emergency authority is bounded;
- how role changes are recorded;
- how production authority is authenticated;
- how pilot authority is separated from production authority;
- and how authority relates to accountability.

This document does not assign production roles to specific people, wallets, contracts, multisigs, or organizations.

Those assignments require authenticated deployment and operational records.

---

## 3. Relationship to the GFC Accountability Model

The long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

This document primarily defines the **Authority** element and its relationship to the surrounding stages.

For a material GFC action, it SHOULD be possible to reconstruct:

1. what funds, assets, records, contracts, or rights were affected;
2. which role had authority to act;
3. which rules constrained that authority;
4. which decision authorized the action;
5. what execution and outcome followed;
6. and what evidence supports the record.

Authority without identifiable rules is insufficient.

A decision without attributable authority is insufficient.

A transaction without an authority record does not by itself establish that the transaction was properly authorized.

---

## 4. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are normative only when:

- they appear in uppercase;
- the containing document declares `Authority: Normative`;
- and the applicable version governs the implementation, process, or communication being evaluated.

Because this document is Draft, its requirements may change before the first versioned production-governing release.

---

## 5. Core Definitions

Terminology in this document is interpreted according to [`glossary.md`](glossary.md).

The following concepts are foundational.

### 5.1 Authority

Authority is the ability of a person, role, wallet, multisig, contract, entity, or defined process to cause, approve, block, modify, or execute a material action.

### 5.2 Role

A role is a defined set of permissions, responsibilities, constraints, and accountability obligations.

A role name does not itself create technical authority.

### 5.3 Role Holder

A role holder is the authenticated person, entity, wallet, multisig, contract, or other mechanism currently assigned to a defined role.

### 5.4 Authority Surface

The authority surface is the complete set of material actions a role or role holder can perform.

### 5.5 Material Authority

Authority is material where misuse or compromise could materially affect:

- token supply;
- token transfers;
- fees;
- allocations;
- vesting or locks;
- presale participants or funds;
- treasury assets;
- liquidity;
- staking;
- governance execution;
- contract upgrades;
- pauses;
- migrations;
- official deployment records;
- transparency records;
- evidence status;
- participant rights;
- or production availability.

### 5.6 Technical Authority

Authority enforced or enabled directly by code, keys, roles, contract ownership, multisig control, or another technical mechanism.

### 5.7 Operational Authority

Authority exercised through off-chain procedures, operational access, hosting, publication, review, accounting, evidence handling, or other non-contract processes.

### 5.8 Advisory Authority

A role that may recommend, discuss, review, or propose actions but cannot independently approve or execute them.

Advisory authority MUST NOT be represented as binding authority.

### 5.9 Binding Authority

Authority whose valid exercise can directly approve, block, or cause a material action.

---

## 6. Foundational Authority Principles

### 6.1 Explicit authority

All material authority MUST be explicit.

Material authority MUST NOT exist solely through:

- retained private keys;
- undocumented ownership;
- informal team practice;
- hidden backend access;
- unrecorded signer control;
- frontend-only assumptions;
- unpublished operational convention;
- or unclear contract administration.

### 6.2 Least privilege

Each role MUST receive only the minimum authority required for its documented function.

A role MUST NOT receive unrelated authority merely for convenience.

### 6.3 Responsibility follows authority

A role exercising material authority MUST have identifiable accountability obligations.

Greater authority requires greater:

- disclosure;
- control;
- reviewability;
- security;
- and change discipline.

### 6.4 Separation of duties

Where reasonably possible, GFC SHOULD separate:

- proposal;
- review;
- approval;
- execution;
- custody;
- verification;
- evidence submission;
- evidence review;
- accounting reconciliation;
- and public reporting.

Where separation is not yet operationally feasible, concentration of authority MUST be disclosed and treated as an explicit trust assumption.

### 6.5 No authority by label

A wallet or contract label such as:

- `Treasury`;
- `Impact Vault`;
- `Guardian`;
- `Governance`;
- `Liquidity`;
- or `Foundation`

does not technically restrict the holder's powers.

Authority is determined by actual technical and operational control.

### 6.6 No authority by token ownership alone

GFC token ownership MUST NOT automatically create unrestricted authority over:

- treasury assets;
- Impact Vault assets;
- liquidity reserves;
- privileged contract roles;
- production deployments;
- protected evidence;
- legal or regulatory decisions;
- emergency response;
- or impact determinations.

### 6.7 No authority by historical status

A former founder role, signer role, reviewer role, partner role, contractor role, or governance role does not create continuing authority after the role has been revoked or superseded.

---

## 7. Role Definition Requirements

Every material production role MUST define:

- role name;
- purpose;
- authority scope;
- affected components;
- permitted actions;
- prohibited actions;
- technical enforcement;
- approval requirements;
- execution requirements;
- timelock requirements where applicable;
- emergency exceptions where applicable;
- appointment process;
- replacement process;
- revocation process;
- recovery process;
- conflict-of-interest requirements;
- logging or record requirements;
- public disclosure level;
- and current role holder.

A role definition MUST distinguish between:

- what the role is intended to do;
- what the role is technically capable of doing;
- and what the role is prohibited from doing.

If technical capability exceeds intended authority, that difference MUST be disclosed as a trust or security risk.

---

## 8. Role Assignment and Authentication

### 8.1 Definition is not assignment

Defining a role in a specification does not assign the role.

### 8.2 Assignment requirements

A production role assignment MUST be authenticated through an applicable production record identifying, where relevant:

- role;
- address or contract;
- network;
- effective date or block;
- assignment transaction;
- approval record;
- applicable specification version;
- source-code or deployment reference;
- and revocation or replacement status.

### 8.3 Official production authority

No wallet, multisig, contract, person, or organization MUST be treated as an official production authority solely because it appears in:

- a Draft specification;
- a README;
- a website;
- a social-media post;
- a screenshot;
- an old deployment;
- a testnet deployment;
- or an unauthenticated third-party source.

### 8.4 Pilot authority

Authority associated with the public Base Sepolia pilot MUST be identified as pilot authority.

Pilot role holders MUST NOT be assumed to hold corresponding Base Mainnet production authority.

---

## 9. Authority Registry

A future production system MUST maintain an authenticated authority record for all material roles.

The authority registry SHOULD identify:

| Field | Required Meaning |
|---|---|
| Role | Canonical role name |
| Environment | Pilot, testnet, production, or other |
| Network | Network and chain ID where applicable |
| Holder | Authenticated address, contract, multisig, entity, or role holder |
| Scope | Components and actions controlled |
| Approval model | Required approvals or threshold |
| Timelock | Applicable execution delay |
| Upgrade authority | Whether upgrade power exists |
| Pause authority | Whether pause power exists |
| Migration authority | Whether migration power exists |
| Effective status | Proposed, active, revoked, superseded, or other |
| Effective date | Date, block, or transaction |
| Evidence | Assignment and authentication record |

The authority registry MUST preserve material historical changes.

A replaced role holder MUST NOT silently disappear from the record.

---

## 10. Authority Categories

The architecture recognizes the following material authority categories.

Not every category MUST become a separate production role.

Where one role holds several categories, the concentration MUST be explicit.

### 10.1 Deployment Authority

Authority to deploy production contracts or initialize production components.

### 10.2 Upgrade Authority

Authority to replace or materially modify deployed contract behavior.

### 10.3 Pause Authority

Authority to temporarily restrict defined system functions.

### 10.4 Migration Authority

Authority to move assets, users, records, or system functions to a successor implementation.

### 10.5 Token Authority

Authority affecting token-level configuration or behavior.

### 10.6 Allocation Authority

Authority affecting custody, release, or movement of allocated GFC.

### 10.7 Treasury Authority

Authority affecting treasury assets or treasury-controlled transactions.

### 10.8 Liquidity Authority

Authority affecting liquidity deployment, withdrawal, rebalancing, or related positions.

### 10.9 Presale Authority

Authority affecting permitted presale operations.

### 10.10 Staking Authority

Authority affecting staking configuration, reward distribution, or emergency operation.

### 10.11 Governance Authority

Authority to create, approve, veto, execute, or otherwise control governance decisions.

### 10.12 Security Authority

Authority to take defined actions in response to security incidents.

### 10.13 Evidence Authority

Authority affecting evidence submission, custody, review, classification, or status.

### 10.14 Transparency Registry Authority

Authority affecting publication, correction, status, or lifecycle of Transparency Registry records.

### 10.15 Publication Authority

Authority to authenticate official technical records, deployment information, or public status statements.

---

## 11. Deployment Authority

A production Deployment Authority MAY exist to perform defined deployment actions.

Its authority MUST be limited to the applicable deployment process.

Where temporary deployment privileges exist, they MUST be:

- documented;
- minimized;
- transferred, revoked, or renounced as intended after deployment;
- and reflected in deployment records.

The deployer MUST NOT retain undocumented production control merely because it created the contracts.

Deployment authority MUST NOT automatically imply:

- upgrade authority;
- treasury authority;
- presale authority;
- staking authority;
- governance authority;
- or custody authority.

---

## 12. Token Authority

The intended GFC production token has a fixed supply of:

**1,000,000,000 GFC**

Token-level authority MUST NOT permit undocumented discretionary inflation.

Any production token role capable of affecting:

- fees;
- fee exemptions;
- recognized liquidity pools;
- transfer restrictions;
- pausing;
- contract configuration;
- or migration

MUST be explicitly defined in [`token.md`](token.md) and reflected in the production authority registry.

No role MAY silently obtain authority to:

- confiscate balances;
- arbitrarily move user tokens;
- create additional supply beyond the applicable fixed-supply rules;
- or introduce undisclosed transfer restrictions.

---

## 13. Allocation Authority

The intended fixed allocation model is defined in [`allocations.md`](allocations.md).

Authority over allocations MUST remain distinguishable by allocation purpose.

Material allocation authority SHOULD NOT be combined into one unrestricted custody role merely for convenience.

At minimum, production records MUST distinguish authority affecting:

- Impact Vault;
- Guardian Growth;
- Presale;
- Treasury Reserve;
- Liquidity Reserve;
- Ecosystem;
- and Core Team.

An allocation role MUST NOT treat allocation ownership as unrestricted beneficial ownership.

Movement of allocated tokens MUST remain subject to the applicable:

- lock;
- vesting;
- custody;
- governance;
- approval;
- and disclosure requirements.

---

## 14. Impact Vault Authority

The intended Impact Vault allocation is subject to a long-term lock design.

No authority associated with the Impact Vault MAY provide an undocumented path to:

- accelerate release;
- shorten the remaining lock;
- withdraw locked assets;
- replace the lock with a weaker structure;
- or migrate assets into a less restrictive system.

Where a migration role exists, the migration MUST preserve or strengthen the remaining restriction.

The existence of an administrative or migration capability MUST NOT make the Impact Vault appear technically immutable if it is not.

---

## 15. Core Team Vesting Authority

The intended Core Team allocation is subject to long-term linear vesting.

Any role affecting Core Team vesting MUST NOT possess undocumented authority to:

- accelerate vesting;
- shorten the vesting period;
- withdraw unvested tokens;
- reassign tokens contrary to the applicable rules;
- or migrate the allocation into a weaker vesting structure.

Beneficiary authority and vesting-administration authority SHOULD remain distinct where technically and operationally appropriate.

Exact beneficiary, succession, reassignment, and revocation rules belong in [`vesting-and-unlocks.md`](vesting-and-unlocks.md).

---

## 16. Treasury Roles

Future production treasury governance MAY distinguish among the following functional roles.

### 16.1 Treasury Proposer

May submit a documented treasury action for review.

Proposal authority does not equal approval authority.

### 16.2 Treasury Approver

May approve or reject treasury actions under defined rules.

### 16.3 Treasury Executor

May technically execute an approved treasury action.

Execution authority MUST NOT be used to bypass required approvals.

### 16.4 Treasury Custodian or Signer

May participate in the technical custody or signing process.

A signer does not automatically possess unilateral beneficial ownership of treasury assets.

### 16.5 Treasury Reviewer

May review proposals, reconciliations, related-party issues, or evidence.

Review authority does not automatically create execution authority.

The final production treasury model MAY combine or further divide these functions.

Any concentration MUST be disclosed.

---

## 17. Liquidity Authority

Liquidity authority MAY include power to:

- deploy liquidity;
- withdraw liquidity;
- rebalance positions;
- change supported venues;
- manage liquidity-provider positions;
- or execute market-making arrangements.

Such authority MUST be explicitly defined before production use.

Liquidity authority MUST NOT be represented as permanently locked if an authorized role can remove or redirect the position.

Any role capable of material liquidity withdrawal MUST be disclosed.

Liquidity authority MUST NOT be used for undisclosed market manipulation.

---

## 18. Presale Authority

No GFC presale is currently live.

The current presale design remains Draft.

The intended production presale is designed around:

- a reference price of €0.05 per GFC;
- an intended duration of eight weeks;
- a €250,000 soft cap;
- no separate monetary hard cap;
- a maximum Presale Allocation of 150,000,000 GFC;
- intended support for ETH, USDC, and DAI on Base;
- immediate token distribution as the current design direction;
- refund rights if the applicable soft-cap success condition is not satisfied;
- and immutable material sale logic as the current design direction.

A future Presale Authority MUST NOT be able to silently change material participant-facing rules after production activation.

At minimum, no authority MAY silently alter:

- price;
- sale duration;
- soft cap;
- Presale Allocation;
- participant accounting;
- supported payment assets;
- refund rights;
- distribution rules;
- or withdrawal conditions.

If any administrative presale authority remains necessary, its scope MUST be narrowly defined in [`presale.md`](presale.md).

The unresolved technical relationship between immediate token distribution and failed-sale refunds MUST be resolved in the presale specification before Stable status.

This document does not invent a return, clawback, burn, cancellation, or replacement mechanism for that unresolved case.

---

## 19. Staking Authority

No production GFC staking system is currently operational.

The current intended design direction is hybrid and non-inflationary.

A future Staking Authority MAY control only those parameters explicitly defined in [`staking.md`](staking.md).

Staking authority MUST NOT permit:

- minting beyond the fixed supply;
- undocumented reward creation;
- confiscation of participant balances;
- arbitrary modification of earned rewards;
- unrestricted treasury withdrawal;
- or automatic acquisition of unrelated governance authority.

Where reward parameters are configurable, permitted ranges and change authority MUST be technically and normatively bounded.

---

## 20. Governance Roles

Governance MAY include distinct roles for:

- proposal;
- review;
- voting or consultation;
- approval;
- veto;
- execution;
- and emergency response.

Governance participation MUST NOT be represented as binding authority unless it actually has binding effect.

A token holder, staker, community participant, expert reviewer, signer, or advisor MUST NOT be described as possessing more authority than the applicable mechanism grants.

The detailed constraints on governance authority are defined in [`governance-constraints.md`](governance-constraints.md).

---

## 21. Multisig and Signer Authority

### 21.1 Multisig use

Material production assets and privileged authority SHOULD use control structures appropriate to their risk.

Where a multisig is used, its configuration MUST identify:

- signer count;
- approval threshold;
- signer categories;
- signer replacement process;
- recovery process;
- transaction review expectations;
- emergency procedures;
- and applicable timelocks.

### 21.2 No automatic decentralization claim

A multisig does not automatically create decentralization or independence.

The following remain relevant:

- common beneficial control;
- organizational dependence;
- device or key concentration;
- economic dependence;
- coercion risk;
- signer coordination;
- and threshold design.

### 21.3 Signer responsibilities

A signer SHOULD review, as applicable:

- destination;
- amount;
- calldata;
- contract;
- network;
- expected effects;
- supporting approval;
- and known simulation results

before approving a material transaction.

### 21.4 Signer replacement

Signer replacement MUST be documented and historically reviewable.

A removed signer MUST lose the relevant technical authority.

An outdated public signer record MUST be corrected without erasing historical status.

---

## 22. Upgrade Authority

Where a production component is upgradeable, Upgrade Authority is among the highest-risk authority categories.

An upgrade process MUST identify:

- who may propose an upgrade;
- who may review it;
- who may approve it;
- who may execute it;
- required threshold;
- applicable timelock;
- emergency exceptions;
- public disclosure requirements;
- and post-upgrade verification.

Upgrade Authority MUST NOT silently introduce:

- additional minting authority;
- weaker allocation locks;
- accelerated vesting;
- higher fees beyond permitted bounds;
- balance confiscation;
- unrestricted transfer blocking;
- reduced refund rights;
- broader treasury authority;
- or weaker approval thresholds.

Where a component is represented as immutable, no undisclosed Upgrade Authority may exist.

---

## 23. Pause Authority

Pause Authority MAY exist only where justified by the applicable component specification.

A pause mechanism MUST define:

- functions affected;
- functions unaffected;
- authorized role;
- approval requirements;
- activation conditions;
- unpause process;
- record requirements;
- and participant implications.

Pause Authority MUST NOT become an undocumented mechanism to:

- seize funds;
- permanently deny participant rights;
- redirect allocations;
- eliminate refund rights;
- or bypass normal governance.

A pause MUST NOT be represented as a cure for a vulnerability unless the underlying issue is actually remediated.

---

## 24. Emergency Authority

Emergency Authority MUST be narrow, predefined, and reviewable.

It MAY exist for defined conditions such as:

- active exploitation;
- critical contract vulnerability;
- key compromise;
- severe dependency failure;
- or another explicitly defined emergency.

Emergency Authority MUST NOT provide unrestricted standing power.

Emergency action MUST NOT silently:

- increase token supply;
- weaken locks;
- accelerate vesting;
- confiscate balances;
- redirect refundable participant assets;
- or permanently change governance rules.

Where emergency action bypasses a normal delay or approval step, the exception MUST be explicitly specified.

---

## 25. Migration Authority

Migration Authority MAY exist where replacing a component is necessary.

Migration MUST NOT be used as a disguised bypass of:

- fixed supply;
- lock duration;
- vesting;
- participant rights;
- treasury restrictions;
- allocation restrictions;
- evidence history;
- or governance constraints.

A migration process MUST define:

- triggering conditions;
- approval authority;
- source component;
- successor component;
- transferred assets or records;
- preserved rights;
- preserved restrictions;
- verification process;
- rollback or failure handling where applicable;
- and public status.

---

## 26. Security Roles

A future production security model MAY define functional roles such as:

- security reporter;
- security reviewer;
- incident coordinator;
- emergency proposer;
- pauser;
- remediation approver;
- and disclosure coordinator.

Security roles MUST NOT receive unrelated financial or governance authority merely because rapid response is desirable.

Security-sensitive information MAY be temporarily restricted where disclosure would increase risk.

The existence and status of a material incident SHOULD remain reviewable once disclosure is safe and appropriate.

Detailed security requirements are defined in [`security-model.md`](security-model.md) and repository-level [`../SECURITY.md`](../SECURITY.md).

---

## 27. Evidence Roles

The accountability system MAY distinguish among:

### 27.1 Evidence Submitter

Supplies evidence or supporting records.

Submission does not imply acceptance or verification.

### 27.2 Evidence Custodian

Stores and protects evidence under applicable access, privacy, retention, and integrity rules.

Custody does not imply authority to declare a claim verified.

### 27.3 Evidence Reviewer

Evaluates evidence under a defined scope.

Review authority MUST be distinguishable from evidence submission where possible.

### 27.4 Independent Reviewer

An external reviewer whose relevant independence, scope, methodology, access, conflicts, and limitations are documented.

External status alone does not establish independence.

### 27.5 Claim Status Authority

A role or process capable of assigning or changing a defined claim status.

Any such authority MUST use predefined status rules and preserve history.

A reviewer MUST NOT be represented as independent where GFC materially controls the relevant review outcome.

---

## 28. Transparency Registry Roles

The planned Transparency Registry is intended to operate as a versioned historical record rather than a permanent approval badge.

Potential registry functions MAY include:

- record submission;
- evidence linkage;
- review;
- status assignment;
- correction;
- supersession;
- suspension;
- downgrade;
- or removal from current active presentation while preserving historical traceability.

No complete production Transparency Registry is currently deployed.

Before production use, the applicable transparency specification MUST define which roles may:

- create records;
- edit draft records;
- publish records;
- attach evidence;
- change status;
- correct records;
- supersede records;
- suspend current status;
- or remove a record from current presentation.

Material historical records MUST NOT be silently rewritten or deleted for reputational convenience.

Registry authority MUST NOT be described as independent verification unless the applicable review process is actually independent.

Detailed requirements are defined in [`transparency-model.md`](transparency-model.md).

---

## 29. Publication Authority

Official technical communication MAY require authenticated Publication Authority.

Publication Authority may include responsibility for publishing:

- official production addresses;
- release identifiers;
- deployment records;
- security notices;
- migration notices;
- deprecation notices;
- authority changes;
- or other authenticated technical records.

Publication Authority MUST NOT be confused with technical control over the underlying contracts.

A public statement cannot create technical authority that the system does not grant.

A public statement also cannot remove technical authority that remains active on-chain or operationally.

---

## 30. Portal and Frontend Authority

A future GFC portal or interface MUST NOT possess undisclosed authority over user funds or production governance.

Where a frontend:

- prepares transactions;
- selects contract addresses;
- displays status;
- submits evidence;
- or communicates official records,

its role and trust assumptions MUST be disclosed.

Where user transactions are involved, the user wallet SHOULD remain the signer unless a different model is explicitly documented.

A compromised frontend MUST NOT be treated as changing the applicable specification or legitimate authority structure.

---

## 31. Off-Chain Operational Authority

Material off-chain access MAY include control over:

- domains;
- hosting;
- DNS;
- repositories;
- release publication;
- evidence storage;
- monitoring;
- indexing;
- analytics;
- communications;
- or other operational systems.

Off-chain authority MUST be documented where compromise could materially affect:

- user safety;
- authenticated addresses;
- evidence integrity;
- public status representation;
- or transaction preparation.

Control of a website or social account MUST NOT be treated as equivalent to on-chain authority.

---

## 32. Conflict of Interest

Material role holders MUST disclose or appropriately manage conflicts of interest where those conflicts could affect impartial decision-making.

Conflict-management mechanisms MAY include:

- disclosure;
- recusal;
- independent review;
- threshold changes;
- exclusion from approval;
- or additional oversight.

A conflicted role holder MUST NOT use undisclosed influence to approve a related-party transaction or review their own material conduct as independent.

---

## 33. Related-Party Actions

A material action involving a related party SHOULD receive heightened review.

The record SHOULD identify, where appropriate:

- relationship;
- economic interest;
- decision-makers;
- recusals;
- approval process;
- rationale;
- terms;
- and supporting evidence.

The mere use of a multisig does not resolve a conflict where the approving signers share the same material conflict.

---

## 34. Transitional Concentration of Authority

Early-stage GFC development may require temporary concentration of roles.

Where this occurs, the concentration MUST NOT be hidden behind decentralization language.

A transitional arrangement SHOULD identify:

- which roles are concentrated;
- why separation is not yet feasible;
- associated risks;
- compensating controls;
- intended review;
- and conditions for later separation.

Temporary concentration MUST NOT silently become permanent production authority.

---

## 35. Role Appointment

A material role appointment SHOULD require:

- documented rationale;
- defined scope;
- conflict review;
- security readiness;
- applicable approval;
- effective date;
- and authenticated role assignment.

Where a role controls keys or signing authority, appointment is incomplete until the technical authority matches the documented assignment.

---

## 36. Role Replacement and Revocation

A material role replacement or revocation MUST address both:

- documented authority;
- and actual technical or operational access.

Removing a person's name from documentation is insufficient if:

- their key remains active;
- their signer slot remains valid;
- their administrator role remains assigned;
- their credentials remain usable;
- or their backend access remains available.

Role changes SHOULD be verified after execution.

---

## 37. Role Recovery

Recovery mechanisms MAY exist for loss or compromise of authorized keys.

Recovery MUST NOT create an undocumented master authority.

A recovery process SHOULD define:

- triggering conditions;
- approvers;
- replacement process;
- security verification;
- affected roles;
- record requirements;
- and emergency limitations.

Recovery authority SHOULD be at least as constrained and reviewable as the authority it can restore or replace.

---

## 38. Authority and Timelocks

Timelocks MAY be used to reduce unilateral or unexpected material changes.

Where a timelock applies, the specification MUST define:

- triggering approval;
- delay;
- affected action;
- cancellation authority;
- emergency exception;
- and public visibility.

A timelock MUST NOT be claimed where an alternative privileged path can execute the same material change immediately without equivalent controls.

---

## 39. Authority and User Interfaces

User interfaces MUST accurately represent authority.

A UI MUST NOT:

- describe an advisory vote as binding;
- describe an upgradeable contract as immutable;
- describe a removable liquidity position as permanently locked;
- describe a single-controller multisig arrangement as independent;
- hide administrator powers;
- or represent a planned role as active.

Where technically feasible, material authority information SHOULD link to authenticated on-chain or release records.

---

## 40. Authority and Evidence

The existence of authority does not prove correct exercise of authority.

The existence of an approval does not prove:

- that the approved purpose was fulfilled;
- that funds were used correctly;
- that the outcome was positive;
- or that impact occurred.

Authority records must therefore remain linkable to:

- applicable rules;
- decision records;
- execution;
- and evidence.

---

## 41. Authority and Privacy

Authority transparency does not require unnecessary publication of sensitive personal information.

Where signer or reviewer identities cannot appropriately be fully public, GFC MAY use role-based or entity-based disclosure where:

- accountability remains meaningful;
- control structure remains understandable;
- conflicts can be managed;
- and the limitation is disclosed.

Protected identity MUST NOT be used to conceal concentrated or unaccountable control.

---

## 42. Authority and Security

Authority concentration and key compromise are security risks.

The security model MUST evaluate at minimum:

- single-key control;
- shared key custody;
- signer collusion;
- signer compromise;
- deployer-key retention;
- upgrade authority;
- pause authority;
- migration authority;
- recovery authority;
- publication authority;
- backend authority;
- and operational credential compromise.

Higher-risk authority SHOULD receive stronger preventative and monitoring controls.

---

## 43. Authority and Production Releases

A production release SHOULD identify all material authorities applicable to the released deployment.

At minimum, where applicable:

- deployer;
- contract owner;
- proxy administrator;
- upgrade authority;
- pauser;
- fee authority;
- allocation custody;
- treasury authority;
- liquidity authority;
- presale authority;
- staking authority;
- governance executor;
- migration authority;
- and authenticated publication authority.

A production release MUST NOT omit a material authority merely because disclosure would make the system appear less decentralized.

---

## 44. Authority Change Classification

A role or authority change MAY constitute a breaking change where it materially changes:

- who can act;
- approval thresholds;
- execution delay;
- custody;
- upgrade power;
- pause power;
- migration power;
- participant rights;
- treasury control;
- allocation control;
- or evidence-status authority.

Material authority changes MUST be versioned and documented.

Editorial changes to role names are not sufficient to disguise a substantive authority change.

---

## 45. Non-Conforming Authority

Examples of authority non-conformance include:

- hidden administrator access;
- undocumented retained deployer power;
- undisclosed proxy administration;
- undocumented fee control;
- role concentration presented as decentralization;
- signer replacement without record;
- execution without required approval;
- approval after unauthorized execution;
- evidence review misrepresented as independent;
- pilot authority presented as production authority;
- revoked authority that remains technically active;
- or public documentation that understates actual technical power.

Material authority non-conformance MAY require:

- correction;
- role revocation;
- key rotation;
- signer replacement;
- pause;
- migration;
- public clarification;
- security review;
- governance review;
- or incident treatment.

---

## 46. Pilot and Production Separation

The public Base Sepolia pilot is non-production.

Pilot roles, keys, deployers, owners, administrators, wallets, or operational processes MUST NOT automatically be reused or recognized as production authorities.

Before any Base Mainnet production deployment, all material production authority MUST be:

- deliberately selected;
- technically instantiated;
- reviewed;
- authenticated;
- and recorded separately.

A production deployment MUST NOT inherit trust merely from the existence of a verified testnet contract.

---

## 47. Dependencies on Other Specifications

This document MUST be interpreted together with:

- [`README.md`](README.md);
- [`glossary.md`](glossary.md);
- [`non-goals.md`](non-goals.md);
- [`architecture.md`](architecture.md);
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

---

## 48. Unresolved Role and Authority Decisions

The following matters remain unresolved unless separately established by a later specification or authenticated implementation record.

### Production custody

- final production wallet architecture;
- multisig platform or equivalent control model;
- signer count;
- signer categories;
- approval thresholds;
- signer disclosure model;
- and recovery model.

### Token authority

- final production upgradeability;
- final fee-control model;
- recognized-liquidity-pool authority;
- fee-exemption authority;
- transfer-pause authority, if any;
- and final deployment-role removal.

### Allocation authority

- final custody structure for each allocation;
- Guardian Growth approval model;
- Treasury Reserve approval model;
- Liquidity Reserve authority;
- Ecosystem distribution authority;
- and allocation migration authority.

### Governance

- final governance participation model;
- proposal authority;
- voting or advisory rights;
- quorum where applicable;
- veto rights where applicable;
- timelocks;
- execution authority;
- and role-removal authority.

### Presale

- final administrative surface;
- final immutable/configurable boundary;
- final refund implementation;
- treatment of immediate-distribution GFC following failed finalization;
- withdrawal authority;
- and cancellation authority.

### Staking

- final configurable parameters;
- reward distribution authority;
- pause authority;
- migration authority;
- and governance relationship.

### Transparency and evidence

- final registry publication roles;
- evidence-custody roles;
- review roles;
- claim-status authority;
- correction authority;
- suspension or downgrade authority;
- independent-review criteria;
- and protected-access roles.

### Security

- final emergency role model;
- pauser model;
- incident coordinator;
- recovery authority;
- security disclosure authority;
- and key-compromise process.

These unresolved matters MUST NOT be represented as finalized production decisions.

---

## 49. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- all material production roles are defined;
- all material production authority surfaces are mapped;
- token authority is finalized;
- allocation authority is finalized;
- lock and vesting authority is finalized;
- treasury authority is finalized;
- liquidity authority is finalized;
- presale authority is finalized;
- staking authority is finalized;
- governance authority is finalized;
- upgrade authority is finalized;
- pause authority is finalized;
- migration authority is finalized;
- security and recovery authority are finalized;
- evidence and Transparency Registry authority are finalized;
- role appointment and revocation processes are finalized;
- authority registry requirements are finalized;
- conflicts with related specifications are resolved;
- and the production release process can authenticate actual role holders.

---

## 50. Final Authority Principles

The GFC authority model preserves the following distinctions:

> A role definition does not assign a role.

> A wallet label does not create a restriction.

> A private key can create real authority even where documentation is silent.

> Undocumented material authority is non-conforming.

> Advisory participation does not equal binding governance.

> Token ownership does not equal unrestricted governance authority.

> A multisig does not automatically mean decentralization.

> Multiple signers do not automatically mean independent signers.

> Deployment authority does not automatically equal ongoing administrative authority.

> Pilot authority does not equal production authority.

> Public communication does not override actual technical authority.

> Revocation in documentation is insufficient if technical access remains active.

> Emergency authority does not justify unlimited authority.

> Migration must not bypass existing rights or restrictions.

> Evidence review does not equal independent verification unless independence is actually established.

> Responsibility follows authority.

The objective is not to claim that authority has disappeared.

The objective is to make material authority explicit, bounded, reviewable, and accountable.

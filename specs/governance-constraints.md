# GFC Governance Constraints Specification

**Document ID:** GFC-GOV-001  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-deployment  
**Intended Network:** Base Mainnet  
**Chain ID:** 8453  
**Last Updated:** 2026-07-23

---

## 1. Document Status

This document defines intended governance constraints for the planned GFC infrastructure.

It is normative because it defines required limitations, prohibited authority, approval boundaries, disclosure requirements, and safeguards.

Its maturity remains Draft. The requirements may change before the first versioned release.

At the time of publication:

- no production GFC governance system is represented as deployed;
- no production governance contract is represented as active;
- no production multisig configuration is established by this document;
- no governance vote, proposal, signer group, or administrative role should be treated as official unless published through an authenticated GFC release;
- exact thresholds, timelocks, role holders, and voting mechanisms remain unresolved;
- this document does not establish complete decentralization;
- no implementation is governed by this document unless it explicitly identifies an applicable versioned release.

The presence of a governance mechanism or role in this specification does not mean that it has already been implemented, assigned, reviewed, audited, or activated.

---

## 2. Purpose

This document defines the governance boundaries of GFC.

Its purpose is not to maximize governance activity or distribute authority without limitation.

Its purpose is to ensure that:

- every material authority is explicit;
- decision-making powers are narrowly scoped;
- no role receives undocumented control;
- authority is separated where reasonably possible;
- material actions require appropriate approval;
- token ownership does not automatically create unrestricted governance authority;
- emergency powers remain exceptional;
- contract upgrade, pause, treasury, fee, and migration authority are constrained;
- governance decisions remain traceable;
- conflicts of interest are disclosed and managed;
- operational convenience does not override long-term commitments;
- public statements accurately represent the actual degree of decentralization and control.

Governance is treated as a control and accountability system, not as a marketing claim.

---

## 3. Scope

This specification applies to governance authority relating to:

- smart-contract deployment;
- contract administration;
- contract upgrades;
- proxy administration;
- contract pausing and unpausing;
- fee parameters;
- fee exemptions;
- recognized liquidity pools;
- token allocation custody;
- treasury movements;
- reserve movements;
- liquidity deployment and withdrawal;
- presale administration;
- refund-related administration;
- vesting and lock administration;
- staking administration;
- signer appointment and removal;
- evidence-policy administration;
- transparency-record administration;
- protected-evidence access;
- incident response;
- emergency intervention;
- system migration;
- contract deprecation;
- governance participation;
- proposals;
- voting;
- vetoes;
- execution;
- and public governance disclosure.

---

## 4. Out of Scope

This document does not independently define:

- the final legal entity or organizational structure;
- exact multisig signers;
- exact signer identities;
- exact approval thresholds;
- exact timelock durations;
- final voting mechanics;
- final voting weight;
- final quorum;
- final proposal thresholds;
- final delegation rules;
- final staking-based governance rights;
- jurisdiction-specific corporate governance requirements;
- final employment or contractor authority;
- final internal approval software;
- final accounting procedures;
- final impact-evaluation methodology;
- final legal privilege or confidentiality rules;
- or final regulatory responsibilities.

These matters require separate specifications, policies, legal documents, or release records.

---

## 5. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are normative only when:

- they appear in uppercase;
- the document declares `Authority: Normative`;
- and the document version applies to the implementation being evaluated.

Because this document is currently Draft, its requirements describe intended governance constraints but remain subject to review and versioned release.

---

## 6. Governance Principles

### 6.1 Explicit authority

Every material authority MUST be documented.

No role, wallet, signer, backend service, deployer, administrator, interface, or legal entity may possess material authority solely through implication or informal practice.

### 6.2 Least privilege

Every role MUST receive only the permissions required for its documented purpose.

Roles MUST NOT be granted broad administrative authority merely for operational convenience.

### 6.3 Separation of duties

Proposal, approval, execution, custody, evidence submission, evidence review, and impact evaluation SHOULD be separated where reasonably possible.

Where separation is incomplete, the concentration MUST be disclosed.

### 6.4 Constraints over discretion

Governance processes SHOULD prefer technically enforced limits over discretionary promises.

Human discretion MAY remain where context, law, privacy, security, or impact assessment requires judgment.

Such discretion MUST remain bounded and reviewable.

### 6.5 Accountability over anonymity

Material governance actions MUST be attributable to a documented role or authority structure.

Public disclosure of personal signer identities is not always required, but the controlling role, approval structure, and accountability process MUST be clear.

### 6.6 No governance theatre

The existence of voting, staking, a multisig, community consultation, or public proposals MUST NOT be presented as decentralization unless the actual authority distribution supports that claim.

### 6.7 Long-term commitments take priority

Governance MUST NOT possess easy or undocumented methods to weaken:

- the fixed token supply;
- the Impact Vault lock;
- Core Team vesting;
- refund rights;
- allocation restrictions;
- or other long-term commitments.

### 6.8 No retrospective authorization

Governance MUST NOT retrospectively approve an unauthorized action merely to create the appearance of prior compliance.

### 6.9 Verifiable governance

Material governance actions SHOULD produce verifiable records covering:

- proposal;
- rationale;
- authority;
- approval;
- execution;
- outcome;
- and any deviation.

---

## 7. Governance Model

GFC may use a hybrid governance model combining:

- technical constraints;
- multisig approvals;
- administrative roles;
- community consultation;
- token- or staking-related participation;
- expert review;
- external review;
- and operational execution.

These mechanisms MUST remain distinguishable.

The existence of one mechanism MUST NOT be used to conceal authority held by another.

A community vote, for example, MUST NOT be presented as directly binding where execution remains entirely discretionary.

---

## 8. Governance Authority Categories

Every governance power MUST be assigned to a documented authority category.

Possible categories include:

### 8.1 Immutable rule

A rule that cannot be changed after deployment.

### 8.2 Constrained administrative authority

A narrowly defined role capable of changing only predefined parameters within fixed limits.

### 8.3 Multisig approval authority

Authority requiring multiple approvals before execution.

### 8.4 Timelocked governance authority

Authority whose approved actions become executable only after a predefined delay.

### 8.5 Community advisory authority

Participation that can signal preferences or produce recommendations but cannot directly execute changes.

### 8.6 Binding governance authority

Participation whose valid decision creates an enforceable execution obligation.

### 8.7 Emergency authority

Narrow authority reserved for defined security or operational emergencies.

### 8.8 External legal or compliance authority

Authority required by applicable legal, contractual, regulatory, privacy, or sanctions obligations.

The applicable category MUST be disclosed for every material governance action.

---

## 9. Authority Registry

Before production deployment, GFC MUST publish an authority registry.

For each privileged role, the registry MUST identify:

- role name;
- controlling wallet or contract;
- network;
- affected component;
- permitted actions;
- prohibited actions;
- approval requirements;
- timelock, if any;
- maximum parameter range, if applicable;
- appointment process;
- removal process;
- replacement process;
- emergency authority;
- revocation status;
- and current operational status.

The registry MUST distinguish between:

- active authority;
- inactive authority;
- renounced authority;
- deprecated authority;
- emergency-only authority;
- and temporary deployment authority.

An undocumented role MUST be treated as a governance defect.

---

## 10. Prohibited Implicit Authority

The following forms of implicit authority are prohibited:

- undocumented deployer privileges;
- hidden proxy administrators;
- undisclosed upgrade keys;
- undocumented backend transaction signing;
- unpublished fee-management roles;
- undisclosed wallet ownership;
- unrecorded signer replacement;
- informal treasury approval rights;
- undocumented liquidity withdrawal authority;
- hidden evidence-modification authority;
- interface-level restrictions presented as contract-level restrictions;
- and operational customs treated as binding governance rules.

A public claim that authority does not exist MUST be supported by the actual technical and operational configuration.

---

## 11. Separation of Responsibilities

### 11.1 Core separation

The following responsibilities SHOULD NOT be concentrated in one person, wallet, or entity without explicit justification:

- transaction proposal;
- transaction approval;
- transaction execution;
- custody;
- accounting reconciliation;
- evidence submission;
- evidence review;
- impact evaluation;
- security response;
- and public disclosure.

### 11.2 Transitional concentration

During early project stages, complete separation may not be operationally feasible.

Any transitional concentration MUST document:

- affected roles;
- responsible parties;
- reason for concentration;
- scope;
- maximum authority;
- risk controls;
- intended end state;
- review date;
- and conditions for termination.

Transitional arrangements MUST NOT silently become permanent governance structures.

### 11.3 Self-approval

A role SHOULD NOT be able to propose, approve, execute, verify, and publicly certify the same material action without independent review.

Where unavoidable, the concentration and limitation MUST be disclosed.

---

## 12. Multisig Governance

### 12.1 Purpose

Multisig custody may reduce unilateral control by requiring multiple approvals.

A multisig does not automatically create decentralization or independence.

### 12.2 Required definition

Each production multisig MUST define:

- total number of signers;
- approval threshold;
- signer role categories;
- signer independence assumptions;
- signer appointment;
- signer removal;
- signer replacement;
- compromised-key procedure;
- lost-key procedure;
- transaction review procedure;
- transaction limits;
- and emergency procedure.

### 12.3 Signer independence

Where several signers are controlled by the same person, organization, device environment, or operational chain, this concentration MUST be disclosed.

Nominally separate signers MUST NOT be represented as independent where they are not operationally independent.

### 12.4 Threshold changes

Signer thresholds MUST NOT be changed silently.

A threshold reduction is a material governance change and MUST require:

- documented rationale;
- approval;
- public disclosure;
- risk assessment;
- and versioned governance records.

### 12.5 Signer security

Material signers SHOULD use:

- hardware-backed signing;
- separate recovery materials;
- secure transaction review;
- phishing-resistant procedures;
- and independent communication channels.

### 12.6 Transaction simulation

Material multisig transactions SHOULD be simulated and reviewed before execution.

---

## 13. Timelocks

### 13.1 Purpose

Timelocks provide time for:

- public review;
- detection of malicious actions;
- stakeholder response;
- security intervention;
- and orderly exit or migration.

### 13.2 Applicability

Material non-emergency actions SHOULD use an appropriate timelock, particularly:

- contract upgrades;
- fee changes;
- authority changes;
- reserve movements;
- major treasury transfers;
- governance-parameter changes;
- and system migrations.

### 13.3 Disclosure

The final governance specification MUST define timelock duration by action category.

### 13.4 Bypass

Any emergency timelock bypass MUST be:

- narrowly scoped;
- separately authorized;
- publicly detectable;
- and subject to post-incident review.

A bypass MUST NOT become a routine execution path.

---

## 14. Proposals

Material governance actions SHOULD begin with a documented proposal.

A proposal SHOULD include:

- proposal identifier;
- title;
- proposer;
- affected component;
- requested action;
- rationale;
- legal or operational basis, where relevant;
- financial impact;
- security impact;
- governance impact;
- implementation plan;
- rollback or migration plan;
- supporting evidence;
- conflicts of interest;
- voting or approval period;
- and proposed execution date.

Incomplete proposals MUST NOT be represented as approved final actions.

---

## 15. Governance Participation

### 15.1 Potential participation mechanisms

GFC MAY support:

- token-based participation;
- staking-based participation;
- community consultation;
- delegate participation;
- expert review;
- guardian review;
- or hybrid processes.

### 15.2 Participation classification

Every participation mechanism MUST state whether it is:

- informational;
- advisory;
- proposal-forming;
- approval-requiring;
- veto-capable;
- or directly executable.

### 15.3 No implied authority

Participation MUST NOT be described as governance power where it only provides feedback.

### 15.4 No unrestricted token governance

GFC token ownership or staking MUST NOT automatically grant unrestricted authority over:

- treasury custody;
- Impact Vault assets;
- Core Team vesting;
- contract upgrades;
- private keys;
- personal data;
- protected beneficiary information;
- legal obligations;
- regulatory decisions;
- sanctions decisions;
- incident-response secrets;
- or final impact-verification status.

### 15.5 Economic concentration

The final governance model MUST address governance capture through:

- concentrated token ownership;
- delegated voting;
- exchange-held balances;
- treasury-controlled balances;
- team allocations;
- sybil behavior;
- borrowed voting power;
- and temporary liquidity-based voting manipulation.

### 15.6 Excluded balances

The governance specification MUST define whether locked, treasury-held, presale, liquidity, team, or contract-held balances carry participation rights.

These rules MUST be public and technically consistent.

---

## 16. Voting Constraints

Where voting is introduced, the applicable specification MUST define:

- eligible participants;
- voting weight;
- proposal threshold;
- quorum;
- approval threshold;
- voting duration;
- delegation;
- snapshot method;
- vote-changing rules;
- abstention treatment;
- tie handling;
- execution conditions;
- cancellation conditions;
- veto authority;
- and dispute procedure.

Voting rules MUST NOT be changed during an active vote except where a critical defect invalidates the process.

An invalidated vote MUST be documented.

---

## 17. Delegation

Where vote delegation is permitted:

- delegation MUST be revocable;
- delegates MUST be identifiable by address;
- delegated voting power MUST be visible;
- conflicts of interest SHOULD be disclosed;
- sub-delegation MUST be explicitly allowed or prohibited;
- and delegation MUST NOT silently transfer custody of tokens.

Delegates MUST NOT claim ownership of delegated assets.

---

## 18. Conflicts of Interest

### 18.1 Disclosure

Governance participants with a material conflict of interest MUST disclose it before participating in the affected decision.

Potential conflicts include:

- financial benefit;
- recipient relationship;
- employment;
- ownership;
- family relationship;
- contractual involvement;
- competing obligation;
- or control over a service provider.

### 18.2 Recusal

The applicable governance process MUST define when recusal is:

- required;
- recommended;
- or unnecessary.

### 18.3 Related-party transactions

Related-party transactions MUST receive heightened review and documentation.

They MUST NOT be approved through undisclosed self-dealing.

### 18.4 Public record

Material conflicts and their handling SHOULD form part of the governance record, subject to legitimate privacy limitations.

---

## 19. Contract Deployment Authority

The authority to deploy official contracts MUST be documented.

Before an official deployment, GFC MUST identify:

- deployer address;
- source-code commit;
- build configuration;
- applicable specification version;
- deployment parameters;
- initial roles;
- role-transfer process;
- temporary deployer authority;
- and authority-renunciation process.

Temporary deployment authority MUST be removed or constrained after deployment where it is no longer required.

The deployer MUST NOT retain undocumented permanent control.

---

## 20. Upgrade Authority

### 20.1 Explicit disclosure

Every upgradeable component MUST disclose:

- proxy type;
- proxy administrator;
- implementation administrator;
- upgrade proposer;
- upgrade approver;
- execution process;
- timelock;
- emergency bypass;
- and public notice process.

### 20.2 Prohibited upgrade effects

An upgrade MUST NOT silently introduce or expand:

- minting authority;
- confiscation authority;
- transfer freezing;
- fee increases;
- fee exemptions;
- treasury withdrawal authority;
- earlier token release;
- shorter vesting;
- weaker locks;
- reduced refund rights;
- broader governance authority;
- or weaker approval thresholds.

### 20.3 Specification requirement

A material upgrade MUST identify the applicable specification version.

An implementation MUST NOT be upgraded first and justified through a later undocumented specification change.

### 20.4 Review

Material upgrades SHOULD undergo:

- technical review;
- security review;
- compatibility review;
- governance review;
- and migration review.

### 20.5 Public notice

Non-emergency upgrades SHOULD be announced before execution.

The notice SHOULD identify:

- affected contracts;
- proposed implementation;
- changes;
- risks;
- execution time;
- and review materials.

---

## 21. Pause Authority

### 21.1 Permitted purpose

Pause authority MAY exist only for defined security, technical, legal, or operational emergencies.

### 21.2 Scope

The final implementation MUST define which functions can be paused.

Pause authority SHOULD be narrower than full contract control.

### 21.3 Prohibited use

Pause authority MUST NOT be used to:

- confiscate balances;
- redirect allocations;
- bypass locks;
- accelerate vesting;
- cancel valid refunds;
- manipulate markets;
- disadvantage selected users without documented basis;
- or avoid governance review.

### 21.4 Duration

A pause MUST be reviewed regularly.

Indefinite suspension without a documented remediation or deprecation plan is NOT RECOMMENDED.

### 21.5 Public disclosure

A material pause SHOULD be publicly disclosed unless immediate disclosure would materially increase an active security risk.

---

## 22. Emergency Governance

### 22.1 Exceptional nature

Emergency authority is exceptional and MUST NOT be treated as normal governance.

### 22.2 Defined emergencies

Emergency authority MAY apply to:

- active exploitation;
- critical smart-contract vulnerability;
- compromised administrative keys;
- compromised multisig signers;
- severe oracle failure;
- fraudulent official interface;
- domain compromise;
- material refund-system failure;
- or legally required immediate suspension.

### 22.3 Constraints

Emergency authority MUST be:

- narrowly scoped;
- time-limited where possible;
- independently reviewable;
- technically observable where possible;
- and incapable of creating permanent standing authority without normal governance approval.

### 22.4 Emergency record

An emergency action SHOULD document:

- incident category;
- authority used;
- affected system;
- action taken;
- time;
- rationale;
- duration;
- user impact;
- remediation;
- and follow-up review.

### 22.5 Delayed disclosure

Sensitive technical information MAY be withheld temporarily where disclosure would increase risk.

The existence of the incident SHOULD still be disclosed when reasonably safe.

---

## 23. Fee Governance

The production governance model MUST define authority relating to:

- sell fee;
- fee calculation;
- fee destination;
- fee exemptions;
- recognized pools;
- router treatment;
- and fee-distribution contracts.

### 23.1 Maximum fee

Unless a later released specification explicitly establishes a stricter model, governance MUST NOT be able to increase the intended sell fee above 1%.

### 23.2 Buy fee

Governance MUST NOT introduce a buy fee through an undocumented administrative action.

### 23.3 Exemptions

Fee exemptions MUST be:

- narrowly justified;
- documented;
- technically identifiable;
- and governed through an explicit process.

Undisclosed exemptions are prohibited.

### 23.4 Fee destination changes

Changing the fee destination is a material governance action.

It MUST require:

- documented rationale;
- authority review;
- public disclosure;
- and updated reporting.

Fee revenue MUST NOT be described as impact funding solely because the destination wallet carries an impact-related label.

---

## 24. Token Supply Governance

### 24.1 Fixed supply

Governance MUST NOT possess authority to increase the fixed maximum supply above:

**1,000,000,000 GFC**

### 24.2 Minting authority

Any temporary deployment mint authority MUST be removed, exhausted, or permanently constrained after initial allocation.

### 24.3 Upgrade-based inflation

Governance MUST NOT use upgradeability to introduce additional discretionary supply.

### 24.4 Allocation integrity

Governance MUST NOT silently alter the approved initial allocation.

Any change before deployment requires an updated specification.

After deployment, allocation movements must be treated as treasury or custody actions and documented accordingly.

---

## 25. Impact Vault Governance

Governance MUST NOT possess authority to:

- reduce the intended 50-year lock;
- withdraw tokens early;
- replace the vault with a weaker structure;
- use emergency authority as an early-release mechanism;
- or reclassify locked tokens as unrestricted inventory.

A migration MAY occur only where it preserves or strengthens:

- locked amount;
- remaining duration;
- economic restriction;
- and allocation purpose.

Any governance claim concerning Impact Vault impact MUST distinguish between:

- locked allocation;
- released allocation;
- documented use;
- verified outcome;
- and verified impact.

---

## 26. Core Team Vesting Governance

Governance MUST NOT possess authority to:

- accelerate the intended 19-year vesting schedule;
- release unvested tokens early;
- replace the vesting contract with a weaker schedule;
- or create an undocumented bypass.

The final governance model MUST define:

- beneficiary replacement;
- succession;
- revocation;
- termination;
- reassignment;
- migration;
- and treatment of unclaimed vested tokens.

Any replacement MUST preserve the remaining vesting constraint unless an applicable released specification explicitly defines a stricter rule.

---

## 27. Presale Governance

### 27.1 Pre-launch authority

Before launch, authorized governance may finalize:

- supported assets;
- pricing implementation;
- duration;
- start conditions;
- refund mechanics;
- eligibility;
- payment routing;
- token-delivery method;
- and operational procedures.

These decisions MUST be published before the presale begins.

### 27.2 Post-launch constraints

Once the production presale begins, governance MUST NOT silently change:

- price;
- eight-week duration;
- €250,000 soft cap;
- maximum Presale Allocation;
- refund rights;
- purchase records;
- accepted payment treatment;
- or withdrawal conditions.

### 27.3 Administrative correction

A narrowly defined correction MAY be permitted for:

- clear technical defects;
- duplicated records;
- failed transactions;
- or legally invalid participation.

Correction authority MUST NOT permit arbitrary purchase alteration.

### 27.4 Presale proceeds

Presale proceeds MUST NOT become freely available before the applicable success and withdrawal conditions are satisfied.

Governance MUST preserve valid refund claims.

### 27.5 Failed presale

If the applicable soft cap is not reached, governance MUST NOT redirect refundable contributions to another purpose.

### 27.6 Unused allocation

Treatment of unused Presale Allocation MUST be defined before launch.

Governance MUST NOT improvise its treatment after the result is known without disclosure and applicable authority.

---

## 28. Treasury Governance

### 28.1 Treasury purpose

Treasury authority exists to execute documented project purposes.

It does not establish unrestricted ownership over treasury assets.

### 28.2 Required controls

Material treasury actions SHOULD require:

- documented purpose;
- proposal;
- budget classification;
- approval;
- recipient review;
- conflict-of-interest disclosure;
- transaction review;
- execution record;
- and reconciliation.

### 28.3 Transaction thresholds

The final treasury specification MUST define approval requirements by transaction value, risk, and purpose.

### 28.4 Prohibited treasury actions

Treasury authority MUST NOT be used for:

- undisclosed personal benefit;
- undisclosed related-party payments;
- market manipulation;
- bypassing allocation restrictions;
- concealing losses;
- falsifying impact claims;
- or avoiding refund obligations.

### 28.5 Public traceability

Treasury movements MUST be publicly traceable on-chain where executed on-chain.

Public traceability does not eliminate the need for purpose and use-of-funds evidence.

### 28.6 Recipient privacy

Recipient identity MAY remain protected where publication would expose personal, beneficiary, contractual, or security-sensitive information.

The reason for restricted disclosure SHOULD be documented.

---

## 29. Liquidity Governance

Governance authority relating to liquidity MUST define:

- approved venues;
- approved pairs;
- deployment amounts;
- price-setting process;
- liquidity-provider position custody;
- fee collection;
- lock status;
- rebalancing;
- removal authority;
- market-making arrangements;
- and reporting.

Liquidity MUST NOT be described as locked unless technically verifiable.

Any authority to remove liquidity MUST be disclosed before deployment.

Governance MUST NOT use liquidity authority to perform undisclosed price manipulation or preferential trading.

---

## 30. Guardian Growth Fund Governance

Before production use, governance MUST define:

- permitted purposes;
- prohibited purposes;
- release conditions;
- approval thresholds;
- transaction limits;
- recipient criteria;
- conflict controls;
- reporting;
- and review.

The word “Guardian” MUST NOT be used to imply independent oversight where control remains internal or concentrated.

Any independent guardian role must have:

- documented appointment;
- defined authority;
- conflict rules;
- removal rules;
- and accountability.

---

## 31. Ecosystem Growth Fund Governance

Governance MUST define eligible use categories, including distinctions between:

- development;
- grants;
- partnerships;
- community incentives;
- marketing;
- infrastructure;
- research;
- and operational support.

Recipients MUST be selected through documented criteria.

Related-party grants or payments require enhanced disclosure and review.

Milestone-based distributions SHOULD be used where appropriate.

---

## 32. Staking Governance

Before staking activation, governance MUST define:

- reward source;
- reward allocation;
- reward duration;
- maximum distribution;
- lock conditions;
- withdrawal conditions;
- governance rights;
- parameter mutability;
- emergency controls;
- and migration.

Governance MUST NOT:

- create additional GFC beyond the fixed supply;
- present variable rewards as guaranteed;
- silently increase reward obligations;
- or grant unrestricted treasury authority through staking.

Material staking parameter changes SHOULD apply prospectively rather than retroactively.

---

## 33. Evidence Governance

### 33.1 Purpose

Evidence governance determines how records are:

- submitted;
- classified;
- anchored;
- reviewed;
- corrected;
- disputed;
- protected;
- and published.

### 33.2 Evidence roles

The system SHOULD distinguish between:

- evidence submitter;
- evidence custodian;
- evidence reviewer;
- impact evaluator;
- portal publisher;
- and dispute reviewer.

### 33.3 No self-certification by default

A project-authored record MUST NOT automatically be presented as independently verified.

### 33.4 Evidence modification

Material evidence records MUST NOT be silently edited or deleted.

Corrections SHOULD preserve:

- prior version;
- correction date;
- correction reason;
- responsible role;
- and revised status.

### 33.5 Evidence-status authority

No single role SHOULD possess unrestricted authority to convert:

- unreviewed evidence;
- project-authored evidence;
- or disputed evidence

into independently verified evidence.

### 33.6 Cryptographic anchoring

Governance authority over evidence anchoring MUST NOT be represented as authority to determine factual truth.

Anchoring establishes integrity of a record, not correctness of its contents.

---

## 34. Impact Governance

### 34.1 Separation from spending authority

The role that approves or executes funding SHOULD NOT be the sole authority determining that the resulting impact was successfully verified.

### 34.2 Impact claims

Governance MUST distinguish between:

- intended impact;
- funded activity;
- delivered output;
- observed outcome;
- and verified impact.

### 34.3 Methodology

Impact status MUST NOT be assigned without reference to an applicable methodology.

### 34.4 Uncertainty

Material limitations, missing data, disputed findings, and uncertainty MUST NOT be concealed.

### 34.5 Independent review

Where GFC describes impact as independently verified, the reviewer’s independence, scope, methodology, and limitations MUST be documented.

---

## 35. Protected Information Governance

### 35.1 Access authority

Access to protected information MUST be:

- role-based;
- purpose-limited;
- logged where possible;
- reviewable;
- and revocable.

### 35.2 Governance limitations

Token holders, voters, or community members MUST NOT automatically receive access to:

- beneficiary data;
- personal data;
- confidential agreements;
- identity documents;
- banking information;
- security-sensitive material;
- or legally privileged information.

### 35.3 Disclosure decisions

Decisions to publish protected information MUST consider:

- lawfulness;
- necessity;
- proportionality;
- consent;
- security risk;
- beneficiary risk;
- and irreversibility.

### 35.4 Blockchain publication

Governance MUST NOT place protected personal information on-chain merely to create an appearance of transparency.

---

## 36. Interface and Backend Governance

### 36.1 Interface limitations

A user interface MUST NOT be treated as governance authority unless it actually controls privileged execution.

### 36.2 Privileged backends

Any backend capable of:

- signing transactions;
- changing records;
- assigning evidence status;
- modifying purchase records;
- redirecting execution;
- or controlling access

MUST be included in the governance authority registry.

### 36.3 UI claims

The interface MUST accurately display:

- contract status;
- upgradeability;
- pause status;
- authority;
- evidence source;
- evidence review status;
- and known limitations.

### 36.4 Front-end compromise

The governance model MUST define authority and procedure for:

- disabling compromised interfaces;
- publishing authenticated warnings;
- rotating infrastructure;
- and directing users to verified contract information.

---

## 37. Signer Appointment and Removal

The final governance process MUST define:

- eligibility;
- appointment authority;
- term, if any;
- security requirements;
- conflict rules;
- resignation;
- removal;
- emergency suspension;
- replacement;
- and handover.

A signer MUST be removable where:

- keys are compromised;
- duties are not fulfilled;
- conflicts become unacceptable;
- legal incapacity exists;
- or governance approval requires replacement.

Removal MUST NOT silently alter approval thresholds.

---

## 38. Role Succession

Material roles MUST have documented succession procedures.

Succession MUST address:

- death or incapacity;
- key loss;
- organizational dissolution;
- prolonged unavailability;
- resignation;
- removal;
- and compromised authority.

Succession procedures MUST NOT create unrestricted recovery authority.

---

## 39. Governance Records

Material governance records SHOULD include:

- unique identifier;
- date;
- responsible role;
- proposal;
- discussion;
- approval result;
- conflicts;
- execution transaction;
- affected assets or contracts;
- supporting documents;
- outcome;
- and final status.

Where information is withheld, the record SHOULD state:

- that information was withheld;
- the category of information;
- and the reason for restriction.

---

## 40. Public Disclosure

GFC SHOULD publicly disclose material governance information through durable and authenticated channels.

Material disclosures include:

- authority registry;
- active privileged roles;
- multisig configuration;
- contract upgrades;
- pauses;
- signer changes;
- fee changes;
- treasury movements;
- major allocation movements;
- liquidity changes;
- incidents;
- migrations;
- and deprecations.

Public disclosure MUST distinguish between:

- proposal;
- approval;
- scheduled execution;
- executed action;
- failed action;
- cancelled action;
- and reversed or migrated action.

---

## 41. Governance Communication

Public governance communication MUST NOT:

- imply decentralization where material authority remains concentrated;
- describe advisory voting as binding;
- describe a multisig as trustless;
- conceal administrative keys;
- present planned governance as active;
- or claim independent oversight without an independent party.

Technical and public descriptions MUST remain consistent.

---

## 42. Governance Security

Governance security controls SHOULD include:

- hardware-backed signing;
- signer separation;
- transaction simulation;
- phishing-resistant verification;
- monitoring;
- timelocks;
- role-change alerts;
- upgrade alerts;
- pause alerts;
- threshold-change alerts;
- fee-change alerts;
- and large-transfer alerts.

Security procedures MUST address both technical compromise and signer collusion.

---

## 43. Governance Incident Classification

Governance incidents MAY include:

- unauthorized transaction;
- unauthorized role assignment;
- compromised signer;
- collusion;
- invalid vote;
- threshold bypass;
- malicious upgrade;
- undisclosed parameter change;
- prohibited treasury use;
- evidence manipulation;
- false impact certification;
- privacy breach;
- or specification deviation.

Each material incident SHOULD be classified by:

- severity;
- affected authority;
- affected assets;
- user impact;
- duration;
- containment;
- remediation;
- disclosure status;
- and continuing risk.

---

## 44. Disputes and Challenges

The final governance system SHOULD provide a process for challenging:

- authority claims;
- governance results;
- transaction classification;
- treasury purpose;
- evidence status;
- impact status;
- conflicts of interest;
- and specification conformance.

The dispute process MUST define:

- eligible challenger;
- submission method;
- evidence requirements;
- reviewer;
- response time;
- possible outcomes;
- and appeal or reconsideration, where applicable.

A dispute MUST NOT be treated as resolved merely because the original decision-maker rejects it.

---

## 45. Governance Change Management

### 45.1 Clarification

A clarification may improve wording without materially changing:

- authority;
- permissions;
- thresholds;
- voting rights;
- approval requirements;
- timelocks;
- treasury controls;
- user rights;
- or security assumptions.

### 45.2 Non-breaking change

A non-breaking change may introduce additional safeguards without invalidating previously conforming governance behavior.

### 45.3 Breaking change

A breaking governance change includes modification of:

- authority;
- approval threshold;
- signer requirements;
- voting rights;
- quorum;
- veto power;
- timelock;
- emergency power;
- treasury control;
- upgrade control;
- pause control;
- fee authority;
- evidence authority;
- or impact-verification authority.

Breaking changes require:

- explicit versioning;
- rationale;
- risk analysis;
- compatibility review;
- public documentation;
- and implementation mapping.

### 45.4 No silent change

Material governance rules MUST NOT be changed solely through informal statements, interface updates, or operational practice.

---

## 46. Conformance

A governance implementation conforms to this specification only when:

- all material authority is documented;
- privileged roles are included in the authority registry;
- no undocumented control paths exist;
- fixed-supply constraints remain protected;
- Impact Vault and vesting constraints cannot be weakened through governance;
- presale rights cannot be silently altered;
- material treasury actions require documented authority;
- token ownership does not automatically create unrestricted governance power;
- protected information remains access-controlled;
- evidence and impact statuses are not assigned through undisclosed authority;
- emergency powers remain limited;
- governance actions are traceable;
- and material deviations are disclosed.

---

## 47. Non-Conformance

Governance non-conformance includes:

- undocumented authority;
- excessive privilege;
- unauthorized action;
- threshold bypass;
- missing required approval;
- undisclosed conflict;
- false governance communication;
- silent rule change;
- hidden upgrade authority;
- improper emergency action;
- retrospective authorization;
- evidence-status manipulation;
- or concealment of material control.

Material non-conformance MAY require:

- authority suspension;
- signer replacement;
- contract pause;
- transaction reversal where possible;
- public disclosure;
- specification update;
- migration;
- independent investigation;
- or incident treatment.

A specification MUST NOT be changed retrospectively merely to conceal governance non-conformance.

---

## 48. Governance Non-Goals

GFC governance does not aim to:

- fully automate all decisions;
- eliminate human judgment;
- grant unrestricted authority through token ownership;
- equate voting participation with legal authority;
- expose protected personal information;
- make every operational detail public;
- describe a multisig as inherently decentralized;
- use community voting to avoid professional responsibility;
- remove emergency response capability entirely;
- permit emergency authority without limitation;
- allow governance to override fixed-supply commitments;
- allow governance to weaken long-term locks or vesting;
- use governance as justification for arbitrary treasury spending;
- or create a false impression that trust has been eliminated.

The purpose of governance is to bound and expose authority, not to deny that authority exists.

---

## 49. Unresolved Governance Decisions

The following matters remain unresolved and MUST be completed before this document can become Stable.

### 49.1 Governance structure

- final governance model;
- role hierarchy;
- legal authority relationship;
- community participation model;
- expert participation;
- guardian participation;
- and execution model.

### 49.2 Multisig

- platform;
- signer count;
- approval threshold;
- signer categories;
- independence requirements;
- signer disclosure;
- and replacement process.

### 49.3 Timelocks

- action categories;
- standard delay;
- high-risk delay;
- emergency bypass;
- and cancellation authority.

### 49.4 Voting

- eligibility;
- voting weight;
- proposal threshold;
- quorum;
- approval threshold;
- delegation;
- snapshots;
- voting duration;
- veto;
- and execution.

### 49.5 Treasury

- transaction thresholds;
- budget categories;
- spending authority;
- recipient review;
- recurring-payment authority;
- and related-party controls.

### 49.6 Contracts

- upgrade authority;
- pause authority;
- fee authority;
- pool recognition;
- migration authority;
- and role renunciation.

### 49.7 Presale

- pre-launch administrator;
- correction authority;
- refund administration;
- withdrawal approval;
- and failed-sale governance.

### 49.8 Evidence

- reviewer roles;
- evidence-status authority;
- protected-access authority;
- correction process;
- dispute process;
- and independent verification standards.

### 49.9 Impact

- evaluator appointment;
- methodology approval;
- conflict rules;
- review independence;
- and impact-status challenge process.

### 49.10 Incidents

- severity model;
- emergency authority;
- public disclosure timing;
- investigation authority;
- remediation approval;
- and post-incident review.

---

## 50. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- the final governance model is defined;
- all privileged roles are identified;
- an authority registry format is approved;
- multisig configuration is defined;
- signer independence requirements are defined;
- signer replacement is defined;
- timelock requirements are defined;
- voting mechanics are defined or explicitly excluded;
- token- and staking-based rights are defined;
- governance capture risks are addressed;
- conflicts-of-interest rules are approved;
- upgrade authority is defined;
- pause authority is defined;
- emergency authority is defined;
- fee governance is finalized;
- supply protection is technically confirmed;
- Impact Vault governance is finalized;
- Core Team vesting governance is finalized;
- presale governance is finalized;
- treasury governance is finalized;
- liquidity governance is finalized;
- evidence governance is finalized;
- protected-information governance is finalized;
- impact-governance boundaries are finalized;
- incident and dispute processes are defined;
- public disclosure requirements are approved;
- security review is completed;
- related specifications are mutually consistent;
- and a versioned release process exists.

---

## 51. Final Governance Principle

GFC governance must make the complete control surface visible.

A public wallet does not reveal who controls it.

A multisig does not automatically prove independence.

A vote does not automatically create binding authority.

A token does not automatically create governance rights.

A governance label does not technically constrain power.

A public explanation does not replace prior authorization.

An emergency does not create permanent authority.

Governance is credible only where authority, limitations, approvals, execution, evidence, and accountability can be examined together.

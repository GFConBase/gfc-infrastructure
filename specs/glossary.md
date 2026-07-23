# Global Foundation Coin Glossary

**Document ID:** GFC-GLO-001  
**Maturity:** Draft  
**Authority:** Normative  
**Version:** Unreleased  
**Implementation Status:** Pre-deployment  
**Intended Network:** Base Mainnet  
**Chain ID:** 8453  
**Last Updated:** 2026-07-23

---

## 1. Document Status

This glossary defines terminology used across the current Global Foundation Coin specifications.

It is normative because consistent terminology is required to interpret requirements, constraints, claims, system states, evidence statuses, and governance authority correctly.

Its maturity remains Draft. Definitions may change before the first versioned release.

At the time of publication:

- no production GFC token contract is represented by this repository as deployed;
- no GFC presale is live;
- no production treasury, staking, governance, vesting, or transparency system is represented as fully operational;
- no public presale date is established by this document;
- no contract or wallet address is established as official by this document;
- no definition in this glossary independently establishes implementation, deployment, audit, legal status, or operational availability.

Definitions describe how terms are intended to be used.

They do not prove that the component described by a term already exists.

---

## 2. Interpretation Rules

### 2.1 Defined terminology

Terms defined in this glossary SHOULD be interpreted consistently across all GFC specifications.

Where a specification assigns a more specific definition to a term, the more specific definition applies within the scope of that specification.

### 2.2 Capitalization

A defined term may retain its meaning regardless of capitalization unless a specification explicitly distinguishes between capitalized and lowercase usage.

### 2.3 Singular and plural

A defined term includes its singular and plural forms where the context permits.

### 2.4 No implementation assumption

The appearance of a term does not mean that the corresponding feature has been:

- implemented;
- tested;
- audited;
- deployed;
- activated;
- or publicly released.

### 2.5 Actual execution and conformance

Deployed code and on-chain state determine what actually executes.

The applicable released specification determines whether that execution conforms to the approved design.

A difference between the two is a deviation, defect, incident, or version mismatch.

It is not automatically resolved by treating one description as an alternative interpretation.

---

# Project and Specification Terms

## 3. GFC

### GFC

The token, project, and associated infrastructure described by the current Global Foundation Coin specifications.

Depending on context, GFC may refer to:

- the GFC token;
- the wider GFC project;
- a specific GFC system component;
- or the complete planned GFC infrastructure.

The intended meaning SHOULD be made explicit where ambiguity is possible.

### Global Foundation Coin

The current project name represented by the abbreviation GFC.

The name does not independently establish:

- a legal foundation;
- charitable status;
- nonprofit status;
- tax-exempt status;
- governmental recognition;
- regulatory approval;
- or any particular legal structure.

### German Foundation Coin

A deprecated historical project name.

Current specifications and public technical documentation SHOULD use `Global Foundation Coin`.

Historical records MAY retain the former name where necessary for accurate archival context.

Historical naming MUST NOT be presented as the current project identity.

---

## 4. Specification

### Specification

A document defining intended system behavior, requirements, constraints, terminology, authority, state transitions, or prohibited behavior.

A specification may describe a system before implementation.

### Spec

An abbreviation for `Specification`.

### Applicable Specification

The specific versioned specification assigned to an implementation, deployment, component, process, or claim.

A Draft document in the `main` branch is not automatically the applicable specification for a production system.

### Specification Set

The collection of related GFC specifications intended to be interpreted together.

### Versioned Specification

A specification included in an identifiable repository release or version.

### Specification Release

A published and identifiable group of specification versions intended to serve as an authoritative reference.

### Main Branch

The current working branch of the repository.

The `main` branch may contain unreleased changes and MUST NOT automatically be treated as the specification governing a production deployment.

### Source of Authority

The authenticated and applicable reference used to determine intended system requirements.

For production implementations, this SHOULD be a versioned specification release linked to the relevant source code and deployment.

### Conformance

The condition in which an implementation, process, interface, or communication satisfies all applicable requirements.

### Conforming Implementation

An implementation that satisfies the applicable versioned specifications and discloses any accepted deviations.

### Non-Conformance

A failure to satisfy an applicable requirement.

### Deviation

A known difference between intended or specified behavior and actual behavior.

A deviation may be:

- accepted;
- unresolved;
- temporary;
- material;
- security-relevant;
- or prohibited.

### Known Deviation

A deviation that has been explicitly identified and documented.

### Defect

An unintended error in specification, implementation, configuration, operation, or documentation.

### Invariant

A condition that MUST remain true throughout applicable system states or operations.

### Requirement

A defined condition that an applicable implementation or process is expected to satisfy.

### Constraint

A limitation intended to narrow authority, behavior, configuration, or possible outcomes.

### Prohibited Behavior

An action or condition explicitly disallowed by an applicable specification.

### Non-Goal

A capability, claim, interpretation, optimization target, or expectation that GFC intentionally does not support under the current architecture.

---

## 5. Specification Metadata

### Maturity

The development and review stage of a document.

### Draft

A maturity status indicating that a document is under active development and may change materially.

### Review

A maturity status indicating that a document is structurally complete and awaiting formal review or approval.

### Stable

A maturity status indicating that a document has been approved for a defined implementation or release.

Stable does not independently mean:

- implemented;
- audited;
- deployed;
- immutable;
- or legally approved.

### Deprecated

A maturity status indicating that a document or implementation is retained for historical reference but should not be used for new deployments.

### Authority

The type of interpretive weight assigned to a document or provision.

### Informative

Explanatory material that provides context but does not independently define binding requirements.

### Normative

Material that defines requirements, constraints, invariants, terminology, or prohibited behavior.

`Normative` is not a maturity level.

A document may be both:

- Draft and Normative;
- Review and Normative;
- Stable and Normative;
- or Stable and Informative.

### Unreleased

A version status indicating that the document has not yet been included in an authoritative versioned release.

### Pre-deployment

An implementation status indicating that no production deployment is represented as active under the document.

---

## 6. Normative Language

### MUST

An absolute requirement.

### MUST NOT

An absolute prohibition.

### SHOULD

A recommended requirement that may be departed from only where a justified reason exists.

### SHOULD NOT

A discouraged behavior that may be used only where a justified reason exists.

### MAY

A permitted but optional behavior.

### REQUIRED

Equivalent in requirement strength to `MUST`.

### OPTIONAL

Equivalent in permission to `MAY`.

Normative terms are binding only where:

- they appear in uppercase;
- the containing document declares `Authority: Normative`;
- and the document version is applicable.

---

# Network and Technical Terms

## 7. Blockchain Terms

### Blockchain

A distributed ledger that records transactions and state according to a defined consensus and execution model.

### Base

The intended initial blockchain network for GFC deployment.

### Base Mainnet

The production Base network.

### Chain ID

A numeric identifier used to distinguish blockchain networks.

The intended GFC network uses Base Chain ID:

`8453`

### On-Chain

Data, state, logic, or transactions recorded or executed on a blockchain.

On-chain does not automatically mean:

- correct;
- lawful;
- independently interpreted;
- or sufficient to verify real-world claims.

### Off-Chain

Data, decisions, processes, evidence, or execution occurring outside the blockchain.

### Smart Contract

Program code deployed to a blockchain and executed according to network rules.

### Contract Address

The blockchain address at which a smart contract is deployed.

### Verified Contract

A contract whose published source code and build information have been matched to the deployed bytecode through an appropriate verification process.

Source verification does not independently constitute a security audit.

### Contract State

The data stored and maintained by a smart contract.

### Contract Event

A structured log emitted during smart-contract execution.

### Transaction Hash

A unique reference identifying a blockchain transaction.

### Block Explorer

A service used to inspect blockchain transactions, addresses, contracts, and state.

A block explorer is a viewing and indexing service, not the blockchain itself.

### RPC Provider

Infrastructure that provides software access to blockchain data and transaction submission.

### Indexer

A system that processes blockchain data into searchable or derived records.

Indexed data may be delayed, incomplete, or incorrect and SHOULD remain reconcilable with primary on-chain data.

### Primary On-Chain Source

Authenticated blockchain state or transaction data obtained directly or through a verifiable network interface.

### Derived Data

Information calculated, summarized, categorized, or indexed from primary data.

---

## 8. Token Terms

### Token

A blockchain-based digital asset represented by a smart contract.

### GFC Token

The intended ERC-20-compatible token of Global Foundation Coin.

### ERC-20

A token-interface standard used by compatible smart contracts on Ethereum-compatible networks.

### Decimals

The number of decimal places used to represent token subdivisions.

The intended GFC token uses 18 decimals.

### Total Supply

The total number of GFC units created and represented by the token contract.

### Fixed Supply

A supply model in which the maximum number of tokens cannot be increased after the approved initial creation process.

The intended GFC fixed supply is:

`1,000,000,000 GFC`

### Inflation

An increase in token supply over time.

The intended GFC model does not include discretionary inflation.

### Minting

The creation of additional token units.

### Mint Authority

A role or mechanism capable of creating token units.

### Burning

The permanent removal of tokens from spendable circulation, generally by reducing supply or transferring tokens to an irrecoverable mechanism.

### Balance

The amount of a token recorded for an address.

### Transfer

Movement of tokens from one address to another.

### Buy

A transfer classified by the applicable token logic as an acquisition through a recognized liquidity or trading mechanism.

### Sell

A transfer classified by the applicable token logic as a disposal through a recognized liquidity or trading mechanism.

### Ordinary Transfer

A wallet-to-wallet or contract interaction that is not classified as a buy or sell under the applicable rules.

### Buy Fee

A fee applied to a transaction classified as a buy.

The current intended GFC buy fee is 0%.

### Sell Fee

A fee applied to a transaction classified as a sell.

The current intended GFC sell fee is 1%.

### Fee Destination

The wallet or contract receiving collected transaction fees.

### Fee Exemption

A documented exception under which a defined address or transaction category is not subject to a fee.

### Recognized Liquidity Pool

A pool address identified by the token logic for buy or sell classification.

### Circulating Supply

The portion of token supply reasonably available for transfer or market participation.

Locked, unvested, unallocated, or otherwise restricted tokens may be excluded depending on the declared methodology.

---

# Allocation Terms

## 9. Token Allocation

### Allocation

A defined portion of the total GFC supply assigned to a specific role or intended purpose.

An allocation name describes intended use.

It does not independently prove compliant use.

### Impact Vault

The intended allocation containing 25% of total GFC supply:

`250,000,000 GFC`

It is intended to be subject to a 50-year lock.

The existence of the allocation does not itself prove future impact.

### Guardian Growth Fund

The intended allocation containing 20% of total GFC supply:

`200,000,000 GFC`

Its mandate, custody, release conditions, and approval rules require separate definition.

The term `Guardian` does not independently establish external or independent oversight.

### Presale Allocation

The intended allocation containing 15% of total GFC supply:

`150,000,000 GFC`

It defines the maximum amount available for the planned presale.

### Treasury Reserve

The intended allocation containing 15% of total GFC supply:

`150,000,000 GFC`

It is intended to serve as a controlled strategic reserve rather than unrestricted inventory.

### Liquidity Reserve

The intended allocation containing 15% of total GFC supply:

`150,000,000 GFC`

It is intended for defined liquidity-related purposes.

### Ecosystem Growth Fund

The intended allocation containing 5% of total GFC supply:

`50,000,000 GFC`

It may support documented ecosystem, development, grant, partnership, infrastructure, community, or growth activities.

### Core Team Allocation

The intended allocation containing 5% of total GFC supply:

`50,000,000 GFC`

It is intended to vest linearly over 19 years.

### Allocation Integrity

The requirement that token allocation amounts equal the fixed total supply and remain reconcilable with deployment records.

### Allocation Label

A descriptive designation assigned to a wallet, contract, or token amount.

A label is not a technical restriction unless enforced by code or applicable authority controls.

---

# Lock and Vesting Terms

## 10. Locking and Vesting

### Lock

A technical restriction preventing tokens or assets from becoming transferable or withdrawable before defined conditions are met.

### Lock Period

The period during which the locked asset remains unavailable under the applicable rules.

### Lock Start

The timestamp or event from which a lock period begins.

### Lock End

The timestamp or condition at which the lock restriction expires.

### Early Release

Release of locked or unvested assets before the applicable schedule permits it.

### Lock Extension

An increase in the duration of a lock without accelerating release.

### Vesting

A process through which token entitlement becomes available progressively according to a defined schedule.

### Linear Vesting

A vesting model in which entitlement accrues proportionally over time.

### Vesting Period

The total time over which an allocation becomes vested.

### Cliff

An initial period during which no tokens become claimable, followed by vesting or release according to the applicable schedule.

### Vested

An amount that has become available under the vesting schedule.

### Unvested

An amount that has not yet become available under the vesting schedule.

### Vested but Unclaimed

An amount that is available under the vesting schedule but has not yet been withdrawn by the beneficiary.

### Claimed

An amount that has been withdrawn or transferred under an applicable entitlement.

### Vesting Acceleration

A change that makes tokens available earlier than the original schedule.

### Migration

Movement from one contract, wallet, system, or implementation to another.

A conforming lock or vesting migration must preserve or strengthen the remaining economic restriction.

---

# Presale Terms

## 11. Presale

### Presale

A time-bound token-distribution process conducted under predefined pricing, allocation, contribution, success, finalization, claim, and refund rules.

### Planned Presale

A presale under design that is not active.

### Active Presale

A presale contract state in which valid contributions are accepted.

### Presale Duration

The period during which the presale is intended to accept contributions.

The current intended duration is eight weeks.

### Presale Start

The contract-level timestamp or state transition after which valid purchases may be accepted.

### Presale End

The contract-level timestamp after which new purchases are no longer accepted.

### Reference Price

The intended value used to calculate GFC entitlement.

The current intended reference price is:

`€0.05 per GFC`

The reference price is not a market-value guarantee or future price floor.

### Fixed Reference Price

A reference price that remains unchanged throughout the active presale.

### Payment Asset

An asset accepted as consideration in the presale.

### Supported Payment Asset

A payment asset explicitly identified by contract address, network, decimals, and applicable valuation rules.

### Unsupported Payment Asset

An asset not authorized for presale participation.

### Conversion Rate

The rate used to translate a payment asset amount into the applicable euro reference value.

### Purchase-Time Reference Value

The euro-denominated reference value assigned when a contribution is accepted.

This value is intended to determine:

- GFC entitlement;
- soft-cap accounting;
- and purchase records.

### Oracle

A mechanism or service supplying external information, such as asset pricing, to an on-chain system.

### Stale Price

Pricing information older than the maximum age permitted by the applicable presale rules.

### Rounding

The deterministic handling of fractional values created during pricing and token calculations.

### Contribution

A payment accepted by the presale under the applicable rules.

### Contributor

The wallet or eligible participant associated with an accepted contribution.

### Purchase

A valid presale transaction that records payment and creates a GFC entitlement.

### Purchase Record

A record identifying the contributor, payment asset, accepted amount, reference value, and GFC entitlement.

### Token Entitlement

The recorded right to claim a defined amount of GFC after successful finalization.

An entitlement is not the same as an immediately transferred token balance.

### Claim

The action through which a valid participant receives GFC associated with a token entitlement.

### Claim Phase

The state or period in which valid GFC entitlements can be claimed following successful finalization.

### Deferred Claim

A token-delivery model in which purchased GFC becomes claimable after successful presale finalization rather than being transferred during the active sale.

### Instant Distribution

A token-delivery model in which tokens are transferred at purchase time.

Instant distribution is not the current intended GFC presale model.

### Soft Cap

The minimum accepted purchase-time reference value required for the presale to satisfy its quantitative success condition.

The current intended soft cap is:

`€250,000`

### Reaching the Soft Cap

The condition in which recorded accepted contributions equal or exceed the soft cap.

Reaching the soft cap does not by itself mean that:

- the presale has ended;
- funds are withdrawable;
- token claims are active;
- or finalization has completed.

### Hard Cap

An explicitly defined maximum fundraising amount.

### No Separate Monetary Hard Cap

A model in which no independent monetary hard cap exists, while token distribution remains limited by the finite Presale Allocation.

The maximum gross reference value at full intended allocation is:

`€7,500,000`

### Allocation Exhaustion

The condition in which the complete Presale Allocation has been assigned to participant entitlements.

### Finalization

The state transition after the presale end that determines and activates the successful or failed outcome.

### Successful Finalization

Finalization after the presale has ended and all applicable success conditions have been satisfied.

### Failed Finalization

Finalization after the presale has failed to satisfy the applicable success conditions or has been cancelled under refundable conditions.

### Successful Presale

A presale that has ended, reached the soft cap, and completed successful finalization.

### Failed Presale

A presale that has ended without reaching the soft cap or has been validly cancelled under refundable conditions.

### Refund

Return of an accepted contribution to the entitled participant under applicable failed-sale or cancellation conditions.

### Refund Right

An enforceable participant entitlement to recover an accepted contribution.

### Refund Phase

The state or period in which eligible participants may reclaim contributions.

### Pull-Based Refund

A refund model in which each participant initiates the return of their own recorded contribution.

### Contribution Custody

The technical and operational control of accepted presale assets before finalization.

### Escrow

A custody structure that restricts project access to contributions until predefined release conditions are satisfied.

### Presale Proceeds

Accepted contribution assets that become available under the successful-finalization and withdrawal rules.

### Withdrawal

Movement of successfully finalized presale proceeds from the presale or escrow mechanism to an authorized destination.

A withdrawal is governed by authority and custody rules and is not automatically a purely technical action.

### Withdrawal Destination

The predefined wallet or contract permitted to receive successfully finalized proceeds.

### Unsold Tokens

Presale Allocation tokens not assigned to participant entitlements when the presale ends.

### Partial Fill

A purchase mechanism that accepts only the portion of a contribution corresponding to the remaining token allocation and returns or rejects the excess.

### Full Reversion

A purchase behavior in which the complete transaction fails if it would exceed an applicable limit.

### Off-Chain Contribution

A contribution processed outside the on-chain presale mechanism.

Off-chain contributions are not authorized unless separately specified.

---

# Governance Terms

## 12. Governance

### Governance

The rules, roles, approvals, decision processes, authority limitations, and execution mechanisms controlling GFC infrastructure and assets.

### Governance Authority

The documented ability to approve, reject, configure, execute, pause, upgrade, migrate, or otherwise influence a system component.

### Authority

The ability of a role, person, wallet, contract, entity, or process to cause or approve a material action.

### Explicit Authority

Authority whose scope, holder, limitations, and approval requirements are documented.

### Implicit Authority

Authority arising from undocumented control, informal practice, technical access, retained keys, or assumed decision rights.

Implicit material authority is prohibited.

### Control Surface

The complete set of actions that privileged actors can perform.

It may include authority to:

- upgrade;
- pause;
- change parameters;
- assign roles;
- move reserves;
- manage fees;
- migrate contracts;
- or alter evidence status.

### Role

A defined set of permissions and responsibilities.

### Privileged Role

A role capable of performing actions unavailable to ordinary users.

### Administrative Role

A privileged role used to configure, maintain, pause, upgrade, migrate, or operate a system.

### Authority Registry

A public or reviewable registry identifying privileged roles, controlling addresses, permitted actions, approval requirements, timelocks, and current status.

### Least Privilege

The principle that a role receives only the minimum authority required for its documented function.

### Separation of Duties

The division of proposal, approval, execution, custody, verification, review, and reporting responsibilities across different roles where reasonably possible.

### Concentration of Authority

A condition in which several material responsibilities or permissions are controlled by the same person, entity, wallet, or operational group.

### Transitional Arrangement

A temporary governance or operational structure used where the intended final separation of roles is not yet feasible.

### Proposal

A documented request for a governance action.

### Proposer

The role or participant submitting a proposal.

### Approval

A documented authorization required before an action may proceed.

### Execution

The technical or operational performance of an approved action.

### Advisory Governance

Participation that expresses preferences or recommendations without directly binding execution authority.

### Binding Governance

A governance mechanism whose valid outcome creates an enforceable approval or execution requirement.

### Governance Participation

A defined ability to submit proposals, discuss decisions, vote, delegate, approve, veto, or otherwise participate in governance.

### Token-Based Governance

Governance participation influenced by token ownership.

### Staking-Based Governance

Governance participation influenced by valid staking positions.

### Hybrid Governance

A model combining several governance mechanisms, such as multisig, token participation, expert review, and community consultation.

### Governance Capture

A condition in which governance authority is controlled or manipulated by a concentrated actor or coordinated group.

### Governance Theatre

Use of governance terminology or mechanisms to create an appearance of participation or decentralization without corresponding effective authority.

---

## 13. Multisig and Signer Terms

### Multisig

A wallet or contract requiring a defined threshold of approvals from multiple signers before execution.

### Multi-Signature Wallet

Equivalent to `Multisig`.

### Signer

A person, role, device, or authority capable of approving a multisig transaction.

### Signer Independence

The degree to which signers are operationally, organizationally, technically, and economically separate.

Multiple signers are not automatically independent.

### Approval Threshold

The minimum number of required approvals.

### Threshold Reduction

A change lowering the number of approvals needed for execution.

### Signer Replacement

Removal of one signer and appointment of another.

### Signer Compromise

Loss or unauthorized control of a signer key or signing process.

### Transaction Simulation

Pre-execution analysis of the expected result of a blockchain transaction.

---

## 14. Governance Safeguard Terms

### Safeguard

A rule, control, process, or mechanism intended to prevent misuse, reduce risk, preserve rights, or improve accountability.

### Timelock

A mechanism delaying execution after approval.

### Execution Delay

The period between approval and permitted execution.

### Veto

Authority to block an otherwise valid proposal or execution.

### Quorum

The minimum participation required for a governance decision to be valid.

### Proposal Threshold

The minimum qualification required to submit a governance proposal.

### Voting Weight

The quantified influence assigned to a participant’s vote.

### Delegation

Assignment of voting power to another address or participant without transferring ownership of the underlying tokens.

### Delegate

A participant authorized to exercise delegated voting power.

### Conflict of Interest

A circumstance in which a participant’s personal, financial, organizational, contractual, or relational interests may affect impartial decision-making.

### Recusal

The withdrawal of a conflicted participant from part or all of a decision process.

### Related-Party Transaction

A transaction involving a party with a material relationship to a decision-maker, controller, team member, signer, or associated entity.

---

# Administrative and Contract-Control Terms

## 15. Contract Authority

### Deployer

The address or role that creates a smart contract on-chain.

### Deployment

The act of publishing smart-contract bytecode and initial configuration to a blockchain.

### Deployment Record

Documentation linking a deployed component to:

- source code;
- specification version;
- build configuration;
- network;
- addresses;
- roles;
- and review status.

### Immutable Contract

A contract whose material behavior cannot be changed through upgrades, external routing, administrator-controlled replacement, or equivalent mechanisms.

### Configurable Contract

A contract containing parameters that may be changed within documented limits.

### Upgradeable Contract

A contract whose behavior may be replaced or materially modified after deployment through a defined mechanism.

### Proxy

A contract that forwards execution to another implementation contract.

### Proxy Administrator

A role capable of changing the implementation used by a proxy.

### Implementation Contract

The contract containing execution logic used through a proxy.

### Upgrade

A change replacing or modifying deployed contract behavior.

### Upgrade Authority

The role or mechanism capable of authorizing or executing an upgrade.

### Pause

A temporary restriction of defined contract functions.

### Pauser

A role capable of activating a pause.

### Unpause

Restoration of paused functionality.

### Emergency Authority

Narrow authority reserved for predefined urgent security, technical, legal, or operational conditions.

### Emergency Bypass

A defined process that permits an action without the standard delay or approval sequence during a qualifying emergency.

### Migration Authority

Authority to move users, assets, records, or system functions from one implementation to another.

### Renounced Authority

A privilege permanently removed or made unusable.

### Deprecated Implementation

An implementation retained for historical reference but no longer intended for new use.

---

# Treasury and Custody Terms

## 16. Treasury

### Treasury

Assets and custody structures controlled for documented GFC purposes.

### Treasury Asset

A token, stablecoin, cryptocurrency, fiat-linked asset, or other resource held under treasury authority.

### Treasury Movement

Transfer of an asset from or within a treasury-controlled structure.

### Treasury Proposal

A documented request to use or move treasury assets.

### Treasury Approval

Authorization required before a treasury action.

### Treasury Reconciliation

Comparison between approved, transferred, spent, returned, and unresolved amounts.

### Custody

Control and safeguarding of assets or privileged keys.

### Custody Model

The technical and organizational arrangement controlling an asset or authority.

### Material Wallet

A wallet whose assets, authority, operational role, or potential impact makes it significant to the GFC system.

### Operational Wallet

A wallet with a narrow, documented operational purpose and limited exposure.

### Single-Key Wallet

A wallet controlled by one private key.

### Wallet Label

A descriptive name assigned to a wallet.

A wallet label does not itself restrict use.

### Beneficial Control

The actual ability to direct or benefit from an asset, even where the controlling address is formally held by another party.

### Liquidity

Assets made available to support token exchange through a trading mechanism.

### Liquidity Pool

A smart-contract pool containing paired assets used for decentralized trading.

### Liquidity-Provider Position

The ownership interest representing assets supplied to a liquidity pool.

### Liquidity Lock

A technical restriction preventing removal of a liquidity-provider position before defined conditions are met.

### Market Making

Activity intended to provide buy and sell liquidity.

### Slippage

The difference between the expected and executed exchange rate caused by market depth or transaction conditions.

---

# Staking Terms

## 17. Staking

### Staking

A mechanism in which tokens are deposited or committed under defined conditions in exchange for possible rewards, participation rights, or community benefits.

### Hybrid Staking

A staking model combining token rewards with governance-related or community-related benefits.

### Staking Position

A participant’s recorded deposited or committed token amount.

### Staking Reward

A token or benefit distributed according to staking rules.

### Reward Source

The predefined allocation or revenue source funding staking rewards.

### Reward Rate

The rate used to calculate staking rewards.

### APY

Annual Percentage Yield.

A displayed APY is an estimate based on defined assumptions and MUST NOT automatically be interpreted as guaranteed.

### Lock-Up Period

A period during which staked assets cannot be freely withdrawn.

### Early Exit

Withdrawal before the intended staking period has ended, where permitted.

### Reward Sustainability

The ability of a staking system to fund rewards under its stated assumptions without undocumented inflation or unsustainable obligations.

---

# Transparency Terms

## 18. Transparency

### Transparency

The structured ability to examine relevant execution, authority, evidence, limitations, and historical records.

Transparency is not equivalent to publication of all information.

### Transparency Infrastructure

The contracts, registries, records, evidence systems, processes, and interfaces used to make GFC activity reviewable.

### Transparency Portal

A public interface aggregating and explaining relevant on-chain and off-chain information.

The portal is not the primary source of actual blockchain execution.

### Transparency Claim

A statement concerning the visibility, verifiability, reviewability, evidence, or accountability of a system or activity.

### Visibility

The ability to observe information.

Visibility does not automatically establish verification.

### Verifiability

The ability of an external observer or authorized reviewer to test whether a claim is supported by relevant evidence.

### Traceability

The ability to follow an asset, decision, claim, record, or authority across connected stages.

### Accountability

The ability to identify responsible authority, applicable rules, actions, evidence, and consequences.

### Public On-Chain

Information publicly recorded or directly derivable from authenticated blockchain data.

### Cryptographically Anchored

A status indicating that the integrity of an off-chain record is linked to a public cryptographic commitment.

### Protected Off-Chain

Evidence or records maintained outside the public blockchain under access, privacy, integrity, and review controls.

### Publicly Auditable

Capable of being independently examined using publicly accessible information and a defined methodology.

The term does not mean that an audit has actually occurred.

### Fully Transparent

An absolute term that SHOULD NOT be used without strict qualification because every system has privacy, security, evidence, and interpretive limitations.

---

# Evidence and Verification Terms

## 19. Evidence

### Evidence

Information or records used to support, challenge, or evaluate a claim.

### Evidence Item

An individual document, record, transaction, statement, dataset, or cryptographic reference used as evidence.

### Evidence Package

A structured collection of evidence associated with a claim, transaction, allocation, outcome, or impact assessment.

### Evidence Provenance

Information describing where evidence came from, who supplied it, when it was created or submitted, and how it was handled.

### Evidence Custodian

The role responsible for storing and protecting evidence.

### Evidence Submitter

The party supplying evidence.

### Evidence Reviewer

The role evaluating evidence against defined requirements.

### Evidence Status

The current review and handling state of an evidence item.

### Submitted

Evidence received but not yet reviewed.

### Integrity Anchored

Evidence linked to a cryptographic commitment.

This status does not establish factual accuracy.

### Under Review

Evidence currently being evaluated.

### Reviewed

Evidence examined under a defined scope.

### Independently Reviewed

Evidence reviewed by an external party whose independence, scope, and limitations are documented.

### Accepted Evidence

Evidence satisfying the applicable review requirements.

### Rejected Evidence

Evidence that does not satisfy the applicable requirements.

### Disputed Evidence

Evidence whose authenticity, completeness, relevance, or interpretation has been formally challenged.

### Superseded Evidence

Evidence replaced by a later version for current interpretation.

### Withdrawn Evidence

Evidence withdrawn by its submitter.

Withdrawal does not automatically erase its historical use.

### Unavailable Evidence

Required evidence that is missing, inaccessible, or unable to be reviewed.

---

## 20. Claim Terms

### Claim

A statement that may require supporting evidence.

### Claim Category

The type of assertion being made, such as:

- transaction;
- allocation;
- authority;
- use;
- delivery;
- outcome;
- impact;
- compliance;
- or security.

### Claim Status

The current degree of support or resolution assigned to a claim.

### Declared Claim

A stated claim not yet supported by sufficient reviewed evidence.

### Evidence Submitted

A claim state indicating that supporting evidence exists but has not completed review.

### Partially Supported

A claim supported in part while material elements remain unresolved.

### Supported

A claim satisfying the applicable internal evidence requirements.

### Independently Supported

A claim reviewed and supported by a suitably independent external party under a documented scope.

### Verified On-Chain

A claim directly determinable from authenticated on-chain data.

The label applies only to facts actually encoded or directly derivable on-chain.

### Disputed Claim

A claim subject to a material unresolved challenge.

### Not Supported

A claim that available evidence does not substantiate.

### Unable to Determine

A claim for which available evidence is insufficient to reach a conclusion.

### Superseded Claim

A claim replaced by a corrected or more current claim.

---

## 21. Verification Levels

### Transaction Verification

Evaluation of whether a transfer or on-chain action occurred as stated.

Primary question:

`Did the funds move as stated?`

### Use-of-Funds Verification

Evaluation of whether funds were used for the documented purpose.

Primary question:

`Were the funds used for the documented purpose?`

### Output Verification

Evaluation of whether a direct deliverable or activity occurred.

### Outcome Evaluation

Evaluation of an observable change following an activity or output.

### Impact Evaluation

Evaluation of whether an activity produced a meaningful broader or longer-term result.

Primary question:

`Did the documented use create a meaningful result?`

### Transaction Verified

A status indicating that the applicable on-chain transaction can be verified.

This status does not independently verify use, outcome, or impact.

### Use Supported

A status indicating that available evidence supports the documented use of funds.

### Impact Verified

A high-strength claim requiring an applicable methodology, evidence, review scope, limitations, and attribution analysis.

The term MUST NOT be inferred from transaction verification alone.

---

## 22. Outcome and Impact Terms

### Intended Purpose

The documented reason for which a payment, allocation, or activity was approved.

### Use of Funds

The actual application of transferred or held assets.

### Reconciliation

Comparison and linkage between:

- approved amount;
- transferred amount;
- invoiced amount;
- paid amount;
- delivered value;
- returned amount;
- and unresolved amount.

### Output

A direct deliverable or completed activity.

### Outcome

An observable change following an output or activity.

### Impact

A meaningful broader or longer-term result that can reasonably be attributed, at least in part, to an activity.

### Impact Claim

A statement asserting that an activity produced a meaningful result.

### Impact Methodology

The documented process used to assess impact.

### Indicator

A measurable variable used to evaluate an output, outcome, or impact.

### Baseline

The condition measured before or without the evaluated activity.

### Target

The intended result or indicator level.

### Attribution

The degree to which an observed outcome can reasonably be linked to a particular activity.

### Attribution Limitation

A restriction on how confidently an outcome can be assigned to one cause.

### Uncertainty

A documented limitation in available data, methodology, interpretation, or confidence.

### Inconclusive Result

A result for which available evidence does not support a reliable positive or negative conclusion.

### Negative Result

An outcome indicating failure, harm, underperformance, or an unfavorable effect.

---

# Cryptographic and Record Terms

## 23. Cryptographic Evidence

### Cryptographic Anchor

A public cryptographic commitment linked to an off-chain record or record set.

### Anchoring

The process of publishing or recording a cryptographic commitment.

### Hash

A deterministic fixed-length value derived from input data.

### Hash Algorithm

The cryptographic function used to produce a hash.

### Salt

Additional data included before hashing to reduce predictability and brute-force confirmation risk.

### Digital Signature

A cryptographic mechanism used to verify that data was signed by the holder of a corresponding private key.

### Timestamp

A recorded time associated with an event, transaction, record, or commitment.

### Merkle Root

A cryptographic commitment representing a structured set of records.

### Content Commitment

A cryptographic value intended to bind a publisher to specific content without necessarily publishing the content itself.

### Integrity

Confidence that a record has not changed from the version represented by its cryptographic reference.

### Authenticity

Confidence that a record came from the claimed source.

Integrity does not automatically establish authenticity.

### Factual Accuracy

The degree to which the content of a record corresponds to reality.

Cryptographic integrity does not automatically establish factual accuracy.

---

## 24. Record Management

### Record

A durable representation of a transaction, decision, evidence item, claim, review, correction, dispute, or incident.

### Record Identifier

A stable reference assigned to a record.

### Record Linkage

The association of related records across the fund-flow, governance, evidence, outcome, or impact lifecycle.

### Historical Integrity

The preservation of previous material versions, statuses, corrections, and changes.

### Version History

A record of changes made over time.

### Correction

A documented change addressing inaccurate or incomplete information.

### Supersession

Replacement of a record or claim by a later version while retaining historical linkage.

### Redaction

Removal or concealment of protected information while preserving an appropriate record that redaction occurred.

### Silent Deletion

Removal of a material record without preserving an appropriate historical indication.

Silent deletion is prohibited where historical accountability is required.

### Append-Only Record

A record model in which new entries may be added without silently modifying or deleting earlier entries.

### Dispute

A formal challenge to a claim, record, authority, evidence item, review, or interpretation.

### Challenge

A submission requesting reconsideration or verification of a record or claim.

---

# Review and Assurance Terms

## 25. Review

### Review

An examination performed under a defined scope.

### Internal Review

A review performed by GFC or a party under GFC control.

### External Review

A review performed by a party outside the direct internal project structure.

External does not automatically mean independent.

### Independent Review

A review performed by a party whose relevant independence, scope, methodology, access, conflicts, and limitations are documented.

### Reviewer Independence

The degree to which the reviewer is free from relationships or controls that could materially impair impartiality.

### Review Scope

The components, period, evidence, methods, exclusions, and questions covered by a review.

### Audit

A formal examination conducted under a defined scope, methodology, and assurance framework.

The term MUST NOT be used as a generic substitute for:

- code review;
- automated scan;
- internal check;
- informal assessment;
- or testing.

### Smart-Contract Audit

A security-focused audit of defined smart-contract code and associated assumptions.

A smart-contract audit does not independently verify:

- legal compliance;
- fund use;
- financial accounts;
- governance integrity;
- or impact.

### Financial Audit

An audit concerning financial records or reporting under a defined accounting or assurance scope.

### Impact Review

An examination of output, outcome, or impact claims under a documented methodology.

### Finding

An issue, observation, weakness, non-conformance, or conclusion identified during review.

### Remediation

Action taken to correct or reduce an identified issue.

---

# Privacy and Security Terms

## 26. Protected Information

### Protected Information

Information subject to privacy, confidentiality, legal, contractual, operational, or security restrictions.

### Personal Data

Information relating to an identified or identifiable natural person.

### Beneficiary Information

Information relating to individuals or groups receiving or intended to receive support.

### Data Minimization

The principle of collecting, using, and publishing only the information necessary for a defined purpose.

### Access Control

Rules and technical mechanisms limiting who may access a system or record.

### Role-Based Access

Access granted according to documented roles.

### Access Log

A record identifying access to protected systems or information.

### Retention Period

The period for which information must or may be stored.

### Deletion

Removal of information where technically, legally, and operationally applicable.

### Legal Hold

A requirement to preserve information due to a legal, regulatory, contractual, or investigatory obligation.

### Privacy-Aware Transparency

A transparency model that supports accountability without unnecessary exposure of protected information.

---

## 27. Security

### Security Incident

An event affecting confidentiality, integrity, availability, custody, authority, or correct execution.

### Governance Incident

An incident involving unauthorized, improper, undisclosed, or non-conforming authority or decision-making.

### Transparency Incident

An incident involving false, altered, missing, misclassified, exposed, or misleading transparency information.

### Presale Incident

An incident affecting purchase, pricing, contribution custody, entitlement, finalization, claim, refund, or withdrawal behavior.

### Vulnerability

A weakness that may be exploited to compromise system behavior or security.

### Exploit

Use of a vulnerability to cause unauthorized or unintended behavior.

### Key Compromise

Unauthorized access to or control of a private key or signing capability.

### Frontend Compromise

Unauthorized modification or control of a public interface.

### Domain Compromise

Unauthorized control of a domain name, DNS configuration, or related publication channel.

### Oracle Failure

Unavailable, stale, incorrect, manipulated, or otherwise invalid external data supplied to a contract.

### Monitoring

Automated or manual observation of relevant contracts, wallets, roles, events, infrastructure, and anomalies.

### Incident Response

The process used to detect, contain, investigate, remediate, disclose, and review an incident.

### Severity

A classification describing the potential or actual impact of an incident.

---

# Release and Communication Terms

## 28. Implementation Status

### Planned

A component or behavior under consideration or described in a Draft specification.

### Specified

A component or behavior defined by a specification.

### Implemented

A component for which working code or operational processes exist.

### Tested

A component evaluated through documented tests.

### Reviewed

A component examined under a defined review scope.

### Audited

A component examined through a qualifying audit under a defined scope.

### Deployed

A component published to its intended technical environment.

### Active

A deployed component currently enabled for intended use.

### Operational

A component functioning as part of an active production process.

### Paused

A component temporarily restricted through an applicable pause mechanism.

### Migrated

A component whose relevant function, assets, rights, or records have been transferred to a successor.

### Retired

A component intentionally removed from active use.

### Official

Authenticated by the applicable GFC release and publication process.

The term does not mean approved by a government or regulator.

---

## 29. Release Terms

### Release

A published and identifiable version of specifications, code, deployment information, or another project artifact.

### Versioned Release

A release carrying a unique identifier or version.

### Authenticated Release

A release whose origin and integrity can be verified through approved GFC publication methods.

### Release Identifier

A unique tag, version, or reference assigned to a release.

### Source-Code Commit

A specific version of repository content identified by its Git commit hash.

### Build Configuration

The compiler, dependency, optimization, and environment settings used to produce deployable code.

### Deployment Address

The blockchain address of a deployed contract.

### Official Address

A wallet or contract address authenticated through the GFC release process.

### Fake Address

An address falsely represented as official or associated with GFC.

### Known Limitation

A documented restriction, weakness, assumption, or unresolved issue.

---

## 30. Communication Terms

### Public Statement

A statement made through a public GFC-controlled or GFC-associated channel.

### Technical Claim

A statement concerning code, contracts, security, supply, authority, execution, or system behavior.

### Financial Claim

A statement concerning value, return, yield, price, liquidity, revenue, or financial performance.

### Impact Claim

A statement concerning meaningful social, charitable, environmental, operational, or other real-world results.

### Implementation Claim

A statement concerning whether a component is planned, implemented, tested, audited, deployed, or active.

### Overstatement

A claim stronger than the available evidence, implementation status, authority, or review supports.

### Marketing Narrative

Promotional communication intended to explain or position GFC.

Marketing narratives MUST NOT override technical specifications or actual implementation behavior.

### Transparency Theatre

Communication or data publication that creates an appearance of accountability without sufficient context, provenance, authority disclosure, evidence, or reviewability.

---

# Legal and Organizational Terms

## 31. Legal Status

### Legal Entity

An organization formally recognized under applicable law.

### Foundation

A term that may describe a concept, organization, or legal structure depending on context.

Use of the word in the project name does not independently establish a legal foundation.

### Legal Foundation

A foundation formally established under applicable law.

### Charitable Status

A legally recognized status relating to charitable purposes.

### Nonprofit Status

A legally recognized organizational or tax status.

### Tax-Exempt Status

A legally recognized exemption from specified taxes.

### Regulatory Approval

Formal approval from a competent regulatory authority.

Technical deployment does not establish regulatory approval.

### Legal Compliance

Conformity with applicable laws, regulations, contracts, and legally binding obligations.

### Participant Eligibility

The legal, technical, geographic, identity, or contractual conditions required for participation.

### Sanctions Control

Processes intended to prevent prohibited participation or transactions under applicable sanctions requirements.

---

# Final Interpretation Principles

## 32. Foundational Distinctions

The following distinctions apply throughout the GFC specification set:

> Specified does not mean implemented.

> Implemented does not mean audited.

> Audited does not mean risk-free.

> Deployed does not mean active.

> Public does not automatically mean verified.

> Visible does not automatically mean attributable.

> A wallet label does not technically constrain authority.

> A multisig does not automatically prove signer independence.

> A vote does not automatically create binding execution authority.

> Token ownership does not automatically create unrestricted governance rights.

> Reaching the soft cap does not equal successful finalization.

> A token entitlement does not equal an immediately transferred token.

> Participant funds are not project funds while refund rights remain active.

> Transaction verification does not equal use-of-funds verification.

> Use-of-funds verification does not equal impact verification.

> Cryptographic integrity does not equal factual truth.

> External review does not automatically equal independent review.

> A security audit does not verify fund use or impact.

> The project name does not establish legal or charitable status.

> Different claims require different evidence.

---

## 33. Requirements Before Stable Status

This glossary MUST NOT be marked Stable until:

- all current specifications have been reviewed for terminology consistency;
- the current project name has been corrected repository-wide;
- deprecated historical terms have been identified;
- token and fee terminology is finalized;
- presale terminology is finalized;
- governance role terminology is finalized;
- evidence and claim status vocabularies are finalized;
- impact terminology and methodology requirements are finalized;
- legal and organizational terminology is reviewed;
- privacy and security terminology is reviewed;
- all unresolved specification conflicts are resolved;
- and no current definition contradicts an applicable specification.

---

## 34. Final Glossary Principle

GFC terminology must describe actual meaning and actual evidence strength.

Terms must not be selected because they sound stronger, safer, more decentralized, more transparent, more charitable, or more final than the underlying system supports.

Precise language is part of the GFC control and transparency architecture.

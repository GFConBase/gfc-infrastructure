# GFC Token Specification

**Document ID:** GFC-TKN-001  
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

This document defines the current intended token-level requirements for the Global Foundation Coin (GFC).

It is normative because it defines intended requirements and prohibited behavior concerning:

- token identity;
- token supply;
- token precision;
- inflation;
- transfer-fee behavior;
- token-level authority;
- upgrade and migration constraints;
- production disclosure;
- and token-level conformance.

Its maturity remains Draft.

At the current repository state:

- the **GFC Token / Economic Layer** is the current primary product focus;
- a public GFC pilot exists on **Base Sepolia**;
- no production GFC token is deployed on Base Mainnet;
- no production GFC token contract address is established as official by this document;
- no production token implementation is designated as conforming;
- no production specification release has been designated;
- and unresolved token-level design decisions remain subject to review before Stable status.

The public Base Sepolia pilot is non-production.

It MUST NOT be interpreted as:

- the production GFC token;
- a Base Mainnet deployment;
- proof that the production token will use identical bytecode;
- proof that the production token will use identical administrative controls;
- proof of production security;
- or proof of production conformance.

Current implementation and deployment status is maintained in [`../STATUS.md`](../STATUS.md).

---

## 2. Purpose

The purpose of this specification is to define the token-level properties that future production implementations must preserve.

This document establishes the intended production token as:

- **Global Foundation Coin**;
- symbol **GFC**;
- ERC-20-compatible;
- deployed initially on Base Mainnet;
- using 18 decimals;
- with a fixed total supply of **1,000,000,000 GFC**;
- with no discretionary inflation;
- with an intended **0% buy fee**;
- and with an intended **1% sell fee**.

This specification also defines the boundaries of token-level privileged authority.

It does not independently define:

- token allocation custody;
- vesting;
- long-term allocation locks;
- presale accounting and refunds;
- treasury spending;
- liquidity operations;
- staking economics;
- final governance participation;
- evidence or impact verification;
- legal classification;
- or regulatory treatment.

---

## 3. Relationship to the GFC Accountability Model

The long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

The token primarily belongs to the **Funds** and **Rules** portions of this model.

Token code determines technical rules concerning:

- supply;
- balances;
- transfers;
- fee behavior;
- and privileged token-level actions.

Token code does not independently establish:

- why funds moved;
- whether authority was legitimate;
- whether an allocation was used correctly;
- whether an outcome occurred;
- or whether impact was achieved.

A token transaction is therefore technical execution evidence, not complete accountability evidence.

---

## 4. Normative Language

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **NOT RECOMMENDED**, **MAY**, and **OPTIONAL** express requirement levels.

These terms are normative only when:

- they appear in uppercase;
- the containing document declares `Authority: Normative`;
- and the applicable version governs the implementation, process, or communication being evaluated.

Because this document is Draft, these requirements remain subject to formal review and versioned release.

---

## 5. Scope

This specification defines:

- token name;
- token symbol;
- production network;
- token standard;
- token decimals;
- total supply;
- fixed-supply requirements;
- inflation constraints;
- minting constraints;
- burning constraints;
- transfer-fee parameters;
- buy-fee constraints;
- sell-fee constraints;
- transaction-classification requirements;
- fee-exemption requirements;
- fee-destination requirements;
- token-level administrative authority;
- pause and restriction boundaries;
- upgradeability requirements;
- migration requirements;
- disclosure requirements;
- security invariants;
- and token-level conformance.

---

## 6. Out of Scope

This document does not independently define:

- allocation percentages or allocation token amounts beyond requiring reconciliation to total supply;
- allocation-specific custody;
- Impact Vault lock implementation;
- Core Team vesting implementation;
- Guardian Growth governance;
- Treasury Reserve spending rules;
- Liquidity Reserve deployment;
- Ecosystem distribution rules;
- presale payment accounting;
- presale contribution custody;
- presale refunds;
- staking reward calculations;
- staking reward duration;
- governance voting mechanics;
- final legal or organizational structure;
- market-making arrangements;
- exchange listings;
- price guarantees;
- impact claims;
- or regulatory eligibility.

These matters belong in the applicable related specifications or later authenticated implementation records.

---

## 7. Token Identity

A conforming production GFC token MUST use the following intended configuration.

| Property | Required Configuration |
|---|---|
| Token name | Global Foundation Coin |
| Symbol | GFC |
| Production network | Base Mainnet |
| Production chain ID | 8453 |
| Token standard | ERC-20-compatible |
| Decimals | 18 |
| Total supply | 1,000,000,000 GFC |
| Supply model | Fixed supply |
| Additional discretionary inflation | Prohibited |
| Intended buy fee | 0% |
| Intended sell fee | 1% |

The historical project name `German Foundation Coin` is deprecated.

It MUST NOT be used as the current production token name.

The project name does not independently establish legal, charitable, nonprofit, tax-exempt, governmental, or regulatory status.

---

## 8. Production Network

The intended initial production network is **Base Mainnet**.

- **Network:** Base Mainnet
- **Chain ID:** `8453`

The public pilot uses **Base Sepolia**:

- **Network:** Base Sepolia
- **Chain ID:** `84532`

A Base Sepolia token MUST NOT be described as the production GFC token.

Any future production deployment MUST be authenticated independently from the pilot.

This specification does not establish a separate GFC Layer 1, Layer 2, application-specific rollup, bridge, or multichain production system.

Any later expansion requires separate versioned specification and deployment records.

---

## 9. ERC-20 Compatibility

The production token MUST be compatible with the applicable ERC-20 interface unless a later versioned specification explicitly defines a justified deviation.

Compatibility MUST NOT be claimed solely because a contract exposes function names commonly associated with ERC-20.

The applicable production implementation MUST document:

- supported token interfaces;
- transfer behavior;
- approval behavior;
- allowance behavior;
- fee behavior;
- any transfer restrictions;
- any pause behavior;
- permit functionality where applicable;
- and any non-standard administrative behavior.

Material deviations from expected ERC-20 behavior MUST be disclosed before production reliance.

---

## 10. Decimals

The GFC token MUST use:

```text
18 decimals
```

Token balances, allocations, public interfaces, presale calculations, accounting systems, and deployment records MUST use consistent decimal handling.

Any rounding behavior capable of materially affecting:

- token balances;
- fees;
- allocation reconciliation;
- presale distribution;
- or settlement

MUST be deterministic, documented, and tested before production deployment.

---

## 11. Total Supply

The intended production total supply is:

```text
1,000,000,000 GFC
```

The production implementation MUST NOT create a canonical GFC supply greater than this amount.

The production token and initial allocation process MUST reconcile to exactly:

```text
1,000,000,000 GFC
```

The allocation model is defined separately in [`allocations.md`](allocations.md).

The total of all initial allocations MUST equal the complete fixed supply.

---

## 12. Fixed-Supply Requirement

The current GFC token model is a fixed-supply model.

After the approved initial supply has been established, no production authority MUST be capable of discretionary expansion beyond:

```text
1,000,000,000 GFC
```

The following MUST NOT be used as hidden inflation mechanisms:

- retained minting authority;
- unrestricted minter roles;
- upgrade-based supply expansion;
- migration-based duplication;
- replacement-token duplication;
- emergency inflation;
- governance-controlled inflation;
- bridge-based duplication represented as additional canonical native GFC;
- or undocumented reissuance.

A production system MUST NOT describe supply as fixed if a privileged path can increase the canonical supply without a breaking versioned change.

---

## 13. Initial Supply Creation

The exact production deployment method remains unresolved.

A production implementation MAY use:

- initial constructor minting;
- initialization-time minting;
- temporary deployment mint authority;
- or another explicitly specified fixed-supply creation method.

Where temporary mint authority is used, it MUST be:

- limited to the approved initial supply process;
- incapable of exceeding the fixed total supply;
- documented;
- included in the authority surface;
- publicly verifiable where technically possible;
- and removed, exhausted, or permanently disabled after the intended initial allocation process.

Temporary mint authority MUST NOT become continuing discretionary inflation authority.

---

## 14. Inflation

Additional discretionary inflation is prohibited under the current specification.

Future:

- staking rewards;
- ecosystem incentives;
- grants;
- participation rewards;
- growth programs;
- or other token distributions

MUST originate from GFC already included within the fixed supply unless the applicable specification is formally changed through an explicit breaking versioned process.

Using already allocated GFC does not create new supply.

It MUST nevertheless comply with the applicable:

- allocation;
- custody;
- authority;
- vesting;
- economic-flow;
- and disclosure requirements.

---

## 15. Mint Authority

A production token MUST NOT retain an undocumented Mint Authority.

If no post-deployment minting is required, the production architecture SHOULD eliminate any unnecessary mint capability.

If technical deployment requires a temporary Mint Authority, the deployment record MUST identify:

- holder;
- scope;
- maximum mintable amount;
- activation point;
- deactivation or renunciation condition;
- and transaction evidence showing final removal or exhaustion.

A claim that minting is impossible MUST match actual deployed contract state.

---

## 16. Burning

A general production burn model is not currently finalized.

The token specification does not require a discretionary burn function.

If burning is implemented, the applicable production release MUST define:

- who may burn;
- whether holders may burn their own tokens;
- whether any role may burn tokens held by another address;
- whether total supply decreases;
- whether the tokens can later be recreated;
- how burned amounts are reported;
- and how burning interacts with migration.

A burn MUST NOT be presented as permanent supply reduction where an equivalent amount can later be recreated through an undisclosed mechanism.

A privileged authority MUST NOT be able to burn user balances without an explicit, separately specified basis.

---

## 17. Transfer Behavior

The production token MUST document the behavior of:

- wallet-to-wallet transfers;
- wallet-to-contract transfers;
- contract-to-wallet transfers;
- contract-to-contract transfers;
- recognized trading transactions;
- liquidity additions;
- liquidity removals;
- router-mediated transfers;
- aggregator-mediated transfers;
- and any exempt transaction categories.

A transfer path MUST NOT produce materially different behavior solely because the public frontend uses a particular route unless that behavior is part of the disclosed token logic.

---

## 18. Transfer Fees

The current intended fee model is:

| Transaction Classification | Intended GFC Token Fee |
|---|---:|
| Buy | 0% |
| Sell | 1% |

The exact treatment of ordinary transfers and non-standard trading paths MUST be defined before Stable status.

The fee model MUST NOT be described as fully implemented until the applicable production implementation exists and has been tested against the intended classification rules.

---

## 19. Buy Fee

The intended buy fee is:

```text
0%
```

A conforming implementation under the current specification MUST NOT impose a positive GFC token buy fee.

A buy MUST NOT be described as having a 0% GFC token fee if an equivalent project-controlled charge is imposed through:

- hidden token deductions;
- mandatory project side payments;
- undisclosed routing;
- or another functionally equivalent token-level mechanism.

This requirement does not refer to:

- Base network gas;
- decentralized exchange fees;
- third-party router fees;
- liquidity-provider fees;
- or other charges not imposed by the GFC token logic.

Such costs SHOULD be described separately where relevant.

---

## 20. Sell Fee

The intended sell fee is:

```text
1%
```

A conforming implementation under the current specification MUST apply the applicable sell fee according to the finalized transaction-classification logic.

The production implementation MUST disclose:

- exact fee basis;
- calculation sequence;
- rounding;
- collection mechanism;
- fee destination;
- exemptions;
- configurability;
- administrative authority;
- and maximum permitted value.

No role MAY possess undocumented authority to increase the sell fee.

Unless a later released specification explicitly establishes another model through a breaking change, the production sell fee MUST NOT exceed:

```text
1%
```

The fee MUST NOT be described as immutable unless unauthorized change is technically impossible under the complete deployed architecture.

---

## 21. Transaction Classification

The exact technical classification of a transaction as:

- buy;
- sell;
- ordinary transfer;
- liquidity addition;
- liquidity removal;
- router-mediated trade;
- aggregator-mediated trade;
- or another category

remains unresolved.

Before production deployment, the applicable implementation specification MUST define:

- recognized liquidity-pool identification;
- pool registration;
- pool removal;
- router handling;
- aggregator handling;
- liquidity-add behavior;
- liquidity-remove behavior;
- ordinary wallet-transfer behavior;
- contract-transfer behavior;
- fee-exempt behavior;
- and unsupported or ambiguous paths.

Classification MUST be deterministic and testable.

No hidden backend or frontend rule may be required to determine the actual on-chain token fee.

---

## 22. Recognized Liquidity Pools

If buy and sell classification depends on recognized liquidity pools, the production implementation MUST define:

- who may designate a pool;
- who may remove a pool;
- which networks and venues are supported;
- whether designation is immutable or configurable;
- applicable approval requirements;
- applicable timelocks;
- and public disclosure.

Recognized-pool authority is a material token authority.

A malicious or incorrect pool designation MUST be considered in the security model.

---

## 23. Fee Exemptions

Fee exemptions are not finalized.

If exemptions are supported, they MUST be:

- explicit;
- technically identifiable;
- narrowly justified;
- bounded;
- governed through documented authority;
- and reviewable.

The production implementation MUST define:

- which address categories may be exempt;
- who may assign exemption;
- who may remove exemption;
- whether exemption changes are timelocked;
- how historical changes are recorded;
- and whether exemptions affect buy, sell, or other transfer classes.

An exemption system MUST NOT create an undisclosed privileged trading class.

---

## 24. Fee Destination

The final sell-fee destination is unresolved.

Before production deployment, the applicable specification MUST define:

- receiving wallet or contract;
- network;
- custody model;
- accounting category;
- transfer authority;
- conversion authority where applicable;
- distribution authority;
- reporting requirements;
- and whether the destination may be changed.

A wallet label alone does not establish a use restriction.

Fee proceeds MUST NOT be described as:

- impact funding;
- treasury funding;
- liquidity funding;
- staking funding;
- or another restricted purpose

unless the applicable economic flow and authority are actually defined and enforced or governed accordingly.

---

## 25. Fee Proceeds

The final use, custody, conversion, and distribution of sell-fee proceeds remain unresolved.

Any future fee-proceeds flow MUST be specified in [`economic-flows.md`](economic-flows.md).

Fee proceeds are part of the fixed token economy.

Their use MUST NOT:

- create new token supply;
- bypass allocation rules;
- create undocumented treasury authority;
- or be represented as verified impact solely because they are assigned to an impact-related destination.

---

## 26. Token-Level Administrative Authority

All token-level administrative authority MUST be:

- explicit;
- limited;
- attributable;
- reviewable;
- consistent with least privilege;
- and disclosed before production reliance.

The production implementation MUST disclose whether any authority can:

- mint;
- burn;
- pause transfers;
- block or restrict addresses;
- exempt addresses from fees;
- modify fees;
- modify transaction classification;
- add or remove recognized liquidity pools;
- upgrade the token;
- migrate balances;
- recover tokens;
- alter token metadata;
- assign or replace privileged roles;
- or redirect integration addresses.

The complete technical authority surface MUST be consistent with [`roles-and-authority.md`](roles-and-authority.md).

An undocumented privileged path is non-conforming.

---

## 27. Transfer Restrictions

No individualized production transfer-restriction model is currently finalized.

The token MUST NOT contain undocumented authority to:

- confiscate balances;
- arbitrarily move user tokens;
- silently freeze selected holders;
- selectively block transfers;
- or alter balances outside specified mechanisms.

If any future:

- pause;
- denylist;
- allowlist;
- compliance restriction;
- transfer restriction;
- or recovery function

is proposed, it MUST be explicitly defined before production deployment.

Its authority, limitations, user impact, and security assumptions MUST be disclosed.

---

## 28. Pause Authority

Token-level pause functionality remains unresolved.

If a production token supports pausing, the applicable specification MUST define:

- functions affected;
- functions unaffected;
- authorized role;
- approval requirements;
- activation conditions;
- unpause process;
- duration expectations;
- and participant impact.

Pause authority MUST NOT create undocumented capability to:

- seize balances;
- permanently disable selected holders;
- increase supply;
- alter allocation balances;
- accelerate vesting;
- or bypass participant rights.

---

## 29. Token Ownership and Governance

Token ownership MUST NOT automatically provide unrestricted authority over:

- treasury assets;
- Impact Vault assets;
- Guardian Growth;
- Liquidity Reserve;
- Ecosystem;
- allocation custody;
- protected information;
- privileged roles;
- contract upgrades;
- emergency controls;
- legal obligations;
- or impact determinations.

Any future token-related governance or participation rights MUST be explicitly defined.

Participation authority MUST be distinguished from execution authority.

The existence of token voting MUST NOT be presented as proof of complete decentralization.

---

## 30. Upgradeability

The final production token upgrade model remains unresolved.

The production deployment MUST declare whether the token is:

- immutable;
- configurable within defined limits;
- upgradeable;
- replaceable through migration;
- or another explicitly defined model.

If upgradeability exists, the deployment and governance records MUST identify:

- upgrade proposer;
- upgrade approver;
- upgrade executor;
- proxy or equivalent architecture;
- administrator;
- threshold;
- timelock;
- emergency path;
- implementation validation;
- storage compatibility process;
- user-notification process;
- and historical upgrade record.

---

## 31. Upgrade Constraints

An upgrade MUST NOT silently introduce or expand:

- token supply;
- mint authority;
- balance confiscation;
- transfer freezing;
- buy fees;
- sell fees above the applicable maximum;
- fee exemptions;
- weaker allocation constraints;
- weaker lock or vesting restrictions;
- reduced presale rights;
- broader treasury authority;
- or weaker approval requirements.

Any material change to these properties requires an applicable versioned specification change.

If a production token is represented as immutable, no undisclosed external router, proxy, registry, owner-controlled replacement, or migration authority may provide equivalent mutable control.

---

## 32. Migration

A token migration MUST NOT create undisclosed duplicate canonical economic claims.

A migration specification SHOULD define:

- source token;
- destination token;
- authenticated deployment addresses;
- conversion ratio;
- eligibility;
- snapshot or state-transfer method;
- migration start;
- migration deadline where applicable;
- treatment of unclaimed balances;
- treatment of allocation balances;
- treatment of locked balances;
- treatment of vesting balances;
- treatment of fee proceeds;
- treatment of staking positions where applicable;
- administrative authority;
- rollback or failure behavior where applicable;
- and supply reconciliation.

Migration MUST preserve the applicable fixed-supply constraint.

A migration MUST NOT function as a disguised supply expansion or bypass of lock, vesting, allocation, or participant protections.

---

## 33. Bridge and Wrapped Representations

No official cross-chain bridge or wrapped GFC representation is currently established by this specification.

A future bridged or wrapped representation MUST NOT be described as official without:

- an applicable versioned specification;
- authenticated contracts;
- supply-accounting rules;
- bridge-security analysis;
- relationship to canonical Base Mainnet GFC;
- and public deployment records.

A bridged representation MUST NOT create misleading additional canonical supply.

---

## 34. Token Metadata

The production implementation MUST identify token metadata required by the applicable standard and implementation.

Material metadata MUST NOT be changeable through undocumented authority.

If token name or symbol can be altered after deployment, that mutability MUST be disclosed.

The current intended production identity remains:

- **Name:** Global Foundation Coin
- **Symbol:** GFC

---

## 35. Security Invariants

The following token-level security invariants apply.

### 35.1 Supply invariant

Canonical production GFC supply MUST NOT exceed:

```text
1,000,000,000 GFC
```

### 35.2 Identity invariant

The authenticated production token MUST use the applicable production identity and network.

### 35.3 Authority invariant

No material token privilege may exist outside the disclosed authority surface.

### 35.4 Fee invariant

Under the current specification:

- the GFC token buy fee is 0%;
- the GFC token sell fee is 1%;
- and no role may silently exceed the applicable sell-fee maximum.

### 35.5 Allocation-reconciliation invariant

Initial token allocation MUST reconcile to the complete fixed supply.

### 35.6 Upgrade invariant

Upgrade or migration MUST NOT silently weaken fixed-supply or token-level participant protections.

### 35.7 Environment invariant

Base Sepolia pilot token state MUST NOT be represented as Base Mainnet production token state.

---

## 36. Security Requirements

The production token SHOULD undergo security review appropriate to its actual architecture and authority surface.

Security review SHOULD include, where applicable:

- access control;
- supply logic;
- transfer behavior;
- fee logic;
- classification logic;
- exemptions;
- recognized pools;
- allowances;
- upgradeability;
- initialization;
- pause behavior;
- migration;
- integration assumptions;
- and deployment configuration.

Relevant security requirements are defined in [`security-model.md`](security-model.md).

A verified source contract MUST NOT be described as audited solely because source verification succeeded.

---

## 37. Testing Requirements

Before production reliance, testing SHOULD cover both required and prohibited behavior.

Tests SHOULD include, where applicable:

- total supply;
- mint restrictions;
- transfer correctness;
- approvals and allowances;
- 18-decimal handling;
- buy classification;
- sell classification;
- ordinary transfers;
- recognized-pool handling;
- fee exemptions;
- fee maximum;
- fee rounding;
- liquidity addition and removal;
- unauthorized administration;
- pause behavior;
- upgrade restrictions;
- migration reconciliation;
- and deployment initialization.

Invariant testing SHOULD verify that supply cannot exceed the permitted maximum.

Passing tests do not establish absence of vulnerabilities.

---

## 38. Production Deployment Requirements

Before a production GFC token is represented as official, the deployment record MUST identify, where applicable:

- production network;
- chain ID;
- authenticated token contract address;
- deployment transaction;
- source-code release or commit;
- compiler version;
- build configuration;
- applicable specification release;
- constructor or initializer parameters;
- initial supply creation method;
- allocation mapping;
- initial recipients;
- administrative roles;
- mint-authority status;
- fee settings;
- recognized-pool configuration;
- fee-exemption configuration;
- fee destination;
- upgradeability;
- pause authority;
- migration authority;
- source-verification status;
- test status;
- review or audit status;
- and known deviations.

The deployment record MUST distinguish production from:

- test deployments;
- pilots;
- staging deployments;
- deprecated deployments;
- and unofficial copies.

---

## 39. Official Token Authentication

A production token MUST NOT be treated as official solely because:

- its source resembles GFC code;
- it uses the GFC name;
- it uses the GFC symbol;
- it appears on a block explorer;
- it appears on a decentralized exchange;
- it is shared on social media;
- or it is deployed by an address previously associated with a pilot.

Official production status requires authenticated deployment records.

A Base Sepolia `tGFC` pilot token MUST NOT be represented as production GFC.

---

## 40. Public Communication Requirements

Public technical communication concerning the token MUST accurately distinguish between:

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

Public communication MUST NOT:

- describe the Base Sepolia pilot as Mainnet production;
- imply a production token exists before authenticated Mainnet deployment;
- present fixed supply as technically enforced before the applicable implementation exists;
- describe a 1% sell fee as deployed before it is actually deployed;
- describe the token as audited without an applicable audit;
- imply guaranteed token price;
- imply guaranteed liquidity;
- imply guaranteed exchange listing;
- imply guaranteed returns;
- or imply unrestricted governance rights through token ownership.

---

## 41. Economic Relationship

This token specification defines token-level behavior.

It does not independently define the full Economic Layer.

The broader Economic Layer includes:

- allocations;
- vesting and unlocks;
- economic flows;
- staking;
- presale mechanics;
- liquidity-related design;
- treasury-related design;
- governance constraints;
- and transparency requirements.

Those components MUST remain consistent with the token invariants defined here.

---

## 42. Conformance

A token implementation conforms to this specification only when:

- it identifies an applicable versioned token specification;
- its authenticated deployed behavior satisfies all applicable normative requirements;
- token identity matches the specification;
- decimals equal 18;
- canonical supply does not exceed the permitted fixed supply;
- the initial allocation reconciles to the full supply;
- fee behavior matches the applicable release;
- token-level administrative authority is fully disclosed;
- upgrade and migration behavior remain within the applicable constraints;
- the production address is authenticated;
- material deviations are documented;
- and pilot status is not misrepresented as production status.

A website, interface, wallet label, social-media statement, or unauthenticated token address does not establish conformance.

Deployment alone does not establish conformance.

---

## 43. Token Non-Conformance

Token non-conformance includes:

- supply exceeding the applicable fixed maximum;
- undisclosed mint authority;
- hidden balance-confiscation authority;
- undisclosed transfer restrictions;
- buy fees inconsistent with the applicable specification;
- sell fees inconsistent with the applicable specification;
- undisclosed fee exemptions;
- undocumented recognized-pool authority;
- hidden upgrade authority;
- migration that duplicates canonical supply;
- pilot token represented as production token;
- unauthenticated contract address represented as official;
- or public claims materially stronger than deployed behavior supports.

Material token non-conformance MAY require:

- correction;
- role revocation;
- configuration change where permitted;
- pause where applicable;
- public clarification;
- specification update;
- migration;
- replacement deployment;
- security review;
- or incident treatment.

A specification MUST NOT be rewritten retrospectively merely to conceal token non-conformance.

---

## 44. Change Classification

A token-specification change is material where it changes:

- token name;
- token symbol;
- decimals;
- total supply;
- supply model;
- minting;
- burning;
- buy fee;
- sell fee;
- fee maximum;
- fee destination authority;
- fee exemptions;
- transaction classification;
- transfer restrictions;
- pause authority;
- upgradeability;
- migration;
- or token-linked governance authority.

A breaking token change requires:

- explicit versioning;
- rationale;
- security impact analysis;
- governance impact analysis;
- participant-rights analysis;
- economic impact analysis;
- compatibility analysis;
- migration analysis;
- and updated public communication.

Material token behavior MUST NOT be changed solely through:

- frontend updates;
- informal statements;
- social-media announcements;
- or undocumented administrative actions.

---

## 45. Current Unresolved Requirements

The following matters remain unresolved unless separately established by a later versioned specification or authenticated implementation record:

- precise buy and sell classification;
- ordinary-transfer fee treatment;
- recognized liquidity venues;
- recognized-pool administration;
- liquidity-add and liquidity-remove classification;
- router and aggregator classification;
- fee calculation sequence;
- fee rounding;
- final fee destination;
- final fee-proceeds use;
- fee configurability;
- fee-exemption model;
- burn functionality;
- recovery functionality;
- pause functionality;
- individualized transfer-restriction functionality, if any;
- token upgrade architecture;
- token migration architecture;
- token-linked governance or participation rights;
- final deployment method;
- temporary deployment authority;
- and production contract implementation.

These unresolved areas MUST NOT be represented as completed or finalized.

---

## 46. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- production token identity is finalized;
- ERC-20 behavior is finalized;
- fixed-supply implementation is finalized;
- initial supply-creation method is finalized;
- temporary mint authority, if any, is fully constrained;
- buy and sell classification is finalized;
- ordinary-transfer treatment is finalized;
- sell-fee calculation is finalized;
- fee rounding is finalized;
- fee destination is finalized;
- fee-proceeds handling is finalized;
- fee mutability is finalized;
- fee exemptions are finalized or explicitly excluded;
- recognized-pool authority is finalized;
- transfer restrictions are finalized or explicitly excluded;
- pause behavior is finalized or explicitly excluded;
- burn behavior is finalized or explicitly excluded;
- upgradeability is finalized;
- migration behavior is finalized;
- token-linked governance rights are finalized or explicitly excluded;
- security invariants are mapped to the intended implementation;
- deployment and authentication requirements are finalized;
- Base Sepolia pilot and Base Mainnet production terminology are consistently separated;
- and all related specifications are mutually consistent.

---

## 47. Related Specifications

This document MUST be interpreted together with:

- [`README.md`](README.md);
- [`glossary.md`](glossary.md);
- [`non-goals.md`](non-goals.md);
- [`architecture.md`](architecture.md);
- [`roles-and-authority.md`](roles-and-authority.md);
- [`governance-constraints.md`](governance-constraints.md);
- [`security-model.md`](security-model.md);
- [`allocations.md`](allocations.md);
- [`vesting-and-unlocks.md`](vesting-and-unlocks.md);
- [`economic-flows.md`](economic-flows.md);
- [`staking.md`](staking.md);
- [`presale.md`](presale.md);
- [`transparency-model.md`](transparency-model.md);
- and repository-level [`../STATUS.md`](../STATUS.md).

Where another Draft specification conflicts with this document, the conflict MUST be resolved explicitly before Stable status.

---

## 48. Final Token Principles

The GFC token specification preserves the following distinctions:

> Fixed supply is a technical invariant, not a price guarantee.

> A token allocation is not proof of compliant use.

> Token ownership does not automatically create unrestricted governance authority.

> A 0% buy fee refers to the GFC token fee, not all transaction costs.

> A 1% sell fee is not immutable unless the deployed architecture makes unauthorized change impossible.

> Source verification does not equal audit.

> Tested does not mean audited.

> Deployed does not automatically mean conforming.

> Pilot does not mean production.

> Base Sepolia does not mean Base Mainnet.

> A wallet label does not constrain technical authority.

> Upgrade and migration paths are part of the token security model.

> Different economic claims require different evidence.

The production token must make supply, fee behavior, authority, deployment identity, and material limitations independently reviewable before production reliance.

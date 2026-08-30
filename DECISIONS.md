# Global Foundation Coin Decision Record

**Document:** DECISIONS.md  
**Status:** Informative decision register  
**Repository Stage:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Canonical Plan Basis:** 2026-08-25  
**Last Updated:** 2026-08-30

---

## 1. Purpose

This document records the current canonical project decisions that shape the Global Foundation Coin (GFC) repository.

It is intended to prevent:

- contradictory specifications;
- reintroduction of deprecated assumptions;
- accidental promotion of unresolved questions into fixed decisions;
- confusion between pilot state and production state;
- and silent changes to material project direction.

This document is informative.

Normative requirements remain defined in the applicable files under [`specs/`](specs/).

Current operational and deployment state is maintained in:

- [`STATUS.md`](STATUS.md)
- [`DEPLOYMENTS.md`](DEPLOYMENTS.md)
- [`ROADMAP.md`](ROADMAP.md)

---

## 2. Decision Status Model

This document distinguishes among four categories.

### 2.1 Canonical Working Decision

A decision currently adopted as the active project direction.

It is binding for repository consistency unless later changed through an explicit project decision.

A Canonical Working Decision is not automatically:

- a Stable specification;
- implemented;
- tested;
- audited;
- deployed;
- live;
- or legally finalized.

### 2.2 Constraint

A boundary that current design and implementation MUST preserve unless explicitly changed through a later versioned decision.

### 2.3 Historical Fact

A project fact that has already occurred.

Historical facts SHOULD NOT be rewritten as though they were future plans.

### 2.4 Open Decision

A material matter that remains unresolved.

Open Decisions MUST NOT be represented as finalized.

---

## 3. Current Product Focus

**Decision ID:** GFC-DEC-001  
**Status:** Canonical Working Decision  
**Effective Basis:** 2026-08-25

The current primary product focus is:

**GFC Token / Economic Layer**

Through the end of Q1 2027, the project should prioritize work that supports credible readiness of the Token / Economic Layer, including:

- specifications;
- smart-contract development;
- testing;
- security;
- governance;
- transparency;
- partnerships;
- funding;
- marketing;
- website and public communication;
- and legal preparation.

This replaces any interpretation that the current primary product is already the full Accountability Infrastructure.

The broader infrastructure remains the long-term direction.

---

## 4. Long-Term Product Direction

**Decision ID:** GFC-DEC-002  
**Status:** Canonical Working Decision

The long-term GFC product direction is broader than the token alone.

The intended long-term system is:

**Accountability Infrastructure**

The Token / Economic Layer remains one component of that system.

From Q2 2027 onward, the project intends to increase emphasis on the broader accountability architecture.

---

## 5. Canonical Accountability Model

**Decision ID:** GFC-DEC-003  
**Status:** Canonical Working Decision

The canonical accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

This model supersedes any presentation in which the older three-layer explanatory model is treated as the primary system model.

The three-layer model MAY remain as a supporting explanatory view.

The canonical model MUST remain the higher-level framing.

---

## 6. Project Identity

**Decision ID:** GFC-DEC-004  
**Status:** Canonical Working Decision

The current project and token identity is:

**Global Foundation Coin (GFC)**

The historical name:

**German Foundation Coin**

is deprecated for current production naming.

Historical references MAY remain where necessary for accurate archival context.

---

## 7. Initial Production Network

**Decision ID:** GFC-DEC-005  
**Status:** Canonical Working Decision

The intended initial production network is:

**Base Mainnet**

with chain ID:

```text
8453
```

No separate GFC Layer 1, Layer 2, appchain, or rollup is currently part of the initial production commitment.

A future dedicated execution environment MAY be evaluated later if justified.

Such an evaluation does not constitute a current production commitment.

---

## 8. Base Sepolia Public Pilot

**Decision ID:** GFC-DEC-006  
**Status:** Historical Fact

A public GFC pilot exists on:

**Base Sepolia**

with:

```text
Chain ID: 84532
Token: tGFC
Contract: 0x7262Cca91938ede6bB6560F81104Aa410848e7f3
Public pilot date: 2026-08-02
Source status: Verified
```

This pilot is explicitly non-production.

It MUST NOT be interpreted as:

- production GFC;
- Base Mainnet deployment;
- live presale;
- production allocation infrastructure;
- production staking;
- production treasury;
- production governance;
- production Transparency Registry;
- or proof that future production code, parameters, addresses, or authority will be identical.

---

## 9. Pilot and Production Separation

**Decision ID:** GFC-DEC-007  
**Status:** Constraint

Pilot and production MUST remain distinct.

Base Sepolia pilot:

- addresses;
- deployers;
- keys;
- roles;
- balances;
- contracts;
- parameters;
- and processes

MUST NOT automatically acquire Base Mainnet production authority or status.

Production deployments require separate:

- specification;
- implementation;
- testing;
- review;
- deployment;
- authentication;
- and authority records.

---

## 10. Production Token Standard

**Decision ID:** GFC-DEC-008  
**Status:** Canonical Working Decision

The intended production GFC token uses:

- ERC-20-compatible behavior;
- 18 decimals;
- Base Mainnet;
- and fixed total supply.

Exact implementation architecture remains subject to the applicable token specification.

---

## 11. Fixed Total Supply

**Decision ID:** GFC-DEC-009  
**Status:** Constraint

The intended fixed GFC total supply is:

```text
1,000,000,000 GFC
```

Additional discretionary inflation is prohibited under the current model.

Staking, migration, governance, upgrades, rewards, replacement contracts, or other mechanisms MUST NOT silently increase canonical GFC supply beyond this amount.

A future change to this fixed-supply model would be a breaking project decision.

---

## 12. Canonical Allocation Model

**Decision ID:** GFC-DEC-010  
**Status:** Canonical Working Decision

The current Draft allocation model is:

| Allocation | Share | Token Amount |
|---|---:|---:|
| Impact Vault | 25% | 250,000,000 GFC |
| Guardian Growth | 20% | 200,000,000 GFC |
| Presale | 15% | 150,000,000 GFC |
| Treasury Reserve | 15% | 150,000,000 GFC |
| Liquidity Reserve | 15% | 150,000,000 GFC |
| Ecosystem | 5% | 50,000,000 GFC |
| Core Team | 5% | 50,000,000 GFC |
| **Total** | **100%** | **1,000,000,000 GFC** |

The canonical current allocation names are:

- Impact Vault
- Guardian Growth
- Presale
- Treasury Reserve
- Liquidity Reserve
- Ecosystem
- Core Team

Older names such as `Guardian Growth Fund` and `Ecosystem Growth Fund` are deprecated for current specifications.

---

## 13. Impact Vault Long-Term Restriction

**Decision ID:** GFC-DEC-011  
**Status:** Canonical Working Decision / Constraint

The intended Impact Vault allocation is:

```text
250,000,000 GFC
```

The intended restriction is:

```text
50-year lock
```

The following remain unresolved:

- production lock-start event;
- production lock-start timestamp;
- exact unlock mechanics;
- post-lock release model;
- final contract architecture;
- and production custody.

The 50-year commitment MUST NOT be represented as technically enforced before a production implementation actually enforces it.

---

## 14. Core Team Vesting

**Decision ID:** GFC-DEC-012  
**Status:** Canonical Working Decision / Constraint

The intended Core Team allocation is:

```text
50,000,000 GFC
```

The intended restriction is:

```text
19-year linear vesting
```

The following remain unresolved:

- production vesting-start event;
- start timestamp;
- cliff, if any;
- claim interval;
- beneficiary structure;
- reassignment;
- succession;
- revocation;
- and final contract architecture.

No production vesting schedule is currently active.

---

## 15. Token Fee Model

**Decision ID:** GFC-DEC-013  
**Status:** Canonical Working Decision

The current intended GFC token fee model is:

```text
Buy fee: 0%
Sell fee: 1%
```

The 1% sell fee is the current intended maximum under the current specification direction unless explicitly changed through a later breaking decision.

The following remain unresolved:

- buy/sell classification;
- recognized pools;
- router and aggregator behavior;
- exemptions;
- final fee destination;
- final fee-proceeds use;
- fee configurability;
- and exact rounding.

No production fee behavior is currently deployed.

---

## 16. Staking Direction

**Decision ID:** GFC-DEC-014  
**Status:** Canonical Working Decision

The current staking design direction is:

**hybrid and non-inflationary**

Staking MUST NOT create additional GFC beyond the fixed supply.

The following are not yet decided:

- reward source;
- reward rate;
- APR/APY;
- lock period;
- reward duration;
- principal custody;
- early exit;
- penalty model;
- governance-related rights;
- community-related benefits;
- and final production contract architecture.

No production staking system is currently operational.

---

## 17. Presale Reference Price

**Decision ID:** GFC-DEC-015  
**Status:** Canonical Working Decision

The current Draft presale reference price is:

```text
€0.05 per GFC
```

This is a specification design parameter.

It is not:

- a market-value guarantee;
- a future market-price guarantee;
- a price floor;
- or evidence that the presale is live.

---

## 18. Presale Duration

**Decision ID:** GFC-DEC-016  
**Status:** Canonical Working Decision

The current intended presale duration is:

```text
8 weeks
```

No precise public production start date is established by this repository.

Internal planning dates MUST NOT automatically be converted into public launch commitments.

---

## 19. Presale Soft Cap

**Decision ID:** GFC-DEC-017  
**Status:** Canonical Working Decision

The current intended presale soft cap is:

```text
€250,000 reference value
```

Reaching the soft cap before the sale ends MUST NOT automatically mean:

- successful finalization;
- unrestricted project access to participant assets;
- or termination of all applicable participant protections.

---

## 20. Presale Hard Cap Model

**Decision ID:** GFC-DEC-018  
**Status:** Canonical Working Decision

The current design has:

**no separate monetary hard cap**

The Presale allocation is finite:

```text
150,000,000 GFC
```

At the current €0.05 reference price, this corresponds to:

```text
€7,500,000
```

maximum gross reference value at full allocation.

The absence of a separate monetary hard cap MUST NOT be described as unlimited fundraising capacity.

---

## 21. Presale Payment Assets

**Decision ID:** GFC-DEC-019  
**Status:** Canonical Working Decision

The current intended payment assets are:

- ETH
- USDC
- DAI

on Base.

The exact production asset identifiers and implementation remain unresolved and MUST be authenticated before activation.

No other payment asset is currently established as part of the active presale design direction.

---

## 22. Presale Token Delivery

**Decision ID:** GFC-DEC-020  
**Status:** Canonical Working Decision

The current intended presale token-delivery model is:

**Immediate GFC Distribution**

The previous deferred-claim model is deprecated.

Current specifications MUST NOT state that purchased GFC becomes claimable only after successful finalization unless the project formally changes the presale design through an explicit versioned decision.

---

## 23. Presale Refund Principle

**Decision ID:** GFC-DEC-021  
**Status:** Canonical Working Decision / Constraint

The current Draft presale model preserves participant refund rights if the applicable soft-cap success condition is not satisfied.

Refundable participant contribution assets MUST NOT become unrestricted project proceeds while those refund rights remain active.

---

## 24. Immediate Distribution and Failed-Sale Refund Interaction

**Decision ID:** GFC-DEC-022  
**Status:** Open Decision / Production Blocker

The combination of:

- immediate GFC distribution; and
- failed-sale refund rights

creates an unresolved technical and economic interaction.

The project has **not** selected a final mechanism for GFC already distributed if finalization fails.

No current decision authorizes:

- clawback;
- forced transfer;
- forced burn;
- mandatory participant return;
- token invalidation;
- blacklist-based immobilization;
- negative balance;
- replacement token;
- or equivalent corrective mechanism.

This issue MUST be resolved before production presale activation.

The final solution MUST preserve:

- participant refund rights;
- fixed supply;
- Presale allocation accounting;
- deterministic settlement;
- and clear participant-facing disclosure.

---

## 25. Presale Material Logic Immutability Direction

**Decision ID:** GFC-DEC-023  
**Status:** Canonical Working Decision

The current presale design direction is that material participant-facing sale logic should be immutable after production deployment.

At minimum, the final architecture should prevent silent privileged changes to:

- reference price;
- Presale allocation ceiling;
- soft cap;
- participant accounting;
- immediate-distribution rules;
- refund rights;
- finalization rules;
- and proceeds-withdrawal conditions.

If the final implementation retains material mutability, it MUST NOT be described as fully immutable.

---

## 26. Unsold Presale GFC

**Decision ID:** GFC-DEC-024  
**Status:** Open Decision

The final treatment of unsold Presale GFC remains unresolved.

The project has not yet decided whether unsold GFC will:

- remain in Presale;
- move to another allocation;
- be locked;
- be burned;
- be reserved for a future specified distribution;
- or receive another treatment.

This MUST be finalized before production presale activation.

---

## 27. Presale Public Launch Date

**Decision ID:** GFC-DEC-025  
**Status:** Constraint

No precise public presale launch date is established by the repository.

Internal scheduling information MUST NOT be presented as a confirmed public launch date unless formally released.

The public roadmap currently identifies Q1 2027 as the intended readiness / potential start phase, subject to production gates.

---

## 28. Contribution Custody Before Finalization

**Decision ID:** GFC-DEC-026  
**Status:** Constraint

Accepted contribution assets required to satisfy valid refund rights MUST remain available for those rights.

Before applicable successful-finalization and withdrawal conditions are met, refundable contribution assets MUST NOT be used for:

- unrestricted operations;
- marketing;
- development spending;
- liquidity deployment;
- staking;
- lending;
- speculative trading;
- or other discretionary project activity.

The final custody architecture remains unresolved.

---

## 29. Governance Design Principles

**Decision ID:** GFC-DEC-027  
**Status:** Canonical Working Decision / Constraint

The current governance design must preserve:

- explicit authority;
- least privilege;
- separation of duties;
- limited upgrades;
- predictable exceptions;
- timelocks where appropriate;
- attributable emergency authority;
- transparent role changes;
- and historical reviewability.

The project does not currently define a final DAO, token-voting mechanism, quorum, proposal threshold, signer threshold, or governance contract.

---

## 30. Token Ownership Does Not Equal Unrestricted Governance

**Decision ID:** GFC-DEC-028  
**Status:** Constraint

GFC token ownership MUST NOT automatically create unrestricted authority over:

- treasury assets;
- Impact Vault;
- Core Team vesting;
- privileged keys;
- production upgrades;
- emergency authority;
- protected evidence;
- legal obligations;
- or final impact-verification status.

Any future token- or staking-related governance rights must be explicitly specified.

---

## 31. Responsibility Follows Authority

**Decision ID:** GFC-DEC-029  
**Status:** Canonical Working Decision / Constraint

The project adopts the principle:

**Responsibility follows material authority.**

Automation, smart contracts, multisigs, voting, or technical execution MUST NOT be used to imply that human or organizational responsibility has disappeared where material authority remains.

---

## 32. Transparency Registry Direction

**Decision ID:** GFC-DEC-030  
**Status:** Canonical Working Decision

The planned GFC Transparency Registry is intended to operate as a:

**versioned historical record**

rather than a permanent approval badge.

Registry history SHOULD preserve changes in:

- disclosure;
- evidence;
- policy;
- governance;
- authority;
- claim status;
- correction;
- downgrade;
- suspension;
- and supersession.

No complete production Transparency Registry is currently deployed.

---

## 33. Registry Inclusion Does Not Mean Permanent Approval

**Decision ID:** GFC-DEC-031  
**Status:** Constraint

Future Registry inclusion MUST NOT automatically imply:

- permanent approval;
- permanent verification;
- permanent endorsement;
- permanent evidence validity;
- permanent compliance;
- or perpetual eligibility.

Status must be capable of changing when:

- evidence changes;
- rules change;
- governance changes;
- conflicts emerge;
- claims change;
- or new information becomes available.

---

## 34. Future Registry Scope

**Decision ID:** GFC-DEC-032  
**Status:** Canonical Working Decision / Future Direction

The future Transparency Registry MAY eventually include eligible:

- external projects;
- NGOs;
- organizations;
- companies;
- programs;
- or other initiatives.

GFC-defined authority MAY eventually govern:

- admission;
- status;
- verification;
- downgrade;
- suspension;
- correction;
- and removal from current presentation

subject to final governance and transparency specifications.

No such complete production process is currently operational.

---

## 35. Verification Vocabulary

**Decision ID:** GFC-DEC-033  
**Status:** Constraint

GFC must distinguish among:

- source verified;
- reviewed;
- audited;
- deployed;
- live;
- active;
- operational;
- independently verified;
- and other applicable repository status terms.

The word `verified` MUST NOT be used without sufficient scope where ambiguity would materially overstate the evidence.

---

## 36. Main Branch Is Not Production Authority

**Decision ID:** GFC-DEC-034  
**Status:** Constraint

The repository's continuously changing `main` branch is not automatically the production specification or production implementation authority.

Future production deployments must identify the exact applicable:

- specification version;
- source release;
- commit;
- deployment record;
- and authority state.

---

## 37. Production Deployment Authentication

**Decision ID:** GFC-DEC-035  
**Status:** Constraint

Future production deployments must be authenticated separately from Draft specifications and pilot deployments.

Production records should identify, where applicable:

- network;
- chain ID;
- address;
- deployment transaction;
- source commit;
- compiler/build data;
- deployer;
- implementation/proxy structure;
- privileged roles;
- configuration;
- source-verification status;
- test status;
- security-review status;
- audit status;
- applicable specification;
- and known deviations.

Unknown fields MUST NOT be invented.

---

## 38. Security Claims

**Decision ID:** GFC-DEC-036  
**Status:** Constraint

GFC public communication MUST NOT equate:

- source verification with security;
- source verification with audit;
- testing with audit;
- audit with risk-free;
- pilot with production security;
- multisig with decentralization;
- or public code with secure code.

No independent production security audit is currently recorded as completed.

---

## 39. Initial Production Does Not Require a Separate GFC Chain

**Decision ID:** GFC-DEC-037  
**Status:** Canonical Working Decision

The initial production design does not require a separate GFC blockchain.

Base Mainnet remains the intended initial production environment.

A future appchain, rollup, or dedicated execution environment MAY be evaluated later.

This remains a future option, not a current production commitment.

---

## 40. Public Communication Before Production

**Decision ID:** GFC-DEC-038  
**Status:** Constraint

Public communication must distinguish between:

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

Planned infrastructure MUST NOT be presented as active production infrastructure.

---

# Open Decisions

## 41. Token Implementation Open Decisions

**Status:** Open

The following token decisions remain unresolved:

- exact production contract architecture;
- initial supply-creation method;
- upgradeability;
- pause functionality;
- burn functionality;
- recovery functionality;
- transfer restrictions, if any;
- buy/sell classification;
- recognized-pool administration;
- fee exemptions;
- fee destination;
- fee-proceeds use;
- and migration architecture.

---

## 42. Allocation and Custody Open Decisions

**Status:** Open

The following remain unresolved:

- production custody for each allocation;
- multisig or equivalent structures;
- signers;
- thresholds;
- timelocks;
- Guardian Growth mandate;
- Treasury Reserve detailed controls;
- Liquidity Reserve control structure;
- Ecosystem distribution rules;
- allocation recovery;
- and allocation migration.

---

## 43. Impact Vault Open Decisions

**Status:** Open

The following remain unresolved:

- production lock-start event;
- lock-start timestamp;
- exact time model;
- post-50-year behavior;
- full versus staged release;
- migration implementation;
- recovery;
- upgradeability;
- and final contract architecture.

---

## 44. Core Team Vesting Open Decisions

**Status:** Open

The following remain unresolved:

- vesting-start event;
- start timestamp;
- cliff;
- claim granularity;
- beneficiary structure;
- reassignment;
- succession;
- revocation;
- vested-but-unclaimed treatment;
- recovery;
- migration;
- and final contract architecture.

---

## 45. Staking Open Decisions

**Status:** Open

The following remain unresolved:

- principal-custody model;
- reward source;
- reward pool;
- reward rate;
- APR/APY methodology;
- reward duration;
- lock model;
- withdrawal rules;
- early exit;
- penalties;
- governance-related rights;
- community-related benefits;
- pause behavior;
- recovery;
- migration;
- upgradeability;
- and production activation criteria.

---

## 46. Presale Open Decisions

**Status:** Open

The following remain unresolved:

- exact USDC production address;
- exact DAI production address;
- pricing source;
- oracle architecture, if used;
- stale-price limits;
- rounding formulas;
- contribution limits;
- final eligibility model;
- exact immediate-distribution transaction ordering;
- failed-sale treatment of already distributed GFC;
- exact refund implementation;
- exact refund amount rule;
- contribution custody architecture;
- proceeds destination;
- withdrawal authority;
- unsold-GFC treatment;
- pause-duration behavior;
- cancellation behavior;
- recovery;
- migration;
- and final immutable/configurable boundary.

---

## 47. Governance Open Decisions

**Status:** Open

The following remain unresolved:

- final governance model;
- final role hierarchy;
- multisig platform, if used;
- signer count;
- approval thresholds;
- timelock durations;
- voting eligibility;
- voting weight;
- quorum;
- proposal threshold;
- veto;
- delegation;
- execution model;
- emergency process;
- and relationship between technical and legal authority.

No value SHOULD be invented for these fields before a project decision is made.

---

## 48. Transparency Registry Open Decisions

**Status:** Open

The following remain unresolved:

- final registry architecture;
- entity eligibility;
- admission criteria;
- evidence schema;
- claim schema;
- status vocabulary;
- reviewer model;
- verification-status rules;
- downgrade criteria;
- suspension criteria;
- removal criteria;
- appeals;
- dispute handling;
- historical-retention implementation;
- anchoring mechanism;
- protected-evidence storage;
- and final production authority model.

---

## 49. Security Open Decisions

**Status:** Open

The following remain unresolved:

- final production security architecture;
- key-management requirements;
- multisig security model;
- monitoring providers;
- alerting architecture;
- incident severity model;
- recovery process;
- exact independent-review scope;
- audit requirement and timing;
- and production security acceptance criteria.

---

# Decision Change Management

## 50. Material Decision Change

A change is material if it affects:

- product focus;
- production network;
- total supply;
- allocation amounts;
- fee model;
- staking inflation model;
- Presale price;
- Presale duration;
- Presale soft cap;
- Presale allocation;
- payment assets;
- token-delivery model;
- refund rights;
- Impact Vault lock;
- Core Team vesting;
- governance authority;
- production authority;
- Transparency Registry philosophy;
- or another participant-facing or security-critical commitment.

Material changes SHOULD be explicitly recorded in this file and reflected in all affected specifications.

---

## 51. No Silent Reversal

A canonical decision MUST NOT be silently reversed through:

- a single specification edit;
- frontend copy;
- marketing text;
- social media;
- implementation convenience;
- or operational practice.

A material reversal requires:

- explicit decision;
- rationale;
- affected-document review;
- security impact review where applicable;
- governance impact review where applicable;
- participant-rights review where applicable;
- and repository-wide consistency updates.

---

## 52. Superseded Decisions

When a material decision is replaced, the prior decision SHOULD remain historically identifiable.

A superseding record SHOULD identify:

- prior decision;
- new decision;
- effective date;
- rationale;
- affected components;
- migration impact;
- and public-communication impact.

Historical decisions SHOULD NOT be deleted solely because they are no longer current.

---

## 53. Relationship to CHANGELOG

Material project-decision changes SHOULD later be reflected in [`CHANGELOG.md`](CHANGELOG.md).

`DECISIONS.md` records what the current project decision is.

`CHANGELOG.md` records how the repository changed over time.

The two documents serve different purposes.

---

## 54. Relationship to ROADMAP

[`ROADMAP.md`](ROADMAP.md) records planned sequencing.

A roadmap milestone is not automatically a decision that the underlying implementation is ready.

`DECISIONS.md` records current architectural, economic, governance, and product choices.

`ROADMAP.md` records intended timing and progression.

---

## 55. Relationship to DEPLOYMENTS

[`DEPLOYMENTS.md`](DEPLOYMENTS.md) records actual deployment state.

A decision to deploy on Base Mainnet does not mean deployment has occurred.

A decision to use a 1% sell fee does not mean a live contract currently applies that fee.

A decision to use immediate Presale distribution does not mean a live Presale currently exists.

Deployment state must be authenticated separately.

---

## 56. Current Decision Summary

The current repository is governed by the following high-level decisions:

1. **Global Foundation Coin** is the current project identity.
2. **GFC Token / Economic Layer** is the current primary product focus.
3. The long-term direction is broader **Accountability Infrastructure**.
4. The canonical accountability model is:
   **Funds → Authority → Rules → Decisions → Outcomes → Evidence**.
5. The intended initial production network is **Base Mainnet**.
6. The public Base Sepolia `tGFC` deployment is a **non-production pilot**.
7. Production GFC uses a fixed intended supply of **1,000,000,000 GFC**.
8. The current seven-category allocation model totals 100%.
9. Impact Vault is intended for **250,000,000 GFC / 50-year lock**.
10. Core Team is intended for **50,000,000 GFC / 19-year linear vesting**.
11. Current intended token fees are **0% buy / 1% sell**.
12. Staking direction is **hybrid and non-inflationary**.
13. Presale Draft parameters are **€0.05 / 8 weeks / €250,000 soft cap / no separate monetary hard cap / 150,000,000 GFC**.
14. Intended Presale payment assets are **ETH, USDC, and DAI on Base**.
15. Current Presale token delivery is **Immediate Distribution**.
16. Failed-sale refund rights remain part of the current Presale design.
17. The treatment of already distributed GFC after failed finalization remains **unresolved and blocks production activation**.
18. Material Presale logic is intended to be immutable after production deployment.
19. The Transparency Registry is intended as **versioned history, not a permanent approval badge**.
20. Governance must preserve explicit authority, least privilege, separation, bounded exceptions, and reviewability.
21. Pilot authority does not become production authority automatically.
22. `main` is not automatically a production release.
23. No official Base Mainnet GFC token or live Presale currently exists.

---

## 57. Final Decision Principle

The GFC repository must distinguish clearly between:

**Decided → Specified → Implemented → Tested → Reviewed → Deployed → Operational**

and:

**Open → Unresolved → Not Deployed**

A decision is not a deployment.

A Draft is not a production release.

A roadmap date is not a launch guarantee.

A pilot is not production.

An unresolved issue must remain unresolved until a real project decision is made.

The purpose of this register is to keep GFC internally consistent while allowing the project to evolve through explicit, reviewable decisions rather than silent assumption drift.

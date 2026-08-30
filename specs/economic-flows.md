# GFC Economic Flows Specification

**Document ID:** GFC-ECO-001  
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

This document defines the current intended economic-flow model for Global Foundation Coin (GFC).

It is normative because it defines intended requirements and boundaries concerning:

- movement of GFC between economic components;
- movement of presale payment assets;
- sell-fee collection;
- allocation movement;
- custody transitions;
- lock and vesting releases;
- treasury flows;
- liquidity flows;
- staking reward flows;
- economic accounting;
- reconciliation;
- and economic-flow disclosure.

Its maturity remains Draft.

At the current repository state:

- the **GFC Token / Economic Layer** is the current primary product focus;
- a public GFC pilot exists on **Base Sepolia**;
- no production GFC token is deployed on Base Mainnet;
- no GFC presale is live;
- no production Treasury Reserve flow is active;
- no production Liquidity Reserve flow is established as official;
- no production staking system is operational;
- no production sell-fee destination is finalized;
- no production staking reward source is finalized;
- no production allocation-flow contracts are established as official;
- and no economic-flow implementation is designated as conforming.

The Base Sepolia pilot MUST NOT be interpreted as evidence that the production economic flows described in this document are deployed or active.

Current deployment and operational status is maintained in [`../STATUS.md`](../STATUS.md).

---

## 2. Purpose

The purpose of this specification is to define how value may move through the intended GFC Economic Layer without confusing:

- allocation with expenditure;
- custody with ownership;
- transfer with authorization;
- vesting with payment;
- fee collection with fee use;
- presale contribution with unrestricted proceeds;
- liquidity provision with permanent liquidity;
- staking rewards with newly issued supply;
- or on-chain movement with verified outcome or impact.

The specification is intended to make economic flows:

- explicit;
- bounded;
- reconcilable;
- attributable;
- historically reviewable;
- and consistent with the fixed-supply model.

This document does not create production wallets, production contracts, production authorities, or production payment routes.

Those require authenticated implementation and deployment records.

---

## 3. Relationship to the GFC Accountability Model

The long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

Economic flows primarily describe the movement and state of **Funds**.

However, a conforming economic-flow record SHOULD also identify:

1. the value being moved;
2. the responsible authority;
3. the applicable rule;
4. the decision authorizing the flow;
5. the resulting transaction or state change;
6. the resulting economic classification;
7. and the evidence supporting that representation.

A transaction record alone does not prove:

- proper authority;
- compliant purpose;
- correct use;
- successful outcome;
- or impact.

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

This specification defines economic-flow requirements for:

- the fixed GFC supply;
- initial allocations;
- ordinary token transfers;
- buy and sell fee flows;
- fee custody and later use;
- Impact Vault flows;
- Guardian Growth flows;
- Presale flows;
- Treasury Reserve flows;
- Liquidity Reserve flows;
- Ecosystem flows;
- Core Team vesting and claim flows;
- staking reward flows;
- migration flows;
- recovery flows;
- accounting boundaries;
- reconciliation;
- public economic-flow records;
- and production conformance.

---

## 6. Out of Scope

This document does not independently define:

- final production addresses;
- final contract code;
- final multisig configuration;
- final signer identities;
- final fee destination;
- final fee-proceeds use;
- final staking reward source;
- final treasury budget categories;
- final liquidity venues;
- final market-making arrangements;
- final presale oracle or pricing mechanism;
- final legal ownership;
- final accounting standard;
- tax treatment;
- regulatory treatment;
- or impact methodology.

These matters MUST be defined by the applicable specifications, policies, legal documentation, or authenticated production records before production reliance where relevant.

---

## 7. Economic Layer Overview

The intended GFC Economic Layer includes the following major economic components:

1. **GFC Token**
2. **Impact Vault**
3. **Guardian Growth**
4. **Presale**
5. **Treasury Reserve**
6. **Liquidity Reserve**
7. **Ecosystem**
8. **Core Team**
9. **Sell-Fee Flow**
10. **Staking**
11. **External payment assets**
12. **Production custody and settlement mechanisms**

These components are related but MUST remain economically distinguishable.

Movement between components MUST NOT silently redefine the purpose or restriction of the originating value.

---

## 8. Fixed-Supply Boundary

The intended canonical GFC supply is:

```text
1,000,000,000 GFC
```

No economic flow MAY create additional canonical GFC beyond the fixed supply.

Economic activity MUST NOT use:

- fee accounting;
- staking rewards;
- migration;
- replacement contracts;
- bridge representations;
- treasury accounting;
- or internal credits

as hidden methods of increasing canonical GFC supply.

The fixed-supply requirements are defined in [`token.md`](token.md).

---

## 9. Initial Allocation Boundary

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

Economic flows MUST preserve reconciliation to this fixed-supply boundary unless an applicable breaking versioned specification explicitly changes the allocation model before production deployment.

The allocation specification is defined in [`allocations.md`](allocations.md).

---

## 10. Economic State Versus Economic Flow

An economic **state** and an economic **flow** MUST NOT be treated as equivalent.

### 10.1 Economic state

Examples include:

- allocated;
- locked;
- unvested;
- vested;
- claimable;
- held in treasury;
- held in liquidity reserve;
- held for staking rewards;
- held as refundable contribution assets;
- or held as finalized proceeds.

### 10.2 Economic flow

Examples include:

- transfer;
- release;
- claim;
- contribution;
- refund;
- fee collection;
- treasury payment;
- liquidity deployment;
- liquidity withdrawal;
- staking reward distribution;
- or migration.

A balance may exist without an active flow.

A flow may change economic state without changing total supply.

---

## 11. Flow Classification

Every material production economic flow SHOULD be classifiable by:

- source asset;
- source component;
- destination asset;
- destination component;
- amount;
- authority;
- applicable rule;
- transaction or settlement mechanism;
- economic purpose;
- resulting classification;
- and supporting evidence.

Where a flow changes classification, the reason and authority SHOULD be reviewable.

---

## 12. Custody Is Not Economic Purpose

Custody location does not determine economic purpose by itself.

A wallet or contract may technically hold assets without proving:

- beneficial ownership;
- allocation purpose;
- authorized use;
- approved spending;
- or impact.

A transfer to a wallet labeled `Treasury`, `Impact`, `Liquidity`, or another purpose-specific name MUST NOT be treated as sufficient evidence of compliant economic use.

---

## 13. Allocation Movement

A movement of GFC from one allocation to another MUST NOT occur merely through informal accounting.

Where reclassification is permitted, the flow MUST identify:

- originating allocation;
- destination allocation;
- amount;
- authority;
- reason;
- applicable versioned rule;
- effect on allocation accounting;
- effect on restrictions;
- and transaction evidence.

Reclassification MUST NOT:

- create duplicate allocation capacity;
- bypass locks;
- bypass vesting;
- conceal spending;
- or weaken participant rights.

---

# Token Transfer and Fee Flows

## 14. Ordinary Token Transfers

Ordinary GFC transfers move existing GFC between addresses.

An ordinary transfer:

- does not create new supply;
- does not automatically change the normative allocation classification;
- does not automatically prove authorized purpose;
- and does not automatically establish a buy or sell.

The final token implementation MUST define how ordinary transfers are distinguished from fee-bearing trading transactions.

---

## 15. Buy Flow

The current intended GFC token buy fee is:

```text
0%
```

A buy flow under the current token model therefore MUST NOT route a positive GFC token fee to a project-controlled fee destination.

This requirement does not eliminate:

- Base network gas;
- decentralized-exchange fees;
- liquidity-provider fees;
- router fees;
- or other third-party costs.

These external costs are distinct from the GFC token fee.

---

## 16. Sell Flow

The current intended GFC token sell fee is:

```text
1%
```

A production sell flow MUST define the exact sequence used to calculate and route the fee.

The implementation MUST document:

- gross GFC amount;
- fee basis;
- fee calculation;
- rounding;
- net amount;
- fee amount;
- fee destination;
- transaction classification;
- and any applicable exemptions.

The sell-fee flow MUST be deterministic and testable.

---

## 17. Sell-Fee Collection

Sell-fee collection transfers part of an existing GFC balance.

It does not mint additional GFC.

The production implementation MUST ensure that:

```text
gross sell amount
=
net transferred amount
+
GFC token fee
```

subject to the finalized calculation and rounding rules.

The exact technical formula remains unresolved until the token classification and fee implementation are finalized.

---

## 18. Sell-Fee Destination

The final production sell-fee destination is unresolved.

This document MUST NOT be interpreted as assigning sell-fee proceeds to:

- Impact Vault;
- Guardian Growth;
- Treasury Reserve;
- Liquidity Reserve;
- Ecosystem;
- staking rewards;
- burn;
- or any other component.

Before production deployment, the applicable specifications MUST define:

- receiving address or contract;
- custody;
- authority;
- accounting classification;
- whether the destination is changeable;
- and later permissible flows.

A production implementation MUST NOT route fees to an undocumented destination.

---

## 19. Fee-Proceeds Use

The final use of sell-fee proceeds is unresolved.

Collected fee GFC MAY only be used according to a later explicitly specified economic-flow rule.

Potential use MUST NOT be inferred from:

- wallet label;
- public narrative;
- marketing statement;
- or historical intention.

Any use of fee proceeds MUST preserve the fixed-supply model.

Fee proceeds MUST NOT be represented as impact funding unless their actual allocation, authority, use, and evidence support that claim.

---

## 20. Fee Conversion

Whether sell-fee GFC may be converted into another asset is unresolved.

If conversion is later permitted, the applicable specification MUST define:

- who may initiate conversion;
- permitted venues;
- permitted destination assets;
- slippage controls;
- execution authority;
- market-impact considerations;
- accounting treatment;
- and reporting.

A conversion flow MUST NOT be used for undisclosed market manipulation.

---

## 21. Fee Exemption Flows

If fee exemptions are implemented, exempt transfers MUST remain distinguishable from standard fee-bearing flows.

The production record SHOULD make it possible to determine:

- which address was exempt;
- which fee category was affected;
- the effective period;
- authority;
- and reason.

An exemption MUST NOT create hidden economic advantage without disclosure.

---

# Impact Vault Flows

## 22. Impact Vault Funding

The intended Impact Vault allocation is:

```text
250,000,000 GFC
```

The initial production allocation flow MUST reconcile this amount to the authenticated Impact Vault custody mechanism.

Initial funding of the Impact Vault is not an impact expenditure.

It is an allocation and custody event.

---

## 23. Impact Vault Locked State

While the 50-year restriction applies, the locked principal MUST NOT flow into unrestricted custody through an undocumented path.

The exact lock-start and lock-end rules remain unresolved and are defined in [`vesting-and-unlocks.md`](vesting-and-unlocks.md).

A balance movement caused by security migration MUST preserve or strengthen the remaining restriction.

---

## 24. Impact Vault Release Flow

No production Impact Vault release flow is currently finalized.

Before production Stable status, the applicable specification MUST define:

- when release becomes eligible;
- whether release is full or staged;
- who or what initiates release;
- destination;
- retained restrictions;
- economic classification;
- and post-release authority.

The existence of a future release right does not authorize early movement.

---

## 25. Impact Vault Use-of-Funds Flow

If GFC or proceeds associated with the Impact Vault are later used for a documented purpose, the economic record SHOULD distinguish:

1. release from long-term restriction;
2. transfer to an authorized spending or settlement component;
3. actual payment;
4. use-of-funds evidence;
5. output or outcome evidence;
6. and any impact claim.

A release is not equivalent to verified use.

A transfer is not equivalent to verified impact.

---

# Guardian Growth Flows

## 26. Guardian Growth Funding

The intended Guardian Growth allocation is:

```text
200,000,000 GFC
```

Initial allocation MUST be distinguishable from later release, spending, grant, incentive, partnership, or transfer flows.

No production Guardian Growth use model is currently finalized.

---

## 27. Guardian Growth Outflows

Before production use, the applicable specification MUST define:

- permitted categories;
- approval authority;
- release conditions;
- destination restrictions where applicable;
- accounting classification;
- and evidence requirements.

Guardian Growth MUST NOT become unrestricted discretionary inventory merely because no lock schedule is currently specified.

---

# Presale Flows

## 28. Presale Economic Boundary

No GFC presale is currently live.

The current Draft presale design includes:

- reference price: **€0.05 per GFC**;
- intended duration: **8 weeks**;
- soft cap: **€250,000**;
- no separate monetary hard cap;
- maximum Presale allocation: **150,000,000 GFC**;
- intended payment assets: **ETH, USDC, and DAI on Base**;
- immediate GFC distribution as the current design direction;
- refunds if the applicable soft-cap success condition is not satisfied;
- and immutable material sale logic as the current design direction.

These are Draft parameters and MUST NOT be represented as a live economic system.

---

## 29. Presale Contribution Flow

A valid presale contribution flow is intended to move an accepted payment asset from an eligible participant into the applicable presale custody or settlement mechanism.

The final implementation MUST define:

- supported asset contract addresses;
- accepted amount;
- reference valuation;
- contribution record;
- participant;
- corresponding GFC amount;
- and state transition.

The payment-asset flow and GFC distribution flow MUST remain reconcilable.

---

## 30. Supported Presale Payment Assets

The current Draft design intends support for:

- **ETH**
- **USDC**
- **DAI**

on Base.

The production implementation MUST authenticate exact network-specific asset identifiers and contract addresses where applicable.

A token with the same symbol on another network or from another contract MUST NOT be accepted as equivalent solely by name.

---

## 31. Presale Pricing Flow

Where an accepted crypto asset is valued against the euro reference price, the production system MUST define:

- pricing source;
- timestamp;
- decimals;
- rounding;
- stale-price limits;
- unavailable-price behavior;
- and calculation order.

Pricing rules MUST be deterministic and reviewable.

The final pricing methodology remains unresolved.

---

## 32. Immediate GFC Distribution

The current Draft design direction uses **immediate token distribution**.

For a valid purchase, the economic flow is intended to include:

1. acceptance of the participant's payment asset;
2. calculation of the applicable GFC amount;
3. participant purchase accounting;
4. immediate transfer of the applicable GFC amount;
5. reduction of remaining Presale allocation capacity;
6. and preservation of the contribution record.

The exact atomicity and technical transaction sequence remain implementation decisions.

A production presale MUST NOT distribute more than:

```text
150,000,000 GFC
```

in aggregate from the Presale allocation.

---

## 33. Presale Allocation Accounting

At any time, the production accounting SHOULD permit reconciliation of:

```text
Presale allocation
=
GFC distributed
+
GFC remaining
+
any explicitly defined exceptional accounting state
```

subject to the final specification.

No exceptional state MAY create duplicate entitlement or additional canonical supply.

---

## 34. Presale Contribution Custody

Accepted payment assets MUST remain subject to the applicable presale success, refund, and withdrawal rules.

Project operators MUST NOT treat all accepted contribution assets as unrestricted project proceeds immediately upon receipt if valid refund rights remain active.

The custody model MUST preserve the ability to satisfy valid refunds.

---

## 35. Soft-Cap Accounting

The production presale MUST define how accepted contributions are counted toward the:

```text
€250,000 soft cap
```

The calculation MUST distinguish:

- accepted contributions;
- rejected contributions;
- invalid contributions;
- refunded contributions where relevant;
- and any other explicitly specified state.

The final euro-reference accounting methodology remains unresolved.

---

## 36. Reaching the Soft Cap

Reaching the soft cap before the presale ends MUST NOT automatically be interpreted as:

- presale completion;
- finalization;
- unrestricted withdrawal rights;
- or termination of all refund rights

unless the final applicable presale specification explicitly establishes that result.

---

## 37. Successful Presale Proceeds Flow

The final conditions under which accepted payment assets become withdrawable as successful presale proceeds MUST be defined in [`presale.md`](presale.md).

A conforming flow MUST identify:

- success condition;
- finalization state;
- withdrawal authority;
- destination;
- amount by payment asset;
- approval requirements;
- and transaction evidence.

This document does not establish a production proceeds destination.

---

## 38. Failed Presale Refund Flow

If the applicable presale fails the soft-cap success condition, eligible participants MUST retain the refund rights defined by the applicable presale specification.

Refund flows MUST return the applicable accepted contribution assets according to the production accounting model.

Project authority MUST NOT redirect refundable assets to:

- treasury;
- liquidity;
- operations;
- staking;
- impact activities;
- or another use.

---

## 39. Immediate Distribution and Failed Finalization

The combination of:

- immediate GFC distribution; and
- refund rights after failed finalization

creates a material unresolved economic interaction.

The final presale specification MUST define the economic and technical treatment of GFC already distributed to a participant if the presale fails.

This document does not invent or authorize:

- clawback;
- forced transfer;
- forced burn;
- mandatory token return;
- token invalidation;
- replacement token;
- negative balance;
- or another corrective mechanism.

A production presale MUST NOT activate while this interaction remains undefined.

---

## 40. Unsold Presale GFC

The treatment of unsold Presale GFC remains unresolved.

The final production rule MUST define:

- amount determination;
- timing;
- custody;
- destination or continued classification;
- authority;
- supply impact;
- and public reporting.

Unsold GFC MUST NOT be reassigned opportunistically after the sale result is known without a predefined applicable rule.

---

# Treasury Reserve Flows

## 41. Treasury Reserve Funding

The intended Treasury Reserve allocation is:

```text
150,000,000 GFC
```

Initial allocation to Treasury Reserve custody is not itself treasury spending.

The economic system MUST distinguish:

- allocation;
- custody;
- approved budget;
- payment;
- reconciliation;
- and outcome.

---

## 42. Treasury Outflows

A material Treasury Reserve outflow SHOULD identify:

- purpose;
- proposal or authorization;
- amount;
- asset;
- recipient;
- applicable authority;
- transaction;
- accounting category;
- and evidence.

Treasury flow requirements MUST remain consistent with [`governance-constraints.md`](governance-constraints.md).

---

## 43. Treasury Asset Conversion

Whether Treasury Reserve GFC may be converted into other assets, and under what conditions, remains unresolved.

If permitted, the applicable specification MUST define:

- authorized venues;
- authority;
- limits;
- slippage controls;
- accounting treatment;
- custody destination;
- and reporting.

Treasury conversion MUST NOT be used for undisclosed price manipulation.

---

## 44. Treasury Recipient Flow

A Treasury Reserve payment to a recipient MUST NOT be treated as final proof of use.

Where relevant, records SHOULD distinguish:

- authorization;
- payment;
- receipt;
- use of funds;
- delivery;
- reconciliation;
- and outcome.

Protected recipient information MAY remain non-public where justified.

---

# Liquidity Reserve Flows

## 45. Liquidity Reserve Funding

The intended Liquidity Reserve allocation is:

```text
150,000,000 GFC
```

Initial allocation to Liquidity Reserve custody is not equivalent to deployed market liquidity.

---

## 46. Liquidity Deployment Flow

Before production liquidity deployment, the applicable specification MUST define:

- venue;
- pair;
- GFC amount;
- paired asset;
- paired-asset source;
- initial price-setting methodology;
- liquidity-provider position ownership;
- custody;
- and withdrawal authority.

Liquidity deployment MUST be publicly distinguishable from Liquidity Reserve balance.

---

## 47. Paired-Asset Flow

The source of any non-GFC asset paired with GFC for liquidity MUST be documented.

A liquidity pair may require assets such as ETH or stablecoins.

This document does not establish the final paired asset, amount, or funding source.

Paired-asset funding MUST NOT be silently sourced from refundable presale contributions before those assets become validly withdrawable under the presale rules.

---

## 48. Liquidity-Provider Position

A liquidity-provider position is an economic asset.

The production model MUST define:

- who or what owns the position;
- who may withdraw it;
- who receives trading fees;
- whether the position is locked;
- and how the position is accounted for.

A liquidity-provider position MUST NOT be represented as permanently locked unless technical restrictions support that claim.

---

## 49. Liquidity Withdrawal Flow

Any production liquidity withdrawal MUST identify:

- authority;
- amount;
- venue;
- assets received;
- destination;
- reason;
- and resulting reserve classification.

Liquidity withdrawal authority is a material economic and governance authority.

---

## 50. Trading-Fee Flow

Trading fees generated by external liquidity venues are distinct from the GFC token's 1% sell fee.

The production accounting model MUST distinguish:

- GFC token fee proceeds;
- decentralized-exchange or liquidity-provider fees;
- and other third-party revenue or rebates.

These flows MUST NOT be combined in reporting without explanation.

---

# Ecosystem Flows

## 51. Ecosystem Funding

The intended Ecosystem allocation is:

```text
50,000,000 GFC
```

Initial allocation MUST be distinguished from later:

- grants;
- incentives;
- development payments;
- partnership distributions;
- infrastructure payments;
- marketing-related distributions;
- or other approved uses.

---

## 52. Ecosystem Outflows

Before production use, the applicable specification MUST define permitted economic categories and approval requirements.

Material Ecosystem outflows SHOULD identify:

- category;
- recipient;
- amount;
- authority;
- milestone or condition where applicable;
- transaction;
- and reporting requirement.

Ecosystem flows MUST NOT be used for undisclosed insider distributions.

---

# Core Team Flows

## 53. Core Team Allocation

The intended Core Team allocation is:

```text
50,000,000 GFC
```

subject to:

```text
19-year linear vesting
```

Initial allocation into a vesting mechanism is not equivalent to immediate team compensation.

---

## 54. Vesting State Versus Economic Flow

Vesting changes entitlement state over time.

Vesting itself does not necessarily move tokens.

The production system SHOULD distinguish:

- unvested amount;
- vested amount;
- vested but unclaimed amount;
- claimed amount;
- and transferred amount.

The detailed vesting rules are defined in [`vesting-and-unlocks.md`](vesting-and-unlocks.md).

---

## 55. Core Team Claim Flow

A Core Team claim or release flow MUST NOT exceed the amount vested under the applicable schedule.

The final production model MUST define:

- claimant;
- beneficiary;
- amount;
- destination;
- calculation;
- fee treatment;
- and transaction record.

A claim MUST NOT create additional supply.

---

## 56. Core Team Transfer After Claim

Once GFC has been validly claimed under the applicable vesting rules, subsequent holder transfers are ordinary token movements unless another rule applies.

A claimed-token transfer MUST NOT be represented as a vesting release if the vesting release occurred earlier.

---

# Staking Flows

## 57. Staking Economic Boundary

No production GFC staking system is currently operational.

The current intended staking design direction is:

**hybrid and non-inflationary**

The staking specification is defined separately in [`staking.md`](staking.md).

---

## 58. Staking Principal Flow

If staking is implemented, the production specification MUST define whether staking principal is:

- transferred into a staking contract;
- locked under user ownership;
- represented through another accounting method;
- or managed through another explicitly specified mechanism.

Staking principal MUST NOT be confused with staking rewards.

---

## 59. Staking Reward Source

The final staking reward source is unresolved.

Staking rewards MUST NOT be created through additional GFC inflation under the current fixed-supply model.

The reward source MUST therefore come from:

- GFC already included in the fixed supply;
- or another explicitly specified non-minting economic source.

This document does not assign staking rewards to:

- Ecosystem;
- Guardian Growth;
- Treasury Reserve;
- sell-fee proceeds;
- or any other specific component.

That decision remains unresolved.

---

## 60. Staking Reward Flow

A production staking reward flow MUST define:

- reward source;
- reward custody;
- eligibility;
- calculation;
- accrual;
- claim or distribution mechanism;
- maximum distributable amount;
- authority;
- and reconciliation.

The accounting MUST ensure that reward distributions do not exceed available authorized reward assets.

---

## 61. Staking Yield Communication

A displayed reward rate, APR, APY, or equivalent metric MUST NOT be represented as guaranteed.

The economic record SHOULD identify the assumptions underlying any displayed rate.

Staking rewards are token distributions or economic benefits, not newly created value guaranteed by the protocol.

---

## 62. Locked or Unvested GFC and Staking

GFC subject to the Impact Vault lock or Core Team vesting MUST NOT enter a staking flow that defeats the original restriction.

If restricted GFC is later allowed to participate in staking, the applicable specifications MUST define:

- principal custody;
- reward ownership;
- withdrawal restrictions;
- governance implications;
- and preservation of the original lock or vesting schedule.

---

# Migration and Recovery Flows

## 63. Migration Flow

A migration moves assets or economic state from one authenticated component to a successor.

Migration MUST NOT create:

- duplicate supply;
- duplicate entitlement;
- duplicate allocation capacity;
- weakened lock restrictions;
- weakened vesting restrictions;
- or hidden economic reclassification.

Migration accounting MUST reconcile source and destination states.

---

## 64. Migration Accounting

A migration record SHOULD identify:

- source;
- destination;
- asset;
- amount;
- pre-migration classification;
- post-migration classification;
- authority;
- transaction;
- preserved restrictions;
- and known deviations.

Where source assets remain technically accessible after migration, the economic model MUST prevent double counting.

---

## 65. Recovery Flow

Recovery is not ordinary spending.

A recovery flow MUST identify:

- triggering condition;
- affected asset;
- source;
- destination;
- authority;
- approvals;
- preserved economic restrictions;
- and resulting classification.

Recovery MUST NOT become a hidden bypass around allocation, vesting, lock, or custody rules.

---

# Accounting and Reconciliation

## 66. Economic Accounting Principles

Production economic accounting SHOULD distinguish:

- asset ownership or custody;
- normative allocation;
- current balance;
- restricted balance;
- available balance;
- distributed amount;
- spent amount;
- refundable amount;
- finalized proceeds;
- outstanding liability;
- and migrated amount.

These categories MUST NOT be collapsed where doing so would create a materially misleading representation.

---

## 67. On-Chain and Off-Chain Reconciliation

Where an economic flow has both on-chain and off-chain elements, reconciliation SHOULD link:

- on-chain transaction;
- accounting record;
- authority;
- purpose;
- supporting evidence;
- and status.

An off-chain record MUST NOT override authenticated on-chain execution.

An on-chain transaction MUST NOT independently establish off-chain purpose.

---

## 68. Payment-Asset Accounting

Presale, treasury, liquidity, or other economic flows MAY involve assets other than GFC.

Production records MUST identify the actual asset and not normalize materially different assets into one balance without explaining the valuation methodology.

Where euro-reference values are used, the methodology and timestamp MUST be documented.

---

## 69. Double-Counting Prohibition

Economic reporting MUST NOT count the same value simultaneously as separate independent assets or outcomes where doing so materially overstates:

- treasury value;
- allocation availability;
- presale capacity;
- staking reward capacity;
- liquidity;
- or impact funding.

Internal transfers between GFC-controlled components MUST NOT be represented as new external inflows.

---

## 70. Internal Transfers

An internal transfer between GFC-controlled wallets or contracts changes custody or classification.

It does not automatically create:

- revenue;
- expenditure;
- external funding;
- impact;
- or economic gain.

Public reporting SHOULD distinguish internal movement from external inflow or outflow.

---

## 71. External Inflows

External inflows MAY include:

- presale contributions;
- donations where separately established;
- grants;
- third-party funding;
- trading fees;
- or other external transfers.

This specification does not establish any external inflow as active except where separately authenticated.

External inflows MUST be classified according to their actual legal and economic nature.

---

## 72. External Outflows

External outflows MAY include:

- treasury payments;
- grants;
- vendor payments;
- liquidity deployment;
- refunds;
- or other approved transfers.

The economic classification MUST distinguish outflow purpose from mere transaction direction.

---

## 73. Liabilities and Restricted Assets

An asset held by a GFC-controlled mechanism MAY still be economically restricted or associated with an obligation.

Examples may include:

- refundable presale contributions;
- vested but unclaimed entitlement;
- contractually restricted funds;
- or assets pending settlement.

Possession MUST NOT be represented as unrestricted project ownership where a valid obligation exists.

---

## 74. Reconciliation Frequency

The final production reconciliation frequency remains unresolved.

Material production economic components SHOULD be reconcilable at a frequency appropriate to their risk and activity.

High-value or participant-facing flows SHOULD support timely reconciliation.

---

## 75. Reconciliation Exceptions

A reconciliation difference MUST NOT be silently written off.

Material differences SHOULD be classified as:

- timing difference;
- rounding difference;
- pending transaction;
- failed transaction;
- incorrect classification;
- accounting defect;
- unauthorized flow;
- or other documented category.

Material unexplained differences MAY constitute an incident.

---

# Authority and Governance

## 76. Economic Authority

Authority over economic flows MUST be consistent with [`roles-and-authority.md`](roles-and-authority.md).

Material economic authority MAY include:

- allocation release;
- treasury proposal;
- treasury approval;
- treasury execution;
- fee administration;
- liquidity deployment;
- liquidity withdrawal;
- presale withdrawal;
- refund administration;
- staking reward administration;
- migration;
- and recovery.

No material economic authority may remain undocumented.

---

## 77. Separation of Economic Duties

Where reasonably possible, the production model SHOULD separate:

- proposal;
- approval;
- execution;
- custody;
- accounting;
- reconciliation;
- and evidence review.

Where one actor holds multiple functions, the concentration MUST be disclosed.

---

## 78. Economic Governance

Economic governance MUST NOT silently:

- expand total supply;
- reassign locked value;
- accelerate vesting;
- eliminate refund rights;
- redirect refundable assets;
- create undisclosed fee destinations;
- or convert one allocation into unrestricted inventory.

Governance constraints are defined in [`governance-constraints.md`](governance-constraints.md).

---

# Security

## 79. Economic-Flow Security

Economic-flow security MUST consider:

- unauthorized transfer;
- duplicate accounting;
- incorrect decimals;
- rounding;
- reentrancy;
- malicious token behavior;
- wrong-network assets;
- wrong-address transfers;
- price manipulation;
- stale pricing;
- refund insolvency;
- liquidity withdrawal;
- reward insolvency;
- migration duplication;
- and compromised authority.

Detailed security requirements are defined in [`security-model.md`](security-model.md).

---

## 80. Economic Invariants

The following high-level invariants apply.

### 80.1 Fixed supply

```text
canonical GFC supply ≤ 1,000,000,000 GFC
```

### 80.2 Allocation reconciliation

Initial allocation MUST reconcile to:

```text
1,000,000,000 GFC
```

### 80.3 Presale ceiling

Aggregate Presale distribution MUST NOT exceed:

```text
150,000,000 GFC
```

### 80.4 Core Team

Core Team claims MUST NOT exceed vested entitlement.

### 80.5 Impact Vault

Locked Impact Vault principal MUST NOT become unrestricted before valid release eligibility.

### 80.6 Staking

Staking rewards MUST NOT require additional GFC inflation.

### 80.7 Refund availability

Assets required to satisfy valid refund rights MUST remain available under the applicable presale rules.

### 80.8 Migration

Migration MUST NOT duplicate canonical economic claims.

---

# Transparency and Evidence

## 81. Economic-Flow Transparency

Material production economic flows SHOULD be reviewable through a combination of:

- authenticated on-chain data;
- allocation records;
- governance records;
- accounting records;
- supporting evidence;
- and historical status.

A public transaction alone is incomplete context.

---

## 82. Transparency Registry Relationship

The planned Transparency Registry MAY later record economic-flow relationships such as:

- allocation;
- custody;
- authority;
- transfer;
- purpose;
- evidence;
- correction;
- dispute;
- and historical status.

The Registry is intended to operate as a versioned historical record rather than a permanent approval badge.

No complete production Transparency Registry is currently deployed.

A Registry record MUST NOT override authenticated settlement state.

---

## 83. Use-of-Funds Distinction

Economic-flow transparency MUST preserve the distinction between:

- transaction verification;
- use-of-funds verification;
- output verification;
- outcome evaluation;
- and impact evaluation.

A payment from Treasury Reserve or Impact Vault does not independently prove correct use.

---

## 84. Public Economic Claims

Public economic communication MUST NOT imply that:

- allocated tokens have already been spent;
- locked tokens are liquid;
- vested tokens are unvested;
- presale contributions are unrestricted proceeds before applicable conditions;
- fee collection proves fee use;
- liquidity reserve proves active market liquidity;
- staking rewards are inflationary when they are not;
- staking yields are guaranteed;
- or internal transfers represent new external funding.

---

# Pilot and Production Separation

## 85. Base Sepolia Pilot

The public Base Sepolia pilot is non-production.

Pilot token movements, balances, wallets, or test flows MUST NOT be represented as:

- production allocation flows;
- production treasury flows;
- production liquidity flows;
- production staking flows;
- production fee flows;
- or production presale settlement.

---

## 86. Production Economic Authentication

Before a production economic flow is represented as official, the applicable records SHOULD identify:

- production network;
- authenticated token contract;
- authenticated source;
- authenticated destination;
- asset;
- amount;
- authority;
- applicable specification;
- and transaction or settlement evidence.

---

# Conformance and Change Management

## 87. Conformance

An economic-flow implementation conforms to this specification only when:

- it identifies an applicable versioned specification;
- canonical GFC supply remains within the fixed-supply boundary;
- initial allocations reconcile;
- flows preserve applicable allocation restrictions;
- presale distribution remains within the Presale allocation;
- refund rights are economically supportable where applicable;
- staking remains non-inflationary;
- material authorities are disclosed;
- fee destinations and uses are not misrepresented;
- material flow classifications are accurate;
- production and pilot status remain separated;
- and material deviations are documented.

A wallet label, UI category, accounting label, or marketing statement does not establish conformance.

---

## 88. Economic Non-Conformance

Economic non-conformance includes:

- creation of additional canonical supply;
- duplicate allocation accounting;
- unauthorized allocation movement;
- early release of restricted GFC;
- Core Team distribution above vested entitlement;
- Presale distribution above 150,000,000 GFC;
- refundable assets made unavailable contrary to applicable rules;
- undisclosed fee destination;
- undisclosed fee use;
- inflation-funded staking contrary to the current design;
- duplicate migration claims;
- internal transfers reported as external inflows;
- pilot economic activity represented as production;
- or materially misleading economic classification.

Material non-conformance MAY require:

- reconciliation;
- correction;
- authority review;
- pause where applicable;
- refund remediation;
- migration;
- public clarification;
- security review;
- governance review;
- or incident treatment.

A specification MUST NOT be rewritten retrospectively merely to conceal economic non-conformance.

---

## 89. Change Classification

A material economic-flow change includes a change to:

- sell-fee destination;
- sell-fee use;
- Presale settlement;
- refund economic treatment;
- Treasury Reserve flow authority;
- Liquidity Reserve deployment or withdrawal authority;
- staking reward source;
- allocation reclassification;
- locked or vested token flow;
- migration treatment;
- or economic accounting that materially changes participant rights or represented value.

A breaking economic-flow change requires:

- explicit versioning;
- rationale;
- economic analysis;
- security analysis;
- governance analysis;
- participant-rights analysis;
- implementation analysis;
- migration analysis where relevant;
- and updated public communication.

---

## 90. Current Unresolved Requirements

The following matters remain unresolved unless separately established by a later versioned specification or authenticated implementation record.

### Token fee flows

- precise sell-fee calculation sequence;
- fee rounding;
- final fee destination;
- fee-destination mutability;
- fee-proceeds custody;
- final fee-proceeds use;
- and fee-conversion authority.

### Presale flows

- final pricing methodology;
- final supported-asset contract addresses;
- contribution custody implementation;
- finalization mechanics;
- successful-proceeds destination;
- withdrawal authority;
- refund implementation;
- treatment of already distributed GFC if finalization fails;
- and unsold Presale GFC treatment.

### Treasury flows

- detailed permitted-use categories;
- transaction thresholds;
- asset-conversion rules;
- recurring-payment rules;
- and final custody model.

### Liquidity flows

- final venue;
- final pair;
- paired-asset source;
- initial deployment amount;
- price-setting process;
- liquidity-provider position custody;
- lock status;
- withdrawal authority;
- rebalancing;
- and market-making arrangements.

### Guardian Growth and Ecosystem

- permitted economic categories;
- release schedules;
- approval models;
- recipient rules;
- and final custody.

### Core Team

- vesting start;
- claim mechanism;
- claim frequency;
- fee treatment;
- and beneficiary structure.

### Staking

- final reward source;
- reward custody;
- reward calculation;
- reward duration;
- maximum reward distribution;
- and relationship to other economic components.

### Shared accounting

- production accounting format;
- valuation methodology;
- reconciliation frequency;
- exception treatment;
- and economic-reporting schema.

These unresolved matters MUST NOT be represented as finalized production decisions.

---

## 91. Requirements Before Stable Status

This document MUST NOT be marked Stable until:

- sell-fee flow calculation is finalized;
- sell-fee destination is finalized;
- sell-fee use is finalized;
- allocation transfer and reclassification rules are finalized;
- Impact Vault release economics are finalized;
- Guardian Growth flow rules are finalized;
- Presale contribution accounting is finalized;
- Presale immediate distribution is fully specified;
- the immediate-distribution and failed-sale refund interaction is technically and economically resolved;
- successful presale proceeds flow is finalized;
- unsold Presale GFC treatment is finalized;
- Treasury Reserve flow rules are finalized;
- Liquidity Reserve flow rules are finalized;
- paired-asset funding rules are finalized;
- Ecosystem flow rules are finalized;
- Core Team claim economics are finalized;
- staking reward source is finalized;
- staking reward-flow accounting is finalized;
- migration and recovery flow rules are finalized;
- accounting and reconciliation requirements are finalized;
- economic-flow security invariants are mapped to the intended implementation;
- Base Sepolia pilot and Base Mainnet production economic terminology are consistently separated;
- and all related specifications are mutually consistent.

---

## 92. Related Specifications

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
- [`staking.md`](staking.md);
- [`presale.md`](presale.md);
- [`transparency-model.md`](transparency-model.md);
- and repository-level [`../STATUS.md`](../STATUS.md).

Where another Draft specification conflicts with this document, the conflict MUST be resolved explicitly before Stable status.

---

## 93. Final Economic-Flow Principles

The GFC Economic Layer preserves the following distinctions:

> Allocation is not expenditure.

> Custody is not unrestricted ownership.

> Vesting is not the same as transfer.

> Claiming is not the same as spending.

> Fee collection is not the same as fee use.

> Treasury allocation is not treasury expenditure.

> Liquidity Reserve is not active liquidity.

> A liquidity-provider position is itself an economic asset.

> Presale contribution is not automatically unrestricted project proceeds.

> Immediate token distribution does not eliminate refund-accounting obligations.

> Staking rewards must not create new GFC supply under the current model.

> Internal transfers are not new external funding.

> Migration must not create duplicate economic claims.

> Transaction verification does not equal use-of-funds verification.

> Use-of-funds verification does not equal outcome verification.

> Outcome verification does not automatically equal impact verification.

> Pilot economic activity does not establish production economic activity.

The objective is to make every material movement of value attributable to a source, authority, rule, destination, economic classification, and evidence record without overstating what the movement proves.

# GFC Deployment Registry

**Document:** DEPLOYMENTS.md  
**Status:** Informative deployment record  
**Repository Stage:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Last Updated:** 2026-08-30

---

## 1. Purpose

This document records authenticated or publicly established GFC deployment status.

It is not a deployment script, smart-contract specification, audit report, or guarantee of production readiness.

Its purpose is to distinguish clearly between:

- public pilot deployments;
- future production deployments;
- test or development deployments;
- deprecated deployments;
- and components that are **Not Deployed**.

A contract, wallet, address, or deployment MUST NOT be treated as official production infrastructure solely because it:

- uses the GFC name;
- uses the GFC symbol;
- appears on a block explorer;
- appears in a repository;
- is shared through social media;
- or was used in a test or pilot environment.

Production status requires an authenticated production deployment record.

---

## 2. Current Deployment Summary

| Component | Environment | Network | Status |
|---|---|---|---|
| `tGFC` public pilot token | Pilot | Base Sepolia | **Pilot / Deployed** |
| Production GFC token | Production | Base Mainnet | **Not Deployed** |
| Production presale | Production | Base Mainnet | **Not Deployed** |
| Impact Vault | Production | Base Mainnet | **Not Deployed** |
| Guardian Growth custody | Production | Base Mainnet | **Not Deployed** |
| Treasury Reserve infrastructure | Production | Base Mainnet | **Not Deployed** |
| Liquidity Reserve infrastructure | Production | Base Mainnet | **Not Deployed** |
| Ecosystem custody/distribution | Production | Base Mainnet | **Not Deployed** |
| Core Team vesting | Production | Base Mainnet | **Not Deployed** |
| Production staking | Production | Base Mainnet | **Not Deployed** |
| Production governance contracts | Production | Base Mainnet | **Not Deployed** |
| Production Transparency Registry | Production | Base Mainnet | **Not Deployed** |
| Broader Accountability Infrastructure | Production | Base Mainnet / future architecture | **Not Deployed** |

This table describes the current repository state.

It MUST NOT be interpreted as a commitment that every listed future component will use a separate contract.

---

## 3. Public Base Sepolia Pilot

A public GFC pilot exists on Base Sepolia.

### 3.1 Pilot token

| Property | Recorded Value |
|---|---|
| Environment | Public pilot / testnet |
| Network | Base Sepolia |
| Chain ID | `84532` |
| Token label | `tGFC` |
| Contract address | `0x7262Cca91938ede6bB6560F81104Aa410848e7f3` |
| Public pilot date | 2026-08-02 |
| Source verification status | Verified |
| Production status | **Non-production** |
| Base Mainnet authority | None established by this deployment record |
| Presale status | Not a presale |
| Production GFC status | Not the production GFC token |

### 3.2 What this pilot establishes

The public pilot establishes only that a GFC-related test token deployment exists on Base Sepolia at the address recorded above.

It may serve as evidence of:

- early technical execution;
- testnet deployment capability;
- public contract interaction;
- and source-verification activity.

### 3.3 What this pilot does not establish

The pilot MUST NOT be interpreted as evidence of:

- a production GFC token;
- Base Mainnet deployment;
- a live presale;
- production tokenomics;
- production fee behavior;
- production allocations;
- a production Impact Vault;
- production Core Team vesting;
- production staking;
- production treasury infrastructure;
- production liquidity infrastructure;
- production governance;
- production multisig configuration;
- production authority assignments;
- production security review;
- completed independent audit;
- production Transparency Registry;
- or complete Accountability Infrastructure.

The pilot also MUST NOT be treated as proof that a future production deployment will use identical:

- source code;
- bytecode;
- constructor parameters;
- roles;
- administrator structure;
- upgradeability;
- fee logic;
- allocation logic;
- contract addresses;
- or operational controls.

---

## 4. Pilot Deployment Details Not Yet Authenticated in This Record

The following details are not established by the current repository record available for this file and therefore are not asserted here:

- deployment transaction hash;
- deployer address;
- source-code commit;
- compiler version;
- optimizer settings;
- build configuration;
- constructor parameters;
- initial supply transaction details;
- pilot ownership or administrator mapping;
- pause authority;
- upgrade authority;
- migration authority;
- pilot signer structure;
- external security-review status;
- audit status beyond the explicit absence of a production audit claim;
- and complete pilot lifecycle history.

These fields SHOULD be added only when they can be authenticated from the relevant source, transaction, verified contract metadata, repository commit, or other authoritative record.

Unknown fields MUST NOT be guessed for completeness.

---

## 5. Intended Production Network

The intended initial production environment is:

| Property | Intended Value |
|---|---|
| Network | Base Mainnet |
| Chain ID | `8453` |
| Production token | Global Foundation Coin (`GFC`) |
| Production token status | **Not Deployed** |

This is an intended production environment, not an active deployment.

No official Base Mainnet GFC token contract address is established by this document.

No token on Base Mainnet MUST be treated as official GFC unless it is authenticated through the future production release and deployment process.

---

## 6. Production GFC Token

### Status

**Not Deployed**

No official production GFC token is currently recorded on Base Mainnet.

Accordingly, the following production details do not yet exist as authenticated deployment records:

- production GFC contract address;
- deployment transaction;
- production deployer;
- production bytecode;
- production source-code commit;
- production compiler configuration;
- production token administrator;
- production fee authority;
- production recognized-pool configuration;
- production fee-exemption configuration;
- production pause authority;
- production upgrade authority;
- production migration authority;
- and production source-verification record.

The current token specification describes intended behavior only.

See [`specs/token.md`](specs/token.md).

---

## 7. Production Presale

### Status

**Not Deployed / Not Live**

No production GFC presale contract is currently recorded.

No public production presale address is established by this document.

No public launch date is established by this document.

The current Draft presale design includes:

- reference price of €0.05 per GFC;
- intended eight-week duration;
- €250,000 soft cap;
- no separate monetary hard cap;
- maximum Presale allocation of 150,000,000 GFC;
- intended support for ETH, USDC, and DAI on Base;
- immediate GFC distribution as the current design direction;
- and refunds if the applicable success condition is not satisfied.

These are specification parameters, not deployed behavior.

The unresolved interaction between immediate GFC distribution and failed-sale refunds remains a production activation blocker.

See [`specs/presale.md`](specs/presale.md).

---

## 8. Production Allocations

### Status

**Not Deployed**

No production allocation wallet or contract is authenticated as official by this file.

The current Draft allocation model is:

| Allocation | Share | Token Amount | Production Deployment Status |
|---|---:|---:|---|
| Impact Vault | 25% | 250,000,000 GFC | Not Deployed |
| Guardian Growth | 20% | 200,000,000 GFC | Not Deployed |
| Presale | 15% | 150,000,000 GFC | Not Deployed |
| Treasury Reserve | 15% | 150,000,000 GFC | Not Deployed |
| Liquidity Reserve | 15% | 150,000,000 GFC | Not Deployed |
| Ecosystem | 5% | 50,000,000 GFC | Not Deployed |
| Core Team | 5% | 50,000,000 GFC | Not Deployed |
| **Total** | **100%** | **1,000,000,000 GFC** | — |

These values are specification state.

They are not evidence of funded production wallets or deployed allocation contracts.

See [`specs/allocations.md`](specs/allocations.md).

---

## 9. Impact Vault

### Status

**Not Deployed**

The current specification intends:

- allocation: `250,000,000 GFC`;
- share: `25%`;
- intended restriction: `50-year lock`.

No production Impact Vault address, lock contract, start timestamp, or authenticated lock state is currently recorded.

The phrase `50-year locked` MUST NOT be used as a statement of current production enforcement.

See [`specs/vesting-and-unlocks.md`](specs/vesting-and-unlocks.md).

---

## 10. Core Team Vesting

### Status

**Not Deployed**

The current specification intends:

- allocation: `50,000,000 GFC`;
- share: `5%`;
- intended restriction: `19-year linear vesting`.

No production vesting contract, beneficiary mapping, vesting-start timestamp, or claim state is currently recorded.

The production vesting period MUST NOT be treated as already running.

See [`specs/vesting-and-unlocks.md`](specs/vesting-and-unlocks.md).

---

## 11. Treasury Reserve

### Status

**Not Deployed**

No production Treasury Reserve wallet, multisig, contract, signer set, or approval threshold is authenticated as official by this record.

No production treasury custody structure MUST be inferred from:

- a Draft role definition;
- an allocation name;
- a pilot wallet;
- or an informal project wallet.

Future deployment records MUST authenticate actual treasury custody and authority separately.

---

## 12. Liquidity Reserve

### Status

**Not Deployed**

No production Liquidity Reserve wallet or liquidity-provider position is authenticated as official by this record.

No production GFC liquidity deployment is established by this file.

The existence of a planned Liquidity Reserve does not prove:

- active liquidity;
- locked liquidity;
- protocol-owned liquidity;
- market depth;
- or permanent liquidity availability.

---

## 13. Guardian Growth

### Status

**Not Deployed**

No production Guardian Growth custody mechanism is authenticated as official by this record.

No signer, guardian, wallet, approval threshold, or independent oversight structure is established by this file.

The word `Guardian` MUST NOT be interpreted as evidence of independent control.

---

## 14. Ecosystem

### Status

**Not Deployed**

No production Ecosystem custody or distribution mechanism is authenticated as official by this record.

No grant, incentive, recipient, or distribution infrastructure is established as deployed by this document.

---

## 15. Production Staking

### Status

**Not Deployed / Not Operational**

No production staking contract or reward pool is authenticated as official.

The current staking design direction is:

**hybrid and non-inflationary**

No production reward source, reward rate, APR, APY, lock period, governance right, or reward duration is established by this deployment record.

See [`specs/staking.md`](specs/staking.md).

---

## 16. Production Governance

### Status

**Not Deployed**

No production governance contract, executor, timelock, voting system, multisig, signer set, or governance role holder is authenticated as official by this file.

Draft role and governance specifications define constraints.

They do not assign production authority.

Actual production authority MUST be recorded through authenticated production deployment and authority records.

See:

- [`specs/roles-and-authority.md`](specs/roles-and-authority.md)
- [`specs/governance-constraints.md`](specs/governance-constraints.md)

---

## 17. Transparency Registry

### Status

**Not Deployed as a complete production system**

The planned Transparency Registry is intended to operate as a:

**versioned historical record rather than a permanent approval badge**

No complete production Registry deployment, Registry contract, Registry authority mapping, evidence schema, admission system, verification-status system, or production review workflow is authenticated as operational by this file.

See [`specs/transparency-model.md`](specs/transparency-model.md).

---

## 18. Broader Accountability Infrastructure

### Status

**Not Deployed as a complete production system**

The broader long-term GFC accountability model is:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

The existence of the Base Sepolia token pilot does not establish this wider system as implemented.

Long-term accountability infrastructure may include multiple on-chain and off-chain components.

This file MUST NOT be interpreted as committing GFC to a specific future deployment topology beyond the currently intended initial Base Mainnet production environment.

---

## 19. Authority and Deployment Records

A Draft role definition is not a deployment.

A deployment is not automatically active production authority.

Future production deployment records SHOULD authenticate, where applicable:

- deployer;
- contract owner;
- proxy administrator;
- upgrade authority;
- pauser;
- migration authority;
- fee authority;
- allocation custody;
- treasury authority;
- liquidity authority;
- presale authority;
- staking authority;
- governance executor;
- recovery authority;
- and publication authority.

Actual production role holders MUST NOT be inferred from pilot or Draft state.

---

## 20. Production Deployment Record Requirements

Before a component is represented as an official production deployment, the applicable deployment record SHOULD identify:

- component name;
- environment;
- network;
- chain ID;
- authenticated contract or wallet address;
- deployment transaction where applicable;
- deployment date or block;
- source-code repository;
- source-code commit;
- compiler and build information where applicable;
- constructor or initializer parameters;
- implementation address where applicable;
- proxy architecture where applicable;
- deployer;
- initial ownership;
- current privileged roles;
- timelocks;
- multisig or signer structure where applicable;
- configuration parameters;
- source-verification status;
- test status;
- security-review status;
- audit status;
- applicable specification version;
- known deviations;
- pause status;
- upgradeability;
- migration status;
- and current operational status.

Unknown fields MUST be identified as unknown or not yet authenticated.

They MUST NOT be invented.

---

## 21. Deployment Status Terminology

Deployment records MUST use implementation-status terminology consistently with [`specs/glossary.md`](specs/glossary.md).

Relevant distinctions include:

- **Draft**
- **Proposed**
- **Planned**
- **Specified**
- **Implemented**
- **Tested**
- **Pilot**
- **Reviewed**
- **Audited**
- **Deployed**
- **Live**
- **Active**
- **Operational**
- **Independently Verified**
- **Not Deployed**
- **Paused**
- **Migrated**
- **Retired**

These terms are not interchangeable.

In particular:

> Pilot does not mean production.

> Deployed does not automatically mean active.

> Active does not automatically mean audited.

> Source verified does not mean audited.

> Tested does not mean production-ready.

---

## 22. Source Verification

Source verification means that source code has been matched or published through the applicable verification mechanism for the relevant contract.

It does not independently establish:

- security;
- audit completion;
- correct authority;
- production readiness;
- business legitimacy;
- or specification conformance.

The Base Sepolia `tGFC` pilot is recorded as source verified.

That source-verification status applies to the pilot and MUST NOT be carried over automatically to any future Base Mainnet deployment.

---

## 23. Security and Audit Status

No independent production security audit is established as completed by this deployment registry.

If a future deployment is audited, the record SHOULD identify:

- auditor;
- scope;
- exact reviewed code or deployment;
- report date;
- exclusions;
- findings;
- remediation status;
- and report reference.

An audit of one component MUST NOT be represented as an audit of the complete GFC system.

See [`specs/security-model.md`](specs/security-model.md).

---

## 24. Pilot-to-Production Migration

No automatic pilot-to-production migration is established.

A future Base Mainnet production deployment MUST be separately:

- specified;
- implemented;
- tested;
- reviewed as appropriate;
- deployed;
- authenticated;
- and recorded.

The production system MAY differ materially from the pilot.

No participant or reviewer SHOULD assume that:

- pilot balances migrate;
- pilot addresses remain relevant;
- pilot administrators remain authorities;
- pilot bytecode is reused;
- or pilot parameters become production parameters.

---

## 25. Deprecated and Replaced Deployments

Future replaced or deprecated deployments SHOULD remain historically recorded.

A deployment record SHOULD identify, where applicable:

- previous address;
- successor address;
- deprecation date;
- migration transaction;
- reason;
- remaining risks;
- and whether users must take action.

A replacement deployment MUST NOT silently erase the existence of an earlier deployment.

---

## 26. Fake and Unauthenticated Deployments

A contract or token MUST NOT be treated as official GFC production infrastructure if it cannot be authenticated through the applicable GFC release and deployment record.

Users and integrators SHOULD verify:

- network;
- chain ID;
- contract address;
- release;
- source verification;
- and current deployment status

before relying on a contract.

An unauthenticated token using `GFC`, `Global Foundation Coin`, or related branding does not become official by name.

---

## 27. Repository Relationship

This file records deployment state.

Normative component requirements belong in the applicable files under [`specs/`](specs/).

Current overall project status is maintained in [`STATUS.md`](STATUS.md).

The repository `main` branch is not automatically a production release.

A future production deployment MUST identify the exact applicable specification and source release.

---

## 28. Current Known Deployment Record

At the date of this document, the only public on-chain deployment recorded here as an established GFC project deployment is the Base Sepolia `tGFC` pilot:

```text
Network: Base Sepolia
Chain ID: 84532
Token: tGFC
Contract: 0x7262Cca91938ede6bB6560F81104Aa410848e7f3
Status: Public Pilot / Non-Production
Source: Verified
```

No Base Mainnet production GFC contract is recorded.

No live production presale is recorded.

No complete production GFC economic or accountability infrastructure is recorded.

---

## 29. Final Deployment Principles

This deployment registry preserves the following distinctions:

> Base Sepolia is not Base Mainnet.

> `tGFC` is not the production GFC token.

> Pilot is not production.

> Source verified is not audited.

> Deployed is not automatically active.

> Draft specification is not deployment.

> A wallet label is not authenticated authority.

> A testnet administrator is not automatically a production administrator.

> A future contract address must be authenticated before it is treated as official.

> Production deployment records must describe actual deployed state, not intended architecture.

The current public pilot demonstrates limited testnet execution.

It does not establish a production GFC system.

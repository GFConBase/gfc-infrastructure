# Global Foundation Coin Roadmap

**Document:** ROADMAP.md  
**Status:** Informative planning document  
**Repository Stage:** Pre-mainnet specification and pilot development  
**Primary Product Focus:** GFC Token / Economic Layer  
**Long-Term Direction:** Accountability Infrastructure  
**Current Plan Basis:** 2026-08-25 canonical project plan  
**Last Updated:** 2026-08-30

---

## 1. Purpose

This roadmap describes the current intended development sequence for Global Foundation Coin (GFC).

It is an informative planning document.

It does not itself:

- deploy contracts;
- authorize production;
- establish a public sale date;
- create participant rights;
- assign production authority;
- confirm audit completion;
- guarantee funding;
- guarantee partnerships;
- guarantee regulatory approval;
- or make a future milestone operational.

Normative technical requirements are defined in the applicable files under [`specs/`](specs/).

Current deployment status is recorded in [`STATUS.md`](STATUS.md) and [`DEPLOYMENTS.md`](DEPLOYMENTS.md).

---

## 2. Current Strategic Direction

The current primary product focus is the:

**GFC Token / Economic Layer**

Through the end of Q1 2027, the operational priority is to move this product toward credible:

- technical readiness;
- economic readiness;
- security readiness;
- governance readiness;
- transparency readiness;
- operational readiness;
- and legal readiness

for a future production launch process.

Supporting work includes:

- website and public documentation;
- specifications;
- governance constraints;
- transparency architecture;
- smart-contract development;
- testing;
- security review;
- deployment planning;
- partnerships;
- funding;
- community development;
- and legal preparation.

From Q2 2027 onward, the intended direction broadens toward a wider:

**Accountability Infrastructure**

based on:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

The token remains part of that wider system.

---

## 3. Current State — 2026-08-30

GFC is currently in:

**Pre-mainnet specification and pilot development**

### Established today

- Global Foundation Coin is the current project identity.
- The current primary product focus is the GFC Token / Economic Layer.
- A public Base Sepolia pilot exists.
- Pilot token: `tGFC`.
- Pilot network: Base Sepolia.
- Pilot chain ID: `84532`.
- Pilot contract:
  `0x7262Cca91938ede6bB6560F81104Aa410848e7f3`
- Pilot source is verified.
- The fixed-supply token model is specified at:
  `1,000,000,000 GFC`.
- The current Draft allocation model is specified.
- The current Draft presale model is specified.
- The current Draft staking direction is hybrid and non-inflationary.
- Governance, security, authority, vesting, economic-flow, and transparency constraints are being formalized.
- The intended initial production network is Base Mainnet.

### Not established today

- no production GFC token on Base Mainnet;
- no live GFC presale;
- no production presale contract;
- no production allocation infrastructure;
- no production Impact Vault;
- no production Core Team vesting contract;
- no production treasury infrastructure;
- no production liquidity infrastructure;
- no production staking system;
- no production governance infrastructure;
- no complete production Transparency Registry;
- no complete broader Accountability Infrastructure;
- and no completed independent production security audit represented by this repository.

The Base Sepolia pilot MUST remain distinct from future production deployments.

---

## 4. Roadmap Principles

The roadmap follows the principles below.

### 4.1 Readiness before activation

A target date does not override technical, security, legal, economic, or operational readiness.

### 4.2 Specification before production reliance

Material participant-facing and authority-sensitive behavior SHOULD be specified before production activation.

### 4.3 Pilot is not production

Testnet success does not automatically authorize Mainnet deployment.

### 4.4 Security gates are real gates

A milestone that depends on unresolved critical security behavior MUST NOT be treated as ready merely because its target period has arrived.

### 4.5 Public communication must match actual status

Planned work MUST remain labeled Planned.

Implemented work MUST NOT be labeled Audited unless actually audited.

Deployed work MUST NOT be labeled Operational unless actually operational.

### 4.6 Long-term expansion must not weaken current product execution

The wider Accountability Infrastructure remains strategically important, but the current product-development priority is the Token / Economic Layer.

---

# Phase 1 — Foundation Finalization

## 5. August–September 2026

**Primary objective:** complete and professionalize the public, technical, and specification foundation.

### Core workstreams

#### Repository and specification baseline

- complete the current specification set;
- remove outdated terminology and legacy assumptions;
- align all documents to the current canonical GFC state;
- formalize status terminology;
- separate Pilot from Production consistently;
- document the Base Sepolia pilot;
- define deployment-record requirements;
- define security and authority boundaries;
- and establish a coherent public technical repository.

#### Website and public information

- maintain the public GFC website as an accurate representation of current status;
- clearly distinguish what exists from what is planned;
- keep the GFC Token / Economic Layer visible as the current primary product;
- preserve the broader long-term Accountability Infrastructure direction;
- improve search discoverability and analytics;
- and keep public communication consistent with repository status.

#### Governance and transparency foundation

- formalize authority constraints;
- formalize separation-of-duties principles;
- formalize upgrade, pause, migration, and emergency constraints;
- formalize the versioned Transparency Registry concept;
- and preserve the principle that Registry status is not a permanent approval badge.

#### Community and credibility

- continue public communication;
- build relevant professional and crypto-native reach;
- establish communication channels;
- develop relationships with potential partners, reviewers, funders, and ecosystem participants;
- and prioritize credibility over hype.

### Exit condition

Phase 1 is substantially complete when the public project surface, repository, terminology, specifications, and pilot status are mutually consistent and suitable as a credible foundation for implementation work.

---

# Phase 2 — Production Design and Implementation

## 6. Q4 2026

**Primary objective:** convert the specification baseline into production-oriented implementation candidates.

### Token implementation

Planned work includes:

- finalize production token architecture;
- finalize supply-creation method;
- finalize buy/sell classification;
- finalize 0% buy / 1% sell fee implementation;
- finalize fee destination and fee-proceeds handling;
- finalize recognized-pool behavior;
- finalize exemptions or explicitly exclude them;
- finalize pause behavior or explicitly exclude it;
- finalize upgradeability;
- finalize migration behavior;
- and implement the production candidate.

### Allocation implementation

Planned work includes:

- finalize custody architecture;
- finalize Impact Vault implementation;
- finalize Core Team vesting implementation;
- finalize allocation migration constraints;
- finalize Guardian Growth control model;
- finalize Treasury Reserve control model;
- finalize Liquidity Reserve control model;
- finalize Ecosystem control model;
- and prepare production allocation deployment logic.

### Presale implementation

Planned work includes:

- finalize ETH, USDC, and DAI handling on Base;
- finalize pricing and conversion architecture;
- finalize contribution accounting;
- finalize immediate GFC distribution mechanics;
- resolve the failed-sale refund treatment of already distributed GFC;
- finalize contribution custody;
- finalize refund mechanics;
- finalize successful-proceeds handling;
- finalize unsold-GFC treatment;
- finalize immutable/configurable boundaries;
- and implement a production candidate.

### Staking implementation

Planned work includes:

- finalize staking principal model;
- select and document a non-inflationary reward source;
- finalize reward accounting;
- finalize reward-rate model;
- finalize reward duration;
- finalize lock and withdrawal behavior;
- finalize governance-related rights or explicitly exclude them;
- and implement only when economic sustainability is supportable.

### Security and testing

Planned work includes:

- unit testing;
- integration testing;
- invariant testing;
- fuzz testing where appropriate;
- deployment rehearsal;
- role and authority review;
- failure-state testing;
- presale refund testing;
- migration testing;
- and contract/source review.

### Exit condition

Q4 implementation work should produce reviewable production candidates rather than merely conceptual specifications.

No production activation follows automatically from completion of implementation.

---

# Phase 3 — Mainnet and Presale Readiness

## 7. Q1 2027

**Primary objective:** move the GFC Token / Economic Layer from production-candidate status toward controlled production activation.

This phase remains dependent on successful completion of unresolved technical, security, governance, legal, and operational gates.

### Production-readiness work

Planned work includes:

- freeze applicable production specifications;
- map implementation to exact specification versions;
- finalize production authority structure;
- finalize multisig or equivalent custody where applicable;
- finalize signer and approval processes;
- finalize timelocks;
- finalize production addresses and deployment procedures;
- finalize monitoring;
- finalize incident response;
- finalize public authentication of production contracts;
- and prepare production deployment records.

### Security review

Planned work includes security review appropriate to the final production architecture.

Where an independent audit or equivalent independent security review is feasible before production activation, it SHOULD be pursued.

An audit MUST NOT be represented as completed until it has actually occurred.

### Legal and operational readiness

Planned work includes:

- participant-facing legal review;
- presale eligibility framework;
- payment-asset handling review;
- public disclosures;
- privacy processes;
- operational controls;
- and incident/escalation procedures.

### Presale readiness

The public roadmap does not establish a precise public launch date.

Before any presale activation, the following must be resolved:

- production GFC token deployment;
- production Presale allocation funding;
- exact payment-asset identifiers;
- pricing;
- immediate-distribution semantics;
- failed-sale refund treatment;
- contribution custody;
- refund implementation;
- proceeds handling;
- unsold-GFC treatment;
- participant terms;
- authority;
- security review;
- monitoring;
- and public deployment authentication.

### Production activation

If the applicable readiness gates are satisfied, Q1 2027 is the intended phase for presale preparation and potential start.

This statement is a planning target.

It is not a launch guarantee.

---

# Phase 4 — Broader Production Expansion

## 8. Q2 2027

**Primary objective:** expand beyond the initial pre-mainnet/presale-readiness phase and begin broader production development.

Potential work includes:

### Token launch progression

Depending on the result and state of the Q1 work:

- continue presale lifecycle;
- complete required finalization;
- complete participant settlement;
- complete refunds where required;
- progress toward broader Mainnet token operations;
- and authenticate resulting production deployment state.

### Security

If a full independent audit was not completed earlier, prioritize it when technically and financially feasible.

Security work remains continuous rather than a one-time milestone.

### Transparency infrastructure

Begin broader implementation of the Transparency Registry and accountability tooling, including:

- versioned historical records;
- authority records;
- evidence linkage;
- status changes;
- corrections;
- disputes;
- downgrade and suspension concepts;
- and improved automation.

The Registry MUST remain a historical accountability system rather than a permanent approval badge.

### Economic operations

Where production-ready and justified:

- activate approved treasury processes;
- activate approved liquidity processes;
- activate staking only if its non-inflationary reward model is finalized and sustainable;
- and improve reconciliation and reporting.

### Partnerships and ecosystem

Continue:

- partnerships;
- institutional relationships;
- funding efforts;
- adoption discussions;
- and external-user discovery.

### Exit condition

Q2 should establish whether GFC can move from a token-focused production phase into a broader accountable system without weakening the token's security, economic, or governance foundations.

---

# Phase 5 — Accountability Infrastructure Expansion

## 9. H2 2027 and Beyond

**Primary objective:** expand GFC from the Token / Economic Layer toward broader Accountability Infrastructure.

Potential work includes:

- broader Transparency Registry functionality;
- external project and organization records;
- evidence packages;
- protected evidence workflows;
- review workflows;
- dispute handling;
- corrections and supersession;
- historical status reconstruction;
- automated data ingestion;
- stronger economic-flow reconciliation;
- governance-record integration;
- outcome and impact evidence linkage;
- and public accountability interfaces.

External Registry participation MAY eventually include eligible:

- projects;
- NGOs;
- organizations;
- companies;
- programs;
- or other initiatives

under GFC-defined admission and status rules.

Such functionality remains future-oriented until actually implemented and deployed.

---

## 10. Application and User Experience

A dedicated application MAY be developed as the system expands.

Potential functions may include:

- token information;
- authenticated deployment records;
- transparency records;
- allocation visibility;
- governance records;
- staking interfaces where applicable;
- evidence navigation;
- and user-facing accountability tools.

No application is established as production-operational by this roadmap.

---

## 11. Future Execution Environment Evaluation

The intended initial production network remains:

**Base Mainnet**

GFC does not currently commit to launching its own independent blockchain.

At a later stage, GFC MAY evaluate:

- an appchain;
- rollup;
- dedicated execution environment;
- or another Base-aligned or otherwise appropriate scaling architecture

if the system's scale and requirements justify it.

Any such move would require separate:

- architecture;
- security;
- governance;
- migration;
- economic;
- and deployment specifications.

It is not a current production commitment.

---

# Cross-Cutting Workstreams

## 12. Security

Security remains continuous across all phases.

Work includes:

- threat modeling;
- access-control review;
- key security;
- multisig/signing security;
- upgrade security;
- pause and emergency security;
- migration security;
- contract testing;
- monitoring;
- incident response;
- and independent review where appropriate.

No roadmap date overrides a critical unresolved security issue.

---

## 13. Governance

Governance development includes:

- explicit authority;
- least privilege;
- separation of duties;
- limited upgrades;
- predictable exceptions;
- timelocks;
- emergency constraints;
- authority registry;
- historical role changes;
- and accurate decentralization claims.

Token ownership or staking MUST NOT automatically create unrestricted governance authority.

---

## 14. Transparency

Transparency development includes:

- authenticated contract and wallet records;
- allocation reporting;
- authority reporting;
- economic-flow reporting;
- evidence classification;
- historical status;
- correction;
- dispute handling;
- review status;
- and limitation disclosure.

The long-term Transparency Registry principle is:

**history, not badge**

---

## 15. Legal and Compliance

Legal work is a continuing readiness requirement.

It may include:

- participant terms;
- jurisdiction analysis;
- eligibility;
- sanctions controls;
- privacy;
- data protection;
- token-related legal analysis;
- presale-related legal analysis;
- disclosure;
- and operational obligations.

The roadmap does not make a legal conclusion.

---

## 16. Funding

GFC may pursue:

- accelerator funding;
- grants;
- institutional funding;
- partnerships;
- and other appropriate financing

to support development, audits, legal work, security, infrastructure, and full-time execution.

Funding is not guaranteed.

Funding plans MUST NOT be represented as completed financing before funds are actually committed and received under the applicable terms.

---

## 17. Partnerships

Potential partnerships may support:

- technical development;
- security;
- Base ecosystem integration;
- transparency;
- verification;
- NGOs and impact organizations;
- funding;
- liquidity;
- legal readiness;
- distribution;
- and adoption.

A conversation or application does not equal a partnership.

A partnership MUST NOT be represented as active until actually established.

---

## 18. Community and Public Communication

Public communication should continue to prioritize:

- accurate status;
- clear product positioning;
- transparency;
- education;
- accountability;
- and evidence of execution.

GFC MUST avoid:

- false launch claims;
- exaggerated decentralization claims;
- false audit claims;
- guaranteed-return language;
- guaranteed-impact language;
- or presentation of planned infrastructure as operational.

---

# Critical Gates

## 19. Mainnet Gate

Before an official Base Mainnet GFC token is represented as production, the project should have:

- finalized production token architecture;
- finalized applicable specifications;
- completed production testing;
- resolved privileged authority;
- authenticated production deployment records;
- completed appropriate security review;
- established monitoring;
- and aligned public communication.

---

## 20. Presale Gate

Before any production presale activation:

- production GFC MUST be authenticated;
- Presale distribution capacity MUST be available;
- ETH, USDC, and DAI production handling MUST be finalized;
- pricing MUST be finalized;
- immediate distribution MUST be technically defined;
- failed-sale treatment of already distributed GFC MUST be resolved;
- refund mechanics MUST be enforceable;
- contribution custody MUST preserve refund rights;
- proceeds withdrawal MUST be constrained;
- unsold-GFC treatment MUST be predefined;
- authority MUST be authenticated;
- security requirements MUST be satisfied;
- and participant-facing terms MUST be ready.

The unresolved immediate-distribution/refund interaction is currently a hard production blocker.

---

## 21. Staking Gate

Before staking becomes production-operational:

- reward source MUST be explicit;
- rewards MUST remain non-inflationary;
- reward accounting MUST be finalized;
- reward capacity MUST be sustainable;
- principal custody MUST be finalized;
- lock and withdrawal rules MUST be defined;
- governance-related rights MUST be defined or excluded;
- security review MUST be completed as appropriate;
- and production deployment MUST be authenticated.

---

## 22. Transparency Registry Gate

Before the Transparency Registry is represented as a production system:

- admission rules MUST be defined;
- status vocabulary MUST be defined;
- evidence requirements MUST be defined;
- review authority MUST be defined;
- correction rules MUST be defined;
- downgrade and suspension rules MUST be defined;
- dispute handling MUST be defined;
- historical retention MUST be defined;
- privacy controls MUST be defined;
- and Registry authority MUST be disclosed.

---

# Roadmap Status Model

## 23. Status Terms

Roadmap items SHOULD use the repository's established status vocabulary.

Relevant terms include:

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

A roadmap target is normally **Planned** until stronger evidence supports a later status.

---

## 24. Date Interpretation

Quarter and month ranges in this roadmap are planning windows.

They are not automatic commitments.

A milestone MAY move if required by:

- security;
- implementation complexity;
- funding;
- legal review;
- external dependencies;
- partnership timing;
- audit availability;
- testing results;
- or newly discovered risk.

Material roadmap changes SHOULD be recorded transparently.

---

## 25. Internal Versus Public Dates

Internal planning may use more precise dates than the public roadmap.

An internal planning date MUST NOT be treated as a confirmed public launch date unless formally released through the applicable public process.

This roadmap intentionally does not publish a precise presale start date.

---

# Current Roadmap Snapshot

## 26. Summary Table

| Period | Primary Objective | Current Status |
|---|---|---|
| Aug–Sep 2026 | Foundation Finalization | **Active** |
| Q4 2026 | Production design, implementation, testing | **Planned** |
| Q1 2027 | Mainnet and presale readiness / potential presale start | **Planned** |
| Q2 2027 | Broader production expansion and transparency build-out | **Planned** |
| H2 2027+ | Accountability Infrastructure expansion | **Planned** |
| Later, if justified | Dedicated execution environment / appchain evaluation | **Proposed future option** |

---

## 27. Near-Term Priority Order

The current near-term execution order is:

1. finalize the public technical repository;
2. maintain accurate public status;
3. complete production-oriented specifications;
4. implement production candidates;
5. test economic and security invariants;
6. resolve the Presale immediate-distribution/refund interaction;
7. finalize authority and custody;
8. perform appropriate security review;
9. finalize legal and operational readiness;
10. authenticate production deployment only when readiness gates are met.

---

## 28. Roadmap Non-Goals

This roadmap does not:

- guarantee a Mainnet launch date;
- guarantee a presale date;
- guarantee a successful presale;
- guarantee the soft cap will be reached;
- guarantee an audit will occur by a specific date;
- guarantee funding;
- guarantee partnerships;
- guarantee exchange listing;
- guarantee liquidity;
- guarantee staking returns;
- guarantee token appreciation;
- guarantee regulatory approval;
- or guarantee impact.

It also does not authorize skipping unresolved production gates.

---

## 29. Relationship to Deployment Status

Roadmap state and deployment state MUST remain separate.

For example:

- `Planned` Mainnet deployment does not mean `Deployed`;
- `Specified` presale does not mean `Live`;
- `Implemented` staking code does not mean `Operational`;
- `Reviewed` code does not mean `Audited`;
- and a Base Sepolia `Pilot` does not mean Base Mainnet production.

Actual deployment state is recorded in [`DEPLOYMENTS.md`](DEPLOYMENTS.md).

---

## 30. Final Roadmap Principle

The roadmap is intended to move GFC through the following progression:

**Specify → Implement → Test → Review → Deploy → Operate → Evidence**

without collapsing those stages into one another.

The current priority is to build a credible GFC Token / Economic Layer.

The long-term objective is broader Accountability Infrastructure in which:

**Funds → Authority → Rules → Decisions → Outcomes → Evidence**

can be reconstructed and reviewed.

Progress is measured by verified execution and readiness, not by roadmap dates alone.

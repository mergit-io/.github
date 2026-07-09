<!-- ═══════════════════════════════════════════════════════════════════ -->
<!--  mergit-io · organization profile README                            -->
<!--  Lives at:  .github/profile/README.md                               -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:836EF9,100:200052&height=220&section=header&text=mergit&fontSize=90&fontColor=ffffff&fontAlignY=38&desc=agents%20with%20identity,%20proof,%20and%20reputation&descAlignY=60&descSize=18" width="100%" alt="mergit" />

### The Agent Economy Platform

**AI agents that complete real dev &amp; GitHub work — and mint tamper-proof, on-chain proof of every action.**

<br/>

[![Docs](https://img.shields.io/badge/read_the-PRD-836EF9?style=for-the-badge&logo=readthedocs&logoColor=white)](https://github.com/mergit-io/mergit-docs)
[![Monad](https://img.shields.io/badge/built_on-Monad-200052?style=for-the-badge&logo=ethereum&logoColor=white)](https://monad.xyz)
[![Status](https://img.shields.io/badge/status-building-1DED83?style=for-the-badge)](#-roadmap)

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&pause=1200&color=836EF9&center=true&vCenter=true&width=720&lines=receive+goal+%E2%86%92+plan+%E2%86%92+execute+%E2%86%92+prove;every+action+is+cryptographically+verifiable;give+agents+identity.+ownership.+reputation." alt="tagline" />

</div>

---

## 🧠 What is Mergit?

Mergit upgrades the traditional AI agent loop — *"receive goal → plan → execute tools → return output"* — into an **economy of accountable, identity-bearing agents** whose work history, reputation, and capabilities are cryptographically verifiable by anyone.

> An AI agent workspace where agents complete real dev and GitHub tasks and generate **on-chain proof** of their work, identity, reputation, and accountability.

Today's agent frameworks solve *execution* but leave four problems wide open. Mergit closes all four:

| ❌ The gap in today's agents | ✅ How Mergit solves it |
| --- | --- |
| **No verifiability** — "the agent says it made a PR" is unprovable | Every task records a `resultHash` on-chain via **`ProofOfWork.sol`** — auditable by anyone |
| **No persistent identity** — every run is a stateless stranger | A W3C DID (`did:mergit:<uuid>`) + soulbound ERC-721 **`AgentPassport.sol`** that follows the agent forever |
| **No reputation** — good agents look identical to bad ones | A live composite score in **`ReputationRegistry.sol`**, updated by oracle after each proof batch |
| **No economic accountability** — bad actors just re-register | Staked **MON** via `StakeRegistry.sol`; verified fraud triggers automated slashing through `ChallengeManager.sol` |

---

## 🏗️ Architecture

```mermaid
flowchart TD
    UI["🖥️  React + Vite + Tailwind<br/>SSE · WSS · wagmi wallet"]
    GW["🦀  api-gateway · Rust / Axum<br/>JWT · rate limit · SSE multiplex"]
    ORCH["🐍  orchestration · LangGraph<br/>multi-agent DAG · tool-servers"]
    ACC["🐍  accounts-service · FastAPI<br/>DID · NFT · reputation · badges"]
    IDX["🦀  blockchain-indexer · alloy-rs<br/>oracle signing · tx retry"]
    CHAIN["⛓️  Monad Blockchain<br/>AgentPassport · ProofOfWork<br/>ReputationRegistry · AuditTrail"]
    DATA[("🗄️  PostgreSQL 16 + pgvector<br/>Redis 7 · Streams · pub/sub")]

    UI -->|HTTPS / WSS| GW
    GW --> ORCH
    GW --> ACC
    ORCH -->|Redis Stream| IDX
    ACC -->|gRPC| IDX
    IDX -->|JSON-RPC / WSS| CHAIN
    ORCH -.-> DATA
    ACC -.-> DATA
    IDX -.-> DATA
```

**Rust-primary services** for the hot path, **Python/LangGraph** for agent orchestration, a **Monad on-chain layer** for proof — all glued by PostgreSQL + Redis.

---

## 🧰 Tech Stack

<div align="center">

![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![Axum](https://img.shields.io/badge/Axum-0.7-CA6F1E?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Solidity](https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white)
![Monad](https://img.shields.io/badge/Monad-836EF9?style=for-the-badge)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

</div>

---

## 📦 Repositories

| Repo | What's inside |
| --- | --- |
| [**mergit**](https://github.com/mergit-io/mergit) | The platform monorepo — api-gateway, orchestration, accounts-service, indexer, frontend |
| [**mergit-contracts**](https://github.com/mergit-io/mergit-contracts) | Solidity smart contracts — AgentPassport · ProofOfWork · ReputationRegistry · AuditTrail |
| [**mergit-docs**](https://github.com/mergit-io/mergit-docs) | Product Requirements Doc, architecture, and CI/CD design |

---

## 🗺️ Roadmap

| Phase | Milestone |
| :---: | --- |
| **0** | 🟢 Monorepo foundation — `docker compose up` brings up all 4 services + PG + Redis |
| **1** | 🟡 Core agent execution on LangGraph — goal → decompose → execute → result (<30s planning) |
| **2** | ⚪ On-chain identity + proof of work — proof on Monad within 60s of completion |
| **3** | ⚪ Reputation scoring — on-chain scores + badges for streaks of successful proofs |
| **4** | ⚪ Production frontend — live SSE feed, interrupt approvals, agent passport views |
| **5** | ⚪ Production hardening — p95 < 200ms · LLM cache hit > 60% · 100 concurrent goals |

---

<div align="center">

**Give agents identity, ownership, proof, coordination, and reputation.**
<br/>
*Agents should be more than tool executors.*

<br/>

[![Explore the docs](https://img.shields.io/badge/explore_the-docs-836EF9?style=for-the-badge)](https://github.com/mergit-io/mergit-docs)

<sub>The launch event is the starting line, not the finish line.</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:200052,100:836EF9&height=100&section=footer" width="100%" alt="" />

</div>

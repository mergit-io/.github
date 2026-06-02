## Summary

<!-- What does this change do? Link the issue: Closes #N -->

## Type of Change

- [ ] `feat` — new feature
- [ ] `fix` — bug fix
- [ ] `chore` — maintenance / dependencies / docs
- [ ] `contracts` — Solidity changes
- [ ] `infra` — infrastructure / CI / Docker / K8s

## Service(s) Affected

- [ ] `api-gateway` (Rust / Axum)
- [ ] `orchestration` (Python / LangGraph)
- [ ] `identity` (Rust / alloy)
- [ ] `blockchain-indexer` (Rust / alloy)
- [ ] `reputation` (Rust / Axum)
- [ ] `tool-server-github`
- [ ] `tool-server-code`
- [ ] `tool-server-search`
- [ ] `frontend` (React / TypeScript)
- [ ] `contracts` (Solidity / Foundry)
- [ ] `infra` / `libs`

## Checklist

**All changes**
- [ ] Tests added or updated
- [ ] No secrets committed (no private keys, API keys, or `.env` files)
- [ ] `ARCHITECTURE.md` updated if service topology or gRPC contracts changed

**Rust changes**
- [ ] `cargo fmt --check` passes
- [ ] `cargo clippy -- -D warnings` clean
- [ ] `cargo test --workspace --locked` passes
- [ ] `cargo audit` clean

**Python changes**
- [ ] `ruff check` and `ruff format --check` pass
- [ ] `mypy` passes
- [ ] `pytest --cov` passes with ≥80% coverage on changed modules

**Contract changes**
- [ ] `forge fmt --check` passes
- [ ] `forge build` succeeds
- [ ] `forge test -vvv --gas-report` passes
- [ ] `slither` output reviewed and findings addressed or documented
- [ ] `deployments/{chain_id}.json` updated if contracts redeployed
- [ ] Gas diff noted in **Blockchain Impact** section below

**Frontend changes**
- [ ] TypeScript type-checks clean (`tsc --noEmit`)
- [ ] Tested in browser against local dev stack

## Blockchain Impact

<!-- Fill in if contracts/ or blockchain-indexer/ or identity/ changed -->

- Contract redeployment needed? Yes / No
- New roles granted or revoked? Yes / No — if yes, list changes
- Oracle key path affected? Yes / No — if yes, security review requested
- Gas diff (if applicable):

| Function | Before | After | Delta |
|----------|--------|-------|-------|
|          |        |       |       |

## LangGraph / Orchestration Impact

<!-- Fill in if orchestration/ or tool-server-* changed -->

- New or modified graph nodes?
- Interrupt points added or changed?
- LLM prompt or caching strategy changed?
- New tools added to tool servers?

## Test Plan

<!-- Steps to verify this change manually against `docker compose up` -->

1.
2.
3.

## Evidence

<!-- Monad explorer link for on-chain changes, UI screenshot for frontend, curl output for API changes -->

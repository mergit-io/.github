## Summary

<!-- What does this change do, and why? Link the issue: Closes #N -->

## Type of change

- [ ] `paper` — correction, derivation, or new section in the research
- [ ] `docs` — requirements, README, or other prose
- [ ] `feat` — new functionality
- [ ] `fix` — bug fix
- [ ] `contracts` — Solidity
- [ ] `chore` — dependencies, tooling, CI

## What I verified

<!--
Be specific, and say what you did NOT check. "Derivation re-done by hand, numbers in the table not
recomputed" is a complete and useful answer. An unverified claim presented as verified is the exact
failure mode this project exists to fix.
-->

- Verified:
- Not verified:

## Checklist

- [ ] One concern per PR — this change does one thing
- [ ] No secrets committed (no private keys, API keys, `.env` files, mnemonics)
- [ ] Claims in the diff are supported by something a reviewer can check

**If this touches the paper**
- [ ] Citation numbers resolve against `paper/research.md` (that register is the only place numbering changes)
- [ ] Every new citation is marked `VERIFIED` or `TO VERIFY` — nothing unchecked is presented as confirmed
- [ ] `paper/whitepaper.md` updated if the change affects anything it also states
- [ ] Nothing is claimed as measured — the project is pre-implementation

**If this touches contracts**
- [ ] `forge fmt --check`, `forge build`, `forge test -vvv` pass
- [ ] Gas diff noted below if a public function changed
- [ ] Security implications stated, or explicitly "none"

**If this touches the runtime**
- [ ] Tests added or updated
- [ ] Receipt format changes are backward-compatible, or the break is called out below

## Evidence

<!--
Paste what backs the change: test output, a recomputed number, a quote from the cited source with
its page or section, an explorer link for an on-chain change, a screenshot for UI.
-->

## Breaking changes / follow-ups

<!-- Anything a reader should know next. "None" is a valid answer. -->

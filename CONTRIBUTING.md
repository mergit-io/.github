# Contributing to Mergit

Mergit is **pre-implementation**. There is no runtime to patch yet, and that shapes what is
useful to contribute right now.

## The most valuable contribution today is a correction to the paper

The whole project rests on an argument: that agent work cannot be verified by re-execution, and
that attested receipts plus cost-adjusted reputation are the right response. If that argument is
wrong somewhere, we would rather find out from you than from a reviewer.

Especially welcome:

- **A mechanism that breaks.** A deviation that profits an agent under our stated conditions, a
  case where the deterrence inequality does not bind, a Sybil or collusion path we missed.
- **Prior art we failed to cite or mis-positioned.** If an existing protocol already does what we
  claim is novel, that is the single most useful issue you can open.
- **Derivation errors** — the audit-rate condition, the concurrency cap, the value-density
  posteriors, the worked numbers.
- **Over-claiming.** If a sentence reads stronger than the evidence behind it, say so. The paper's
  §13 exists because this failure mode is the one we most want to avoid.

Open these on [**mergit-research**](https://github.com/mergit-io/mergit-research/issues) using the
*Paper correction* or *Mechanism challenge* form. Quote the section and line, and say what should
replace it.

## Code

When the rebuild starts, the runtime lands in [`mergit`](https://github.com/mergit-io/mergit) and
the Solidity in [`mergit-contracts`](https://github.com/mergit-io/mergit-contracts). Until a repo
has a README describing how to build it, assume it is not ready for patches — open an issue first
and ask.

The archived [`Mergit-proto`](https://github.com/mergit-io/Mergit-proto) is **not** accepting
feature work. It is kept as a record of the v0 execution model.

## Ground rules

- **One concern per issue or PR.** A correction to §7 and a correction to §9 are two issues.
- **Link the issue from the PR** (`Closes #N`) and fill in the template honestly — a checkbox you
  did not verify is worse than an unchecked one.
- **Never commit secrets.** No private keys, API keys, `.env` files, or wallet mnemonics. Anything
  committed is assumed compromised and must be rotated, not just reverted.
- **Say what you did not check.** "Tested locally, not against a live service" is a complete and
  useful statement. Claims presented as verified when they were not are the exact failure mode this
  project is about.

## Licensing

By contributing you agree your contribution is licensed under the terms of the repo you are
contributing to. Check its `LICENSE` — the code repos and the research repo are not under the same
licence.

## Security

Do not open a public issue for a vulnerability. See [SECURITY.md](SECURITY.md).

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

## Before you start work

**Claim the issue first.** This applies to anything already filed — do not open a pull request
against an existing issue without being assigned to it.

1. **Check that nobody beat you to it.** Look at open *and* recently closed pull requests for the
   same issue. A duplicate is wasted effort for you and review time for us.
2. **Comment on the issue** saying you want it, and say **how you intend to approach it** — which
   section or file you will change and what the change is. "I'd like to take this" without an
   approach is not enough to assign on, because for most issues here the approach *is* the
   disagreement.
3. **Wait to be assigned.** Once you are, the issue is yours.
4. **Say so if you stop.** Unassigning yourself is not a failure; silence for a couple of weeks
   means we reassign it.

For something not yet filed, open the issue first and propose it there. An unsolicited pull request
that rewrites an argument is very likely to be closed, not because it is wrong but because the
decision it changes was made somewhere we can point at.

## What we close as not planned

Reviewing a claim costs more than making one, so submissions that cannot be acted on are closed
rather than left open:

- **Unverified claims presented as fact.** "This citation is wrong" without the source, or a
  correction to a derivation without the working.
- **Ambiguous reports.** No section reference, no quote, no reproduction — anything we would have
  to guess at to act on.
- **Unrelated or out of scope.** Changes to the archived prototype, speculative features, or work
  on a repo whose rebuild has not started.
- **Duplicates**, including of a closed issue that was already decided.
- **Pull requests against an unassigned issue**, per the section above.

**One deliberate exception: a labelled hypothesis is welcome.** A mechanism challenge is a
conjecture by nature — "I think this deviation profits an attacker, here is my arithmetic, I am not
certain about assumption X" is exactly the contribution we want, and it will not be closed for
being uncertain. What gets closed is uncertainty presented as certainty. Say which parts you
checked and which you did not, and the submission stands on that.

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

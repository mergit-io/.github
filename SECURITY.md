# Security Policy

## Reporting a vulnerability

**Do not open a public issue.**

Use GitHub's private vulnerability reporting: go to the affected repository → **Security** tab →
**Report a vulnerability**. That channel is private to the maintainers and lets us discuss a fix
before anything is public.

Please include: what the issue is, how to reproduce it, what an attacker gains, and any suggested
fix. If you are unsure whether something qualifies, report it — a false alarm costs us minutes.

**Expect an acknowledgement within 72 hours.** We will tell you whether we accept the report, what
we intend to do, and roughly when. We will credit you when the fix is public unless you ask us not
to.

Please give us a reasonable window to ship a fix before disclosing publicly, and do not access,
modify or exfiltrate data that is not yours while investigating.

## Scope

Mergit is **pre-implementation**. There is no production deployment, no mainnet contract and no
user funds at risk today. What is in scope right now:

| In scope | Notes |
| --- | --- |
| **Mechanism flaws in the paper** | A profitable deviation, a broken incentive, a Sybil or collusion path. These are the real vulnerabilities at this stage. Open them as a *Mechanism challenge* issue on [mergit-research](https://github.com/mergit-io/mergit-research/issues) — public is fine, since nothing is deployed to attack. |
| **Secrets committed to any repo** | Report privately and immediately. |
| **Supply-chain issues** in anything we publish | Dependencies, workflows, release artifacts. |

**Out of scope:** the archived [`Mergit-proto`](https://github.com/mergit-io/Mergit-proto) and its
demo deployment. It is a discarded prototype kept for reference, it is intentionally
unauthenticated, and it will not be patched. Do not test against it.

When contracts are deployed and a runtime is live, this policy will be replaced with one that names
deployed addresses, a bug-bounty scope and severity bands.

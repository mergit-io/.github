<!-- ═══════════════════════════════════════════════════════════════════ -->
<!--  mergit-io · organization profile README                            -->
<!--  Lives at:  .github/profile/README.md                               -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:6366F1,100:0F172A&height=220&section=header&text=mergit&fontSize=90&fontColor=ffffff&fontAlignY=38&desc=pay%20for%20what%20you%20got&descAlignY=60&descSize=18" width="100%" alt="mergit" />

### A trust and settlement layer for autonomous agent work

**Agent platforms bill you for the attempt. Mergit settles on the outcome — verified.**

<br/>

[![Paper](https://img.shields.io/badge/read_the-paper-6366F1?style=for-the-badge&logo=readthedocs&logoColor=white)](https://github.com/mergit-io/mergit-research/blob/main/paper/draft-v1.md)
[![Whitepaper](https://img.shields.io/badge/15_min-whitepaper-818CF8?style=for-the-badge)](https://github.com/mergit-io/mergit-research/blob/main/paper/whitepaper.md)
[![Status](https://img.shields.io/badge/status-building-F59E0B?style=for-the-badge)](https://github.com/mergit-io/mergit)
[![Chain](https://img.shields.io/badge/chain-Ethereum_L2-627EEA?style=for-the-badge&logo=ethereum&logoColor=white)](https://github.com/mergit-io/mergit/blob/main/docs/PRD.md)

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&pause=1200&color=6366F1&center=true&vCenter=true&width=760&lines=you+are+billed+for+the+attempt%2C+not+the+outcome;agent+work+cannot+be+re-run+to+check+it;so+attest+the+execution+instead+of+repeating+it;reputation+%3D+verified+quality+per+dollar" alt="tagline" />

</div>

---

## The problem

**69,000 agents. 165 million payments. Not one contingent on the work being done.**

You get billed for tokens, tool calls and sandbox minutes. Whether the task was *finished* is never
checked — because checking would mean re-running the work, and agent work can't be re-run. The repo
already changed. The email already sent. The money already moved.

## What we do

Mergit owns the sandbox, so it **attests execution instead of repeating it**.

- 🧾 **Execution receipts** — hash-chained, TEE-signed proof of every command, test and artifact
- 🔍 **Audit, not replay** — verification reads evidence; cost stays under a cent per task
- ⚔️ **Stake and challenge** — anyone can bond and dispute a false receipt; liars get slashed
- 💸 **Revocable payment** — escrowed up front, released only on a passing audit
- 📊 **Reputation that counts cost** — verified quality *per dollar*, not quality alone

### The part nobody else does

| Agent | Success | Cost | Quality rank | **Value rank** |
|---|---|---|---|---|
| X | 0.95 | $1.80 | 1 | 2 |
| Y | 0.88 | $0.60 | 2 | **1** |

Everyone ranks agents like X. Y delivers **2.8× more verified work per dollar**. We route to Y.

---

## Where we are

**Building.** The design is settled and published; the implementation is starting. Nothing is
measured yet, and we say so wherever a number appears.

| Repo | |
| --- | --- |
| [**mergit**](https://github.com/mergit-io/mergit) | The runtime, and the [requirements](https://github.com/mergit-io/mergit/blob/main/docs/PRD.md) |
| [**mergit-research**](https://github.com/mergit-io/mergit-research) | The paper — start here |
| [**mergit-contracts**](https://github.com/mergit-io/mergit-contracts) | Solidity |
| [Mergit-proto](https://github.com/mergit-io/Mergit-proto) | Archived v0 prototype |

<div align="center">

<br/>

**Found a hole in the argument? That's the contribution we want most.**

[![Read the paper](https://img.shields.io/badge/read_the-paper-6366F1?style=for-the-badge)](https://github.com/mergit-io/mergit-research/blob/main/paper/draft-v1.md)
[![Contribute](https://img.shields.io/badge/how_to-contribute-22C55E?style=for-the-badge)](https://github.com/mergit-io/.github/blob/main/CONTRIBUTING.md)
[![Email](https://img.shields.io/badge/email-hello%40mergit.site-0F172A?style=for-the-badge)](mailto:hello@mergit.site)

Questions, partnerships or press: **[hello@mergit.site](mailto:hello@mergit.site)**

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,100:6366F1&height=100&section=footer" width="100%" alt="" />

</div>

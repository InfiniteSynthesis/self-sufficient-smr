<h1 align="center">State Machine Replication Among Strangers,<br/>Fast and Self-Sufficient</h1>

<p align="center">
Juan Garay<sup>1</sup>, Aggelos Kiayias<sup>2,3</sup>, Yu Shen<sup>2</sup>
</p>

<p align="center">
<sup>1</sup>Texas A&M University
<sup>2</sup>University of Edinburgh
<sup>3</sup>IOG
</p>

<p align="center">
    <a href="http://creativecommons.org/licenses/by/4.0/"><img src="https://img.shields.io/badge/License-CC--BY--4.0-bb6688.svg?style=for-the-badge&labelColor=884499" alt="License"></a>
    <img src="https://img.shields.io/badge/Proceedings-CRYPTO 2025-8888cc.svg?style=for-the-badge&labelColor=884499" alt="Proceedings">
    <a href="https://eprint.iacr.org/2025/616"><img src="https://img.shields.io/badge/Full-Version-ccaa88.svg?style=for-the-badge&labelColor=884499" alt="Full Version"></a>
</p>

> [!NOTE]  
> This repository contains the LaTeX source code of "State Machine Replication Among Strangers, Fast and Self-Sufficient." An abridged version of this paper appears in _Proc. CRYPTO 2025_.

## :books: Abstract

A set of unacquainted parties, some of which may misbehave, communicate with each other over an unauthenticated and unreliable gossip network.
They wish to jointly replicate a state machine $\Pi$ so that each one of them has fair access to its operation.
Specifically, assuming parties' computational power is measured as queries to an oracle machine $H(\cdot)$, parties can issue symbols to the state machine in proportion to their queries to $H(\cdot)$ at a given fixed rate.
Moreover, if such access to the state machine is provided continuously in expected constant time installments we qualify it as _fast fairness._

A _state machine replication_ (SMR) protocol in this _permissionless_ setting is expected to offer consistency across parties and reliably process all symbols that honest parties wish to add to it in a timely manner despite continuously fluctuating participation and in the presence of an adversary who commands less than half of the total queries to $H(\cdot)$ per unit of time.

A number of protocols strive to offer the above guarantee together with fast settlement --- notably, the Bitcoin blockchain offers a protocol that settles against Byzantine adversaries in polylogarithmic rounds, while fairness only holds in a fail-stop adversarial model (due to the fact that Byzantine behavior can bias access to the state machine in the adversary's favor).
In this work, we put forth the first Byzantine-resilient protocol solving SMR in this setting with both expected-constant-time settlement and fast fairness.
Furthermore, our protocol is **self-sufficient** in the sense of performing its own time keeping while tolerating an adaptively fluctuating set of parties.

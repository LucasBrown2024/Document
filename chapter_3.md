# Problem Statement

Traditional blockchain platforms offer security and decentralization but are often plagued by inherent limitations in scalability and efficient transaction processing. This issue is particularly noticeable in the context of fully onchain blockchain gaming, where the demand for rapid state updates, high transaction throughput, and modularity is critical.

Previous efforts to incorporate sharding in blockchain structures mainly faced obstacles due to insufficient infrastructure, including a lack of robust mechanisms to maintain state consistency and facilitate effective communication between shards.

Scalable sovereignty is one of the most important requirements for games, especially FOCGs (free-to-own and creator gas-efficient games). We understand it's extremely difficult to build a successful game. It would be even harder if, after finally obtaining decent user engagement, the chain grinds to a halt due to an NFT launch in which the entire gas limit is consumed by minting transactions. Therefore, it is crucial that a game can effectively have its own dedicated blockspace if it chooses to. Since FOCGs naturally require more blockspace to run, it is increasingly vital for each game to have its own sovereign scalability.&#x20;

At the same time, composability cannot be compromised since it is one of the most important reasons for building a fully onchain game. Having community-building User Generated Content (UGC) such as metagames and tools that sustain value is only possible if all the logic and state of the game are available in a trustless and modular way onchain. Effectively, the game should maintain composability with other ecosystem parts. Games should resemble countries on the same planet where tourists, builders, and traders can travel between them seamlessly and leave their unique mark.

The only way to ensure scalable sovereignty and composability is via sharding, with optimization on cross-shard communication and effective settlement. Historically, sharding implementations encountered several challenges:

* **Cross-Shard Communication**: Ensure the efficient and reliable processing of transactions that involve multiple shards.
* **Data Consistency**: Maintain a unified view of the state across various shards without incurring prohibitive overheads.
* **Infrastructure Overheads**: Implement a complex sharded system with adequate support for seamless operation and maintenance.

These challenges often led to fragmented ecosystems, where the potential scalability advantages of sharding were offset by increased complexity and decreased overall system efficiency.

Lastly, the tooling and developer kits for onchain gaming are limited at best.

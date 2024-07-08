#### Detailed Design of State Synchronization

The Shard-Sharing State revolutionizes how states are managed and synchronized in a sharded blockchain environment, employing two distinct yet complementary mechanisms:

1. **State Synchronization Between Adventure Layer L2 and Shards**:

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXdWJxhUj9m0prWr1eOXTTYOiH7BiCcInWWDvniCV4MoBJhH1jJ1zp4Yd0GY8PCVLAcvlboNAf4M0IeBqN1Kgb_CskWp7RXO5yH9rA5bU8iUI7mnjMdnIA82fZd77TLhQjsz5Gp2jIFQlbwsAg59?key=MX1cCxpr6-qyzTQezewHqQ)

**State Cache Module**: Positioned atop the state database, this module acts as an intermediary that intercepts storage access commands (SSTORE/SLOAD). When a shard accesses storage, it first queries the state cache module to check if the required state is already cached. This mechanism ensures that the most recent state from L2 is available to the shards in a read-only format to maintain data consistency and prevent direct shard-to-L2 state modifications.

This design allows smart contracts deployed on shards to access and process L2 assets, like reading balances, without risking the consistency of the L2 state. It provides a real-time, consistent view of the L2 state across all shards, enhancing the responsiveness and dynamism of gaming and other applications on **The Adventure Layer**.

2. **State Synchronization Among Shards**:

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXcPuqTweEFZS0C4nBfbbHUj3cOkffh-v16AHh32PFBY2yzWuExAaAaqdOf97dICvSYPkzuovcGdlq_i4HNsJZaxcqLxYPLkENhZ2K3sbhJlwOSwCLEZcwhNx8LPWonFG_iIFAncRn4LSMZONr7bVQ?key=MX1cCxpr6-qyzTQezewHqQ)

**Shared State Smart Contract**: A specialized smart contract on L2 allows developers to create shared addresses. These addresses facilitate a controlled state-sharing mechanism across shards. A shard that "borrows" a shared address gains write access to the associated state, ensuring that only one shard can modify the state at a time. Once the state is released, another shard can borrow and modify it.

This innovative approach maintains state integrity and allows for efficient, dynamic sharing of state information. It empowers developers to design more complex, interactive applications that require state interactions across multiple shards, such as large-scale decentralized games or interconnected financial services.

  
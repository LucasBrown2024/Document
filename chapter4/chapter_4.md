## Architecture of The Adventure Layer

### The Adventure Layer as an Optimistic Rollup

**The Adventure Layer** is built upon an optimistic rollup framework chosen for its efficiency and compatibility with Ethereum L1. This layer serves as the base where transactions are batched and executed off-chain, with final state commitments made on Ethereum L1. This setup ensures that the core operations benefit from the security of the main Ethereum network while operating at greater speed and at a lower cost.

### Validator Dynamics within The Adventure Layer

Validators validate both L2 and the shards for **The Adventure Layer**:

- **Validating L2**: Validators validate the transactions and state transitions on the L2 optimistic rollup.
    
- **Validating Shards**: Validators validate the transactions within local shards.
    

The integrity of this dual-validation mechanism is maintained through a rigorous incentive system:

- **Rewards**: Validators receive rewards for each successful validation, encouraging them to accurately process transactions and state transitions.
    
- **Slashing**: Validators stand to lose a portion of their staked tokens if they fail to correctly validate either the L2 or any of the localized shards, ensuring a high degree of accountability.
    

### Shard-Sharing State: A Novel EVM Sharding Infrastructure

**The Adventure Layer** introduces the **Shard-Sharing State** to overcome traditional challenges with sharding, such as interoperability and state consistency. This innovative sharding infrastructure is native to **the Adventure Layer** L2 but facilitates seamless read/write operations across both the L2 and individual shards. The Shard-Sharing State significantly enhances interoperability and allows for efficient state management across the network.

### Data Availability and State Settlement

Shards within **The Adventure Layer** utilize blob storage for data availability (DA), ensuring data integrity and accessibility with minimal gas costs. Each shard's state root is committed to **the Adventure Layer** L2, using the optimistic rollup mechanism. This approach not only secures the data but also aligns it with the overall state of the network, maintaining coherence and reliability.

#### Design of the Parallel Ticking System

The Parallel Ticking System is structured to maximize the computational efficiency and scalability of the gaming environment in **The Adventure Layer**. Here’s how the system is designed:

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXdEpXXV_-ZZcaag3KmLh7aNzUdZaMfXmjtI06TjOR4r9Tk1fcHU_Xii5Nip6WHvK2YCx4ot4YxoKEza-8LwwEz4AX2c2fEADZSMCQK8UxuszGfh3IovpzmgweofKGCHK9NwOXgcBSdkN-IA1JjsFg?key=MX1cCxpr6-qyzTQezewHqQ)

  
1. **Namespace-based Component Storage**:

   - Each game component is instantiated with a unique global namespace within a Merkle tree-like storage structure. Each entity within the game has a designated namespace, and all properties and states related to that entity are initialized under this namespace. This arrangement ensures organized and secure data management.

2. **Stateless Component Design**:

   - Each component operates as a stateless program, taking its namespace as input. The output from each component is a vector of state changes restricted to its own namespace and events that may interact with different namespace components. This design ensures that each component's logic is self-contained, enhancing reliability and ease of updates.

3. **Parallel Component Ticking**:

   - The ticking process, which updates component states, occurs in parallel across all shards within **The Adventure Layer**. At the start of each block, validators collect all components requiring ticking services for that frame. Since each component accesses only its namespace state, there are no conflicts during execution, allowing for true parallel processing.

4. **Sorting and Application of Changes**:

   - Once the parallel ticking has been executed, the resulting group vectors of state changes and events are sorted and systematically applied to the appropriate components in the storage system. This step ensures that all state transitions are handled accurately and efficiently.

5. **Performance Optimization**:

   - By implementing the Parallel Ticking System, **The Adventure Layer** fully utilizes the multicore architecture of modern servers. This allows the shards to run active game logic while retaining ultra-high performance, which is crucial for maintaining fluid and responsive gameplay in complex onchain games.

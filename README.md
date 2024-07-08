# **The Adventure Layer - Technical Proposal**

## Introduction

The traditional web2 gaming market, with global annual sales of over $400Bn, is larger than the film and music industries combined. Thus, it’s no surprise that gaming-specific blockchains have been a well-researched area, pioneered by companies such as ImmutableX ($5Bn market cap), Ronin ($3Bn), Beam ($2Bn), Oasys ($1Bn), and WAX ($250M). Noticeably, though, they all compromise on security or decentralization in favor of the scalability needed in gaming. The scalability trilemma is a complex problem to solve, after all. Beyond scalability, most of the existing gaming-specific blockchains did not architect for the rise of fully onchain games(FOCGs), the new chapter of blockchain gaming that many crypto experts like Paradigm have written [pieces](https://www.paradigm.xyz/2023/08/onchain-games) about.

At Adventure Gold DAO, we are the first to launch a blockchain specific for fully onchain gaming. Our roots stem from Loot, the first composable NFT issued on August 27th, 2021, by Dom Hoffmann. Adventure Gold ($AGLD), which governs the DAO, is the token behind Loot and was airdropped to owners of the Loot NFTs on August 29th, 2021, as an entirely fair launch token. Since its inception, AGLD has inspired a community of fully onchain games and autonomous world builders. The token is traded on exchanges like Binance, Coinbase, Upbit, and OKX. AGLD has been the subject of research from [Coinbase](https://www.coinbase.com/en-sg/learn/market-updates/around-the-block-issue-17), [Bybit](https://learn.bybit.com/altcoins/what-is-adventure-gold-agld-loot-nft-project/), and more.

Adventure Gold DAO’s first blockchain built in 2023 was Loot Chain, which was the world’s first chain dedicated to FOCGs and aimed to bring sovereignty to the Loot and AGLD communities. Despite our limited resources as a fully decentralized DAO with zero VC backing or a functional treasury, we were committed to solving scalability & adoption for users of fully onchain games. Building Loot Chain, an L2 built with Caldera on the OP stack using Polygon as the DA layer, helped us realize the massive underserved market for developers building for this new chapter of web3. 

A FOCG executes all of its state transitions and logic on a blockchain, usually represented via changes in the ECS system. This means the entire world state, updated via a ticker system, runs on a distributed ledger. A player's every move, win, and loss are onchain. A developer’s every modification to the game is also onchain. We realized that Loot Chain was a good start, but we needed to build a much more scalable and developer-centric Layer 2 blockchain that could grow alongside this new sector for the next five years. Thus, **the Adventure Layer** was born - an Ethereum Layer 2 that implements several designs that are tried and true in existing L1s and L2s while also adding innovative designscustom-made for FOCGs. 



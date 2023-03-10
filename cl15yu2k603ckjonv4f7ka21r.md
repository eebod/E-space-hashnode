---
title: "The Blockchain Trilemma"
datePublished: Sun Mar 20 2022 18:02:37 GMT+0000 (Coordinated Universal Time)
cuid: cl15yu2k603ckjonv4f7ka21r
slug: the-blockchain-trilemma
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1674487253813/863d8fe9-9b41-4071-97ce-c350fbe7d72a.png
tags: blockchain, bitcoin, ethereum, web3, decentralization

---

> In the beginning, was a block, the chain was good but the blockchain shied away from perfection.

Earlier we touched on Blockchain technology, its types, its use cases, and the possible improvements it would bring into the tech space in the coming years.

Like everything or any technology, perfection is impossible. In this article, we discuss the three major properties(scalability, security and decentralization) the blockchain attempts to have at the same time but that remains elusive, mainly due to its design structure and the type of service it offers.

The inability of a blockchain system to equally cover or have all of the three earlier properties mentioned is known as the 'Blockchain Trilemma'. Vitalik Buterin(Co-Founder of Ethereum) described the trilemma as a situation where a blockchain can't be decentralized, secured and at the same time highly scalable, instead, certain properties are reduced or increased to create balance. This statement has been heavily contested, but in the end, it stayed proven and true.

💡| Ethereum is one of the most active blockchains. It is, has and is still being battle tested. The devs in charge, take a great deal of caution and precaution making core changes.

## THE TRILEMMA

The perfect blockchain has the best security, scales easily and is fully decentralized. But just like an individual in real life, we don't get to have everything, how we manage what we have and strive for better defines us. This analogy resonates with what's happening in the blockchain space. Let's go over the properties a chain seeks to have.

### DECENTRALIZATION

This refers to the distribution of the blockchain network's power and decision-making authority among its participants, rather than having a central authority control the network. This allows for a more democratic and transparent system, as no single entity holds disproportionate power over the network. If a decision is to be made, there has to be a form of consensus(agreement).

### SECURITY

The blockchain has serious defense mechanisms in place against malicious actors, preventing them from doing stuff like overwhelming the network(a 51% attack) to manipulate data and then going ahead to cause things like a double spend and other possible attack varieties. For the blockchain to be really useful, it has to guarantee a certain level of security while still being decentralized.

### SCALABILITY

This is the ability of the chain to handle an increase in the number of participants on the network and also an increase in the number of activities (mostly transactions) at any time. As the use case of the technology increases, adoption and user activities on the network increase and in a correctly working environment, performance and efficiency should likewise increase. That's what being scalable means.

## WHERE THE PROBLEM COMES KNOCKING

Now you'll probably ask, why can't the all-powerful and supreme blockchain technology have all three of that? Glad you asked;

Decentralization is the backbone of blockchain technology, it gives everyone a hand in the decision-making process. Although giving every and anyone the power to make decisions, also comes with its downsides.

No one on the network can be trusted. Securing a decentralized system comes with its own set of complexities. One of these is making sure every participant on the network gets updated in near real-time with actions by other participants on the network to enable them to take part in the validation process. The problem is, the more participants come on the network, the more transactions are made, and the heavier the load on the network becomes to process, validate and propagate transactions across the network quickly enough.

If the technology cannot keep up with traditional centralized systems or at certain points beat the system, the possibility of adoption looks bleak. But alas! Different solutions attempting to handle the problems have and are been developed.

## Solutions to the Trilemma problem

Different blockchain implementations have different teams of developers behind them. Everyone doesn't think in the same direction, which is a good thing in this case, as the problem creative and diverse approach.

In solving the trilemma problem, a lot of Innovative ideas and solutions have come around, we'll touch on different approaches to a solution briefly.

Currently, most of the solutions available fall under two major categories;

* LAYER-1 (L1) solutions
    
* LAYER-2 (L2) solutions
    

### LAYER-1 solutions

These solutions are implemented directly on the main blockchain's protocols. By 'main' blockchain, I mean the base/primary blockchain network. Examples of these chains include but are not limited to Bitcoin, Ethereum, Litecoin, Solana, Cardano, and Elrond. Some of the solutions applied in this layer include:

\[-\] **Improving the Consensus Protocol** The use of the proof-of-work consensus model is not favored, due to its computational difficulty. The more participants join the network, the more complex the operations required to run the network become. This increases the barrier of entry to becoming a miner or taking part in the network, killing decentralization. Hence blockchains tend to either transition to Proof-of-Stake or other consensus mechanisms, to reduce their computational complexities and lower the barriers of entry and promote decentralization.

\[-\] **Sharding** In the blockchain context, it means breaking large transaction data into smaller datasets called "shards". In doing this, the network doesn't make each participant hold all the data from the genesis block on the network, instead, it is split up and shared across specifically designed Nodes. This allows a different section of the network handle different transactions and data at different periods. When sharding is implemented, a system is built to monitor and keep all the shards across the nodes in sync with each other. In the case of Ethereum, the system that does that is the Beacon Chain.

### LAYER-2 solutions

A blockchain "layer 2" solution refers to a technology built on top of an existing blockchain network that aims to improve scalability and speed without compromising the security provided by the underlying blockchain.

For example, a layer 1 blockchain is Bitcoin, which has a relatively slow transaction processing time and high fees. A layer 2 solution like the Lightning Network is then built on top of the Bitcoin blockchain to allow for faster and cheaper transactions without compromising the security of the underlying blockchain.

Another example is Ethereum's layer 2 scaling solution, which is used to offload some of the computational and storage load from the base layer of the Ethereum blockchain, by moving some of the workloads to a separate layer.

Examples of layer-1 solutions are detailed below.

\[-\] **Sidechains** sidechains are blockchains that are attached to the main chain. This makes it possible to move digital assets, such as coins or tokens, back and forth between the two chains. They are used to handle large numbers of transactions. Most sidechains use an independent consensus mechanism unlike that of the main chain to optimize for speed and scalability. They allow for more flexibility and scalability, as well as the ability to test new features without disrupting the main blockchain network.

\[-\] **Rollups** Rollups allow networks on Ethereum’s blockchain to “roll up” multiple transactions off-chain(that are validated) and then submit the rolled-up data to the main chain. Rollups reduce the data and computational power needed for multiple transactions on the main chain by merging multiple transactions that are not on the main chain into one and then posting it on the main chain. It also reduces traffic and enhances speed.

\[-\] **Polkadot: Relay and Parachain** Polkadot came up with a new idea and approach to the trilemma in the blockchain space. Instead of being a single blockchain solution, it embodies the implementation of an l1 and l2 solution as its default features. There is the relay chain, which is the backbone of the network and offers high scalability, then there are multiple parachains, which are themselves also independent blockchains but connect and communicate with the relay chain. Multiple smaller blockchains(parachains) operate independently in their decision-making process and can scale easily, but they all converge at the feet of the relay chain for security and top-level validation.

This idea of relay and para chains comes off as an exciting way to handle the trilemma. It also does feel like something from a movie. If you've watched Avatar(James Cameron), the Tree of Souls, where all things come to unite, even though they can be independent, that's the vibe being given off here.

Yeah, it's been a very lengthy article on the trilemma, I hope it was worthwhile and you found it useful.
---
title: "Blockchains and Oracles"
datePublished: Sun Mar 27 2022 02:05:10 GMT+0000 (Coordinated Universal Time)
cuid: cl1mxllxc01n34wnvap4khso1
slug: blockchains-and-oracles
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1650267249077/5vn21AioC.png
tags: oracle, blockchain, bitcoin, ethereum, web3

---

There is this African saying; (more likely Yoruba) ::&gt;

> A single tree can't make a forest

This also goes for a blockchain network. A stand-alone chain/network is only as powerful as the data it can handle. As blockchains attain the computationally powerful helm, it would be a bummer if they could not communicate with other chains or the real world for live data.

This article aims to touch on what an oracle is(in the blockchain context), its use cases, and a little on the types of oracles.

### What is an Oracle?

An Oracle is a bridge between on-chain data and off-chain data in a blockchain network. The next question that would pop up then would be, what are off or on-chain data and what do they do?

* **On-Chain Data**: In a previous [article](https://ebode.hashnode.dev/what-is-blockchain-technolgy), we talked about the structure of the blockchain and how it works. On a blockchain network, some nodes participate in creating and validating transactions and also keeping the network safe. Most blockchain networks are built to guarantee uniformity. Uniformity in this context means everyone has the same data, therefore they can all agree on how to move forward(Consensus). If the data available to participants on the network for one reason or the other goes out of sync, multiplied across the possible thousands of nodes on the network, chaos would rip through the network and break it down.
    
    This data available within the blockchain network is the on-chain data. The on-chain data consists of all information written into blocks, most of which are transactional data(user A transferred D amount to user B ) 'A, D and B' are data. There is also the block's metadata( information about a block in the blockchain ), all of this makes up the data on the chain(on-chain).
    
* **Off-Chain Data**: It's any data that comes from the outside world (outside the blockchain network). Off-chain data is not limited to anything as long as it can be computed and transferred, it is valid. Examples of off-chain data include::
    
    **\[-\]** Total number of astronauts aboard the International space station and their names.
    
    **\[-\]** Long Tennis player's global ranking and their points.
    
    **\[-\]** Scores from a football match
    
    **\[-\]** Prices of stock and assets in the real world.
    
    Almost any type of data from the real world can be regarded as off-chain data. A simple definition of off-chain data is that it is information that cannot be generated or would rarely be created on the blockchain but rather gotten from outside it.
    

Back to the definition of an oracle, it is an entity, program, tool, medium or bridge that brings data from the outside world onto the blockchain network.

### What's the need for Off-chain data on the blockchain?

Yeah, right. Why?

Initially, everyone was satisfied with how the first generation of blockchain worked(majorly Bitcoin). It made the transfer of value to anywhere in the world, possible and faster in comparison to banks, it also served as a store of value.

As humans, we always want things to be better and strive to improve things, this is good, as it is what fuels development. We realized Bitcoin had its limitations and developers began to make proposals to improve Bitcoin's core structure. This created friction among blockchain developers and eventually lead to the creation of multiple factions, one of which is Bitcoin cash. Developers eventually agreed to build on top and around Bitcoin, but not rebuild.

Things like colored coins popped up, the lightning network and other infrastructures/systems to extend Bitcoin capabilities. It was at this point Vitalik Buterin(co-founder of Ethereum), had the brilliant idea to create smart contracts(codes that lived and got executed on the blockchain). This brought about a paradigm shift in the blockchain space and gave it new powers. I am beginning to diverge away from the main point. I think I'll write about the generations of blockchain in the next article, for now, Let's get back to Oracles.

Off-chain data became important with the existence of smart contracts. It meant the blockchain wasn't just for recording transactions, developers could now write codes to perform tasks. Once the code(smart contract) is put up on the blockchain, it was nearly impossible to stop except explicitly determined by the creator at the time of creation. Executing a smart contract is as simple as interacting with its address.

This new shift meant developers could write smart contracts to do almost anything, but there was a big limitation, they could only use data that was available on the chain. Blockchains at the time were designed to be independent.

Problems like the absence of a source of true randomness(some dev tried finding ways around it, but most were vulnerable to exploits) and others popped up. They were left to use data from the chain. Some beautiful things happened in the space even with these limitations. Tokens became a thing, Fungible Tokens following the ERC-20 standards, Non-Fungible Tokens following ERC-721, etcetera. Decentralized exchanges came alive using Automated Market Makers, instead of order books(this enabled users to exchange their tokens), there were automated IEOs(Initial Exchange Offerings) and other creative innovations with smart contracts and on-chain data. There was more that could happen if there was a way for developers to get access to external data. Then this happened, Oracle came to the aid of mortal developers.

In essence, off-chain data brings a whole new range of possibilities to writing smart contracts. Oracles came around and it became possible to write Insurance smart contracts that settled individuals based on what happens in the outside world, betting on sports became a thing, and true randomness could now be gotten and used in games and programs like random NFT purchases, gambling(flipping a coin or dice on the chain), etcetera. One other important thing is that oracles also give smart contracts the ability to call APIs in the regular web2 world.

### A question

If we say the blockchain is decentralized(no central authority) and a smart contract is almost impossible to change when up there, and now smart contracts on the blockchain depend on Oracles who get data from a centralized world, isn't that defeating the purpose of decentralization? How do we trust the oracle? So many things could go wrong with smart contracts if an Oracle goes rogue.

Hey! easy, oracle developers have had those same thoughts and worries too. Almost everyone in space within the early Oracle days thought about this same issue too, and there happened to be a solution. They are called **'Decentralized Oracles'**. These oracles do not get their data from a single source, rather they aggregate data from across multiple sources and weigh them with the aid of algorithms to pick the most trusted data entry. This put everyone's fear to rest.

### How Oracles work

Oracles work almost the same way smart contracts do, they can talk to other smart contracts, they can be interacted with via their address and other contracts can place listeners to know when an event occurs or changes. One big difference between a regular smart contract and an Oracle is that it has a component that lets it talk to the outside world. In the case of Ethereum, it talks via JSON-RPC ( a communications protocol for Ethereum blockchain nodes).

To complete the communication channel, there is a system on the outside world that collects all real world data in a decentralized manner as we earlier discussed, and on a request, passes the data from the off-chain systems onto the listening smart contract on the blockchain network. Other smart contracts would then reach out to that smart contract to request and use its data at a fee. Examples of Oracle service providers include::

* [Chainlink](https://chain.link/)
    
* [Witnet](https://witnet.io/)
    
* [Provable](https://provable.xyz/)
    
* [Paralink](https://paralink.network/)
    
* [Dos.Network](https://dos.network/)
    

In summary, an oracle is a tool(the smart contract and the external data aggregation system) that allows smart contracts to access data or external events from outside the blockchain network. It acts as a bridge between the smart contract and the external world.

### Types Of Oracle

Due to the nature of the JSON-RPC commonly used by nodes to communicate, this means communication could go in two ways, into the blockchain network or out of the network, creating a range of possibilities.

* **Input/Inbound Oracles** :&gt;&gt; This type of oracle transmit data from external sources(real-world) into the chain, it's the most common way oracles are used.
    
* **Output/Outbound Oracles** :&gt;&gt; Data or commands are sent out, to real word systems( a listening computer ), which on receiving the data or command, triggers it to take an action. One example of such would be sending a command with data for a task that would be too computationally expensive to do on-chain, the result is later fed back on-chain after processing.
    
* **Cross-chain Oracles** :&gt;&gt; The oracles can both listen and send commands to more than one blockchain. This enables data sharing amongst different blockchains, making them interoperable.
    

We have come to the end of this article. This was just a scratch on Oracles, there's still so much involved, but the aim of the article was to subtly touch on oracles as smoothly as possible.
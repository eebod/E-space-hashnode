---
title: "What is Blockchain Technolgy"
datePublished: Sun Mar 13 2022 18:05:20 GMT+0000 (Coordinated Universal Time)
cuid: cl0pl7h1j00veyunvb3nl4se8
slug: what-is-blockchain-technolgy
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1674484284325/1e0c4a8f-8076-4d20-bf70-f763c3aa684c.png
tags: technology, blockchain, bitcoin, ethereum, web3

---

Let's start here;

> Bitcoin is not the BLOCKCHAIN

Bitcoin's pseudonymous creator(s) **'Satoshi Nakamoto'** brought to life the idea of a decentralized currency, built on blockchain technology. The currency system also uses other important technologies like Networking(peer-to-peer), Cryptography(Hashing and Digital signing), Agreement Logic(Consensus) and other systems to achieve its desired functionality. Therefore, I think it is safe to say, *'the Bitcoin system works on top of blockchain technology'*.

## What is Blockchain Technology

Technically, Wikipedia says:

* A blockchain is a growing list of records, called blocks, that are linked together using cryptography. Each block contains a cryptographic hash of the previous block, a timestamp, and transaction data (generally represented as a Merkle tree).
    

So what does all this mean? The word blockchain is made up of two parts, **block** and **chain**. The block in 'blockchain', describes a store with the ability to hold data(any type of data). In the case of Bitcoin, this block holds mostly transaction data, while on Ethereum(a higher-order blockchain system), the blocks hold both transactional data and also executable programs(a smart contract).

The chain defines how blocks are securely connected over a network, to ensure everyone on the network has access to the blocks and the data contained in them.

There are other components to a blockchain ;

**Miner** &gt;&gt; Depending on the consensus mechanism adopted, a miner can either operate on:

* **Proof of Work**; where every miner competes to find the next block by attempting to solve a complex mathematical problem with their computer/machine. Whichever miner finds a block first, writes a portion of transactions in the transaction pool into the block they found. Once the block is filled, it is verified across the network by other miners and the winning miner is either rewarded or punished.
    
* **Proof of Stake;** Here, the miners(more technically 'Validators') do not compete. They submit an agreed amount of money(a stake) in that cryptocurrency. The validators are then randomly selected in a supposed fair manner. The money submitted is used as a method of punishment, by either destroying half or a good amount to deter a chosen validator from acting irrationally and against the rules of the system, when filling transactions into the block
    

There are other consensus mechanisms;

1. Delegated proof of stake
    
2. Proof of space-time
    
3. Proof of Elapsed time
    
4. Proof of Capacity
    

**Nodes** &gt;&gt; They are computers on the blockchain network that solely store every transaction and data(metadata) for each block. They listen to miners to get block updates and also serve as storage for miners and non-miners to retrieve information about a block or a transaction. Back to the definition Wikipedia gave, there are certain words mentioned that we should go over;

**Cryptographic Hash** &gt;&gt; We wouldn't delve too much into computer science here, so this might be a little oversimplified. A cryptographic hash function is a term used to define a mathematical method that takes in any size of data and returns a fixed length of very very random and unique data as its output. A little or any change to the input changes the resulting output. One other thing to take note of is that the input(whatever you put in) must always give out the same output every time.

Below is an example of a sha256 hash function to explain better.

```bash
sha256('adunni');
>> 99DCA03A59525C5AEED4C3C018B37D1B596F697F9EE474EEA1A0666543B9E648
```

The result of using 'adunni' as the input to a sha256 function, is a random 256bits (64chacracters) output. This shows the randomness of a hashing function.

Bitcoin uses this same hashing function primarily but does the data hashing twice(double sha256).

```bash
sha256('Adunni');
>> C55C0C7C6BC033081D0DE5352742081680DBCE87F22881F1B6353EA8BAE0C954
```

Earlier I mentioned how a little change to a hashing function's input changes the output. In this case, I capitalized the first letter of the previous input( 'a' became 'A') and the content above shows how the resulting output changed. This shows the level of randomness and unpredictability of a hash function.

Another important feature of a hash function is that it is a one-way function. This means that it should be practically impossible to get back the input from the output, if I give you the hash **C555...C954** from above, you shouldn't be able to easily find out 'Adunni' was the input.

**Hashing and Blockchain**

The blockchain uses hashing as one of its core features to reduce the size of data moving across the network, create and manage keys, and handle digital signatures.

For block hashing, each block and its metadata is hashed and a fixed length output is gotten. The output of the hash becomes the pointer to the block, previously mined block can point to that reference and any block mined later ahead of it can also point back to the reference hash. If for any reason a bad actor tries to change something inside a block in the past, the resulting hash would be different and the system's protocol and other miners on the network would automatically spot and flag the bad actor.

**Timestamp &gt;&gt;** The blockchain's timestamp is data that is stored in the block metadata field, to determine when the block was mined or created and it is verified by the system. It functions to provide a type of security, as timestamps are monitored to determine and adjust block mining difficulty, which is based on the total mining power available on the network.

**Transaction Data &gt;&gt;** This is the main content of each block. The data stored in blocks refers to users' actions across the blockchain network. On the Bitcoin network, it is the transfer of X amount of coins from one user to another, on Ethereum, it is the transfer of Ether from a wallet address to another, it's also the execution of a program(smart contract) on Ethereum's network. on Storj and Filecoin networks, it is the storage and transfer of data across the network. What is regarded as an action on a blockchain-powered network is defined by the system.

Earlier on, we mentioned the 'Merkle tree'. A Merkle tree in the blockchain context is the hash of all the transactions in a block in order from the bottom to the top, the topmost hash is called the 'root hash'. This is useful to quickly and simply validate transactions in a block using its hash and the root hash. For blockchain efficiency, the Merkle root hash of all transactions in a block, instead of the hash, is what is carried in the header of the block ahead.

![Hash_Tree.svg.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647193153058/pID0zkg1T.png align="left")

I didn't plan to get this deep, but here we are. I'll try to reduce what comes next.

## Types of Blockchain networks

**Private Blockchain Network:** These networks implement the basic underlying blockchain technology components we mentioned earlier and more, but in this case, the network is not publicly accessible.

**Public Blockchain Network:** Bitcoin and other Cryptocurrencies operate on this type of network, making use of distributed ledger technology. Here, the network is available to everyone and anyone and a lot of standards are built to ensure the safe and orderly entry of data into the ledgers. Consensus Algorithms such as Proof of Work, Proof of stake, Delegated Proof of stake etcetera are implemented to fairly select the next miner or validator.

**Permissioned Blockchain Network** In a permissioned blockchain, majorly used on private networks, participants on the network are assigned different roles by a governing entity. Each member can only perform activities permitted by the roles they are assigned.

**Consortium Blockchains** This type of blockchain has both public and private components to them, but the major difference is that it is set up, organized and maintained by multiple organizations or collaborating companies, which allows them to share data and make transactions amongst themselves.

**SideChains** A side chain is another type of blockchain. It is a chain that doesn't run independently, instead, it runs dependent on another chain(a Main Chain). The side and main chain are connected via a bridge that goes both ways. It allows for the exchange of data between both chains. Side chains mostly exist to take some load off the main chain, but rely on the main chain for security.

## Blockchain Features

Most Blockchain but not all, have certain core characteristics to make them accessible and open to the public, and at the same time, keep transactions and activities happening on the chain within the bounds of sanity.

**Consensus** **\&gt;** Before data is written into a block and linked to the blockchain, the majority of the participant on the network have to agree.

**Finality** **\&gt;** An real-life scenario of finality would be that after paying for a frozen chicken at a store and it is cut, sealed and handed over to you, the purchase is final, and the chicken can't be returned. Except that this is Nigeria!! anything can happen, till that chicken is eaten.

That same idea is carried over to how blockchains operate, most transactions don't instantly attain finality, and this is dependent on the underlying network's design. In most cases, finality happens over time, 'probabilistic finality'. In this situation, the more blocks are mined atop the block in which a certain transaction is written, the more it becomes impossible to revert.

* Bitcoin is regarded as finalized after 6 blocks in depth(a block is mined every ~10mins, that's around 60mins for finality).
    
* BNB - 1 second (1 second per block, needs 1 commitment).
    

Some other blockchain network transactions attain instant or near instant finality(Absolute finality) ex:: Tendermint blockchain. There is also Economic Finality, this type of finality is dependent on value(money). Here, it is expensive/costly to revert a transaction. These are used in Proof Of Stake(POS) environments.

Reverting a transaction is considered malicious, so if a validator tries to do so and the system picks up the actor, their stake is slashed. This makes it gives finality an economic value. Examples of blockchains using Proof of Stake include Polkadot, Cardano and now Ethereum.

**Immutability** **\&gt;** This means, once data has successfully been recorded in a block and enough blocks have been mined ahead of that block to reach finality, that data can no longer be changed.

**Provenance** **\&gt;** A user can prove beyond reasonable doubt that something happened on the chain. This happens due to two main reasons, one is that blockchain data and transactions are public, and the other is that transactions require practically unforgeable signatures to be valid, so any finalized transaction, can be proven to have been intentionally carried out.

## Blockchain Use Cases

It's gotten long enough, so we'd gloss over it here, there are a lot of possible use cases for blockchain technology, those we can already see happening now and those we have no idea are coming.

* Cryptocurrency and digital payments: Blockchain technology is the backbone of many cryptocurrencies such as Bitcoin and Ethereum.
    
* A global and decentralized computing Infrastructure: Blockchain technology can be used to create self-executing contracts.
    
* Digital Identity Management: Blockchain technology can be used to create secure and decentralized digital identities
    
* IoT: Blockchain technology is used to secure and manage data from Internet of Things (IoT) devices.
    
* Gaming and digital collectibles: Blockchain technology is used to create unique, digital assets that can be bought, sold and traded.
    
* Healthcare: Blockchain technology can be used to securely store and share patient health information and medical records.
    
* Government: Blockchain technology can be used to create secure and transparent government services, such as voting systems and public record management.
    
* Banking and finance: Blockchain technology is increasingly being used in the banking and finance sector to streamline processes, reduce costs and enhance security.
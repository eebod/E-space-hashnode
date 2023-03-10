---
title: "Nakamoto's Consensus"
datePublished: Sun Apr 24 2022 03:55:23 GMT+0000 (Coordinated Universal Time)
cuid: cl4rx7ran056q9vnvcpju4u5d
slug: nakamotos-consensus
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1656043400294/u1XFzrxpi.png
tags: blockchain, bitcoin, ethereum, web3, decentralization

---

> How do you maintain order and sanity in an organization without a central authority, whilst still making sure the majority of everyone is on the same page??

Maintaining order in a system or environment without a centralized authority or governing body and where every individual within the system have equal power to make decisions and influence the direction of the network becomes a very complex task. This is the same dilemma decentralized systems face. The decentralized system has to ensure that even with the presence of malicious actors, it can still work efficiently and at some point, kick the bad actors off its network. There is also the problem of how to ensure all participants on the system/network agree on how to move forwards. The agreements make it such that all the participants have a consistent view of the state of the system, ensure there is no central authority to impose a single version of the truth and avoid confusion, mistrust, and ultimately, the failure of the system. This agreement is called a 'Consensus'.

**CONSENSUS**  
A consensus is simply a general agreement. A general agreement, wherein the majority of individuals within a group or system decide on a course of action. A simple example of this would be the process of how five roommates decide if the lights in the room should be turned off or on at night. For any decision to be reached, not less than three of the roommate must pick any one of the options.

Agreement within a decentralized system is exponentially tougher than in the example above. Here, participants are nodes across the network all over the world. Rules on how decisions can be made, the impact of decisions, and the requirements to participate in the decision-making process all have to be stated right from the onset.

A system like this should be able to handle a wide variety of cases, normal cases, malicious cases, incorrect cases, biased cases and other cases and scenarios. The first efficient, usable and accepted solution to succeed in being able to both handle such decision-making complexity and also continuously exist in a decentralized manner, was Bitcoin, which it implemented with its Nakamoto Consensus spelled out in its white paper.

![bitcoin's white paper.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655931350057/mV2djclqQ.png align="center")

The writing in Nakamoto's white paper proposed block selection and proof of work mechanism used in Bitcoin till today. It created a system to incentivize honest miners and also make the system trustless. The fact that bitcoin as a decentralized peer-to-peer electronic cash system is successful, answers the question asked at the beginning of this article and this article, goes on to explain how it was answered.

## NAKAMOTO'S CONSENSUS

The implementation of Nakamoto's Consensus is why bitcoin is trusted even though it's trustless. Nakamoto's consensus is a set of rules that verify the authenticity of a peer-to-peer network which is itself based on the Byzantine Fault Tolerance(BFT) model. BFT was born out of a logical problem, 'The Byzantine's General Problem', where a supposed set of Eastern Roman Empire Byzantine generals had to come up with a solution to handle combining forces in a war attack scenario, where communication might be a problem.

Take a look at the Byzantine Generals Problem paper [here](https://www.microsoft.com/en-us/research/uploads/prod/2016/12/The-Byzantine-Generals-Problem.pdf).

In this theory, generals at different geographical locations in the war had to make a coordinated decision to either attack or not attack a common enemy in war. A single general's army can't single-handedly attack and win the war, rather a joint force from all the army generals is required to secure a win. They had to all agree on either attack or not, once a decision is reached, it could not change and they also all had to attack at the same time and there was the possibility of having rogue generals. Looking at it, the problem centered around communication. How would they all communicate with each other quickly enough, securely and be sure every general got the message?

Applying this to the Blockchain's context, the generals are nodes and the nodes have to agree(come to a consensus) on the state of the network, even in the presence of evil generals(malicious nodes).

All of this eventually led to the development of highly fault-tolerable systems in the real world.

**How it fits into the big picture**  
We've already touched on the cores in the consensus, but how this fits into bitcoin's blockchain architecture might still seem vague. To see the picture clearer, we have to take a look at what Bitcoin's Blockchain network has to do to achieve a stable network;

* Organize the network of individuals to agree on the generation of a new block
    
* Select a miner fairly from the network.
    
* Collect all the transactions from all over the network and write them into the blocks and make sure the majority of everyone on the network sees and agrees to it quickly enough.
    
* Give a good reason for anyone to be a part of the network or contribute computational power.
    
* Make sure participants who provide computational power to the network(miners) do not act irrationally or act maliciously.
    

The question goes on and on. Nakamoto's answer to these questions came in the form of 'Proof of Work'.

## PROOF OF WORK

The proof of work consensus algorithm solved major problems, which in turn solved other problems till a stable and usable system emerged. These problems include:

* Problem I:: Fair miner selection and Incentivizing miners
    
* Problem II:: Block creation, Transactions entry, Block propagation, Block validation
    
* Problem III:: Security and longest chain rule
    

How is a miner selected and how does that happen fairly was one question I always asked myself while learning how all this worked. On the bitcoin network, there are over 200,000 nodes(a rough estimate), that take part in the decision-making, validation and mining process. Not all of the nodes on the blockchain are mining nodes. They carry out different actions based on their nature. There are full nodes, light nodes and mining nodes.

![bitcoin nodes.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656006881441/g9lNMTSTb.png align="center")

No entity or authority selects a miner, doing this would betray the whole idea of decentralization. Instead, one miner is selected amongst thousands of others every ten minutes based on their speed in solving a cryptographic puzzle generated by Bitcoin's core protocol. The process of solving the puzzle is mining.

### **MINING**

What miners do when they mine, is to gather all valid transactions that could be fitted into a block from the memory pool(temporary storage for transactions on the network before they are recorded into a block). The miner creates a new block, orders the transactions into the block, writes a valid header for the block and then shows other miners the block, so they can verify its validity before appending it to the existing chain of blocks. For a deep dive into cryptocurrency mining, I wrote an article [here](https://ebode.hashnode.dev/what-does-it-mean-to-mine-cryptocurrencies).

A block header has different fields, but for mining, the most important field is the **Nonce** header field. The image below shows the different fields in Bitcoin's block header.

![bitcoin block header.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656001440185/Ea3oKAw7i.png align="center")

### **REWARD SYSTEM**

For any miner who successfully creates a new block, the first transaction written into the block is a Coinbase transaction. A Coinbase is the only transaction that creates Bitcoin. It creates Bitcoin out of thin air as a reward for the computational power provided by the miner and transfers it to the wallet address of that miner. The reward given to the miner was defined early in the development of Bitcoin's system by Satoshi Nakomoto. The reward to the miner gets halved over the years till it gets to zero. The reward started at fifty(50) Bitcoins per miner and it's currently at 6.25 Bitcoins.

The mining reward gets halved over time to control the rate at which new Bitcoins are created and released into the market. This halving happens after every 210,000 new blocks are created. It takes an average of about 10mins for a new block to be created and added to the Bitcoin network. Doing the maths,

```plaintext
10mins(block creation) * 210,000(blocks mined before reward halving) 
= 2100000mins(for every halving);

2100000mins / 1440mins = ~ 1458days;
(1day = 1440mins)

1458days / 365days = ~ 4years;
```

From above, we see why the bitcoin mining reward halving happens every 4years. right from the inception of bitcoin. The Bitcoin mining milestone is shown below:

* (2009) - 50 Bitcoins rewarded to miners.
    
* (2013) - 25 Bitcoins rewarded to miners.
    
* (2017) - 12.5 Bitcoins rewarded to miners.
    
* (2021) - 6.25 Bitcoins rewarded to miners.
    
* (2025) - Next halving to 3.125 Bitcoins would occur.
    
* (2140) - The supposed final halving would occur.
    

This reward helps miners offset their running expenses. Bitcoin mimics gold scarcity with the halving and mining process, it also keeps the value of existing bitcoins stable, as there can only ever be twenty-one million coins.

### LONGEST CHAIN RULE

**CHAIN SELECTION**  
While I was learning, a question popped into my head, wasn't it possible for two or more miners to find a valid block at the same time, what happens then? This question leads us to the next property of Nakamoto's consensus.

There is a possibility of multiple miners finding and propagating new blocks onto the network simultaneously, it only happens to be rare though. Let's paint a scenario of what happens and how it does in one such case.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674311947038/a58311b9-fe9e-4c17-aec9-ab0bb7922250.png align="center")

Let's assume two miners on different ends of the network find a valid hash and create a new block, this block is sent to the network for validation and storage. One thing to note is that miners are allowed to pick transactions randomly and fill them into their block, this means every miner's blocks contain different transactions and the Coinbase reward also is sent to different addresses(the different miners). This would mean that nodes on the chain now have different data and the chain is no longer unified. To resolve this, the **'longest chain rule'** is applied. The longest chain rule enforces prioritizing the chain with the highest number of blocks preceding. Blocks preceding a newly created block are tracked with the 'block-height' field in the block's header.

**How the longest chain rule is implemented**  
Earlier, I said every node on the blockchain gets out of sync when two miners find and contest for the same block creation, and its reward. How then is a miner decided as the final creator? The two miners are allowed to keep their block and reward, but a miner is chosen based on the next miner who finds the newest block. When a new miner finds a new block, the block on which they find this new block becomes the top priority block, because now it is longer, and the next miner after that adds their new block onto the longer chain and on till the length is decided to be finalized, without the possibility of ever reverting.

![Blockchain image attempting to solve the fork situation](https://cdn.hashnode.com/res/hashnode/image/upload/v1674312119953/3a2176ea-fc04-49fe-af63-406d65c6f40d.png align="center")

In the image above, the two miners we mentioned created blocks **Y** and **Y2** simultaneously, creating an imbalance. The two miners then had to wait for a new miner to decide who stays, the new miner created block **Z** and linked it to block **Y**, deciding that Block Y stays.

All the transactions in the unaccepted block put back into the memory pool by the miner that mined them and the nodes that took that miner's block, this is is called block re-organization. This situation is what leads to the concept of FINALITY( when it is sure that a transaction can no longer be returned to the memory pool). Exchanges have to be sure a transaction is final so that they do not pay customers, only for the transaction to send their asset to the exchange to get reversed later. If this happens, the exchange would be at a loss.

For bitcoin, the accepted block finality is after a 6-blocks depth. A block takes on average ten minutes to be mined, 6-blocks finality time would equal one hour.

The block with the longer chain continues to get linked to, while the rejected block becomes stale. The stale block is referred to as an ORPHAN BLOCK on bitcoin and the miner for that block doesn't get any reward. On Ethereum, it used to be called an UNCLE BLOCK, now it is called an OMMER BLOCK the miner gets a small reward for their efforts.

### **SECURITY**

All of these parts come together to create a balanced and secured blockchain network. Security features put in place on the blockchain network(using Bitcoin as a reference), include:

* Miners are randomly selected
    
* The network difficulty adjusts to the number of nodes on the network(increases or decreases to make sure block creation time stays in range).
    
* Miners are incentivized to do the right thing. Other nodes and miners validate a miner's generated block, if it doesn't meet the criteria, it is not recorded and discarded and they lose their reward.
    

For an entity to successfully control or hijack a blockchain's network, they would need to control more than half of the nodes on the network(51%), which would enable them to create the longest chain and only let in transactions they want. This is called a 51% attack, it is also limited in what it could do, as every transaction on the blockchain requires a signature from the account holder before it can become valid. This means the attacker can't steal bitcoin from other accounts.

As of 24th of April 2022, [blockchain.com](https://www.blockchain.com/explorer?view=btc) puts the hashing power on the Bitcoin network to over 216 quintillion hashes per second (216,000,000,000,000,000,000 h/s) \[ 216 Exahash per second\] power on the network, so for any one entity to get more than half of this, would cost way much that it would for any reasons they might want to, there sure would almost be no financial gain at that point. Also, as such actions would send people running off the network, the value and use of the network, would almost immediately become worthless.

![powerrrrr.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656041335621/iKx_sdgIw.png align="center")

This is a lot to take in, but if you can, it's fun and worth the time. I'll leave links to resources I found useful while learning and writing this article.

**RESOURCES**

#&gt;: [Byzantine Fault](https://en.wikipedia.org/wiki/Byzantine_fault)

#&gt;: [BITCOIN.ORG RESOURCE](https://bitcoin.org/en/resources)

#&gt;: [Byzantine Fault](https://en.wikipedia.org/wiki/Byzantine_fault)

#&gt;: [Golden's page on Nakamoto's Consensus](https://golden.com/wiki/Nakamoto_consensus-AMB5VWM)

#&gt;: [BITCOIN's WHITE PAPER](https://bitcoin.org/bitcoin.pdf)

%[https://youtu.be/CdyDoCk8IKs] 

Crypto Economic's channel on Nakamoto's Consensus
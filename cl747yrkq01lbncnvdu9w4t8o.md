---
title: "What does it mean to mine cryptocurrencies?"
datePublished: Mon Aug 22 2022 03:49:26 GMT+0000 (Coordinated Universal Time)
cuid: cl747yrkq01lbncnvdu9w4t8o
slug: what-does-it-mean-to-mine-cryptocurrencies
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1661056411010/cFBynQCpY.png
tags: blockchain, bitcoin, cryptocurrency, blockchain-technology, decentralization

---

> At the most basic level, cryptocurrency miners are playing a game of guesses.

At this point, talking about mining or a miner is almost always synonymous with cryptocurrency mining or miners. They are both across different fields, but in certain ways share some similarities. A cryptocurrency miner and an actual miner(someone who obtains mineral resources), both bring into existence or make usable something that wasn't. They both create value from labor, one being physical and the other computational.

For a cryptocurrency like Bitcoin, it is only created by mining(a computational process). People transfer Bitcoins, cryptocurrency exchanges sell you Bitcoins, and the government seizes bitcoins, but the only way it got into anyone's hands was after it was mined. Therefore, **what is mining?** Unlike physical mining, there are no diggers, tractors or persons wearing hard hats at a mining site. Instead, mining is a virtual process that happens within computers. The bigger and better the computer, the higher the chances of mining and finding Bitcoins.

**WHY MINING?**  
The first question anyone might ask would be why would I want to mine a cryptocurrency? There are two big answers to that, the first being that, you are incentivized to do so. This simply means you make some money(in the form of the cryptocurrency you are mining) for yourself, I think that's pretty obvious already. The second reason is that while you engage in the mining process, you increase the security of the network and increase its decentralization.

**HOW DOES MINING WORK?**  
In previous articles, I talked about a blockchain network operating on a peer-to-peer architecture, with armies of computers or servers(bigger and better computers) that all talk to each other over the network, and abide by the rules and protocols defined in the software they all run.

On a decentralized network (a network where no one/computer has special rights), an acceptable number of participants on the network needs to agree before any decision is made on the network. How an agreement is reached, was one of the problems Satoshi Nakomoto's Proof-of-Work used for bitcoin solved. Simply put, the proof-of-work fairly picks a participant on the network to rule the network for ten minutes every ten minutes. This ten-minute leader is accountable to both the software it is running on and every other participant on the network. The leader has to show everyone that what he did went according to the laid down rule and only when an acceptable number of participants agree, would they take his results and store them on the blockchain. The process of being selected to rule is mining.

**WHAT COMPLEX PROBLEM IS GETTING SOLVED?**  
Right at the start, I said mining is simply a guessing game, yeah it is, just complex. Miners try to get a large hexadecimal(base 16) number closest to a number chosen by the network and software. This number is a very very large number

The process of solving starts out like a race, every miner has to initially fill a block body with transactions, which are sourced from the transaction/memory pool and after that, fill up the block header with the right values, these include:

* Previous block hash
    
* Merkle root hash
    
* Timestamp
    
* Difficulty target
    
* Nonce(very important data for miners).
    

Once all of this is assembled, the call to begin a new race of who solves the new problem first begins immediately after a winner for a previous round is found.

**THE HEADERS**

![header.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1661114883408/DUfUXr_3j.png align="center")

---

![field-header.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1661129980357/zEo-UHExj.png align="center")

**HASHING**  
At this point when the block is completely set up(filled with ), the game of guessing and hashing begins. What does hashing mean? In an earlier [article](https://ebode.hashnode.dev/what-is-blockchain-technolgy) talking about web 3.0 technology, I touched on hashing. Simply put, to hash something means to select a word, text, picture, video, music or any digital file and convert it into a fixed length of very random and unpredictable data. The length and other properties of a hash are decided by the hashing algorithm. There are different hashing algorithms. Bitcoin uses the Sha-256 algorithm, while Ethereum uses Keccak-256.

Let's try with examples. If you hash the letter '*a'* with the sha256 hashing function, you get the resulting hash value:

```plaintext
sha256(a)
output >> ca978112ca1bbdcafac231b39a23dc4da786eff8147c4e72b9807785afee48bb
```

If you hash letters ( *ab* )using sha256 :

```plaintext
sha256(ab)
output >> fb8e20fc2e4c3f248c60c39bd652f3c1347298bb977b8b4d5903b85055620603
```

If you hash the word ( *I am a cryptocurrency miner* ) using sha256 :

```plaintext
sha256(I am a cryptocurrency miner)
output >> 3206361d094df9beadf6cec28e3efa6b8e36303206aae99c83148874ab8d2153
```

If you hash all the words in the dictionary combined using sha256, you would still get a 64-character length hexadecimal, likewise hashing a 300-hour youtube video or a bitcoin block header, the output would always be 64 characters. These characters are also very random and almost unpredictable.

Hashing should not be mistaken for encryption, in encryption, what is encrypted can be recovered by reversing the encryption process(decryption). Once data is hashed, it can't be recovered, it can only be compared with other hashes. Therefore a hash has to be deterministic(given the same input, a hash function will always return the same output), it also means the hash value for 'ab' should remain the same forever. Another hash function property is that a little change to its input should cause a big and unpredictable change in the output(Avalanche effect).

**HOW HASHING IS USED IN MINING**  
Earlier, I mentioned the **nonce in** Bitcoin's block header. A nonce is a number that is used only once in the mining process of Bitcoin. It is a field in the block header of a transaction. Miners repeatedly change the nonce value in the block header, along with other fields such as the timestamp, in an attempt to find a hash lower than the target hash set by Bitcoin's network.

The target hash is adjusted from time to time based on the overall mining power of the network. The mining power is the sum of the number of computers on the network at a particular time mining. It is designed to be a very difficult value to find and it changes over time, making the mining process more challenging as more miners join the network.

The network adjusts the target hash such that a new block is added to the blockchain approximately every 10 minutes. This is called **difficulty retargeting**. The network calculates how long it took for 2016 blocks(about two weeks) to get mined, it compares that time with a time set by the network, if the time to mine 2016 blocks was lesser than the network-defined time, it meant the difficulty had reduced and it would get increased and if it was higher, it meant the difficulty was higher and it would get decreased.

```plaintext
Target Hash : 00000000000000000007bafbad22baee03420dccc0a853ac60673398e66ec8ca
```

The more zeroes at the start, the greater the difficulty, it increases exponentially with each zero. If you remember from earlier, any little change to a hash input changes the hash output unexpectedly, it is random and not guessable. To solve the problem, the miner takes the block header of the block it created and hashes it. The goal here is to find a number lesser than the target hash. To keep getting different hash values, the miner keeps changing the value in the nonce field in the block header and for each new value, it compares it with the target hash to see if it is lesser.

An example of a hash with a lesser than the target hash would begin with something like this *00000000000000000005\. If you observe, you would notice that 5 is less than 7, this is an indicator it is lesser. These are very large numbers and this is one example I could come up with that could easily show which is lesser or greater.*

```plaintext
Target Hash:⬇️
0000000000000000000(7)bafbad22baee03420dccc0a853ac60673398e66ec8ca

0000000000000000000(5)a1f9e8d7c6b5a4f3e2d1c2b3a4f5e6d7c8b9a0f1e2d3
⬆️:Value lesser than Target Hash
```

If a miner finds the lesser-than-target hash while hashing his nonce, the rest of the block header and the block body, he automatically wins that round. Now you see how it is more of a game of guessing. Just that the numbers involved are very very very large numbers which make the game something only computers can play. Also, the process of hashing and comparing is intensive. The more data a computer can hash per second the stronger it is. Mining machines are ranked by that.

```plaintext
Target Hash(base 16 | Hexadecimal):
00000000000000000007bafbad22baee03420dccc0a853ac60673398e66ec8ca
Target Hash(base 10 | Decimal):
740,425,486,432,857,267,178,346,074,642,572,195,919,787,393,044,971,520

Mining:
a game of incredibly large number
```

![validity.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1661133986331/pVTXo1jLM.png align="center")

> > check the block explorer [here](https://www.blockchain.com/btc/block/000000000000000000021fffa7d23a20229abf52b6e8c0262e63a504e0e8fd35)

The image above is a valid block from Bitcoin's blockchain, you can check it with the link above. The hash circled in orange, was the hash lower than the target difficulty, the miner had to find to win the mining process. The Nonce circled in blue was the magic value his machines had to guess, which he hashed the block header and body to get the winning hash. That is the magic there is to it.

There are situations where miners exhaust all the valid nonce values and still don't find a hash lower than the target hash. In situations like this, a field for ExtraNonce is introduced and used.

**MINERS REWARD**  
The process we just talked about is energy intensive and the energy here refers to electricity, which also costs money. Regular computer CPUs can't mine Bitcoin anymore, due to the competition on the network, although it was initially possible. Specialized hardware are used for mining these days.

* GPU (⤵️)
    
    ![geforce.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1661135333753/iQykLql6t.jpg align="center")
    
* GPU FARM (⤵️)
    

![gpu-farm.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1661136044171/Ia8Qk-Q8Z.jpg align="center")

**GPU(Graphics Process Units)** were made specifically to handle graphics processing in intensive graphics use environments like Animation rendering, 3D Modeling, Gaming, etcetera. Due to having more strength than CPUs, and also being compatible with mining certain cryptocurrencies, they found a spot in the cryptocurrency mining field. It is especially used in Ethereum Mining.

* FPGA(⤵️)
    
    ![FPGA.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1661135604092/DboZ8KyYt.jpg align="center")
    

A **Field Programmable Gate Array (FPGA)** is an electrical circuit that is programmed to carry out one particular logical process. This makes it possible to program an FPGA miner to mine specific cryptocurrencies. However, if necessary, it could be reconfigured to mine a different cryptocurrency. FPGA programming and configuration, however, call for specialized skills.

* ASIC (⤵️)
    
    ![asic.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1661135815847/535Fyph7W.jpg align="center")
    
* ASIC FARM
    

![asic-farm.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1661135973201/mMffYmnNS.jpg align="center")

**Application-Specific Integrated** **Circuit** (ASIC) are electronic chips that are designed specifically to carry out a given function. One such possible function is to mine a cryptocurrency. ASICs are well used for Bitcoin mining. ASICs are not as flexible as FPGAs.

Buying and using such equipment is expensive. Therefore, miners make sure that their mining covers the expenses involved in setting up and running the whole process.

In most cryptocurrency mining, there is a mining reward for a miner who successfully adds a block to the blockchain. On the Bitcoin network, the mining reward started at 50 bitcoins(2009), but halves every 4 years. It is currently at 6.25 Bitcoins. Other cryptocurrencies follow a similar approach.

**SOLO MINING Vs POOL MINING Vs MINING FARMERS**  
A **solo miner** is an individual that sets up his machine(computer or GPU or ASIC or FPGA), to validate, record transactions and propagate transactions on a cryptocurrency's blockchain network. They compete with other miners to solve the cryptographic puzzle.

**Pool mining** is more like a community activity, where miners put together all of their machine's power and mine as one entity. This gives them an edge over other miners, especially solo miners. There are two types of mining pools:

* Mining pools that pay miners according to the power they provide to the pool's network.
    
* Mining pools that pay miners only when a block mined by that particular miner is found.
    

The first option is the most popular, as it means, users don't have to be lucky, they get rewards every day. Popular Mining Pools are [FoundryUSA](https://foundrydigital.com/), [AntPool](https://www.antpool.com/home), [F2Pool](https://www.f2pool.com/), etcetera.

A **Mining Farm** has more is structured corporately. There are shareholders, managers and staff(technicians, electrical engineers, software engineers and lots more). The stakes here are high, and so are the rewards. Farms like this could have thousands and thousands of ASICs mining (24/7)/365. The video below would show what it feels and looks like on a mining farm.

%[https://youtu.be/f0HC1Udk6-E] 

A great deal of energy is used in the mining process where **millions** of miners compete and exhaust electricity only for about **144** miners to be selected each day, there has been a lot of upset amongst people and the government. They want cryptocurrency consensus algorithms to switch to less electricity-demanding mining algorithms.

Bitcoin never really asked for permission before breaking into space and getting accepted, I doubt it would bend now.

This was a long post. I hope you picked up something.
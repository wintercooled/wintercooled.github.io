---
layout: page
title: How it works
permalink: /how-it-works
---

# How Elements works and the roles of network participants.

## Elements provides a technical solution to problems blockchain users face daily: transaction latency, commercial privacy, fungibility, and reliability.

Elements overcomes these problems through its use of Strong Federations and the optional ability to run Elements as a sidechain.

The process of block signing within an Elements based blockchain is not reliant on Proof of Work (PoW) but instead a Strong Federation of signatories called Block Signers. The use of these signatories removes the inherent latency in the PoW mining process, whilst not introducing the need for third party trust.
 
Functionaries within a Strong Federation (called Watchmen) enable the secure and controlled transfer of assets between a main chain and an Elements based sidechain.

* * * 
 
### Strong Federations

Blockchains built on Elements benefit from quicker block times compared to blockchains that use a Proof of Work (PoW) system to verify the movement of assets between participants and arrive at consensus.
 
Elements uses an approach to consensus made available by Blockstream called Strong Federations. A Strong Federation removes the need for costly Proof of Work mechanisms and replaces it with the collective actions of a group of mutually distrusting participants, called functionaries.
 
The role of a functionary is to sign off on actions within the blockchain. These actions are then verified against protocol rules and approved by other functionaries only if they are deemed valid. Once a threshold of signatories have signed off on an action, consensus is seen to have been reached and the action is given finality within the network.
 
The network operators of a Strong Federation consist of functionaries which either have the ability to control the transfer of assets between blockchains (in the case of a sidechain implementation) or to enforce the consensus rules of a stand alone blockchain. These actions are split between two distinct roles in order to enhance security and limit the damage an attacker can cause.
 
The two roles a functionary can fulfill within a Strong Federation are...
 
* **Watchmen** - responsible for moving assets in to and out of a sidechain by signing transactions on the main chain.
 
* **Block Signers** - create blocks of transactions by signing, defining its consensus history.

Combined, these roles allow Elements to deliver both rapid block creation (faster and final transaction confirmation) and assured assets (pegged assets directly linkable to another blockchain).
 
We will look at how Block Signers create blocks in a later section and will begin by discussing how Watchmen enable the use of something called a Federated Peg to allow the 1 to 1 transfer of assets between an Elements based sidechain and another blockchain.

* * * 

### The role of Watchmen in a Strong Federation

In order for a sidechain to operate in a trustworthy manner it must allow participants to verify that the supply of assets is controlled, verifiable and guaranteed. An Elements sidechain uses something called a ‘Federated Peg’ to enable the two way transfer of assets in and out of the Elements network’s blockchain. This satisfies the requirements of provable issuance and inter-chain transfers, as we shall now see.
 
At a high level, these transfers work by freezing the assets in a transaction on the main chain, making them unusable there, and then creating a transaction on the sidechain that describes the locked asset. This process effectively moves assets from the parent chain to a sidechain. To move assets back to the main chain a similar process occurs — a transaction is created in the sidechain describing an output of the asset on the main blockchain and destroying them on the sidechain.
 
This process of creating and destroying assets on the sidechain is secured by a consensus mechanism within the sidechain and is performed by functionaries named ‘Watchmen‘ who move assets into and out of the sidechain by signing transactions on both chains. Most importantly, the members of the federation cannot directly control any users’ assets inside the system other than their own.
 
In order to transfer bitcoin between chains a multi-signature mechanism is used, whereby a certain number of participants in the federation of mutually distrusting participants must sign before the transaction is considered valid and the assets transferred between chains.
 
The Watchmen observe both the main blockchain and the Elements sidechain in order to validate asset transfers between them. A set of geographically and jurisdictionally distributed servers are preferred, creating a compromise-resistant network of functionaries.
 
This network retains a number of the beneficial properties of a fully decentralized security model without introducing the need for a trusted 3rd party or single point of failure.
 
!!! insert image here !!!

#### Diagram showing how Watchmen transfer assets into and out of an Elements sidechain

* * * 
 
### The role of Block Signers in a Strong Federation

We have already mentioned how a federation of Watchmen control the transfer of assets between blockchains and we will now look at how Block Signers perform their role within the Strong Federation and secure an Elements blockchain.
 
A blockchain like Bitcoin’s is extended when anyone forming part of a dynamic group of block signers extends the chain by demonstrating proof of work expended. The dynamic nature of the set introduces the latency issues inherent to such systems.
 
By using a fixed signer set a federated model offers another solution, in which the dynamic set is replaced with a traditional multi-signature scheme. Reducing the number of participants needed to extend the blockchain increases the speed and scalability of the system, while validation by all parties ensures integrity of the transactions.
 
The diagram below shows how consensus is achieved in a Strong Federation. It is referred to as federated block signing and consists of several phases:
 
**Step 1** - Block Signers propose candidate blocks in a round-robin fashion to all other signing participants.
 
**Step 2** - Each Block Signer signals their intent by pre committing to sign the given candidate block.
 
**Step 3** - If threshold X is met, each Block Signer signs the block.
 
**Step 4** - If threshold Y (which may be different from X) is met, the block is accepted and sent to the network, the Strong Federation reaches a consensus that the transaction occurred.
 
**Step 5** - The next block is then proposed by the next Block Signer in the round-robin.

Because a Strong Federation’s block generation is not probabilistic and is based on a fixed set of signers, it can be made to never reorganize. This allows for a significant reduction in the wait time associated with confirming transactions. It also removes the incentive to mine for profit (i.e. the block rewards) and replaces it with an incentive to productively participate in a network where all participants have a shared goal of ensuring the network continues to function in a manner that is beneficial to all, without introducing a single point of failure or higher trust requirements.
 
!!! insert image here !!!

#### Diagram showing how federated block signing achieves consensus within a Strong Federation:

* * * 
 
### Asset Issuance and transfers

Initial asset issuance and the re-issuance of additional amounts of those assets are controlled by the use of issuance tokens. These tokens act as a verifiable right to issue an asset and are exchangeable and verifiable amongst participants in the network. 
 
Elements allows new applications such as token issuance, digitizable collectables, reward points, and attested assets (for example gold coins) to be transacted on a blockchain. With Elements, you can issue and transact as many different asset types as you like. 
 
Every asset type optionally benefits from features such as Confidential Transactions, which provides privacy around the amount and type of asset being transferred. This allows different assets to be given different privacy properties depending on the requirements of the network.
 
The Federated 2-way Peg feature allows such assets to be interoperable with other blockchains and representative of another blockchain’s native assets. By pegging your blockchain to another you can extend the capabilities of the main chain and overcome some of its inherent problems by making small trade offs in your security model.

#### Whether your Elements project is set up to operate as a stand-alone blockchain or as a sidechain to another blockchain, Strong Federation technology provides a significant advantage over more cost and time intensive consensus processes whilst retaining the properties of a trustless system.



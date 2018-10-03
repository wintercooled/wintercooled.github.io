---
layout: page
title: Blockchain or Sidechain?
permalink: /blockchain-or-sidechain
---
# The correct approach to deploying a solution built on Elements.

## Elements can operate as a general purpose blockchain or as a sidechain.

A general purpose blockchain built on Elements acts as a stand alone blockchain with no dependencies on another chain for its asset issuance.
In the context of the Elements platform, a Sidechain is an extension to an existing blockchain. Assets are transferable between chains allowing the main chain to benefit from the enhanced features of the sidechain such as rapid transfer finality and confidential transactions. Whilst a sidechain is aware of the main chain and its transaction history, the main chain has no awareness of the sidechain, and none is required for its operation. This enables sidechains to innovate without restriction or the delays associated with main chain protocol improvement proposals. Rather than trying to alter it directly, extending the main protocol allows the main chain itself to remain secure and specialized, underpinning the smooth operation of the sidechain.
 
An example of an Elements based sidechain in production use is Liquid.
 
Liquid is an implementation of a federated sidechain - a private blockchain with different features, capabilities, and benefits than the main Bitcoin blockchain.
 
By extending the functionality of Bitcoin and leveraging its underlying security, the Liquid network is able to provide new functionality that was previously not available to Bitcoin users.
 
Liquid was designed to address the needs of exchanges, brokers and institutions. It enables the rapid, confidential and secure transfer of funds between participants and provides a solution to the inherent problem of delayed transaction finality on the Bitcoin network.
 
Every Liquid bitcoin held within the sidechain is pegged to bitcoin on the main chain using Element’s Federated 2-way Peg. This allows bitcoin to be deposited in the sidechain whilst retaining the ability to withdraw assets back to the main Bitcoin blockchain.
 
Elements provides the tools needed to prototype and deploy your own blockchains and sidechains in a cost effective and timely manner.

* * * 

### When to use a blockchain

A blockchain is an inherently inefficient means of data storage when compared to centralised database solutions. This inefficiency is a price worth paying if you require the properties that a blockchain offers. It is important to correctly evaluate the requirements of your proposed system before deciding on a blockchain based solution.

**If your requirements do not necessitate it, implementing a blockchain based system will be counterproductive.**
 
When should you use a blockchain as a solution?

* No central or single party should have sole authority to write data entries.

* A group of participants need to be able to access and audit data and be sure that it is cryptographically protected against tampering.

* Speed of transaction sending is not a key requirement. The Elements federated block signing process is still much faster than Dynamic-Membership Multi-party Signature (DMMS) Proof of Work (PoW).

* Immutability (inability to adjust confirmed transactions) is required.

* Security and redundancy with no single point of failure is required.

* Participants have the same incentives to participate.

* * *

### Checklist

If you can answer 'Yes' to each of the following then your project is a good candidate for a private, federated Elements-based blockchain:

* Do you need to record transactions of financial value in the system?

* Is it unacceptable to use a trusted third party to perform this action?

* Is there a need for multiple entities to register transactions?

* Are all such entities known?

* Do participants require that they should not have to trust any other participant to validate the accuracy of the written data?

* Should transactions be privately and not publicly verifiable?
<br />
<br />

#### Deciding if a blockchain is an appropriate way to deliver your project is the most important of these steps and it is worth highlighting up front that blockchains provide solutions to very specific types of problem.


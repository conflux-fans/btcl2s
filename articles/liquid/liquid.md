# **Exploring Liquid Network’s Bitcoin Sidechain**

## **Introduction**

This article is part of a series exploring the different scaling solutions built on or around Bitcoin's blockchain. The aim is to provide a comprehensive insight into these protocols, highlighting their functionalities, security features, and their role in the broader cryptocurrency ecosystem. In this edition, we will explore the Liquid Network, examining its design, operation, and its implications for Bitcoin's scalability and privacy enhancements.

## **Overview**

Liquid Network is a sidechain-based settlement network that functions as a Bitcoin Layer-2 solution. It interconnects global cryptocurrency exchanges and institutions, facilitating rapid and confidential Bitcoin transactions along with the issuance of digital assets.

Liquid aims to address some of the limitations of the Bitcoin network by providing faster transaction settlements and enhanced privacy, all while maintaining robust security. It enables the issuance of various types of digital assets which opens new avenues for trading and asset management on its platform.

The network was officially launched in 2018 by Blockstream, and it operates as an implementation of Elements, a sidechain-capable blockchain platform. 

![l1](./img/l1.png)

## **Protocol Quick Scan**

The Liquid Network was specifically designed as a sidechain to Bitcoin that aims to address the scalability and privacy limitations of its parent chain. This section provides a concise overview of how the Liquid Network operates, its unique features, and the technical innovations it introduces to enhance transaction capabilities on Bitcoin.

### **Operational Mechanics**

At its core, the Liquid Network facilitates faster and more private transactions through a sidechain mechanism linked directly to the Bitcoin blockchain. Users can transfer Bitcoin into the Liquid Network using a two-way peg, which converts BTC to Liquid Bitcoin (L-BTC) at a 1:1 ratio. This conversion enables the use of L-BTC across Liquid’s ecosystem with all transactions benefiting from the sidechain’s enhanced features like rapid settlement times and increased privacy.

### **Key Differentiators**

**Federated Consensus**: Unlike Bitcoin’s decentralized proof-of-work system, Liquid utilizes a federated consensus model managed by a consortium of trusted functionaries. These functionaries are responsible for maintaining the network’s integrity and security. This model allows for consistent block times and immediate transaction finality, reducing the typical wait times associated with Bitcoin’s block confirmations.

**Confidential Transactions**: Liquid introduces privacy as a core component of its architecture. Through Confidential Transactions, transaction amounts and asset types are obscured, providing privacy for financial transactions while still maintaining the ability to audit and verify transfers securely. This feature is particularly appealing to institutions and individuals seeking privacy without sacrificing transparency.

### **Technical Innovations**

**Liquid’s Two-Way Peg**: The pegging mechanism used by Liquid allows for secure and verifiable movement of Bitcoin between the Bitcoin blockchain and the Liquid sidechain. This peg is crucial for maintaining a trustless exchange environment where users can move assets across blockchains without reliance on intermediary transfer services.

**Speed and Finality**: The network’s design emphasizes speed and reliability. Transactions on Liquid can achieve final settlement within two minutes, a significant improvement over Bitcoin. This is made possible through the streamlined block generation process managed by the functionaries, ensuring that transactions are processed swiftly and without the delays associated with mining on Bitcoin.

**Asset Issuance Platform**: Beyond transacting in Bitcoin, Liquid provides functionalities for issuing a variety of digital assets. These assets can represent real-world entities like fiat currencies or securities, or they can be entirely digital creations such as tokens for specific ecosystems. The issuance process is integrated with Liquid’s privacy features, allowing issuers to maintain confidentiality over the operations while enabling the broad utility of these assets across the network.

## **Trust & Security**

Liquid Network, while offering enhanced functionality and performance over the Bitcoin blockchain, necessitates a degree of trust in various components and entities. This trust is balanced by a comprehensive suite of security measures designed to safeguard the network and its participants.

### **Trust Components**

**1. Federated Consensus Model**: Unlike decentralized blockchains like Bitcoin, Liquid operates under a federated consensus model, requiring users to place trust in the federation of functionaries. These functionaries, selected from among reputable financial and technological institutions, are responsible for validating transactions and creating blocks.

**2. Functionaries as Block Signers and Watchmen**:

- **Block Signers**: Users must trust that these functionaries will act honestly and efficiently in proposing and signing blocks within the agreed-upon one-minute intervals.
- **Watchmen**: Responsible for managing the two-way peg that allows the transfer of BTC to and from Liquid. Users must trust them to securely handle these conversions and to safeguard the locked BTC.

**3. Multi-Sig Wallets and Timelocks**: Liquid’s security model requires trust in the implementation and management of multisig wallets and timelocks that control the release of funds. These mechanisms need to operate correctly to prevent unauthorized access and ensure the proper execution of emergency recovery procedures.

**4. Key Storage Modules** The integrity of the Key Storage Modules crucial as they store critical cryptographic keys used by functionaries to sign transactions. Trust is placed in the physical and operational security of these devices.

**5. Emergency Recovery Procedure**: In the event of a significant portion of the network going offline, users must trust in the predefined emergency procedures designed to recover the network and secure the funds.

### **Key Security Features**

**1. Confidential Transactions**:

- Liquid uses Confidential Transactions to enhance privacy by obscuring transaction amounts and asset types from public view, while still allowing for network validation.

**2. Strong Federation**:

- A tightly controlled group of functionaries, known as a Strong Federation, mitigates the risks of double-spending and ensures rapid transaction processing and finality.

**3. Multisig Wallets with Timelocks**:

- Multisig wallets add an extra layer of security, requiring multiple functionaries to agree on transaction validity. Timelocks ensure that even if a significant number of functionaries were compromised, the network could still recover.

**4. Federated Block Signing**:

- Blocks are signed by functionaries using a round-robin mechanism, which provides resistance against fraud or collusion among a minority of participants.

**5. Key Storage Modules**:

- All cryptographic operations are processed using Key Storage Modules, ensuring that private keys do not leave the device and are not exposed to potential online threats.

**6. Network Resilience and Failover Protocols**:

- The network is designed to be resilient, with protocols in place to handle the failure of one or more functionaries without halting network operations. This includes the ability to continue operations as long as two-thirds of the functionaries are operational.

**7. Emergency Recovery Keys**:

- In case the network stalls due to a major disruption, a set of emergency keys activated by a timelock can recover the network, ensuring that the funds remain accessible.

While the Liquid Network introduces several points of trust not present in fully decentralized blockchains, these are counterbalanced by robust, multi-layered security measures. These features are designed to protect user assets, maintain privacy, and ensure the integrity and continuity of the network under a variety of scenarios. 

## **Additional Information**

### **Virtual Machine**

Liquid does not employ a traditional virtual machine but uses a scriptable platform similar to Bitcoin for asset issuance and transfer, focusing on performance and security.

### **Scalability**

Liquid can process transactions faster than the Bitcoin network, with block times set at one minute and transaction finality achieved within two minutes under normal conditions.

### **Total Value Locked**

The Total Value Locked (TVL) in Liquid Network indicates how much Bitcoin was deposited. The actual TVL is of approximately [3855 BTC](https://l2.watch/bitcoin/) ($255M) showing the amount of assets engaged in the Liquid Network.

## **Pros and Cons**

### **Pros**

- **Speed**: Transactions are finalized within two minutes, significantly faster than Bitcoin.
- **Privacy**: Confidential Transactions ensure transaction amounts and asset types are hidden, enhancing user privacy.
- **Interoperability**: Supports multiple asset types and enables seamless transfers within its ecosystem.

### **Cons**

- **Centralization Risks**: The reliance on a federation for consensus might introduce risks of central control and potential failure points.
- **Complexity**: The dual-token system and the concept of functionaries can be complex for new users.
- **Limited Throughput**: Despite its improvements over Bitcoin, Liquid's transaction throughput may not match that of major centralized payment processors.

## **Protocol Details of Liquid Network**

This section delves deeper into the architectural nuances and technical mechanisms that underpin Liquid's functionality, illustrating how it differentiates itself from both Bitcoin and other blockchain solutions.

### **Integration with Bitcoin**

Liquid operates as a sidechain to Bitcoin, which means it functions in parallel while utilizing Bitcoin as the parent chain for locking and unlocking Bitcoin (BTC) through a two-way peg system. This system allows users to transfer BTC to the Liquid network, where it is transformed into Liquid Bitcoin (L-BTC) at a 1:1 ratio, and vice versa.

**Peg-in and Peg-out Mechanisms**:

- **Peg-in**: Users send BTC to a multisig address controlled by the Liquid functionaries. After 102 confirmations on the Bitcoin network, the corresponding amount of L-BTC is issued to the user on the Liquid sidechain.

![l2](./img/l2.png)

- **Peg-out**: The reverse process involves converting L-BTC back to BTC. This requires a quorum of functionaries to sign off on the transaction, providing an additional layer of security before the BTC is released back to the user on the Bitcoin blockchain.

![l3](./img/l3.png)

### **Federated Consensus Model**

Liquid departs from Bitcoin's Proof of Work (PoW) consensus mechanism, adopting a federated model known as a Strong Federation. This model is central to Liquid’s operations, involving a group of functionaries—vetted and authorized entities such as exchanges and financial institutions—that are geographically distributed. These functionaries perform two critical roles:

1. **Block Signers**: Functionaries participate in block creation, proposing and signing blocks every minute. This regular interval contrasts with Bitcoin’s variable block time and helps achieve faster settlement times on Liquid.
2. **Watchmen**: This role involves overseeing the pegged BTC, managing peg-in and peg-out processes, and ensuring that the two-way peg remains secure and verifiable.

The federated model ensures that no single entity controls the network while providing the necessary speed and security for institutional-grade transactions.

### **Confidential Transactions and Asset Issuance**

One of the hallmark features of Liquid is its support for Confidential Transactions (CT). These transactions allow amounts and asset types to be encrypted, visible only to the transacting parties and optionally to others they choose to disclose. This is achieved through the use of cryptographic techniques known as blinding factors, which obscure transaction details from other network participants, including functionaries.

**Issued Assets**: Beyond L-BTC, Liquid supports the issuance of various digital assets, such as tokenized fiat, securities, and other cryptocurrencies. These assets utilize the same privacy features as L-BTC, providing a secure and private means of asset transfer and management across the network. Issued assets are given unique identifiers and can be issued, transferred, and destroyed within the Liquid network, providing a flexible platform for digital asset innovation.

### **Security Mechanisms**

**Multisig Wallets with Timelocks**: All BTC stored within the Liquid network is secured in multisig wallets controlled by the functionaries. To enhance security, these wallets are equipped with timelocks to ensure that, even if a significant portion of the functionaries were compromised or offline, the funds could still be retrieved after a predefined period.

**Key Storage Modules**: Functionaries use Key Storage Modules to manage and protect the private keys necessary for signing block transactions and managing the peg. These devices ensure that keys are never exposed to the internet and are immune to remote attacks.

### **Network Resilience and Recovery**

**Emergency Recovery Procedure**: In the event of a catastrophic network failure where one-third or more of the functionaries are offline, Liquid incorporates an emergency recovery procedure using a set of backup keys held by a trusted third party. This measure ensures that funds can be recovered and the network can be restored even in extreme scenarios.

**Dynamic Federation Management**: The federation can be dynamically adjusted, with new functionaries being added or removed as needed to adapt to changing security requirements or to expand the network’s capabilities.

## **References**

- [Liquid Network](https://docs.liquid.net/)
- [Blockstream](https://blockstream.com/liquid/)
- [Elements Project](https://elementsproject.org/en/doc/)
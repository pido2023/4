# Asymmetric Encryption & Meta-Asset

## **Asymmetric Encryption**

In the digital titling process of real-world assets (RWAs), asymmetric encryption technology plays a crucial role. This technology allows for the digital mapping of physical assets through blockchain technology, while utilizing asymmetric encryption algorithms to ensure the security, immutability, and traceability of ownership.

### Security

Asymmetric encryption achieves security through unique public-private key pairs, allowing only the private key holder to operate their assets. This mechanism greatly enhances the security of asset transfer and management operations, essentially constructing a cryptographic barrier that prevents unauthorized access and manipulation.

### Immutability and Transparency

Once an asset is recorded and titled on the blockchain, its information is maintained on a distributed ledger across multiple nodes. The ledger's consensus mechanism ensures that any unverified tampering attempts will be detected and rejected by other parts of the network, thus guaranteeing the immutability of the data. At the same time, the audibility and high transparency of the blockchain ensure that asset titling records are publicly accessible, enhancing the trust in transactions and reducing the potential for fraudulent activity.

### Programmability

The introduction of smart contracts provides the potential for the automation of asset transactions and management. This not only increases the flexibility of transactions but also significantly improves processing efficiency. The programmability of smart contracts means that complex logic and transaction conditions can be encoded into contracts and executed automatically, reducing intermediaries and lowering the risk of errors and abuse.

## Meta-Asset Binding and Verification Analysis

Pido employs external NFC certificate technology to link tangible assets with on-chain NFTs, ensuring consistency between off-chain assets and blockchain records. During implementation, the following issues may arise:

### **Forgery Issues Post-Asset Binding**

* If a forged physical asset is indistinguishable in material and craftsmanship from the original, the genuine asset could lose its trading value and be mistaken for a counterfeit; conversely, forgeries that closely resemble the original could enter the market as genuine.&#x20;
* For counterfeits with obvious material and craftsmanship discrepancies, community reporting and voting can be used for adjudication, with blockchain records available to reverse transactions if necessary.&#x20;

### Asset Transaction Process

* When a meta-asset is traded, it and its associated NFT are transferred to a new owner, with the transaction recorded on the blockchain.&#x20;
* Pido's asset binding effectively prevents high-quality forgeries, as counterfeits lack the authenticated value of genuine items on the blockchain, making the cost of forgery unlikely to yield returns and thus reducing the incentive to create fakes.&#x20;
* Nevertheless, Pido cannot guarantee the complete elimination of low-quality forgeries, although such counterfeits are usually identifiable through basic detection methods. Therefore, the platform will still provide users with necessary verification tools to protect their rights.

### NFC Certificate

* Offline transaction verification: NFC certificates enable users to verify the authenticity of physical assets without directly interacting with the blockchain, providing a convenient means of authenticity verification for physical transactions.
* Enhanced cryptographic security: NFC certificates provide a non-replicable identity tag at the physical level for assets, which is associated with an on-chain NFT, further increasing the difficulty of assets being forged or tampered with.

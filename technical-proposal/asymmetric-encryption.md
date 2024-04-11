# Asymmetric Encryption

Pido employs asymmetric encryption technology to link physical design/artworks with their digital NFT counterparts, enhancing the security and credibility of the design/artworks' digital identity. Here's an overview of how Pido authenticates physical design/artworks and maps them to digital NFTs using asymmetric encryption technology:

1. **Generating Digital Certificates**: For each design/artwork, Pido platform generates a unique digital certificate that contains detailed information about the design/artwork, such as the designer/artist, title, year of creation, and provenance. This certificate serves as the digital representation of the design/artwork's identity.
2. **Creating Public and Private Key Pairs**: The platform generates an asymmetric pair of public and private keys for each design/artwork. The private key is kept secure by the design/artwork's owner and is not disclosed, while the public key is stored on the blockchain alongside the design/artwork's digital certificate for public verification.
3. **Authentication and NFT Issuance**: The ownership information of the design/artwork is encrypted with the private key to create an encrypted record of authentication, and a corresponding NFT is issued. This NFT contains the design/artwork's digital certificate and authentication data, ensuring that only the legitimate owner can manage and transfer the NFT.
4. **Ownership Verification and Transfer**: When the ownership of a design/artwork needs to be verified or transferred, the owner uses their private key to sign and authorize the transaction. Others can use the publicly available public key to verify the authenticity of the signature, thus confirming the operator's ownership. This process ensures the security and transparency of the transaction.
5. **Immutability and Traceability**: Changes in ownership and transaction records are updated on the blockchain and verified by multiple nodes within the network. Thus, even if the platform itself is compromised, the records of the design/artwork cannot be altered, ensuring the immutability and traceability of the historical record.
6. **Application of Smart Contracts**: Pido will also use smart contracts to handle the transaction logic for design/artwork NFTs, such as terms of trade, royalty payments, etc. The execution of smart contracts is automated, ensuring that transaction conditions are strictly adhered to and transparently recorded on the blockchain.

By implementing such mechanisms, Pido ensures that the digitization and authentication process of physical design/artworks is both secure and efficient, bringing new opportunities and challenges to the design/art market with blockchain technology.

Check the details of encryption steps in:

{% content-ref url="../artworks-and-nfts/pido-nft/nft-copyright/" %}
[nft-copyright](../artworks-and-nfts/pido-nft/nft-copyright/)
{% endcontent-ref %}

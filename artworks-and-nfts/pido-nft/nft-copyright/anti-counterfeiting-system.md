# Anti-counterfeiting System

Pido introduces an anti-counterfeiting system for physical goods, which utilizes NFTs and NFC chips, in conjunction with a public and private key mechanism to verify the authenticity of physical commodities.&#x20;

## Primary Market Issuance

### **Designers/Artists**

* **Key Generation:** The system generates a pair of keys $$(V_0, W_0)$$ for each NFT, where $$V_0$$ is the public key, and $$W_0$$ is the private key.&#x20;
* **Private Key Distribution:** After the NFT is sold, the system sends the private key $$W_0$$ to the buyer.
* **Encryption and Storage:** The designer/artist uses the public key $$V_0$$ to encrypt the unique identifier (Hash ID) of the NFT, and stores this encrypted information on the NFC chip embedded in the physical designer item.

### **Consumers**

* **Private Key Receipt and Custody:** The consumer receives the private key $$W_0$$ and is responsible for its confidentiality and safekeeping.
* **Decryption and Verification:** The consumer uses the private key $$W_0$$ to decrypt the ciphertext on the NFC chip to verify the Hash ID.
* **Verification Result:** If the decrypted Hash ID is valid, the consumer can confirm that the item is genuine.

## Secondary Market Transactions

### **Sellers**

* **New Key Pair Generation:** Before listing the item on the secondary market platform, the system generates a new pair of keys $$(V_1, W_1)$$ and sends the private key $$W_1$$ to the seller.
* **Digital Signature:** The seller uses the private key $$W_1$$ to encrypt their blockchain address, creating a digital signature, and updates the NFT information and NFC chip with this signature.
* **NFC Data Update:** The seller must also re-encrypt the NFT's Hash ID with the primary market's public key $$V_0$$ and update the NFC chip.
* **Private Key Transfer:** Once the secondary transaction is completed, the seller must privately transfer the primary market's private key $$W_0$$ to the buyer.

### **Buyers**

* **Private Key Receipt and Custody:** The buyer receives $$W_0$$ and keeps it confidential while also checking the public key $$V_1$$ on the platform.
* **Decryption and Verification:** The buyer uses $$W_0$$ to decrypt the Hash ID on the NFC chip and $$V_1$$ to decrypt the digital signature to confirm the seller's blockchain address.
* **Address Verification:** The buyer needs to verify that the seller's address decrypted from the digital signature matches the current holder's address of the NFT.
* **Transaction Verification:** If the addresses do not match, the item is considered counterfeit, and the transaction is canceled.
* **New Transaction Process:** If the buyer later wishes to resell the item, the system will generate a new key pair $$(V_2, W_2)$$ for the new secondary transaction and repeat the previous process.

## **Notes**

* The system utilizes the concept of public and private keys from cryptography to ensure the authenticity of items. The public key, which can be made public, is used for encrypting information, while the private key must be kept secret and is used for decrypting information.
* The NFC chip serves as a carrier, storing encrypted data related to the item, facilitating verification at different stages of the transaction.
* The system generates a new pair of keys for each transaction, increasing security because even if old keys are compromised, they will not affect new transactions.
* Every step in the process involves the generation, distribution, and use of keys, all designed to ensure the verification of authenticity in both the primary and secondary markets. This process leverages blockchain technology, where the NFT acts as a digital certificate for the item, and the NFC chip is the physical carrier storing the certificate's encrypted information.&#x20;
* By regenerating a new pair of keys after each transaction, the system enhances security and prevents potential abuse of private keys.

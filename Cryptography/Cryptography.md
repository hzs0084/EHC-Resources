# Cryptography

## What is Cryptography?
- Cryptography is the process of obscuring communications so only those with authorization have access.
- The process of obscuring those communications is known as encryption and the person on the other side of your communication must use decryption to access the information.
- There are 4 main principles of Cryptography:
    1. Confidentiality: Encrypted data may only be accessed by the intended party(s).
    2. Integrity: Encrypted data cannot be modified before it is recieved by the intended party(s) without alterations being detected.
    3. Non-Repudiation: The sender of the encrypted data cannot deny they sent it.
    4. Authentication: The party being sent the encrypted data is who they say they are.
- This [section](https://www.ibm.com/think/topics/cryptography) of the IBM website is a great resource for learning more about Cryptography and is what I used as a framework for this section of the Github.

 ## Applications of Cryptography
 - Anything you do online that involves an exchange of sensitive information should involve some sort of Cryptography.
 - The passwords you use are often verified through a two-factor authenticator (such as DUO for Auburn University).
 - End-to-End Encryption is often used for private messaging systems to ensure only invited parties may read your messages.
 - Cryptocurrencies such a Bitcoin and Etherium use heavy layers of encryption to ensure confidentiality for their users.
 - These are just a few select examples of the power of a good encryption algorithm.

## Methods of Encryption

### Symmetric (Secret Key)
- Both the sender and reciever share a secret key to encrypt and decrypt data.
- The main advantage of this form of encryption is speed.
- Symmetric encryption typically uses less computational power compared to Asymmetric.
- Common Uses:
    - AES (Advanced Encryption Standard): A symmetric block cipher adopted by the U.S. government.
    - Triple DES (3DES): Applies the DES algorithm three times with three keys; more suited for hardware; largely replaced         by the far safer AES.
    - Twofish: Successor of Blowfish; Uses block ciphering with a single key of 256 bits.
    - Blowfish: Best permutation technique for sipher-related encryption.
    - 
### Asymmetric (Public Key)
- Uses a mathematically linked key pair: a public key for encryption and a private key for decryption.
- The private key cannot be derived from the public key, making it highly secure.
- Enables safe key exchange.
- Common Uses:
    - RSA (Rivest, Shamir and Adleman)
    - Elliptic Curve Cryptography (ECC)
    - Digital Signature Algorithm (DSA)



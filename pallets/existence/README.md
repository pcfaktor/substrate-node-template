# Proof of Existence Module

Proof-of-existence is an approach to validating the authenticity and ownership of a digital object by storing information about the object on the blockchain.
Because the blockchain associates a timestamp and account with the object, the blockchain record can be used to "prove" that a particular object existed at a specific date and time.
It can also verify who the owner of a record was at that date and time.

## Digital objects and hashes

Instead of storing an entire file on the blockchain, it can be much more efficient to simply store a [cryptographic hash](https://en.wikipedia.org/wiki/Cryptographic_hash_function) of that file.
This is also known as a "digital fingerprint".
The hash enables the blockchain to store files of arbitrary size efficiently by using a small and unique hash value.
Because any change to a file would result in a different hash, users can prove the validity of a file by computing the hash and comparing that hash with the hash stored on chain.

![File Hash](https://raw.githubusercontent.com/substrate-developer-hub/substrate-docs/main/content/media/images/docs/tutorials/custom-pallet/file-hash.png)

## Digital objects and account signatures

Blockchains use [public key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) to map digital identities to accounts that have private keys.
The blockchain records the account you use to store the hash for a digital object as part of the transaction.
Because the account information is stored as part of the transaction, the controller of the private key for that account can later prove ownership as the person who initially uploaded the file.
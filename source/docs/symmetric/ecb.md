# AES Electronic code book

[RootMe Challenge: AES-ECB](https://www.root-me.org/en/Challenges/Cryptanalysis/AES-ECB): Find the password in this file and use it to validate the challenge.

## Symmetric methods

There are methods that can be used to alter the way a symmetric cipher works. Some of these are meant to increase the security of the cipher. Others to change a block cipher into a stream cipher.

## ECB

The most basic encryption mode is the electronic codebook (ECB) mode. The message is divided into blocks and each block is encrypted separately. The problem is that if you submit the same plain text more than once, you always get the same ciphertext. This gives attackers a place to begin analysing the cipher to attempt to derive the key. ECB is using the cipher exactly as it is described without improving its security.

There is no good reason to use ECB over CBC, if both ends of the communication can support CBC. Cipher block chaining is a strong deterrent to known plain text attacks.
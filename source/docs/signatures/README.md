# Introduction

## What?

A signature scheme typically consists of three different algorithms:

* A key pair generation algorithm that a signer uses to create a new private and public key (the public key can then be shared with anyone).
* A signing algorithm that takes a private key (signing key) and a message to produce a signature.
* A verifying algorithm that takes a public key (verifying key), a message, and a signature and
returns a success or error message.

* ECDSA is an elliptic curve variant of DSA that was invented only to circumvent patents in Schnorr signatures.

## Why?

Signatures are good for authenticating the origin of a message and the integrity of a message. In cryptography, we’re mostly interested in proofs of knowledge that don’t divulge the witness to the verifier. Such proofs are called zero-knowledge proofs (ZKPs).

ECDSA, like DSA, does not come with a zero-knowledge proof, while Schnorr signatures did. Nonetheless, ECDSA has been widely adopted and is one of the most used signature schemes. 

## How?

- [ ] [ECDSA: Conventional attack](ecdsa-conventional.md)
- [ ] [ECDSA: Implementation error](ecdsa-error.md)


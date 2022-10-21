# Determine symmetric key via other means

## Attack tree

```text
1 Fool sender into encrypting message using public key whose private key is known (OR)
    1.1 Convince sender that a fake key (with known private key) is the key of the intended recipient
    1.2 Convince sender to encrypt using more than one key–the real key of the recipient, and a key whose private key is known
    1.3 Have the message encrypted with a different public key in the background, unbeknownst to the sender
2 Have the recipient sign the encrypted symmetric key (OR)
3 Monitor computer memory of sender (OR)
4 Monitor computer memory of recipient (OR)
5 Determine key from pseudorandom number generator (OR)
    5.1 Determine state of randseed.bin when message was encrypted (OR)
    5.2 Implant malware (virus) that deterministically alters the state of randseed.bin (OR)
    5.3 Implant software that directly affects the choice of symmetric key
6 Implant malware (virus) that exposes the symmetric key
```

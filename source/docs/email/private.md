# Obtain private key of recipient

## Attack tree

```text
1 Factor RSA modulus/calculate ElGamal discrete log (OR)
2 Get private key from recipient's key ring (OR)
    2.1 Obtain encrypted private key ring (AND)
        2.1.1 Copy it from user's hard drive (OR)
        2.1.2 Copy it from backups (OR)
        2.1.3 Monitor traffic (OR)
        2.1.4 Implant malware (virus/worm) to expose copy of the private key
    2.2 Decrypt private key
        2.2.1 Break IDEA encryption (OR)
            2.2.1.1 Brute-force break IDEA (OR)
            2.2.1.2 Cryptanalysis of IDEA (OR)
        2.2.2 Learn passphrase
            2.2.2.1 Monitor keyboard when user types passphrase (OR)
            2.2.2.2 Convince user to reveal passphrase (OR)
            2.2.2.3 Use keyboard logging software to record passphrase when typed by user (OR)
            2.2.2.3 Guess passphrase 
3 Monitor recipient's computer memory (OR)
4 Implant malware (virus) to expose private key
5 Generate insecure private/public key pair for recipient
```

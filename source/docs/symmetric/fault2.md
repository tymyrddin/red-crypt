# AES Fault attack #2

[RootMe Challenge: Recover the key after a simulated fault attack](https://www.root-me.org/en/Challenges/Cryptanalysis/AES-Fault-attack-2): Recover the AES-128 key to get the validation password for this challenge.

To solve the challenge, you have access to an encryption oracle and have the possibility to inject fault during the encryption of chosen plaintexts. In order to simulate fault injections, the oracle takes as additional input an integer between 1 and 160 that represents one of the 160 Sboxes applied during an AES-128 encryption. The fault is injected on a single bit at the output of that Sbox.

This time, you only have 2 injections before recovering the key.

    Time limitation 	120 seconds
    Data limitation 	2 chosen plaintexts and fault injections


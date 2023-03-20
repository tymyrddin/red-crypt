# AES Fault attack #1

[RootMe Challenge: Recover the key using a simulated fault attack](https://www.root-me.org/en/Challenges/Cryptanalysis/AES-Fault-attack-1): Recover the AES-128 key to get the validation password for this challenge.

To solve this challenge you have access to an encryption oracle and may inject a single fault during the encryption of a chosen plaintext, repeatedly. In order to simulate the fault injection the oracle takes an additional parameter: an integer between 1 and 160 which represents one of the 160 Sboxes applied during an AES-128 encryption. The fault is injected on a single bit at the output of that Sbox.

    Time limitation 	120 seconds
    Data limitation 	32 chosen plaintexts and fault injections

## Differential Fault attacks

Differential Fault Attacks (DFA) has emerged. DFA has shown that several ciphers can be compromised if the faults can be suitably controlled. DFA is not restricted to old ciphers, but can be a powerful attack vector even for modern ciphers, like the Advanced Encryption Standard (AES).

## Resources

* [A Differential Fault Attack Technique against SPN Structures, with Application to the AES and KHAZAD - Piret and Quisquater](https://repository.root-me.org/Cryptographie/Sym%C3%A9trique/EN%20-%20A%20Differential%20Fault%20Attack%20Technique%20against%20SPN%20Structures,%20with%20Application%20to%20the%20AES%20and%20KHAZAD%20-%20Piret%20and%20Quisquater.pdf)


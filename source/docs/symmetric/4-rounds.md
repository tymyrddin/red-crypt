# AES 4 rounds

[RootMe Challenge: Classical attack on AES-128 reduced to 4 rounds](https://www.root-me.org/en/Challenges/Cryptanalysis/AES-4-Rounds): The encryption oracle available at the address below performs 4-round AES-128 encryption (the last round does not apply the MixColumns transformation). You can query as many chosen plaintexts as you need.

Exploit this reduction of the round number to recover the secret key and then retrieve the password to validate this challenge.

    Time limitation 	None
    Data limitation 	None

## Resources

* [FIPS 197 - Advanced Encryption Standard (AES)](https://repository.root-me.org/Cryptographie/Sym%C3%A9trique/EN%20-%20FIPS%20197%20-%20Advanced%20Encryption%20Standard%20(AES).pdf)
* [The Block Cipher SQUARE - Daemen, Knudsen, Rijmen](https://repository.root-me.org/Cryptographie/Sym%C3%A9trique/EN%20-%20The%20Block%20Cipher%20SQUARE%20-%20Daemen,%20Knudsen,%20Rijmen.pdf)

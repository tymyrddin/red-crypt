# Mono-alphabetic substitution: Caesar

[RootMe Challenge: Monoalphabetic substitution - Caesar](https://www.root-me.org/en/Challenges/Cryptanalysis/Monoalphabetic-substitution-Caesar): We just caught the messenger of the Emperor. He transmitted a coded message to his son. This could be an important message. You’ve to decrypt it ! To validate, you must enter the concatenation of the first letters of each line followed by the concatenation of the last letters of each line (for example : `tfhqdlhfpkmeokgq`).

## Substitution ciphers

The oldest ciphers in recorded history are substitution ciphers. With this method, each letter of plaintext is substituted for some letter of ciphertext according to some algorithm. There are two types of substitution ciphers: single-alphabet (or mono-alphabet) and multi-alphabet (or poly-alphabet). In a single-alphabet substitution cipher, a given letter of plaintext is always substituted for the corresponding letter of ciphertext. For example, an `a` in the plaintext would always be a `k` in the ciphertext.

## Caesar cipher

One of the most widely known historical encryption methods is the Caesar cipher. According to the Roman historian Gaius Suetonius Tranquillus (c. 70–130 CE), Julius Caesar used this cipher to encrypt military messages, shifting all letters of the plaintext three places to the right.

Although the Caesar cipher is not useful for modern cryptographic needs, it does contain all the fundamental concepts needed for a cryptography algorithm

* A plaintext message
* An algorithm: shift every letter
* A key: for example +3
* A ciphertext

This is, essentially, the same structure used by all modern symmetric algorithms. Because there are only 26 letters in the English alphabet, the key space is 26 (in English).

## Solution

I used [DCode: Caesar](https://www.dcode.fr/caesar-cipher) to first shift with 1 for the first word, shift with 2 to get the second word, 3 for the third word, etc. 
Oh, and the poem is in French, of course, which made it a bit harder:

```text
un deux trois
j'irai dans les bois
quatre cing six
cueillir des cerises
sept huit neuf
dans un panier neuf
dix onze douze
elles seront toutes rouges
```

Result:

```text
ujqcsddessxsffes
```

## Resources

* [Le code de César](https://www.root-me.org/spip.php?article82)
* [Le chiffrement par décalage](https://repository.root-me.org/Cryptographie/Sym%C3%A9trique/FR%20-%20Le%20chiffrement%20par%20d%C3%A9calage.pdf)

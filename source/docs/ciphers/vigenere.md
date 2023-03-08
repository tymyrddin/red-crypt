# Poly-alphabetic substitution: Vigenère

[RootMe Challenge: Polyalphabetic substitution: Vigenère](https://www.root-me.org/en/Challenges/Cryptanalysis/Polyalphabetic-substitution-Vigenere): We need your expert opinion on this document. This is an old letter, and it appears that it is important for the pirates that we are searching for. Your mission is to decipher the text and give us the full name of the author (example : "John Doe").

## Poly-alphabetic substitution

Multi-alphabet substitution uses multiple substitutions, so that, for example, an `a` in the plaintext is sometimes a `k` and sometimes a `j` in the ciphertext. 

## Vigenère

Perhaps the most widely known multi-alphabet cipher is the Vigenère cipher. This cipher was described in 1553 by Giovan Battista Bellaso, but was misattributed to nineteenth century cryptographer Blaise de Vigenère. It is a method of encrypting alphabetic text by using a series of different mono-alphabet ciphers selected based on the letters of a keyword. Bellaso also added the concept of using any keyword, thereby making the choice of substitution alphabets difficult to calculate.

For many years, Vigenère was considered very strong, even unbreakable. In the nineteenth century, Friedrich Kasiski published a technique for breaking the Vigenère cipher.

## Math

The math for Vigenère looks very similar to that of Caesar, with one important difference: the value $K$ changes:

\begin{align} C_i\equiv P_i \oplus K_i\mod(26) \end{align}

The $i$ denotes the current key with the current letter of plaintext and the current letter
of ciphertext. Many sources use $M$ (for message) rather than $P$ (for plaintext) in this notation. 

## Solution

I used [Vigenere Hack](https://github.com/tymyrddin/scripts-cryptanalysis/blob/main/ciphers/vigenere/vigenere_hack.py) which tells me the **Key/Password** is most likely `THEMENTOR`. Using that I got a halfway readable text. Obviously the latter part has another **Key/Password**. Not needed, I recognise the text.

The **Conscience of a Hacker** (also known as **The Hacker Manifesto**) is a small essay written January 8, 1986, by a computer security hacker who went by the handle (or pseudonym) of **The Mentor**, who belonged to the second generation of hacker group Legion of Doom.

The Manifesto was written after the author's arrest, and first published in the underground hacker ezine [Phrack](http://phrack.org/).


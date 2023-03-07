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

[DCode](https://www.dcode.fr/vigenere-cipher) tells me the **Key/Password** is `THEMENTOR`. Using that I got a halfway readable text. Obviously the latter part has another **Key/Password**. Not needed, I recognise the text.

```text
The Hacker Manifesto

Un autre s'est fait prendre aujourd'hui, c'est partout dans les journaux. "Scandale: Un adolescent arrete pour crime informatique,
"Arrestation d'un 'hacker' apres le piratage d'une banque"...

Satanes gosses, tous les memes.

Mais avez vous, dans votre psychologie en trois piece et votre profil
technocratique de 1950, un jour pense a regarder le monde derriere les yeux d'un hacker?
Ne vous etes vous jamais demande ce qui l'avait fait agir, quelles forces l'avaient modele?
Je suis un hacker, entrez dans mon monde...
Le mien est un monde qui commence avec l'ecole... Je suis plus astucieux que la plupart des autres enfants, les conneries qu'ils m'apprennent me lassent...

Je suis au college ou au lycee. J'ai ecoute les professeurs expliquer pour la quinzieme fois comment reduire une fraction.
Je l'ai compris. "Non Mme Dubois, je ne peux pas montrer mon travail. Je l'ai fait dans ma tete"
Satane gosses. Il l'a certainement copie. Tous les memes.

J'ai fait une decouverte aujourd'hui. J'ai trouve un ordinateur.
Attends une minute, c'est cool. Ca fait ce que je veux.
```

The **Conscience of a Hacker** (also known as **The Hacker Manifesto**) is a small essay written January 8, 1986 by a computer security hacker who went by the handle (or pseudonym) of The Mentor (born `Loyd Blankenship`), who belonged to the second generation of hacker group Legion of Doom.

The Manifesto was written after the author's arrest, and first published in the underground hacker ezine Phrack. 

## Resources

* [The code book: the science of secrecy from ancient Egypt to quantum cryptography](https://archive.org/details/codebook00simo/page/n13/mode/2up)


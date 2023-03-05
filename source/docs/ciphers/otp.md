# Poly-alphabetic substitution: One Time Pad

[RootMe Challenge: Polyalphabetic substitution - One Time Pad](https://www.root-me.org/en/Challenges/Cryptanalysis/Polyalphabetic-substitution-One-Time-Pad): Break the code, hint: Apocalypsis 10.2

## One-time pad

The concept behind a one-time pad is that the plaintext is somehow altered by a random string of data so that the resulting ciphertext is truly random. To truly be a one-time pad, by modern standards, a cipher needs two properties:

* The key is only used once. After a message is enciphered with a particular key, that key is never used again. This makes the one-time pad quite secure, but also very impractical for ongoing communications. 
* The key must be at least as long as the message. That prevents any patterns from emerging in the ciphertext.

One-time pads are still used for communications today, but only for the most sensitive communications. The keys must be stored in a secure location, such as a safe, and used only once for very critical messages. The keys for modern one-time pads are simply strings of random numbers sufficiently large enough to account for whatever message might be sent.

While one-time pads provide perfect secrecy if generated and used properly, small mistakes can lead to successful cryptanalysis.

## Vernam cipher

The Vernam cipher is a type of one-time pad. Gilbert Vernam proposed a stream cipher that would be used with teleprinters. It would combine character by character a prepared key that was stored on a paper tape, with the characters of the plaintext to produce the ciphertext. The recipient would again apply the key to get back the plaintext.

Vernam’ s method uses the binary XOR (Exclusive OR) operation applied to the bits of the message.

## Resources

* [Vernam Cipher (One Time Pad Vigenere)](https://www.dcode.fr/vernam-cipher)


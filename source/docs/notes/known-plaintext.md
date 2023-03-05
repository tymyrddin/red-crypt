# Known-plaintext attack

In known-plaintext attacks, an attacker has access to the ciphertext and its corresponding plaintext. The goal is to guess the secret key (or a number of secret keys), or to develop an algorithm which would allow for decrypting further messages. The attacker can not actively change the data or secret keys to be processed by the cipher.

This type of attack is useful when finding or knowing the plaintext of some portions of the ciphertext using information gathering techniques.

For example, known-plaintext attacks were used for attacking the ciphers used during the Second World War, like the attacks on German Enigma ciphers. The English intelligence targeted some common phrases, commonly appearing in encrypted German messages, like weather forecasts or geographical names.

The ancient and simple XOR cipher of the early digital days, can also easily be broken by knowing only some parts of plaintext and corresponding encrypted messages.

Modern ciphers are generally resistant against purely known-plaintext attacks, save for the old encryption method used in the PKZIP application. Having just one copy of encrypted file, together with its original version, it was possible to completely recover the secret key.

## Resources

* [Breaking Machine Ciphers](http://practicalcryptography.com/cryptanalysis/breaking-machine-ciphers/)
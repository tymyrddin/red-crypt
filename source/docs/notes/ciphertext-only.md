# Ciphertext-only attack

This is a type of attack model in which the attacker only knows the ciphertext (encrypted text) and has no knowledge of the plaintext (decrypted text). In the history of cryptography, early ciphers, implemented using pen-and-paper, were routinely broken using ciphertexts alone.

In this attack vector, the attacker gains access to a collection of ciphertext. Although the plaintext can still not be read, it is theoretically possible to determine the ciphertext from the collection. On occasion, it works. 

A one time pad (OTP) can not be broken because there are many answers (that make sense) given a specific ciphertext, so there is no way to know the intended plaintext. In practice, an attacker usually has at least some knowledge of the plaintext, like the set of characters used or the language used.

## Remediation

A cipher whose key space is too small is subject to brute force attack with access to nothing but ciphertext by simply trying all possible keys.

Do not derive keys for otherwise impregnable ciphers like AES from a user-selected password. Because users rarely use passwords with anything close to the entropy of the cipher's key space, such systems are often quite easy to break using only ciphertext.

## Resources

* [How to Calculate Password Entropy?](https://generatepasswords.org/how-to-calculate-entropy/)
* [Unicity Distance](http://www.practicalcryptography.com/cryptanalysis/text-characterisation/statistics/#unicity-distance)
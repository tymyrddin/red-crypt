# ECDSA: Conventional attack

[RootMe Challenge: Conventional attack on ECDSA](https://www.root-me.org/en/Challenges/Cryptanalysis/ECDSA-Introduction): You are provided with 30 messages to break our ECDSA cipher. Each message has been signed with our private key. Get the flag by faking a signature.

Retrieve the necessary files using SSH then validate the challenge by sending your signed message to the provided network service.

## Elliptic curve digital signature algorithm

ECDSA, an elliptic curve variant of DSA that was invented only to circumvent patents in Schnorr signatures. The signature scheme is specified in many standards including ISO 14888-3, ANSI X9.62, NIST’s FIPS 186-2, IEEE P1363, and so on. Not all standards are compatible, and applications that want to interoperate have to make sure that they use the same standard.

As with all such schemes, the public key is pretty much always generated according to the same formula:

* The private key is a large number x generated randomly.
* The public key is obtained by viewing $x$ as an index in a group created by a generator (called base point in elliptic curve cryptography).

To compute an ECDSA signature, you need the same inputs required by a Schnorr signature: a hash of the message you’re signing $(H(m))$, your private key $x$, and a random number $k$ that is unique per signature.

* $k$ must never be repeated nor be predictable! Without that, it is trivial to recover the private key.
* Even more subtle, if the nonce $k$ is not picked uniformly and at random (specifically, if you can predict the first few bits), there still exist powerful attacks that can recover the private key in no time (so-called lattice attacks). In theory, these kinds of key retrieval attacks are called **total breaks** (because they break everything!). They are quite rare in practice, which makes ECDSA an algorithm that can fail in spectacular ways.

## Resources

* [Elliptic_Curve_Digital_Signature_Algorithm](https://en.wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm)
* [NIST.FIPS.186-4 Digital Signature Standard](https://repository.root-me.org/Cryptographie/EN%20-%20NIST.FIPS.186-4%20Digital%20Signature%20Standard.pdf)
* [Practical cryptography for developers: ECDSA: Elliptic Curve Signatures](https://cryptobook.nakov.com/digital-signatures/ecdsa-sign-verify-messages)

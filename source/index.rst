Beyond the visible
==============================================

Come backstage with us to discover what is usually not seen concerning encoded and encrypted data in rest, underway, and in use. Witness the strategic decisions, the designing of algorithms, the complex implementations, the innovative (yet old and not really changing) technological solutions, the endless resources invested into research and development of security and privacy ... and everything that isn't, and everything that is, but gets hacked.

.. image:: _static/images/in-progress.png
  :alt: Forever in progress ...

----

.. toctree::
   :maxdepth: 1
   :includehidden:
   :caption: Preparation

   Build a local testlab <https://red.tymyrddin.dev/projects/testlab/en/latest/docs/crypto/README.html>

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Notes on techniques

   docs/notes/README.md
   docs/notes/classical.md
   docs/notes/bruteforce.md
   docs/notes/models.md
   docs/notes/goals.md
   docs/notes/block.md
   docs/notes/aes.md
   docs/notes/stream.md
   docs/notes/hashes.md
   docs/notes/rsa.md
   docs/notes/dh.md
   docs/notes/ec.md

----

.. toctree::
   :maxdepth: 1
   :includehidden:
   :caption: Coding classical ciphers

   docs/classical/README.md
   Caesar's cipher <https://github.com/tymyrddin/scripts-classical-ciphers/blob/main/caesar/README.md>
   Vigenere's cipher <https://github.com/tymyrddin/scripts-classical-ciphers/blob/main/vigenere/README.md>
   Columnar transposition cipher <https://github.com/tymyrddin/scripts-classical-ciphers/blob/main/columnar/README.md>
   Rail fence transposition cipher <https://github.com/tymyrddin/scripts-classical-ciphers/blob/main/railfence/README.md>

.. toctree::
   :maxdepth: 1
   :includehidden:
   :caption: Coding modern ciphers

   docs/modern/README.md
   AES: A symmetric block cipher <https://github.com/tymyrddin/scripts-modern-ciphers/tree/main/aes>
   LFSR: Linear feedback shift registers <https://github.com/tymyrddin/scripts-modern-ciphers/tree/main/aes>
   RSA: An asymmetric key exchange <https://github.com/tymyrddin/scripts-modern-ciphers/tree/main/rsa>

----

.. toctree::
   :maxdepth: 1
   :includehidden:
   :caption: Classical cipher breaking

   docs/ciphers/README.md
   docs/ciphers/caesar.md
   docs/ciphers/vigenere.md
   docs/ciphers/rail-fence.md
   docs/ciphers/polybe.md
   docs/ciphers/gedefu.md
   docs/ciphers/enigma.md
   docs/ciphers/otp.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: AES busting

   docs/aes/README.md
   docs/aes/cbc-bit-flipping.md
   docs/aes/ecb.md
   docs/aes/iv.md
   docs/aes/4-rounds.md
   docs/aes/ctr.md
   docs/aes/fault1.md
   docs/aes/cbc-padding.md
   docs/aes/cpa.md
   docs/aes/sc-first-round.md
   docs/aes/weaker-variant.md
   docs/aes/fault2.md
   docs/aes/pmac.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Down streams

   docs/streams/README.md
   docs/streams/lfsr.md

.. toctree::
   :maxdepth: 1
   :includehidden:
   :caption: Hash hacking

   docs/hashes/README.md
   docs/hashes/dcc.md
   docs/hashes/dcc2.md
   docs/hashes/lm.md
   docs/hashes/md5.md
   docs/hashes/nt.md
   docs/hashes/sha2.md
   docs/hashes/cisco.md
   docs/hashes/hash-length.md
   docs/hashes/sha3.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: RSA puzzling

   docs/rsa/README.md
   docs/rsa/factorisation.md
   docs/rsa/oracle.md
   docs/rsa/corrupted-key1.md
   docs/rsa/fractions.md
   docs/rsa/modulus.md
   docs/rsa/padding.md
   docs/rsa/signature.md
   docs/rsa/corrupted-key2.md
   docs/rsa/corrupted-key3.md
   docs/rsa/multiple-recipients.md
   docs/rsa/lee-cooper.md

.. toctree::
   :maxdepth: 1
   :includehidden:
   :caption: Data dares

   docs/data/README.md
   docs/data/elf64-pid.md
   docs/data/pkzip.md
   docs/data/bmp-xor.md
   docs/data/insecure-storage1.md
   docs/data/android-lock.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Diffie-Hellman

   docs/dh/README.md
   docs/dh/discrete-log.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Elliptic curve balls

   docs/ecc/README.md
   docs/ecc/ecdhe.md
   docs/ecc/ecdsa-conventional.md
   docs/ecc/ecdsa-error.md

----

.. image:: _static/images/books.png
  :alt: Useful books
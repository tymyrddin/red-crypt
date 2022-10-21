Beyond the visible
==============================================

Many people assume that when information is not being transmitted, it is safe. But to effectively encrypt personally
identifiable information, many variables must be considered, including the state the data is in:
at rest, in transit, or in use.

Data at rest is more valuable than data in transit because it often has a higher level of sensitive information.
And just because data is at rest does not mean it is not moving. Many data breaches happen due to a lost USB
drive or laptop.

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Attacks

   docs/attacks/README.md
   docs/attacks/plaintext.md
   docs/attacks/ciphertext.md
   docs/attacks/unknown-key.md
   docs/attacks/forgery.md
   docs/attacks/group-impersonation.md
   docs/attacks/side-channel.md
   docs/attacks/pgp.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Prevention

   docs/prevent/README.md
   docs/prevent/transit.md
   docs/prevent/rest.md
   docs/prevent/use.md

.. toctree::
   :caption: Links

   Red Team <https://tymyrddin.github.io/red/>
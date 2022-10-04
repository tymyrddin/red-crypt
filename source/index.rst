Beyond the visible
==============================================

Many people assume that when information is not being transmitted, it is safe. But to effectively encrypt personally
identifiable information, many variables must be considered, including the state the data is in:
at rest, in transit, or in use.

Data at rest is more valuable than data in transit because it often has a higher level of sensitive information.
And just because data is at rest doesn not mean it is not moving. Many data breaches happen due to a lost USB
drive or laptop.

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: In transit

   docs/transit/README.md
   docs/transit/*

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: At rest

   docs/rest/README.md

.. toctree::
   :caption: Links

   Red Team <https://tymyrddin.github.io/red/>
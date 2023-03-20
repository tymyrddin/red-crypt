# Side channel AES: first round

[RootMe Challenge: Side Channel - AES: first round](https://www.root-me.org/en/Challenges/Cryptanalysis/Side-Channel-AES-first-round): To perform secure AES encryption, your intern R. Hamming has just acquired a new state-of-the-art embedded card. Young, carefree and confident, he challenges you to find the encryption key he uses. But beware, this card is resistant to fault injections! Armed only with your oscilloscope, you, the great K. Pearson, decide to take an interest in the power consumption of this mysterious card...

Notes:

* The validation flag is the key used by AES converted to ASCII format
* The length of the key is the minimum size of an AES key
* The .bini8 file starts with an 8 bytes header in little endian.
* The first 4 bytes give you the number of bytes representing a single capture during AES encryption. The next 4 bytes tell you the number of AES encryption runs that were performed to generate this file. The bytes are signed, and 1 byte = 1 piece of data (except for the header)
* You have the plaintexts used. They are in unsigned hexadecimal format.

## Resources

* [Correlation Power Analysis with a Leakage Model](https://link.springer.com/content/pdf/10.1007/978-3-540-28632-5_2.pdf)

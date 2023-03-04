# Shift cipher

Shift Cipher is one of the earliest and the simplest cryptosystems. A given plaintext is encrypted into a ciphertext by shifting each letter of the given plaintext by `n` positions.

Opening the challenge will download a binary `ch7.bin`. Use this short python program to keep on turning.

```text
#!/bin/env python3

text = open('ch7.bin','rb').read()

i = 0
while i < 11:
    print(''.join([chr(c - i) for c in text]))
    i += 1
```

## Resources

* [Dcode: Shift cipher](https://www.dcode.fr/shift-cipher)
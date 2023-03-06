# Transposition: Rail Fence

[RootMe Challenge: Transposition - Rail Fence](https://www.root-me.org/en/Challenges/Cryptanalysis/Transposition-Rail-Fence): USA, American Civil War, August 3, 1862. You are on patrol around the camp when you see an enemy rider. Once you intercepted him, you discover that he carries a message but nobody at the camp manages to decipher it. You are the only hope to find the hidden information. It could be crucial !

## Transposition

Transposition ciphers provide yet another avenue for encryption. The simplest implementation of a transposition cipher is to reverse the plaintext.

## Rail fence cipher

The rail fence cipher may be the most widely known transposition cipher. You encrypt the message by alternating each letter on a different row.

```text
Attack at dawn
```

is written like this:

```text
A t c a d w
 t a k t a n
```

## Solution

Using [DCode: Rail Fence (Zig-Zag) Cipher](https://www.dcode.fr/rail-fence-cipher):

```text
Will·invade·Kentucky·on·October·the·eighth.·signal·is·"Frozen·chicken"
```


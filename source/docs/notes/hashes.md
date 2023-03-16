# Hacking hashes

Hash functions, like MD5, SHA-1, SHA-256, SHA-3, and BLAKE2, are used in digital signatures, public-key encryption, integrity verification, message authentication, password protection, key agreement protocols, and many other cryptographic protocols.

## Cracking hashes

Having the hash value of something, and wanting to calculate the data it came from, there is not a unique solution. In practice, for short objects like passwords, there is. So, if someone uses an MD5 function to obscure a password, which is done by some old web applications, then you can reverse it by guessing passwords until finding a match. 

There is no mathematical way to undo a hash function, so the best way is to make (or use) a library. That's how hash cracking works. Not complicated, just annoying.

## Windows passwords

The hash used by, for example, Windows Server is the NT Hash. If two users have the same password, they have exactly the same hash. 

The algorithm Microsoft uses takes the password and encodes in Unicode instead of ASCII, to allow for passwords in languages such as Chinese and Japanese that do not encode with 8-bits per character but 16-bits per character. Then it is run through MD4 (an algorithm even older than MD5) to produce the NT hash value.

Because password hashes have no variation and any two users with the same password will have the same hash, all the hackers that had cracked wordlists for the last decades have put their results on the internet. For example, you can use the [crackstation](https://crackstation.net/) or  [hashes.com](https://hashes.com/en/decrypt/hash). This availability has even resulted in a situation where you can just Google frequently used password hashes.

When the passwords cannot be cracked, you can try guessing using `hashlib`. Make series of guesses (or use a passwordlist), hash them, and hunt for the answer. 

```text
import hashlib

hashlib.new("md4", "password".encode("utf-16le")).hexdigest()
```

## Linux password hashes

In Linux, the hashes can be found in the `/etc/shadow` file.

```text
username:$6$ligE06T/QLQMANm9$8GDajwZJahwNnnW/OtfwLUGZHYcmTd9RByNz2e32iJAx37fSu7R1mpxTwWOqwlc4etyR/SLBkfiksitUHXRVV.:18961:0:99999:7:::
```

After each username comes `$6`, which indicates it is a type 6 password, then there is a random string of characters that goes up to the next dollar sign, the salt, and then an even longer random string of characters, which is the actual password hash itself.

When users have the same password, they have completely different hashes, because a random salt is added before hashing them, to obscure the fact that these passwords are the same.

Besides salting, stretching is also used. Calculating the hash uses 5,000 rounds of SHA-512, which takes much more CPU time. This might slow down attackers trying to make dictionaries of password hashes.

Make series of guesses (or use a wordlist for a dictionary attack), hash them, and hunt for an answer. 

```text
from passlib.hash import sha512_crypt

sha512_crypt.using(salt="ligE06T/QLQMANm9", rounds=5000).hash("password")
```

This will be very, very, time-consuming.

## Using hashcat

[Hashcat](https://hashcat.net/hashcat/) comes pre-installed in Kali and Parrot OS. In addition to Hashcat, also download a wordlist like the [10-million-password-list-top-100.txt](https://github.com/danielmiessler/SecLists/blob/master/Passwords/Common-Credentials/10-million-password-list-top-100.txt) or [rockyou.txt](https://github.com/teamstealthsec/wordlists/blob/master/rockyou.txt.gz). It contains a list of commonly used passwords and is popular among pen testers. You can find the Rockyou wordlist under `/usr/share/wordlists` in Kali Linux.

And the [mode](https://hashcat.net/wiki/doku.php?id=hashcat#options) (`-m`) for the type of hash.

For example, the hash mode value for SHA1 is `100`, and for doing a dictionary attack (`-a 0`):

    $ hashcat -m 100 -a 0 sha1.txt /usr/share/wordlists/rockyou.txt

## Using John the Ripper

While you can use popular wordlists like RockYou, [John the Ripper](https://www.openwall.com/john/) also has its own set of wordlists with thousands of common passwords. This makes John very effective when cracking systems with weak passwords.

No mode needs to be entered. John recognises the hash type, generates hashes on the fly for all the passwords in the dictionary, and stops when a generated hash matches the current hash.

If you are using Kali Linux, John is pre-installed.

```text
$ john --single --format=raw-sha1 crackthishash.txt
```

`crackthishash.txt` contains username and hash value of the password (separated by a colon).

Dictionary attack:

```text
$ john --wordlist=/usr/share/wordlists/rockyou.txt --format=raw-sha1 crackthishash.txt
```

## RootMe challenges

* [DCC Hash](../hashes/dcc.md)
* [DCC2 Hash](../hashes/dcc2.md)
* [LM Hash](../hashes/lm.md)
* [Message Digest 5](../hashes/md5.md)
* [NT Hash](../hashes/nt.md)
* [SHA-2 Hash](../hashes/sha2.md)
* [CISCO Salted password](../hashes/cisco.md)
* [SHA-3 Hash](../hashes/sha3.md)


## Security

Despite their apparent simplicity, hash functions can cause major security troubles when used at the wrong place or in the wrong way—for example, when weak checksum algorithms like CRCs are used instead of a crypto hash to check file integrity in applications transmitting data over a network. However, this weakness pales in comparison to some others, which can cause total compromise in seemingly secure hash functions.
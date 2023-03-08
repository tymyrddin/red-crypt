# ELF64 PID encryption

[RootMe: ELF64 - PID encryption](https://www.root-me.org/en/Challenges/Cryptanalysis/ELF64-PID-encryption): Bad idea to use predictable stuff.

## ELF

ELF (Executable and Linkable Format) is a standard file format for executable files, object code, shared libraries and core dumps. Linux and many UNIX-like operating systems use this format.

## Solution

[ch21.c](https://github.com/tymyrddin/scripts-cryptanalysis/blob/main/data/ELF64%20-%20PID%20encryption/ch21.c): If the first parameter passed to the file is equal to the hash of the pid of the file salted with `$1$awesome`, we’ll have a shell.

We have to guess the PID though.

[ahaAha.py](https://github.com/tymyrddin/scripts-cryptanalysis/blob/main/data/ELF64%20-%20PID%20encryption/ahaAha.py) takes its own pid, prints its pid+1, and hashes pid+1 with `$1$awesome`.

```text
cryptanalyse-ch21@challenge01:~$ cd /tmp
cryptanalyse-ch21@challenge01:/tmp$ vi aha.py
cryptanalyse-ch21@challenge01:/tmp$ cd ~
cryptanalyse-ch21@challenge01:~$ ./ch21 $(python3 /tmp/aha.py)
$1$awesome$jAoZL2/ryRF9HRhYI9daW.=$1$awesome$5iuf4NVeErY8xYO/mxRC80Fail... :/
cryptanalyse-ch21@challenge01:~$ ./ch21 $(python3 /tmp/aha.py)
$1$awesome$O0AKFH9d5sNQf37g8ElUC0=$1$awesome$O0AKFH9d5sNQf37g8ElUC0WIN!
bash-5.0$ cat .passwd
```

Note: The `crypt` module is deprecated (see [PEP 594](https://peps.python.org/pep-0594/#crypt) for details and alternatives). Deprecated since version 3.11, will be removed in version 3.13. The [hashlib](https://docs.python.org/3/library/hashlib.html#module-hashlib) module is a potential replacement for certain use cases.

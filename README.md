# gpg-signature-guide

## Introduction

Gpg Signature Guide for newbies

  In the scope of the [EU-FOSSSA-2 Project](https://joinup.ec.europa.eu/collection/eu-fossa-2), [hackathon](https://eufossahackathon.bemyapp.com/), the memebers of the tomcat team give us a samll introduction. Here you will find my findings.

## Generate yout key


```bash
 brew install gpg 
```


```bash
gpg --gen-key

gpg (GnuPG) 2.2.15; Copyright (C) 2019 Free Software Foundation, Inc.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Note: Use "gpg --full-generate-key" for a full featured key generation dialog.

GnuPG needs to construct a user ID to identify your key.

Real name: Angel-Ventura MENDO GOMEZ
Email address: MyEmail@toto.com
You selected this USER-ID:           
    "Name  <MyEmail@toto.com>"

Change (N)ame, (E)mail, or (O)kay/(Q)uit? O
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.

gpg: key XXXXXXXXXXXXXXXX marked as ultimately trusted


```

```bash
gpg --armor  --export  MyEmail@toto.com

-----BEGIN PGP PUBLIC KEY BLOCK-----
...
iBTgeoePzguaboCGpU/UFo+VyPIb9ccUAN1+XutqLazogLt++MMzFfDcnW7IVCPo
LNQvncwgcUSg6zUWAUshz4xY5IZjHC8CUBtJABEBAAG0MkFuZ2VsLVZlbnR1cmEg
TUVORE8gR09NRVogPGFuZ2VsdmVudHVyYUBnbWFpbC5jb20+iQFUBBMBCAA+FiEE
czb91aSb95+8XnJagrE3+TTarW0FAlzOn7QCGwMFCQPCZwAFCwkIBwIGFQoJCAsC
BBYCAwECHgECF4AACgkQgrE3+TTarW3kuQf7Bm7IIJdbq0UZetMJqgp1JVFXkHs4
...
-----END PGP PUBLIC KEY BLOCK-----
```

Commit into one of those servers:

* http://pgp.mit.edu/
* https://hkps.pool.sks-keyservers.net/


[Doc](http://www.cryptnet.net/fdp/crypto/keysigning_party/en/keysigning_party.html#generating_revocation_cert)


Signn a friend KEY :

```bash
 gpg --recv-keys KEY
 gpg --sign-key KEY
 gpg --send-key KEY
```



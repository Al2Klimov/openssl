# How to build OpenSSL 1.0.2k on M3 Macs

## What you do

* `git ls-files -z |xargs -0 -n 1 perl -pi -e 's/-arch i386//g'`
  (already done in this branch)
* `./config no-asm`
* `make`

## What you get

* `./libcrypto.a`
* `./libssl.a`
* `./include/openssl/`
* `./apps/openssl` (`file(1)`: "Mach-O 64-bit executable arm64")

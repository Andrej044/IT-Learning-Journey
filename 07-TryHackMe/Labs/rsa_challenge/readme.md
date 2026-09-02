# TryHackMe RSA Challenge — Close Prime Factorization

## Challenge overview

In this challenge, an intercepted Python file revealed how an RSA key pair and encrypted message were generated. The objective was to recover the secret message from the published ciphertext and public modulus.

The relevant weakness was in the generation of the two RSA primes:

p = getPrime(1024)
q = primo(p)

Instead of generating two independent random primes, the program selected q as the next prime after p. Consequently, p and q were extremely close together.

Vulnerability

RSA security relies on the difficulty of factoring the public modulus:

n = p × q

When p and q are sufficiently large, random, and independent, recovering them from n is computationally infeasible with conventional computers.

However, when the primes are very close, the modulus can be factored efficiently using Fermat’s factorization method:

n = a² − b²
n = (a − b)(a + b)

This gives:

p = a − b
q = a + b

Because the challenge’s primes were consecutive, only a small search around the square root of n was required.

Solution approach

The challenge was solved using the following process:

Extract the ciphertext c, modulus n, and public exponent e from the recovered file.

Apply Fermat factorization to recover p and q.

Confirm that p × q = n.

Calculate Euler’s totient:

φ(n) = (p − 1)(q − 1)

Calculate the private exponent:

d = e⁻¹ mod φ(n)

Decrypt the ciphertext:

m = cᵈ mod n

Convert the resulting integer back into readable bytes.

Solver

from math import isqrt
from Crypto.Util.number import long_to_bytes

c = CIPHERTEXT
n = MODULUS
e = 0x10001  # 65537

a = isqrt(n)

if a * a < n:
    a += 1

while True:
    b_squared = a * a - n
    b = isqrt(b_squared)

    if b * b == b_squared:
        p = a - b
        q = a + b
        break

    a += 1

assert p * q == n

phi = (p - 1) * (q - 1)
d = pow(e, -1, phi)

plaintext_integer = pow(c, d, n)
plaintext = long_to_bytes(plaintext_integer)

print(plaintext.decode())

Replace CIPHERTEXT and MODULUS with the values supplied by the challenge.

Key lesson

RSA primes must be generated independently using a cryptographically secure random source. Even very large primes can produce an insecure key if they are too close together.

The challenge demonstrates that cryptographic security depends not only on key size, but also on correct key generation.

The recovered TryHackMe flag has intentionally been omitted. This repository documents the technique without publishing the room’s final answer.
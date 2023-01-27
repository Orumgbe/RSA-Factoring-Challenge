RSA algorithm is an asymmetric cryptography algorithm. It is a public key cryptosystem that is used to secure data transmissions.
This project explores the factorisation principle which the RSA encryption and decryption process capitalises upon.

Steps on how the cryptosystem works:
1. Generating the keys

    Select two large prime numbers, x and y.
    Calculate n = xy.
    Calculate the totient function; ϕ(n)=(x−1)(y−1).
    Select an integer e, such that e is co-prime to ϕ(n) and 1<e<ϕ(n).
    The pair of numbers (n,e) makes up the public key.

    Note: Two integers are co-prime if the only positive integer that divides them is 1.

    Calculate d such that e.d = 1 mod ϕ(n).

    'd' can be found using the extended euclidean algorithm. The pair (n,d) makes up the private key.

2. Encryption

	Given a plain text P, represented as a number, the ciphertext C is calculated as:

	C = P^e mod n.

3. Decryption

	Using the private key (n,d), the plain text can be found using:

	P = C^d mod n.

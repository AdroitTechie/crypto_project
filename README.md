# crypto_project
This Project is based on Digital Signature Scheme
         
 (ElGamal Digital Signature)
A powerful and practical public-key and digital signature scheme was produced by ElGamal. We implement the classical and modified ElGamal digital signature scheme to compare and to test their functionality, reliability and security.

The objective of the proposed project is to design an ElGamal digital signature algorithm such that the time complexity of the algorithm is reduced and the security is kept high. Earlier improvement was made by adding a random number to the original algorithm because of which security was increased. But time complexity was still high.


The ElGamal cryptosystem was first described by Taher Elgamal in 1985 and is closely related to the Diffie-Hellman key exchange. The Diffie-Hellman key exchange provides a method of sharing a secret key between Alice and Bob, but does not allow Alice and Bob to otherwise communicate securely. Cryptographically secure digital signature schemes are formed of two parts, the signing protocol and the authentication process.


Implementation Details : 
The signing protocol for an ElGamal signature is as follows. Suppose Alice wants to sign a message, m.
The initial setup is the same as that for ElGamal encryption.
Alice chooses a large prime p and a primitive root α.
She then chooses a secret integer z and calculates β ≡ αz (mod p).
The values of p, α and β are made public and z is kept private.
In order to sign the message m Alice follows the steps below:
She selects a secret random integer k such that GCD(k, p – 1) = 1.
She then computes r ≡ αk (mod p).
She then finally computes s ≡ k-1(m – zr) (mod p – 1).
The signed message is the triplet (m, r, s).

The verification process can then be performed by Bob using public information only.
Bob computes v1 ≡ (β^r)*(r^s) (mod p) and v2 ≡ (α^m) (mod p).
The signature is declared valid if and only if v1 ≡ v2 (mod p).
Correctness
The verification procedure works by the following argument. Assume that the signature is valid. As s ≡ k-1(m – zr) (mod p – 1), we have sk ≡ (m – zr) (mod p – 1) and hence m ≡ sk + zr (mod p – 1). Therefore by Fermat’s little theorem, that a congruence mod p – 1 in the exponent yields a congruence mod p overall, we have:
v2 ≡ (α^m) ≡ (α^(sk+zr)) ≡ (α^(sk))(α^(zr)) ≡ (β^r)(r^s) ≡ v1 (mod p)

Problem Statement  :
problem‐based ElGamal public‐key encryption and signature schemes that exhibit strong security features and efficient implementation

Literature Survey and Inference :
ElGamal digital signature is the asymmetric approach ofauthentication mechanism based on discrete logarithmproblem. This technique uses  as the universally knownrandom number that  serves  as  the generator, u as theuniversally known prime number that serves as the modulus,H() as the universally known hash function

Motivation :
The ElGamal signature scheme is known as a signature with appendix: the message is not readily recovered from the signature pair (r, s) and the message m must be included in the verification procedure. This is in contrast to a message recovery scheme wherein the message is easily recoverable from the signature.

Conclusion : 
The private knowledge required to sign a document is solely represented by the integer z and hence this must be kept secret as in the ElGamal signature scheme.
Most signature schemes including ELGamal signature mode do not allow message recovery. Based on ELGamal signature mode, an improved scheme was proposed, which allows message recovery and has better security than the original one.

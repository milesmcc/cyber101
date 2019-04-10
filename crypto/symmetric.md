# Symmetric Cryptography

Now that you know what encryption is, we can now dive into specifics. The oldest encryption algorithms (ciphers) tend to be _symmetric_ &mdash; that is, knowledge of the 'secret key' is required to both _encode_ and _decode_ text. Most of the cryptographic algorithms you've learned about so far are symmetric.

More generally, symmetric cryptography refers to situations in which there is _symmetry of knowledge_ between communicating parties. For example, if Alice wants to communicate with Bob using a symmetric encryption algorithm, both Alice and Bob need to have a _shared key_ ahead of time.

The following readings will introduce you to the fundamentals of symmetric cryptography, as well as several modern symmetric cryptographic algorithms, some of which are in active use on your own computer.

---

### [Symmetric Cryptography](https://www.ibm.com/support/knowledgecenter/en/SSB23S_1.1.0.14/gtps7/s7symm.html) (IBM Documentation)

![Documentation](https://img.shields.io/badge/Type-Documentation-success.svg)
![5m long](https://img.shields.io/badge/Duration-5m-yellow.svg)
![Informational style](https://img.shields.io/badge/Style-Informational-informational.svg)

This brief documentation for z/OS produced by IBM provides a succinct overview of symmetric cryptography. This is a short reading, but it's dense with important information. Make sure you understand it well.

#### Key Questions

* What information is necessary to _encrypt_ some ciphertext?
* What information is necessary to _decrypt_ some ciphertext?
* Where might _symmetry of knowledge_ prove to be difficult?
* What are some built-in benefits of symmetric encryption?

---

### [A Brief Introduction to Symmetric Cryptography](https://wiki.math.ntnu.no/_media/tma4160/2015h/sym.pdf) (NTNU KG)

![Report](https://img.shields.io/badge/Type-Report-success.svg)
![45m long](https://img.shields.io/badge/Duration-45m-yellow.svg)
![Technical style](https://img.shields.io/badge/Style-Technical-informational.svg)

This introductory report provides a background on various different types of symmetric ciphers. While it doesn't get caught in technical details, it doesn't forego them entirely either. Your goal here is to understand the concepts and ciphers at a technical level, so don't skim over the math! (You _can_, however, skim over the block ciphers that involve matrix multiplication.)

#### Key Questions

* What is symmetric cryptography? Why is it called 'symmetric'?
* In a symmetric cryptographic algorithm, is the decryption function the exact inverse of the encryption function? How does this contrast from a hashing algorithm?
* What are several common attacks on symmetric cryptography? (Keep in mind that these attacks aren't necessarily applicable to _only_ symmetric algorithms.)
* What is cryptographic integrity?
* Why are block-based ciphers useful?

---

### [Guess Why We’re Moving to 256-bit AES Keys](https://blog.1password.com/guess-why-were-moving-to-256-bit-aes-keys/) (Jeffrey Goldberg)

![Blog Post](https://img.shields.io/badge/Type-Blog-success.svg)
![15m long](https://img.shields.io/badge/Duration-15m-yellow.svg)
![Informal style](https://img.shields.io/badge/Style-Informal-informational.svg)

This 1Password company blog post by security expert Jeffrey Goldberg explains the company's usage of AES-128 (a modern symmetric cryptographic algorithm), and their decision to move to AES-256. In addition to exploring the nuances of AES in practice, Goldberg also provides useful advice about threat modeling a cryptography stack.

_Note: if you see numbers such as `2128` in the article, these are incorrectly formatted exponentiations (i.e. `2128` is meant to be `2^128`)._

#### Key Questions

* What is AES? How about AES-128? AES-256? What is the difference?
* What is the average number of computations necessary to brute-force a 2^128 bit key?
* Why does the government require top-secret information to be encrypted using AES-256?
* Why did 1Password originally use AES-128? What prompted the move to AES-256 now?
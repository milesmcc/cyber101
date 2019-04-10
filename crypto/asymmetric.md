# Asymmetric Cryptography

Asymmetric cryptography &mdash; also known as _public key cryptography_ &mdash; is among the great marvels of the world. It is as close to magic as humanity can achieve. Asymmetric cryptography is a beautiful thing.

In an asymmetric cryptosystem, there is _asymmetry of knowledge_ between communicating parties. In other words, Alice and Bob don't need to have a shared secret key. If Alice wants to send a message to Bob, she encrypts her message using Bob's _public key_. Then, she sends her message to Bob, who can decrypt it only using his corresponding _private key_. If you're confused, consider [Wikipedia](https://en.wikipedia.org/wiki/Public-key_cryptography)'s explanation:

> Public-key cryptography, or asymmetric cryptography, is a cryptographic system that uses pairs of keys: public keys which may be disseminated widely, and private keys which are known only to the owner. The generation of such keys depends on cryptographic algorithms based on mathematical problems to produce one-way functions. Effective security only requires keeping the private key private; the public key can be openly distributed without compromising security.
>
> In such a system, any person can encrypt a message using the receiver's public key, but that encrypted message can only be decrypted with the receiver's private key.
>
> Robust authentication is also possible. A sender can combine a message with a private key to create a short digital signature on the message. Anyone with the corresponding public key can combine a message, a putative digital signature on it, and the known public key to verify whether the signature was valid, i.e. made by the owner of the corresponding private key. (Wikipedia, "Public-key cryptography")

The following readings will introduce you to the fundamentals of asymmetric cryptography, as well as several modern asymmetric cryptographic algorithms. Get used to the idea of public and private keys; it is a foundational element of nearly every "secure" system you'll encounter.

---

### [Public Key Cryptography](https://www.bbc.co.uk/programmes/p04vqrwy) (BBC World Service)

![Podcast](https://img.shields.io/badge/Type-Podcast-success.svg)
![9m long](https://img.shields.io/badge/Duration-9m-yellow.svg)
![Informational style](https://img.shields.io/badge/Style-Informational-informational.svg)

This BBC World Service podcast episode (from "50 Things That Made the Modern Economy") introduces asymmetric cryptography and the asymmetric RSA algorithm. Not only does the episode explain how RSA works in the abstract, it also explains the historical and political context that saw its creation.

#### Key Questions

* Why was the development of public-key cryptography almost kept secret?
* Why might asymmetric encryption sometimes be more useful than symmetric encryption?
* How does cryptography intersect with the law? Why did the episode mention "nuclear secrets"?
* What might be the biggest threat to RSA in the future?

---

### [Understanding RSA Cryptosystem](https://medium.com/crypto-0-nite/understanding-rsa-cryptosystem-5e82af321cff) (Belavadi Prahalad)

![Article](https://img.shields.io/badge/Type-Article-success.svg)
![15m long](https://img.shields.io/badge/Duration-15m-yellow.svg)
![Technical style](https://img.shields.io/badge/Style-Technical-informational.svg)

This short article explains the math behind RSA, an extremely common asymmetric cryptography algorithm that provides both confidentiality and integrity when used correctly. RSA forms the basis of common security tools such as PGP and SSH.

#### Key Questions

* What are `p` and `q`?
* What is `n` in relation to `p` and `q`?
* What is `e`? (Read until the end of the article before answering this one.)
* What is `d`?
* Which of these values makes up the _public key_? Which make up the _private key_?
* From where does RSA derive its strength? In other words, why isn't it simple to calculate the corresponding private given some public key?

---

### [Public-Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) (Wikipedia)

![Wikipedia Article](https://img.shields.io/badge/Type-Wikipedia-success.svg)
![30m long](https://img.shields.io/badge/Duration-30m-yellow.svg)
![Informational style](https://img.shields.io/badge/Style-Informational-informational.svg)

A critical element of effective cybersecurity is having _domain knowledge_ &mdash; that is, having a wide store of information that you might not necessarily be an expert on, but that you know about and factor into your thought process. In the case of cryptography, maintaining proper domain knowledge is _critical_ for security: knowing the weaknesses of a given cryptosystem can be the difference between a secure system or a vulnerable one.

To build your domain knowledge around public-key cryptography, read this Wikipedia article. Hover over the links to topics you don't know and read the brief descriptions that pop up. Your goal here is not to know every detail in the field of asymmetric encryption. Instead, it's to get a thorough idea of what is going on.

#### Key Questions

* When was asymmetric encryption developed?
* What are common vulnerabilities in asymmetric cryptosystems? Are all these vulnerabilities inherent to the algorithms, or do some arise in the ways the algorithms have been put into practice?
* What are common asymmetric cryptographic algorithms?
# Tools of the Trade

While inherently valuable, the cryptographic algorithms discussed up until now have little utility to the average computer user. In this section, you'll learn about the "tools of the trade" — that is, the real-world tools that make encryption accessible to the average person. Some of these tools are so widely used that people may not even realize they are using them at all.

This section will ignore topics such as HTTPS, filesystem encryption, TLS, and other similar systems. (Don't worry, we'll address those topics later, once we've built up the appropriate background knowledge.) Instead, we're going to explore "user-space tools" such as PGP ("Pretty Good Privacy") and Signal.

---

### [How PGP Works](https://users.ece.cmu.edu/~adrian/630-f04/PGP-intro.html#p8) (Adrian Perrig)

![Guide](https://img.shields.io/badge/Type-Guide-success.svg)
![1h long](https://img.shields.io/badge/Duration-1h-yellow.svg)
![Technical style](https://img.shields.io/badge/Style-Technical-informational.svg)

This long-form guide will introduce you again to public-key cryptography before diving into the specifics of PGP, an extremely common system for email and file encryption built primarily on RSA. The link above will take you to the beginning of relevant portion of the page; you will benefit greatly if you read from this point until the end. (No need to read the beginning. It's just a rehash of the Caesar Cipher.)

#### Key Questions

* What is PGP? How is it fundamentally different from RSA?
* What about PGP makes it a _hybrid cryptosystem_?
* What is a digital signature?
* What is a digital certificate?
* What is a PGP certificate? What is an X.509 certificate?
* What is _public key infrastructure_? How does it work?
* What is the _web of trust_?

---

### [15 Reasons Not to Start Using PGP](https://secushare.org/PGP) (SecuShare)

![Article](https://img.shields.io/badge/Type-Article-success.svg)
![20m long](https://img.shields.io/badge/Duration-20m-yellow.svg)
![Technical style](https://img.shields.io/badge/Style-Technical-informational.svg)

This short list-article explains why you _should not_ start using PGP. It is decently technical, and likely references a lot of technology that is foreign to you. When the article mentions something you are unfamiliar with, pause and look it up.

?> If you have a spare moment, consider also reading ["We're calling it: PGP is dead"](https://www.wired.co.uk/article/efail-pgp-vulnerability-outlook-thunderbird-smime) by WIRED.

#### Key Questions

* To you, what are the three main reasons why you wouldn't use PGP?
* How does PGP kill anonymity? What 'metadata' does it make available?
* What is a downgrade attack?

---

### [Demystifying the Signal Protocol for End-to-End Encryption](https://medium.com/@justinomora/demystifying-the-signal-protocol-for-end-to-end-encryption-e2ee-ad6a567e6cb4) (Justino Mora, Janelle Wong, and Ksenia Kozhukhovskaya, 2017)

![Blog Post](https://img.shields.io/badge/Type-Blog-success.svg)
![15m long](https://img.shields.io/badge/Duration-15m-yellow.svg)
![Informational style](https://img.shields.io/badge/Style-Informational-informational.svg)

The _Signal Protocol_ is the cryptosystem behind the popular encrypted messaging app [Signal](https://signal.org). It is much more modern than PGP, and has been even incorporated into mainstream messaging apps such as WhatsApp and Messenger. This brief Medium article will give you a sense of how its cryptography works at an abstract level.

#### Key Questions

* What are the advantages of the Signal Protocol over PGP?
* Where is the Signal Protocol designed for use?
* Which "cryptographic primitives" does Signal use?
* What is forward secrecy?
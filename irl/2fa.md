# Two-Factor Authentication

Two-Factor Authentication (and, more broadly, _multi-factor authentication_) is an authentication system in which users must go through two or more steps to prove their identity. For example, in addition to entering a passphrase, users must also enter a code that was sent to their phone via SMS.

!> **Phones aren't secure.** As you'll learn in the following readings, sending a login to a phone is [not a secure way](https://www.twilio.com/learn/account-security/why-using-sms-in-the-authentication-chain-is-risky) to verify a user's identity. Phones are notoriously insecure.

---

### [What Is Two-Factor Authentication (2FA)?](https://authy.com/what-is-2fa/) (Authy)

![Blog](https://img.shields.io/badge/Type-Blog-success.svg)
![10m long](https://img.shields.io/badge/Duration-10m-yellow.svg)
![Informational style](https://img.shields.io/badge/Style-Informational-informational.svg)

In this blog post, Authy, a company that provides a 2FA service for companies, describes the history of authentication and why passwords simply aren't sufficient anymore. It describes the various authentication philosophies and methods for security.

### Key Questions

* What are the three general ways that authentication can verify who you are?
* What are the primary methods of secondary authentication?

---

### [Implementing Google's Two-Step Authentication to Your App](https://www.codementor.io/slavko/google-two-step-authentication-otp-generation-du1082vho) (Vyacheslav)

![Guide](https://img.shields.io/badge/Type-Guide-success.svg)
![20m long](https://img.shields.io/badge/Duration-20m-yellow.svg)
![Technical style](https://img.shields.io/badge/Style-Technical-informational.svg)

This Codementor article explains how OTP, a common 2FA system provided most notably by the Google Authenticator app, can be implemented in your own application. While you don't need to follow along with the guide in your own application, you should use these steps to inform your own understanding of OTP.

?> **OTP is nothing special.** If you want to learn about OTP works at an even deeper level, you can read the [official specification](https://tools.ietf.org/html/rfc6238) as published by the IETF.

#### Key Questions

* What does the typical OTP secret key look like?
* How is OTP related to public-key cryptography?
* From where does OTP derive its "cryptographic strength"? In other words, what makes it difficult to attack?
* What are potential weak points in an OTP system?

---

### [The SIM Hijackers](https://www.vice.com/en_us/article/vbqax3/hackers-sim-swapping-steal-phone-numbers-instagram-bitcoin) (VICE/Motherboard)

![Article](https://img.shields.io/badge/Type-Article-success.svg)
![30m long](https://img.shields.io/badge/Duration-10m-yellow.svg)
![Story style](https://img.shields.io/badge/Style-Story-informational.svg)

!> **This article contains potentially troubling material,** including threats of sexual assault and murder. If you do not feel comfortable reading this type of content, skip this reading.

This article describes the shady underworld of SIM hijackers, who use people's phones to uproot their online world&mdash;often only in the pursuit of an attractive online username.

#### Key Questions

* What are common methods of attack for SIM hijackers?
* How would you go about protecting yourself from the kinds of attacks described in the article?
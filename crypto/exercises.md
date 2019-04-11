# Exercises

?> **Stuck?** If you are having trouble completing any of these exercises, remember to consult Google. You're not meant to work in a silo. If you don't know something, look it up. Don't feel confined to the units' readings either. (Just be sure to keep academic honesty policies in mind when submitting work.)

---

### Hello, Crypto!

![Code Experiment](https://img.shields.io/badge/Type-Code%20Experiment-success.svg)
![2h long](https://img.shields.io/badge/Duration-2h-yellow.svg)
![Primary skill is modeling](https://img.shields.io/badge/Primary%20Skill-Following%20the%20Spec-informational.svg)

Now that you've read about all sorts of cryptosystems, why not try to implement them yourself? While any [Turing-complete](https://en.wikipedia.org/wiki/Turing_completeness) programming language could work, you should probably use Python for this task.

!> **Never _actually_ implement your own crypto.** This is an exercise for learning purposes. When designing real-world systems, don't implement cryptographic algorithms yourself. Use well-known libraries like [LibreSSL](https://www.libressl.org/) or [BouncyCastle](https://www.bouncycastle.org/) instead.

1. **Implement a Caesar cipher.** Write two functions `encrypt(shift, text)` and `decrypt(shift, text)` that correspondingly encrypt and decrypt `text` using `shift`.
2. **Implement RSA.** Okay, you won't _really_ be implementing RSA. But you'll be implementing RSA for very small numbers! Write three functions `generate()`, `encrypt(publickey, number)`, and `decrypt(privatekey, number)`. `generate()` returns a tuple of `(publickey, privatekey)` (the actual structure of these objects is up to you, but will _probably_ be dictionaries). Then, write the two functions `encrypt(publickey, number)` and `decrypt(privatekey, number)` that encrypt and decrypt some `number` using `publickey` and `privatekey`, respectively. (Optional challenge: turn your implementation into a block-based cipher that can encrypt not only numbers, but text!)

---

### Getting Started with PGP

![Group Learning](https://img.shields.io/badge/Type-Group%20Learning-success.svg)
![20m long](https://img.shields.io/badge/Duration-20m-yellow.svg)
![Primary skill is using PGP](https://img.shields.io/badge/Primary%20Skill-Using%20PGP-informational.svg)

?> **This is a group exercise.** It is best completed in class. It is designed for 1 partner. (Students should pair off with one other student.)

In this exercise, you'll use PGP to send an encrypted email and verify the integrity of a cleartext document.

1. If you don't already have a PGP key, create one! You should probably use a tool like [GPG](https://www.gnupg.org/). Make sure you tie your key to your school email, as you don't want to accidentally litter a keyserver with a key for your personal account.

2. Share your public key with your partner. The public key should be a block of text starting with `-----BEGIN PGP PUBLIC KEY BLOCK-----`. It's probably easiest to just email your public keys to one another in plaintext. (It's probably not worth uploading your key to a keyserver.) Be sure to import your partner's public key into your internal keystore, if necessary.

3. Send an encrypted email to your partner! The contents can be anything you'd like, but use your judgement. The encryption might be able to keep out major governments, but nothing can stop your teacher from looking at your partner's screen!

?> **Do it the old-fashioned way!** For the sake of the exercise, don't just use a built-in PGP client for your email software. To send this encrypted email, write up the plaintext in a text document (`.txt`) and manually encrypt it. (For the folks using GPG, the command to do this is something like `gpg --output encrypted.txt --encrypt --recipient your_partner@andover.edu --armor plaintext.txt`.) Then, paste the encrypted PGP message into your email software and send it to your partner. Be sure to use the `--armor` option, as that way it will create an ASCII-encoded output, as opposed to raw data.

4. Try to decrypt the message you received from your partner. It may take a few tries. See if you can figure it out on your own (and using Google). If you're _really_ stuck, ask your instructor for help.

5. Send a _signed cleartext message_ to your partner, and have them verify the authenticity of the message. Try changing something in the text and _then_ performing the integrity check passes. (It shouldn't.)

---

### Design Your Own Crypto

![Learning Experiment](https://img.shields.io/badge/Type-Learning%20Experiment-success.svg)
![2h long](https://img.shields.io/badge/Duration-2h-yellow.svg)
![Primary skill cryptography engineering](https://img.shields.io/badge/Primary%20Skill-Cryptographic%20Engineering-informational.svg)

In this exercise, your task is simple: design your own symmetric cryptographic algorithm! There are no strict requirements, but your algorithm _should_ provide some degree of confidentiality and integrity. Your algorithm need not necessarily be advanced; in fact, it will almost certainly _not_ be advanced. Nonetheless, you should devote some serious thinking about 

Once you design and implement your own cryptographic algorithm, respond to the following questions:

1. How does your algorithm perform encryption? How does it perform decryption? Are there any limitations on the type of content it can encrypt? (Is it block-based?)
2. Is your algorithm symmetric or asymmetric? What makes it "hard to break," if it's even hard to break at all?
3. Imagine someone used your algorithm to encrypt a top-secret message, and the government now desperately needs you to decrypt it. Where would you begin? What kind of vulnerabilities would you try to exploit?

---

### De-Anonymize Me

![Real Task](https://img.shields.io/badge/Type-Real%20Task-success.svg)
![45m long](https://img.shields.io/badge/Duration-45m-yellow.svg)
![Primary skill sleuthing](https://img.shields.io/badge/Primary%20Skill-Sleuthing-informational.svg)

Below, you'll see the content of an encrypted email. Using your knowledge of PGP and its ecosystem, answer the following questions:

1. Who sent the email? How do you know?
2. When did they send the email?
3. To whom was the email sent? How do you know?

```
-----BEGIN PGP MESSAGE-----

hQIMA3iy7rZdXxNWAQ/+M6bWfiBRrcnrDkP6waTz0WTBFsLGgXQb/gAURejGu2t2
UF934QfsN/jLgX6medDi9s+YB4z+cAppqSHskNujOVOB8ViaSbKrsuIh6lNHPj/f
c0s0PZknlUzIloUh9+AjVT9gtKJIXLOSr1sHBe/f+SfYCk8le0QHXEjUh4xHe+g3
19WtVVmGbx0razxS/4p2TIhvDIPM8NG+GRZhSHlWltXXC2XUmPY3okG4H5YzWK7r
AI5yfmpj9Rqv3GkliNLVle67AoNnr0/pAOFEzMkZyZEcJiYPZJ0YZpogdnwohojI
DQ8yR/xMsjCjuok87Z5Zq0Lj1UBsJIHGl/kX/3mZ9jxe8iihT8jk0IzUZsAothAh
6GZ7MZV97hGAK0Fch7KMDG8iMx4GI7hqQ9mXmOOGIltioGadF3cJ5Tk6ZYtRsdzK
ga/Y67HrZCcILFtqxAbMqL8suzrAljw72EExzSwfgOKmwjb8shtY1x4Ug+nV7AVR
m/bbk3xCNjRkKhf2Annpa0ltZI7V/9HTCyyFEDjnP5BrCc3CRloXiJfxXu9ULm67
lK37ow5LBJyHtVc7AHV4aGHHza0hvwqkppRPO3n7YiC7jaHB0fgACQU2dgsvbRCP
TQSq/F0zphdv+3Anm9Fvv3rzUeqB/EatCRtL+y0ocxjcwHRO9+PZ6PoDXBuvD0nS
wBABqyAxLaLI/pzfe3aUCPoJCxDIVjc9QcMG8x5VL9Scadcbf5yTWx6cg8QmESgR
du6sYnlJaC6w3WvuLtoYPpeIPxpec46oUxUbjCbTS348ycj56rOVWUIlCYicf6Vt
m56fVTZElrOxNEpJry+9C+qbIOVFQ2IEvDZ6jgv16fAYrE4XamkyJ+/9i3Qvylcp
tPaSzjkd/YDj07joQF5lE9N4jlDukDpYUe1DhJq918eOjHxEQQEFbP9oo3Xy+ZN3
PkSd8mYapp1GSwDtDaHUU8oZ
=+sIu
-----END PGP MESSAGE-----
```
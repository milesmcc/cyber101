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

?> **Do it the old-fashioned way!** For the sake of the exercise, don't just use a built-in PGP client for your email software. To send this encrypted email, write up the plaintext in a text document (`.txt`) and manually encrypt it. (For the folks using GPG, the command to do this is something like
 `gpg --encrypt --armor`.) Then, paste the encrypted PGP message into your email software and send it to your partner. Be sure to use the `--armor` option, as that way it will create an ASCII-encoded output, as opposed to raw data.

4. Try to decrypt the message you received from your partner. It may take a few tries. See if you can figure it out on your own (and using Google). If you're _really_ stuck, ask your instructor for help.

5. Send a _signed cleartext message_ to your partner, and have them verify the authenticity of the message. Try changing something in the text and _then_ performing the integrity check passes. (It shouldn't.)

---

### Design Your Own Crypto

![Learning Experiment](https://img.shields.io/badge/Type-Learning%20Experiment-success.svg)
![2h long](https://img.shields.io/badge/Duration-2h-yellow.svg)
![Primary skill cryptography engineering](https://img.shields.io/badge/Primary%20Skill-Cryptographic%20Engineering-informational.svg)

In this exercise, your task is simple: design your own symmetric cryptographic algorithm! There are no strict requirements, but your algorithm _should_ provide some degree of confidentiality and integrity. Your algorithm need not necessarily be advanced; in fact, it will almost certainly _not_ be advanced.

[add example]

Once you design and implement your own cryptographic algorithm, respond to the following questions:

1. How does your algorithm perform encryption? How does it perform decryption? Are there any limitations on the type of content it can encrypt? (Is it block-based?)
2. Is your algorithm symmetric or asymmetric? What makes it "hard to break," if it's even hard to break at all?
3. Imagine someone used your algorithm to encrypt a top-secret message, and the government now desperately needs you to decrypt it. Where would you begin? What kind of vulnerabilities would you try to exploit?

---

### De-Anonymize Me

![Real Task](https://img.shields.io/badge/Type-Real%20Task-success.svg)
![45m long](https://img.shields.io/badge/Duration-45m-yellow.svg)
![Primary skill sleuthing](https://img.shields.io/badge/Primary%20Skill-Sleuthing-informational.svg)

Below, you'll see the content of an encrypted email. Using your knowledge of PGP and its ecosystem, figure out who the following message was sent to. (Note: there may be two possible recipients.)

?> **You won't be able to read the message's contents.** Breaking PGP is not necessary to completing the assignment.

```
-----BEGIN PGP MESSAGE-----

hQIMA3iy7rZdXxNWARAAw0ukkWqCIt7lMacwkyIXFp5oEjZjzalBrRU06ZjApOEb
1OZ+LbHQvQJNbnQpgtnaQ7e20yh+OO9qUmyxpzTMgTZfpLi0m8kLhT80jrSrBBFx
w2RZNxSZu7Si8WPjZZsbLgQ1Uaj8KH2S+aFPASeRlvFkHK5+S58pbpZybii/sGAN
022H+cTwZliOcTonY07G/Y/u4Mx5GXFU/wvSh0renPxU7TIkwyWGM1Eug4FRa8Hc
0r8U+xSY/7jRGD0oIZdspTwQRzYriM9Pct8DgQu7LjDYf6yxOTFBx3Ck483piDFk
bfE3nPh3lheApBfVDif9+5OeS8y1C9i6txGzON2KMMYLXFrD/z8KuSSxXCFgNpE3
tAdkpNI7aolK8gHDojmvS5IbVBJSvQmMnI4l9tOpyclRVqjsoJjNIqM9/DueGsRo
rwrABfvemYiSsiW5xya4skxDtQ46KqFiFQQmxHumX8+XFSOAlzO9q9TGIs1i1cQy
UsvFjjvopRl5DArArPda6qaDLff/wI/8co3F3jNXhPF35Dxda5FtgXupcFwn1hdP
N7MuyowCswxLHfiEFqY9O9/+5zxLwJgOthhTUEINx3DwT7Wbzq4Utr0s/g3OtvzN
Q8dihKLEq6k6XkM1t0a+yHcXMtBNS0oRbUC2CCgjuHF31rSBW/5FPCXL5ev4LJbS
6QH2XgkOUgrnsfxWSoMSqvvuoffADyqb3JA2qEoIQGBtihmqrnLvsq+Wb3VnBT/v
5iBEdbLJN6QP2XWKx3DEipssVZsOmG/gA8Fg3U1DQ6St2ERR6TzOcCZ2cU3ctv9d
IydZ3qsCs0XBWT7C+G/TzVAgz1Dvd7BNGfyfCzFrSCDZg/1xkViikyo4N23IHoRQ
JLTQ7NQMDBgreKy8O+8uzhkbp8DnuLggoQxPrQZNkuwmjydtHcetXnO7ppBLegEw
L05a2uc0/LqI5fa4NxDIiWV59agX8a0zsOVqxS9pPNQzX4NmuNApl/gFBOWCYFTm
0zLWae2vQi3kaUXDgAwoTYGDdJgHtuexzVsj7OXVAWpeexKeAxSqaqevkt5jOSGM
E9xrYABQ9lJZqkdxmiWVEg/0FnC9D9ZtLdtPXH7/P+LPwXUWp8XXxOLQCF6Ts8tN
kZHMR3n4EogmGbCJUV3pUlWof9E68sTpW9oJxQ/fpss4IKVHx9V/qwNGWGR8mWUg
mlsZ+fjBZtzL3QXw4DsjWHWave9fxYgLKRlQfbSoB+SfC7eoUfRKiGYLH+kv6OjU
8gpBxbxUHKAD2XVXTPMaiJbYU95Zw/JyAyR+j9K82yc6DS8JlkYy09+llEtg8VDH
ZkHL7E4ObNy1fw7sxfKA4b+6D4c9OjDyiXq8ZKo4K9E2wHr8Fe56pbwIreJg0n43
MGAqKJJtW4K3YZMagtUQVeTAl+P3HmNvplJAMyfcLiDZ/L0Vg1caHsujUHD6E63C
oJeZC/XKKuc43Y1z+tgjToSRWZmsAVnyfMIfuUT+VdXUWlDn2d5G8xvOTb4tOqco
lPOHvmLbqki5CziPhc+msNPLi6kI3kbdmjnArLj7v2YjNdNwyxYUKAP6ZzM08kvq
zSYgauX7q6uZCu1f8QuYhwosYRq2nVK8aslrUDerdLPbw1JhOEZB/F76/rx0WVRq
Hccz9wfRLmoHw56rMzfOk40ffH1T8vvk+bF58BvoWJUSWrFVq3j7bGEL6lohlf/o
yJwtweJveHLw7TXtLrzEZSMqdj/r0Raly43c1cjNupcvpWZzbaaztRlL9z4E6gD8
zax/lgnnaqUduAFzKw==
=Jy5J
-----END PGP MESSAGE-----
```

[add attack exercises; what would you do if I didn't tell you which cipher I used?]
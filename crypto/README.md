# Unit 1: Cryptography

![4 topics](https://img.shields.io/badge/Topics-4-success.svg)
![13 readings](https://img.shields.io/badge/Readings-12-yellow.svg)
![5 exercises](https://img.shields.io/badge/Exercises-5-informational.svg)

Here's a common cryptography puzzle. Imagine you'd like to send a box to Alice, and you also want to make sure that no one except Alice can open the box. You don't trust anyone else &mdash; not even the Postal Service. Unfortunately, the only way you can send anything to Alice (including information) is by using the Postal Service. Assuming that you trust the locks on your safe and the safe itself, is there any way that you can send Alice the box securely without any prior coordination and still allowing her to open it herself?

The answer is _yes_. Here's how it's done:

1. You lock the safe with your own lock, and send it to Alice.
2. Alice puts her own lock on the safe, and sends it back to you. Now, the safe has two locks on it.
3. You take off your lock, and send it back to Alice with only her lock on the safe.
4. Alice takes her lock off the safe and is able to access the contents.

?> **Get accustomed to reading about Alice, Bob, and Eve.** In discussions of cryptography, Alice and Bob are often used to refer to two people trying to communicate securely, while Eve refers to an *eaves*dropper. You'll see these names again.

This is a common introductory analogy for cryptography. To be sure, it isn't perfect: real world cryptography involves lots of math and doesn't involve safes. But the general goal is the same: how can one transmit information from one place to another, guaranteeing both _confidentiality_ and _integrity_, whilst also not trusting the messenger?

This unit is meant to provide an introduction to cryptography topics such as encryption and signatures, as well as to common "cryptography tools" such as PGP, OTR, and Signal.

### Unit Questions

By the end of this unit, you should be able to confidently answer the following questions:

* What is encryption? What is hashing? What is the difference?
* What is a digital signature? Where are digital signatures useful?
* What is symmetric encryption? What is asymmetric encryption?
* What is a key? What is a public key? What is a private key?
* What is PGP? What is OTR? What is Signal? What's the difference?
* What is a brute-force attack? What is a known-ciphertext attack? What are other common attacks on encryption?
# Exercises

---

### 2FA, Your Way

![Design Challenge](https://img.shields.io/badge/Type-Design%20Challenge-success.svg)
![1h long](https://img.shields.io/badge/Duration-45m-yellow.svg)
![Primary skill is algorithm design](https://img.shields.io/badge/Primary%20Skill-Algorithm%20Design-informational.svg)

You know all about One Time Pad (OTP), the algorithm that generates the six-digit codes often used for two-factor authentication. You know that the codes change every thirty seconds, and that there's no way to identify the original "private key" from which the codes are generated from the codes themselves.

In this exercise, your challenge is to build your own OTP-style algorithm. Starting with seed data, your algorithm should produce `n`-digit codes (length is up to you) that rotate every `s` seconds. (Both the length of the codes and the frequency at which they rotate is up to you.)

Your system should have the following properties:

* Given any number of codes (and the times at which they were created), it should not be possible (or, more realistically, it should be _exceptionally hard_) to recover the original key.
* The codes should be relatively difficult to guess and evenly distributed across the output space (that is, `0 <= c <= 10^n` where `n` is the length of your codes and `c` is any given code). A poor algorithm would increment the code by 1 every thirty seconds, while a strong algorithm would "jump around" in the output space.

Implement your OTP algorithm in Python, then write a brief explanation describing 1) how your algorithm works, 2) from where it derives its "security," and 3) how one might try to break or exploit it.

---

### Shell-Based Auth

![Lab](https://img.shields.io/badge/Type-Lab-success.svg)
![2h long](https://img.shields.io/badge/Duration-45m-yellow.svg)
![Primary skill is system design](https://img.shields.io/badge/Primary%20Skill-System%20Design-informational.svg)

In this exercise, you will build a Python program that has user management! The Python program is a simple prefix-based calculator. For example, entering `+ 5 5` should output `10`, while `- 5 3` should output `2`. Your calculator should support the operators `+ - * / ^`.

What makes this calculator special is that users need to authenticate themselves to use it. When they first launch the program, they will be asked for a username and password pair that you will check against a database of usernames and (hashed!) passwords in your program.

?> **For the purposes of this exercise, assume that the user cannot just modify your program to disable authentication.** Pretend that the program is running remotely on a server, for example.

Each user should have its associated _permissions_&mdash;in other words, the operations (`+ - * / ^`) that they are allowed to use.

A successful submission will:

* Use proper password management techniques (and yes, you _may_ use a library to do this; in fact, you're encouraged to)
* Actually work (the calculator shouldn't break, and the authentication should only work with a valid username and password)
* Have clean and organized code (the easier your code is to understand, the less likely there is to be a security vulnerability lurking somewhere)

Authentication information may be hard-coded into your program, as may authorization information (permissions).

---

### Security Audit

![Project](https://img.shields.io/badge/Type-Project-success.svg)
![1h long](https://img.shields.io/badge/Duration-1h-yellow.svg)
![Primary skill is security auditing](https://img.shields.io/badge/Primary%20Skill-Security%20Auditing-informational.svg)

In this project, you will pair up with another member of the class and perform a _security audit_ on either their "OTP"-style algorithm (from the first exercise of this subunit) or their auth-calculator (from the second exercise).

While your ultimate goal is to annotate your partner's code and identify any security vulnerabilities, there are a few things you need to do beforehand. For example, you need to figure out what your partner's threat model is. (An attacker exploiting a CPU zero-day vulnerability to break into the calculator auth system because the database was in the wrong memory register, for example, is likely not a practical concern.)

The "deliverable" for this assignment is an annotated copy of your partner's code (which points out any potential attack surfaces and outlines the general logic of their program) and a small report (no more than 300 words) that explains whether or not you think the program is sufficiently secure in the context of your partner's threat model.
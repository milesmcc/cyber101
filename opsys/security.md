# Security Mechanisms

Because operating systems provide the environment in which nearly all programs run, it's important that they remain secure. Operating systems maintain security in a few different ways, as we'll explore in the readings below. First, though, let's establish _what_ operating systems need to prevent against:

* Users accessing other users' files (without permission)
* Programs accessing other programs' memory (without permission)
* External programs accessing the computer's memory or storage (without permission)
* Programs taking unauthorized control over the system (malware)

Of course, this isn't an exhaustive list. But these are some of the more fundamental security needs of an operating system; you'll want to keep them in mind as you learn about how operating systems work. It may help reveal _why_ they are designed that way.

---

### [Techniques for Securing the Operating System](https://www.ibm.com/support/knowledgecenter/en/SSEP7J_10.2.1/com.ibm.swg.ba.cognos.crn_arch.10.2.1.doc/c_securing_the_operating_system.html) (IBM Documentation)

![Documentation](https://img.shields.io/badge/Type-Documentation-success.svg)
![15m long](https://img.shields.io/badge/Duration-15m-yellow.svg)
![Technical style](https://img.shields.io/badge/Style-Technical-informational.svg)

This article from the IBM Documentation provides an overview of how to secure a UNIX-based operating system. While it doesn't explore how the security features work on a technical level, it does provide a good survey of what security features an end user (or system administrator) would interact with.

### Key Questions

* What are users? What are administrators?
* What is an account policy?
* Where are (hashed!) passwords stored on UNIX-based operating systems?
* What is patching?

---

### [Linux Permissions](http://linuxcommand.org/lc3_lts0090.php) (William Shotts)

![Guide](https://img.shields.io/badge/Type-Guide-success.svg)
![20m long](https://img.shields.io/badge/Duration-20m-yellow.svg)
![Technical style](https://img.shields.io/badge/Style-Technical-informational.svg)

Permissions are a key concept on UNIX-like operating systems, and are in many ways analogous to Windows as well. (Mac OS X is a UNIX-like operating system.) This guide explains how permissions work on Linux, and why they are critical to maintaining system integrity.

#### Key Questions

* What are the three main types of permissions?
* What does the permission `rw-r--r--` indicate?
* What is the _superuser_?

---

### [An Introduction to Qubes OS](https://www.qubes-os.org/intro/) (Qubes OS Team)

![Guide](https://img.shields.io/badge/Type-Guide-success.svg)
![10m long](https://img.shields.io/badge/Duration-10m-yellow.svg)
![Informational style](https://img.shields.io/badge/Style-Informational-informational.svg)

Qubes OS is a highly secure operating system that uses virtualization to maintain its integrity. Read through this guide and look up any concepts you don't understand online. You don't need to know the ins and outs of Qubes specifically, but think what its features suggest of vulnerabilities in other operating systems.

#### Key Questions

* What is Qubes OS?
* Why is Qubes OS "reasonably secure"?
* Who is Qubes OS designed for? Would you ever use it?
* What kind of security mechanisms does Qubes OS employ _on top_ of traditional operating system security techniques?
# Filesystems

As with most high-level operating concepts, you probably have a good idea of what a file is. It's just a piece of persistent data that you interact with using some kind of program (such as a text editor or MP3 player).

In this unit, you'll learn about the internals of filesystems — how they work, why they work, and where they work.

- intro
- extv4, ntfs, etc
- paths
- dotfiles
- encryption

---

### [Introduction to File Systems](http://www.eecs.harvard.edu/~cs161/notes/intro-file-systems.pdf) (Crash Course)

![Presentation](https://img.shields.io/badge/Type-Presentation-success.svg)
![15m long](https://img.shields.io/badge/Duration-16m-yellow.svg)
![Informational style](https://img.shields.io/badge/Style-Informational-informational.svg)

This presentation from CS161 at Harvard will introduce you to the key concepts of filesystems. Don't worry too much about the code excerpts; what matters is that you understand the key ideas. (But for a better understanding of how filesystems work at a low level, the included code snippets are a good resource!)

### Key Questions

* Why are filesystems useful?
* How is a filesystem an 'abstraction'?
* How did filesystems work in the 60's? What is fragmentation?
* What is a 'sector'?
* What is a symbolic link?

---

### [Path (computing)](https://en.wikipedia.org/wiki/Path_(computing)) (Wikipedia)

![Article](https://img.shields.io/badge/Type-Article-success.svg)
![15m long](https://img.shields.io/badge/Duration-30m-yellow.svg)
![Technical style](https://img.shields.io/badge/Style-Technical-informational.svg)

This Wikipedia explains what a "path" is on nearly all different operating systems. If you frequently work on the command line, the article's contents should be familiar. If not, it may seem foreign. Either way, read this article closely — many of the most significant operating systems deal with filesystems and, more specifically, the way _paths_ are handled.

?> **Beware of hidden files.** Though not covered in this article, you should also be familiar with the concept of a [hidden file](https://en.wikipedia.org/wiki/Hidden_file_and_hidden_directory). (Just skim the Wikipedia article and you'll know everything you need to know.)

#### Key Questions

* What is a path?
* What do `.`, `..`, and `~` signify?
* What are common directory signifiers?
* What is a drive letter? Which operating systems have drive letters?

---

### [Encrypt Your Data](http://www.admin-magazine.com/Articles/Filesystem-Encryption) (Jeff Layton)

![Article](https://img.shields.io/badge/Type-Article-success.svg)
![10m long](https://img.shields.io/badge/Duration-10m-yellow.svg)
![Informational style](https://img.shields.io/badge/Style-Informational-informational.svg)

This article in ADMIN magazine explains how you can encrypt a filesystem (and why you should). Armed with your knowledge from the cryptography unit, you should be able to understand almost every idea in the article. (Don't worry too much about the code/shell commands on the second page, though.)

#### Key Questions

* What does filesystem encryption look like in practice?
* Why should you encrypt a file system? Where might it fit into a threat model?
* What is a common cryptographic algorithm for filesystem encryption?
* What is hardware encryption? What is software encryption?
* Is it possible to only encrypt one part of a filesystem?
# Exercises

!> **Be careful!** When working with malware, it's important that you don't accidentally infect &mdash; or damage &mdash; your own computer. Never _run_ malware outside of a virtual machine, for example.

---

### Your Father

![Thought Experiment](https://img.shields.io/badge/Type-Thought%20Experiment-success.svg)
![45m long](https://img.shields.io/badge/Duration-45m-yellow.svg)
![Primary skill is modeling](https://img.shields.io/badge/Primary%20Skill-Following%20the%20Spec-informational.svg)

You receive a frantic call from your father. "Alice, I think I might have infected my computer with malware!" he says to you. Your task is to work with your father to control the situation and minimize the impact of the malware on his computer. Note the following:

* Your father's computer has lots of sensitive information on it, such as bank info and tax returns.
* Your father keeps monthly backups, and the last backup was three weeks ago.
* Your father doesn't know _how_ he got the virus, but he's been saying that there's an odd new toolbar in his browser. Moreover, the CPU and network usage will spike to 100% at random, sometimes for hours at a time.
* You have physical access to the computer (hint: you can remove its hard drive).

Given this information, work with your father to help minimize the impact of the malware. This exercise does not involve any coding.

1. What is the first thing you do?
2. What kind of malware does this resemble?
3. Assuming that you cannot be confident that you have _entirely_ eradicated the malware from your father's computer, you instead salvage all the important documents from his hard drive and then wipe the computer entirely. Assuming that you use the same (now wiped) hard disk, is this approach guaranteed to remove the malware? Why or why not?
4. What next steps do you give your father to secure his life (both online and offline)? 

---

### Server Hardening

![Lab](https://img.shields.io/badge/Type-Lab-success.svg)
![45m long](https://img.shields.io/badge/Duration-45m-yellow.svg)
![Primary skill is system management](https://img.shields.io/badge/Primary%20Skill-System%20Management-informational.svg)

Ubuntu is a popular GNU/Linux-based operating system for servers, phones, laptops, and desktops. In this exercise, you will learn how to navigate and secure an Ubuntu server environment.

?> **Use Google as necessary.** Depending on your prior experience, you may find some of the tasks in this exercise very challenging. If you are unfamiliar with the command line or SSH, research these topics before continuing.

As you work through these tasks, document your work in a text file (that will also be your final submission for this assignment).

1. Set up an Ubuntu VM (virtual machine) on a public cloud such as AWS or Google Cloud Platform. **Both platforms provide a free tier, and you should not be required to input billing details.** Which provider did you choose, and why?
2. Connect to your server using either SSH or a web-based terminal. Were you able to log in? How did you solve your problems in case you weren't originally able?
3. Perform the steps in [this tutorial](https://www.lifewire.com/harden-ubuntu-server-security-4178243) on how to secure an Ubuntu server. Did any steps stick out to you? Do you understand what you did?
4. Run some code&mdash;maybe a Python script that you write yourself&mdash;on your server. What did it do?
5. Try to transfer a large file (maybe an image or something larger than 500KB) from your computer to your server, and from your server to your computer. Were the transfers successful?

---

### Malware? Where?

![Exercise](https://img.shields.io/badge/Type-Exercise-success.svg)
![2h long](https://img.shields.io/badge/Duration-2h-yellow.svg)
![Primary skill is programming](https://img.shields.io/badge/Primary%20Skill-Programming-informational.svg)

In this exercise, you will use your Python skills to develop a piece of "malware." Of course, your software will not do anything malicious&mdash;instead, it will simply create a file somewhere on the host computer called `hello.txt`. Your "malware" should run invisibly to the computer, and should recreate `hello.txt` if it is ever deleted. The file should have the following contents:

```
Hello there. This file was created by "malware" created as a demonstration for a course on cybersecurity. It is not malicious.

To remove this "malware," perform the following steps:

[Here, you would explain how to remove the malware from the host computer.]
```

?> **This will look different on Mac, Linux, and Windows.** Because these operating systems function differently, this assignment will not be completed the same way for all of them.

An example program submitted for this assignment (let's call the program `malware.py`) might function like this:

* When the user runs `malware.py`, the program copies itself to somewhere else on the computer&mdash;for example, to `~/Pictures/organize`. (Note that the `.py` extension was removed; after all, there's no need to keep it!) 
* The program adds `python3 ~/Pictures/organize` to the list of startup commands, so that the program turns on whenever the user logs in.
* The program spawns a 'daemon' process running separate from the calling thread that monitors `hello.txt` (wherever it is) and creates/replaces it as necessary.

For this example malware, the `hello.txt` file would have the following contents:

```
Hello there. This file was created by "malware" created as a demonstration for a course on cybersecurity. It is not malicious.

To remove this "malware," perform the following steps:

1. Delete the file `~/Pictures/organize`
2. Remove 'python3 ~/Pictures/organize` from your startup commands
3. Restart your computer
```
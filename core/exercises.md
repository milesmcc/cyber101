# Exercises

!> **Always be mindful of the law when completing cybersecurity exercises.** You can't go wrong with the exercises below — they do not involve any form of real-world penetration testing — but always keep the law in the back of your mind.

### Unwanted Prank Defense

![Thought Experiment](https://img.shields.io/badge/Type-Thought%20Experiment-success.svg)
![20m long](https://img.shields.io/badge/Duration-20m-yellow.svg)
![Primary skill is modeling](https://img.shields.io/badge/Primary%20Skill-Threat%20Modeling-informational.svg)

Think about your own home, whether it is a dorm room, an apartment, or an entire house. You are trying to defend this home from a friend who is trying to throw a less-than-convenient prank on you. You know that they are determined, but you're _really_ not in the mood for this prank, so you're taking measures to protect yourself.

To complete this exercise, answer the following questions:

1. Who is the threat actor? What is your threat model? (Refer to the EFF guide for more questions to ask.)
2. Identify at least four attack vectors that this determined prankster could potentially exploit — perhaps in tandem with one another — to enter your home.
3. Explore how you could mitigate each of the attack vectors you identified above. Keep in mind that you might not be able to _eliminate_ each one entirely!

---

### Which Hat?

![Thought Experiment](https://img.shields.io/badge/Type-Thought%20Experiment-success.svg)
![30m long](https://img.shields.io/badge/Duration-30m-yellow.svg)
![Primary skill is judgement](https://img.shields.io/badge/Primary%20Skill-Ethics%20and%20Judgement-informational.svg)

In each of the following situations, explore whether you think the person involved acted in line with "white-hat hacking," or if they crossed the line into "black-hat hacking." This prompt is left intentionally broad; after all, there is no clear-cut distinction to be made.

1. Jay, a student at Phillips Academy, is demonstrating how the school email system doesn't authenticate email senders. This vulnerability means that anyone can send emails pretending to be anyone else from the school, and the recipients have no way of knowing whether the email they receive is indeed from the listed sender. He brings this issue to his computer science teacher, who asks him to demonstrate (replicate) the vulnerability. Jay intends to send a fake email from the principal to his teacher, but accidentally puts the principal's email in the recipient field as well. The principal receives an email — from themselves — that reads `this is a demonstration of a spoofed email`. Jay realizes his mistake, but does not follow up with the principle to explain the potentially alarming message.

2. Sarah is playing a competitive multiplayer video game. Realizing that a certain combination of keystrokes triggers a glitch which causes her score to be doubled, she quickly exploits the bug and rises to the top of the leader-board. She does not report the bug to the game's creators, and instead uses it to maintain her #1 status.

3. Elena sees her teacher, Mr. Lane, using a public computer in the computer lab. When Mr. Lane finishes working, Elena realizes that he forgot to log out of his account. With security in mind, she tries to log Mr. Lane out of the computer, but realizes that his login credentials are permanently stored on the computer. Although she tried, she doesn't know how to remove his account from the computer. Because she _really_ needs to finish her paper in time for her next class, she continues working (while Mr. Lane's account is logged in).

4. Alex is tasked with creating a program for his computer science class that connects to the Internet. After submitting his project to his instructor, he realizes that his program has a security hole that could allow anyone to control the computer his code is running on. Nervous, he tries connecting to his teachers' computer, who is running the program on her own computer to grade it. Alex is able to successfully connect. Nervous that his teacher might be mad at him for the oversight and penalize his grade, he keeps quiet and does not tell his teacher anything.
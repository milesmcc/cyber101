# Authentication vs. Authorization

When designing your own applications, you may think of "auth" as a single component—the part that handles _accounts_. While somewhat true, "auth" technically refers to two distinct concepts: _authentication_ and _authorization_.

Authentication is making sure that your application knows who the user is. Authorization is making sure that the user has permission to do what they're trying to do.

For example, many web applications provide admin panels accessible only to users with special privileges. This website must have both authentication and authorization: authentication ensures that the admin user is who they say they are, and authorization ensures that they actually are an _admin_.

If the distinction is still unclear, that's alright. The following readings will help explain the differences between (and importance of) authentication and authorization in practice.

---

### [Authentication versus Authorization](https://stackoverflow.com/questions/6556522/authentication-versus-authorization) (StackOverflow)

![Question](https://img.shields.io/badge/Type-Question-success.svg)
![1m long](https://img.shields.io/badge/Duration-1m-yellow.svg)
![Informational style](https://img.shields.io/badge/Style-Informational-informational.svg)

This StackOverflow question asks what "auth" stands for. The top answer doesn't fail to deliver.

### Key Questions

* What does "auth" stand for?
* What is the difference between authentication and authorization?
* Are both authentication and authorization necessary for security?

---

### [Authentication vs Authorization](https://medium.com/datadriveninvestor/authentication-vs-authorization-716fea914d55) (Anum Siddiqui)

![Article](https://img.shields.io/badge/Type-Article-success.svg)
![5m long](https://img.shields.io/badge/Duration-5m-yellow.svg)
![Technical style](https://img.shields.io/badge/Style-Technical-informational.svg)

This Medium article by Anum Siddiqui goes into greater detail about the differences between authentication and authorization. It also introduces the concepts of two-factor and multi-factor authentication. (These concepts will appear again!)

#### Key Questions

* How is Siddiqui's explanation of authentication versus authorization different/more nuanced than StackOverflow's?
* What is two-factor authentication?
* What is multi-factor authentication?

---

### [Kill the Password: A String of Characters Won't Protect You](https://www.wired.com/2012/11/ff-mat-honan-password-hacker/) (Mat Honan)

![Article](https://img.shields.io/badge/Type-Article-success.svg)
![30m long](https://img.shields.io/badge/Duration-30m-yellow.svg)
![Story style](https://img.shields.io/badge/Style-Story-informational.svg)

This article in ADMIN magazine explains how you can encrypt a filesystem (and why you should). Armed with your knowledge from the cryptography unit, you should be able to understand almost every idea in the article. (Don't worry too much about the code/shell commands on the second page, though.)

#### Key Questions

* Why were passwords appropriate in the pre-Internet age? What changed since then?
* What was the first "authentication attack"? (Hint: it was in 1961.)
* What are Honan's tips for "online survival"?
* Who is the typical Twitter account hacker? (What's an "OG" username?)
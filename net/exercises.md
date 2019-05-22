# Exercises

---

### VPN Me!

![Thought Experiment](https://img.shields.io/badge/Type-Thought%20Experiment-success.svg)
![20m long](https://img.shields.io/badge/Duration-45m-yellow.svg)
![Primary skill is modeling](https://img.shields.io/badge/Primary%20Skill-Following%20the%20Spec-informational.svg)

A VPN (Virtual Private Network) is a system that routes a computer's Internet traffic through an intermediary node, such as an employer's remote network. This can be helpful in allowing employees to access devices on their company's internet network while at home, for example. Because the connection on a VPN between the computer and the intermediary node is encrypted (to various degrees of security), VPNs can also help users protect themselves against insecure local networks or spying ISPs (Internet Service Providers).

For this assignment, perform each of the following tasks:

1. Learn about VPNs by skimming the [Wikipedia page](https://en.wikipedia.org/wiki/Virtual_private_network).
2. Learn about how public security-oriented VPNs, such as [Private Internet Access](https://www.privateinternetaccess.com/) and [ProtonVPN](https://protonvpn.com/) work.
3. Write a brief analysis considering the potential security benefits and drawbacks of public security-oriented VPNs. Think about the various attack vectors these VPN services open and close, as well as who these services might be well suited for.

---

### A Dive into IP

![Lab](https://img.shields.io/badge/Type-Lab-success.svg)
![45m long](https://img.shields.io/badge/Duration-45m-yellow.svg)
![Primary skill is system management](https://img.shields.io/badge/Primary%20Skill-System%20Management-informational.svg)

In this lab, you will dive in to the network functions of the Ubuntu operating system. If you don't already have an Ubuntu server set up, you'll want to create one.

?> **You can get your server for free!** There's no need to pay for your server. Public cloud platforms like AWS (Amazon Web Services) and GCP (Google Cloud Platform) provide free-tier servers which are suitable for this exercise.

Once you've set up your server, work through the questions below. Note any difficulties or interesting findings in a text document on your own computer.

1. Perform a dump of the TCP traffic by running the command `sudo tcpdump`. If you'd like to save the output, run `sudo tcpdump > tcpdump.log`. Then, inspect the output of the TCP dump. Do you recognize parts of the output? What do you understand? What don't you understand?
2. Figure out how to route the path `cybersecurity` to `learn.blueshells.net` on your Ubuntu server. (Hint: Google the `hosts` file.)
3. Turn on UFW (Uncomplicated Firewall) to block traffic on all ports except 22 (SSH, which must remain open for you yourself to connect to the server). How can you test that you were successful?

---

### Trace Your Route

![Lab](https://img.shields.io/badge/Type-Lab-success.svg)
![20m long](https://img.shields.io/badge/Duration-20m-yellow.svg)
![Primary skill is network exploration](https://img.shields.io/badge/Primary%20Skill-Network%20Exploration-informational.svg)

The traceroute command (`traceroute` on Unix-based systems and `tracert` on Windows) displays the path by which your computer accesses a remote host over the Internet. From the Gelb Science Center, the `traceroute` to `1.1.1.1` (Cloudflare's distributed high-performance DNS server) is:

```
$ traceroute 1.1.1.1
traceroute to 1.1.1.1 (1.1.1.1), 30 hops max, 60 byte packets
 1  172.16.248.3 (172.16.248.3)  8.932 ms  8.843 ms  8.810 ms
 2  10.1.1.1 (10.1.1.1)  4.899 ms  4.915 ms  4.887 ms
 3  198.140.203.33 (198.140.203.33)  4.870 ms  4.824 ms  4.807 ms
 4  te-5-0-0-3974-pe02.needham.ma.ibone.comcast.net (24.104.131.245)  8.571 ms  8.490 ms  8.450 ms
 5  162.151.149.97 (162.151.149.97)  4.611 ms  8.256 ms  8.271 ms
 6  be-126-ar01.needham.ma.boston.comcast.net (68.85.106.53)  11.274 ms  8.339 ms  8.257 ms
 7  76.96.121.242 (76.96.121.242)  11.642 ms  11.592 ms  11.575 ms
 8  one.one.one.one (1.1.1.1)  11.484 ms  7.109 ms  14.348 ms
```

Meanwhile, the `traceroute` to `cs.auckland.ac.nz` (in New Zealand) is:

```
$ traceroute cs.auckland.ac.nz
 1  172.16.248.3 (172.16.248.3)  14.597 ms  14.446 ms  14.399 ms
 2  10.1.1.1 (10.1.1.1)  14.232 ms  14.252 ms  14.226 ms
 3  198.140.203.33 (198.140.203.33)  14.200 ms  14.183 ms  14.136 ms
 4  te-5-0-0-3974-pe02.needham.ma.ibone.comcast.net (24.104.131.245)  14.142 ms  14.110 ms  14.107 ms
 5  162.151.149.97 (162.151.149.97)  14.044 ms  14.015 ms  13.974 ms
 6  be-126-ar01.needham.ma.boston.comcast.net (68.85.106.53)  16.659 ms  10.147 ms  10.050 ms
 7  be-1003-pe02.onesummer.ma.ibone.comcast.net (68.86.90.173)  9.855 ms  9.880 ms  9.841 ms
 8  50.208.232.122 (50.208.232.122)  8.402 ms  12.010 ms  11.982 ms
 9  ae-2.r21.chcgil09.us.bb.gin.ntt.net (129.250.4.102)  31.920 ms  35.026 ms  35.010 ms
10  ae-5.r22.snjsca04.us.bb.gin.ntt.net (129.250.5.17)  84.485 ms  88.154 ms  88.129 ms
11  ae-40.r02.snjsca04.us.bb.gin.ntt.net (129.250.3.121)  88.098 ms  87.314 ms  135.470 ms
12  ae-4.r06.plalca01.us.bb.gin.ntt.net (129.250.4.118)  132.063 ms  131.917 ms  131.834 ms
13  xe-0-1-0-0-4.r06.plalca01.us.ce.gin.ntt.net (140.174.28.138)  131.808 ms  131.717 ms  131.640 ms
14  xe-3-0-0.bb1.a.lax.aarnet.net.au (202.158.194.170)  131.600 ms  110.912 ms  108.689 ms
15  xe-0-0-3.pe1.tkpa.akl.aarnet.net.au (202.158.194.172)  286.524 ms  253.979 ms  263.342 ms
16  et-1-0-0-204.and12-nsh.reannz.aarnet.net.au (182.255.119.141)  268.243 ms  262.052 ms  269.891 ms
17  210.7.39.177 (210.7.39.177)  289.885 ms  227.564 ms  248.414 ms
18  210.7.39.178 (210.7.39.178)  222.069 ms  248.420 ms  226.408 ms
19  br-cpf3-north.net.auckland.ac.nz (130.216.252.162)  246.805 ms  231.583 ms  225.878 ms
20  cxj-alfa-ae12-br-cpf3-bond2.net.auckland.ac.nz (130.216.252.166)  248.233 ms  306.947 ms  297.638 ms
21  * * *
22  cs.auckland.ac.nz (130.216.158.22)  298.783 ms  289.304 ms  285.433 ms
```

Notice how the request to `1.1.1.1` takes only eight 'hops,' while the request to `cs.auckland.ac.nz` takes 22. The reason why is simple: New Zealand is farther away than the nearest `1.1.1.1` access point.

In this lab, experiment with the `traceroute`s of various hostnames. What does the output of `traceroute` represent? What does `* * *` mean? Predict whether the route for various hostnames will be short (< 8) or long (> 15), and try to imagine through which geographic regions your request might pass. What is the shortest route you can find? What is the _longest_ route? (Note: you may need to increase the maximum number of 'hops' from 30 to answer this one.) Are there any hops that your network traffic _always_ passes through?

---

### Audit This Site

![Lab](https://img.shields.io/badge/Type-Lab-success.svg)
![45m long](https://img.shields.io/badge/Duration-45m-yellow.svg)
![Primary skill is security auditing](https://img.shields.io/badge/Primary%20Skill-Security%20Auditing-informational.svg)

In this open-ended lab, you will perform a security audit of this website! While you should _not_ try to take the website down, for example, you _should_ look at the code and see how you could _theoretically_ cause problems.

!> **You have permission to audit _this_ website, but no other!** Be careful that you don't do anything that could potentially even _resemble_ cybercrime.

1. What is this course website's threat model?
2. What are two or three attack surfaces for this site?
3. Were you able to identify any concrete vulnerabilities in this site? If so, have you thought about submitting a pull request on [GitHub](https://github.com/milesmcc/cyber101) to fix it?
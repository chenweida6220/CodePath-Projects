# Project 9 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:

* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: __________________

Description:

<img src="blue-vuln1.gif">

Vulnerability #2: __________________

Description:

<img src="blue-vuln2.gif">

## Green

# Vulnerability #1: Username Enumeration

Description:
Username Enumeration is the process of developing a list of all valid usernames on a server or web application and it becomes possible if the server or web application provides a clue as to whether or not the username exists.

When using CodePath's supplied username, "jmonroe99", which already exists, the green site displayed a login error in bold.
But when using a madeup username, "kevin123", which under the assumption that there is no username like this in the server, the green site displayed an unbolded login error.
Although both errors returns "Log in was unsuccessful.", the only visual difference was one was bold and the other was not.

Using the _inspect_ element, I analyzed both the bolded and unbolded login errors and it turns out there are two _span_ tag classes -- "failure", which results in the bolded login error and "failed", which results in an unbolded login error.

<img src="username_enumeration.gif">

Vulnerability #2: __________________

Description:

<img src="green-vuln2.gif">


## Red

Vulnerability #1: __________________

Description:

<img src="red-vuln1.gif">

Vulnerability #2: __________________

Description:

<img src="red-vuln2.gif">


## Notes

Describe any challenges encountered while doing the work

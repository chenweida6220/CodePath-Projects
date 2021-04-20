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

### Vulnerability #1: __________________

Description:

<img src="blue-vuln1.gif">

### Vulnerability #2: __________________

Description:

<img src="blue-vuln2.gif">

## Green

### Vulnerability #1: Username Enumeration

Description:
Username Enumeration is the process of developing a list of all valid usernames on a server or web application and it becomes possible if the server or web application provides a clue as to whether or not the username exists.

When using CodePath's supplied username, "jmonroe99", which already exists, the green site displayed a login error in bold.
But when using a madeup username, "kevin123", which under the assumption that there is no username like this in the server, the green site displayed an unbolded login error.
Although both errors returns "Log in was unsuccessful.", the only visual difference was one was bold and the other was not.

Using the _inspect_ element, I analyzed both the bolded and unbolded login errors and it turns out there are two _span_ tag classes -- "failure", which results in the bolded login error and "failed", which results in an unbolded login error.

<img src="username_enumeration.gif">

### Vulnerability #2: __________________

Description:

<img src="green-vuln2.gif">


## Red

### Vulnerability #1: Insecure Direct Object Reference

Description: Insecure Direct Object Reference is when code accesses a restricted resource based on user input but fails to verify user's authorization to access that resource.

Through changing the _id_ parameter on the red site's "Find a Saleperson" tab, it is explicitly shown that entering the ids from 1-9 shows the salespeople in the database that are unrestricted/publicized, but when entering ids of 10 and 11, it is clearly written in parenthesis that their information is not meant to be shown as of yet.

<img src="insecure_direct_object_reference.gif">

### Vulnerability #2: __________________

Description:

<img src="red-vuln2.gif">


## Notes

Describe any challenges encountered while doing the work

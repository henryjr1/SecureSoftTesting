# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: __________________

Vulnerability #2: __________________


## Green

Vulnerability #1: Username Enumeration

Gif:
![Gif of exploit](https://github.com/henryjr1/SecureSoftTesting/blob/Week-8/ENUMERATION.GIF)

Overview:
Using a valid username like "jmonroe99" with an incorrect password results in a bolded text saying "Log in was unsuccessful." Using an invalid username like "jm" results in the same text accept it is not bolded. This allows attacks to determine which usernames are in the systeme and which ones are not. This would make it easier to attack the system because attackers can soley focus on valid usernames and not waste time with invalid ones. 

Vulnerability #2: __________________


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)

Gif:
![Gif of exploit](https://github.com/henryjr1/SecureSoftTesting/blob/Week-8/IDOR.GIF)

Overview:
Using burp I was able to change the value of id to 10, which gave me access to Testy McTesterson who profile was not supposed to be public until Septermber 1st.

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work

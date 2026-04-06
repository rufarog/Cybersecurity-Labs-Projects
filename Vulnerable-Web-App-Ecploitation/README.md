# Overview
This lab involved exploiting a web application vulnerabilities to gain remote access to a server and escalate privileges to read a restricted file. The attack involved JavaScript analysis, credential stuffing, SQL injection, file upload bypass, reverse shell, and privilege escalation using SUID binaries.

## Lab Details and Background given
Recently BigCorp Security sent a message to your team in head office saying that the firewall had flagged some
suspicious activity. A file named e349802D_complaint was exfiltrated from the corporate server. The IP that the
file was transmitted to appears to belong to a site called “node13”. Working with law enforcement you have been
given the go ahead to attempt to penetrate their website and recover your property.
Local Law Enforcement has no record of the site or the people running it. However, one of their informants is an
ex-member and says his password might still be active. He claims he could not remember exactly what it was but
that it was the title of a well-known film about hackers (all lowercase).

## Tools and Methods Used
- Postman (Password Cracking)
- Netcat (Reverse Shell)
- SQL Injection
- GTFO Bins
- Privilege Escalation

## Step 1 - Website Analysis
I began by using the IP address of the site (192.168.56.108) to access the webpage and upon seing the webpage there was a message that read "NODE13" on the screen. I noticed that there was a pi symbol in the top right corner and nothing happened when clicking on it. I examined the HTML using the inspection tools and noticed there was a simple piece of JavaScript code that required to click that pi symbol while holding Shift and Control at the same time. Upon clicking on the pi symbol again with the two keys I was given a textbox and a button that said "Login" and nothing else. I attempted some passwords and noticed that it was sending the password entered and "login" as credentials. Based on the background it was revealed that the password is the name of a well-known film about hackers. 

## Step 2 - Password Cracking
I compiled a list of well-known films about hacking into a text file and used Postman to send the password attempts to the website to find which may have worked. After running the results all failed but upon some research, I noticed that one of the password attempts had a larger size than the others and I attempted the password and I was able to login. The successful password was the 2001 movie swordfish. 



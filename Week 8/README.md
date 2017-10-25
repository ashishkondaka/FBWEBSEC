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

Vulnerability #1: SQL Injection



Vulnerability #2: __________________


## Green

Vulnerability #1: Username Enumeration

	Vulnerability: Entering in a name of the existing user and a random password will cause an error to pop up in bold. Entering        	in an previously unknown user and a random password will cause a normal error to pop up. The programming lets known users 		know there password is wrong by indicating the message in bold. 

	Here is a walkthrough of the vulnerability:

	GIF Walkthrough: https://i.imgur.com/XZJrlfk.gifv

	GIF Made through LICEcap.app. 

Vulnerability #2: Cross-Site Scripting (XSS)

	Vulnerability: If you create an alert message in the comments section the blue and red sites should put the alert under the 	feedback but if you try the same in the green website then you either get a pop up or the feedback doesnt even show up. 

	Here is a walkthrough of the vulnerability:

	GIF Walkthrough: https://i.imgur.com/FAW7MKa.gifv

	GIF Made through LICEcap.app. 


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
	Vulnerability: Going on the Blue and Green site and changing the ID to 10 or 11 takes you back to you the list of	 members but in the red site changing the numbers will take you to Testy McTesterson and Lazy Lazyman pages. The 	 programmer did not make those users unavailbe on the red site. 
  
  	Here is a walkthrough of the vulnerability:
  
  	GIF Walkthrough: https://i.imgur.com/btyqiJf.gifv
  
  	GIF Made through LICEcap.app.

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work

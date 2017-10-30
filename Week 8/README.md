# Project 8 - Pentesting Live Targets

Time spent: 4 hours spent in total

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
	
	Vulnerability: This exploit can allow anyone to put a SQL Injection into the sales persons page ID. This will cause 	    the page to wait 5 seconds before it gets redirected back to the default page. In the blue page though, typing in this 	   exploit into the URL (%27%20OR%20SLEEP(5)=0--%27) next to id= will cause the URL to head back to the default persons 	page. 
	
	Here is a walkthrough of the vulnerability:

	GIF in repo.

	GIF Walkthrough: https://i.imgur.com/oE63AzA.gifv

	GIF Made through LICEcap.app. 



Vulnerability #2: Session Hijacking/Fixation
	
	Vulnerability: This exploit will let anyone gain acess to the blue site without logging into the blue site. Logging 	    into the red site or the green site and then clicking log in into the blue site will automatically sign you in. 
	
	Here is a walkthrough of the vulnerability:
	
	GIF in repo. 

	GIF Walkthrough: https://i.imgur.com/tPVHzqF.gifv

	GIF Made through LICEcap.app. 


## Green

Vulnerability #1: Username Enumeration

	Vulnerability: Entering in a name of the existing user and a random password will cause an error to pop up in bold. 	    Entering in an previously unknown user and a random password will cause a normal error to pop up. The programming lets 	   known users know there password is wrong by indicating the message in bold. 

	Here is a walkthrough of the vulnerability:
	
	GIF in repo. 

	GIF Walkthrough: https://i.imgur.com/XZJrlfk.gifv

	GIF Made through LICEcap.app. 

Vulnerability #2: Cross-Site Scripting (XSS)

	Vulnerability: If you create an alert message in the comments section the blue and red sites should put the alert 	  under the feedback but if you try the same in the green website then you either get a pop up or the feedback doesnt 	 	 even show up. 

	Here is a walkthrough of the vulnerability:
	
	GIF in repo. 

	GIF Walkthrough: https://i.imgur.com/FAW7MKa.gifv

	GIF Made through LICEcap.app. 


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
	
	Vulnerability: Going on the Blue and Green site and changing the ID to 10 or 11 takes you back to you the list of	 members but in the red site changing the numbers will take you to Testy McTesterson and Lazy Lazyman pages. The 	 programmer did not make those users unavailbe on the red site. 
  
  	Here is a walkthrough of the vulnerability:
	
	GIF in repo. 
  
  	GIF Walkthrough: https://i.imgur.com/btyqiJf.gifv
  
  	GIF Made through LICEcap.app.

Vulnerability #2: Cross-Site Request Forgery
	
	Vulnerability: Allows you to change the data of a user sales without changing the CSRF token when you inspect. In the 	      green site, if you change the CSRF Token to anything else, it will give you an error whereas on the red site, 		instead of an error you are still able to change the user data. 
	
	Here is a walkthrough of the vulnerability:
	
	GIF in repo. 
	
	GIF Walkthrough: https://i.imgur.com/uuWLpAC.gifv
	
	GIF Made through LICEcap.app.


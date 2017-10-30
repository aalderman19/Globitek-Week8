# Project 8 - Pentesting Live Targets

Time spent: **3** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration						 - IN GREEN
* Insecure Direct Object Reference (IDOR)	 - IN RED
* SQL Injection (SQLi)						 - IN BLUE
* Cross-Site Scripting (XSS)				 - IN GREEN
* Cross-Site Request Forgery (CSRF)			 - IN RED
* Session Hijacking/Fixation				 - IN BLUE

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQLi - The user can insert a SQL statement into the id of the url in the find a salesperson display of user information.

 - GIF:
 
 ![Alt text](/Week8BlueSQLI.gif)

Vulnerability #2: Session Hijacking/Fixation - Made the two browsers (IE/Chrome) have the same SESSION ID. Logged in as an admin in chrome and was able to access the site in IE without logging in.

 - GIF:
 
 ![Alt text](/Week8BlueSessionHijacking.gif)


## Green

Vulnerability #1: XSS - The user can submit feedback that when accessed from the admin side, will run code in a script tag. The other sites probably escape the strings that the users can submit feedback for.

 - GIF: 
 
 ![Alt text](/Week8GreenXSS.gif)

Vulnerability #2: Username Enumeration - If the username does not exists when someone attempts to login, the error message will appear not bolded. The developer used the wrong css class "failed". To make the message bold, the class name is "failure".

 - GIF:
 
 ![Alt text](/Week8GreenUserNameEnum.gif)


## Red

Vulnerability #1: IDOR - The "Find a salesperson" will give you further information about a salesperson qwhen you click their name. If you change the id of the salesperson, it will allow you to see private information. In Blue and Green, the private numbers will redirect you to the previous page if you try to use a private id.

 - GIF: 
 
 ![Alt text](/Week8RedIDOR.gif)

Vulnerability #2: CSRF - I created a fake form that submits data through the post request. If there was a real attack, they could fake a site link in the feedback section that would redirect them to the fake site.

 - GIF:
 
 ![Alt text](/Week8RedCSRF.gif)
 
 


## Notes

Describe any challenges encountered while doing the work

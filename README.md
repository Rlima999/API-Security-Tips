# API-Security-Tips
API-Security-Tips Credits to Abhishek Meena

## Never assume there’s only one way to authenticate to an API! Modern apps have many API endpoints for AuthN: /api/mobile/login | /api/v3/login | /api/magic_link; etc.. 

Find and test all of them for AuthN problems.


## SQL Injections used to be extremely common 5-10 years ago, and you could break almost every company? 

BOLA (IDOR) is the new epidemic of API security.

As a pentester, if you understand how to exploit it, your glory is guaranteed.

https://inonst.medium.com/a-deep-dive-on-the-most-critical-api-vulnerability-bola-1342224ec3f2


## Testing a Ruby on Rails App & noticed an HTTP parameter containing a URL? 

Developers sometimes use "Kernel#open" function to access URLs == Game Over. 

Just send a pipe as the first character and then a shell command (Command Injection by design)


## Found SSRF? use it for:

Internal port scanning
Leverage cloud services(like 169.254.169.254)
Use http://webhook.site
 to reveal IP Address & HTTP Library
Download a very large file (Layer 7 DoS)
Reflective SSRF? disclose local mgmt consoles


## Mass Assignment is a real thing. 

Modern frameworks encourage developers to use MA without understanding the security implications. 

During exploitation, don't guess object's properties names, simply find a GET endpoint that returns all of them.


## A company exposes an API for developers? 

This is not the same API which is used by mobile / web application. 

Always test them separately. 

Don't assume they implement the same security mechanisms.


## Pentest for REST API? 

Give it a chance and check if the API supports SOAP also. 

Change the content-type to "application/xml", add a simple XML in the request body, and see how the API handles it.


## Trying to find BOLA (IDOR) vulnerabilities? 

IDs in the HTTP bodies/headers tend to be more vulnerable than IDs in URLs. Try to focus on them first.



## Forget about CSRF! If the authentication mechanism doesn't support cookies, the API is protected against CSRF by design.

Thank you for Reading These these thread 
All credit Goes to @traceableai
















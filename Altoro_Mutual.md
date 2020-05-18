# Altoro Mutual

## Overview

How the fuck did you find this place...... ANYWHO Altoro Mutual is a vulnerable website that you can hack or whatevs, so I'll go through my web hacking methodology, and show you how we do.

## Sub-Domain Enumeration

Lets start off with arguably the most important part of the testing process.

### amass

Lets start off with amass, amass is a great tool that can do tons of DNS enumeration techniques. (Brute Forcing, Reverse DNS, Zone Transfers??)

Amass is already pre installed with kali btw
Make sure you run `apt upgrade` to get the latest version of amass

If you're not running kali you can download amass <a href="https://github.com/OWASP/Amass">Here</a>

For the amass command I ran `amass enum -d testfire.net`

You can see for the output we got

`testfire.net`

`demo.testfire.net`

`evil.testfire.net`

`altoro.testfire.net`

`www.testfire.net`

`demo2.testfire.net`

`localhost.testfire.net`

`ftp.testfire.net`

BTW all these domains just redirect to the main domain so nothing special

And the IP ranges for the domains are

`65.61.136.0/22`

Ight sweet that's our output I guess..

### Subfinder

Lets use another DNS enumeration tool, Subfinder is used for finding subdomains and bla bla bla.
You can install it <a href="https://github.com/projectdiscovery/subfinder">Here</a>

You need to install go lang as well you can install it <a href="https://golang.org/doc/install">Here</a>

Oki Doki when your done installing that bull shniki then we can run Subfinder and see what we GET lulz

I ran the command `subfinder -d testfire.net`

and ba da bing ba da boom
we got

Now that we got both files lets combine the two
and use `sort -u` ovi, KLSDAJFLKJADFJDFJA

This is the final output

`20.testfire.net`

`altoro.testfire.net`

`demo2.testfire.net`

`demo-analytics.testfire.net`

`demo.testfire.net`

`domain2.testfire.net`

`evil.testfire.net`

`ftp.testfire.net`

`httpdemo.testfire.net`

`localhost.testfire.net`

`srchttpdemo.testfire.net`

`testfire.net`

`testsite.testfire.net`

`www.testfire.net`

## Sub-Domain Takeover

## CORS misconfigurations

## Network Enumeration

## Website Enumeration

## Profit

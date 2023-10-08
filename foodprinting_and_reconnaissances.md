# footprinting and reconnaissance

### Learning Objectives








## Understanding Footprinting and Reconnaissance in Cybersecurity

**Introduction:**
Footprinting and reconnaissance are fundamental steps in the process of information gathering. They play a crucial role in cybersecurity, ethical hacking, and competitive intelligence by providing valuable insights into a target, be it a network, organization, or individual.

**Footprinting:**
Footprinting marks the initial phase of information gathering. It involves the discreet collection and analysis of data about the target without any direct interaction. The primary goal is to acquire as much relevant information as possible while avoiding detection. Passive techniques, such as examining public sources, social media profiles, domain registrations, DNS records, and web server banners, are used to build a comprehensive profile of the target. Additionally, this phase identifies potential vulnerabilities and areas of interest within the target's infrastructure.

**Reconnaissance:**
Reconnaissance, also known as active information gathering or probing, follows footprinting. This phase involves actively probing the target to gather specific and detailed information. Unlike footprinting, reconnaissance is more intrusive.

It's important to note that while these activities are essential for security professionals to understand and protect against potential threats, they can also be used maliciously by hackers or cybercriminals. Unauthorized or malicious footprinting and reconnaissance activities are illegal and unethical, as they can lead to security breaches, data theft, or other harmful actions. Ethical hacking, also known as penetration testing, involves performing these activities with proper authorization to identify and mitigate security weaknesses.

In summary, footprinting and reconnaissance are crucial phases in information gathering that can be used for both legitimate security purposes and potentially malicious activities, depending on the intent and authorization of the person conducting them.


# Reconnaissance in Ethical Hacking

Reconnaissance, also known as Footprinting or Information Gathering, is a crucial stage in ethical hacking that involves gathering information about a target system or network. In this guide, we will explore the various techniques and tools used in reconnaissance to identify vulnerabilities that could be exploited.

## Types of Reconnaissance

There are two main types of reconnaissance:

### Passive Reconnaissance

Passive reconnaissance involves gathering information without directly interacting with the target system. This can be done through publicly available sources, such as websites and search engines.

### Active Reconnaissance

Active reconnaissance involves directly interacting with the target system. This can include techniques such as network scans and vulnerability scans and can raise the risk of detection.

## What Ethical Hackers and Pentesters Look For

Ethical hackers and pentesters look for various pieces of information during the reconnaissance phase, including:

- Network Information
  - Domain name
  - Internal Domain
  - IP Address
  - Unmonitored/private websites
  - TCP/UDP Services
  - VPN/IDS/IPS/access controls
  - VPN info
  - Phone numbers/VoIP
  - Network topology
  - Network device
- Operating System Information
  - Users and group names/info
  - Banner grabbing
  - Routing tables
  - SNMP
  - System architecture
  - Remote systems
  - System names
  - Passwords
  - Dumpster diving
  - Version
  - Patch level
- Organization Information
  - Organization website
  - Company directory
  - Employee information
  - Business structure
  - Location details
  - Comments in HTML source code
  - Security policies deployed
  - Webserver links
  - Background of organization
  - Marketing and advertising
  - Prevailing events
  - Partners
  - Phone
  - Financial information

## External Network Pentester

External network pentesters focus on evaluating the security of an organization’s external network infrastructure. They look for:

- Whois
- Operating systems and applications
- Publicly accessible information
- Google and Search Engine
- Website Mirroring
- Archive Sites
- Github recon
- Network Information
- Web server Content
- Email Header
- People Sites
- Social Network
- Alert Website

## Internal Network Pentester

Internal network penetration testing focuses on evaluating the security of an organization’s internal network infrastructure. They look for:

- IP Address
- Internal DNS
- Private Website
- Dumpster Diving
- Shoulder Surfing

## Web Application Pentester

Web application pentesters focus on evaluating the security of an organization’s web applications. They look for:

- Network Information
  - IP address
  - Domain name
  - Network topology
  - Open ports and services
- Web Application Information
  - Web server technology used
  - Application framework
  - Source code (if accessible)
  - Session management
  - Input validation and data handling
  - Authentication and authorization mechanisms
- Web Server Information
  - Operating system
  - Web server software version
  - Server-side scripting language and version
  - Database management system and version
- Web Application Components
  - Dynamic content generation
  - Client-side scripting languages
  - Third-party components and libraries

    ![images (4)](https://github.com/masshuvo/full_ceh_guide/assets/108648096/885a1761-17c0-4f04-bd17-a96c8b6ea91d)


## Conclusion

Reconnaissance is an essential stage in ethical hacking that involves gathering information about a target system or network. It helps ethical hackers and pentesters identify vulnerabilities that could be exploited. By understanding the various techniques and tools used in reconnaissance, you can enhance your skills as an ethical hacker or pentester.


# Footprinting in Cybersecurity

Footprinting involves gathering information about a target system that can be used to execute a successful cyber attack. To obtain this information, hackers use various methods and tools. This information serves as the initial step for the hacker to exploit a system. There are two types of footprinting:

## Active Footprinting
Active footprinting involves direct interaction with the target machine.

## Passive Footprinting
Passive footprinting involves collecting information about a system located remotely from the attacker.

### Information Gathered Through Footprinting

- The operating system of the target machine
- Firewall information
- IP address
- Network map
- Security configurations of the target machine
- Email IDs and passwords
- Server configurations
- URLs
- VPN details

### Sources for Footprinting

1. **Social Media**: Hackers leverage the tendency of many individuals to share sensitive information online. They may create fake accounts to befriend or follow someone to gather their information.

2. **JOB Websites**: Organizations often share confidential data on job websites. For example, a job posting mentioning "Job Opening for Lighttpd 2.0 Server Administrator" reveals that an organization uses the Lighttpd web server version 2.0.

3. **Google**: Search engines like Google can be used for advanced searches, known as "Google hacking." Operators like "inurl," "allinurl," and "filetype" combined with basic search techniques can reveal sensitive information. For example, searching "inurl:ViewerFrame?Mode=" can find public web cameras.

4. **Social Engineering**: Various techniques fall under this category, including eavesdropping and shoulder surfing, where attackers attempt to record personal information through communication mediums.

5. **Archive.org**: This website collects snapshots of older website versions, providing information that may no longer exist on the current site.

6. **Organization's Website**: The organization's website is a prime source for open-source information provided to clients, customers, or the public.

7. **Using Neo Trace**: NeoTrace is a powerful tool for tracing network paths. It displays the route between the user and the remote site, including intermediate nodes and their information.

8. **Whois**: This website allows hackers to trace information about domain names, email IDs, domain owners, and more, serving as a valuable tool for website footprinting.

By understanding these techniques and sources, individuals can enhance their knowledge of footprinting in cybersecurity.

![images (2)](https://github.com/masshuvo/full_ceh_guide/assets/108648096/309fc493-67fc-47fa-85e6-727ff407e55d)


# Fingerprinting in Ethical Hacking

Fingerprinting refers to the methods used in ethical hacking to determine the operating system running on a remote computer. There are two main types of fingerprinting:

## Active Fingerprinting
Active fingerprinting involves sending specially crafted packets to a target machine and analyzing its response to determine the target's operating system. Tools like NMAP can be used for this purpose.

## Passive Fingerprinting
Passive fingerprinting relies on sniffer traces from the remote system, such as Wireshark data. By analyzing these traces, you can deduce the operating system of the remote host.

### Factors Analyzed for OS Determination
To determine the operating system, four important elements are examined:

- TTL (Time-To-Live) set on outbound packets
- Window Size
- DF (Don't Fragment) bit
- TOS (Type of Service) settings

These factors help in OS identification, although it's not always 100% accurate and may work better for some operating systems than others.

### Basic Steps
Before attacking a system, it's crucial to determine the target's operating system. Once known, it's easier to identify potential vulnerabilities for exploitation.

Here's a simple NMAP command to identify the OS and open ports of a website:

```shell
nmap -O -v tutorialspoint.com
```

# Port Scanning
Port scanning reveals open ports on a server. For example:

PORT      STATE   SERVICE 
22/tcp    open    ssh 
80/tcp    open    http 
443/tcp   open    https 
3306/tcp  open    mysql


Ping Sweep
A ping sweep (ICMP sweep) helps find live hosts in a range of IP addresses. For example, using fping:

```shell
fping -a -g 192.168.0.1 192.168.0.255
```

# DNS Enumeration
DNS enumeration gathers information about DNS servers and their records. Tools like nslookup and scripts like DNSenum.pl can assist in this process.

Quick fixes and precautions are also discussed to safeguard systems against potential attacks.

These techniques and tools are essential in ethical hacking to gather information about target systems and enhance security.

# IP Track
❑ IP Logger:-
https://iplogger.org/
https://grabify.link/
❑ IP Locator:-
https://www.iplocation.net/
❑ Google Map(Location Track)
Latitude & Longitude in Google Maps
https://www.google.com/maps

# Domain (Website Info) >> Part-1

- [https://whois.domaintools.com/](https://whois.domaintools.com/)
- [https://domainbigdata.com/](https://domainbigdata.com/)

**DNS:**

- [https://smallseotools.com/domain-ip-lookup/](https://smallseotools.com/domain-ip-lookup/)
- [https://dnsdumpster.com/](https://dnsdumpster.com/)
- [https://www.ultratools.com/tools/dnsLookup](https://www.ultratools.com/tools/dnsLookup)
- [https://dnschecker.org/ns-lookup.php](https://dnschecker.org/ns-lookup.php)

**Site Hosting Company Info:**

- [https://smallseotools.com/domain-hosting-checker/](https://smallseotools.com/domain-hosting-checker/)
- [https://hostingchecker.com](https://hostingchecker.com)


# Domain (Website Info) >> Part-2
❑ Reverse Ip
- [https://www.yougetsignal.com/tools/web-sites-on-web-server/](https://www.yougetsignal.com/tools/web-sites-on-web-server/)
- [https://hackertarget.com/reverse-ip-lookup/](https://hackertarget.com/reverse-ip-lookup/)
- [https://www.whoishostingthis.com/](https://www.whoishostingthis.com/)
- [https://smallseotools.com/reverse-ip-lookup/](https://smallseotools.com/reverse-ip-lookup/)



# Which platform used for developing Ping to identify server details (CMS Check)
❑ CMS Check
- https://whatcms.org/
- https://cmsdetect.com/
- https://www.wpthemedetector.com/
❑ Chrome Extension
- https://chrome.google.com/webstore/detail/what-cms-is-
this/gamohlpmdjkdjepgdgjohkbfpmeelmem
- https://chrome.google.com/webstore/detail/wappalyzer/gppongmhjkpfnbhagpmjfk
annfbllamg?hl=en


# Which platform used for developing Ping to identify server details (Site BuiltWith)
❑ Chrome Extension
WhatRuns
- https://chrome.google.com/webstore/detail/whatruns/cmkdbmfndkfgebld
hnkbfhlneefdaaip?hl=en
BuiltWith
❑ Online Tools
- https://builtwith.com/
- https://sitereport.netcraft.com/
- https://w3techs.com/site



# Extra Site Info
❑ Domain Country Checker
Alexa, Country Flag Etc Browser Extension
❑ Domain Age Checker
- https://www.duplichecker.com/domain-age-checker.php
❑ SSL Checker
- https://www.digicert.com/help/
❑ Check Server Status
- https://smallseotools.com/check-server-status/
❑ Website Speed Checker
- https://tools.pingdom.com/
- https://gtmetrix.com/
❑ WEBSITE LINK COUNTER CHECKER
- https://smallseotools.com/website-links-count-checker/



# Email Header
❑ Online Tools
- https://mxtoolbox.com/EmailHeaders.aspx
- https://www.whatismyip.com/email-header-analyzer/
- https://chrome.google.com/webstore/detail/email-tracker-for-gmail-
m/ndnaehgpjlnokgebbaldlmgkapkpjkkb


# Valid Email Address Checker
## Online Valid Mail Checker
- https://quickemailverification.com/
- https://network-tools.com/
# Valid Mail Verifier Tool
To check mail address valid or invalid


# IP Locator Best One
- https://ipinfo.io

# Data Breach Checker
- https://breachdirectory.org/
- https://haveibeenpwned.com/

# epieos Tools |Email Recon
## epieos Tools - Email Checking Tool - Leaks, Google Profiles | OSINT Recon
- https://tools.epieos.com/



# Subdomain Enumeration Suite
❑ Sub3 Suite is a research-grade suite of tools for Subdomain Enumeration, OSINT
Information gathering & Attack Surface Mapping. Supports both manual and automated
analysis on variety of target types with many available features & tools.
❑ Github: 3nock/sub3suite: a free, open source, cross platform Intelligence
gathering tool. (github.com)


# OSINT Sites List

- [Biggest OSINT Sites List](https://start.me/p/b5Aow7/asint_collection)



# Recon
- [GitHub: Reconator](https://github.com/Teammatrixx/Reconator)


# TryHackMe Room

- [https://tryhackme.com/room/threatinteltools](https://tryhackme.com/room/threatinteltools)

# Theory

- [https://tryhackme.com/room/geolocatingimages](https://tryhackme.com/room/geolocatingimages)
- [https://tryhackme.com/room/ohsint](https://tryhackme.com/room/ohsint)
- [https://tryhackme.com/room/searchlightosint](https://tryhackme.com/room/searchlightosint)










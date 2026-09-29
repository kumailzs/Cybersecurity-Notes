## Cybersecurity Foundation Roadmap
Before we start the roadmap, let's first understand what cybersecurity is, why it matters, and what kinds of roles exist in this field. Knowing the bigger picture makes it easier to see why each foundation skill is needed.
#### What is cybersecurity?
Cybersecurity is the practice of protecting systems, networks, applications, and data from unauthorized access, misuse, disruption, or destruction. It covers both sides of the problem: finding weaknesses in systems, and defending systems against people who exploit those weaknesses.
#### Why it matters
Almost every organization now runs on software, networks, and stored data. When those are compromised, the result can be financial loss, leaked personal information, service outages, or legal consequences. Because of this, organizations need people who understand how systems fail and how to protect them. The field is real and in demand, but it is also competitive at entry level, and it rewards people who actually understand technology rather than people who only know tool names.

**The main sides and job roles**
Cybersecurity is not one job. It is a group of related fields.

**Offensive (Red Team side)**: testing systems by attacking them, with permission
- Penetration Tester
- Red Team Operator
- Application Security Engineer
- Vulnerability Researcher / Exploit Developer
- Bug Bounty Hunter (this is freelance, not a salaried job, and income is irregular)

**Defensive (Blue Team side)**: detecting, preventing, and responding to attacks
- SOC Analyst
- Incident Responder
- Digital Forensics Analyst
- Threat Hunter
- Detection Engineer
- Malware Analyst
- Security Engineer / Cloud Security Engineer

**Other related areas**
- GRC (Governance, Risk, and Compliance)
- Security Architecture
- Security Consulting

**Reality Check:** Most entry-level openings are on the defensive side (for example SOC roles). Offensive roles exist in smaller numbers and usually expect prior experience, strong fundamentals, or a proven track record.
#### Why foundational skills come first
Every security domain sits on top of general IT knowledge. A penetration tester who does not understand networking cannot explain why a scan result matters. A SOC analyst who does not understand Windows or Linux logs cannot tell normal activity from suspicious activity. Tools can be learned in days, but the understanding behind them takes longer, and it is what separates someone who runs tools from someone who can actually analyze a problem.

Skipping the foundation usually leads to one of two outcomes: getting stuck as soon as a task goes beyond a tutorial, or memorizing steps without knowing why they work. Neither holds up in a real job or a technical interview.
#### What we will learn: Foundation (common for everyone)
- Networking: TCP/IP, OSI, DNS, HTTP, ports, Wireshark
- Linux: file system, permissions, processes, services, logs
- Bash: scripting, grep/awk/sed, automation
- Windows: registry, services, event logs, PowerShell basics
- Active Directory Fundamentals: domain, users/groups, GPO, Kerberos/NTLM basics, LDAP
- Python: scripting, networking, APIs, small tools
- Web Fundamentals: requests/responses, cookies/sessions, HTML/JS, authentication flows
- Core Security Concepts: CIA triad, crypto basics, authN/authZ, common attacks, threat modeling
- Basic Cloud Concepts: IaaS/PaaS/SaaS, IAM, shared responsibility model
#### The value of this foundation
- It applies to both offensive and defensive paths, so you can choose a direction later with more information.
- It makes advanced topics (exploitation, forensics, detection engineering) far easier to learn because you already understand what is underneath them.
- It helps you troubleshoot on your own instead of depending on step-by-step guides.
- Interviewers in this field tend to test fundamentals (networking, OS behavior, how authentication works) more than tool knowledge.
#### Timeline
The timeline depends on the individual: prior experience, hours per day, consistency, and how much is practiced hands-on rather than only watched or read. For someone starting from scratch and studying regularly, completing the foundation properly often takes several months to a year or more. Anyone promising a much shorter path is likely leaving gaps.
#### Honest expectations
- Finishing the foundation does not guarantee a job. It makes you ready to specialize and to be a credible candidate.
- Certificates can help with screening, but they do not replace hands-on skill.
- Practice matters more than passive learning: build a home lab, do labs, and write down what you learn.
- Progress is uneven. Some topics (like Active Directory or networking) will feel slow at first, and that is normal.
### Roadmap Overview

> This roadmap has 9 foundation phases. Each phase builds on the previous one, and all of them are common for both offensive and defensive paths. After completing the foundation, you can choose a specialization.
### Phase 1: Networking

**What it is:** Networking is how devices communicate and exchange data. Almost every attack and defense happens over a network, so this is the base for everything else.

**What to learn:**

1. **Network basics:** what a network is, LAN / WAN / MAN, client-server model, peer-to-peer, network topologies
2. **Network devices:** hub, switch, router, modem, access point, firewall
3. **Reference models:** OSI model (7 layers), TCP/IP model, encapsulation and decapsulation
4. **Addressing:** MAC address, IPv4, IPv6, public vs private IPs, subnet mask, CIDR, subnetting, default gateway
5. **Core supporting protocols:** ARP, ICMP (ping, traceroute), DHCP
6. **DNS:** how name resolution works, record types (A, AAAA, CNAME, MX, NS, TXT), recursive vs authoritative servers
7. **Transport layer:** TCP vs UDP, ports and sockets, three-way handshake, flags (SYN, ACK, FIN, RST), connection teardown
8. **Application layer protocols:** HTTP/HTTPS, FTP/SFTP, SSH, Telnet, SMTP/POP3/IMAP, SMB, RDP, SNMP
9. **Switching and routing:** VLANs, trunking, routing tables, static vs dynamic routing, NAT and PAT
10. **Network security basics:** firewalls, ACLs, proxies, VPNs, IDS/IPS
11. **Wireless basics:** Wi-Fi standards, WEP/WPA2/WPA3
12. **Command-line network tools:** ping, traceroute, nslookup/dig, netstat/ss, ipconfig/ifconfig/ip
13. **Packet analysis:** Wireshark, tcpdump, capture filters vs display filters, following a stream, analyzing a TCP handshake, DNS and HTTP traffic
### Recommended Resources
  
You can use the following resources to build your networking foundation. You do **not** need to use all of them at once — pick one as your primary resource and use the others for clarification or additional practice.

**Professor Messer — CompTIA Network+ N10-009**
**Free:** Yes
Professor Messer's N10-009 Network+ course provides structured coverage of networking fundamentals, including OSI, networking devices, protocols, IPv4/IPv6, subnetting, routing, switching, wireless networking, and more. The course currently contains 87 free videos with nearly 13 hours of total runtime.

[Professor Messer — N10-009 Network+ Training Course](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/?utm_source=chatgpt.com)

**Cisco Skills for All — Networking Basics**
**Free:** Yes
Use the **Networking Basics** course from Cisco Skills for All.

- Enroll for free.
    
- Complete **Module 1 → Module 15 in order**.
    
- Take the quiz after each module.
    
- Aim for **80%+** on each quiz.
    
- If you score below 80%, review the module and retake the quiz.
    
- Spend extra time on **Module 9 — Subnetting**, as subnetting is an important networking skill.

[Cisco Skills for All — Networking Basics](https://skillsforall.com/course/networking-basics?utm_source=chatgpt.com)

**NetworkChuck — Free CCNA Course**
**Free:** Yes
NetworkChuck's free CCNA material can be used as an additional resource when you want deeper explanations and practical networking concepts. His free CCNA series covers topics such as network devices, OSI/TCP-IP, Ethernet, IP addressing, subnetting, and other CCNA-level networking concepts.

Use this as a **supplementary resource**, not something you need to complete alongside every other course.

### Practice

TryHackMe networking rooms will be very helpful for turning the concepts you learn into practical skills. Complete these rooms **alongside the roadmap**, rather than waiting until you finish all the theory.

**Recommended TryHackMe Networking Sequence**

1. **What is Networking?**  
    Start with the absolute basics: networks, the Internet, and fundamental networking terminology.
    
2. **Intro to LAN**  
    Learn about Local Area Networks, network technologies, and basic LAN design.
    
3. **OSI Model**  
    Build a strong understanding of the seven-layer OSI model and how network communication is structured.
    
4. **Packets & Frames**  
    Learn how data is broken down, encapsulated, and transmitted across a network.
    
5. **Extending Your Network**  
    Understand how networks are connected and extended beyond a local network.
    
6. **Introductory Networking**  
    Reinforce the OSI/TCP-IP models and start working with practical networking tools such as `ping`, `traceroute`, and `dig`.
    
7. **Networking Concepts**  
    Go deeper into IP addresses, subnets, routing, TCP/UDP, ports, and network communication.
    
8. **Networking Essentials**  
    Practice important networking concepts including DHCP, ARP, ICMP, routing, and NAT.
    
9. **Networking Core Protocols**  
    Learn and practice core protocols such as DNS, WHOIS, HTTP, FTP, SMTP, POP3, and IMAP. This is useful for understanding how common network services communicate.
    
10. **Wireshark 101**  
    Apply your networking knowledge to real packet captures. Practice identifying and analyzing ARP, ICMP, TCP, DNS, and other traffic. TryHackMe recommends completing Introductory Networking first.


------------------------------------------------------------------------
### Phase 2: Linux

**What it is:** Linux is the operating system behind most servers, cloud systems, and security tools. Most security work happens on or against Linux machines.

**What to learn:**

1. **Basics:** what Linux is, distributions (Ubuntu, Debian, Kali, CentOS/RHEL), kernel vs shell, installing Linux (VM or dual boot)
2. **Terminal navigation:** pwd, ls, cd, absolute vs relative paths, hidden files
3. **File system hierarchy:** /, /etc, /var, /home, /bin, /usr, /tmp, /root, /proc, /dev
4. **File and directory management:** touch, mkdir, cp, mv, rm, cat, less, head, tail, find, locate, wildcards
5. **Text editors:** nano, vim basics
6. **Users and groups:** /etc/passwd, /etc/shadow, /etc/group, useradd, usermod, passwd, su, sudo, sudoers
7. **File permissions:** read/write/execute, chmod (numeric and symbolic), chown, chgrp, umask, SUID, SGID, sticky bit
8. **Process management:** ps, top/htop, kill, jobs, foreground/background, process states
9. **Package management:** apt, dpkg, yum/dnf, installing from source
10. **Services and daemons:** systemd, systemctl, enabling/disabling services, cron jobs
11. **Networking on Linux:** ip, ss, netstat, /etc/hosts, /etc/resolv.conf, iptables/ufw basics
12. **Logs:** /var/log, syslog, auth.log, journalctl, reading and searching logs
13. **Remote access:** SSH, key-based authentication, scp, rsync
14. **Disk and system info:** df, du, mount, lsblk, uname, uptime, free
### Recommended Resources

Use these resources to build a strong Linux foundation. You do not need to complete everything simultaneously — use **Linux Journey as your primary structured resource**, and use the other resources for deeper learning and hands-on practice.

**Linux Journey**
**Free:** Yes
[Linux Journey](https://linuxjourney.com/) is beginner-friendly and structured, making it a good starting point for learning Linux from the fundamentals.

Focus on understanding the concepts rather than simply completing the lessons.

**The Linux Command Line — William Shotts
Free:** Yes
[The Linux Command Line](https://linuxcommand.org/tlcl.php) by William Shotts is a free book focused on learning the Linux command line in depth.

Use it as a reference alongside your practical learning, especially when you want a deeper understanding of commands, shell usage, filesystems, permissions, processes, and scripting.

**TryHackMe — Linux Fundamentals
Free/Paid:** Some content may require a subscription
Complete the **Linux Fundamentals Part 1, Part 2, and Part 3** rooms.

These rooms provide hands-on practice with Linux commands and concepts in a cybersecurity-oriented environment.
### Practice

Hands-on practice is essential for building Linux skills. Use these platforms alongside the Linux learning roadmap to reinforce what you learn through real command-line exercises and practical labs.

**OverTheWire — Bandit
Free:** Yes
[OverTheWire Bandit](https://overthewire.org/wargames/bandit/) is designed for beginners and teaches Linux command-line skills through a series of progressively challenging levels.

Complete the levels in order and try to solve each challenge yourself before looking for hints or solutions.

Focus on understanding the commands and techniques you use rather than simply getting the password for the next level.

### 2. BreachLabs

Use **BreachLabs** for additional hands-on Linux and cybersecurity practice after building the basic command-line foundation.

Work through the labs gradually and apply the Linux concepts you have already learned.

### Recommended Practice Flow

**Learn Linux concept → Practice the commands locally → OverTheWire Bandit → BreachLabs → Review and take notes**

The goal is to become comfortable working in a Linux terminal, not just to complete labs as quickly as possible.

------------------------------------------------------------------------

  

# Phase 2 --- Linux + Bash

  

**Time:** 4 weeks

  

## Linux Fundamentals

  

Learn:

  

### Filesystem

  

Understand:

  

``` text

/

├── etc

├── var

├── home

├── bin

├── usr

├── tmp

└── root

```

  

### Essential Commands

  

Navigation:

  

``` bash

cd

ls

pwd

mkdir

```

  

File operations:

  

``` bash

rm

cp

mv

```

  

Reading files:

  

``` bash

cat

less

head

tail

nano

```

  

Permissions:

  

``` bash

chmod

chown

```

  

Understand:

  

- `r`

- `w`

- `x`

- `755`

- `644`

  

Users and groups:

  

``` bash

useradd

passwd

su

sudo

```

  

Packages:

  

``` bash

apt update

apt upgrade

apt install

```

  

Processes:

  

``` bash

ps

top

kill

```

  

Networking:

  

``` bash

ip addr

ping

ss

curl

wget

```

  

Text processing:

  

``` bash

grep

find

which

cut

sort

uniq

wc

```

  

Also understand:

  

- Pipes `|`

- Redirection `>`

- Append `>>`

- Input `<`

- Error redirection `2>`

- Environment variables

- SSH

- SSH keys

  

## Bash Fundamentals

  

Learn:

  

- Variables

- User input

- `if/else`

- `for`

- `while`

- Functions

- Script arguments

- `$1`, `$2`, `$@`

- Exit codes

- Shebang

- Executable permissions

  

## Resources

  

### TryHackMe --- Linux Fundamentals

  

https://tryhackme.com/module/linux-fundamentals

  

Complete:

  

- Linux Fundamentals Part 1

- Linux Fundamentals Part 2

- Linux Fundamentals Part 3

  

### Linux Journey

  

https://linuxjourney.com/

  

Focus on:

  

- Basic command line

- Text processing

- Permissions

- Processes

- User management

  

### The Linux Command Line

  

http://linuxcommand.org/tlcl.php

  

Use this for deeper Linux understanding.

  

### Bash Tutorial

  

https://ryanstutorials.net/bash-scripting-tutorial/

  

Focus on the basic chapters covering:

  

- Shell basics

- Variables

- Input

- Arithmetic

- Conditions

- Loops

- Functions

  

## Practice

  

### OverTheWire --- Bandit

  

https://overthewire.org/wargames/bandit/

  

Work through the early levels and focus on understanding the commands

used to solve each problem.

  

### Linux Strength Training

  

https://tryhackme.com/room/linuxstrengthtraining

  

Use after the basic Linux material.

  

## Project

  

Write a Bash script that:

  

1. Reads IP addresses from a text file.

2. Pings each address.

3. Reports which addresses respond and which do not.

  

**Do not copy the final script. Build it yourself.**

  

## Phase Goal

  

You should be able to:

  

- Navigate a Linux filesystem.

- Find and modify files.

- Understand permissions.

- Work with processes/users.

- Use pipes and redirection.

- Write a basic Bash script using arguments.

  

------------------------------------------------------------------------

  

# Phase 3 --- Windows + Active Directory Fundamentals

  

**Time:** 2--3 weeks

  

## Windows Fundamentals

  

Learn:

  

### Windows Filesystem

  

Understand:

  

``` text

C:\Windows

C:\Windows\System32

C:\Users

C:\Program Files

```

  

### Registry

  

Understand:

  

- What the Windows Registry is

- HKLM

- HKCU

  

### CMD

  

Basic commands:

  

``` text

ipconfig

dir

cd

type

netstat

tasklist

schtasks

```

  

### PowerShell

  

Basic commands:

  

``` powershell

Get-Process

Get-Service

Get-ChildItem

```

  

Understand how PowerShell differs from traditional CMD.

  

### Users and Permissions

  

Learn:

  

- Local users

- Administrators group

- NTFS permissions

  

### Logging

  

Understand Windows Event Logs and important authentication events such

as:

  

- 4624 --- successful logon

- 4625 --- failed logon

- 4648 --- explicit credentials

  

### Security Components

  

Understand:

  

- Windows Firewall

- Microsoft Defender

- Windows Services

  

------------------------------------------------------------------------

  

## Active Directory Fundamentals

  

Learn:

  

- Domain

- Domain Controller

- Organizational Units (OUs)

- Users

- Groups

- Group Policy

- Kerberos

- TGT

- TGS

- NTLM

- LDAP

- SAM

- Forests

- Domains

- Trust relationships

  

At this stage, focus on **how the system works**, not attacking it.

  

## Resources

  

### TryHackMe --- Windows & Active Directory Fundamentals

  

https://tryhackme.com/module/windows-and-active-directory-fundamentals

  

Focus on:

  

- Windows Fundamentals Part 1

- Windows Fundamentals Part 2

- Windows Fundamentals Part 3

- Active Directory Basics

  

### Microsoft Learn

  

https://learn.microsoft.com/en-us/training/

  

Use Microsoft Learn to reinforce:

  

- Windows Server fundamentals

- Active Directory Domain Services

  

### TCM Security --- Active Directory Overview

  

Search YouTube for:

  

`TCM Security Active Directory 101 Heath Adams`

  

Use it as a conceptual introduction.

  

## Practice

  

Build a small Windows Server lab if your hardware allows it:

  

- Windows Server VM

- Domain Controller

- Test users

- Test groups

- Client VM joined to the domain

  

## Phase Goal

  

Explain what happens when a domain user logs into a Windows domain,

especially the role of **Kerberos**.

  

------------------------------------------------------------------------

  

# Phase 4 --- Python Programming

  

**Time:** 4 weeks

  

The goal is **not** to become a full-time software developer.

  

The goal is to become comfortable enough with Python to:

  

- Read security scripts.

- Modify scripts.

- Automate repetitive tasks.

- Understand basic security tooling.

- Build small utilities.

  

## What to Learn

  

### Core Python

  

- Variables

- Data types

- Strings

- Lists

- Dictionaries

- Booleans

- Conditions

- Loops

- Functions

- Arguments

- Return values

  

### Practical Python

  

- File handling

- Error handling

- Modules

- `sys`

- `os`

- `subprocess`

- `socket`

- `requests`

- `json`

- `argparse`

  

## Resources

  

### Automate the Boring Stuff with Python

  

https://automatetheboringstuff.com/

  

Focus on the fundamental Python chapters first.

  

### TCM Security --- Python 101

  

Search YouTube for:

  

`TCM Security Python 101 for Hackers`

  

Use it after learning Python fundamentals.

  

### Real Python

  

https://realpython.com/

  

Useful topics:

  

- Requests

- JSON

- Python command-line interfaces

  

### CodeWithHarry

  

https://www.codewithharry.com/

  

Use the Python course if you need Hindi explanations before studying the

English material.

  

## Practice

  

### HackerRank Python

  

https://www.hackerrank.com/domains/python

  

Complete beginner-level problems and focus on writing the solutions

yourself.

  

## Projects

  

Build small programs such as:

  

1. Read IP addresses from a file and check connectivity.

2. Build a basic TCP port-checking program for your own lab.

3. Build a simple HTTP request utility that displays response

information.

  

Keep all testing limited to systems you own or are explicitly authorized

to test.

  

## Phase Goal

  

You should be able to write a small Python program without copying a

complete solution from the internet.

  

------------------------------------------------------------------------

  

# Phase 5 --- Web Fundamentals

  

**Time:** 4--5 weeks

  

> **Important:** Learn how the web works before studying web

> vulnerabilities.

  

## Step 1 --- How the Internet Works

  

Understand:

  

- Client-server model

- Request-response cycle

- Browser

- DNS

- URL structure

  

Example URL structure:

  

``` text

https://example.com/path?query=value

```

  

Understand:

  

- Protocol

- Hostname

- Path

- Query string

  

------------------------------------------------------------------------

  

## Step 2 --- HTTP

  

Learn:

  

### Methods

  

``` text

GET

POST

PUT

DELETE

PATCH

```

  

### Important Headers

  

- Content-Type

- User-Agent

- Authorization

- Cookie

- Set-Cookie

  

### Status Codes

  

Understand common categories and examples:

  

``` text

200

201

301

302

400

401

403

404

500

```

  

Also understand:

  

- HTTP request structure

- HTTP response structure

- Cookies

- Sessions

- Authentication flow

- HTTP vs HTTPS

  

------------------------------------------------------------------------

  

## Step 3 --- HTML

  

Learn:

  

- HTML structure

- Elements

- Attributes

- Forms

- Input fields

- GET vs POST form submission

- View Source

- Basic browser developer tools

  

------------------------------------------------------------------------

  

## Step 4 --- SQL Fundamentals

  

Learn:

  

- Databases

- Tables

- Rows

- `SELECT`

- `FROM`

- `WHERE`

- `INSERT`

- `UPDATE`

- `DELETE`

- Basic `UNION`

- SQL comments

  

The purpose here is understanding databases, not jumping directly into

SQL injection.

  

------------------------------------------------------------------------

  

## Step 5 --- APIs

  

Understand:

  

- REST APIs

- Endpoints

- Requests

- Responses

- JSON

- API keys

- Frontend vs backend

  

------------------------------------------------------------------------

  

## Step 6 --- JavaScript Basics

  

Learn enough JavaScript to understand what happens in a browser:

  

- Variables

- Functions

- `var`, `let`, `const`

- Events

- DOM

- `console.log`

- `fetch`

- `localStorage`

  

You do **not** need to become a JavaScript developer for this foundation

track.

  

## Resources

  

### TryHackMe --- How the Web Works

  

https://tryhackme.com/module/how-the-web-works

  

Recommended order:

  

1. DNS in Detail

2. HTTP in Detail

3. How Websites Work

4. Putting It All Together

  

### MDN --- HTTP

  

https://developer.mozilla.org/en-US/docs/Web/HTTP

  

Focus on:

  

- HTTP overview

- HTTP messages

- HTTP request methods

- HTTP response status codes

  

### W3Schools --- HTML

  

https://www.w3schools.com/html/

  

Focus on basic HTML and forms.

  

### SQLZoo

  

https://sqlzoo.net/

  

Use the beginner SQL tutorials for hands-on SQL practice.

  

### The Odin Project --- JavaScript Foundations

  

https://www.theodinproject.com/paths/foundations/courses/foundations

  

Focus only on JavaScript fundamentals and DOM/events.

  

### CodeWithHarry

  

Use the Hindi JavaScript and SQL material when an English explanation is

unclear.

  

## Burp Suite --- Foundation-Level Familiarity

  

https://portswigger.net/burp/documentation/desktop/getting-started

  

At this stage, learn:

  

- What a proxy is

- How Burp fits between browser and server

- How to intercept your own HTTP traffic

- How to inspect requests/responses

- Basic Repeater usage

  

The goal is **understanding HTTP traffic**, not learning exploitation

yet.

  

## Phase Goal

  

You should be able to:

  

> Intercept your own HTTP request, identify its method, URL, headers,

> cookies and parameters, modify a harmless value, send it, and explain

> the response.

  

------------------------------------------------------------------------

  

# Phase 6 --- Core Security Concepts

  

**Time:** 2 weeks

  

Now connect the technical foundations to cybersecurity concepts.

  

## What to Learn

  

### Security Principles

  

- CIA Triad

- Confidentiality

- Integrity

- Availability

- AAA

- Authentication

- Authorization

- Accounting

- Least privilege

- Defense in depth

- Zero Trust

  

### Threats and Attacks --- Concept Level

  

Understand:

  

- Phishing

- Social engineering

- Man-in-the-middle

- DoS

- DDoS

- Malware categories

  

At this stage, understand **what they are, how they work conceptually,

and how they are defended against**.

  

### Cryptography Fundamentals

  

Understand:

  

- Symmetric encryption

- Asymmetric encryption

- Hashing

- AES

- RSA

- SHA-256

- Encryption vs hashing

- Digital certificates

- PKI

- Certificate chains

- TLS handshake

  

### Network Security

  

Understand:

  

- Stateful vs stateless firewalls

- IDS

- IPS

- VPNs

  

### Vulnerability Concepts

  

Learn:

  

- CVE

- CVSS

- Vulnerability vs threat vs risk

- Basic vulnerability lifecycle

  

### OWASP

  

Understand the major categories in the OWASP Top 10 conceptually.

  

For each vulnerability category, ask:

  

1. What is the problem?

2. What can happen because of it?

3. How can it be prevented?

  

Do not rush into exploitation.

  

## Resources

  

### Professor Messer --- Security+

  

https://www.professormesser.com/security-plus/

  

Focus on:

  

- Threats, attacks and vulnerabilities

- Cryptography

- Network security

- Identity and access management

- Architecture and design

  

### TryHackMe --- Pre-Security

  

https://tryhackme.com/path/outline/presecurity

  

Use this as a broad foundation review.

  

### OWASP Top 10

  

https://owasp.org/www-project-top-ten/

  

Use it to understand common web application security categories.

  

### NVD

  

https://nvd.nist.gov/

  

Read real CVE entries and learn how vulnerability information is

documented.

  

### MITRE ATT&CK

  

https://attack.mitre.org/

  

Explore the framework at a high level:

  

- Tactics

- Techniques

- Initial Access

- Execution

- Persistence

  

Do not go deep yet.

  

## Phase Goal

  

You should be able to look at a basic security scenario and explain:

  

- What asset is involved?

- What security property is affected?

- What type of threat/vulnerability is present?

- What defensive control could reduce the risk?

  

------------------------------------------------------------------------

  

# Phase 7 --- Cloud Basics

  

**Time:** \~1 week

  

Cloud is increasingly part of modern infrastructure, so foundation-level

awareness is useful.

  

## What to Learn

  

### Cloud Fundamentals

  

- Cloud computing

- On-premises vs cloud

- IaaS

- PaaS

- SaaS

- Shared responsibility model

  

### AWS Basics

  

Understand:

  

- AWS

- EC2

- S3

- VPC

- IAM

  

### Security Concepts

  

Focus on:

  

- IAM

- Permissions

- S3 access

- VPC networking

- Cloud misconfiguration

- Shared responsibility

  

## Resource

  

### AWS Skill Builder

  

https://skillbuilder.aws/

  

Look for:

  

**AWS Cloud Practitioner Essentials**

  

Focus on:

  

- Introduction to AWS

- Compute

- Networking

- Storage

- Security

  

### TryHackMe --- Cloud Fundamentals

  

Use a beginner cloud fundamentals room to reinforce the concepts.

  

## Safe Practice

  

If using a cloud account, understand the platform first and carefully

monitor resources and permissions.

  

## Phase Goal

  

You should be able to explain:

  

> What is a cloud server, what is an S3 bucket, what does IAM control,

> and how is cloud security different from simply securing a local

> computer?

  

------------------------------------------------------------------------

  

# 🧪 Foundation Completion Checklist

  

Before moving into dedicated offensive-security training, you should be

comfortable with the following.

  

## Networking

  

- [ ] Explain OSI and TCP/IP

- [ ] Understand IPv4 addressing

- [ ] Understand CIDR and subnetting

- [ ] Explain DNS

- [ ] Explain DHCP

- [ ] Explain ARP

- [ ] Understand TCP/UDP

- [ ] Explain the TCP handshake

- [ ] Understand common ports and services

- [ ] Use Packet Tracer

- [ ] Read basic traffic in Wireshark

  

## Linux

  

- [ ] Navigate the filesystem

- [ ] Manage files

- [ ] Understand permissions

- [ ] Manage users/groups

- [ ] Understand processes

- [ ] Use pipes/redirection

- [ ] Use basic networking commands

- [ ] Connect using SSH

- [ ] Write basic Bash scripts

  

## Windows / AD

  

- [ ] Understand Windows filesystem

- [ ] Understand Registry basics

- [ ] Use CMD

- [ ] Use basic PowerShell

- [ ] Understand Windows users/groups

- [ ] Understand NTFS permissions

- [ ] Read basic Event Logs

- [ ] Explain domains

- [ ] Explain Domain Controllers

- [ ] Explain Group Policy

- [ ] Understand Kerberos conceptually

- [ ] Understand NTLM conceptually

- [ ] Understand LDAP basics

  

## Python

  

- [ ] Write basic Python programs

- [ ] Use conditions and loops

- [ ] Write functions

- [ ] Read/write files

- [ ] Handle errors

- [ ] Use modules

- [ ] Work with JSON

- [ ] Make basic HTTP requests

- [ ] Use command-line arguments

  

## Web

  

- [ ] Explain client/server architecture

- [ ] Explain DNS in the web context

- [ ] Understand HTTP requests/responses

- [ ] Understand methods and status codes

- [ ] Understand headers

- [ ] Understand cookies and sessions

- [ ] Understand basic HTML/forms

- [ ] Understand SQL fundamentals

- [ ] Understand APIs/JSON

- [ ] Understand basic JavaScript/DOM

- [ ] Inspect HTTP traffic with Burp Suite

  

## Security

  

- [ ] Explain CIA Triad

- [ ] Explain AAA

- [ ] Understand authentication vs authorization

- [ ] Explain hashing vs encryption

- [ ] Understand symmetric/asymmetric cryptography

- [ ] Understand TLS/PKI basics

- [ ] Understand firewalls

- [ ] Understand IDS/IPS

- [ ] Understand VPN basics

- [ ] Understand CVE/CVSS

- [ ] Understand OWASP vulnerability categories

- [ ] Understand least privilege

- [ ] Understand defense in depth

- [ ] Understand Zero Trust concept

  

## Cloud

  

- [ ] Explain IaaS/PaaS/SaaS

- [ ] Explain shared responsibility

- [ ] Understand EC2

- [ ] Understand S3

- [ ] Understand VPC basics

- [ ] Understand IAM basics

  

------------------------------------------------------------------------

  

# 🎓 Foundation Exit Test

  

Before starting a dedicated offensive-security curriculum, you should be

able to do these without blindly following a tutorial:

  

1. Explain what happens when a browser accesses a website.

2. Capture and identify DNS and TCP traffic in Wireshark.

3. Build a small network in Packet Tracer.

4. Navigate and troubleshoot a Linux VM.

5. Explain Linux permissions.

6. Write a basic Bash script.

7. Explain Windows authentication at a conceptual level.

8. Explain the role of Active Directory.

9. Write a small Python utility.

10. Inspect an HTTP request in Burp Suite.

11. Explain cookies, sessions and authentication.

12. Explain basic SQL.

13. Explain CIA, AAA, hashing and encryption.

14. Read a basic CVE entry.

15. Explain basic cloud IAM, S3 and VPC concepts.

  

If you can do these confidently, you have a **real foundation** to build

on.

  

------------------------------------------------------------------------

  

# 🚀 What Comes After This?

  

This document intentionally stops at the **foundation boundary**.

  

The next roadmap should be a separate track covering topics such as:

  

- Pentesting methodology

- Enumeration

- Vulnerability discovery

- Web security

- Internal network security

- Active Directory security

- Privilege escalation

- Exploitation

- Post-exploitation

- Red-team methodology

- Specialized areas such as LLM/AI security

  

Those topics should **not be mixed into this foundation roadmap**.

  

------------------------------------------------------------------------

  

## Final Principle

  

> **Learn the system before learning how to break the system.**

  

A strong foundation means you understand the underlying technology well

enough that security concepts make sense instead of becoming a

collection of tools and commands.
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

**BreachLabs**
Use **BreachLabs** for additional hands-on Linux and cybersecurity practice after building the basic command-line foundation.

Work through the labs gradually and apply the Linux concepts you have already learned.

------------------------------------------------------------------------
### Phase 3: Bash

**What it is:** Bash is the command-line shell and scripting language used on Linux. It lets you automate tasks and process data quickly, which is used daily in both offensive and defensive work.

**What to learn:**

1. **Shell basics:** how the shell works, commands, arguments, options, man pages, command history
2. **Input/output:** stdin, stdout, stderr, redirection (>, >>, <, 2>), pipes (|)
3. **Text processing tools:** grep, egrep, cut, sort, uniq, wc, tr, head, tail
4. **Advanced text processing:** sed, awk, basic regular expressions
5. **Variables and environment:** variables, environment variables, PATH, export, quoting rules
6. **Script fundamentals:** shebang, creating and running scripts, permissions, arguments ($1, $2, $@, $#), exit codes
7. **Control flow:** if/else, test conditions, case statements
8. **Loops:** for, while, until
9. **Functions:** defining and calling, return values, scope
10. **Input handling:** read, user prompts, validating input
11. **Automation:** cron, combining commands, simple log parsing scripts, batch file operations
12. **Debugging:** set -x, error handling, checking exit status
## Recommended Resources

**Linuxize — Bash Scripting Fundamentals**
**Free:** Yes

Use the **Bash Scripting Fundamentals** series as the primary resource. It is a 50-part series covering Bash from the basics through scripting and automation, including variables, environment variables, I/O and redirection, conditionals, loops, functions, arguments, exit codes, and debugging-related topics.

[Linuxize — Bash Scripting Fundamentals](https://linuxize.com/series/bash-scripting-fundamentals/?utm_source=chatgpt.com)

**freeCodeCamp — Bash Scripting Tutorial for Beginners
Free:** Yes
This beginner-friendly tutorial covers commands, creating scripts, variables, positional arguments, input/output redirection, `if/elif/else`, `case`, loops, functions, exit codes, `awk`, and `sed`.
Use it when you want a **video-based explanation** or another explanation of a topic you find difficult.

**GNU Bash Reference Manual
Use the official Bash documentation as a **reference** when you need to understand specific Bash features or behavior in more depth.

[GNU Bash Reference Manual](https://www.gnu.org/software/bash/manual/?utm_source=chatgpt.com)

### Practice
Use these platforms to practice Bash hands-on alongside the roadmap.

**TryHackMe — Bash Scripting

Practice Bash scripting in a cybersecurity-focused environment, including variables, parameters, arrays, conditionals, and other scripting fundamentals.

**OverTheWire — Bandit

Use Bandit to strengthen your command-line problem-solving skills through progressively challenging Linux tasks. It is especially useful for practicing commands, file manipulation, permissions, pipes, redirection, and text processing.

**Exercism — Bash Track

Use the Bash track for dedicated programming exercises. It gives you small problems where you have to write Bash code yourself, making it useful for improving scripting logic and problem-solving.


------------------------------------------------------------------------
### Phase 4: Windows

**What it is:** Windows is the most common operating system in corporate environments. Understanding how it works internally is necessary to secure it or test it.

**What to learn:**

1. **Basics:** Windows editions (Home, Pro, Server), installing Windows in a VM, GUI vs command line
2. **File system:** NTFS, drive structure, important folders (System32, Program Files, Users, ProgramData), file permissions and ACLs
3. **Users and groups:** local users, administrators, built-in accounts, SIDs, UAC
4. **Command prompt:** cmd basics, navigation, file operations, network commands (ipconfig, netstat, nslookup, tasklist, net user)
5. **PowerShell basics:** cmdlets, verb-noun structure, pipeline, Get-Help, Get-Process, Get-Service, Get-ChildItem, variables, simple scripts, execution policy
6. **Processes and services:** Task Manager, services.msc, service accounts, startup items, scheduled tasks
7. **Registry:** structure (HKLM, HKCU, etc.), common persistence and configuration locations, regedit
8. **Event logs:** Event Viewer, Security/System/Application logs, important Event IDs (for example 4624, 4625, 4688, 4720), Sysmon overview
9. **Windows security features:** Windows Defender, Windows Firewall, BitLocker, patching and Windows Update
10. **Windows networking:** shares, SMB, RDP, WinRM basics
11. **Administrative tools:** Computer Management, Local Security Policy, Task Scheduler, Sysinternals tools (Process Explorer, Autoruns)
### Recommended Resources

**Microsoft Learn — Windows Fundamentals

**Free:** Yes

Use Microsoft Learn to understand Windows fundamentals, including the filesystem, users and groups, permissions, processes, services, networking, security features, and administrative tools.

[Microsoft Learn — Windows](https://learn.microsoft.com/en-us/windows/)

**Microsoft Learn — PowerShell

**Free:** Yes

Use this for the basics of PowerShell: cmdlets, pipeline, variables, `Get-Help`, common commands, and simple scripts.

[Microsoft Learn — PowerShell](https://learn.microsoft.com/en-us/powershell/)

**Hack The Box Academy — Windows Fundamentals

Use HTB Academy's **Windows Fundamentals** material for additional hands-on learning and exercises covering Windows administration and security concepts.
### Practice

**TryHackMe — Windows Fundamentals

Complete the **Windows Fundamentals** rooms to practice Windows filesystem, users, permissions, processes, networking, and security concepts in a hands-on environment.

**Your Own Windows VM

Install Windows in a VM and practice the basics yourself:

- CMD and PowerShell commands
    
- Users and groups
    
- NTFS permissions
    
- Processes and services
    
- Event Viewer
    
- Registry basics
    
- Windows networking
    
- Firewall and security settings

---
### Phase 5: Python

**What it is:** Python is a general-purpose programming language. In security it is used to automate tasks, parse data, interact with APIs, and build small custom tools.

**What to learn:**

1. **Setup:** installing Python, running scripts, virtual environments, pip
2. **Basics:** variables, data types (int, float, string, boolean), operators, input/output
3. **Control flow:** if/elif/else, for and while loops, break/continue
4. **Data structures:** lists, tuples, dictionaries, sets
5. **Functions:** defining functions, arguments, return values, scope
6. **Modules and libraries:** importing, creating your own modules, standard library overview
7. **File handling:** reading and writing files, working with CSV and JSON, parsing logs
8. **Error handling:** try/except, common exceptions, basic debugging
9. **String handling and regex:** string methods, formatting, the re module
10. **Object-oriented basics:** classes, objects, methods (basic level only)
11. **Networking with Python:** socket module, simple TCP client/server, port scanner concept
12. **Web and APIs:** requests library, working with REST APIs, parsing JSON responses, basic web scraping
13. **System interaction:** os, sys, subprocess, argparse for command-line tools
14. **Small projects:** log analyzer, simple port scanner, password strength checker, file hash checker, API-based IP lookup tool
### Recommended Resources

**CS50P — Introduction to Programming with Python**

**Free:** Yes

Use CS50P as the primary resource for learning Python fundamentals, including variables, data types, control flow, functions, data structures, exceptions, libraries, and file handling.

[CS50P — Harvard](https://cs50.harvard.edu/python/)

**Automate the Boring Stuff with Python**

**Free:** Yes

Use this for practical Python and automation, especially file handling, regular expressions, working with data, and automating repetitive tasks.

[Automate the Boring Stuff](https://automatetheboringstuff.com/)

**Real Python**

Use Real Python as a reference for specific topics such as `requests`, sockets, JSON, regex, file handling, and `subprocess`.

[Real Python](https://realpython.com/)

### Practice

**Exercism — Python Track**

Solve beginner Python exercises to improve programming fundamentals, problem-solving, functions, data structures, and clean code.

[Exercism — Python](https://exercism.org/tracks/python)

**HackerRank — Python**

Use HackerRank for additional beginner-level Python exercises covering strings, collections, functions, and problem solving.

[HackerRank — Python](https://www.hackerrank.com/domains/python)

**Small Projects**

Build a few small projects after learning the fundamentals:

- Log analyzer
- Simple port scanner
- File hash checker
- API-based IP lookup tool
- Rewrite one of your Bash scripts in Python

Keep your projects in a GitHub repository and document what each project does.

-------
### Phase 7: Web Fundamentals

**What it is:** Web fundamentals cover how websites and web applications work. Web applications are one of the most common attack surfaces, so this knowledge is needed for both testing and defending them.

**What to learn:**

1. **How the web works:** client, server, browser, URL structure, DNS lookup to page load
2. **HTTP in depth:** request and response structure, methods (GET, POST, PUT, DELETE, etc.), headers, status codes
3. **HTTPS and TLS:** what encryption in transit does, certificates, certificate authorities, handshake overview
4. **Cookies and sessions:** how cookies work, session IDs, cookie flags (HttpOnly, Secure, SameSite), session lifecycle
5. **HTML basics:** structure, forms, links, inputs
6. **CSS basics:** only enough to read a page
7. **JavaScript basics:** variables, functions, DOM, events, how the browser runs JS
8. **Same-origin policy and CORS:** what they are and why they exist
9. **Web architecture:** front end, back end, databases, web servers (Apache, Nginx), reverse proxies, CDNs
10. **Databases and SQL basics:** tables, SELECT/INSERT/UPDATE/DELETE, WHERE, joins
11. **APIs:** REST basics, JSON, API keys, tokens
12. **Authentication flows:** username/password login, session-based auth, token-based auth (JWT), OAuth 2.0 overview, SSO, MFA
13. **Browser developer tools:** Network tab, inspecting requests, storage, console
14. **Proxy tools:** intercepting and viewing traffic using Burp Suite or OWASP ZAP (viewing level only at this stage)
  

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
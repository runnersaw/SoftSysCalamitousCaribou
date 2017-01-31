
# Security Project Proposal

##### Deniz Celik, Sawyer Vaughan, Chris Wallace

## Project Goals
For our first project, we are investigating C security. We will be researching exploitation techniques, and techniques for mitigating exploitation vulnerabilities.

### Lower bound:
- We jailbroke Sawyer’s iPod touch using compiled source code.
- We exploited a zero day bug on an old Linux distribution and wrote a writeup of how we exploited that bug and how the bug was mitigated.
- We created at least three examples of exploits, along with code that can be exploited and a write-up of how the exploit works and how it could be mitigated
- We created a write-up of common exploit mitigation techniques

### Upper Bound:
- We modified/commented the jailbroken source code to do something else
- We found code in a library, project or operating system that can be exploited.
- We downloaded an old version of a linux/unix OS, and recreated and documented an exploit that was found for that kernel/OS.

## Research

We have already done research and found information about various sorts of vulnerabilities. Sources that provide general information about C vulnerabilities:
- https://handouts.secappdev.org/handouts/2011/Frank%20Piessens/C-vulnerabilities-slides.pdf
  - This paper goes deeper into the technical details of the stack, with a walkthrough of what the values of the stack are throughout an exploit
- https://handouts.secappdev.org/handouts/2012/Yves%20Younan/C%20and%20C++%20vulnerabilities.pdf
  - The best resource that we’ve found. This clearly details many types of vulnerabilities, along with code examples.
- https://security.web.cern.ch/security/recommendations/en/codetools/c.shtml
  - A nice paper with common vulnerable C functions, along with techniques to mitigate those vulnerabilities.
- https://github.com/struct/mms
  - A github repository with code examples of exploits
- https://github.com/dirtycow/dirtycow.github.io/wiki/PoCs
  - An in-depth look at the “Dirty Cow” exploit that exists on current versions of Linux
  - https://github.com/gbonacini/CVE-2016-5195
- https://www.oreilly.com/ideas/the-state-of-linux-security?utm_medium=social&utm_source=twitter.com&utm_campaign=lgen&utm_content=State-of-Linux-Security-jj&cmp=tw-security-free-article-scny17_state_of_linux_security_jj
  - Article listing vulnerabilities found in linux in 2016

We have compiled a list of the following vulnerabilities, and have found the following information about many of them. 

- Buffer Overflow
  - http://www.tenouk.com/Bufferoverflowc/Bufferoverflow6.html
  - https://www.exploit-db.com/docs/33698.pdf
- Dangling Pointers 
  - http://www.blackhat.com/presentations/bh-usa-07/Afek/Whitepaper/bh-usa-07-afek-WP.pdf
- Double Free
  - http://www.blackhat.com/presentations/bh-usa-07/Ferguson/Whitepaper/bh-usa-07-ferguson-WP.pdf
  - http://phrack.org/issues/57/8.html#article
  - http://phrack.org/issues/57/9.html#article
  - http://www.securityfocus.com/archive/1/309913
  - Malloc Maleficarum
- Format String Vulnerabilities
  - Basically SQL injection
  - http://codearcana.com/posts/2013/05/02/introduction-to-format-string-exploits.html
  - https://www.owasp.org/index.php/Format_string_attack
- File Open Attacks
  - http://research.cs.wisc.edu/mist/presentations/kupsch_miller_secse08.pdf

We have found documentation about the existence of the following vulnerabilities, but have not extensibly researched them. 

- Indirect Pointer Overwriting
- Memory Leaks
- Heap Overflow
- Return Address Modification
- Symbolic Link Attack 
- Global Offset Table
- Virtual Function Table Overwrite
- Lack of Null Terminator

For our goal of jailbreaking an old iPhone, we have researched several past jailbreaks and found a good candidate for recreating. The specific jailbreak that we are looking at is called p0sixspwn. The source code for the posix_spawn iOS vulnerability exploit can be found in this Github repo https://github.com/p0sixspwn/p0sixspwn/. There is also a detailed slide deck showing how the posix_spawn function was exploited by Stefan Esser http://conference.hitb.org/hitbsecconf2013kul/materials/D2T2%20-%20Stefan%20Esser%20-%20Tales%20from%20iOS%206%20Exploitation%20and%20iOS%207%20Security%20Changes.pdf

## Current Status

We have already implemented proof-of-concepts for two types of vulnerabilities (buffer overflow and format string injection). We have posted write-ups of these two vulnerabilities, along with example code on our GitHub repository (https://github.com/runnersaw/SoftSysCalamitousCaribou/tree/master/Security/test_exploits).

## Project Backlog
Our project backlog is at the following URL: https://trello.com/b/a5FLTuaz/softsyscalamitouscaribou

## Potential Roadblocks
There are a few potential roadblocks in our way
- Difficulty and complexity of exploit tactics
- Exploit mitigation present on modern operating systems
- Lack of documentation or information about exploitation techniques



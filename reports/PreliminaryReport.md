## Preliminary Report Calamitous Caribou
Deniz Celik, Sawyer Vaughan, Chris Wallace

### Introduction
For our first project, we are investigating C security. We will be researching exploitation techniques, and techniques for mitigating exploitation vulnerabilities.

### Objective
#### Lower bound:
- We jailbroke Sawyer’s iPod touch using compiled source code.
- We exploited a zero day bug on an current Linux distribution and wrote a writeup of how we exploited that bug and how the bug was mitigated. [Dirty Cow Exploit] (https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/test_exploits/dirty_cow/README.md) 
- We created at least three examples of exploits, along with code that can be exploited and a write-up of how the exploit works and how it could be mitigated. [String Format Vulnerability](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/test_exploits/StringFormatVulnerability/README.md), [Buffer Overflow](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/test_exploits/buffer_overflow/README.md)
- We created a write-up of common exploit mitigation techniques.

#### Upper Bound:
- We modified/commented the jailbroken source code to do something else.
- We found code in a library, project or operating system that can be exploited.
- We downloaded an old version of a linux/unix OS, and recreated and documented an exploit that was found for that kernel/OS. [Dirty Cow Exploit] (https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/test_exploits/dirty_cow/README.md) 
- We have performed all of the exercises https://exploit-exercises.com/nebula/ and https://exploit-exercises.com/protostar/ and provided write-ups of what the vulnerability was, how we exploited it, and how it can be mitigated. 

### Project Progress
Our project’s Trello board can be found [here] (https://trello.com/b/a5FLTuaz/softsyscalamitouscaribou). For information about the tasks that we’ve completed on the project, take a look at the “Project Done” list.
### Research
We have already done research and found information about various sorts of vulnerabilities. Sources that provide general information about C vulnerabilities and a list of common vulnerability types can be found in our [previous proposal](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/reports/proposal.md).
During this sprint we identified and investigated certain exploits in more detail:
#### Use-After Free
An broad exploit that was investigated in order to accomplish some of the heap questions in exploit-exercises. It deals with reusing or re-setting memory after it has been free but not yet allocated. 

#### Dirty Cow
https://dirtycow.ninja/
#### P0sixspwn
This is a jailbreak for iOS 6 called p0sixspwn. The source code for the posix_spawn iOS vulnerability exploit can be found in this Github [repo] (https://github.com/p0sixspwn/p0sixspwn/). There is also a detailed [slide deck](http://conference.hitb.org/hitbsecconf2013kul/materials/D2T2%20-%20Stefan%20Esser%20-%20Tales%20from%20iOS%206%20Exploitation%20and%20iOS%207%20Security%20Changes.pdf.) showing how the posix_spawn function was exploited by Stefan Esser 
### Project Status
- We’ve created an example of a buffer overflow vulnerability. We wrote-up the how the exploit works along with relevant code in a [README]( https://github.com/runnersaw/SoftSysCalamitousCaribou/tree/master/Security/test_exploits/buffer_overflow).
- We also created an example of a format string vulnerability. A write-up of the vulnerability and example code that can be exploited exist in this [README](https://github.com/runnersaw/SoftSysCalamitousCaribou/tree/master/Security/test_exploits/StringFormatVulnerability).
- We have researched an exploit found in modern versions of Linux called Dirty COW. It is called Dirty COW because there is a bug in how the Linux kernel handled copy-on-write in a very specific way that allows users to write to files that they don’t have privileges to write to. A write-up that includes code and scripts for testing the exploit can be found [here](https://github.com/runnersaw/SoftSysCalamitousCaribou/tree/master/Security/test_exploits/dirty_cow).
- We have been working on compiling the p0sixspwn jailbreak tool but have been running into issues due to the age of the code and difficulty installing the libraries that it needs on modern operating systems.
- We have completed 10 of the Nebula vulnerability exercises. Solutions are [here](https://github.com/runnersaw/SoftSysCalamitousCaribou/tree/master/Security/nebulaExploits)
- We have completed 2 of the Protostar exercises. Solutions are found [here](https://github.com/runnersaw/SoftSysCalamitousCaribou/tree/master/Security/protostarExploits)

### Product Backlog
Our product backlog is [here](https://trello.com/b/a5FLTuaz/softsyscalamitouscaribou). The things that we are planning to do in the next sprint are now in the “This Sprint” list. There are a few tasks left in the “Backlog” that we are not planning to include as part of the sprint but we will do them if we have more time. 

### Potential Roadblocks and Instructor Assistance
We don’t feel that the roadblocks from our earlier project proposal are as impactful anymore. One of our main concerns was that we would have difficulty finding a middle ground between the most basic C exploits (stack/buffer overflows) and the complicated monster that is the iOS exploits we intend to run. However, finding the exploit-exercises website gave us insight not only into intermediate and advanced C exploits, but also enlightened us to some common UNIX exploits as well. In addition, our discovery of the Dirty Cow exploits assuaged many of our concerns that we would be unable to implement a simple UNIX zero-day without having to spend large amounts of time on it. Instead, a relatively modern Linux OS (Ubuntu 14.04) was able to be exploited with a few dozen lines of C code. As such, we believe that many of the roadblocks we had previously identified have been minimized or removed by our progress in this sprint.


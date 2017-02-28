
## Software Systems Security Project

#### An investigation into computer security. This work was done by Deniz Celik, Sawyer Vaughan, and Chris Wallace as a part of our Software Systems class at Olin College in the spring of 2017.

### Goal

This project is an investigation into computer security, which includes research about general types of vulnerabilites present in Unix operating systems and C code as well as examples of specific vulnerabilites in modern operating systems. As a part of our investigation into these vulnerabilites, we have included exploitable code as well as instructions about how to exploit it and how to write your code to mitigate the vulnerability for several kinds of exploits.

### Computer Security

In the world where we all own many different interconnected devices of all shapes and sizes, an emphasis on computer security has become increasingly important. Just recently, we have been engaged in crucial debates about [privacy](https://en.wikipedia.org/wiki/FBI%E2%80%93Apple_encryption_dispute), we've seen [hacking to rig elections](https://www.nytimes.com/news-event/russian-election-hacking), and experienced [widespread vulnerabilites](http://heartbleed.com/) that leak [private and protected information](https://bugs.chromium.org/p/project-zero/issues/detail?id=1139). In this day and age, an emphasis on computer security is crucial.

We aimed to investigate types of general vulnerabilites that can be used by hackers, as well as learning about how software engineers can create code that is protected from these kinds of attacks.

In fitting with the focus of the class, the emphasis of vulnerabilites researched revolves around Unix and C vulnerabilites.

### Project Work

After researching many different types of vulnerabilities, we created proof-of-concept exploits for a few types of vulnerabilities. For exploitable C code, we created C code that could reasonably exist in real-world projects. Then, we explained how the code could be exploited, and the steps that one would have to take to exploit the code. Included in the write-up of each vulnerability is steps that developers can take to mitigate that type of vulnerability in their code.

As well as a few C code exploitation demonstrations, we researched a well-known, recent zero-day vulnerability in the Linux kernel. For this, we included code and instructions to demonstrate the vulnerability on the user's operating system.

We also discovered the website [exploit-exercises.com](https://exploit-exercises.com/), which included a set of levels demonstrating various types of vulnerabilities. The site provides a virtual machine that is set up with these hypothetical users and environment. We performed many of the exploits provided by this website and provided write-ups for the levels that we completed.

#### C Exploits

##### Buffer Overflow

Here is our buffer overflow demonstration:
[Buffer Overflow](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/test_exploits/buffer_overflow).

A buffer overflow is when a program writes outside of the bounds of an array or buffer, accidentally overwriting memory that it should not be accessing. This type of vulnerability can allow others to run any code that they would like.

##### String Format

An example of using printf to pass malicious string data:
[String Format](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/test_exploits/StringFormatVulnerability).

This type of vulnerability allows users to overwrite arbitrary locations in memory, enabling them to gain access to a shell.

#### Linux Exploit

##### Dirty Cow

A recent zero-day race condition for bypassing file permissions:
[Dirty C0W](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/test_exploits/dirty_cow).

This is a vulnerability for Linux kernels that existed on even the newest versions of Linux operating systems in 2016. It exploits a bug in a copy-on-write operation in order to overwrite a file that the user should not have access to.

#### Exploit Exercises

##### Nebula Exercises

A collection of exercises that we found at [exploit-exercises.com](https://exploit-exercises.com/nebula/) to be useful for learning about UNIX exploit techniques:

###### [Level 1](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level01.md)

In Level 1, we learn about exploiting code that uses `/usr/bin/env` and making the code exploit your script rather than the script it was attempting to execute.

###### [Level 2](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level02.md)

In Level 2, we learn about abusing environment variables to run arbitrary shell commands.

###### [Level 3](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level03.md)

In Level 3, we learn about creating a script that will be run by a crontab.

###### [Level 4](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level04.md)

In Level 4, we learn about using symlinks to get around a script that protects reading from a file by checking the filename.

###### [Level 5](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level05.md)

In Level 5, we learn about finding a backup that has weak permissions but contains a copy of the user's ssh keys.

###### [Level 6](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level06.md)

In Level 6, we learn about old Linux systems' password storage and using a password cracker to break into an account if we know the hash of the password.

###### [Level 7](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level07.md)

In Level 7, we learn about abusing the parameter of a Perl web server in order to run arbitrary commands.

###### [Level 8](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level08.md)

In Level 8, we learn about dumping a packet capture file in order to find a password.

###### [Level 9](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level09.md)

In Level 9, we learn about exploiting a vulnerable `preg_replace` call in PHP.

###### [Level 10](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level10.md)

In Level 10, we learn about swapping symlinks in order to exploit a time-to-check to time-to-use bug.

##### Protostar Exercises

A collection of exercises that we found at [exploit-exercises.com](https://exploit-exercises.com/protostar/) to be useful for learning about C exploit techniques:

[Stack 0](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/stack0.md)
[Stack 3](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/stack3.md)
[Stack 4](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/stack4.md)
[Stack 6](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/stack6.md)
[Format 0](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/format0.md)
[Heap 0](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/heap0.md)
[Heap 1](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/heap1.md)

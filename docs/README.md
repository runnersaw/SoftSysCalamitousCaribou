
## Software Systems Security Project

#### An investigation into computer security. This work was done by Deniz Celik, Sawyer Vaughan, and Chris Wallace as a part of our Software Systems class at Olin College in the spring of 2017.

### Goal

This project is an investigation into computer security, which includes research about general types of vulnerabilites present in Unix operating systems and C code as well as examples of specific vulnerabilites in modern operating systems. As a part of our investigation into these vulnerabilites, we have included exploitable code as well as instructions about how to exploit it and how to write your code to mitigate the vulnerability for several kinds of exploits.

### Computer Security

In the world where we all own many different interconnected devices of all shapes and sizes, an emphasis on computer security has become increasingly important. Just recently, we have been engaged in crucial debates about [privacy](https://en.wikipedia.org/wiki/FBI%E2%80%93Apple_encryption_dispute), we've seen [hacking to rig elections](https://www.nytimes.com/news-event/russian-election-hacking), and experienced [widespread vulnerabilites](http://heartbleed.com/) that leak [private and protected information](https://bugs.chromium.org/p/project-zero/issues/detail?id=1139). In this day and age, an emphasis on computer security is crucial.

We aimed to investigate types of general vulnerabilites that can be used by hackers, as well as learning about how software engineers can create code that is protected from these kinds of attacks.

In fitting with the focus of the class, the emphasis of vulnerabilites researched revolves around Unix and C vulnerabilites.

### Simple Exploit Demonstrations

A basic buffer overflow demonstration:
[Buffer Overflow](../Security/test_exploits/buffer_overflow)

An example of using printf to pass malicious string data:
[String Format](../Security/test_exploits/StringFormatVulnerability)

A recent zero-day race condition for bypassing file permissions:
[Dirty C0W](../Security/test_exploits/dirty_cow)

### Nebula Exercises

A collection of exercises that we found at [exploit-exercises.com](https://exploit-exercises.com/nebula/) to be useful for learning about UNIX exploit techniques:

[Level 1](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level01.md)
[Level 2](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level02.md)
[Level 3](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level03.md)
[Level 4](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level04.md)
[Level 5](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level05.md)
[Level 6](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level06.md)
[Level 7](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level07.md)
[Level 8](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level08.md)
[Level 9](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level09.md)
[Level 10](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/nebulaExploits/level10.md)

### Protostar Exercises

A collection of exercises that we found at [exploit-exercises.com](https://exploit-exercises.com/protostar/) to be useful for learning about C exploit techniques:


[Stack 0](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/stack0.md)
[Stack 3](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/stack3.md)
[Stack 4](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/stack4.md)
[Stack 6](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/stack6.md)
[Format 0](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/format0.md)
[Heap 0](https://github.com/runnersaw/SoftSysCalamitousCaribou/blob/master/Security/protostarExploits/heap0.md)

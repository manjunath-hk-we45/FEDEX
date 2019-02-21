# REVERSE ENGINEERING

### What is Reverse Engineering?

Reverse engineering is a process of disassembling a software package to understand its structure by analyzing its components, we can also duplicate the product by modifying the contents of the original package. This process helps you in understanding underlying program features and also if you know essentials of software programming, a duplicate of the same can also be created and some applications can even disclose embedded private or confidential data.

### What can we get out of it?

There are many tools available online to accomplish this process like OllyDBG, IDA,Hex-workshop and many more, but we need need to have skill to digest the raw data and put it in a understandable way.

we can get information from this process as follows:

* Assembly code, strings, functions and also libraries used by the application
* Monitoring application at run-time by using breakpoints and also we can get stack dump and analyze its contents by providing different inputs
* Editing binary files by using binary editors.
* exploring application and its resources and modifying its contents to make changes.
* we can extract sensitive information which are hard coded in the application during its development and can manipulate it further

### Tools that can HELP!

Reverse Engineering is all about tools and PATIENCE!!!, Tools we can look are:

#### **System Monitors** 

These tools will help you to get view of application from operating systems perspective as they can sniff, monitor and provide statistics of the application. some tools are

* CFF Explorer
* Win Hex
* PE Explorer
* SysInternals suite from Microsoft

#### **Disassembles** 

Powerful tool which can generate complete or part of assembly code for the given application. This process is processor/architecture specific. some tools are:

* IDA pro \(You can use Freeware IDA as it is available\)
* OllyDBG
* PE Explorer
* Binary Ninja
* GDB
* There are some online dis assemblers too
  * [https://retdec.com/](https://retdec.com/)
  * [https://onlinedisassembler.com/](https://onlinedisassembler.com/)






# THE PROCESS

## \*\*\*\*🎯 **How did we do it?**

In this section we will explain the approach we took to test a windows thick client application.

###  1⃣ Learning about Host - Network Scanning

      Initially we tried external testing of the machine, i.e., we considered Host \(application was installed and running on host during this process\) instead of the application, hence we used **NMAP** with some scripts so that we can see if any open ports are made available by the host or by an application which can act as our entry point to the host, but unfortunately none were. Then we tested the host with **Nessus** and **OpenVAS** for vulnerability but the host was hardened enough so we were not able to find any critical issues which we could have been used to exploit.

### 2⃣ Learning about Application - Static and Dynamic Analysis

      Here we checked the application \(.EXE file\) we used **OllyDBG, IDA Freeware** to disassemble the code and analyzed the code \(this was exhaustive process\) found an  interesting data in the application and also information about DLL files and dependencies.

### 3⃣ Manual traversal - Storage analysis/System testing

      We read the contents of the installed files and folders of the application and also checked for any information stored in temp folder and cache folder of the application, here we were able to get information of the applications log files communication logs and also application storage where it stored user data in a encrypted file. we were also able get the details about how application is identifying host and also its **RSA keys, also the JWT token**, it used to communicate with the server, which obviously we tampered to check for server responses, where we were able understand more about application internals and some fuzzing attacks to compromise the server using MITM attacks

### 4⃣ Compromising the host - Host Level

      We used KALI live USB and mounted the host HDD read the contents of the above mentioned folder and also used like **MIMIKATZ, Crunch and John Ripper** to get admin password and Finally, we were able to crack admin pass and logged into the host, which of course gave more privileges and we explored more as an administrator.

{% hint style="info" %}
Password cracking needs ample amount time and lots of word-list file, instead use Crunch if you want to generate your own
{% endhint %}

### 5⃣ Sniffing at Host level

      Sniffing at the host level for socket connection turned out to be very effective as we already had the admin privileges we used tools like **Microsoft message analyzer, Network monitor, Fiddler** to intercept communication which revealed all the communication unencrypted to us and also using Fiddler we performed MITM attacks by reproducing the requests for which we were able to get some info but server was already hardened enough.

### 6⃣ Getting Credentials

      After extensive checks, we uninstalled and reinstalled the application by keeping the intercept ON, Finally the application disclosed a user credential in one of the packets which it used to communicate with the server and we were able to get some information by using REST API calls, as the user has limited rights the only attack we were able devise on that is DOS.

### 7⃣ Final Attack - Subscriber to super user

      As the application, we tested was a subscriber based you officially cannot use the service for free, you have pay get subscribed and use it, but we explored the clients **GitHub repository** and were able get some working credentials!\(Information Disclosure\) which of course we used to make sure our attack impact grows and yes it worked for us we started using the service without paying.

      _FYI, we also did tests for the web application for the client and we were able to get privilege escalation on the application to superuser so now you can think how free subscriber can become superuser for some organization which he is not affiliated to._


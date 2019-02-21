# THICK CLIENT TESTING METHODOLOGY

### 1 Information Gathering and Reconnaissance

The first phase in a thick client application penetration test focuses on collecting as much information as possible about a target application. Reconnaissance, is one of the most critical steps of an application pen test. This is done through the use of public tools, scanners, sending simple HTTP requests, or specially crafted requests. As a result, it is possible to force the application to leak information, e.g., disclosing error messages or revealing the versions and technologies used.

### \*\*\*\*2 **Target Mapping**

The goal of mapping is to gain an understanding of the application from a typical user's perspective. And create the threat model and test cases based on the understanding of the application.

### 3 Vulnerability Discovery

It’s generally time to transition from mapping to discover after you’ve established your threat model and test cases, and conducted some initial functional analysis of the target. At this point you’re going to be looking to identify as many vulnerabilities in the target application as possible. 

### 4 Exploitation

Referring to the notes that you’ve taken during information gathering, mapping, and the discovery and dig as deep as possible into the vulnerabilities that you’ve discovered. During the exploitation process, you may traverse different \(higher\) levels of privilege within the target application.

### 5 Analysis and Reporting

Once you find the vulnerabilities reproduce and confirm the vulnerabilities and create the report by mentioning the OWASP name of the vulnerability, Description, affected host, affected layer, Severity, CVSS Score and remedy to fix those vulnerabilities.




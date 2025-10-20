# Vulnerability Scan Report
System Scanned – Metasploitable <br/>
### Objective
The vulnerability scan conducted was to identify potential security risk and provide a comprehensive, actionable report that highlight the security posture of scanned systems and networks, enabling the organization to prioritize and remediate identified security weaknesses. Enhancing the organization security standpoint and responsiveness.

### Skills Learned
- Vulnerability assessment and scanning.
- Risk analysis and prioritization.
- Remediation and reporting

### Tools Used
- Nessus vulnerability scanning tool (Version 10.8.3)

### Steps
Created an excutable scan file, with the system IP value (Metasploitable) <br/>
<img width="468" height="311" alt="image" src="https://github.com/user-attachments/assets/8d9f6293-08a7-4218-bda9-c424340489c9" />
Ref. Nessus Scan Report (Metasploitabe/ 10.0.2.15)
### Vulnerabilities Identified
Pandas DataFrame.query Code injection (Unpatched)	- Rating : (High)

Nodejs Node.js (Multiple Issues)			            - Rating : (High)

SSL Certificate Cannot Be Trusted			            - Rating : (Medium) <br/>
### Criticality Assessment
The severity of these identified vulnerabilities is high, and it requires immediate intervention.
A malicious attacker/black hat hacker could exploit these vulnerabilities. For example, the Python’s pandas library (DataFrame.query code) vulnerabilities could affect your company in several ways, in terms of data integrity (e.g., data annotation in production) and employee/user privacy through code injection attacks which can lead to loss of data integrity and compliance risks, code injection often result in the execution of arbitrary code which enables attackers to gain access to your data flow and security remote access to control authentication system.

Other identified vulnerabilities like JavaScript runtime due to unpatched Node.js and unverified SSL certificate can post as a security risk to any company. 
JavaScript runtime is an environment that allows JavaScript code to execute and Node.js is an entity that enables JavaScript to run on the server, typically company’s database or active directory. Unpatched Node.js could cause memory leak, and this happen when there is a gap in the network which causes the connection to break unexpectedly without warning, at this point company is already at security risk of allowing a malicious attacker to overload this system with DoS attack. 
By executing a Denial-of-Service (DoS) attack, an attacker can temporarily disable or completely shut down company’s network and disrupt business operations, and sometimes this kind attack can leverage this vulnerability as a diversion for more invasive cyber intrusions. 

Furthermore, an unverified SSL certificate could cause sensitive data leak, which could damage the company’s reputation.

### Suggested Fixes/Solutions
Python’s Pandas Library (DataFrame.query Code Injection) Solution –   There is no current fix for this vulnerability, but code can be modified for temporary fix to control vulnerability until there is a new release for fix. While wait, a warning has been added to the official package documentation to prevent arbitrary code from running like eval(). <br/>
Helpful tips:
https://pandas.pydata.org/docs/dev/reference/api/pandas.DataFrame.query.html#pandas.DataFrame.query 

Node.js Patches Solution –  Upgrade to Node.js version 18.20.6 / 20.18.2 / 22.13.1 / 23.6.1 or later for vulnerability patch. <br/>
Use this link –  https://nodejs.org/en/download to download Nodejs latest version.

SSL Certificate Solution – Purchase a verifiable certificates or generate a proper SSL certificate for the remote host.

<i>Steps on how to generate a proper SSL certificate:</i>
-	Choose the appropriate type (DV, OV, EV) based on your needs. Then, 
-	Select a trusted Certificate Authority (CA) e.g., Let's Encrypt, Entrust, GlobalSign or DigiCert. 
-	Generate a Certificate Signing Request (CSR) via your hosting control panel or  your server.
-	Submit it to the CA, and upon validation, install the issued certificate on your server. 
-	Finally, configure your web server to use HTTPS and verify the installation using online tools. 

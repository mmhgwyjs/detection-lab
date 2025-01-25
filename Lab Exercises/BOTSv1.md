# **Boss of the SOC Version 1**

https://bots.splunk.com/event/3oQ7sqI5bajOCP43o0svqT

---

## **Scenario 1: Website Defacement**

Alice's first task at Wayne Enterprises' Security Operations Center involves investigating a possible website defacement. The website, www.imreallynotbatman.com, hosted within Wayne Enterprises' IP address space, is suspected of being compromised by the Po1s0n1vy group. Lucius has asked Alice to confirm whether the website was compromised.

### **Resources**
- Splunk Server: [https://gettingstarted.splunk.show](https://gettingstarted.splunk.show)  
- Credentials: `user001-splk` / `Splunk.5`

### **Questions**

101. What is the likely IPv4 address of someone from the Po1s0n1vy group scanning imreallynotbatman.com for web application vulnerabilities?  
102. What company created the web vulnerability scanner used by Po1s0n1vy? Provide the company name.  
103. What content management system is imreallynotbatman.com likely using?  
104. What is the name of the file that defaced the imreallynotbatman.com website? Provide only the file name with its extension.  
105. This attack used dynamic DNS to resolve to the malicious IP. What fully qualified domain name (FQDN) is associated with this attack?  
106. What IPv4 address has Po1s0n1vy tied to domains pre-staged to attack Wayne Enterprises?  
107. (Question intentionally left blank in the source material.)  
108. What IPv4 address is likely attempting a brute force password attack against imreallynotbatman.com?  
109. What is the name of the executable uploaded by Po1s0n1vy?  
110. What is the MD5 hash of the executable uploaded?  
111. Provide the SHA256 hash of the custom malware used in Po1s0n1vy's phishing attacks, connected to their initial infrastructure.  
112. What special hex code is associated with the customized malware discussed in the previous question?  
113. (Question intentionally left blank in the source material.)  
114. What was the first brute force password attempted?  
115. What is the six-character Coldplay song that James Brodsky (a victim) is known to like, used in the brute force attack?  
116. What was the correct password for admin access to the CMS running imreallynotbatman.com?  
117. What was the average password length used during the brute force password attack?  
118. How many seconds elapsed between the time the correct password was identified and the compromised login occurred?  
119. How many unique passwords were attempted in the brute force attack?  

---

## **Scenario 2: Ransomware**

On her second day, Alice investigates a ransomware outbreak affecting Bob Smith's workstation, `we8105desk`. Bob plugged a USB drive he found in the parking lot into his workstation, triggering the ransomware attack. The incident resulted in encrypted files, altered desktop settings, and unusual behavior.

### **Resources**
- Splunk Server: [https://gettingstarted.splunk.show](https://gettingstarted.splunk.show)  
- Credentials: `user001-splk` / `Splunk.5`

### **Questions**

200. What was the most likely IPv4 address of `we8105desk` on 24AUG2016?  
201. Among the Suricata signatures that detected the Cerber malware, which one alerted the fewest number of times? Provide only the signature ID.  
202. What fully qualified domain name (FQDN) does the Cerber ransomware attempt to redirect users to after encryption?  
203. What was the first suspicious domain visited by `we8105desk` on 24AUG2016?  
204. During the initial Cerber infection, a VBScript is run. What is the length of the value of this script, pre-pended with the name of the launching `.exe`?  
205. What is the name of the USB drive inserted by Bob Smith?  
206. What is the IPv4 address of the file server connected to Bob's workstation during the ransomware outbreak?  
207. How many distinct PDFs were encrypted by the ransomware on the remote file server?  
208. What is the ParentProcessId of the VBScript that launches `121214.tmp`?  
209. How many `.txt` files in Bob Smith’s Windows profile were encrypted by the ransomware?  
210. What is the name of the file downloaded by the ransomware that contains the Cerber encryptor code?  
211. What obfuscation technique is likely used by the ransomware encryptor file?  

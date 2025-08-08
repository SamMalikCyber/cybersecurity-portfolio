# NIST CSF Incident Response Report

## Summary  
This morning, an intern contacted the IT department after being locked out of her internal network account. While she couldn’t log in, access logs showed that her credentials were still being used to access customer database records. She also reported receiving a suspicious email earlier in the day that asked her to visit an external site and sign in using her internal credentials.  

Shortly after, other employees noticed customer records missing or altered. Based on our initial investigation, it looks like someone gained unauthorized access and not only viewed sensitive data but deleted or changed parts of it.

---

## Identify  
The incident response team reviewed the systems, devices, and user permissions involved. We found that a malicious actor likely used the intern’s compromised credentials to access the customer database. Some customer data appears to have been deleted during the intrusion.

---

## Protect  
To avoid this kind of breach in the future, the team has already rolled out stronger login security. This includes multi-factor authentication (MFA), a limit of three login attempts, and new employee training on how to keep credentials safe. We’re also reconfiguring our firewall and adding an intrusion prevention system (IPS) for extra protection.

---

## Detect  
To improve how we catch unauthorized access moving forward, we’re enabling stronger firewall logging and deploying an intrusion detection system (IDS) to keep a close eye on any suspicious traffic from the internet.

---

## Respond  
The intern’s account was disabled right away. All interns and employees have been given a quick refresher on credential safety and phishing awareness. Upper management is now preparing customer notifications about the incident and will also follow required legal steps, including reporting the breach to relevant authorities.

---

## Recover  
The database will be restored using a full backup from last night. Staff have been informed that any customer updates from this morning will need to be manually re-entered once the backup is complete. We're prioritizing accuracy during this step to make sure no legitimate data is lost.

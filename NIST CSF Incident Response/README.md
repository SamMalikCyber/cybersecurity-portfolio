# NIST CSF Incident Response

This project focuses on using the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF) to analyze and respond to a simulated Distributed Denial of Service (DDoS) attack.  

I walked through each NIST CSF function — Identify, Protect, Detect, Respond, and Recover to break down the event and propose steps to improve network security. This was a practical way for me to focus on structured response strategies and how they support an organization's resilience during security incidents.

---

## Scenario

You are a cybersecurity analyst working for a multimedia company that offers web design services, graphic design, and social media marketing solutions to small businesses. Your organization recently experienced a DDoS attack, which compromised the internal network for two hours until it was resolved.

During the attack, your organization’s network services suddenly stopped responding due to an incoming flood of ICMP packets. Normal internal network traffic could not access any network resources. The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services offline, and restoring critical network services.

The company’s cybersecurity team then investigated the security event. They found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a distributed denial of service (DDoS) attack.

To address this security event, the network security team implemented:

- A new firewall rule to limit the rate of incoming ICMP packets  
- Source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets  
- Network monitoring software to detect abnormal traffic patterns  
- An IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics

As a cybersecurity analyst, you are tasked with using this security event to create a plan to improve your company’s network security using the NIST CSF.

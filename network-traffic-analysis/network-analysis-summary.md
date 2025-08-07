# Cybersecurity Incident Report  
**Network Traffic Analysis**

---

## Part 1: Summary of the problem found in the DNS and ICMP traffic log

The UDP protocol was used to contact the DNS server to retrieve the IP address for the domain name **yummyrecipesforme.com**. Using the network analysis tool **tcpdump**, we observed that an ICMP error message, _“udp port 53 unreachable,”_ was returned. Since port 53 is commonly used for DNS traffic, this points to the DNS server being either down or unreachable.

---

## Part 2: Analysis and cause of the incident

The incident occurred at **1:24 p.m.** Customers contacted the organization to report that they were unable to access the website and received the message _“destination port unreachable.”_ The network team began investigating the issue to restore access.  

Our investigation confirmed that **DNS port 53 was unreachable** during the time of the incident. This could be due to the DNS server being taken offline or blocked. The most likely causes include a **firewall misconfiguration** or a **Denial of Service (DoS) attack** against the DNS server.

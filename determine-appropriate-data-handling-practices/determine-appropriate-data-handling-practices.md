# Determine Appropriate Data Handling Practices

## Project Description
In this project, I reviewed a data leak incident and assessed how the principle of least privilege could have prevented it. I analyzed what led to the leak, summarized NIST SP 800-53 AC-6, and suggested improvements for data handling to avoid similar issues in the future. This activity helped me think about how role-based access and regular permission audits can make a big difference in preventing accidental data exposure.

---

## Incident Analysis
The leak happened when a sales manager shared a folder of internal documents with their team during a meeting. The folder had sensitive materials for a product launch, along with customer analytics. After the meeting, the manager didn’t revoke access, and later, a sales rep accidentally shared the folder link (instead of just the promotional materials) with a business partner. The partner posted it on social media, thinking it was okay to share, and the role I play in analyzing these incidents to make appropriate suggestions to higher ups.

Key issues: access was broader than necessary, and link-sharing wasn’t restricted.

---

## NIST SP 800-53: AC-6 (Least Privilege)
NIST SP 800-53 AC-6 is about giving people the least amount of access they need to do their job, and nothing more. It recommends keeping privileges tightly controlled, limiting them by role, automatically revoking them when no longer needed, logging account activity, and doing regular audits. The goal is to stop people from having unnecessary access that could lead to mistakes or security issues.

---

## Recommendations
| Risk | Recommendation | Benefit |
|------|----------------|---------|
| Sensitive files accessible to too many employees | Restrict access to sensitive resources based on user role | Only authorized employees can view or share confidential information |
| Permissions remain even after no longer needed | Regularly audit user privileges | Ensures access stays appropriate and reduces the chance of accidental leaks |

---

## Justification
By limiting access to sensitive files and reviewing permissions regularly, the risk of accidentally sharing confidential data drops significantly. This ensures employees only have what they truly need to work, and if something is shared by mistake, fewer people will have the chance to leak it further.

---

## Summary
I analyzed the factors that caused a real-world style data leak, applied NIST SP 800-53 AC-6 to identify gaps in access controls, and proposed two targeted control enhancements to strengthen least privilege. By combining role-based access control with scheduled permission audits, I created a plan that reduces the likelihood of similar incidents in the future and improves the company’s overall data handling practices.

---

## Skills Demonstrated
- Understanding and applying the principle of least privilege  
- Reviewing and analyzing incident reports  
- Using NIST SP 800-53 controls for practical recommendations  
- Identifying security gaps and proposing solutions

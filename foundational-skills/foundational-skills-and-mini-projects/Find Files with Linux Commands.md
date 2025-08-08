# Find Files with Linux Commands

In this mini project, I used foundational Linux shell commands to navigate directories, locate files, and read their contents all from the command line. These are everyday tasks in security environments, especially when investigating incidents or managing systems without a GUI.

---

### 🛠️ Tools Used

- Bash shell (Debian-based Linux environment)

---

### 🧪 Commands Practiced & Examples

```bash
pwd
# Output:
# /home/analyst

ls
# Output:
# logs  projects  reports  temp

cd reports
ls
# Output:
# users

cd users
ls
cat Q1_added_users.txt
# Example Output:
# username: aezra | department: Human Resources
# username: mreed | employee_id: 1104 | department: Information Technology

cd /home/analyst/logs
ls
# Output:
# server_logs.txt

head server_logs.txt
# Shows the first 10 lines, including:
# WARNING: Disk usage at 85%
# WARNING: CPU usage high

### Summary

This mini project helped me build confidence navigating the Linux file system using commands like `pwd`, `ls`, `cd`, `cat`, and `head`, which is one of my weaknesses as of right now. These tools are essential for investigating files, logs, and user activity without relying on a graphical interface.

This is the kind of fundamental skill that I think becomes second nature over time and supports a lot of more advanced cybersecurity work.

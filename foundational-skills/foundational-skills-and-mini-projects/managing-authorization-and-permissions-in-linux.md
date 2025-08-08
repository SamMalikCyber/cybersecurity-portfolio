# Managing Authorization and Permissions in Linux

This mini project focuses on how I used Linux commands to review and set permissions for files and directories, a critical part of securing systems and managing access as a security analyst.

---

### Tools Used

- Bash shell (Debian-based Linux VM)
- `ls`, `chmod`, `cd`

---

### Commands Practiced and Their Output

```bash
# Navigate to the projects directory
cd projects

# List files and their permissions
ls -l

# Show all files (including hidden) and their permissions
ls -la

# Remove 'write' permission for 'others' on a file
chmod o-w project_k.txt

# Remove 'read' permission for 'group' on a file
chmod g-r project_m.txt

# Remove write for user and group, add read for group, on a hidden file
chmod u-w,g-w,g+r .project_x.txt

# Remove execute permission for group on a directory
chmod g-x drafts

---

Summary

This task helped me get hands-on with reviewing and changing file and directory permissions in Linux. Managing authorization like this is a mundane but vital part of protecting sensitive data and ensuring only the right people have access. These practical steps are building my comfort and reliability with Linux system security, especially since IAM is a domain that interests me.

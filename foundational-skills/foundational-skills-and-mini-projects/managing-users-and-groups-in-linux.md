# Managing Users and Groups in Linux

This mini project demonstrates how I used Linux Bash commands to add and manage users, assign permissions, and clean up groups—basic but critical skills for system administration and strengthening security.

---

### Tools Used

- Bash shell (Debian-based Linux VM)
- `sudo`, `useradd`, `usermod`, `chown`, `userdel`, `groupdel`

---

### Commands Practiced and Their Output

```bash
# Add a new user
sudo useradd researcher9

# Add user to research_team group as primary
sudo usermod -g research_team researcher9
# (Or both at once)
sudo useradd researcher9 -g research_team

# Assign ownership of a file
sudo chown researcher9 /home/researcher2/projects/project_r.txt

# Add user to a secondary group (sales_team)
sudo usermod -a -G sales_team researcher9

# Delete the user
sudo userdel researcher9

# Remove the user's default group
sudo groupdel researcher9

---

Summary:

This task gave me direct experience managing Linux users and groups, adding and removing accounts, assigning group memberships, and managing file ownership. These are skills I’ll need to be comfortable with as a security analyst, especially in environments where user access and group permissions need to be tightly controlled in a real world organization.

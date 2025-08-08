# Manage Files with Linux Commands

This mini project shows how I used core Linux commands to create, remove, and move directories and files, as well as edit a text file using `nano`. Organizing files is a fundamental part of working securely and efficiently on Linux systems.

---

### Tools Used

- Bash shell (Debian-based Linux VM)
- `mkdir`, `ls`, `rmdir`, `cd`, `mv`, `rm`, `touch`, `nano`, `cat`, `clear`

---

### Commands Practiced and Their Output

```bash
# Create a new logs directory
mkdir logs

# Confirm the new logs directory
ls
# Output: logs notes reports temp

# Remove the temp directory
rmdir temp

# Confirm temp is gone
ls
# Output: logs notes reports

# Move Q3patches.txt from notes to reports
cd notes
mv Q3patches.txt /home/analyst/reports/

# Confirm all three quarterly patch files in reports
ls /home/analyst/reports
# Output: Q1patches.txt Q2patches.txt Q3patches.txt

# Remove the unused tempnotes.txt file
rm tempnotes.txt
ls
# Output: (shows remaining files in notes)

# Create an empty tasks.txt file
touch tasks.txt
ls
# Output: tasks.txt

# Edit tasks.txt in nano and add:
# Completed tasks
# 1. Managed file structure in /home/analyst

nano tasks.txt

# (Exit nano, saving changes)

# View the file to confirm contents
cat tasks.txt
# Output:
# Completed tasks
# 1. Managed file structure in /home/analyst

# Clear the terminal
clear

---

Summary:

This project let me practice more hands-on file and directory management in Linux, including creating, moving, and deleting files and folders. I also worked on editing text files with nano. These are more basic but critical skills for managing and securing information in any Unix-based environment, and I’m getting more comfortable using them through direct practice.

# Filter with grep

This mini project highlights how I used the `grep` command and piping in the Linux shell to search through logs and filter specific lines or filenames. These are essential skills when reviewing large sets of logs or directories during an investigation.

---

### Tools Used

- Bash shell (Debian-based Linux VM)
- `grep`, `ls`, `cd`
- Piping (`|`)

---

### Commands Practiced and Their Output

```bash
# Navigate to the logs directory
cd logs

# Find all lines containing 'error' in a log file
grep error server_logs.txt
# Output: 6 lines containing the word "error"

# Navigate to the users directory
cd /home/analyst/reports/users

# List only files containing "Q1"
ls | grep Q1
# Output: 3 files containing "Q1"

# List only files containing "access"
ls | grep access
# Output: 4 files containing "access"

# Search for a specific username in a file
grep jhill Q2_deleted_users.txt
# Output: Line with user jhill from the deleted users file

# Search for users added to the HR department
grep "Human Resources" Q4_added_users.txt

---

Summary:

This mini project gave me more hands-on practice using the `grep` command and piping to isolate specific pieces of information from larger files and directories. These skills are important for efficiently navigating logs, investigating alerts, and filtering useful details without a GUI. Being comfortable with this kind of command-line work is something I’m steadily improving as I prepare for real-world analysis tasks.


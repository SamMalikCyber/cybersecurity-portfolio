# Getting Help in the Linux Command Line

This mini project shows how I used built-in Linux tools to quickly find help and information about commands, something every analyst needs when working in the terminal.

---

### Tools Used

- Bash shell (Debian-based Linux VM)
- `whatis`, `man`, `apropos`

---

### Commands Practiced and Their Output

```bash
# Get a short description of a command
whatis cat
# Output: cat (1) - concatenate files and print on the standard output

# Read the manual page for a command
man cat
# Found option: -n, --number  # (number all output lines)

# Search for commands based on keywords
apropos -a first part file
# Output: head (1) - output the first part of files

# Get help on useradd and find the expiration date option
man useradd
# Option found: -e (set account expiration date)

# Quick difference between rm and rmdir
whatis rm
# Output: rm (1) - remove files or directories
whatis rmdir
# Output: rmdir (1) - remove empty directories

# Search for the command to create a new group
apropos -a create new group
# Output: groupadd (8) - create a new group

---

Summary

This exercise helped me get comfortable using man, whatis, and apropos to look up command details and options in real time. Knowing how to quickly find answers directly in the shell is key for troubleshooting and learning more things on the job, especially when dealing with new tools or unfamiliar tasks.

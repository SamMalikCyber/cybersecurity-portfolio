# Use Linux Commands to Manage File Permissions

## Project Description
The research team at my organization needed to update file and directory permissions in the `projects` directory. Current settings didn’t match the intended level of authorization, which could allow unnecessary or risky access. My goal was to check existing permissions, compare them against what should be in place, and make changes so the right people had the right level of access.

---

## Check File and Directory Details
Ran:

```bash
ls -la
```

This lists all files, including hidden ones, with their permissions, owners, and other details.  
Found:
- One directory: `drafts`
- Hidden file: `.project_x.txt`
- Several project files

These results gave me a clear view of what permissions each file and directory currently had.

![Listing of projects directory](./images/ls-la-projects.png)

---

## Describe the Permissions String
Each entry starts with a 10-character permissions string:
1. File type (`d` = directory, `-` = regular file)  
2–4. User permissions  
5–7. Group permissions  
8–10. Others permissions  

Example: `-rw-rw-r--` means it’s a file, user and group can read/write, others can read only.

---

## Change File Permissions
Policy is that “others” should never have write access.  
Found `project_k.txt` allowed it, so I removed it:

```bash
chmod o-w project_k.txt
ls -la
```

![Removing write from others](./images/chmod-o-w.png)

---

## Change File Permissions on a Hidden File
`.project_x.txt` is archived, so it should be read-only for user and group, with group explicitly granted read access.

```bash
chmod u-w,g-w,g+r .project_x.txt
ls -la
```

![Hidden file permission changes](./images/chmod-hidden-file.png)

---

## Change Directory Permissions
Only `researcher2` should be able to access the `drafts` directory. Group had execute permission, so I removed it:

```bash
chmod g-x drafts
ls -la
```

Execute permission on a directory allows a user to enter it, so removing it for group prevents access.

![Directory permission change](./images/chmod-dir.png)

---

## Summary
Using `ls -la` to check permissions first, I:
- Removed write for “others” on `project_k.txt`
- Made `.project_x.txt` read-only for user/group, added group read
- Removed group execute on `drafts`

These changes aligned the system with least privilege principles and reduced unnecessary access for the research team’s files.

# 🔐 File & Directory Permission Management with chmod

## Scenario
I reviewed and corrected file and directory permissions in a shared Linux project directory to enforce the principle of least privilege and prevent unauthorized access.

## Objectives
- Inspect file and directory permissions
- Identify over-permissive access
- Modify permissions using chmod
- Secure hidden files and directories

## Tools
ls, chmod, Bash

## Environment
/home/researcher2/projects

## Task 1 🟦 Permission Inspection
```bash
cd projects
ls -l
ls -la
Result:

Files are owned by user researcher2

Group owner is research_team

A hidden file (.project_x.txt) exists

Multiple files and a directory have excessive permissions

Task 2 🟦 File Permission Hardening
bash
Copy code
chmod o-w project_k.txt
chmod g-r project_m.txt
Results:

Removed write access for other users on project_k.txt

Restricted group access on sensitive file project_m.txt

Task 3 🟦 Hidden File Permission Correction
bash
Copy code
chmod u=r,g=r,o= .project_x.txt
ls -l .project_x.txt
Results:

Hidden file set to read-only for user and group

All write permissions removed

Final permissions: -r--r-----

Task 4 🟦 Directory Permission Restriction
bash
Copy code
chmod g-x drafts
Results:

Removed group execute permission from drafts

Only the file owner can access the directory and its contents

Conclusion
This lab demonstrates practical experience auditing and hardening Linux file and directory permissions. By inspecting access levels and applying precise permission changes, I enforced least privilege using standard Linux CLI tools relevant to SOC and security operations.
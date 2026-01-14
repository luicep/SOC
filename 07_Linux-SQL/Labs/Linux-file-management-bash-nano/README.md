Linux File & Directory Management (Bash + nano)
Scenario

I reorganized /home/analyst by creating/removing directories, moving/deleting files, and documenting changes in a text file using nano.

Objectives

Create logs/

Remove temp/

Move Q3patches.txt into reports/

Delete tempnotes.txt

Create and edit tasks.txt

Tools

ls, mkdir, rmdir, rm, mv, touch, nano, cat, Bash

Environment

/home/analyst

Task 1 🟦 Create logs directory
cd /home/analyst
mkdir logs
ls

Task 2 🟦 Remove temp directory
rmdir /home/analyst/temp
ls /home/analyst

Task 3 🟦 Move Q3 patch file
cd /home/analyst/notes
mv Q3patches.txt /home/analyst/reports/
ls /home/analyst/reports

Task 4 🟦 Remove unused file
rm /home/analyst/notes/tempnotes.txt
ls /home/analyst/notes

Task 5 🟦 Create tasks.txt
touch /home/analyst/notes/tasks.txt
ls /home/analyst/notes

Task 6 🟦 Edit tasks.txt using nano
nano /home/analyst/notes/tasks.txt


Added:

Completed tasks
1. Managed file structure in /home/analyst


Verify:

clear
cat /home/analyst/notes/tasks.txt

Conclusion

This lab demonstrates core Linux file management skills used in SOC workflows: organizing directories, maintaining reporting files, and documenting actions using CLI tools.
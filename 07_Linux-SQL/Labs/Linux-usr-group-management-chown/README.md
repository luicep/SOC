🔐 LAB: User & Group Management + Ownership Control (Linux)
Scenario

A new employee joined the Research department and needed access configured correctly. I created the user, assigned proper group memberships, transferred ownership of a project file, then removed the user after they left the organization.

Objectives

Create a new user (researcher9)

Assign correct primary group (research_team)

Transfer file ownership (project_r.txt)

Add secondary group membership (sales_team)

Remove user and clean up leftover group

Tools

useradd, usermod, chown, userdel, groupdel, id, groups

Environment

Linux Bash shell

Task 1 🟦 Add a new user + set primary group
sudo useradd researcher9
sudo usermod -g research_team researcher9

Task 2 🟦 Assign file ownership
sudo chown researcher9 /home/researcher2/projects/project_r.txt

Task 3 🟦 Add secondary group membership
sudo usermod -aG sales_team researcher9

Task 4 🟦 Delete user + cleanup group
sudo userdel researcher9
sudo groupdel researcher9

Conclusion

This lab demonstrates foundational Linux identity and access management (IAM): provisioning users, managing primary vs secondary groups, controlling resource ownership, and applying proper offboarding cleanup.
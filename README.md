# 🐧 Linux Lab: File Permissions & User Management

## 📌 Purpose
This lab demonstrates how to create files, manage directories, and modify permissions in Linux. It also includes an optional step to add a user account. These are essential skills for system administrators and cybersecurity professionals.

---

## 🛠 Steps to Complete

```bash
# Step 1: Create a project directory and move into it
mkdir linux-permissions-lab
cd linux-permissions-lab

# Step 2: Create sample files and a directory
echo "This is a test file." > file1.txt
echo "Confidential log file." > file2.txt
mkdir logs

# Step 3: View default permissions
ls -l

# Step 4: Modify permissions
chmod 444 file1.txt    # make file1.txt read-only for all users
chmod u+x file2.txt    # give the owner execute permission on file2.txt
chmod 700 logs         # restrict logs directory to the owner only

# Step 5 (Optional): Add a test user
sudo useradd testuser
tail -n 1 /etc/passwd   # verify the new user was added

## Sample Output

ls -l
-r--r--r-- 1 user user  20 Sep 30 18:01 file1.txt
-rwxr--r-- 1 user user  24 Sep 30 18:01 file2.txt
drwx------ 2 user user  40 Sep 30 18:01 logs


## 🎯 Learning Outcomes

Created and organized files and directories
Interpreted Linux permission strings (r, w, x)
Modified file and directory permissions using chmod
Added a user account using useradd













# 🧰 Basic Linux Commands

📁 File: basic

# 🧰 Basic Linux Commands

This section covers foundational commands for navigating the file system, handling files/directories, managing permissions, and basic system usage.

---

## 📂 Navigation & Directory Handling

```bash
pwd                        # Show current directory
ls                         # List files in current directory
ls -la                     # List all files with detailed info
cd /path/to/directory      # Change to a specific directory
cd ~                       # Change to home directory
cd ..                      # Move one level up
cd -                       # Switch to previous directory

📁 Files & Directories

touch file.txt             # Create an empty file
mkdir new_folder           # Create a new directory
mkdir -p folder1/folder2   # Create nested directories
cp file.txt backup.txt     # Copy file
mv oldname.txt newname.txt # Rename or move file
rm file.txt                # Delete file
rm -r folder/              # Delete folder and contents

🛡️ File Permissions

chmod +x script.sh         # Make a script executable
chmod 755 file.sh          # Set rwxr-xr-x permissions
chown user:user file.txt   # Change file ownership
ls -l                      # View permissions

🧑‍💻 Users & Groups

whoami                     # Show current user
id                         # Display user ID and group info
adduser newuser            # Add new user (Debian/Ubuntu)
useradd -m newuser         # Add user (RHEL/CentOS)
passwd newuser             # Set password
deluser newuser            # Delete user
groupadd devs              # Create a new group
usermod -aG devs user1     # Add user to group

🧮 File Viewing & Editing

cat file.txt               # View contents of a file
less file.txt              # View large files, scrollable
head -n 10 file.txt        # Show first 10 lines
tail -n 20 file.txt        # Show last 20 lines
nano file.txt              # Open file in Nano editor
vi file.txt                # Open file in Vi editor

🧰 Misc Utilities

clear                      # Clear the terminal
history                    # Show command history
date                       # Display current date/time
cal                        # Display calendar
uptime                     # Show system uptime
df -h                      # Show disk space usage
du -sh folder/             # Show folder size

✅ Tip: Use man <command> to see the manual/help for any command.

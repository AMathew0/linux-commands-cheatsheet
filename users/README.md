# 👥 Linux User & Group Management

This section covers commands to create, modify, and manage users and groups in Linux systems — essential for access control and permission management.

---

## 🧑 User Management

```bash
adduser john                 # Add new user (interactive)
useradd -m alice             # Add user with home directory
passwd john                 # Set or change user password
usermod -aG sudo alice       # Add user to 'sudo' group
deluser mike                 # Delete user

👨‍👩‍👧‍👦 Group Management

groupadd devs               # Create a new group
groupdel devs               # Delete a group
gpasswd -a john devs         # Add user to group
gpasswd -d john devs         # Remove user from group
groups john                  # Show groups a user belongs to

🔁 Switch Users

su - john                    # Switch to user account
exit                         # Exit user session

📂 File Ownership & Permissions

chown john:devs file.txt     # Change file owner and group
chmod 755 script.sh          # Set read/write/execute permissions
chmod +x backup.sh           # Make script executable

🧾 View and List

whoami                       # Current logged-in user
id john                      # UID, GID, and groups
getent passwd                # List all system users
getent group                 # List all groups

🔒 Lock/Unlock Accounts
bash
Copy
Edit
passwd -l alice              # Lock user account
passwd -u alice              # Unlock user account

💡 Use groups to simplify permission management. Always test permissions before applying them in production.
